---
title: Kaleyra
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

[Kaleyra](https://www.kaleyra.com/) is a Communications Platform as a Service (CPaaS) provider that helps businesses send and receive SMS messages across global markets.

By integrating Kaleyra with CleverTap, you can manage SMS campaigns directly from the CleverTap dashboard, alongside other engagement channels. This integration supports message delivery and DLR (Delivery Report) tracking, allowing you to run personalized, targeted SMS campaigns as part of your omnichannel strategy.

Here are a few ways businesses use Kaleyra with CleverTap:

* *Transactional Alerts*: Deliver real-time OTPs, order confirmations, and payment updates.
* *Promotional Campaigns*: Announce offers, discounts, or product launches to targeted user segments.
* *Abandoned Cart Reminders*: Prompt users to complete their purchase with time-sensitive nudges.

Integrate CleverTap’s segmentation engine with Kaleyra SMS to trigger context-aware messages and increase engagement.

# Prerequisites for Integration

To integrate ICS with CleverTap, check the following:

* You must have an active Kaleyra account with API access.
* You must obtain the HTTP Endpoint, API Key, SID, and Kaleyra host URL from [Kaleyra support](https://www.kaleyra.com/contact-us/).
* You must have a CleverTap account with SMS setup enabled.
* If your account is based in India, ensure your message templates and sender IDs are registered with DLT.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Kaleyra. The CleverTap and Kaleyra integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Kaleyra](https://developers.kaleyra.io/docs/support) for support and resolution.

# Integrate Kaleyra with CleverTap

The integration includes three major steps:

1. [Find Kaleyra API Credentials](doc:kaleyra-sms#find-kaleyra-api-credentials)
2. [Set Up CleverTap Dashboard](doc:kaleyra-sms#set-up-clevertap-dashboard)
3. [Send a Test SMS](doc:kaleyra-sms#send-a-test-sms)

## Find Kaleyra API Credentials

To complete the setup, gather the following details from your Kaleyra account or Kaleyra support:

* [API Key](https://developers.kaleyra.io/docs/view-api-key-and-sid): Found under **API Settings** in your Kaleyra Customer Portal. Used in the `api-key` header.
* [SID](https://developers.kaleyra.io/docs/view-api-key-and-sid): Sender ID linked to your Kaleyra account. Used in the `sid` header.
* API Host Domain: The base URL used to send requests. Set this in the `kaleyra-host` header.

For more information on locating Kaleyra API credentials, refer to [View API Key and SID](https://developers.kaleyra.io/docs/view-api-key-and-sid)

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate your Kaleyra SMS provider. To configure the CleverTap dashboard:

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
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter the nickname of the SMS provider to identify it uniquely. For example:`Kaleyra_SMS`
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        Enter this URL in the Kaleyra platform to receive delivery status updates for your SMS messages. Refer to [Set Up SMS Callbacks](doc:kaleyra-sms#set-up-sms-callbacks).
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Select`POST`
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Paste the URL received from Kaleyra team.\
        Ensure that the URL is in HTTPS format, that is, your URL must begin with `https://`.
      </td>
    </tr>

    <tr>
      <td>
        Authentication
      </td>

      <td>
        Under Authentication, select one of the following options:  

        * No Authentication.
        * Basic Authentication: Enter the username and password.
      </td>
    </tr>
  </tbody>
</Table>

4. Under *Headers*, enter the following Key/Value pair.

| Key            | Value                   |
| -------------- | ----------------------- |
| `api-key`      | API Key from Kaleyra    |
| `sid`          | SID from Kaleyra        |
| `kaleyra-host` | API domain from Kaleyra |
| `callback_url` | CleverTap callback URL  |

<Image alt="Provider Configuration" align="center" width="60% " border={true} src="https://files.readme.io/5eb83c696b3e71eb60c613dd5c9453ae41865a13744db421c9f601f1f193dc17-image.png">
  Provider Configuration
</Image>

5. In the *Parameters* tab, set the *Type* to `x-www-form-urlencoded`. Enter the following as a Key/Value pair:
6. Under the *Parameters* tab:
   * Set *Type* to `x-www-form-urlencoded`
   * Add the following key-value pairs:

| Key           | Value          | Description                                                    | Required |
| ------------- | -------------- | -------------------------------------------------------------- | -------- |
| `to`          | `$$To`         | Recipient’s phone number                                       | Yes      |
| `sender`      | `$$Sender`     | Sender ID (dynamic if mapped)                                  | Yes      |
| `body`        | `$$Body`       | Message content                                                | Yes      |
| `template_id` | `$$TemplateID` | DLT Template ID (mandatory for messages in India)              | Optional |
| `message_id`  | `$$MessageID`  | Unique CleverTap message ID for tracking                       | Yes      |
| `campaign_id` | `$$CampaignID` | CleverTap campaign ID                                          | Optional |
| `type`        | `$$TYPE`       | Message type (`OTP`, `MKT`, `TXN`, or `Default`, `OTP`)        | Optional |
| `long_url`    | `$$LongURL`    | Long URL to shorten and insert into the message (if supported) | Optional |

> 📘 Note
>
> `$$MessageID` is required for accurate DLR (Delivery Report) tracking. Kaleyra must return the same ID in the delivery callback.

<Image alt="Set Parameters" align="center" width="60% " border={true} src="https://files.readme.io/55bedfb8ee5b06a39b06aa171fb34d64d0fd2047d8baee4a0b2a5d644c2e5bc9-sssdfd.png">
  Set Parameters
</Image>

7. Click on **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:kaleyra-sms#send-a-test-sms).

## Send a Test SMS

Sending a test SMS helps confirm that your Kaleyra integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To validate your configuration:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   * *Country Code and Mobile Number*: Enter the country code and mobile number to which you want to send the message.
   * *Template ID*: (if applicable)
   * *Message*: Enter sample text, such as *This is a test message powered by Kaleyra*.
   * *Dynamic Fields*: If `sender`, `type`, or `long_url` are dynamic, provide those values as key-value pairs

<Image alt="Send a Test SMS" align="center" width="65% " border={true} src="https://files.readme.io/f671d6b824955a1b3f771626eea96544804220666b19ab82cebc93a2e9a73649-image.png">
  Send a Test SMS
</Image>

3. Click **Send Test**.

If the configuration is correct, the test message will be delivered, and Kaleyra will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from the CleverTap dashboard and share it with the Kaleyra support team.

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider Setup page *Settings* > *Channels* > *SMS* > *Provider Nickname*
2. Share this URL with [Kaleyra support]().

<Image alt="Set Up SMS Callbacks" align="center" width="60% " border={true} src="https://files.readme.io/6a0d89d8e39ddbb0e19894dd105695dd3605ef8ea3bb96670f0434de1c018573-image.png">
  Set Up SMS Callbacks
</Image>

### Verifying Successful Integration

Your integration is considered successful when the following criteria are met:

* The test SMS is delivered to the intended mobile number.
* You receive a DLR (Delivery Report) callback from Kaleyra at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
* CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using Kaleyra as your SMS provider.
