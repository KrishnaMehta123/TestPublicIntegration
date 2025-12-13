---
title: Kaleyra
excerpt: Understand how to integrate Kaleyra with CleverTap for WhatsApp communication.
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
> This integration is completed by Kaleyra, and they are dedicated to maintaining and enhancing it. The CleverTap and Kaleyra integration has undergone stringent testing to ensure seamless functionality. For any support or query resolution, contact Kaleyra.

# Introduction

CleverTap users can leverage the following WhatsApp capabilities of Kaleyra to communicate with their customers to:

- Send just-in-time offers to customers to drive purchases
- Gather feedback on the services 
- Keep customers informed and more

# Prerequisites For Integration

Following are the prerequisites:

- WhatsApp add-on enabled on the CleverTap account in addition to the essentials price plan.
- WhatsApp onboarding for the phone number to be used with CleverTap is completed.
- Kaleyra WhatsApp Business API. 

# Integrate Kaleyra with CleverTap

This process involves the following three steps:

1. [Find Kaleyra Details](doc:kaleyra#find-kaleyra-details).
2. [Configure CleverTap Dashboard](doc:kaleyra#configure-clevertap-dashboard).
3. [Set Up CleverTap Callbacks in Kaleyra](doc:kaleyra#set-up-clevertap-callbacks-in-kaleyra).

## Find Kaleyra Details

We recommend keeping the _API key_ and _HTTP Endpoint_ handy before starting with the configuration on the CleverTap dashboard.  To do so:

1. Get the CleverTap endpoint URL from the Kaleyra support team.
2. To get the _API keys_:  
   i. Log into your Kaleyra account.  
   ii. From the left menu bar, click **Developers**. The _API Keys_ page appears.  
   iii. Hover over the API key to view the _API Key_ and the _SID_.  
   iv. Click the ellipses icon **(...)** at the right end of the API Key list and click **Edit**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f56045-Kaleyra_API_Key_View.png",
        null,
        "Kaleyra API View"
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra API View"
    }
  ]
}
[/block]


You can view the following details:

- ** API Name**
- **Whitelisted IP Addresses**: The whitelisted IP addresses for the API Key.
- **API Domain**: The base URL to send the API requests.
- **SID (Security Identifier)**: Unique SID of your kaleyra account. This value is the same for all your API Keys.
- **API Key**: API key details. 

3. Click the copy icon next to the _API Key_ to copy the API to the clipboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d0eb9bd-copy_API_key.png",
        "Copy Kaleyra API",
        1144
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra API Keys"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Go to _Settings_ > _Channels_ > _WhatsApp_  > _WhatsApp Connect_ from the CleverTap dashboard.
2. Click **+ Provider** and _Log in to Facebook_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/735ebce-Whatsapp_Common_Provider_Setup.png",
        null,
        "Kaleyra Provider Setup"
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra Provider Setup"
    }
  ]
}
[/block]


3. Enter the following details:

| <p>Field</p>                    | <p>Description</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Provider</p>                 | <p>Select <em>Generic (Other)</em> from the dropdown list.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p>Nickname</p>                 | <p>Enter the nickname as <em>Kaleyra</em> to identify the provider easily.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p>WhatsApp Business Number</p> | <p>Enter your approved WhatsApp number with your country code. </p><p>To view the approved WhatsApp number, navigate to  <em>Channels</em> > <em>WhatsApp Manage</em> > <em>Configurations</em> > filter by Approved Status from Kaleyra's Dashboard. </p><p>From the Number column, copy the mobile number with the country code.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <p>Request Type</p>             | <p>Ensure that the <em>Request Type</em> is <em>POST</em>.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p>HTTP End Point</p>           | <p>Enter the CleverTap endpoint URL provided by the Kaleyra support team.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <p>Headers</p>                  | <p>Select <em>Headers</em> under the <em>Body</em> section and add the following key-value pairs: </p><ul><li><p>In the <em>Key</em> field, enter API key, and in the <em>Value</em> field, enter the API Key value from your Kaleyra application. To get the API Key details, refer to <a href="https://developers.kaleyra.io/docs/view-api-key-and-sid">View API Key and SID.</a></p></li><li><p>In the <em>Key</em> field, enter sid; in the <em>Value</em> field, enter the SID value retrieved from your Kaleyra application. To get the sid details, refer to <a href="https://developers.kaleyra.io/docs/view-api-key-and-sid">View API Key and SID</a>.</p></li><li><p>In the <em>Key</em> field, enter kaleyra-host, and in the <em>Value</em> field, enter <a href="https://api.kaleyra.io/">https\://api.kaleyra.io/</a> as API domain URL from your Kaleyra application.</p></li><li><p>In the <em>Key</em> field, enter inbound-message-callback-url, and in the <em>Value</em> field, copy and paste the inbound message callback URL.</p></li><li><p>In the <em>Key</em> field, enter delivery-report-callback-url, and in the <em>Value</em> field, copy and paste the delivery report callback URL.</p></li></ul> |

4. To make this service provider as the default provider to send a WhatsApp message, select the _Mark this as default_ checkbox. 
5. To automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard, select the _Set auto-reply for users not tracked on CleverTap_ checkbox.
6. (Optional) You can set the _Maximum Concurrent API requests_ anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save**. 

## Set Up CleverTap Callbacks in Kaleyra

> 📘 Naming WhatsApp Templates
> 
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
> 
> For example, if you have multiple provider configurations, such as _Phone_1, phone_2_, you can use the same template name once within _Phone_1 and Phone_2_.

CleverTap callbacks are already configured in send message API request headers. You must enable a custom callback URL provided by the Kaleyra support team.

To set up the custom callback URL:

1. Log into your Kaleyra.io account.
2. Click **user profile** in the top right bar, 
3. Click **Settings**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e9ea95-callback1.png",
        "Navigate to Kaleyra ",
        1366
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Kaleyra Settings"
    }
  ]
}
[/block]


4. Navigate to the _Settings_ tab

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1cb895-callback_2.png",
        "Navigate to Settings",
        1366
      ],
      "align": "center",
      "border": true,
      "caption": "Settings Tab"
    }
  ]
}
[/block]


5. In the _Enable WhatsApp Callback URLs_ field, enter the HTTP Endpoint shared by the Kaleyra Support team to configure the WhatsApp Callback.
6. Click **Save**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7dde791-callback_3.png",
        "Enter the HTTP Endpoint shared by the Kaleyra Support team",
        1366
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Enable WhatsApp Callbacks"
    }
  ]
}
[/block]


To enable incoming messages callback URL in Kaleyra:

1. Sign in to your Kaleyra.io account.
2. On Kaleyra's dashboard page, click **Channels** from the left menu bar.  
   The Channels page appears.
3. From the _WhatsApp_ section, click **Manage**. The WhatsApp Dashboard page appears. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9f1832-incoming_message_URL_1.png",
        "Navigate to Kaleyra Dashboard",
        1366
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra Dashboard"
    }
  ]
}
[/block]


4. Click **Configurations**. The _Configurations_ page appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9799147-incoming_message_URL_2.png",
        "Navigate to Kaleyra Configurations",
        1366
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra Configuration"
    }
  ]
}
[/block]


5. Locate the number you have configured in CleverTap > Click the ellipsis > click _Edit_. The _Edit Number_ pop-up appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a0bf30c-incoming_message_URL_3.png",
        "Kaleyra Configuration",
        1137
      ],
      "align": "center",
      "border": true,
      "caption": "Kaleyra Configuration"
    }
  ]
}
[/block]


6. Enter the incoming message URL provided by the Kaleyra Support team in the _Incoming URL_ field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e3468db-incoming_message_URL_5.png",
        "Setup Incoming Callback URL",
        437
      ],
      "align": "center",
      "border": true,
      "caption": "Setup Incoming Callback URL"
    }
  ]
}
[/block]


7. Add the following two query parameters:

- ? followed by _inbound_message_callback_url=_ and paste the _Inbound Message Callback URL_ from the CleverTap's Provider page.
- & followed by _payload_version=_ and then enter the Payload Version in the Body section of the CleverTap's Provider page.

# Find Template Details

You need to add the details of your pre-approved templates on the CleverTap dashboard. To find the details of your pre-approved templates on Kaleyra, navigate to the _Template_ section from the Kaleyra dashboard. You can replicate these pre-approved templates in CleverTap to start sending campaigns. Refer to the section below to understand how to add templates in CleverTap.

# Add Message Template

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved on the CleverTap dashboard. 

To add the message templates:

1. Go to _Settings_ > _Channels_ > _WhatsApp_ > _WhatsApp Connect_ from the CleverTap dashboard. 
2. Enter the _Provider Nickname_ in the _Search_ field. 
3. Select the _Templates_ tab, and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e0cf22-non_CT_approved_templates.jpg",
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
5. You can choose to use the Limited Time Offer template for your message. For more information, refer to [Limited Time Offer Template](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates).
6. Enter the message content.
7. Select _Footer_ to add a footer text and a button (Quick Reply or a Call To Action).
8. Select the _Language_ in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05f7706-whatsapp_template_addition.png",
        "Define Template Content",
        2036
      ],
      "align": "center",
      "border": true,
      "caption": "Define Template Content"
    }
  ]
}
[/block]


7. Click **Save Template**.

# Test Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template.
2. Click **Send Test WhatsApp**.
3. Select the test profiles or manually enter the mobile number to whom you want to send the message and click **Send Test**.  

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


The success or failure response appears on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Kaleyra team to debug the issue, as shown in the following figure:

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

To create a WhatsApp campaign using Kaleyra as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp).

# Creating a Journey

To create a WhatsApp journey using Kaleyra as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).