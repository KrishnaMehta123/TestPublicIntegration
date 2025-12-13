---
title: Nexmo
excerpt: >-
  This guide demonstrates how to integrate Nexmo with CleverTap for WhatsApp
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
# Introduction

The primary vendor CleverTap uses in the backend for WhatsApp communications is Nexmo. Contact our sales team at [sales@clevertap.com](mailto:sales@clevertap.com) to enable WhatsApp for your organization.

CleverTap users can now leverage the following WhatsApp capabilities of [Nexmo](https://www.vonage.com/communications-apis/) to communicate with their customers:

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback on the services 
* Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

* You must have WhatsApp add-on enabled on the Clevertap account in addition to the essentials price plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
* Ensure that you have all the credentials from Nexmo handy.

# Integrate Nexmo with CleverTap

This process involves the following three major steps:

1. Find Nexmo Details.
2. Configure CleverTap Dashboard.
3. Set up CleverTap callbacks in Nexmo.

## Find Nexmo Details

We recommend that you keep the following information handy before starting with the configuration on the CleverTap dashboard:

* **Mobile Number**: It is the mobile number on which the WhatsApp business account is activated. 

* **App ID** :  To obtain the *App ID*, navigate to the *Build and Manage* > *Applications* page from the Nexmo dashboard.

<Image title="Locate Nexmo Details" alt={2866} align="center" border={true} src="https://files.readme.io/85c10c7-ct_test.png">
  Nexmo Credentials
</Image>

If the application is not created, you can go to *Applications* and click + *Create a new application*.

* **Private Key:** A private key is downloaded automatically after you create a new application on the Vonage dashboard. Store this key as you may need this for future usage.

<Image title="Download Private Key" alt="Download Private Key" align="center" border={true} src="https://files.readme.io/5379bb9-private_key.png">
  Download Private Key
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* >*Channels* > *WhatsApp* from the CleverTap dashboard.
2. Click **+ Add Provider**. The *Add WhatsApp provider* screen displays.
3. Select *Nexmo* from the dropdown displays. 

<Image title="Configure Nexmo Details on CleverTap" alt={1142} align="center" border={true} src="https://files.readme.io/4595f55-nexmo_final_.png">
  Configure Provider
</Image>

4. Now, enter the following credentials obtained from the [Nexmo dashboard](https://docs.clevertap.com/docs/nexmo-whatsapp#find-nexmo-details) in the above step on the *Provider credentials* screen:

   * Private Key
   * App ID

5. To send an automatic reply to users who message on WhatsApp, but are not tracked on the CleverTap dashboard, you can select the *Set auto-reply for users not tracked on CleverTap* checkbox. 

6. Send a Test WhatsApp notification: 

<Image title="Send a Test WhatsApp Message" alt="Send a Test WhatsApp Message" align="center" border={true} src="https://files.readme.io/c384922-sendtest.png">
  Send a Test WhatsApp Message
</Image>

   To ensure that the integration is successful:\
   a. Click the *Send Test WhatsApp* hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:\
      i. Save the business contact and send a WhatsApp message to that number.\
      ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.\
      iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:\
      ***Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.\&#xA;* **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on *Send Test*, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

7. Click **Save** to save the details. 

## Set up CleverTap Callbacks in Nexmo

You must copy the *Inbound Message Callback URL* and *Status Callback URL* from the CleverTap *Provider credentials* screen and paste them into the Nexmo dashboard. This helps you receive incoming messages and the delivery status of outgoing messages.

To add/paste the callback URLs, login to your Nexmo dashboard > navigate to *Applications* > Click **Edit** under the *Messages* section as shown in the image below.

<Image title="Configure Callback URLs" alt="Callback URLs" align="center" border={true} src="https://files.readme.io/6168c57-ct_test.png">
  Callback URLs
</Image>

> 📘 Callback Payload Version
>
> Ensure that you select the payload version as 0.1 in the Nexmo dashboard to receive the callbacks properly. Refer to the image below for a better understanding.

<Image title="Nexmo Capablities" alt={2266} align="center" border={true} src="https://files.readme.io/1e1b478-payload_version.png">
  Capabilities
</Image>

## Adding Message Template

> 📘 Naming WhatsApp Templates
>
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
>
> For example, if you have multiple provider configurations, such as *Phone\_1, phone\_2*, you can use the same template name once within *Phone\_1 and Phone\_2*.

To create WhatsApp campaigns, you need to have pre-approved WhatsApp message templates saved in the CleverTap dashboard. Follow the procedure below to add the templates.

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *Provider Nickname* in the CleverTap dashboard. Further, select the *Templates* option, and click **+Template**.

<Image title="Add a Message Template" alt={2164} align="center" border={true} src="https://files.readme.io/302521b-nexmo_whatsapp_.png">
  Adding Message Template
</Image>

2. Enter the namespace in the *Namespace* field from your Facebook Business Manager dashboard. Refer to the screenshot below for a better understanding. You need to enter this only for the first template configuration.

<Image title="Enter the namespace in the Namespace field" alt="Template Namespace" align="center" border={true} src="https://files.readme.io/8c2bc47-template_name.png">
  Template Namespace
</Image>

3. Enter the template name from the Facebook Business Manager page in the *Template Name* field.

<Image title="Enter Template Name" alt={1825} align="center" border={true} src="https://files.readme.io/0c845a7-temp_name.png">
  Enter Template Name
</Image>

4. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*
5. Enter the message content.
6. You can also choose to add a Footer text and a Button (Quick Reply or a Call To Action).
7. You can also choose the language in which you want to display the message.

<Image title="Enter Template Content" alt={2160} align="center" border={true} src="https://files.readme.io/5a52036-nexmo_template.png">
  Define Template Body
</Image>

8. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Hover over the desired template for which you want to send a test notification.
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click *Send Test*.  

<Image title="Test Message Template" alt={1304} align="center" border={true} src="https://files.readme.io/fbf00f7-test_template.png">
  Test Message Template
</Image>

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Nexmo team to debug the issue, as shown in the following figure:

<Image title="Validate the Test Response" alt={728} align="center" width="80%" border={true} src="https://files.readme.io/363a140-sendtest_campaign.png">
  Validate the Test Response
</Image>

## Create Campaign

To create a WhatsApp campaign using Nexmo as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Creating a Journey

To create a WhatsApp journey using Nexmo as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.
