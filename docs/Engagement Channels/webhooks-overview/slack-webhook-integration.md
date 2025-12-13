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

1. Navigate to *Apps* from your Slack workspace and search for incoming webhooks in the search bar.
2. Click **Add** under the *Incoming WebHooks* app.

<Image title="Add Webhook Add-on to Slack Workspace" alt={1892} align="center" border={true} src="https://files.readme.io/3c1f654-webhooks.png">
  Add Incoming WebHooks
</Image>

The *Slack App Directory* page opens.

3. Click **Add to Slack**.

<Image title="Click Add to Slack to Add Webhook Add-on to Slack Workspace" alt={1330} align="center" border={true} src="https://files.readme.io/c2670d5-add_to_slack.png">
  Integrate WebHooks with Slack
</Image>

> 📘 Admin Permissions
>
> If your Slack workspace is managed by admins, you will need to raise a request for adding incoming webhooks to your Slack workspace.

4. On the same screen, after you click *Add to Slack*, select a channel where you want to post the Slack alerts from the dropdown or create a new one, and click *Add Incoming WebHooks integration*. 

<Image title="Channel Configuration for Posting Webhooks" alt={1680} align="center" border={true} src="https://files.readme.io/c30f410-post_to_channel.png">
  Channel Configuration
</Image>

## Save the Webhook URL

After selecting the channel to post your alerts, Slack generates a webhook URL for that specific channel.

<Image title="View Endpoint" alt={2114} align="center" border={true} src="https://files.readme.io/fad99b0-webhook_url.png">
  View Endpoint
</Image>

Copy and save that webhook URL in a file, as you will need it while configuring the webhook campaign on CleverTap.

## Configure and Create a Webhook on CleverTap

To configure a webhook campaign on CleverTap:

1. Navigate to *Settings* > *Channels* > *Webhooks* on the CleverTap dashboard.
2. Click **+Add Webhook**
3. Enter the webhook name.
4. Select the appropriate HTTPS method (POST in this case) and paste the saved URL (from the [previous step](doc:slack-webhook-integration#save-the-webhook-endpoint) in the *Destination URL*.

> 📘 Webhook Setup
>
> Refer to [Webhooks Setup](doc:setup-webhooks) to learn more about the setup process in detail.

5. Click **Create**.
6. Define the structure of the message payload you wish to post on Slack while setting up the *What* section in the [webhook editor](https://docs.clevertap.com/docs/create-message-webhook#webhook-editor). 

Consider a sample custom body payload as shown in the following image:

<Image title="Sample Custom Payload" alt={2518} align="center" border={true} src="https://files.readme.io/c85a308-payload.png">
  Custom Payload
</Image>

> 📘 Note
>
> In the Custom Body payload, ensure that your message Key is in lowercase. For example: "text" not "Text".

7. After defining the payload structure, test the alert:\
   a. Click *Preview & Test*\
   b. Select a sample test profile.\
   c. Click **Apply** and click **Send Test**.

<Image title="Test Webhook Alert" alt={1564} align="center" src="https://files.readme.io/152ffa4-test.png">
  Preview and Test
</Image>

The Slack alert for the above-defined payload appears as follows on the selected Slack channel.

<Image title="Sample Webhook Alert on Slack" alt={1946} align="center" border={true} src="https://files.readme.io/da35813-dummy.png">
  Test Webhook Alert
</Image>

To learn more about the overall campaign creation process for Webhooks, refer to [create webhook message](https://docs.clevertap.com/docs/create-message-webhook) document.
