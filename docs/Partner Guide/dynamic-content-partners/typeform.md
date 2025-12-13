---
title: Typeform
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

[Typeform](https://www.typeform.com/) is a powerful platform that helps you create interactive, conversational surveys that users actually want to complete. Whether you are collecting feedback, measuring NPS, or qualifying leads. Typeform makes it easy to capture high-quality responses.

With CleverTap’s Typeform integration, you can now embed surveys directly into your Email, In-App, and Web Pop-up campaigns.

This integration empowers you to:

- Gather real-time feedback at key moments in the user journey
- Automatically update user profiles based on survey responses
- Trigger personalized campaigns based on how users respond

# Prerequisites for Integration

The following are the prerequisites for integrating Typeform with CleverTap:

- Ensure you have access to your Typeform account.
- Ensure you have a CleverTap account.

# Integrate Typeform with CleverTap

Use Typeform surveys to collect actionable feedback from your users within CleverTap campaigns. This integration allows you to configure Email, In-App Message, and Web Pop-up campaigns with embedded Typeform surveys to drive engagement and capture insights.

To do so, perform the following two major steps:

1. [Set Up Typeform Survey](doc:typeform#set-up-typeform-survey).
2. [Configure Typeform in CleverTap Campaigns](doc:typeform#configure-typeform-in-clevertap-campaigns).

> 📘 Important
> 
> Always publish your survey on Typeform before attempting to embed it in a campaign.

## Set Up Typeform Survey

Configure and publish your Typeform survey before embedding it into any campaign. This ensures that the survey is accessible and ready to be rendered across different channels.

Follow these steps to prepare your survey:

1. Log in to your [Typeform](https://www.typeform.com/) account.
2. Create a new survey or open an existing one.
3. Click the **Share** tab.
4. Select one of the following:
   - **Embed in an Email**: Click **Start Embedding** to generate an HTML snippet.
   - **Standard URL**: Copy the survey URL (for In-App or Web Pop-up).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e9745bf2bace885248f018a0111efd834cc8a0492f32461953f2a5a3696be2d-2025-04-14_12-02-27_1.gif",
        null,
        "Create a new survey"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a new survey"
    }
  ]
}
[/block]


> 📘 Note
> 
> Append query parameters to pass user identifiers for better targeting.

## Configure Typeform in CleverTap Campaigns

Configure Typeform in CleverTap Campaigns to effectively embed the survey across different campaign types to collect user responses. You can configure the following campaign types to include your Typeform survey:

- [Email Campaign](doc:typeform#configure-an-email-campaign): Embed the survey in emails to reach users directly in their inbox.
- [In-App Message Campaign](doc:typeform#configure-in-app-campaign): Display the survey within your app at key moments.
- [Web Pop-up Campaign](<>): Surface the survey as a pop-up on your website.

### Configure an Email Campaign

Set up and personalize your email campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   - Select a **Basic Template, Pre-used Template, or a Saved Template**.
   - Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the copied **Typeform HTML snippet** (from step 4 of [Set Up Typeform Survey](doc:typeform#set-up-typeform-survey)) inside the `<body>` section in CleverTap Email editor Source.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1819eb876f94ad67d63576966fa6b2343927a1bae63bc0cd4882e1b988291807-email-_typeform_1.gif",
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


4. Preview and test your email campaign to ensure the survey is embedded correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/20ffe2b7e15f6a305d7c77fd7936acf8605fec3c77a01a1078e9440ffa541858-image.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


5. Publish the email campaign once testing is complete. The embedded Typeform survey will be delivered as part of the personalized email to your users.

## Configure In-App Campaign

Before creating an In-App campaign, ensure your app is configured with the [CleverTap SDK](https://developer.clevertap.com/docs/clevertap-sdks) and has [Push Notifications](https://docs.clevertap.com/docs/setup-push-notification) enabled. This ensures seamless delivery and functionality of In-App messages.

Set up and personalize your In-App campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to **Campaigns** in the CleverTap dashboard. Click on **+ Campaign** and select **In-App Messages** from the dropdown menu.
2. Click **Go to Editor** under the _What_ section.
3. Select any template from the available options. For this example, we will use **Custom HTML Templates**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png",
        null,
        "Custom HTML Templates"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Custom HTML Templates"
    }
  ]
}
[/block]


4. Paste the **Typform HTML snippet** (from step 4 of [Set Up Typeform Survey](doc:typeform#set-up-typeform-survey)) inside the `<body>` tag of the custom HTML.
5. Replace YOUR_SURVEY_URL with your Typeform survey URL, available in the Share section of your Typeform account. Adjust the width and height values as needed for optimal display.
   ```html
   <iframe src="YOUR_SURVEY_URL" width="100%" height="500px">
   ```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/69fd3819804a8b6d099cc8913af0d5fb8688c86a18132bdf19cc650e4cf332c6-2025-04-14_13-19-24_1.gif",
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


6. Click **Send Test** to preview and verify the In-App message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a89acfabf5d8c5a68a7bb4eea179e92073f8aa130a0dcb04840ac9b7c30b7bf-image.png",
        null,
        "Send Test"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Send Test"
    }
  ]
}
[/block]


7. Click **Save** and **Publish** to launch your In-App campaign.

Once published, users will receive personalized In-App messages with the embedded Typeform survey.

In a similar way, you can configure a Web Pop-up campaign to embed a Typeform survey. To learn how to create a Web Pop-up campaign in CleverTap, refer to [Create a Message in Web Pop-up](doc:create-message-web-popup).