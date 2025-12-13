---
title: Send Test Personalization
excerpt: >-
  Learn how to send personalized test Inbox campaigns from the CleverTap
  dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 📘 Private Beta
> 
> This feature is released in Private Beta. To know more about this feature, contact your Customer Success Manager.

# Overview

The Send Test Personalization feature for the Inbox channel allows you to test personalized messages before sending Inbox campaigns to your users. This ensures that the campaign content displays correctly for specific users without creating separate campaigns. For example, using Send Test Personalization for a campaign, you can select a few internal test profiles and ensure it meets expectations without creating a duplicate campaign.

# Using Send Test Personalization

You can send a test Inbox campaign with personalized values using the _Preview & Test_ option from the _What_ section of the campaign page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ef96aa4bb4d5042a6e1aede84f45e8bfe7c18e369ca1b7b5734c1c105d1363dd-2025-01-08_16-41-52_3.gif",
        "",
        "Preview & Test Popup"
      ],
      "align": "center",
      "border": true,
      "caption": "Preview & Test Popup"
    }
  ]
}
[/block]


# Ways to Send Personalized Test Message

CleverTap provides two profile categories to select users to send a personalized test message:

- _Test Profiles_: Select one or multiple profiles that are marked as [test profiles for internal testing](doc:user-profiles#mark-a-user-profile-as-a-test-profile). 
- _All Profiles_: Select the email address, CleverTap ID, or identity of the profiles already present on your dashboard. 

> 📘 Handling Anonymous Profiles
> 
> - Anonymous profiles are excluded from the server response and will not appear in the test profiles dropdown. 
> - If the search returns an anonymous profile, it will also be excluded from the response.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/66a029de33d111e5d814fda2bfeedf44f9f29c3bfb482ae45dc0d8f62163e4c4-2025-01-08_18-59-48.png",
        "",
        "Select User Profiles"
      ],
      "align": "center",
      "border": true,
      "caption": "Select User Profiles"
    }
  ]
}
[/block]


Test notifications are sent via a custom API that fetches Inbox notifications, which are displayed in the user’s custom inbox. As the API only gathers the notifications for the user, the rendering of test messages must be handled within your custom inbox. 

The Time To Live (TTL) for test notifications can be a maximum of one hour. The _ Preview & Test _ option is available for all existing campaigns across all statuses.

Event personalization allows sending dynamic values for event properties in messages. The values come from the triggering event chosen in the WHO section. The Event Personalization section lists the top 20 event property values from the selected event in the last five days. You can select a value from this list to include in your test message. The chosen value is sent to all profiles selected for the test.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5d3c1167468165729d9a6a41e9caa5ac418d7805dba9ce417c32b1af30c7f189-image.png",
        null,
        "Event Personalization"
      ],
      "align": "center",
      "border": true,
      "caption": "Event Personalization"
    }
  ]
}
[/block]


# Send Test Response

You can view the response details as soon as you send the test message. To do so, click **Send Test** from the _Preview & Test_ popup. The Send Test Response window opens, and the response details are categorized into the following categories. 

- Details of the message sent successfully
- General Errors, if any
- Linked Content Response: You can copy the responses by clicking the ![](https://files.readme.io/7534549-Copy_icon.png) icon against the respective response.
- Liquid Tags Error, if any. 
- Click the + sign against each user to view all the details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa7968a9956031fded3ba636585aa3f776631ca95fc01010ffd599f7e55605b7-image.png",
        null,
        "Send Test Response"
      ],
      "align": "center",
      "border": true,
      "caption": "Send Test Response"
    }
  ]
}
[/block]


> 📘 Note
> 
> If errors (such as faulty personalization) occur during response creation, messages are dropped silently without error logging in targeting stats. So, delivery success is determined by saving message info in server successfully. For Send Test, the behavior remains the same:
> 
> - A successful dispatch is shown when the message is successfully saved to the server.
> - Therefore, despite content errors, the Send Test UI will show a successful dispatch.

The Send Test Personalization for Inbox allows message testing with real profiles, improving content accuracy and reducing the need for separate Inbox testing campaigns.