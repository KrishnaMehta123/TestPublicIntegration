---
title: ValueFirst Digital
excerpt: >-
  This guide demonstrates how to integrate ValueFirst Digital with CleverTap for
  WhatsApp communication
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 🚧 Note
> 
> This integration is completed by ValueFirst, and they are dedicated to maintaining and enhancing it. The CleverTap \<> ValueFirst integration has undergone stringent testing to ensure its seamless functionality. In the event of any questions or issues, users must rely on ValueFirst for support and resolution.

# Introduction

CleverTap users can now leverage the WhatsApp capabilities of ValueFirst Digital to communicate with their customers. The communication includes:

- Sending just-in-time offers to customers to drive purchases
- Gathering feedback on the services
- Keeping customers informed and more

## Prerequisites for Integration

- You must have WhatsApp add-on enabled on the Clevertap account in addition to the basic price plan.
- You need to have an XML account for WhatsApp channel API. (Raise a request at [connectors@vfirst.com](mailto:connectors@vfirst.com) to get the WhatsApp XML account in case you do not have one). Expect a response with the WhatsApp account details (Username, Password, WhatsApp number.)
- Ensure that the IP (3.108.187.149) is whitelisted against the XML account at the ValueFirst side.

# Integrate ValueFirst with CleverTap

This process involves the following three steps:

1. Signup for ValueFirst-CleverTap Integration Plugin
2. Configure ValueFirst 
3. Configure CleverTap dashboard.

## Signup for ValueFirst-CleverTap Integration Plugin

To get started with the integration, the first step is to sign up for ValueFirst-CleverTap WhatsApp Integration. Click this [link](https://ct.vfplugin.com/signup) to sign up. Signup by entering the Name, Email, Company name, and Password.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7f3174-valuefirst-whatsapp.png",
        "valuefirst-whatsapp.png",
        1266
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



The next step is to log into the ValueFirst portal and configure the connection.

## Configure ValueFirst

1. To configure the ValueFirst-WhatsApp connection, you need to log in to the ValueFirst portal using the credentials configured in the previous step. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7f8f097-valuefirst.png",
        "valuefirst.png",
        1284
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



2. After you log in, enter the credentials - _Username_, _Password_, _WhatsApp Phone number_ (received as part of a prerequisite) and click **Authenticate** to configure the connector. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2f9111-valuefirst1.png",
        "valuefirst1.png",
        1302
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



After successful authentication, you will get a message - _Successfully authenticated ValueFirst account_

You can copy the webhook URL available at the bottom (as shown in the image above) and share it with the ValueFirst sales or support team for inbound message and delivery reports configuration.

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ from the CleverTap dashboard.
2. Click **+ Add Provider** and select Generic (Other) from the dropdown. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/131f79a-Valuefirst_sendtest.png",
        "Valuefirst sendtest.png",
        1076
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



3. Enter the following details:

| Field                    | Description                                                            |
| :----------------------- | :--------------------------------------------------------------------- |
| Provider                 | Select _Other (Generic)_ from the dropdown list.                       |
| Nickname                 | Enter the nickname as _ValueFirst_                                     |
| WhatsApp Business Number | Enter your phone number onboarded to WhatsApp API by ValueFirst.       |
| Request Type             | Ensure Request Type is _Post_                                          |
| HTTP End point           | You need to paste the Auth URL from ValueFirst post its configuration. |

4. Click **Header** > Enter the _Key name_ as Authorization and paste the _Basic Token_ Value from the ValueFirst plugin.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74a5341-basic_token.png",
        "basic token.png",
        768
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



5. Select the _Mark this as default_ checkbox to make this service provider the default provider to send a WhatsApp message.
6. To send an automatic reply to users who message on WhatsApp, but are not tracked on the CleverTap dashboard, you can select the _Set auto reply for users not tracked on CleverTap_ checkbox. 
7. Send a Test WhatsApp notification: 

![](https://files.readme.io/c384922-sendtest.png "sendtest.png")

   To ensure that the integration is successful:  
   a. Click the _Send Test WhatsApp_ hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:  
      i. Save the business contact and send a WhatsApp message to that number.  
      ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.  
      iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:  
      _ **Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.  
      _ **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on _Send Test_, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

8. Click **Save** to save the details.

You can find the Auth URL under the _CleverTap_ tab on the ValueFirst connector as shown below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eef72c6-auth_URL.png",
        "auth URL.png",
        1106
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



## Configure CleverTap Webhooks

To configure the webhooks, you need to:

Copy the _Delivery report callback URL_ and  _Inbound Message Callback URL_  from CleverTap and paste them into Valuefirst’s _Status Callback_ and _Incoming Callback_ fields respectively

You can find the _Delivery report callback URL_  and _Inbound Message Callback URL_  under the _Provider Setup_ page ( _Settings > Channels > WhatsApp > Provider Nickname)_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7574030-copy_calbacks.png",
        "copy calbacks.png",
        1450
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



To paste the callback URLs, navigate to ValueFirst-CleverTap WhatsApp Plugin > select the _CleverTap_ tab next to the _ValueFirst_ tab and paste the _Status Callback_ & _Incoming Callback_. After pasting the URLs, click **Save** to save the configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1af3997-callbacks.png",
        "callbacks.png",
        1168
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



## Adding Message Template

In order to create WhatsApp campaigns, you need to have pre-approved WhatsApp message templates saved in the CleverTap dashboard. Follow the procedure below to add the templates.

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > _Provider Nickname_ in the CleverTap dashboard. Further Select the _Templates_ option, and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0b4ba63-Valuefirst_templates.png",
        "Valuefirst templates.png",
        2150
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



2. Enter the template name in the _namespace_ field.
3. Choose the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, and _Location_
4. Enter the message content.
5. You can also choose to add a Footer text and a Button (Quick Reply or a Call To Action).
6. You can also choose the language in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05f7706-whatsapp_template_addition.png",
        "whatsapp template addition.png",
        2036
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



7. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Hover over the desired template for which you want to send a test notification.
2. Click _Send Test_.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click _Send Test_.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fbf00f7-test_template.png",
        "test template.png",
        1304
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the ValueFirst team to debug the issue, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/363a140-sendtest_campaign.png",
        "sendtest campaign.png",
        728
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



## Create Campaign

To create a WhatsApp campaign using ValueFirst as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Creating a Journey

To create a WhatsApp journey using ValueFirst as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.