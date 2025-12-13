---
title: Poplar
excerpt: Direct Mail
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

[Poplar](https://heypoplar.com) is a performance-driven direct mail platform that enables businesses to send physical mailers to customers at any stage of the customer journey. With Poplar and CleverTap, you can trigger direct mail campaigns based on user activity, segmentation, or lifecycle stage.

The Poplar CleverTap integration allows you to:

- Send personalized direct mailers from within CleverTap campaigns
- Automate physical mail delivery as part of omnichannel journeys
- Enrich customer engagement with offline touchpoints triggered by real-time events

# Prerequisites for Integration

Ensure you have the following:

- Access to your Poplar dashboard and Poplar API key.
- Access to your CleverTap dashboard with permissions to configure webhooks and campaigns

# Integrate Poplar with CleverTap

The integration process involves the following two major steps:

1. [Set up Webhook in CleverTap](doc:poplar#set-up-webhook-in-clevertap)
2. [Configure Webhook Campaign in CleverTap](doc:poplar#configure-webhook-campaign-in-clevertap)

## Set up Webhook in CleverTap

To begin the integration, you'll first create a webhook in CleverTap. This webhook sends recipient and campaign-specific data to Poplar whenever the campaign is triggered. It ensures real-time delivery of personalized mailers to users based on their behavior and profile attributes.

To do so, follow these steps:

1. Go to _Settings_ > _Channels_ > _Webhook_.
2. Click **+ Add Webhook** and enter the following:

| Field         | Value                                  |
| ------------- | -------------------------------------- |
| Name          | Poplar                                 |
| HTTP Method   | `POST`                                 |
| Endpoint URL  | `https://api.heypoplar.com/v1/mailing` |
| Authorization | `Bearer <Poplar API key>`              |
| Content-Type  | `application/json`                     |

3. Click **Save** to create the webhook.

## Configure Webhook Campaign in CleverTap

Once the webhook is set up, the next step is to use it within a campaign. This campaign will send the recipient’s information and trigger mail delivery via Poplar’s API when users meet specific conditions.

To trigger the direct mailer using CleverTap:

1. Go to _Campaigns_ > _+ Campaign_ > _Webhook_.
2. Select the Webhook configured in [Create a Webhook in CleverTap](doc:poplar#create-a-webhook-in-clevertap)
3. In the _What_ section, under the _Webhook Content_ section, select the _Content Format_ as JSON and click the **Custom body** option.
4. Paste the following JSON payload:

```json
{
  "campaign_id": "{{ Profile.campaign_id | default: "-" }}",
  "recipient": {
    "city": "Thane",
    "email": "{{ Profile.Email | default: "-" }}",
    "state": "Maharashtra",
    "address_1": "Rutu Towers",
    "address_2": "Thane",
    "first_name": "{{ Profile.name | default: "-" }}",
    "last_name": "test",
    "postal_code": "400607"
  },
  "merge_tags": {
    "promo-code": ""
  },
  "creative_id": "<creative id>"
}
```

Use the personalization toolbar (`{`, `{{`, or `@`) to insert dynamic user profile values.

5. Click **Preview and Test** to validate the integration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd275445e2b7ca1f1b8010e7ce9345751fef51c2ea942c306b1312744b9bf1d5-image.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


6. In the Poplar dashboard:
   - Navigate to the campaign used in your payload
   - Go to the **History** section
   - Confirm if the test data is reflected

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ab3a2469b2efef8ec31fc9365355b1bcf4d1c66dcb3a21edb2ed051adb3a7c6-Screen_Recording_2025-02-17_at_2.13.14_PM_1.gif",
        "",
        "Verify the data on Poplar"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Verify the data on Poplar"
    }
  ]
}
[/block]


7. Once confirmed, click **Publish** in CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53fb29f32d1aa8d08ad12da400902f3abae1a16cc1aea6acee2a23441a0b7136-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true
    }
  ]
}
[/block]


By connecting Poplar with CleverTap, you can create impactful, timely direct mail campaigns as part of your user engagement strategy.