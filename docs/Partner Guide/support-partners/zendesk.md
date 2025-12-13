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

* You must have a Zendesk Admin account and an API token to send requests from CleverTap to Zendesk for creating tickets.
* You must have an account with CleverTap.

# Integrate CleverTap with Zendesk

This integration involves the following two major steps:

1. [Set Up a Webhook](doc:zendesk#set-up-webhook).
2. [Create a CleverTap Campaign to create support tickets](doc:zendesk#create-a-webhook-campaign).

## Set up Webhook

Set up a webhook to send HTTP API requests with all the information. To set up a webhook: 

1. Navigate to *Settings* > *Engage* > *Channels* > *Webhooks* from the CleverTap dashboard. 
2. Click **+ Add Webhook**.

<Image title="Set up a Webhook from CleverTap dashboard" alt={2858} align="center" border={true} src="https://files.readme.io/1967920-Add_Webhook.png">
  Set Up a Webhook from the CleverTap Dashboard
</Image>

3. Configure the webhook template by adding the following details: 

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
        Name
      </td>

      <td>
        Enter the nickname for your webhook to uniquely identify the webhook.
      </td>
    </tr>

    <tr>
      <td>
        Destination URL
      </td>

      <td>
        Enter the following URL:\
        https\://\{\{your\_sub\_domain}}.zendesk.com/api/v2/tickets.json
      </td>
    </tr>

    <tr>
      <td>
        Method
      </td>

      <td>
        Select the *POST* method from the dropdown.
      </td>
    </tr>

    <tr>
      <td>
        Basic Authorization
      </td>

      <td>
        Enable this option.
      </td>
    </tr>

    <tr>
      <td>
        Username
      </td>

      <td>
        Enter the username as follows:\
        *\{emailaddress}/token* 
      </td>
    </tr>

    <tr>
      <td>
        Password
      </td>

      <td>
        Enter the password as \<API Token>\. To obtain the API token, refer to [Generating a new API token](https://support.zendesk.com/hc/en-us/articles/4408889192858).
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Enter all the required details and create a Webhook template" alt={1006} align="center" width="80%" border={true} src="https://files.readme.io/fb5dbd8-Create_webhook_template.png">
  Create a Webhook Template
</Image>

## Create a Webhook Campaign

To create a webhook campaign:

1. **Define the audience**.\
   The **Rating Submitted** event is raised when a user submits their feedback through [NPS Campaign](https://docs.clevertap.com/docs/user-ratings). The campaign targets users who give ratings of less than **3**. 

<Image title="Define Target Audience for Webhook campaign" alt={3182} align="center" border={true} src="https://files.readme.io/31c11b3-Define_the_audience.png">
  Define Target Audience for Webhook Campaign
</Image>

2. **Define the campaign content.**\
   a. Click **Go To Editor** to create your message.\
   b. Select *Custom JSON Body* and use the following example to help structure your payload and enter the desired fields:

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

<Image title="Define custom body for Webhook campaign" alt={3178} align="center" width="80%" border={true} src="https://files.readme.io/90c30d4-Define_campaign_content.png">
  Custom Body for Webhook Campaign
</Image>

Ticket details are extensible and customized based on the [Zendesk ticket API](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#create-ticket). To learn more about creating a webhook, refer to [Create a Webhook Campaign](doc:create-message-webhook).

# Common Identifier

If you have a common identifier between CleverTap and Zendesk, we recommend using this identifier as the `requester_id`. This helps unify the two sets of users. Alternatively, if this is not the case, we recommend passing a group of identifying attributes such as name, email address, phone number, or others.
