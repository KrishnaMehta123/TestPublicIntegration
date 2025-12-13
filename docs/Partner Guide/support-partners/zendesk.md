---
title: Zendesk
excerpt: Support Partner
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

[Zendesk Support Suite](https://www.zendesk.com/support-suite/) (ZSS) allows businesses to have natural conversations with their customers through omnichannel support using email, webchat, voice, or social messaging applications. Zendesk offers a streamlined ticketing system that tracks and prioritizes interactions, allowing businesses to have a unified historical view of their customers.

This integration helps you to create a support ticket using a CleverTap webhook. For example, you send out a CleverTap [Rating In-app](https://docs.clevertap.com/docs/create-message-inapp#ratings-template) campaign, and the customer provides negative feedback. CleverTap can create a support ticket on Zendesk for this feedback automatically, which allows your support team to follow up with the customer.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- You must have a Zendesk Admin account and an API token to send requests from CleverTap to Zendesk for creating tickets.
- You must have an account with CleverTap.

# Integrate CleverTap with Zendesk

This integration involves the following two major steps:

1. [Set Up a Webhook](doc:zendesk#set-up-webhook).
2. [Create a CleverTap Campaign to create support tickets](doc:zendesk#create-a-webhook-campaign).

## Set up Webhook

Set up a webhook to send HTTP API requests with all the information. To set up a webhook: 

1. Navigate to _Settings_ > _Engage_ > _Channels_ > _Webhooks_ from the CleverTap dashboard. 
2. Click **+ Add Webhook**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1967920-Add_Webhook.png",
        "Set up a Webhook from CleverTap dashboard",
        2858
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up a Webhook from the CleverTap Dashboard"
    }
  ]
}
[/block]


3. Configure the webhook template by adding the following details: 

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Name",
    "0-1": "Enter the nickname for your webhook to uniquely identify the webhook.",
    "1-0": "Destination URL",
    "1-1": "Enter the following URL:  \nhttps\\://{{your_sub_domain}}.zendesk.com/api/v2/tickets.json",
    "2-0": "Method",
    "2-1": "Select the _POST_ method from the dropdown.",
    "3-0": "Basic Authorization",
    "3-1": "Enable this option.",
    "4-0": "Username",
    "4-1": "Enter the username as follows:  \n_{emailaddress}/token_ ",
    "5-0": "Password",
    "5-1": "Enter the password as \\<API Token>\\. To obtain the API token, refer to [Generating a new API token](https://support.zendesk.com/hc/en-us/articles/4408889192858)."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fb5dbd8-Create_webhook_template.png",
        "Enter all the required details and create a Webhook template",
        1006
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create a Webhook Template"
    }
  ]
}
[/block]


## Create a Webhook Campaign

To create a webhook campaign:

1. **Define the audience**.  
   The **Rating Submitted** event is raised when a user submits their feedback through [NPS Campaign](https://docs.clevertap.com/docs/user-ratings). The campaign targets users who give ratings of less than **3**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/31c11b3-Define_the_audience.png",
        "Define Target Audience for Webhook campaign",
        3182
      ],
      "align": "center",
      "border": true,
      "caption": "Define Target Audience for Webhook Campaign"
    }
  ]
}
[/block]


2. **Define the campaign content.**  
   a. Click **Go To Editor** to create your message.  
   b. Select _Custom JSON Body_ and use the following example to help structure your payload and enter the desired fields:

```json
{
 "ticket":{
   		"requester_id": "@Profile - Identity | default:"1"",
   		"requester": {
    			 "name": "@Profile - Full Name | default: "CleverTap"",
    			 "email": "@Profile - Email | default: "integrations@clevertap.com"",
    			 "phone": "@Profile - Phone | default: "+919999999999""},
   			"type": "task",
   			"subject": "Rating Submitted - @Rating Submitted - User Rating | default:"3"",
   			"comment": {
     				"body": "@Rating Submitted - Comment | default:"Rating submitted""
   			},
   			"priority": "urgent",
   			"status": "new"
 		}
}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90c30d4-Define_campaign_content.png",
        "Define custom body for Webhook campaign",
        3178
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Custom Body for Webhook Campaign"
    }
  ]
}
[/block]


Ticket details are extensible and customized based on the [Zendesk ticket API](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#create-ticket). To learn more about creating a webhook, refer to [Create a Webhook Campaign](doc:create-message-webhook).

# Common Identifier

If you have a common identifier between CleverTap and Zendesk, we recommend using this identifier as the `requester_id`. This helps unify the two sets of users. Alternatively, if this is not the case, we recommend passing a group of identifying attributes such as name, email address, phone number, or others.