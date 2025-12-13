---
title: Blitzllama
excerpt: Dynamic Content
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

[Blitzllama](https://blitzllama.com) helps you gather targeted user feedback through micro-surveys. By integrating with CleverTap, you can push defined user cohorts from CleverTap into Blitzllama, enabling precise targeting and richer user insights.

With this integration, you can:

- Import CleverTap user segments via one-time, scheduled, or recurring campaigns.
- Use these cohorts in Blitzllama to trigger micro-surveys to the right users.

# Prerequisites for Integration

Ensure the following before starting the integration:

- Ensure you have access to your CleverTap account.
- Ensure you have a Blitzllama account.
- Ensure you have Blitzllama API access.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Blitzllama. The CleverTap and Blitzllama integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Blitzllama](mailto:tech@blitzllama.com) for support and resolution.

# Integrate Blitzllama with CleverTap

To integrate Blitzllama with CleverTap, perform the following three major steps:

1. [Find Blitzllama Details](doc:blitzllama#find-blitzllama-details).
2. [Set Up Webhook in CleverTap](doc:blitzllama#set-up-webhook-in-clevertap).
3. [Create Webhook Campaign in CleverTap](doc:blitzllama#create-webhook-campaign-in-clevertap).

## Find Blitzllama Details

Access your Blitzllama destination and API key for integration. To do so, perform the following steps:

1. Go to the _Connections_ tab in the Blitzllama dashboard.
2. Select _CleverTap_ to find the _Destination URL_ and _API key_.
3. Copy the _Destination URL_ and _API key_ and save this information. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a6fa1c5efe950a889257d00a6b6bf0ce6fe1c8601593685d7b6ad14a30ad95e-image.png",
        null,
        "Get Destination URL"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Get Destination URL"
    }
  ]
}
[/block]


## Set Up Webhook in CleverTap

Configure the Webhook channel in CleverTap to communicate with Blitzllama. To do so, perform the following steps:

1. Go to _Settings_ > _Channels_ > _Webhooks_ from the CleverTap dashboard.
2. Click **+ Add Webhook** and provide a meaningful name for the webhook.
3. Set the _HTTP Method_ to `POST` and paste the _Destination URL_ copied in _step 3_ of [Find Blitzllama Details](<>).
4. Add the following key-value pair under _Headers_:

| Key         | Value                                                                      |
| ----------- | -------------------------------------------------------------------------- |
| `X-api-key` | Paste the _API key_ copied from _step 3_ of [Find Blitzllama Details](<>). |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74eed9a262eb62b2879a2e6b672ca391f262ace3f359cff076481c73df85311b-image.png",
        null,
        "Create Webhook"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Create Webhook"
    }
  ]
}
[/block]


5. Click **Save** to create the webhook.

After saving the webhook, CleverTap is now ready to send user profile data directly to Blitzllama.

## Create Webhook Campaign in CleverTap

Create a Webhook campaign in CleverTap to send user data to Blitzllama. To do so, follow these steps to configure and publish the campaign:

1. Go to _Campaigns_ on the CleverTap dashboard, click **+ Campaign** and select _Webhook_ from the list of messaging channels.
2. Configure the following campaign settings: target audience, schedule, and other basic settings.
3. Perform the following steps under the _What_ section:

   1. Select the webhook created in [Set Up Webhook in CleverTap](doc:blitzllama#set-up-webhook-in-clevertap).
   2. Set Content Format to `JSON`.
   3. Select _Profile variables & custom key value pairs_, to define which user fields you want to send to Blitzllama, such as Name, Email, Phone, Created Date, and so on.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b463e177d22f40be669ed15c0658bb2040e648a4376a768683e43276f8f9e707-29396b66-5ecf-44a7-ac2a-f3b7c4ace003.png",
        null,
        "Webhook Content"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Webhook Content"
    }
  ]
}
[/block]


> 🚧 Note
> 
> You cannot preview or test this campaign before publishing. Ignore test errors. Once published, the sync works as expected.

4. Click **Publish**. Syncing may take up to 30 minutes.

Once synced, you can view and manage cohorts under the _User & Cohorts_ > _View details_ in the Blitzllama dashboard.

Clicking **View details** shows the list of users received from CleverTap. You can use these cohorts to target micro-surveys directly within Blitzllama’s survey configuration workflow.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc2bed06a7e0a38bbff2510420878bd6dbcdbc1dc5999999eb4ac9912ab32a92-image.png",
        null,
        "User & Cohorts"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "User & Cohorts"
    }
  ]
}
[/block]