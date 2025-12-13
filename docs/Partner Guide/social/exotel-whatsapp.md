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

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback on the services 
* Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

* You must have WhatsApp add-on enabled on the Clevertap account in addition to the essentials price plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
* Ensure that you have the infra URL and credentials from Exotel.

If you want to activate a new phone number with WhatsApp business API via Exotel, contact your account manager or email [hello@exotel.in](mailto:hello@exotel.in).

# Integrate Exotel with CleverTap

This process involves the following three steps:

1. Find Exotel Details
2. Configure CleverTap Dashboard
3. Set up CleverTap callbacks in Exotel

## Find Exotel Details

We recommend that you keep the following information handy before starting with configuration on the CleverTap dashboard:

* **API Credentials**: To obtain the *API KEY*, *API TOKEN*, and *Account sid*, log in to your Exotel account and navigate to the *Settings* > *API Settings* page from the Exotel dashboard. 

<Image title="Locate Exotel Details" alt={2874} align="center" border={true} src="https://files.readme.io/e388cc6-API_Settings_page.png">
  Exotel Credentials
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and select Generic (Other) from the dropdown. 

<Image alt="Provider Setup" align="center" width="70% " border={true} src="https://files.readme.io/a7e44c5-Whatsapp_Common_Provider_Setup.png">
  Provider Setup
</Image>

3. Enter the following details:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Provider
      </td>

      <td>
        Select *Other (Generic)* from the dropdown list.
      </td>
    </tr>

    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter the nickname as *Exotel* 
      </td>
    </tr>

    <tr>
      <td>
        WhatsApp Business Number
      </td>

      <td>
        Enter your phone number onboarded to WhatsApp API by Exotel.
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Ensure the Request Type is *Post* 
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Enter\
        HTTP Endpoint as: [https://api.in.exotel.com/v2/accounts/Exotel/messages/clevertap/whatsapp](https://api.in.exotel.com/v2/accounts/Exotel/messages/clevertap/whatsapp)  

        Ensure that you replace Exotel with your **Account SID.**
      </td>
    </tr>

    <tr>
      <td>
        Authentication
      </td>

      <td>
        Select *Basic Authentication*  and enter the Username and Password (From step 1)
      </td>
    </tr>
  </tbody>
</Table>

4. Select the *Mark this as default* checkbox to make this service provider the default provider to send a WhatsApp message.
5. To send an automatic reply to users who message on WhatsApp, but are not tracked on the CleverTap dashboard, you can select the *Set auto reply for users not tracked on CleverTap* checkbox. 
6. (Optional) You can set the *Maximum Concurrent API requests* anywhere between 30 to 1000 requests. Consider your requirements and the provider's limitations to define this value.
7. Send a Test WhatsApp notification: 

<Image title="Send Test Message on WhatsApp" alt={1488} align="center" border={true} src="https://files.readme.io/c384922-sendtest.png">
  Send Test Message on WhatsApp
</Image>

   To ensure that the integration is successful:\
   a. Click the *Send Test WhatsApp* hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:\
               i. Save the business contact and send a WhatsApp message to that number.\
              ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.\
             iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:\
      ***Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.\&#xA;* **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on *Send Test*, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

7. Click **Save** to save the details. 

## Set up CleverTap Callbacks in Exotel

Further, share the following details of your WhatsApp-enabled phone number with Exotel support at \*[messaging-pm-team@exotel.in](mailto:messaging-pm-team@exotel.in) for enabling WhatsApp integration with Clevertap.

* URL: Exotel.abc.net port XXXX
* Username: Abcorp
* Password: XXXXXXXX
* Phone number: 734550771X
* Account SID: Abc\_1
* Delivery Report Callback URL
* Inbound Message Callback URL 

You can copy the *Delivery Report Callback URL* and *Inbound Message Callback URL* from the CleverTap dashboard.

<Image alt="Setup Callbacks" align="center" width="80% " border={true} src="https://files.readme.io/7b30b47-generic_Whatsapp_Provider_configuration.jpg">
  Setup Callbacks
</Image>

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
> For example, if you have multiple provider configurations, such as *Phone\_1, phone\_2*, you can use the same template name once within *Phone\_1 and Phone\_2*.

To create WhatsApp campaigns, you need to have pre-approved WhatsApp message templates saved in the CleverTap dashboard. Follow the procedure below to add the templates.

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Provider Nickname* in the CleverTap dashboard. Further, Select the *Templates* option and click **+Template**.

<Image title="Create a New Template" alt={2174} align="center" border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg">
  Create a New Template
</Image>

2. Enter the template name in the *namespace* field.
3. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*.
4. You can choose to use  the **Limited Time Offer** template for your message. For more information, refer to [Limited Time Offer Template.](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
5. Enter the message content.
6. You can also add a Footer text and a Button (Quick Reply or a Call To Action).
7. You can also choose the language in which you want to display the message.

<Image alt="Define Template content for Exotel" align="center" border={true} src="https://files.readme.io/641e6d5-Generic_template_create.jpg">
  Define Template Content
</Image>

7. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template. 
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click *Send Test*.  

<Image title="Test a Message Template" alt={1304} align="center" border={true} src="https://files.readme.io/fbf00f7-test_template.png">
  Test a Message Template
</Image>

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Exotel team to debug the issue, as shown in the following figure:

<Image title="Successful Delivery Response" alt="Screen shows the format of a successful delivery response after sending a WhatsApp Message" align="center" width="smart" border={true} src="https://files.readme.io/2fc576b-Whatsapp_Infobip_send_test.png">
  Successful Delivery Response
</Image>

## Create Campaign

To create a WhatsApp campaign using Exotel as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Creating a Journey

To create a WhatsApp journey using ValueFirst as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.
