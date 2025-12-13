---
title: Sinch
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

[Sinch](https://www.sinch.com/) is a global cloud communications provider that helps businesses to deliver SMS, voice, and other communication services across global markets. By integrating Sinch with CleverTap, you can send transactional and promotional SMS messages through CleverTap’s unified engagement dashboard.

This integration supports message delivery, tracking via DLR (Delivery Receipt), and DLT compliance for enterprises in India.

Here’s how businesses use Sinch with CleverTap:

- _Send OTPs and Alerts_: Deliver real-time authentication and transaction confirmations.
- _Promote Offers and Sales_: Target user segments with promotional SMS blasts.
- _Re-engage Drop-Offs_: Remind users to complete transactions or renew subscriptions.

Integrate CleverTap’s segmentation and campaign engine with Sinch’s SMS delivery pipeline for high-engagement, context-driven messaging.

# Prerequisites for Integration

To integrate Sinch with CleverTap, ensure the following:

- You must have an active SMS account with Sinch (including username, password, and endpoint), provided by [Sinch India support](mailto:nam-ACL@sinch.com).
- You must have a CleverTap account with SMS setup enabled.
- If your account is registered in India, ensure all templates and headers are DLT-approved.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Sinch India. The CleverTap and Sinch India integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Sinch India](mailto:support.cm@sinch.com) for support and resolution.

# Integrate Sinch with CleverTap

To integrate Sinch SMS with CleverTap, follow these three steps:

1. [Sinch API for Integration](doc:sinch-sms#sinch-api-for-integration)
2. [Set Up CleverTap Dashboard](doc:sinch-sms#set-up-clevertap-dashboard)
3. [Send a Test SMS](doc:sinch-sms#send-a-test-sms)

## Sinch API for Integration

CleverTap sends HTTPS POST requests to the Sinch API to initiate SMS delivery. The payload must follow the format below to ensure successful delivery and DLT compliance.

- _API Endpoint_: `https://ap.awsigateway.com/v1/enterprises/messages.json`
- _Sample Request Payload_:

```json
{
  "appid": "clvrtap",
  "userId": "clvrtap",
  "pass": "clvrtap_18",
  "contenttype": "1",
  "from": "ACLALT",
  "to": "$$To",
  "selfid": "false",
  "msgid": "$$MessageID",
  "intflag": "false",
  "alert": "1",
  "text": "$$Body",
  "dpi": "1701158123540939524",
  "dtm": "$$TemplateID"
}
```

This payload includes the recipient details, message content, and DLT information. CleverTap dynamically replaces variables like `$$To`, `$$Body`, and `$$TemplateID` at runtime.

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate your Sinch SMS provider. To configure the CleverTap dashboard:

1. Go to _Settings_ > _Engage_ > _Channels_ > _SMS_ in the CleverTap dashboard.
2. Click **+ Add Provider**. The Add SMS provider page opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ca98feff96deb7a4d4b6c4a0576f0b108f3d696f98dfbaa9b61faca58641cf2-image.png",
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
    "0-1": "Enter the nickname of the SMS provider to identify it uniquely. For example:`Sinch_India`.",
    "1-0": "Callback URL",
    "1-1": "Enter this URL in the Sinch platform to receive delivery status updates for your SMS messages. Refer to [Set Up SMS Callbacks](doc:sinch-sms#set-up-sms-callbacks).",
    "2-0": "Request Type",
    "2-1": "Select `POST`, then specify the Sinch API endpoint: `https://ap.awsigateway.com/v1/enterprises/messages.json`. Refer to [Sample Payload Structure (JSON)](doc:sinch-sms#sample-payload-structure-json).",
    "3-0": "HTTP Endpoint",
    "3-1": "Paste the URL received from Sinch India NAM team.  \nEnsure that the URL is in HTTPS format, that is, your URL must begin with `https://`.",
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

Use the following sample JSON payload when configuring the Sinch provider in CleverTap. The payload represents the structure used to send an SMS message via Sinch. Replace placeholder variables with system dynamic replacements like `$$To` and `$$Body`.

```json
{
  "appid": "clvrtap",
  "userId": "clvrtap",
  "pass": "secure_password",
  "contenttype": "1",
  "from": "ACLALT",
  "to": "$$To",
  "selfid": "false",
  "msgid": "$$MessageID",
  "intflag": "false",
  "alert": "1",
  "text": "$$Body",
  "dpi": "1701158123540939524",
  "dtm": "$$TemplateID"
}
```

This structure ensures that message-specific data, such as recipient, sender, content, and a unique message ID is correctly passed to the Sinch API.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1721da1676d07d0f2e1066248cfb9ac194781f9c7c01d42de93bd6e9469865dc-image.png",
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

CleverTap replaces the following variables dynamically when sending SMS requests to the provider. These placeholders must be used in the payload or headers, depending on your Sinch configuration:

| Parameter     | Description                                                                                 | **Required** |
| ------------- | ------------------------------------------------------------------------------------------- | ------------ |
| `appid`       | Application ID assigned by Sinch.                                                           | Yes          |
| `userId`      | Username provided by Sinch India.                                                           | Yes          |
| `pass`        | Password for the above user ID.                                                             | Yes          |
| `from`        | Sender ID (six characters). Use alphanumeric for service messages, numeric for promotional. | Yes          |
| `to`          | Recipient’s mobile number. Use commas to send to multiple numbers.                          | Yes          |
| `text`        | Message body. Use `$$Body` as a placeholder.                                                | Yes          |
| `msgid`       | Unique CleverTap message ID. Must be returned by Sinch in the callback.                     | Yes          |
| `dtm`         | DLT Template ID. Use `$$TemplateID`.                                                        | Optional     |
| `dpi`         | DLT Principal Entity ID.                                                                    | Optional     |
| `alert`       | Indicates message type: `1` for transactional, `0` for promotional (default).               | Yes          |
| `contenttype` | Always set to `1` for text messages.                                                        | Yes          |
| `selfid`      | Set to `true` to enable message ID mapping.                                                 | Yes          |
| `intflag`     | Set to `false` for domestic and `true` for international messages.                          | Yes          |
| `s`           | Enables URL shortening: `0` = disable, `1` = enable.                                        | Optional     |

> 📘 Note
> 
> `$$MessageID` is required for accurate DLR (Delivery Report) tracking. Sinch must return the same ID in the delivery callback.

4. Select the Batch option to upload multiple SMS records in one go. Enter the required details for each record.

> 📘 Single Batch Limit
> 
> A single batch can have a maximum of 1,000 records.

5. Click on **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:sinch-sms#send-a-test-sms).

## Send a Test SMS

Sending a test SMS helps confirm that your Sinch integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To validate your configuration:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   - _Country Code and Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   - _Message_: Enter sample text, such as _This is a test message powered by Sinch_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/440d338366857bc07cb488cff8ce0b667c10fe20e57ca880cb2b9e4689cdff65-image.png",
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

If the configuration is correct, the test message will be delivered, and Sinch will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from the CleverTap dashboard and share it with the Sinch support team.

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider Setup page _Settings_ > _Channels_ > _SMS_ > _Provider Nickname_.
2. Share this URL with [Sinch India support](mailto:support.cm@sinch.com).

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
- You receive a DLR (Delivery Report) callback from Sinch at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
- CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using Sinch Mobile as your SMS provider.