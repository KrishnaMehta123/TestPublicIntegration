---
title: Movable Ink
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

[Movable Ink](https://movableink.com/) is a visual experience platform that enables marketers to embed dynamic, real-time content into their CleverTap campaigns. With this integration, you can enhance Email, Push, and In-App messages using intelligent content blocks such as polls, countdown timers, scratch-off effects, and more. Movable Ink helps deliver personalized, data-driven creatives at the moment of engagement, boosting campaign performance and user engagement.

With Movable Ink and CleverTap, you can:

- Automatically personalize content at the time of engagement.
- Drive urgency with real-time countdown timers for flash sales or events.
- Deliver gamified promotions using scratch-off effects.
- Enrich campaigns with dynamic visuals powered by CRM, APIs, inventory, or user profile data.
- Target users contextually based on behavior, location, or inventory levels.

# Channel Compatibility Matrix

| **Feature**       | **Push** | **In-App** | **Email** | **Notes**                                                                                                          |
| ----------------- | -------- | ---------- | --------- | ------------------------------------------------------------------------------------------------------------------ |
| Targeting by Date | ✔\*      | ✔          | ✔         | \*Supported on Push, but not recommended as notifications are cached and do not refresh after delivery.            |
| Day of Week       | ✔\*      | ✔          | ✔         | \*Push notifications are cached; using day-based targeting may result in outdated content.                         |
| Time of Day       | ✔\*      | ✔          | ✔         | \*Avoid using this in Push campaigns when content must reflect the exact delivery time, due to caching behavior.   |
| Deep Linking      | ✔\*      | ✔\*        | ✔         | \*Requires Branch deep linking for accurate redirection in Push and In-App campaigns.                              |
| Countdown Timer   | ✔\*      | ✔          | ✔         | \*In Push, timers are not dynamic after delivery; best used in In-App or Email where content updates in real time. |
| Polling           | ✗        | ✔\*        | ✔         | \*After voting, the user is redirected to a mobile landing page.                                                   |
| Scratch Off       | ✔\*      | ✔\*        | ✔         | \*Users exit the app to view the Scratch Off experience; consider for time-sensitive or incentive-based messages.  |
| Video             | ✔        | ✔          | ✔         | Fully supported across all channels.                                                                               |

# Benefits and Use Cases

Use the integration to build more engaging and dynamic campaigns. Example use cases include:

- **Promote Flash Sales:** Use the countdown timer to notify users about upcoming events such as Black Friday or Holiday sales.
- **Distribute Promo Codes:** Create an interactive scratch-off experience that reveals unique voucher codes.
- **Enrich Push Notifications:** Combine API or CRM data to generate rich creatives with live inventory, location, or weather information.
- **Deliver Contextual Offers:** Serve visuals that reflect the user's preferences or behaviors, improving relevance and engagement.

# Prerequisites for Integration

The following are the prerequisites for Movable Ink and CleverTap integration:

- Ensure you have access to your Movable Ink account.
- Ensure you have a CleverTap account with access to campaign creation.

# Integrate CleverTap with Movable Ink

To set up the CleverTap integration with your Movable Ink account, perform the following steps:

1. [Create a Data Source in Movable Ink](doc:movable-ink#create-a-data-source-in-movable-ink)
2. [Create a Campaign in Movable Ink](doc:movable-ink#create-a-campaign-in-movable-ink)
3. [Configure Movable Ink in CleverTap campaigns](doc:movable-ink#configure-movable-ink-in-clevertap-campaigns)

## Create a Data Source in Movable Ink

Set up a data source in Movable Ink to enable real-time personalization using data from your website, CRM, or other platforms.

Movable Ink supports data sources via:

- CSV upload
- API connection
- Website scraping

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98e5fd243fee97ec0849460a3db8245aa08e85eff64d8dcf0c80a741691b6497-image.png",
        null,
        "Supported Data Sources"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Supported Data Sources"
    }
  ]
}
[/block]


Follow [Movable Ink’s guide](https://support.movableink.com/hc/en-us) to set up your data source.

## Create a Campaign in Movable Ink

Create and customize a visual campaign in Movable Ink to generate dynamic content blocks for use in CleverTap campaigns. To do so, perform the following steps:

1. Go to _Campaigns_ > _Create Campaign_ in the Movable Ink dashboard.
2. Select a channel (for example, Email) and select a _Block_ format.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80e91d2375ae6566a48432559f397ee6410abf6208c7d6d2f741748c8153f6be-Screen_Recording_2025-04-09_at_11.52.11_AM_1.gif",
        "",
        "Create Campaign in the Movable Ink"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Campaign in the Movable Ink"
    }
  ]
}
[/block]


3. Click **Add Content**, then select _App Gallery_ and pick a visual component (for example, Countdown Timer).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c749fdf678fec9dab31eacb7909f89603d51f3b6f12b227fb714bd39ce29da78-Screen_Recording_2025-04-09_at_12.01.41_PM_1.gif",
        "",
        "Add Content"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Add Content"
    }
  ]
}
[/block]


3. Use the visual editor to drag and drop elements such as text and images.
4. Insert personalization placeholders (for example, first name) and save your campaign.

> 📘 Personalization
> 
> Add dynamic fields to text during setup. Later, replace these placeholders with [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags) for real-time personalization.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/185512ac5f047b8b5d790ba640d4d12ee040c7fe833f9db362c1cb556d54dc30-image.png",
        null,
        "Personalization"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Personalization"
    }
  ]
}
[/block]


5. Click **Finish**, then **Copy Creative Tag** (HTML or image URL).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/faa5deb91c1d094cc93b11e4a093a454c2004f5b2412721bddff7c221fafc06a-Screen_Recording_2025-04-09_at_12.16.19_PM_1.gif",
        "",
        "Copy Creative Tag"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Copy Creative Tag"
    }
  ]
}
[/block]


Visit the [Movable Ink support center](https://support.movableink.com/)  for more information on using the Movable Ink Platform.

## Configure Movable Ink in CleverTap campaigns

The personalized content generated in Movable Ink, such as countdown timers, polls, and scratch-off blocks, can be used in any CleverTap campaign that supports HTML or image URLs. While this example focuses on an [email campaign](doc:movable-ink#configure-personalized-email-campaign-in-clevertap), you can embed Movable Ink content in [Push Notifications](doc:create-message-push) and [In-App messages](doc:create-message-in-app) campaigns to create real-time, dynamic user experiences.

### Configure Personalized Email Campaign in CleverTap

Set up and personalize your email campaigns in CleverTap using Movable Ink’s visual blocks. To do so, follow these steps:

1. Go to the _Campaigns_, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Configure the campaign as per your requirements and click **Go to Editor** under the _What_ section.
3. Select a _Basic Template_, _Pre-used Template_, or a _Saved Template_.
4. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
5. Paste the **Movable Ink Creative Tag** you copied in _Step 5_ of [Create a Campaign in Movable Ink](doc:movable-ink#create-a-campaign-in-movable-ink) inside `the <body>` section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad99a7d12cc603109ee8846698e690c7d0453226b6207838f3f33615cbc9984d-Screen_Recording_2025-04-09_at_12.34.31_PM_1.gif",
        "",
        "Insert the HTML Code Snippet"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Insert the HTML Code Snippet"
    }
  ]
}
[/block]


6. Replace the `MERGE_TAG` with the appropriate [CleverTap Liquid Tag](doc:personalize-message-all#liquid-tags) for personalization.  
   Set default values to ensure a fallback is displayed when specific data is not available (for example, `{{Profile.name | default: "There"}}` will display "There" if the name field is empty).
7. Send a test email to verify personalization and ensure the Litmus integration functions correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0143041e7dfb799edda8eda62222a1d89a859531ab8c58d459824b788c6d6671-image.png",
        null,
        "Test Email"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Test Email"
    }
  ]
}
[/block]


8. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured Liquid Tags and settings.

Once published, users will see personalized visual content powered by Movable Ink directly in your CleverTap messaging.