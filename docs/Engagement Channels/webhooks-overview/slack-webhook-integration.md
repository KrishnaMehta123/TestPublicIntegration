---
title: Slack - Alerts
excerpt: Understand how to send slack alerts for your CleverTap webhook campaign.
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

You can set up Slack alerts for your CleverTap [Webhook](doc:webhooks-overview) campaign every time a user performs a specific event. For example, you may need to post a Slack alert whenever a user makes a high-value purchase. 

To set up these Slack alerts for your webhook campaign, you need to perform three major steps:

1. [Enable incoming webhooks in your workspace](doc:slack-webhook-integration#enable-incoming-webhooks-in-your-workspace)
2. [Save the Webhook Endpoint URL](doc:slack-webhook-integration#save-the-webhook-endpoint)
3. [Configure and Setup a Webhook campaign on CleverTap to send Slack alerts](doc:slack-webhook-integration#configure-and-create-a-webhook-on-clevertap)

## Enable Incoming Webhooks In Your Workspace

To enable the incoming webhook alerts in Slack:

1. Navigate to _Apps_ from your Slack workspace and search for incoming webhooks in the search bar.
2. Click **Add** under the _Incoming WebHooks_ app.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c1f654-webhooks.png",
        "Add Webhook Add-on to Slack Workspace",
        1892
      ],
      "align": "center",
      "border": true,
      "caption": "Add Incoming WebHooks"
    }
  ]
}
[/block]

The _Slack App Directory_ page opens.

3. Click **Add to Slack**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2670d5-add_to_slack.png",
        "Click Add to Slack to Add Webhook Add-on to Slack Workspace",
        1330
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate WebHooks with Slack"
    }
  ]
}
[/block]

> 📘 Admin Permissions
> 
> If your Slack workspace is managed by admins, you will need to raise a request for adding incoming webhooks to your Slack workspace.

4. On the same screen, after you click _Add to Slack_, select a channel where you want to post the Slack alerts from the dropdown or create a new one, and click _Add Incoming WebHooks integration_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c30f410-post_to_channel.png",
        "Channel Configuration for Posting Webhooks",
        1680
      ],
      "align": "center",
      "border": true,
      "caption": "Channel Configuration"
    }
  ]
}
[/block]

## Save the Webhook URL

After selecting the channel to post your alerts, Slack generates a webhook URL for that specific channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fad99b0-webhook_url.png",
        "View Endpoint",
        2114
      ],
      "align": "center",
      "border": true,
      "caption": "View Endpoint"
    }
  ]
}
[/block]

Copy and save that webhook URL in a file, as you will need it while configuring the webhook campaign on CleverTap.

## Configure and Create a Webhook on CleverTap

To configure a webhook campaign on CleverTap:

1. Navigate to _Settings_ > _Channels_ > _Webhooks_ on the CleverTap dashboard.
2. Click **+Add Webhook**
3. Enter the webhook name.
4. Select the appropriate HTTPS method (POST in this case) and paste the saved URL (from the [previous step](doc:slack-webhook-integration#save-the-webhook-endpoint) in the _Destination URL_.

> 📘 Webhook Setup
> 
> Refer to [Webhooks Setup](doc:setup-webhooks) to learn more about the setup process in detail.

5. Click **Create**.
6. Define the structure of the message payload you wish to post on Slack while setting up the _What_ section in the [webhook editor](https://docs.clevertap.com/docs/create-message-webhook#webhook-editor). 

Consider a sample custom body payload as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c85a308-payload.png",
        "Sample Custom Payload",
        2518
      ],
      "align": "center",
      "border": true,
      "caption": "Custom Payload"
    }
  ]
}
[/block]

> 📘 Note
> 
> In the Custom Body payload, ensure that your message Key is in lowercase. For example: "text" not "Text".

7. After defining the payload structure, test the alert:  
   a. Click _Preview & Test_  
   b. Select a sample test profile.  
   c. Click **Apply** and click **Send Test**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/152ffa4-test.png",
        "Test Webhook Alert",
        1564
      ],
      "align": "center",
      "caption": "Preview and Test"
    }
  ]
}
[/block]

The Slack alert for the above-defined payload appears as follows on the selected Slack channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da35813-dummy.png",
        "Sample Webhook Alert on Slack",
        1946
      ],
      "align": "center",
      "border": true,
      "caption": "Test Webhook Alert"
    }
  ]
}
[/block]

To learn more about the overall campaign creation process for Webhooks, refer to [create webhook message](https://docs.clevertap.com/docs/create-message-webhook) document.