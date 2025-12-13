---
title: Infobip
excerpt: Understand how to integrate Infobip with CleverTap for WhatsApp communication
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

CleverTap users can now leverage the WhatsApp capabilities of Infobip to communicate with their customers:

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback about services 
* Keeping customers informed and more

> 🚧 Support For Integration
>
> This integration is completed by Infobip, and they are dedicated to maintaining and enhancing it. The CleverTap and Infobip integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact Infobip for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

* You must enable a WhatsApp Connect add-on on the Clevertap account in addition to the essentials price plan.
* The WhatsApp onboarding must be completed for the phone number to be used with CleverTap.
* You must have Infobip's user credentials.
* The Infobip API endpoint - *[https://clevertap-whatsapp.ibintegrations.com/api/sendmessage](https://clevertap-whatsapp.ibintegrations.com/api/sendmessage)*. 

# Integrate Infobip with CleverTap

This process involves the following three steps:

1. [Find Infobip Details](https://docs.clevertap.com/docs/infobip#find-infobip-details).
2. [Configure CleverTap Dashboard](https://docs.clevertap.com/docs/infobip#configure-clevertap-dashboard).
3. [Set Up CleverTap callbacks in Infobip](https://docs.clevertap.com/docs/infobip#set-up-clevertap-callbacks-in-infobip).

## Find Infobip Details

We recommend that you keep the *API endpoint* and *Login Credentials* handy before starting with the configuration on the CleverTap dashboard:

To find these credentials:

1. Navigate to your Infobip dashboard. 
2. [Create a new user](https://www.infobip.com/docs/essentials/manage-users#create-a-user) from *Account* > *User profile*.\
   We recommend creating a separate user for the Infobip-CleverTap WhatsApp integration. Use these user credentials to authenticate the [Infobip API](https://clevertap-whatsapp.ibintegrations.com/api/sendmessage) and provide basic authentication on the CleverTap dashboard. For more information about user management, refer to [Manage Infobip Users](https://www.infobip.com/docs/essentials/manage-users).

<Image title="Create a New User" alt="The New User screen on the Infobip dashboard to create a new user " align="center" border={true} src="https://files.readme.io/5c05b2b-Whatsapp_Infobip_create_user.png">
  Infobip Dashboard
</Image>

3. Navigate to *Channels and Numbers* > *WhatsApp* > *Senders* tab to find the WhatsApp number.
4. Copy the WhatsApp phone number and keep it handy for further use. 

<Image title="Copy WhatsApp Phone Number" alt="The sender tab on the Infobip dashboard shows the WhatsApp Number" align="center" border={true} src="https://files.readme.io/778ac61-Whatsapp_Infobip_phone_number.png">
  Copy WhatsApp Phone Number
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Channels* > *WhatsApp* >  *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and *Login to Facebook.* 

<Image alt="Add a WhatsApp Provider" align="center" border={true} src="https://files.readme.io/29282ee-Whatsapp_Common_Provider_Setup.png">
  Add a WhatsApp Provider
</Image>

3. Enter the following details: 

| Field                        | Description                                                                                                                                                            |
| :--------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Provider                     | Select *Other (Generic)* from the dropdown list.                                                                                                                       |
| Nickname                     | Enter the nickname as *Infobip* or Infobip \<10-digit phone number> for easy reference.                                                                                |
| Mobile Number                | Enter your phone number onboarded to WhatsApp API by Infobip.                                                                                                          |
| Request Type                 | Ensure the Request Type is *Post*.                                                                                                                                     |
| HTTP Endpoint                | Enter HTTP Endpoint as the following: *[https://clevertap-whatsapp.ibintegrations.com/api/sendmessage](https://clevertap-whatsapp.ibintegrations.com/api/sendmessage)* |
| Authentication               | Select *Basic Authentication* and enter the *Username* and *Password* for the user.                                                                                    |
| Delivery Report Callback URL | This URL is generated automatically. Share the URL with your Infobip account manager.                                                                                  |
| Inbound Message Callback URL | This URL is generated automatically. Share the URL with your Infobip account manager.                                                                                  |

4. (Optional) Select *Mark this as default* to make this service provider the default provider to send a WhatsApp message. 
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard. 
6. (Optional) You can set the *Maximum Concurrent API requests* anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save** to save the details. 

## Set Up CleverTap Callbacks in Infobip

You can find the Callback URLs on the CleverTap dashboard under the Provider *Setup* page. Naviagte to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* >*Infobip*. 

To set up the CleverTap callbacks, share the following with your Infobip account manager:

* Delivery Report Callback URL
* Inbound Message Callback URL
* The WhatsApp phone number that will be used in CleverTap 

<Image alt="Callback URLs" align="center" width="85% " border={true} src="https://files.readme.io/b61e35f-Whatsapp_provider_credentials.png">
  Callback URLs
</Image>

# Find or Create Templates

You can find or create WhatsApp templates from the Infobip dashboard. To do so:

1. Navigate to *Channels and Numbers* from the left menu as shown below:

<Image title="Set up WhatsApp on Infobip" alt="Screen shows the WhatsApp Tile that must be clicked to configure WhatsApp details on Infobip" align="center" border={true} src="https://files.readme.io/9169034-Whatsapp_Infobip_Integration.png">
  Set up WhatsApp on Infobip
</Image>

2. Select *WhatsApp* and click the *Senders* tab.

3. From the *Action* menu, click **View Templates.** 

<Image title="View WhatsApp Templates" alt="Screen shows the hamburger action menu on the sender tab. Click menu to show the view templates and edit configuration options" align="center" border={true} src="https://files.readme.io/62a8cd2-Whatsapp_Infobip_view_template.png">
  View WhatsApp Templates
</Image>

3. From the list of templates, search for your template. Expand the template that you want to save in the CleverTap Dashboard. 

<Image title="Expand WhatsApp Template" alt="Screen shows a list of available templates. Click the expand icon to expand the required template" align="center" src="https://files.readme.io/16fd59e-Whatsapp_Infobip_sample_template_list.png">
  Expand a WhatsApp Template
</Image>

4. Export and save the template on your machine. 

<Image title="Export WhatsApp Template" alt="Screen shows how to expand, select and export a WhatsApp Template and save it on your local machine" align="center" border={true} src="https://files.readme.io/e8125e5-Whatsapp_Infobip_export_template.png">
  Export WhatsApp Template
</Image>

> 📘 Exporting a Template
>
> The Infobip dashboard does not display all the details for the selected template. We recommend exporting the template and keeping the details handy. You can copy and paste the values from the exported template to the CleverTap dashboard to ensure you are not missing any field. For more information, refer to [Adding a WhatsApp Template in CleverTap](doc:infobip#adding-message-template).

# Add Message Template

> 📘 Naming WhatsApp Templates
>
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
>
> For example, if you have multiple provider configurations, such as *Phone\_1, phone\_2*, you can use the same template name once within *Phone\_1 and Phone\_2*.

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the message templates:

1. Navigate to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* >*Provider Nickname* from the CleverTap dashboard. 
2. Select the *Templates* option, and click **+Template**.

<Image title="Pre-Approved Message Templates" alt="The screen shows multiple pre-approved message templates for WhatsApp" align="center" border={true} src="https://files.readme.io/66956a6-non_CT_approved_templates.jpg">
  Add Pre-Approved Message Template 
</Image>

3. Enter the template name in the *Namespace* field.
4. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*.
5. You can choose to use the Limited Time Offer template for your message. For more information, refer to [Limited Time Offer Template](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
6. Enter the message content.
7. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).
8. Select the *Language* in which you want to display the message.

<Image alt="Define Template content for Infobip" align="center" border={true} src="https://files.readme.io/2939b98-Generic_template_create.jpg">
  Define Template Content
</Image>

7. Click **Save Template**.

# Test a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template.
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click **Send Test**.  

<Image title="Test WhatsApp Message" alt="Screen shows how to preview and test a WhatsApp message from the CleverTap dashboard" align="center" border={true} src="https://files.readme.io/fbf00f7-test_template.png">
  Test WhatsApp Message
</Image>

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Infobip team to debug the issue, as shown in the following figure:

<Image title="Successful Delivery Response" alt="Screen shows the format of a successful delivery response after sending a WhatsApp Message" align="center" width="smart" border={true} src="https://files.readme.io/2fc576b-Whatsapp_Infobip_send_test.png">
  Successful Delivery Response
</Image>

# Create Campaign

To create a WhatsApp campaign using Infobip as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

# Creating a Journey

To create a WhatsApp journey using Infobip as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp) for detailed instructions.
