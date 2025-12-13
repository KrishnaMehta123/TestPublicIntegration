---
title: Pingbix
excerpt: Learn how to integrate Pingbix with CleverTap for WhatsApp communication.
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

[Pingbix](https://pingbix.com/) is a WhatsApp Business Service Provider (BSP) that helps businesses automate and scale customer communication through WhatsApp. It supports features such as campaign management, real-time delivery tracking, and secure message routing via WhatsApp’s Cloud API.

When integrated with CleverTap, Pingbix enables you to do the following:

- Track message delivery via Pingbix’s callback system.
- Combine WhatsApp messaging with CleverTap’s segmentation and personalization.
- Use pre-approved templates for transactional and promotional campaigns.
- Send WhatsApp messages directly from the CleverTap dashboard.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Pingbix. The CleverTap and Pingbix integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Pingbix](https://pingbix.com/contact) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

- WhatsApp Campaigns feature is enabled on your CleverTap account.
- Active Pingbix WABA (WhatsApp Business Account) credentials.
- Pingbix API key and message delivery callback URLs.

# Integrate Pingbix with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:pingbix#configure-clevertap-dashboard)
2. [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix)

## Configure CleverTap Dashboard

To configure the CleverTap dashboard for Pingbix:

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
    "0-1": "Enter the nickname as Pingbix or the `<10-digit phone number>` for easy reference.",
    "1-0": "Mobile Number",
    "1-1": "Add your WhatsApp Integrated number with country code (for example, +918889500122)",
    "2-0": "HTTP End Point",
    "2-1": "Paste the URL received from the Pingbix team.  \nCheck that the URL is in HTTPS format, that is, your URL must begin with **https\\://**.",
    "3-0": "Request Type",
    "3-1": "Ensure the Request Type is _POST_.",
    "4-0": "Headers",
    "4-1": "Click **Header**  \nEnter the first key name as a user and enter the user value received from Pingbix.  \nEnter the second key name as the password, and enter the value received from Pingbix.",
    "5-0": "Delivery Report Callback URL",
    "5-1": "This URL is generated automatically on the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix).",
    "6-0": "Inbound Message  \nCallback URL",
    "6-1": "This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix)."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    null,
    null
  ]
}
[/block]


4. (Optional) Select _Mark this as default_ to make Pingbix as the default provider when sending a WhatsApp messages.
5. (Optional) Select _Set auto-reply for users not tracked on CleverTap_ to automatically reply to a WhatsApp message from users not tracked on the CleverTap dashboard.
6. (Optional) Set the _Maximum Concurrent API requests_ to any value between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification to verify if the configuration is successful.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8218fbb75f9546083d2e6bdcfdd5ad32895514885569383c9ec157e337176e2d-image.png",
        null,
        "Send a test message on whatsapp"
      ],
      "align": "center",
      "border": true,
      "caption": "Send a Test Message on WhatsApp"
    }
  ]
}
[/block]


## Set Up CleverTap Callbacks in Pingbix

To set up CleverTap callbacks in Pingbix, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ > _Pingbix_ from the CleverTap dashboard. You will find the _Delivery Report Callback URL_ and _Inbound Message Callback URL_ under the _Provider Configuration_ page.
2. **Share Callback URLs with Pingbix team**: Copy the Delivery and Inbound report callback URLs and send them to the Pingbix WhatsApp support team for configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/17b2d251719811d51b3ba0ae7173be50be62ca9e7e716c2c445c2c6ed21362fb-image.png",
        null,
        "Callback URLs"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Callback URLs"
    }
  ]
}
[/block]


Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Pingbix.

> 📘 Note:
> 
> Your templates must be approved on the Pingbix dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the Pingbix integration, write to [Pingbix Support](https://pingbix.com/contact).

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
      "sizing": "70% ",
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
   > For example, if you have multiple provider configurations, such as Phone_1 and Phone_2, you can use the particular template name once within Phone_1 and Phone_2.
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
      "sizing": "70% ",
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

For detailed instructions on creating a WhatsApp campaign using Pingbix as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using Pingbix as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp).