---
title: Telegram Messenger
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

[Telegram](https://telegram.org/) is a fast, secure, and cloud-based instant messaging app that allows brands to engage customers using rich messaging formats.

Integrating Telegram with CleverTap allows you to:

- Send event-triggered messages to users via Telegram bots.
- Personalize messages using user profile data.
- Leverage CleverTap segmentation, journeys, and predictive capabilities for Telegram outreach.

# Prerequisites for Integration

The following are the prerequisites for CleverTap and Telegram integration:

- **Access to the CleverTap Dashboard**: You must have the necessary permissions to configure webhooks and campaigns.
- **Telegram Bot**: You must create a Telegram bot, which provides a unique token for authentication. Learn more [here](https://core.telegram.org/bots/features#botfather).
- **Channel Access Token**: Required to send messages to users who have added your Telegram bot.
- **Telegram Chat IDs**: These are required to message users and must be stored in CleverTap as `telegram_chat_id`.

> ⚠️ Messaging Eligibility Criteria
> 
> You can only send messages to users who:
> 
> - Have added your Telegram bot.
> - Have interacted with your bot (excluding those who blocked it).

Ensure that user consent is collected before sending any messages.

# Integrate Telegram with CleverTap

The integration process involves the following three major steps:

1. [Capture and Store Telegram Chat IDs](doc:telegram-messenger#capture-and-store-telegram-chat-ids)
2. [Set Up Webhook in CleverTap](doc:telegram-messenger#set-up-webhook-in-clevertap)
3. [Create Webhook Campaign in CleverTap](doc:telegram-messenger#create-webhook-campaign)

To send messages via Telegram from CleverTap, configure a Webhook and create a Webhook campaign.

## Capture and Store Telegram Chat IDs

Telegram Chat IDs are required to identify and message users. These IDs are different from usernames and must be obtained once a user interacts with your bot.

Refer to the [Telegram API documentation](https://core.telegram.org/bots/api#available-methods) to obtain user, group, or channel Chat IDs.

Once collected, save the Chat IDs to user profiles in CleverTap as a custom user property named `telegram_chat_id`. You can do this:

- Via [CSV upload](doc:csv-upload)
- Via [CleverTap's APIs](https://developer.clevertap.com/docs/user-profile-object)
- Or via [SFTP](doc:imports-via-sftp)

## Set Up Webhook in CleverTap

Set up a webhook to send messages from CleverTap to Telegram using your bot.

1. Go to _Settings_ > _Channels_ > _Webhooks_ from the CleverTap dashboard.
2. Click **+ Add Webhook** and provide a meaningful name for the webhook.
3. Set the _HTTP_ Method to `POST` and enter the following Endpoint URL.

```json
https://api.telegram.org/bot<YOUR_BOT_TOKEN>/sendMessage
```

> 📘 Note
> 
> Learn how to create a bot token using [BotFather](https://core.telegram.org/bots/features#botfather).

4. Add the following key-value pair under Headers:

| Key          | Value              |
| :----------- | :----------------- |
| Content-Type | `application/json` |

5. Click **Save** to configure the Webhook in CleverTap.

## Create Webhook Campaign

Create a Webhook campaign to deliver Telegram messages triggered by user actions or segments.

1. Go to _Campaigns_ on the CleverTap dashboard, click **+ Campaign** and select _Webhook_ from the list of messaging channels.
2. Configure the following campaign settings: target audience, schedule, and other basic settings.
3. Perform the following steps under the _What_ section:

   1. Select the webhook created in [Set Up Webhook in CleverTap](doc:telegram-messenger#set-up-webhook-in-clevertap).
   2. Set Content Format to `JSON`.
   3. Select _Custom Body_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b0fc07b06e7eb830724731b27111799d57f1fa3fd1ce267189bdaf18888e668-image.png",
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


4. Enter the payload under the _Custom Body_ section using [Liquid Tags](doc:personalize-message-all#liquid-tags):

```json
{
 "chat_id": {{ Profile.telegram_chat_id | default: "NULL" }},
 "text": "<b>Bold</b> and <a href='https://example.com'>inline link</a> and <code>code</code>",
 "parse_mode": "HTML"
}
```

5. Click the variable selector (`@`, `{`, or `{{`) in the editor to personalize the campaign. You can dynamically reference user profile properties using [Liquid Tags](doc:personalize-message-all#liquid-tags).
6. Select `parse_mode` as [HTML](https://core.telegram.org/bots/api#html-style), [Markdown](https://core.telegram.org/bots/api#markdown-style), or [MarkdownV2](https://core.telegram.org/bots/api#markdownv2-style) based on your formatting needs. In this example, we have used `parse_mode` as `HTML`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c74c86849459fb9429c030c4ad300b30b5a22f2ec4f3be6a6074066bb44bf35f-image.png",
        null,
        "Parse mode Formatting"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Parse Mode Formatting"
    }
  ]
}
[/block]


7. Click **Preview and Test** to validate the webhook request.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3550adbb37c5c2980ce77a107ffe061c768582e90f6d57a130bf7cbacf43e1c4-image.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


8. Click **Publish** to the campaign to your targeted users.

> 📘 Group and Channel Messaging
> 
> To message groups or channels, store the channel/group ID as `telegram_chat_id`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c9400a648432c5ce4af29e87fb77524d4d858f8249df0f632db630dd358b21b-image.png",
        null,
        "Test Message"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Test Message"
    }
  ]
}
[/block]


With this integration, you can automate and personalize Telegram communications at scale, making your user engagement more immediate and effective.