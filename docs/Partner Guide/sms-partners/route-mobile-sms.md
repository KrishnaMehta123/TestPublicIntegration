---
title: Route Mobile
excerpt: >-
  Learn how to integrate Route Mobile with CleverTap to send SMS notifications,
  OTPs, and campaigns globally with delivery tracking and DLT compliance.
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

[Route Mobile](https://routemobile.com/) is a cloud communications platform that provides scalable and secure SMS delivery across global markets. When integrated with CleverTap, it allows businesses to send real-time SMS notifications and promotional messages with advanced tracking and delivery insights.

Here’s how businesses use Route Mobile with CleverTap:

- _OTP and Alerts_: Send authentication codes, transaction updates, and critical account messages.
- _Promotional Campaigns_: Reach user segments with marketing offers and time-bound deals.
- _Order Notifications_: Deliver shipping, order, and service status updates instantly to customers.

Integrate CleverTap’s segmentation and campaign engine with Route Mobile's SMS delivery pipeline for high-engagement, context-driven messaging.

# Prerequisites for Integration

To integrate Route Mobile with CleverTap, ensure the following:

- You must have Route Mobile credentials (username, password, sender ID, DLT credentials), provided by the Route Mobile SPOC.
- You must have a CleverTap account with SMS channels enabled.
- If registered in India, your Route Mobile account must be DLT-compliant.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Route Mobile. The CleverTap and Route Mobile integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Route Mobile](mailto:support@routemobile.com) for support and resolution.

# Integrate Route Mobile with CleverTap

To integrate Route Mobile SMS with CleverTap, follow these three steps:

1. [Route Mobile API for Integration](doc:route-mobile-sms#route-mobile-api-for-integration)
2. [Set Up CleverTap Dashboard](doc:route-mobile-sms#set-up-clevertap-dashboard)
3. [Send a Test SMS](doc:route-mobile-sms#send-a-test-sms)

## Route Mobile API for Integration

CleverTap sends HTTP(S) requests to Route Mobile's API for SMS delivery. Following are the common endpoints based on the message region:

- Domestic SMS API: Used to send messages to Indian mobile numbers with DLT compliance.

  ```
  http://sms6.rmlconnect.net:8080/bulksms/personalizedbulksms?...parameters...
  ```
- International SMS API: Used for sending messages to numbers outside India.

  ```
  https://api.rmlconnect.net/bulksms/bulksms?...parameters...
  ```

These are the static authentication and sender parameters typically required in the Route Mobile API:

| Parameter  | Description                     |
| ---------- | ------------------------------- |
| `username` | Route Mobile account username.  |
| `password` | Route Mobile account password.  |
| `source`   | Sender ID used for sending SMS. |

These parameters are set once during configuration and do not change per campaign.

### System Dynamic Replacements

CleverTap dynamically replaces the following placeholders during SMS campaign execution to personalize and route each message appropriately:

| Dynamic Parameter     | Description                                     | Required         |
| --------------------- | ----------------------------------------------- | ---------------- |
| `$$To`                | Recipient’s phone number                        | Yes              |
| `$$Body`              | SMS content                                     | Conditional      |
| `$$TemplateID`        | DLT Template ID (required for India)            | Conditional      |
| `$$TemplateVariables` | Additional values for customizing DLT templates | Optional         |
| `$$CampaignID`        | Unique CleverTap campaign identifier            | Optional         |
| `$$MessageID`         | Unique message ID for tracking delivery reports | Required for DLR |

These dynamic fields must be used in the request URL or payload and will be replaced by CleverTap at send time.

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate your Route Mobile SMS provider. To configure the CleverTap dashboard:

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
    "0-1": "Enter the nickname of the SMS provider to identify it uniquely. For example:`RouteMobile`.",
    "1-0": "Callback URL",
    "1-1": "Enter this URL in the Route Mobile platform to receive delivery status updates for your SMS messages. Refer to [Set Up SMS Callbacks](doc:route-mobile-sms#set-up-sms-callbacks).",
    "2-0": "Request Type",
    "2-1": "Select `POST`, then specify the Route Mobile API endpoint: `https://ap.awsigateway.com/v1/enterprises/messages.json`. Refer to [Sample Payload Structure (JSON)](doc:route-mobile-sms#sample-payload-structure-json).",
    "3-0": "HTTP Endpoint",
    "3-1": "Paste the URL received from Route Mobile.  \nEnsure that the URL is in HTTPS format, that is, your URL must begin with `https://`.",
    "4-0": "Authentication",
    "4-1": "Under Authentication, select one of the following options:  \n  \n- No Authentication.\n- Basic Authentication: Enter the username and password."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    null,
    null
  ]
}
[/block]


4. Enter the following details under the _Headers_ section.

| Key           | Value              |
| ------------- | ------------------ |
| Authorization | `Bearer <API_KEY>` |
| Content-Type  | `application/json` |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2d150958aebb2dd35c5b3971d8cca19650dd768e4b387c106c726777c9adfb2e-image.png",
        null,
        "Set Headers"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Set Headers"
    }
  ]
}
[/block]


5. Under _Parameters_, select `JSON` as the request type for the POST request.  
   Refer to the following [sample payload](doc:route-mobile-sms#sample-payload-structure-json) below for the expected structure.

#### Sample Payload Structure (JSON):

Use the following sample JSON payload when configuring the Route Mobile provider in CleverTap. The payload represents the structure used to send an SMS message via Route Mobile. Replace placeholder variables with system dynamic replacements such as `$$To` and `$$Body`.

```json
{
  "username": "xxxx",
  "password": "xxxx",
  "source": "xxxx",
  "destination": "$$To",
  "message": "$$Body",
  "entityid": "xxxx",
  "tempid": "$$TemplateID",
  "tagname": "$$CampaignID",
  "msgid": "$$MessageID"
}
```

This structure ensures that message-specific data, such as recipient, sender, content, and a unique message ID are correctly passed to the Route Mobile API.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0375f6135ab52ab979ec8df24ee5febb626c58d088e98136c66501d8b90151dc-rou.png",
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


> 📘 Note
> 
> `$$MessageID` is required for accurate DLR (Delivery Report) tracking. Route Mobile must return the same ID in the delivery callback.

6. Select the Batch option to upload multiple SMS records. Enter the required details for each record.

> 📘 Single Batch Limit
> 
> A single batch can have a maximum of 1,000 records.

7. Click on **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:route-mobile-sms#send-a-test-sms).

## Send a Test SMS

Sending a test SMS helps confirm that your Route Mobile integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To validate your configuration:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   - _Country Code and Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   - _Message_: Enter sample text, such as _This is a test message powered by Route Mobile_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc535d7dbc1c198862a34b9231c4d87bf901e78b67547c0dbc99395f25b5d079-image.png",
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

> 🚧 DLT Compliance Requirements for Messaging
> 
> - Domestic messages must exactly match DLT templates.
> - International messages do not require DLT compliance.

If the configuration is correct, the test message will be delivered, and Route Mobile will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from the CleverTap dashboard and share it with the Route Mobile team.

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider Setup page _Settings_ > _Channels_ > _SMS_ > _Provider Nickname_.
2. Share this URL with [Route Mobile Support](mailto:support@routemobile.com).

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
- You receive a DLR (Delivery Report) callback from Route Mobile at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
- CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using Route Mobile as your SMS provider.