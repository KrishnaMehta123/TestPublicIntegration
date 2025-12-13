---
title: AiSensy
excerpt: Learn how to integrate AiSensy with CleverTap for WhatsApp communication.
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

[AiSensy](https://www.aisensy.com/) offers a native integration with CleverTap that enables businesses to send WhatsApp broadcasts directly from the CleverTap dashboard. This integration allows you to:

- Trigger campaigns using pre-approved WhatsApp templates.
- Automate user engagement based on behavioral events.
- Track delivery and response metrics using CleverTap analytics.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by AiSensy. The CleverTap and AiSensy integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [AiSensy](mailto:support@aisensy.com) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

- The WhatsApp Campaigns feature is enabled on your CleverTap account.
- An active AiSensy account with WhatsApp Business API (WABA) access.
- A provisioned WhatsApp number from AiSensy.

> 📘 Enable the CleverTap add-on
> 
> Check that you have enabled the CleverTap add-on in the AiSensy dashboard before proceeding with the integration.

# Integrate AiSensy with CleverTap

This process involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:aisensy#create-a-passcode-on-the-clevertap-dashboard)
2. [Configure CleverTap Dashboard](#configure-clevertap-dashboard)
3. [Set Up Callbacks in AiSensy](#set-up-callbacks-in-aisensy)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to its REST API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Configure CleverTap Dashboard

To set up AiSensy as your WhatsApp provider from the CleverTap dashboard:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_.

2. Click **+ Add Provider** and select _Generic (Other)_ from the Provider list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e451b36150e189f94b3d4082226e5ef5b9a8517791b6774746a9137ad43370e9-image.png",
        null,
        "Provider Setup"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Provider Setup"
    }
  ]
}
[/block]


3. Enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "**Field**",
    "h-1": "**Details**",
    "0-0": "Nickname",
    "0-1": "Enter the nickname as AiSensy_WA for easy reference.",
    "1-0": "Mobile Number",
    "1-1": "Add your WhatsApp Integrated number with country code (for example, +918889500122)",
    "2-0": "Request Type",
    "2-1": "Ensure the Request Type is _POST_.",
    "3-0": "HTTP Endpoint",
    "3-1": "Paste the following URL:`https://backend.aisensy.com/clever-tap/t1/messages`  \nCheck that the URL is in HTTPS format, that is, your URL must begin with https//",
    "4-0": "Delivery Report Callback URL",
    "4-1": "This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in AiSensy](doc:aisensy#set-up-callbacks-in-aisensy).",
    "5-0": "Inbound Message Callback URL",
    "5-1": "This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in AiSensy](doc:aisensy#set-up-callbacks-in-aisensy)."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    null,
    null
  ]
}
[/block]


4. Add Headers from AiSensy. To do so, follow the steps to configure headers:
   1. Go to _AiSensy Dashboard_ > _Integrations_ > _CleverTap_ > click **Regenerate Key**.
   2. Copy the Authorization Headers.
   3. Paste the headers into the Header section in CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0bdb0c80b88f1b3e9786dadf8dbc5219d4831ee6d9499066dc6aa6b73921b2bc-image.png",
        null,
        "Configure Headers"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Configure Headers"
    }
  ]
}
[/block]


5. (Optional) Select _Mark this as default_ to make the service provider the default provider for sending a WhatsApp message via AiSensy.
6. (Optional) Select _Set auto-reply for users not tracked on CleverTap_ to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
7. (Optional) Set the _Maximum Concurrent API requests_ between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
8. Test the integration and click **Save** to trigger a test message and automatically save your credentials.

## Set Up Callbacks in AiSensy

Callbacks ensure delivery reports and inbound user messages from WhatsApp are synced back to CleverTap, enabling accurate tracking and engagement workflows.

To set up CleverTap callbacks with AiSensy, follow the steps below:

1. In the AiSensy dashboard, go to _Integrations_ > _CleverTap_.
2. Click **Regenerate Key** under _CleverTap Header Key_.
3. In the CleverTap dashboard, go to _Settings_ > _Channels_ > _WhatsApp_. The _Delivery Report Callback URL_ and _Inbound Message Callback URL_ are under the Provider Configuration page. Copy them.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/931f649e1d2a8e6a9c805ef928b38b661294cc92d1d2597d120df3702259a820-image.png",
        null,
        "Callback URLs"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Callback URLs"
    }
  ]
}
[/block]


4. Paste both callback URLs in AiSensy and click **Submit**.

Once configured, check that message delivery reports and inbound messages sync correctly between CleverTap and AiSensy.

You can now broadcast WhatsApp messages directly from the CleverTap dashboard using AiSensy.

# Add WhatsApp Message Templates

WhatsApp message templates are reusable, pre-approved messages you can send to users at scale, such as alerts, reminders, or promotional campaigns. For detailed instructions on creating and testing WhatsApp message templates, refer to [WhatsApp Message Templates](doc:whatsapp-message-templates).

# Create Campaign

For detailed instructions on creating a WhatsApp campaign using AiSensy as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

# Creating a Journey

For detailed instructions on creating a WhatsApp journey using AiSensy as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).