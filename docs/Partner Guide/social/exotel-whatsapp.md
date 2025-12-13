---
title: Exotel
excerpt: >-
  This guide demonstrates how to integrate Exotel with CleverTap for WhatsApp
  communication
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 🚧 Note
> 
> This integration is completed by Exotel and they are dedicated to maintaining and enhancing it. The CleverTap \<> Exotel integration has undergone stringent testing to ensure its seamless functionality. In the event of any questions or issues, users must rely on Exotel for support and resolution.

# Introduction

CleverTap users can now leverage the following WhatsApp capabilities of [Exotel](https://exotel.com/) to communicate with their customers. Communications include:

- Sending just-in-time offers to customers to drive purchases
- Gathering feedback on the services 
- Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

- You must have WhatsApp add-on enabled on the Clevertap account in addition to the essentials price plan.
- Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
- Ensure that you have the infra URL and credentials from Exotel.

If you want to activate a new phone number with WhatsApp business API via Exotel, contact your account manager or email [hello@exotel.in](mailto:hello@exotel.in).

# Integrate Exotel with CleverTap

This process involves the following three steps:

1. Find Exotel Details
2. Configure CleverTap Dashboard
3. Set up CleverTap callbacks in Exotel

## Find Exotel Details

We recommend that you keep the following information handy before starting with configuration on the CleverTap dashboard:

- **API Credentials**: To obtain the _API KEY_, _API TOKEN_, and _Account sid_, log in to your Exotel account and navigate to the _Settings_ > _API Settings_ page from the Exotel dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e388cc6-API_Settings_page.png",
        "Locate Exotel Details",
        2874
      ],
      "align": "center",
      "border": true,
      "caption": "Exotel Credentials"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ from the CleverTap dashboard.
2. Click **+ Add Provider** and select Generic (Other) from the dropdown. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a7e44c5-Whatsapp_Common_Provider_Setup.png",
        null,
        "Provider Setup"
      ],
      "align": "center",
      "sizing": "70% ",
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
    "1-1": "Enter the nickname as _Exotel_ ",
    "2-0": "WhatsApp Business Number",
    "2-1": "Enter your phone number onboarded to WhatsApp API by Exotel.",
    "3-0": "Request Type",
    "3-1": "Ensure the Request Type is _Post_ ",
    "4-0": "HTTP Endpoint",
    "4-1": "Enter  \nHTTP Endpoint as: <https://api.in.exotel.com/v2/accounts/Exotel/messages/clevertap/whatsapp>  \n  \nEnsure that you replace Exotel with your **Account SID.**",
    "5-0": "Authentication",
    "5-1": "Select _Basic Authentication_  and enter the Username and Password (From step 1)"
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


4. Select the _Mark this as default_ checkbox to make this service provider the default provider to send a WhatsApp message.
5. To send an automatic reply to users who message on WhatsApp, but are not tracked on the CleverTap dashboard, you can select the _Set auto reply for users not tracked on CleverTap_ checkbox. 
6. (Optional) You can set the _Maximum Concurrent API requests_ anywhere between 30 to 1000 requests. Consider your requirements and the provider's limitations to define this value.
7. Send a Test WhatsApp notification: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c384922-sendtest.png",
        "Send Test Message on WhatsApp",
        1488
      ],
      "align": "center",
      "border": true,
      "caption": "Send Test Message on WhatsApp"
    }
  ]
}
[/block]


   To ensure that the integration is successful:  
   a. Click the _Send Test WhatsApp_ hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:  
               i. Save the business contact and send a WhatsApp message to that number.  
              ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.  
             iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:  
      _ **Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.  
      _ **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on _Send Test_, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

7. Click **Save** to save the details. 

## Set up CleverTap Callbacks in Exotel

Further, share the following details of your WhatsApp-enabled phone number with Exotel support at \*[messaging-pm-team@exotel.in](mailto:messaging-pm-team@exotel.in) for enabling WhatsApp integration with Clevertap.

- URL: Exotel.abc.net port XXXX
- Username: Abcorp
- Password: XXXXXXXX
- Phone number: 734550771X
- Account SID: Abc_1
- Delivery Report Callback URL
- Inbound Message Callback URL 

You can copy the _Delivery Report Callback URL_ and _Inbound Message Callback URL_ from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7b30b47-generic_Whatsapp_Provider_configuration.jpg",
        "",
        "Setup Callbacks"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Setup Callbacks"
    }
  ]
}
[/block]


Upon receiving the request, the support team configures the callbacks with your WhatsApp phone number, and the integration is confirmed (within 24 hours) post which you can proceed with creating campaigns. 

> 🚧 Note:
> 
> To use templates whitelisted on the META business manager dashboard provided by Exotel, you need to add them to the Clevertap dashboard.

For more information and queries about the Exotel integration, you can write to [hello@exotel.com](mailto:hello@exotel.com).

## Adding Message Template

> 📘 Naming WhatsApp Templates
> 
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
> 
> For example, if you have multiple provider configurations, such as _Phone_1, phone_2_, you can use the same template name once within _Phone_1 and Phone_2_.

To create WhatsApp campaigns, you need to have pre-approved WhatsApp message templates saved in the CleverTap dashboard. Follow the procedure below to add the templates.

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ > _Provider Nickname_ in the CleverTap dashboard. Further, Select the _Templates_ option and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70d1653-non_CT_approved_templates.jpg",
        "Create a New Template",
        2174
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Template"
    }
  ]
}
[/block]


2. Enter the template name in the _namespace_ field.
3. Choose the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, and _Location_.
4. You can choose to use  the **Limited Time Offer** template for your message. For more information, refer to [Limited Time Offer Template.](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
5. Enter the message content.
6. You can also add a Footer text and a Button (Quick Reply or a Call To Action).
7. You can also choose the language in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/641e6d5-Generic_template_create.jpg",
        "",
        "Define Template content for Exotel"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Template Content"
    }
  ]
}
[/block]


7. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template. 
2. Click _Send Test_.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click _Send Test_.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fbf00f7-test_template.png",
        "Test a Message Template",
        1304
      ],
      "align": "center",
      "border": true,
      "caption": "Test a Message Template"
    }
  ]
}
[/block]


The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Exotel team to debug the issue, as shown in the following figure:

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


## Create Campaign

To create a WhatsApp campaign using Exotel as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Creating a Journey

To create a WhatsApp journey using ValueFirst as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.