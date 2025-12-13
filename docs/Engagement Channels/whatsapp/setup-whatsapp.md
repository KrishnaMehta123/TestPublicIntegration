---
title: Setup
excerpt: Understand how to set up WhatsApp as a channel for your marketing campaigns
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: >-
    Refer to the pages listed below to learn more about the following WhatsApp
    sections:
---
# Overview

CleverTap offers WhatsApp as a paid add-on, allowing businesses to communicate with their customers effectively and efficiently.

To enable WhatsApp as a communication channel for your organization, you raise a request on [sales@clevertap.com](mailto:sales@clevertap.com).

# Getting Started

To use WhatsApp as a channel for your marketing campaigns and customer journeys, you need access to the WhatsApp Business API.  
CleverTap currently supports no-code integration with the following partners:

- Gupshup
- Nexmo
- ValueFirst
- Exotel

If you have access to the WhatsApp Business API through a service provider that is not currently supported by CleverTap, you can use CleverTap's [Generic WhatsApp APIs](https://docs.clevertap.com/docs/generic-whatsapp) to integrate your service provider with CleverTap. 

Alternatively, you can request your service provider to become a supported WhatsApp partner by integrating CleverTap's generic API with their native messaging APIs using middleware.

By enabling your service (check for all such instances) provider with CleverTap, you'll be able to utilize all the features and benefits offered by our platform.

> 📘 Using CleverTap BSP
> 
> To access the WhatsApp Business API directly through CleverTap, refer to the detailed [integration document](https://docs.clevertap.com/docs/clevertap-bsp).

# Setup WhatsApp Service Provider

To setup a WhatsApp service provider, perform the following steps:

- From the dashboard, navigate to _Settings_ > _Channels_ > _WhatsApp_.
- Click **+ Provider** to add a provider.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70663ad-Add_WhatsApp_Service_Provider.png",
        "Add WhatsApp Service Provider",
        "Click the +Provider button to add a new service provider for WhatsApp"
      ],
      "align": "center",
      "border": true,
      "caption": "Add WhatsApp Service Provider"
    }
  ]
}
[/block]


- Add the WhatsApp service provider's information.
- Click **Send Test WhatsApp** to check if the provider has been set up correctly and can send WhatsApp messages. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/043a64e-Save_Provider_Details.png",
        "Save Provider Details",
        "Click the Save button to save the WhatsApp provider details."
      ],
      "align": "center",
      "border": true,
      "caption": "Save Provider Details"
    }
  ]
}
[/block]


- Click **Save** 

Refer to the following integration guides for more details:

- [Adding Gupshup as a provider](https://docs.clevertap.com/docs/gupshup).
- [Adding Nexmo as a provider](https://docs.clevertap.com/docs/nexmo-whatsapp).
- [Adding ValueFirst as a provider](https://docs.clevertap.com/docs/valuefirst-digital-whatsapp).
- [Adding Exotel as a provider](https://docs.clevertap.com/docs/exotel-whatsapp). 

# Provider Operations

This section describes the different user actions for the available WhatsApp service providers.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eaa04e2-Service_Provider_Operations.png",
        "Service Provider Operations",
        "The image represents the WhatsApp service provider operations available for the end users."
      ],
      "align": "center",
      "border": true,
      "caption": "Service Provider Operations"
    }
  ]
}
[/block]


## Edit Settings

You can edit the WhatsApp provider settings to update the provider configurations.

Follow the steps to edit provider settings:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _WhatsApp_ > Providers tab.
- Click the ellipsis next to the provider.
- Select _Edit settings_ from the list. The provider credentials window displays.
- Update the required information.
- Click **Send Test WhatsApp** to check that the provider is working correctly.
- Click **Save**.

## Archive Service Providers

You can archive any of the current WhatsApp service providers from the settings. Archiving the WhatsApp service provider stops any active Campaigns or Journeys for this provider. The archived provider will not be available for use in the future. 

Follow the steps to archive a WhatsApp service provider:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _WhatsApp_ > Providers (highlight this as well) tab.
- Click the ellipsis next to the provider.
- Select _Archive_ from the list. 

## Delete Service Providers

You can delete any of the current WhatsApp service providers from the settings. Deleting the WhatsApp service provider will remove all existing data from our system and stop any active Campaigns or Journeys. The deleted provider will not be available for use in the future.

Follow the steps to delete a WhatsApp service provider:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ >_WhatsApp_ > Providers tab.
- Click the ellipsis next to the provider.
- Select _Delete_ from the list.

## Opt-in Users into WhatsApp

Most people do not like receiving unsolicited messages on WhatsApp. Therefore, it is important for you to explicitly request permission before sending messages to your users on their WhatsApp account. 

By default, CleverTap keeps all the profiles opted out of WhatsApp. To opt-in profiles, update the profile using the following code:

```json
"MSG-whatsapp":true
```

You have the following two ways to opt-in users for WhatsApp:

- [Opt-in via updating the user's profile property](https://developer.clevertap.com/docs/concepts-user-profiles#section-updating-the-user-profile). 
- [Opt-in via the API profile update](https://developer.clevertap.com/docs/upload-user-profiles-api). 

## Message Templates in WhatsApp

WhatsApp restricts brand-initiated messages (the messages that you send via campaigns) to pre-approved templates. You can fill in the variables in the templates to personalize a message. 

For example:

_Hello {{1}}, Congratulations on your ticket booking. Here is your ticket number: {{2}}. Please ensure you visit us on {{3}}. Enjoy your experience._

The variables _{{1}}_ or _{{2}}_ or _{{3}}_ can be replaced by a text of your choice. You can use CleverTap's event and profile personalization to personalize the message for your audience.

To set up a message template, follow the steps listed under [Sending Message Templates](https://developers.facebook.com/docs/whatsapp/message-templates/creation) documentation on Facebook.

## Configure Message Templates

All your message templates must be approved by WhatsApp. At CleverTap, we help you with the verification. For more information on how to create message templates, refer to the [Creating Message Templates](https://developers.facebook.com/docs/whatsapp/message-templates/creation/) documentation by Facebook. 

The media message templates allow you to expand the content you can send to the recipients beyond the standard messages. The template is organized primarily into four sections - _Header_, _Body_, _Footer_, and _Buttons_.

Using this template, you can attach media files (image, video, document, location) within the **Header** along with the message body. 

Additionally, WhatsApp also allows marketers to include **CTAs** or **Quick Reply** buttons in the text or media message templates for making the conversations more interactive. 

- Call-to-Action (CTAs) — Enables the customer to make a phone call or visit a website.
- Quick Reply — Allows your customer to respond with a simple text message.

Once your interactive message templates have been created and approved, you can use them in notification messages as well as customer service/care messages.

The images below represent different templates that marketers can create for engaging their customers effectively.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa88774-Templates.png",
        "Templates.png",
        2318
      ],
      "align": "center",
      "border": true,
      "caption": "WhatsApp Message Templates"
    }
  ]
}
[/block]


After your templates are verified, you can add them in the WhatsApp settings under the _Templates_ tab.

To use WhatsApp with CleverTap, it is important to copy the templates accurately in the settings by performing the following steps:

1. From the dashboard, navigate to _Account > Settings > Engage > Channels > WhatsApp_. 
2. Click one of the Provider names.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c423fd6-image.png",
        "image.png",
        1894
      ],
      "align": "center",
      "border": true,
      "caption": "WhatsApp Providers"
    }
  ]
}
[/block]


3. Navigate to the **Templates** tab.
4. Click **+ Template** .

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af37717-Screenshot_2021-09-21_at_8.37.29_PM.png",
        "Screenshot 2021-09-21 at 8.37.29 PM.png",
        2346
      ],
      "align": "center",
      "border": true,
      "caption": "Add Template"
    }
  ]
}
[/block]


5. Now, enter the _Namespace_ for your template.

> 🚧 Namespace Format
> 
> When copying the message templates from the WABA dashboard, use the following format for the namespace: \<template_namespace>:\<template_name>. You can find the \_Namespace_ value from the _Message templates_ section on the WABA dashboard as shown in the image below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f755093-namespace.png",
        "namespace.png",
        2879
      ],
      "align": "center",
      "border": true,
      "caption": "Message Template Namespace"
    }
  ]
}
[/block]


Following is an example of _Namespace_ format

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d7f6250-Screenshot_2021-09-23_at_1.01.12_PM.png",
        "Screenshot 2021-09-23 at 1.01.12 PM.png",
        1354
      ],
      "align": "center",
      "border": true,
      "caption": "Namespace Format"
    }
  ]
}
[/block]


6. Copy and save the approved message templates from your WABA dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5729acc-Whatsapp_interactive.png",
        "Whatsapp interactive.png",
        1452
      ],
      "align": "center",
      "border": true,
      "caption": "Save WhatsApp Template"
    }
  ]
}
[/block]


7. Click **Save Template** to save the message template.  

> 📘 Language Support
> 
> - For Vonage (Nexmo), if you don't find the required language support on the CleverTap dashboard, contact our support team to enable the required language for your account.
> - Gupshup supports and handles all languages automatically, hence you do not need to add them on the CleverTap dashboard.