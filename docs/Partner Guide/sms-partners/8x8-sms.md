---
title: 8x8
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

[8x8](https://www.8x8.com/) is a global cloud communications platform that provides enterprise-grade SMS and Chat messaging services. Integrating 8x8 with CleverTap allows you to send real-time marketing and transactional messages across channels using CleverTap’s unified engagement dashboard.

This integration supports HTTP-based SMS delivery, dynamic parameter mapping, and event-based message triggering.

Here’s how businesses use 8x8 with CleverTap:

* *Send OTPs and Notifications*: Trigger real-time messages from mobile/web events.
* *Promote Offers and Campaigns*: Reach targeted users with SMS powered by event segmentation.
* *Enhance Chat App Messaging*: Expand your channel strategy with multi-mode engagement.

# Prerequisites for Integration

To integrate 8x8 with CleverTap, ensure the following:

* You must have an active 8x8 account with access to your Subaccount ID and API Key.
* Your sender ID or virtual number must be provisioned in your 8x8 account.
* You must have a CleverTap account with SMS setup enabled.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by 8x8. The CleverTap and 8x8 integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [8x8](https://www.8x8.com/services/support) for support and resolution.

# Integrate 8x8 with CleverTap

To integrate 8x8 with CleverTap, follow these three steps:

1. [Find 8x8 API Credentials](doc:8x8-sms#find-8x8-api-credentials)
2. [Set Up CleverTap Dashboard](doc:8x8-sms#set-up-clevertap-dashboard)
3. [Send a Test SMS](doc:8x8-sms#send-a-test-sms)

## Find 8x8 API Credentials

To complete the setup, gather the following details from your 8x8 Customer Portal:

* Subaccount ID: Required for the API endpoint URL.
* API Key: Used in the `Authorization` header.
* Sender ID / Virtual Number: Required as the source in the payload.

You can find all these under API Keys in your [8x8 Customer Portal Dashboard](https://connect.8x8.com/login).

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate the 8x8 SMS provider. To configure the CleverTap dashboard:

1. Go to *Settings* > *Engage* > *Channels* > *SMS* in the CleverTap dashboard.
2. Click **+ Add Provider**. The Add SMS provider page opens.

<Image alt="Add Provider" align="center" width="65% " border={true} src="https://files.readme.io/8ca98feff96deb7a4d4b6c4a0576f0b108f3d696f98dfbaa9b61faca58641cf2-image.png">
  Add Provider
</Image>

3. Under **Provider**, select *Other (Generic)* and enter the following details:

<Table>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter the nickname of the SMS provider to identify it uniquely. For example:`8x8_SMS`
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        Enter this URL in the 8x8 platform to receive delivery status updates for your SMS messages. Refer to [Set Up SMS Callbacks](doc:8x8-sms#set-up-sms-callbacks). This callback URL must be passed to 8x8 as part of the JSON payload in the Parameters section.
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Select `POST`
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Paste the URL`<https://sms.8x8.com/api/v1/subaccounts/{subAccountId}/partners/clevertap/batch>`\
        Replace `{subAccountId}` with your actual Subaccount ID from 8x8.\
        Ensure that the URL is in HTTPS format, that is, your URL must begin with `https://.`
      </td>
    </tr>

    <tr>
      <td>
        Authentication
      </td>

      <td>
        Select `No Authentication`.
      </td>
    </tr>
  </tbody>
</Table>

<Image alt="Provider Configuration" align="center" width="65% " border={true} src="https://files.readme.io/4146d54984627248ea4affc5b1646c2ea54b45ea7119d1bbc306f6a2b0d114f2-image.png">
  Provider Configuration
</Image>

4. Enter the following details under the *Headers* section.

| Key           | Value              |
| ------------- | ------------------ |
| Authorization | `Bearer <API_KEY>` |
| Content-Type  | `application/json` |

<Image alt="Set Headers" align="center" width="65% " border={true} src="https://files.readme.io/2d150958aebb2dd35c5b3971d8cca19650dd768e4b387c106c726777c9adfb2e-image.png">
  Set Headers
</Image>

5. Under *Parameters*, select `JSON` as the request type for the POST request.\
   Refer to the sample payload below for the expected structure.

#### Sample Payload Structure (JSON):

```json
{
  "msgs": [
    {
  "source": "<Your Sender ID or Virtual Number>", // Must be a valid sender ID or number registered in your 8x8 account.
  "destination": "$$To",
  "text": "$$Body",
  "mid": "$$MessageID",
  "encoding": "Auto",
  "partnerCallbackUrl": <Delivery Report Callback URL HERE>
    }
  ]
}
```

<Image alt="Set Parameters" align="center" width="65% " border={true} src="https://files.readme.io/c62c38c39734da3f06ba4a19e9e9aee54b5bb02f45cc7c843e383ce6498cf2f9-8x8_3.png">
  Set Parameters
</Image>

6. Select the Batch checkbox and fill in the details as required.

> 📘 Single Batch Limit
>
> A single batch can have a maximum of 1,000 records.

7. Click on **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:8x8-sms#send-a-test-sms).

## Send a Test SMS

Sending a test SMS helps confirm that your 8x8 integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To validate your configuration:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   * *Country Code and Mobile Number*: Enter the country code and mobile number to which you want to send the message.
   * *Message*: Enter sample text, such as `This is a test message powered by 8x8`

<Image alt="Send a Test SMS" align="center" width="65% " border={true} src="https://files.readme.io/4141da97af121d16805772fb980f0888272958269467d79efd1a0a9f5f7c7dab-image.png">
  Send a Test SMS
</Image>

3. Click **Send Test**.

If the configuration is correct, the test message will be delivered, and 8x8 will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from CleverTap and add it in the JSON payload

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider\
   Setup page *Settings* > *Channels* > *SMS* > *Provider Nickname*
2. Add it in the JSON payload

<Image alt="Set Up SMS Callbacks" align="center" width="65% " border={true} src="https://files.readme.io/27be1e248b9101270026cf9be1bc09c56248d3f3b3c6cbbb4feef98e3bb6c85f-image.png">
  Set Up SMS Callbacks
</Image>

### Verifying Successful Integration

Your integration is considered successful when the following criteria are met:

* The test SMS is delivered to the intended mobile number.
* You receive a DLR (Delivery Report) callback from 8x8 at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
* CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using 8x8 as your SMS provider.
