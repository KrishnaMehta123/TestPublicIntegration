---
title: Formsuite
excerpt: Customer Relationship Management
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

[Formsuite](https://formsuite.co/) is a no-code platform that helps businesses create and embed custom forms for lead capture, user onboarding, and survey collection. With built-in integrations, conditional fields, and dynamic styling, Formsuite simplifies data collection across digital touchpoints.

With the CleverTap and Formsuite integration, you can:

- Collect real-time user data from forms embedded in CleverTap campaigns
- Update CleverTap user profiles using Zapier workflows
- Trigger journeys based on new responses
- Personalize future campaigns with enriched profile data

This integration captures Formsuite submissions and automatically maps them to CleverTap user properties, enabling hyper-personalized engagement based on user responses.

# Prerequisites for Integration

Ensure the following before starting the integration:

- An active Formsuite account with access to form sharing.
- A valid CleverTap account with **Account ID **and **Passcode**.
- An active Zapier account to create workflows

# Integrate Formsuite with CleverTap

To integrate Formsuite with CleverTap, perform the following three major steps:

1. [Create and Embed a Formsuite Form](doc:formsuite#create-and-embed-formsuite-form)
2. [Create In-App Campaign in CleverTap](doc:formsuite#create-in-app-campaign-in-clevertap)
3. [Create Zap to Send Form Data to CleverTap](doc:formsuite#create-zap-to-send-form-data-to-clevertap)

## Create and Embed Formsuite Form

Consider a scenario where a FinTech app wants to promote a new investment product by embedding a Formsuite form in an In-App campaign to capture name, email, and interest level. They can send these responses to CleverTap via Zapier. The users can then be segmented as follows: high-interest users receive a webinar invite, medium get product details, and low enter a nurture journey.

Now, build your form in Formsuite and prepare it for embedding in CleverTap. To do so, perform the following steps:

1. In your Formsuite dashboard, create a form with the following fields:

   - Full Name (Text)
   - Email Address (Email)
   - Investment Interest (Dropdown: High, Medium, Low)

   [block:image]{"images":[{"image":["https://files.readme.io/54f77da334a8a038e17beee8b29cb4af7e1183c16d70f0c5844373cf6f36cf53-image.png",null,"Create Form on Formshite dashboard"],"align":"center","sizing":"75% ","border":true,"caption":"Create Form on Formshite dashboard"}]}[/block]
2. Click **Publish**, then go to the _Share_ tab and click **\</> Copy Code** to copy the form code.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ad97abba7803317dd74470b9aba2c023b4f09b4c272ed33e2014acf78391083-image.png",
        null,
        "Create and Embed a FormSuite Form"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create and Embed FormSuite Form"
    }
  ]
}
[/block]


## Create In-App Campaign in CleverTap

Set up an In-App campaign in CleverTap to display your Formsuite form to users. To do so, perform the following steps:

1. Go to _Campaigns_ on the CleverTap dashboard, click **+ Campaign** and select _In-App Messages_ from the list of messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03be0be6a6a95eb8264710b0d853073f041640b3e0c528e4c5fb145a6527b4d2-image.png",
        null,
        "Create In-App Campaign"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create In-App Campaign"
    }
  ]
}
[/block]


2. Configure the following campaign settings: qualification criteria, target segment, and delivery preferences.
3. In the _What_ section, select _Custom HTML Template_ and select the _Interstitial_ layout.
4. Paste the embed code in the HTML editor copied from _Step 2_ of  [Create and Embed a Formsuite Form](doc:formsuite#create-and-embed-formsuite-form) 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7529a95aca39b791b8cd098ee146b03ecd2a058e59f41448375d6dd46a14bc98-image.png",
        null,
        "Set up an In-App campaign"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set up an In-App campaign"
    }
  ]
}
[/block]


5. Click **Preview & Test** to verify that the form renders correctly.

## Create Zap to Send Form Data to CleverTap

Use Zapier to automate sending form responses from FormSuite to CleverTap user profiles.

1. Go to your [Zapier Dashboard](https://zapier.com/app/home) and click **+ Create Zap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5e73078a5614dec0bf4b039ccd6697ed6bb08851bf116e61d93a76b76675b34-image.png",
        null,
        "Create a Zap on Zapier Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Zap on Zapier Dashboard"
    }
  ]
}
[/block]


2. Set Formsuite as the trigger app as follows:
   1. Select the Trigger Event as _New Response_.
   2. Connect your Formsuite account by adding your Formsuite credentials.
   3. Select the form and test the trigger.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bdbe9389c9e4330727c316f4efa75600698cf073a9756aee8e5504abb0c9f49c-image.png",
        null,
        "Set Trigger"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Set Trigger"
    }
  ]
}
[/block]


3. Set CleverTap as the action app as follows: 

   1. Select the Action Event as _Create/Update User Profile_.

   [block:image]{"images":[{"image":["https://files.readme.io/45a2915806d73600438255cc13563b8f14be09b01885bcf5932b18dc0a2b9643-image.png",null,"Set CleverTap as the Action"],"align":"center","sizing":"50% ","border":true,"caption":"Set CleverTap as the Action"}]}[/block]

   2. Connect CleverTap using the CleverTap Account ID and Passcode. To find CleverTap project details, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/66d1ffebef9897504dfaccbb54b86a03bc761e28b00d50dbf5d982611a868acf-image.png",
        null,
        "Connect CleverTap Account"
      ],
      "align": "center",
      "sizing": "55% ",
      "border": true,
      "caption": "Connect CleverTap"
    }
  ]
}
[/block]


4. Configure the Action by mapping the Formsuite data fields to CleverTap fields. For example:

| CleverTap Field    | Formsuite Field                                                                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Identity           | Formsuite user ID / Email ID or any unique identity field corresponding to the user                                                             |
| Object ID          | Unique identifier for the user                                                                                                                  |
| Creation Date      | Date of the user’s creation in your system                                                                                                      |
| Profile Properties | JSON object of user properties (e.g., `{ "name": "John Doe", "email": "john@example.com", "role": "Investor", "investment_interest": "High" }`) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f956929addf37d229d7285f6faad05c8ae3136c00bdf62eaa347495000231a93-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true
    }
  ]
}
[/block]


5. Click **Test & Review** to validate data mapping. 

You can verify if the correct user profile was updated with the correct data from the _Find People_ > _Profile Preview_ page on the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6e4005803e53e9e41c3898104a3107b5cfb9e4310a8c17273c4589ed8d58e95-image.png",
        null,
        "Verify Data in CleverTap"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Verify Data in CleverTap"
    }
  ]
}
[/block]


Once verified, your integration is live and ready to capture and sync Formsuite responses in real time.