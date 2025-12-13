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

- Sending just-in-time offers to customers to drive purchases
- Gathering feedback about services 
- Keeping customers informed and more

> 🚧 Support For Integration
> 
> This integration is completed by Infobip, and they are dedicated to maintaining and enhancing it. The CleverTap and Infobip integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact Infobip for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

- You must enable a WhatsApp Connect add-on on the Clevertap account in addition to the essentials price plan.
- The WhatsApp onboarding must be completed for the phone number to be used with CleverTap.
- You must have Infobip's user credentials.
- The Infobip API endpoint - _<https://clevertap-whatsapp.ibintegrations.com/api/sendmessage>_. 

# Integrate Infobip with CleverTap

This process involves the following three steps:

1. [Find Infobip Details](https://docs.clevertap.com/docs/infobip#find-infobip-details).
2. [Configure CleverTap Dashboard](https://docs.clevertap.com/docs/infobip#configure-clevertap-dashboard).
3. [Set Up CleverTap callbacks in Infobip](https://docs.clevertap.com/docs/infobip#set-up-clevertap-callbacks-in-infobip).

## Find Infobip Details

We recommend that you keep the _API endpoint_ and _Login Credentials_ handy before starting with the configuration on the CleverTap dashboard:

To find these credentials:

1. Navigate to your Infobip dashboard. 
2. [Create a new user](https://www.infobip.com/docs/essentials/manage-users#create-a-user) from _Account_ > _User profile_.  
   We recommend creating a separate user for the Infobip-CleverTap WhatsApp integration. Use these user credentials to authenticate the [Infobip API](https://clevertap-whatsapp.ibintegrations.com/api/sendmessage) and provide basic authentication on the CleverTap dashboard. For more information about user management, refer to [Manage Infobip Users](https://www.infobip.com/docs/essentials/manage-users).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5c05b2b-Whatsapp_Infobip_create_user.png",
        "Create a New User",
        "The New User screen on the Infobip dashboard to create a new user "
      ],
      "align": "center",
      "border": true,
      "caption": "Infobip Dashboard"
    }
  ]
}
[/block]


3. Navigate to _Channels and Numbers_ > _WhatsApp_ > _Senders_ tab to find the WhatsApp number.
4. Copy the WhatsApp phone number and keep it handy for further use. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/778ac61-Whatsapp_Infobip_phone_number.png",
        "Copy WhatsApp Phone Number",
        "The sender tab on the Infobip dashboard shows the WhatsApp Number"
      ],
      "align": "center",
      "border": true,
      "caption": "Copy WhatsApp Phone Number"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ >  _WhatsApp Connect_ from the CleverTap dashboard.
2. Click **+ Add Provider** and _ Login to Facebook._ 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29282ee-Whatsapp_Common_Provider_Setup.png",
        null,
        "Add a WhatsApp Provider"
      ],
      "align": "center",
      "border": true,
      "caption": "Add a WhatsApp Provider"
    }
  ]
}
[/block]


3. Enter the following details: 

| Field                        | Description                                                                                             |
| :--------------------------- | :------------------------------------------------------------------------------------------------------ |
| Provider                     | Select _Other (Generic)_ from the dropdown list.                                                        |
| Nickname                     | Enter the nickname as _Infobip_ or Infobip \<10-digit phone number> for easy reference.                 |
| Mobile Number                | Enter your phone number onboarded to WhatsApp API by Infobip.                                           |
| Request Type                 | Ensure the Request Type is _Post_.                                                                      |
| HTTP Endpoint                | Enter HTTP Endpoint as the following: _<https://clevertap-whatsapp.ibintegrations.com/api/sendmessage>_ |
| Authentication               | Select _Basic Authentication_ and enter the _Username_ and _Password_ for the user.                     |
| Delivery Report Callback URL | This URL is generated automatically. Share the URL with your Infobip account manager.                   |
| Inbound Message Callback URL | This URL is generated automatically. Share the URL with your Infobip account manager.                   |

4. (Optional) Select _Mark this as default_ to make this service provider the default provider to send a WhatsApp message. 
5. (Optional) Select _Set auto-reply for users not tracked on CleverTap_ to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard. 
6. (Optional) You can set the _Maximum Concurrent API requests_ anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save** to save the details. 

## Set Up CleverTap Callbacks in Infobip

You can find the Callback URLs on the CleverTap dashboard under the Provider _Setup_ page. Naviagte to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ >_Infobip_. 

To set up the CleverTap callbacks, share the following with your Infobip account manager:

- Delivery Report Callback URL
- Inbound Message Callback URL
- The WhatsApp phone number that will be used in CleverTap 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b61e35f-Whatsapp_provider_credentials.png",
        null,
        "Callback URLs"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Callback URLs"
    }
  ]
}
[/block]


# Find or Create Templates

You can find or create WhatsApp templates from the Infobip dashboard. To do so:

1. Navigate to _Channels and Numbers_ from the left menu as shown below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9169034-Whatsapp_Infobip_Integration.png",
        "Set up WhatsApp on Infobip",
        "Screen shows the WhatsApp Tile that must be clicked to configure WhatsApp details on Infobip"
      ],
      "align": "center",
      "border": true,
      "caption": "Set up WhatsApp on Infobip"
    }
  ]
}
[/block]


2. Select _WhatsApp_ and click the _Senders_ tab.

3. From the _Action_ menu, click **View Templates.** 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/62a8cd2-Whatsapp_Infobip_view_template.png",
        "View WhatsApp Templates",
        "Screen shows the hamburger action menu on the sender tab. Click menu to show the view templates and edit configuration options"
      ],
      "align": "center",
      "border": true,
      "caption": "View WhatsApp Templates"
    }
  ]
}
[/block]


3. From the list of templates, search for your template. Expand the template that you want to save in the CleverTap Dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/16fd59e-Whatsapp_Infobip_sample_template_list.png",
        "Expand WhatsApp Template",
        "Screen shows a list of available templates. Click the expand icon to expand the required template"
      ],
      "align": "center",
      "caption": "Expand a WhatsApp Template"
    }
  ]
}
[/block]


4. Export and save the template on your machine. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e8125e5-Whatsapp_Infobip_export_template.png",
        "Export WhatsApp Template",
        "Screen shows how to expand, select and export a WhatsApp Template and save it on your local machine"
      ],
      "align": "center",
      "border": true,
      "caption": "Export WhatsApp Template"
    }
  ]
}
[/block]


> 📘 Exporting a Template
> 
> The Infobip dashboard does not display all the details for the selected template. We recommend exporting the template and keeping the details handy. You can copy and paste the values from the exported template to the CleverTap dashboard to ensure you are not missing any field. For more information, refer to [Adding a WhatsApp Template in CleverTap](doc:infobip#adding-message-template).

# Add Message Template

> 📘 Naming WhatsApp Templates
> 
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
> 
> For example, if you have multiple provider configurations, such as _Phone_1, phone_2_, you can use the same template name once within _Phone_1 and Phone_2_.

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the message templates:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ >_Provider Nickname_ from the CleverTap dashboard. 
2. Select the _Templates_ option, and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/66956a6-non_CT_approved_templates.jpg",
        "Pre-Approved Message Templates",
        "The screen shows multiple pre-approved message templates for WhatsApp"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Pre-Approved Message Template "
    }
  ]
}
[/block]


3. Enter the template name in the _Namespace_ field.
4. Choose the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, and _Location_.
5. You can choose to use the Limited Time Offer template for your message. For more information, refer to [Limited Time Offer Template](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
6. Enter the message content.
7. Select _Footer_ to add a footer text and a button (Quick Reply or a Call To Action).
8. Select the _Language_ in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2939b98-Generic_template_create.jpg",
        "",
        "Define Template content for Infobip"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Template Content"
    }
  ]
}
[/block]


7. Click **Save Template**.

# Test a Message Template

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
        "Test WhatsApp Message",
        "Screen shows how to preview and test a WhatsApp message from the CleverTap dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Test WhatsApp Message"
    }
  ]
}
[/block]


The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Infobip team to debug the issue, as shown in the following figure:

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

To create a WhatsApp campaign using Infobip as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

# Creating a Journey

To create a WhatsApp journey using Infobip as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp) for detailed instructions.