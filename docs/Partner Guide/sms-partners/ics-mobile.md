---
title: ICS Mobile
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

[ICS Mobile](https://icsmobile.in/) is a Communications Platform as a Service (CPaaS) provider that helps businesses send and receive SMS messages across global markets.

By integrating ICS with CleverTap, you can manage SMS campaigns directly from the CleverTap dashboard, alongside other engagement channels. This integration supports message delivery and DLR (Delivery Report) tracking, allowing you to run personalized, targeted SMS campaigns as part of your omnichannel strategy.

Here are a few ways businesses use ICS Mobile with CleverTap:

- _Transactional Alerts_: Deliver real-time OTPs, order confirmations, and payment updates.
- _Promotional Campaigns_: Announce offers, discounts, or product launches to targeted user segments.
- _Abandoned Cart Reminders_: Prompt users to complete their purchase with time-sensitive nudges.

Integrate CleverTap’s segmentation engine with ICS SMS to trigger context-aware messages and increase engagement.

# Prerequisites for Integration

To integrate ICS with CleverTap, check the following:

- You must have an active SMS account with ICS.
- You must have a CleverTap account with SMS setup enabled.
- If your account is registered in India, check that all templates and headers are DLT-approved.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by ICS. The CleverTap and ICS integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [ICS Mobile](mailto:sms.support@icsportal.in) for support and resolution.

# Integrate ICS Mobile with CleverTap

The integration includes three major steps:

1. [Set Up the ICS Dashboard](doc:ics-mobile#set-up-the-ics-dashboard)  
2. [Set Up CleverTap Dashboard](doc:ics-mobile#set-up-clevertap-dashboard)  
3. [Send a Test SMS](doc:ics-mobile#send-a-test-sms)

## Set Up the ICS Dashboard

To comply with the DLT (Distributed Ledger Technology) mandate for SMS delivery in India, you must upload specific template-related details to the ICS Account dashboard under the DLT Templates section. This setup ensures that your SMS campaigns sent via CleverTap adhere to government regulations.

### Upload the Following to ICS

- _Entity ID_: Unique ID assigned to your business by the DLT registrar.
- _Sender ID_: The six-character alphanumeric ID from which your SMS messages are sent.
- _Template ID_: Unique ID assigned to each approved transactional or promotional SMS template.
- _Template Details_: The actual content of the DLT-approved message templates. These must be entered manually into the ICS dashboard.
- _SMS Type_: Classifies the nature of the SMS message. Options include:

  - Transactional
  - Service Explicit
  - Service Implicit
  - Promotional

> 🚧 Template ID Handling
> 
> - _If the Template ID is not passed from CleverTap_:  
>   You must manually configure the template in the ICS dashboard. Ensure that all templates have been uploaded and validated to avoid delivery failures.
> - _If the Template ID is passed from CleverTap_:  
>   No manual configuration is required. CleverTap automatically maps the template during campaign execution.

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate your ICS Mobile SMS provider. To configure the CleverTap dashboard:

1. Go to _Settings_ > _Engage_ > _Channels_ > _SMS_ in the CleverTap dashboard.

2. Click **+ Add Provider**. The Add SMS provider page opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3355f85d920880e21c2d3646b71fc1c40e300fc2409d2a8d67a1e96bd8d363b1-image.png",
        null,
        "Add Provider"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Add Provider"
    }
  ]
}
[/block]


3. Under **Provider**, select _Other (Generic)_ and enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Nickname",
    "0-1": "Enter the nickname of the SMS provider to identify it uniquely. For example: `ICS`.",
    "1-0": "Callback URL",
    "1-1": "Enter this URL in the ICS platform to receive delivery status updates for your SMS messages. Refer to [Set Up SMS Callbacks](doc:ics-mobile#set-up-sms-callbacks).",
    "2-0": "Request Type",
    "2-1": "Select `POST`, then specify the ICS API endpoint: `https://sms.sendmsg.in/datasend`. Refer to [Sample Payload Structure (JSON)](doc:ics-mobile#sample-payload-structure-json).",
    "3-0": "HTTP Endpoint",
    "3-1": "Paste the URL received from the ICS team.  \nEnsure that the URL is in HTTPS format, that is, your URL must begin with `https://`.",
    "4-0": "Authentication",
    "4-1": "Under Authentication, select one of the following options:  \n  \n- No Authentication.\n- Basic Authentication: Enter the username and password.",
    "5-0": "Headers",
    "5-1": "Select Headers to include in the HTTP request sent to the API endpoint. These headers allow you to pass additional information, such as authentication tokens or content type."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    null,
    null
  ]
}
[/block]


#### Sample Payload Structure (JSON):

Use the following sample JSON payload when configuring the ICS provider in CleverTap. The payload represents the structure used to send an SMS message via ICS. Replace placeholder variables with system dynamic replacements like `$$To` and `$$Body`.

```json
{
  "user": "john_doe",
  "pass": "secure_password",
  "smstosend": [
    {
      "to": "$$To",
      "from": "$$uid",
      "smstext": "$$Body",
      "smsgid": "$$MessageID"
    }
  ]
}
```

This structure ensures that message-specific data such as recipient, sender, content, and a unique message ID is correctly passed to the ICS API.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/924775b6db70897d548c42d185c43da86a317b55f7a64ee743ad5f8a310a03c3-image.png",
        null,
        "Provider Configuration"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Provider Configuration"
    }
  ]
}
[/block]


#### System Dynamic Replacements

CleverTap replaces the following variables dynamically when sending SMS requests to the provider. These placeholders must be used in the payload or headers, depending on your ICS configuration:

| Variable              | Description                                                                                                                                                                         | Required |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| `$$To`                | Represents the recipient's mobile number. Must be included in the payload for successful message delivery.                                                                          | Yes      |
| `$$Body`              | Represents the SMS content. Either `$$Body` or `$$TemplateID` must be present in the payload.                                                                                       | Optional |
| `$$TemplateID`        | Represents the DLT-approved template ID. Required only for messages sent to Indian mobile numbers. Either `$$TemplateID` or `$$Body` must be included.                              | Optional |
| `$$TemplateVariables` | Represents variables used in the template message. Use this to dynamically replace placeholder names, OTP, or order numbers in the message body.                                    | No       |
| `$$CampaignID`        | Represents the unique CleverTap Campaign ID. Helpful for logging and reporting purposes, but not mandatory.                                                                         | No       |
| `$$MessageID`         | A unique message identifier generated by CleverTap. This must be sent back in the delivery callback under the `meta` field to enable end-to-end tracking (delivery, failure, etc.). | Yes      |

> 📘 Note
> 
> `$$MessageID` is required for accurate DLR (Delivery Report) tracking. ICS must return the same ID in the delivery callback.

4. Select the Batch option to upload multiple SMS records in one go. Enter the required details for each record.

> 📘 Single Batch Limit
> 
> A single batch can have a maximum of 1,000 records.

5. Click **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:ics-mobile#send-a-test-sms).

## Send a Test SMS

Sending a test SMS helps confirm that your ICS integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To validate your configuration:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   - _Country Code and Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   - _Message_: Enter sample text, such as _This is a test message powered by ICS_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bdfca6c237f34bfd23b0ab5055849f3fd71dca9fba7bf7ab98ba31405b7fad6f-image.png",
        null,
        "Send a Test SMS"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Send a Test SMS"
    }
  ]
}
[/block]


3. Click **Send Test**.

If the configuration is correct, the test message will be delivered, and ICS will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from the CleverTap dashboard and share it with the ICS support team.

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider Setup page _Settings_ > _Channels_ > _SMS_ > _Provider Nickname_.
2. Share this URL with [ICS mobile support](mailto:sms.support@icsportal.in).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a0d89d8e39ddbb0e19894dd105695dd3605ef8ea3bb96670f0434de1c018573-image.png",
        null,
        "Set Up SMS Callbacks"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Set Up SMS Callbacks"
    }
  ]
}
[/block]


### Verifying Successful Integration

Your integration is considered successful when the following criteria are met:

- The test SMS is delivered to the intended mobile number.
- You receive a DLR (Delivery Report) callback from ICS at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
- CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using ICS Mobile as your SMS provider.