---
title: QuickReply
excerpt: >-
  Learn how to integrate QuickReply with CleverTap to send personalized WhatsApp
  messages at scale.
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

[QuickReply](https://quickreply.ai/) is a conversational commerce platform that helps brands automate WhatsApp communication at scale. By integrating QuickReply with CleverTap, you can send personalized, automated WhatsApp messages triggered by user behavior, leveraging QuickReply’s API and infrastructure.

With this integration, you can do the following:

- Send automated WhatsApp messages based on user actions or campaigns.
- Personalize messages using CleverTap’s user profiles.
- Track message delivery and user engagement within CleverTap.

This setup combines QuickReply’s automation capabilities with CleverTap’s real-time engagement engine to drive relevant conversations and increase conversions.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by QuickReply. The CleverTap and QuickReply integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [QuickReply](mailto:help@quickreply.ai) for support and resolution.

# Prerequisites for Integration

To integrate QuickReply with CleverTap:

- You must have the WhatsApp add-on enabled on your CleverTap account in addition to the Essentials Plan.
- WhatsApp onboarding for the phone number must be completed via QuickReply.
- Check that you have the Project ID and Passcode from CleverTap and the Authorization Header from the QuickReply dashboard.

# Integrate QuickReply with CleverTap

This process involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:quickreply#create-a-passcode-on-the-clevertap-dashboard)
2. [Configure CleverTap dashboard](doc:quickreply#configure-clevertap-dashboard)
3. [Set Up CleverTap Callbacks with QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to its REST API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Configure CleverTap dashboard

To configure the CleverTap dashboard, perform the following steps:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ from the CleverTap dashboard.

2. Click **+ Add Provider** and select _Generic (Other)_ from the dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5ea73360e548e7e9e865b5c4eee5d3de38df679e2e570c832c3c3d023bfa99e-image.png",
        null,
        "Provider Setup"
      ],
      "align": "center",
      "sizing": "65% ",
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
    "0-1": "Enter a name such as `QuickReply` for reference.",
    "1-0": "Mobile Number",
    "1-1": "Add your WhatsApp Integrated number with country code (for example, 918889500122)",
    "2-0": "Request Type",
    "2-1": "Ensure the Request Type is `POST`.",
    "3-0": "HTTP Endpoint",
    "3-1": "Enter HTTP Endpoint as the following: `https://app.quickreply.ai/integrations/api/clevertap/WHATSAPP/send-message`.",
    "4-0": "Delivery Report Callback URL",
    "4-1": "This URL is generated automatically in the CleverTap dashboard. Share the URL with the QuickReply account manager to configure it with the WhatsApp account. Refer to [Set Up CleverTap Callbacks in QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply).",
    "5-0": "Inbound Message  \nCallback URL",
    "5-1": "This URL is generated automatically in the CleverTap dashboard. Share the URL with the QuickReply account manager to configure it with the WhatsApp account. Refer to [Set Up CleverTap Callbacks in QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply) ."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    null,
    null
  ]
}
[/block]


4. Add Headers from QuickReply. To do so, follow the steps to configure headers:
   1. Go to _Settings_ > _CleverTap Integration_ in QuickReply Dashboard.
   2. Copy the _Authorization Headers_.
   3. Paste the headers into the _Header_ section in CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b93b1972c649d1067acbbbdaa9b099db3261ac6f521a21de3fb1c5c1ded21576-image.png",
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


5. (Optional) Select _Markthis as default_ to make this service provider the default provider for sending a WhatsApp message via QuickReply.
6. (Optional) Select _Set auto-reply for users not tracked on CleverTap_ to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
7. (Optional) Set the _Maximum Concurrent API requests_ between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
8. Test the integration and click **Save** to trigger a test message and automatically save your credentials.

## Set Up CleverTap Callbacks in QuickReply

To set up CleverTap callbacks with QuickReply, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to _Settings_ > _Channels_ > _WhatsApp_ from the CleverTap dashboard. You will find the _Delivery Report Callback URL_ and _Inbound Message Callback URL_ under the _Provider Configuration_ page.
2. **Share Callback URLs with QuickReply**: Copy both URLs and the WhatsApp phone number used in CleverTap, and send them to the QuickReply Account Manager or email [help@quickreply.ai](mailto:help@quickreply.ai).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/33695bf450091675cae04a63f9fcdc03d5b8a0fa04c6d77d7b8b718bbdb52b6b-image.png",
        null,
        "Callback URLs"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Callback URLs"
    }
  ]
}
[/block]


Once configured, ensure that message delivery reports and inbound messages sync correctly between CleverTap and QuickReply.

> 📘 Message Templates
> 
> You have to get your templates approved on the QuickReply dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the QuickReply integration, write to [help@quickreply.ai](mailto:help@quickreply.ai).

## Add Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, perform the following steps:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ > _QuickReply_ on the CleverTap dashboard. 
2. Select _Templates_ and click **+ Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70d1653-non_CT_approved_templates.jpg",
        "Create a New Template",
        "Create a New Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Template"
    }
  ]
}
[/block]


3. Enter the template name.

> 📘 Naming WhatsApp Templates
> 
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
> 
> For example, if you have multiple provider configurations, such as Phone_1 and Phone_2, you can use a particular template name once within Phone_1 and then again on Phone_2.

4. Select the language in which you want to display the message.
5. Select the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, or _Location_.
6. Create a [Limited Time Offer Template](doc:whatsapp-message-templates#limited-time-offer-templates), if required.
7. Enter the message content.
8. Select _Footer_ to add a footer text and a button (Quick Reply or a Call To Action).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5bd5090-Generic_template_create.jpg",
        "",
        "Define Template Content"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Template Content"
    }
  ]
}
[/block]


9. Click **Save Template**.

## Test a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

# Create Campaign

For detailed instructions on creating a WhatsApp campaign using QuickReply as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

# Create a Journey

For detailed instructions on creating a WhatsApp journey using QuickReply as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).