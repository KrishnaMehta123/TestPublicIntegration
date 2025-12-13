---
title: Interakt
excerpt: Learn how to integrate Interakt with CleverTap for WhatsApp communication.
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

[Interakt](https://www.interakt.ai/) is a WhatsApp Business platform that allows businesses to engage customers using automated notifications, product catalogs, and real-time messaging. Integrating Interakt enables businesses to send personalized WhatsApp campaigns powered by CleverTap's user segmentation and behavior analytics.

Use this integration to:

- Send personalized campaigns using Meta-approved templates.
- Automate user communication with template-triggered journeys.
- Track delivery and engagement using CleverTap’s reporting.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Interakt. The CleverTap and Interakt integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Interakt](mailto:hello@interakt.ai) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

- The WhatsApp Campaigns feature is enabled on your CleverTap account.
- A WhatsApp Business account on Interakt.
- An approved phone number is onboarded to WhatsApp Business via Interakt.
- The API credentials shared by the Interakt support team.

To activate a new WhatsApp Business number with Interakt, contact your Interakt Account Manager or write to [hello@interakt.ai](mailto:hello@interakt.ai).

# Integrate Interakt with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:interakt#configure-clevertap-dashboard)
2. [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt)

## Configure CleverTap dashboard

To configure the CleverTap dashboard:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ from the CleverTap dashboard.
2. Click **+ Add Provider** and select _Generic (Other)_ from the _Provider_ list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/885f26f7e2110aab22dd2bda2eba90bc4c3e187863d865a407301bc495da3a4d-image.png",
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
    "h-0": "Field",
    "h-1": "Details",
    "0-0": "Nickname",
    "0-1": "Enter the nickname as Interakt  or `Interakt91XXXXXXXXXX` for easy reference.",
    "1-0": "Mobile Number",
    "1-1": "Add your WhatsApp Integrated number with country code (for example, +918889500122)",
    "2-0": "Request Type",
    "2-1": "Ensure the Request Type is _POST_.",
    "3-0": "HTTP Endpoint",
    "3-1": "Paste the following URL:`https://api.interakt.ai/v1/platform_integrations/clevertap/message/`  \nCheck that the URL is in HTTPS format, that is, your URL must begin with `https//`",
    "4-0": "Headers",
    "4-1": "Click **Header** >  \nEnter the Key name as a user and enter the user value received from Interakt.  \nEnter the second key name as password and enter the value received from Interakt.",
    "5-0": "Delivery Report Callback URL",
    "5-1": "This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt).",
    "6-0": "Inbound Message  \nCallback URL",
    "6-1": "This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt)."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


4. (Optional) Select _Mark this as default_ to make this service provider the default provider when sending a WhatsApp message via Interakt.
5. (Optional) Select _Set auto-reply for users not tracked on CleverTap_ to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the _Maximum Concurrent API requests_ between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c384922-sendtest.png",
        "Send Test Message on WhatsApp",
        "Send a test message on whatsapp"
      ],
      "align": "center",
      "border": true,
      "caption": "Send a Test Message on WhatsApp"
    }
  ]
}
[/block]


## Set Up CleverTap Callbacks in Interakt

To set up CleverTap callbacks in Interakt, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ > _Interakt_ from the CleverTap dashboard. You will find the _Delivery Report Callback URL_ and _Inbound Message Callback URL_ under the _Provider Configuration_ page.
2. **Share Callback URLs with Interakt**: Copy the Delivery and Inbound report callback URLs and send them to the Interakt WhatsApp support team for configuration or email the URLs at [hello@interakt.ai](mailto:hello@interakt.ai).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8422e19929f1eaab1b982d4d8a98785454eb8da322dcb9d4894562d55ce3dc5b-image.png",
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


Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Interakt.

> 📘 Note
> 
> You have to get your templates approved on the Interakt dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages.

## Adding Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, follow these steps:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ > _Provider Nickname_ in the CleverTap dashboard. 
2. Select the _Templates_ option and click **+Template**.

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
> For example, if you have multiple provider configurations, such as Phone_1 and Phone_2, you can use the  particular template name once within Phone_1 and Phone_2.

4. You can also choose the language in which you will display the message.
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

## Testing a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

## Create Campaign

For detailed instructions on creating a WhatsApp campaign using Interakt as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using Interakt as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).