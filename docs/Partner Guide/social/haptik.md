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

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback on the services 
* Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

* You must have a WhatsApp add-on enabled on the Clevertap account in addition to the essentials price plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
* You must have Haptik's WhatsApp Business API 

# Integrate Haptik with CleverTap

This process involves the following three steps:

1. [Find Haptik Credentials](doc:haptik#find-haptik-credentials)
2. [Configure CleverTap Dashboard](doc:haptik#configure-clevertap-dashboard)
3. [Set up CleverTap callbacks in Haptik](doc:haptik#set-up-clevertap-callbacks-in-haptik)

## Find Haptik Credentials

We recommend that you keep the *Callback URL* and *Token* details handy before starting with the configuration on the CleverTap dashboard:

To find these credentials:

1. Navigate to your Haptik *Conversation Studio* platform.
2. Open your bot account.
3. Navigate to *Business Manager* > *Channels* > *Platform Deployments*. 
4. Select CleverTap from the *Platform* drop-down. 

Copy the credentials for configuring the CleverTap dashboard:

* Callback URL
* Token

<Image title="Locate Haptik Credentials" alt={2552} align="center" border={true} src="https://files.readme.io/95ffcb4-haptik_configuration.png">
  Haptik Credentials
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and *Log in to Facebook*. 

<Image alt="Provider Setup" align="center" width="80% " border={true} src="https://files.readme.io/23dde0f-Whatsapp_Common_Provider_Setup.png">
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
        Enter the nickname as *Haptik* or Haptik \<10 digit phone number> for easy reference.
      </td>
    </tr>

    <tr>
      <td>
        WhatsApp Business Number
      </td>

      <td>
        Enter your phone number onboarded to WhatsApp API by Haptik.
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
        Paste the *Callback URL* from Haptik's *Platform Deployments* tab as illustrated in the previous step.  

        Ensure that the URL is in HTTPS format, i.e, your URL must begin with **https\://**.
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click *Header* > and then Enter the Key name as *Token* and paste the token value copied from Haptik's *Platform Deployments* tab, as illustrated in the previous step.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Callback URL
>
> While pasting the Callback URL from the Haptik dashboard to the CleverTap dashboard, ensure that the URL is in HTTPS format, i.e your URL must begin with **https\://**.

4. Select the *Mark this as default* checkbox to make this service provider the default provider to send a WhatsApp message.
5. To send an automatic reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard, select the *Set auto-reply for users not tracked on CleverTap* checkbox. 
6. (Optional) You can set the *Maximum Concurrent API requests* anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save** to save the details. 

## Set Up CleverTap Callbacks in Haptik

To set up the CleverTap callbacks:

1. Copy the *Delivery Report Callback URL*  from the CleverTap dashboard. You can find the Callback URLs under the Provider *Setup* page ( *Settings* > *Channels* > *WhatsApp* > *Haptik*)

<Image title="Configure Callbacks" alt={938} align="center" border={true} src="https://files.readme.io/0479084-callback_haptik.png">
  Configure Callbacks
</Image>

2. Paste the callback URL:\
   a. Open your Haptik bot account > navigate to *Business Manager* > *Channels* > *Platform Deployments*.\
   b. Paste the callback URL under the *CleverTap Webhook URL* as illustrated in the following image.

<Image title="Paste the Callback" alt={2552} align="center" border={true} src="https://files.readme.io/4043bf8-haptik_configuration_callback.png">
  Configure Callbacks
</Image>

# Finding Template Details

You need to replicate the details of your pre-approved templates on CleverTap. To find the details of your pre-approved templates on Haptik, navigate to the *Template* section from the Haptik dashboard, as shown below.

<Image title="Locate Template Details" alt={1314} align="center" border={true} src="https://files.readme.io/bdae381-haptik_templates.png">
  Find Template Details
</Image>

The Green dot indicates the approved templates. You can replicate these pre-approved templates in CleverTap to start sending campaigns. Refer to the section below to understand how to add templates in CleverTap.

# Adding Message Template

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the message templates:

1. Navigate to *Settings* > *Channels* > *WhatsApp* > WhatsApp Connect *>\_Provider Nickname* from the CleverTap dashboard. 
2. Select the *Templates* option, and click **+Template**.

<Image title="Create a New Template" alt={2174} align="center" border={true} src="https://files.readme.io/130b3f6-non_CT_approved_templates.jpg">
  Create a New Template 
</Image>

3. Enter the template name in the *Namespace* field.
4. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*.
5. You can choose to use the Limited Time Offer template for your message. For more information, refer to [Limited Time Offer Template.](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
6. Enter the message content.
7. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).
8. Select the *Language* in which you want to display the message.

<Image alt="Define Template Content for Haptik" align="center" width="100% " border={true} src="https://files.readme.io/9927992-Generic_template_create.jpg">
  Define Template Content
</Image>

7. Click **Save Template**.

# Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template.
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click **Send Test**.  

<Image title="Test Message Template" alt={1304} align="center" border={true} src="https://files.readme.io/fbf00f7-test_template.png">
  Test a Message Template
</Image>

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Haptik team to debug the issue, as shown in the following figure:

<Image title="Successful Delivery Response" alt="Screen shows the format of a successful delivery response after sending a WhatsApp Message" align="center" width="smart" border={true} src="https://files.readme.io/2fc576b-Whatsapp_Infobip_send_test.png">
  Successful Delivery Response
</Image>

# Create Campaign

To create a WhatsApp campaign using Haptik as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

# Creating a Journey

To create a WhatsApp journey using Haptik as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp) for detailed instructions.
