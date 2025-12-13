---
title: Yellow.AI
excerpt: >-
  Understand how to integrate Yellow.AI with CleverTap for WhatsApp
  communication.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 🚧 Support For Integration
> 
> This integration is completed by Yellow.AI, and they are dedicated to maintaining and enhancing it. The CleverTap and Yellow.AI integration has undergone stringent testing to ensure seamless functionality. For any support or query resolution, contact Yellow.AI.

# Introduction

CleverTap users can now leverage the following WhatsApp capabilities of Yellow.AI to communicate with their customers:

- Sending just-in-time offers to customers to drive purchases
- Gathering feedback on the services 
- Keeping customers informed and more

# Prerequisites for Integration

The following are the prerequisites:

- You must have a WhatsApp add-on enabled on the CleverTap account in addition to the basic or essentials price plan.
- Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
- You must have Yellow.AI WhatsApp Business API 

# Integrate Yellow.AI with CleverTap

This process involves the following three steps:

1. [Find Yellow.AI Credentials](https://docs.clevertap.com/docs/yellowai#find-yellowai-details).
2. [Configure CleverTap Dashboard](https://docs.clevertap.com/docs/yellowai#configure-clevertap-dashboard)
3. [Set Up CleverTap Callbacks in Yellow.AI](https://docs.clevertap.com/docs/yellowai#set-up-clevertap-callbacks-in-yellowai)

## Find Yellow.AI Details

We recommend that you keep the API key and Endpoint handy before starting with the configuration on the CleverTap dashboard. To find these credentials:

1. Select _Integrations_ from the top navigation of your Yellow.AI dashboard.
2. Search for _CleverTap_ under _All Integrations_ section on the left. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/175c94a-ct-yellow.png",
        "Navigate to Yellow.AI Dashboard",
        "Yellow.AI Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Yellow.AI Dashboard"
    }
  ]
}
[/block]

3. Click **API Key** to copy the key and save it for future use.
4. Click **Endpoint URL** to copy the endpoint and save it for future use.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f863a39-api_and_endpoint.png",
        "Locate Yellow.AI Details",
        2540
      ],
      "align": "center",
      "border": true,
      "caption": "Yellow.AI Credentials"
    }
  ]
}
[/block]

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ from the CleverTap dashboard.
2. Click **+ Provider** and select _Generic (Other)_ from the _Provider_ dropdown. 

<!---->

3. Enter the following details:

| <p>Field</p>                    | <p>Description</p>                                                                                                                                                                                                                                                                             |
| :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Provider</p>                 | <p>Select <em>Generic (Other)</em> from the dropdown list.</p>                                                                                                                                                                                                                                 |
| <p>Nickname</p>                 | <p>Enter the nickname as <em>Yellow.AI</em> to identify the provider easily.</p>                                                                                                                                                                                                               |
| <p>WhatsApp Business Number</p> | <p>Enter your phone number onboarded to WhatsApp API by Yellow.AI.</p>                                                                                                                                                                                                                         |
| <p>Request Type</p>             | <p>Ensure that the <em>Request Type</em> is <em>POST</em>.</p>                                                                                                                                                                                                                                 |
| <p>HTTP End Point</p>           | <ul><li>Enter the following URL as the HTTP End Point: <a href="https://cloud.yellow.ai/integrations/genericIntegration/clevertap">https\://cloud.yellow.ai/integrations/genericIntegration/clevertap</a></li></ul>                                                                            |
| <p>Headers</p>                  | <p>Select <em>Headers</em> under the <em>Body</em> section and enter the following key-value pair: </p><ul><li>Enter Key as <em>Authorization</em> and paste the <em>API key</em>, obtained in <em>Step 2</em> of <a href="">Find Yellow.AI Details</a>, in the <em>Value</em> field</li></ul> |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7c0e8c2-Whatsapp_Common_Provider_Setup.png",
        null,
        "HTTP Endpoint and Headers"
      ],
      "align": "center",
      "border": true,
      "caption": "HTTP Endpoint and Headers"
    }
  ]
}
[/block]

4. Select the _Mark this as default_ checkbox to make this service provider as the default provider to send a WhatsApp message.
5. To automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard, select the _Set auto-reply for users not tracked on CleverTap_ checkbox. 
6. (Optional) You can set the _Maximum Concurrent API requests_ anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save** to save the details. 

## Set Up CleverTap Callbacks in Yellow.AI

To set up the CleverTap callbacks:

1. Copy the _Delivery Report Callback URL_  and _Inbound Message Callback URL_ from the CleverTap dashboard. You can find the Callback URLs under the _Setup_ tab of the _Provider_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb81965-yellow_callback_1.png",
        "Setup Callbacks",
        1078
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Setup Callbacks"
    }
  ]
}
[/block]

2. Paste the Delivery Report and Inbound Message callback URL:  
   a. Log in to your Yellow.AI account.  
   b. Navigate to _Engage_ > _More_ > _Preferences_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9492264-callback_yellow1.png",
        "Yellow.AI Dashboard",
        1176
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Yellow.AI Dashboard"
    }
  ]
}
[/block]

b. Toggle ON the _Postback URL_ and paste the URL obtained in _Step 2_ of [Find Yellow.AI Details](<>).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d45f808-toggle_callback.png",
        "Configure Postback URL",
        1608
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Postback URL"
    }
  ]
}
[/block]

c. Paste the Inbound Message Callback URL on the _Integrations_ page of Yellow.AI as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b41016c-inbound_callback.png",
        "Configure Inbound Callback URL",
        1800
      ],
      "align": "center",
      "border": true,
      "caption": "Setup Inbound Message Callback URL"
    }
  ]
}
[/block]

# Find Template Details

You need to add the details of your pre-approved templates on the CleverTap dashboard. To find the details of your pre-approved templates on Yellow.AI, navigate to the _Template_ section from the Yellow.AI dashboard, as shown below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9240e8c-Yellow._AI_Template.png",
        "Locate Template Details",
        "Find Template Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Find Template Details"
    }
  ]
}
[/block]

# Add Message Template

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved on the CleverTap dashboard. To add the message templates:

1. Navigate to _Settings_ > _Channels_ > _WhatsApp_ from the CleverTap dashboard. 
2. Enter the _Provider Nickname_ in the _Search_ field. 
3. Select the _Templates_ tab, and click **+Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/024a8b8-exotel_templated.png",
        "Create a New Message Template",
        2174
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Template"
    }
  ]
}
[/block]

3. Enter the template name in the _Namespace_ field.
4. Choose the type of template header (Text or Media). For Media headers, you can use _Image_, _Video_, _Document_, and _Location_
5. Enter the message content.
6. Select _Footer_ to add a footer text and a button (Quick Reply or a Call To Action).
7. Select the _Language_ in which you want to display the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05f7706-whatsapp_template_addition.png",
        "Define Message Template Content",
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

# Test a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Hover over the desired template for which you want to send a test notification.
2. Click **Send Test WhatsApp**.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click **Send Test**.  

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

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Yellow.AI team to debug the issue, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/363a140-sendtest_campaign.png",
        "Validate the Test Response",
        728
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Validate the Test Response"
    }
  ]
}
[/block]

# Create Campaign

To create a WhatsApp campaign using Yellow.AI as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp) for detailed instructions.

# Creating a Journey

To create a WhatsApp journey using Yellow.AI as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp) for detailed instructions.