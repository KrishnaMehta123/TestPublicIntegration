---
title: Delighted
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

[Delighted](https://delighted.com) is a customer feedback platform that helps you gather real-time, actionable feedback through email, web, or SMS surveys.

By integrating CleverTap with Delighted, you can:

- Automatically trigger Delighted surveys when specific events are captured in CleverTap.
- Pass user profile information to Delighted to personalize survey delivery.
- Add users to Delighted Autopilot based on their interactions within your app or website.

This integration allows you to send a survey to the user with pre-filled location and wallet balance data, giving you targeted, context-rich feedback. For example, a retail app wants to trigger a Delighted survey immediately after a successful purchase. Here,

- Event trigger: For example, Charged
- Survey type: NPS or CSAT
- Expected output: personalized survey sent, feedback returned to the dashboard

# Prerequisites for Integration

Before setting up the integration, ensure you have the following:

- Delighted Private API Key (available in your Delighted account settings).
- Access to your CleverTap dashboard with permissions to configure webhooks and campaigns.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Delighted. The CleverTap and Delighted integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Delighted](https://help.delighted.com/) for support and resolution.

# Integrate Delighted with CleverTap

To integrate Delighted with CleverTap, perform the following two major steps:

1. [Set Up Webhook in CleverTap](doc:delighted#set-up-webhook-in-clevertap)
2. [Create Webhook Campaign in CleverTap](doc:delighted#create-webhook-campaign-in-clevertap)

These steps enable you to automate survey triggers based on user behavior and enrich your feedback data using user profile properties stored in CleverTap.

## Set Up Webhook in CleverTap

> ⚠️ Enable Webhooks
> 
> If Webhooks are not enabled for your account, contact [CleverTap Support](mailto:support@clevertap.com).

1. Go to _Settings_ > _Channels_ > _Webhooks_ from the CleverTap dashboard.
2. Click **+ Add Webhook** and provide a meaningful name for the webhook.
3. Set the _HTTP Method_ to `POST` and enter the following _Endpoint URL_. For more information, refer to [Delighted API](https://delighted.com/docs/api).

```json
https://api.delighted.com/v1/people.json
```

4. Add the following key-value pair under _Headers_:

```json
Content-Type: application/json
```

5. Select _Basic Authentication_ for Authentication and enter the following:
   - Username: Your Delighted _Private API Key_
   - Password: Use a hyphen (`-`)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4dc71b36a758f944e28515775c5c0ae8f188fedc2716f0d4c10eee6b17cdd17-image.png",
        null,
        "Create Webhook"
      ],
      "align": "center",
      "sizing": "30% ",
      "border": true,
      "caption": "Create Webhook"
    }
  ]
}
[/block]


6. Click **Save** to configure the Webhook in CleverTap.

## Create Webhook Campaign in CleverTap

> 🚧 Prepare Delighted Survey in Advance
> 
> Ensure your Delighted survey is created and ready to receive user data via API.

1. Go to _Campaigns_ on the CleverTap dashboard, click **+ Campaign** and select _Webhook_ from the list of messaging channels.
2. Configure the following campaign settings: target audience, schedule, and other basic settings.
3. Perform the following steps under the _What_ section:

   1. Select the webhook created in the previous step.
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
  "email": "{{ Profile.Email | default: 'test@clevertap.com' }}",
  "properties": {
    "Purchase Experience": "Mobile App",
    "State": "{{ Profile.State | default: '-' }}",
    "City": "{{ Profile.City | default: '-' }}",
    "Wallet": "{{ Profile.wallet_balance | default: '0' }}"
  }
}
```

5. Click the variable selector (`@`, `{`, or `{{`) in the editor to personalize the campaign. You can dynamically reference user profile properties using [Liquid Tags](doc:personalize-message-all#liquid-tags).
6. Click **Preview and Test** to validate the webhook request.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a2efa50203f47d96add3b3979caf34edc281fc0c7ea9b69b72a43f734a709f1-image.png",
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


7. Click **Publish** to the campaign to your targeted users. Once a user qualifies for the campaign conditions:
   - Your Delighted Dashboard will reflect the data with the user properties corresponding to the users we sent as a request payload.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ff2926681da4c84bd584fd7829829132379bd735efaf239461cab237223e92b-image.png",
        null,
        "Delighted Dashboard"
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Delighted Dashboard"
    }
  ]
}
[/block]


- Delighted uses this information to trigger a personalized survey via email.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b48153596e81151eec8a8667ef66dd906a9bc6a3f813fa9fc8f2cebeeeb94b3b-image.png",
        null,
        "Survey via Email"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Survey via Email"
    }
  ]
}
[/block]


- Survey responses and associated user properties are visible on your Delighted dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/df18c8d6d3fc4c05dc251ce79c3968de1269dcbba8dc3f659cf2e26cb6df7d73-image.png",
        null,
        "Survey responses"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Survey responses"
    }
  ]
}
[/block]


Integrating Delighted with CleverTap empowers your team to collect timely, contextual feedback at critical milestones in the user journey. By automatically triggering personalized surveys based on In-App behavior, you can close the loop between customer actions and sentiment.