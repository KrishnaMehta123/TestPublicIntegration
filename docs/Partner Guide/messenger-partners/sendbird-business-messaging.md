---
title: Sendbird Business Messaging
excerpt: Messenger Partner
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

[Sendbird Business Messaging](https://sendbird.com/products/business-messaging) empowers Product, Operations, Support, and Engineering teams with software and API to message customers through their apps. This document is a comprehensive guide for integrating Sendbird and CleverTap. This integration helps you to send In-App notifications via CleverTap using Sendbird Business Messaging Builder, a Chrome extension.

# Prerequisites for Integration

Ensure that you have the following:

- Sendbird account 
- CleverTap account

# Integrate CleverTap with Sendbird

To set up the CleverTap integration with your Sendbird account:

1. [Set up Sendbird dashboard](doc:sendbird-business-messaging#set-up-sendbird-dashboard).
2. [Create a template on the Sendbird dashboard](doc:sendbird-business-messaging#create-a-template-on-sendbird-dashboard).
3. [Set up CleverTap dashboard](doc:sendbird-business-messaging#set-up-clevertap-dashboard). 

## Set Up Sendbird Dashboard

1. Log in to your Sendbird account and navigate to _Settings_ > _Integrations_.
2. Select **CleverTap** from the available integrations.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ad5bfe-Sendbird_Clevertap_Integration.png",
        "",
        "CleverTap Integration on Sendbird Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap Integration on Sendbird Dashboard"
    }
  ]
}
[/block]


3. Toggle ON the **Event callback** option to set up and track campaign metrics. This step is optional.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cb65a3a-2024-06-20_14-15-53_1.gif",
        "",
        "Sendbird Event Callback"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Event Callback"
    }
  ]
}
[/block]


4. Enter the following details:
   - **Project ID**: You can obtain the Project ID by navigating to the _Settings_ > _Project_ page of the CleverTap dashboard.
   - **Passcode**: To find the passcode for your project, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
   - **API endpoint**: To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7571569-2024-06-20_14-22-50.png",
        "",
        "Sendbird Project ID, Passcode and API endpoint"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Project ID, Passcode and API endpoint"
    }
  ]
}
[/block]


You can find these details on the CleverTap dashboard by navigating to the _Settings_ > _Project_ page.

5. Select from the following configurations and click **Save**

| Endpoint               | Description                                                                                                                                                                                                  |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Event callback         | Determines whether to send the delivery and read status of a notification to CleverTap. For more information, refer to [CleverTap custom events.](https://developer.clevertap.com/docs/events#custom-events) |
| Project details        | Specify the project ID and passcode under _Settings_ > _Project_ on the CleverTap dashboard.                                                                                                                 |
| CleverTap API endpoint | Specifies the CleverTap API endpoint. Copy and paste the API endpoint under API in the [CleverTap documentation](https://developer.clevertap.com/docs/idc#api) based on your data center region              |

6. Install Sendbird Business Messaging Builder.  
   Install the Sendbird Business Messaging Builder [Chrome extension](https://chromewebstore.google.com/detail/sendbird-business-messagi/apbhgfffamdcdogeijjcnjbmghahoaji). The extension link is present under _Business Messaging_ > _Integrations_ > _CleverTap_ on the Sendbird Dashboard. Copy the App ID and API Token for further configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/65564a2-Chrome_Ext_SB.png",
        "",
        "Sendbird Chrome Extension"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Chrome Extension"
    }
  ]
}
[/block]


7. Access the extension by clicking the _Sendbird Business Messaging Builder_ icon in your Chrome browser and then click **Go to Settings**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ae17b3-API_ID_SB_chrome.png",
        "",
        "Sendbird Settings"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Settings"
    }
  ]
}
[/block]


8. Enter your **App ID** and **API token** to load the created templates into the Sendbird Business Messaging Builder.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ddb270c-Crome_ext_App_ID_token.png",
        "",
        "Sendbird Authentication"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Authentication"
    }
  ]
}
[/block]


## Create a Template on Sendbird Dashboard

Create a Webhook template on the Sendbird Dashboard under **Business Messaging > Template > Create Template +**. Once the template is built on Sendbird, individuals or brands can utilize it to send personalized notifications through multiple channels when launching campaigns from the CleverTap dashboard. For instructions on building a template on Sendbird, refer to this [link.](https://sendbird.com/docs/business-messaging/guide/v2/templates)

## Set Up CleverTap Dashboard

To set up CleverTap Dashboard:

1. Navigate to _Settings_ > _Channels_ > _Webhooks_ on the CleverTap dashboard.
2. Click **+ Add Webhook** to begin adding a new webhook.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a825944-CT_Webhook.png",
        "",
        "Clevertap Add Webhook"
      ],
      "align": "center",
      "border": true,
      "caption": "Clevertap Add Webhook"
    }
  ]
}
[/block]


3. Enter the following details and click **Save**:

[block:parameters]
{
  "data": {
    "h-0": "Parameter",
    "h-1": "Description",
    "0-0": "Name ",
    "0-1": "Enter the webhook name. CleverTap recommends naming the webhook **Sendbird single** or **Sendbird multi **for each endpoint.",
    "1-0": "HTTP method",
    "1-1": "Select the desired action. In this case, you must set it to _POST_.",
    "2-0": "Destination URL",
    "2-1": "Navigate to **Business Messaging > Integrations > CleverTap** on the Sendbird dashboard to select one of the following CleverTap integration endpoints:  \n  \n<li> single: Select this endpoint to send real-time notifications to users as soon as a specific event occurs. Sending a large batch of notifications at once through this endpoint could result in [rate limiting](https://sendbird.com/docs/chat/platform-api/v3/application/understanding-rate-limits/rate-limits#1-rate-limits). The endpoint is in the following format: <https://api-{app_id}.notifications.sendbird.com/clevertap/notifications/single> </li>\n<li> multi: Select this endpoint to send notifications to a large group of users. Notifications are not sent in real-time but can be delivered to a significant number of target users simultaneously without encountering rate limit problems. The endpoint is in the following format:\n[https://api-{app_id}.notifications.sendbird.com/clevertap/notifications/multi](https://api-{app_id}.notifications.sendbird.com/clevertap/notifications/mutli)",
    "3-0": "Key",
    "3-1": "Enter the API token to authenticate. Add a key-value pair with `Api-token` as a key, and copy and paste the CleverTap Integration API token from the Sendbird dashboard under **Business Messaging > Integrations > CleverTap** as a value"
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]


# Create a Campaign on CleverTap Dashboard

To send a notification using the CleverTap dashboard, go to the _Campaigns_ page and select _Sendbird_ from the list of messaging channels. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4b150dd-image.png",
        null,
        "Sendbird Integration Successful"
      ],
      "align": "center",
      "border": true,
      "caption": "Sendbird Integration Successful"
    }
  ]
}
[/block]


> 📘 Download the Chrome Extension
> 
> To integrate SendBird directly into the messaging channels on CleverTap, it's essential to download the Chrome extension. This lets you view integrated fields from SendBird in the campaign editor on CleverTap.
> 
> Go to the _Campaigns_ page from the CleverTap dashboard and click **+ Campaign**. The integration is successful if _Sendbird_ appears in the list of Messaging Channels.

Select the webhook that you created while setting up the CleverTap dashboard under the _Start here_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05c7c62-image_4.png",
        "",
        "Select Webhook"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Webhook"
    }
  ]
}
[/block]


Click **Go To Editor** from the What section to define the campaign message. The Create Webhook Content window opens. To send the notification, select the template you created on the Sendbord dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ff72293-Select_Sendbird_Template_.png",
        "",
        "Select Sendbird Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Sendbird Template"
    }
  ]
}
[/block]


The fields displayed on the Clevertap dashboard correspond to the fields defined in the SendBird dashboard when [creating a template](doc:sendbird-business-messaging#create-a-template-on-sendbird-dashboard).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/909f025-image_3.png",
        "",
        "Send Notification from CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Send Notification from CleverTap"
    }
  ]
}
[/block]


You can publish the campaign after defining all the campaign sections.

# FAQs

### How can I set up the campaign metrics?

You can do so by following the steps listed below: 

1. Map Sendbird user ID to CleverTap user ID.  
   CleverTap creates a user profile for each person who uses your app. User profiles have a set of default fields, such as email, phone number, and language. But you can also add more identifiers to the user's custom attributes. To map a Sendbird user ID to a CleverTap user ID, you must add a Sendbird user ID as a custom identifier.  
   You can refer to the following example code for CleverTap's Android SDK:

   ```javascript
   HashMap<String, Object> profileUpdate = new HashMap<String, Object>();
   profileUpdate.put("SendbirdID", "<Sendbird User ID>");

   cleverTap.pushProfile(profileUpdate);
   ```

   Once set, this shows in the Receiver field of the Editor page while sending the Campaign from the CleverTap dashboard.
2. Toggle on the _Event callback_ option on the Sendbird Dashboard.  
   This helps integrate the delivery receipt and read receipt events of the notification with CleverTap's [custom events](doc:events#custom-events). When an event takes place, the Sendbird server uses CleverTap's [upload events API](https://developer.clevertap.com/docs/upload-events-api) to raise an event on the CleverTap.  
   The following is a sample JSON payload of the callback:  
   <br />
   ```json
   {
     "evtName": "My First Campaign", // The Event name value you’ve set in Editor
                                     // during the notification creation.
     "evtData": {
       "status": "READ",             // The status of a notification. Either SENT
                                     // or READ.
       "target_id": 123123           // The campaign or journey ID.
     }
   }
   ```