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

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback on the services
* Keeping customers informed and more

## Prerequisites for Integration

* You must have WhatsApp add-on enabled on the Clevertap account in addition to the basic price plan.
* You need to have an XML account for WhatsApp channel API. (Raise a request at [connectors@vfirst.com](mailto:connectors@vfirst.com) to get the WhatsApp XML account in case you do not have one). Expect a response with the WhatsApp account details (Username, Password, WhatsApp number.)
* Ensure that the IP (3.108.187.149) is whitelisted against the XML account at the ValueFirst side.

# Integrate ValueFirst with CleverTap

This process involves the following three steps:

1. Signup for ValueFirst-CleverTap Integration Plugin
2. Configure ValueFirst 
3. Configure CleverTap dashboard.

## Signup for ValueFirst-CleverTap Integration Plugin

To get started with the integration, the first step is to sign up for ValueFirst-CleverTap WhatsApp Integration. Click this [link](https://ct.vfplugin.com/signup) to sign up. Signup by entering the Name, Email, Company name, and Password.

<Image title="valuefirst-whatsapp.png" alt={1266} align="center" className="border" width="80%" border={true} src="https://files.readme.io/c7f3174-valuefirst-whatsapp.png" />

The next step is to log into the ValueFirst portal and configure the connection.

## Configure ValueFirst

1. To configure the ValueFirst-WhatsApp connection, you need to log in to the ValueFirst portal using the credentials configured in the previous step. 

<Image title="valuefirst.png" alt={1284} align="center" className="border" width="80%" border={true} src="https://files.readme.io/7f8f097-valuefirst.png" />

2. After you log in, enter the credentials - *Username*, *Password*, *WhatsApp Phone number* (received as part of a prerequisite) and click **Authenticate** to configure the connector. 

<Image title="valuefirst1.png" alt={1302} align="center" className="border" width="80%" border={true} src="https://files.readme.io/c2f9111-valuefirst1.png" />

After successful authentication, you will get a message - *Successfully authenticated ValueFirst account*

You can copy the webhook URL available at the bottom (as shown in the image above) and share it with the ValueFirst sales or support team for inbound message and delivery reports configuration.

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Channels* > *WhatsApp* from the CleverTap dashboard.
2. Click **+ Add Provider** and select Generic (Other) from the dropdown. 

<Image title="Valuefirst sendtest.png" alt={1076} align="center" className="border" border={true} src="https://files.readme.io/131f79a-Valuefirst_sendtest.png" />

3. Enter the following details:

| Field                    | Description                                                            |
| :----------------------- | :--------------------------------------------------------------------- |
| Provider                 | Select *Other (Generic)* from the dropdown list.                       |
| Nickname                 | Enter the nickname as *ValueFirst*                                     |
| WhatsApp Business Number | Enter your phone number onboarded to WhatsApp API by ValueFirst.       |
| Request Type             | Ensure Request Type is *Post*                                          |
| HTTP End point           | You need to paste the Auth URL from ValueFirst post its configuration. |

4. Click **Header** > Enter the *Key name* as Authorization and paste the *Basic Token* Value from the ValueFirst plugin.

<Image title="basic token.png" alt={768} align="center" className="border" width="80%" border={true} src="https://files.readme.io/74a5341-basic_token.png" />

5. Select the *Mark this as default* checkbox to make this service provider the default provider to send a WhatsApp message.
6. To send an automatic reply to users who message on WhatsApp, but are not tracked on the CleverTap dashboard, you can select the *Set auto reply for users not tracked on CleverTap* checkbox. 
7. Send a Test WhatsApp notification: 

![](https://files.readme.io/c384922-sendtest.png "sendtest.png")

   To ensure that the integration is successful:\
   a. Click the *Send Test WhatsApp* hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:\
      i. Save the business contact and send a WhatsApp message to that number.\
      ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.\
      iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:\
      ***Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.\&#xA;* **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on *Send Test*, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

8. Click **Save** to save the details.

You can find the Auth URL under the *CleverTap* tab on the ValueFirst connector as shown below.

<Image title="auth URL.png" alt={1106} align="center" className="border" width="80%" border={true} src="https://files.readme.io/eef72c6-auth_URL.png" />

## Configure CleverTap Webhooks

To configure the webhooks, you need to:

Copy the *Delivery report callback URL* and  *Inbound Message Callback URL*  from CleverTap and paste them into Valuefirst’s *Status Callback* and *Incoming Callback* fields respectively

You can find the *Delivery report callback URL*  and *Inbound Message Callback URL*  under the *Provider Setup* page ( *Settings > Channels > WhatsApp > Provider Nickname)*

<Image title="copy calbacks.png" alt={1450} align="center" className="border" width="80%" border={true} src="https://files.readme.io/7574030-copy_calbacks.png" />

To paste the callback URLs, navigate to ValueFirst-CleverTap WhatsApp Plugin > select the *CleverTap* tab next to the *ValueFirst* tab and paste the *Status Callback* & *Incoming Callback*. After pasting the URLs, click **Save** to save the configuration.

<Image title="callbacks.png" alt={1168} align="center" className="border" width="80%" border={true} src="https://files.readme.io/1af3997-callbacks.png" />

## Adding Message Template

In order to create WhatsApp campaigns, you need to have pre-approved WhatsApp message templates saved in the CleverTap dashboard. Follow the procedure below to add the templates.

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *Provider Nickname* in the CleverTap dashboard. Further Select the *Templates* option, and click **+Template**.

<Image title="Valuefirst templates.png" alt={2150} align="center" className="border" width="80%" border={true} src="https://files.readme.io/0b4ba63-Valuefirst_templates.png" />

2. Enter the template name in the *namespace* field.
3. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*
4. Enter the message content.
5. You can also choose to add a Footer text and a Button (Quick Reply or a Call To Action).
6. You can also choose the language in which you want to display the message.

<Image title="whatsapp template addition.png" alt={2036} align="center" className="border" width="80%" border={true} src="https://files.readme.io/05f7706-whatsapp_template_addition.png" />

7. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Hover over the desired template for which you want to send a test notification.
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click *Send Test*.  

<Image title="test template.png" alt={1304} align="center" className="border" border={true} src="https://files.readme.io/fbf00f7-test_template.png" />

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the ValueFirst team to debug the issue, as shown in the following figure:

<Image title="sendtest campaign.png" alt={728} align="center" className="border" width="80%" border={true} src="https://files.readme.io/363a140-sendtest_campaign.png" />

## Create Campaign

To create a WhatsApp campaign using ValueFirst as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Creating a Journey

To create a WhatsApp journey using ValueFirst as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.
