---
title: Contentful
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

[Contentful](https://www.contentful.com/) is a powerful headless Content Management System (CMS) that enables marketers to manage and deliver content across websites, mobile apps, and more. Unlike traditional CMSs, Contentful separates content from presentation, enabling flexible and reusable content modeling.

The CleverTap and Contentful integration empowers teams to:

- Pull structured content directly from Contentful using Linked Content APIs.
- Personalize content dynamically using Liquid tags in CleverTap campaigns.
- Deliver tailored messages across channels such as Email, Push Notification, and In-App.

# Prerequisites for Integration

The following are required to complete the integration:

- A Contentful account with access to the Content Delivery API.
- Your Contentful **Space ID**, **Environment ID**, and **API token**.
- A CleverTap account with Linked Content enabled.

# Integrate Contentful with CleverTap

The integration process involves the following three major steps:

1. [Find Contentful API Credentials](doc:contentful#find-contentful-api-credentials)
2. [Configure Linked Content in CleverTap](doc:contentful#configure-linked-content-in-clevertap)
3. [Create Personalized Campaign Using Linked Content](doc:contentful#create-personalized-campaign-using-linked-content)

## Find Contentful API Credentials

Access your Contentful API credentials to connect your content with CleverTap securely. To do so, perform the following steps:

1. Go to _Settings_ > _API keys_ in your [Contentful dashboard](https://app.contentful.com/).
2. If you don’t already have a key, click **+ Add API key**.
3. Enter a name, select the appropriate environment (for example, `master`), and click **Save**.
4. Copy your **Space ID** and **Content Delivery API Access Token**.
5. Make note of your **Environment ID** (usually `master`, unless customized).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7b3940d43bdf6babd7aa8d8c5dadb3c15607f3c36c5bcfc9923f3b5cb519b135-image.png",
        null,
        "Find Contentful API Credentials"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Find Contentful API Credentials"
    }
  ]
}
[/block]


These credentials will be required to [ Configure Linked Content in CleverTap](doc:contentful#configure-linked-content-in-clevertap).

## Configure Linked Content in CleverTap

To display the personalized images in CleverTap campaigns, you must configure Linked Content. To do so, follow these steps:

1. Go to _Settings > Setup > Linked Content_ in CleverTap.
2. Click **+ Add Linked Content**.
3. Fill in the following:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Value",
    "0-0": "Name",
    "0-1": "Provide a name for the Linked Content. For example, Contentful API.",
    "1-0": "Method",
    "1-1": "Set the HTTP method to `GET`",
    "2-0": "Endpoint URL",
    "2-1": "Enter the following endpoint URL: `https://cdn.contentful.com/spaces/{space_id}/environments/{env_id}/entries`  \nReplace `{space_id}` and `{env_id}` with your actual Contentful credentials.",
    "3-0": "Headers",
    "3-1": "` Bearer <API_TOKEN>`"
  },
  "cols": 2,
  "rows": 4,
  "align": [
    null,
    null
  ]
}
[/block]


4. Click **Test Linked Content**.
5. Click **Auto-Fill Objects with Response ** to automatically handle responses and populate objects.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb112d5cd763a21e64fff0dc2a4eea6b6607d985f327338f52435b4d8c144469-Screen_Recording_2025-04-15_at_1.57.08_PM_1.gif",
        "",
        "Configure Linked Content in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure Linked Content in CleverTap"
    }
  ]
}
[/block]


6. Click **Test & save changes** to complete the setup.

You can now use this Contentful-generated linked content in various CleverTap campaigns.

## Create Personalized Campaign Using Linked Content

With Contentful connected to CleverTap via Linked Content, you can now add personalized content to your CleverTap campaigns. For this example, let us create a short, personalized Push Notification for promotional advertisement. To do so, perform the following steps:

1. Go to _Campaigns_  from the CleverTap dashboard and click **+ Campaign**.

2. Select _Push Notifications_ from the _Messaging Channels_ list.

3. Configure all the campaign settings and then go to the _What_ section:
   1. Click **Personalization**. 
   2. Select the _Linked Content_ configured under [Configure Linked Content in CleverTap](doc:contentful#configure-linked-content-in-clevertap) and click **Apply**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46b0a83646f6f4fc30d01d1966ea7b55510813fadeb22c2d9c82f9ea854f5609-image.png",
        null,
        "Personalization"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Personalize Push Notification Using Linked Content"
    }
  ]
}
[/block]


4. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid Tags](doc:personalize-message-all).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c8a23a4dd00ddf5acf75c0436f72401a6ca4ee2dfe4f621f1a27039e2ea122d2-789c4e27-201e-472d-ba5e-6925c7854506.png",
        null,
        "Linked content"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Personalized Message Using Linked Content"
    }
  ]
}
[/block]


For this example, we will use the `items` object from the above-linked content options and use the `id` and  `text` keys from the JSON response to retrieve the personalized message generated by Contentful.

The following is the sample response generated by Contentful Linked Content:

```json JSON
{
  "total": 1,
  "items": [
    {
      "sys": {
        "id": "2DhLXpWYk9n5emtCA7GqfE",
        "type": "Entry",
        "createdAt": "2025-04-14T04:47:00.629Z",
        "updatedAt": "2025-04-14T04:47:00.629Z",
        "space": {
          "sys": {
            "type": "Link",
            "linkType": "Space",
            "id": "alu97stg42ry"
          }
        },
        "environment": {
          "sys": {
            "id": "master",
            "type": "Link",
            "linkType": "Environment"
          }
        }
      }
    }
  ]
}
```

Use the following Liquid Tag to fetch the personalized text:

```text Liquid Tag Syntax
{{ Linked[" Testing ContentFul"].items[0].fields.pageTitle | default: "NULL" }}
{{ Linked[" Testing ContentFul"].items[0].fields.pageDescription | default: "NULL" }}
```

5. Click **Preview & Test** to see if the campaign correctly renders personalized content or default fallback values.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9c0aa2a3dae654eec27ad5d4466d06f52bb5a537f9fed1acb85e0601715cd7c-3e2277e3-8b08-48b3-b8ec-5e8d86c2c4c2.png",
        null,
        "Preview & Test"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


6. From the Media subsection, use the following syntax to insert the Contentful image URL from the auto-mapped asset:

```liquid
{{ Linked[" Testing ContentFul"].Asset[0].fields.file.url | default:"fallback_image" }}
```

7. Click **Publish** to launch the campaign. Verify if everything works as intended, users will receive a push notification like the one below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b6c852bb12809cbe58d074c9641ae81234b904632e3114c530d756b55d704d8-a7c45794-ff21-40ac-b4a0-f020fdb73ffe.png",
        null,
        "Push Notifications"
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "Push Notification Using Contentful API"
    }
  ]
}
[/block]


By integrating Contentful with CleverTap, you can automate the creation of hyper-personalized content across different CleverTap campaigns. 

Whether you are creating [Push Notifications](doc:create-message-push), [Email](doc:create-message-email), [In-App messages](doc:create-message-in-app), or [Web Pop-ups](doc:create-message-web-popup), Contentful empowers you to deliver highly relevant, personalized messaging at scale.