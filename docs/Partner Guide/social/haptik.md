---
title: Haptik
excerpt: Understand how to integrate Haptik with CleverTap for WhatsApp communication
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 🚧 Support For Integration
> 
> This integration is completed by Haptik, and they are dedicated to maintaining and enhancing it. The CleverTap and Haptik integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact Haptik for support and resolution.

# Introduction

CleverTap users can now leverage the following WhatsApp capabilities of [Haptik](https://docs.haptik.ai/clevertap-integration/clevertap-integration) to communicate the following with their customers.

- Sending just-in-time offers to customers to drive purchases
- Gathering feedback on the services 
- Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

- You must have a WhatsApp add-on enabled on the Clevertap account in addition to the essentials price plan.
- Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
- You must have Haptik's WhatsApp Business API 

# Integrate Haptik with CleverTap

This process involves the following three steps:

1. [Find Haptik Credentials](doc:haptik#find-haptik-credentials)
2. [Configure CleverTap Dashboard](doc:haptik#configure-clevertap-dashboard)
3. [Set up CleverTap callbacks in Haptik](doc:haptik#set-up-clevertap-callbacks-in-haptik)

## Find Haptik Credentials

We recommend that you keep the _Callback URL_ and _Token_ details handy before starting with the configuration on the CleverTap dashboard:

To find these credentials:

1. Navigate to your Haptik _Conversation Studio_ platform.
2. Open your bot account.
3. Navigate to _Business Manager_ > _Channels_ > _Platform Deployments_. 
4. Select CleverTap from the _Platform_ drop-down. 

Copy the credentials for configuring the CleverTap dashboard:

- Callback URL
- Token

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/95ffcb4-haptik_configuration.png",
        "Locate Haptik Credentials",
        2552
      ],
      "align": "center",
      "border": true,
      "caption": "Haptik Credentials"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ from the CleverTap dashboard.
2. Click **+ Add Provider** and _Log in to Facebook_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23dde0f-Whatsapp_Common_Provider_Setup.png",
        null,
        "Provider Setup"
      ],
      "align": "center",
      "sizing": "80% ",
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
    "h-1": "Description",
    "0-0": "Provider",
    "0-1": "Select _Other (Generic)_ from the dropdown list.",
    "1-0": "Nickname",
    "1-1": "Enter the nickname as _Haptik_ or Haptik \\<10 digit phone number> for easy reference.",
    "2-0": "WhatsApp Business Number",
    "2-1": "Enter your phone number onboarded to WhatsApp API by Haptik.",
    "3-0": "Request Type",
    "3-1": "Ensure the Request Type is _Post_",
    "4-0": "HTTP Endpoint",
    "4-1": "Paste the _Callback URL_ from Haptik's _Platform Deployments_ tab as illustrated in the previous step.  \n  \nEnsure that the URL is in HTTPS format, i.e, your URL must begin with **https\\://**.",
    "5-0": "Headers",
    "5-1": "Click _Header_ > and then Enter the Key name as _Token_ and paste the token value copied from Haptik's _Platform Deployments_ tab, as illustrated in the previous step."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


> 📘 Callback URL
> 
> While pasting the Callback URL from the Haptik dashboard to the CleverTap dashboard, ensure that the URL is in HTTPS format, i.e your URL must begin with **https\://**.

4. Select the _Mark this as default_ checkbox to make this service provider the default provider to send a WhatsApp message.
5. To send an automatic reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard, select the _Set auto-reply for users not tracked on CleverTap_ checkbox. 
6. (Optional) You can set the _Maximum Concurrent API requests_ anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save** to save the details. 

## Set Up CleverTap Callbacks in Haptik

To set up the CleverTap callbacks:

1. Copy the _Delivery Report Callback URL_  from the CleverTap dashboard. You can find the Callback URLs under the Provider _Setup_ page ( _Settings_ > _Channels_ > _WhatsApp_ > _Haptik_)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0479084-callback_haptik.png",
        "Configure Callbacks",
        938
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Callbacks"
    }
  ]
}
[/block]


2. Paste the callback URL:  
   a. Open your Haptik bot account > navigate to _Business Manager _> _Channels_ > _Platform Deployments_.  
   b. Paste the callback URL under the _CleverTap Webhook URL_ as illustrated in the following image.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4043bf8-haptik_configuration_callback.png",
        "Paste the Callback",
        2552
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Callbacks"
    }
  ]
}
[/block]


# Finding Template Details

You need to replicate the details of your pre-approved templates on CleverTap. To find the details of your pre-approved templates on Haptik, navigate to the _Template_ section from the Haptik dashboard, as shown below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bdae381-haptik_templates.png",
        "Locate Template Details",
        1314
      ],
      "align": "center",
      "border": true,
      "caption": "Find Template Details"
    }
  ]
}
[/block]


The Green dot indicates the approved templates. You can replicate these pre-approved templates in CleverTap to start sending campaigns. Refer to the section below to understand how to add templates in CleverTap.

# Adding Message Template

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the message templates:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > WhatsApp Connect_ > \_Provider Nickname_ from the CleverTap dashboard. 
2. Select the _Templates_ option, and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/130b3f6-non_CT_approved_templates.jpg",
        "Create a New Template",
        2174
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Template "
    }
  ]
}
[/block]


3. Enter the template name in the _Namespace_ field.
4. Choose the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, and _Location_.
5. You can choose to use the Limited Time Offer template for your message. For more information, refer to [Limited Time Offer Template.](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
6. Enter the message content.
7. Select _Footer_ to add a footer text and a button (Quick Reply or a Call To Action).
8. Select the _Language_ in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9927992-Generic_template_create.jpg",
        "",
        "Define Template Content for Haptik"
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true,
      "caption": "Define Template Content"
    }
  ]
}
[/block]


7. Click **Save Template**.

# Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template.
2. Click _Send Test_.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click **Send Test**.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fbf00f7-test_template.png",
        "Test Message Template",
        1304
      ],
      "align": "center",
      "border": true,
      "caption": "Test a Message Template"
    }
  ]
}
[/block]


The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Haptik team to debug the issue, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2fc576b-Whatsapp_Infobip_send_test.png",
        "Successful Delivery Response",
        "Screen shows the format of a successful delivery response after sending a WhatsApp Message"
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Successful Delivery Response"
    }
  ]
}
[/block]


# Create Campaign

To create a WhatsApp campaign using Haptik as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

# Creating a Journey

To create a WhatsApp journey using Haptik as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.