---
title: SurveyMonkey
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

[SurveyMonkey](https://www.surveymonkey.com/) is a leading survey and feedback platform that enables businesses to collect, analyze, and act on customer insights. It supports multi-channel distribution of surveys, including email, web links, and mobile.

By integrating CleverTap with SurveyMonkey, you can:

- Automatically trigger survey delivery based on user actions or lifecycle stages.
- Pass user attributes from CleverTap to personalize survey links or targeting.
- Analyze responses in SurveyMonkey to enhance campaign strategy and product development.

This integration helps you close the feedback loop by capturing customer sentiment in context, improving retention, and decision-making. For example, you can trigger an NPS survey three days after a user's first purchase.

# Prerequisites for Integration

The following are the prerequisites for SurveyMonkey:

- Ensure you have access to your SurveyMonkey account with access to the Personalize module.
- Ensure you have a CleverTap account.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by SurveyMonkey. The CleverTap and SurveyMonkey integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [SurveyMonkey](https://help.surveymonkey.com/en/) for support and resolution.

# Integrate SurveyMonkey with CleverTap

CleverTap can trigger a SurveyMonkey survey via a campaign or webhook. To implement this, follow these two major steps:

1. [Create a Survey in SurveyMonkey](doc:surveymonkey#create-a-survey-in-surveymonkey)
2. [Configure CleverTap Campaign with Survey Link](doc:surveymonkey#configure-clevertap-campaign-with-survey-link)

## Create a Survey in SurveyMonkey

1. Log in to your SurveyMonkey account.
2. Click **Create Survey** and select from a template or build one from scratch.
3. Add the required questions when designing a survey, such as Net Promoter Score (NPS), Customer Satisfaction (CSAT), or multiple-choice questions.
4. Click **Collect Response** and select _Email Collector_ from the _Add New Collector_ dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/13c63077a705733725566bc7f83f4a6aab387fdb51fdca32eae7c26f59a2c233-image.png",
        null,
        "Email Collector"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Email Collector"
    }
  ]
}
[/block]


5. Copy the survey link to use in your CleverTap campaign.

For more information about pre-populating answers for supported parameters, refer to [SurveyMonkey's guide](https://help.surveymonkey.com/en/surveymonkey/send/custom-variables/).

## Configure CleverTap Campaign with Survey Link

The [SurveyMonkey survey](doc:surveymonkey#create-a-survey-in-surveymonkey) can be used in any CleverTap messaging channel that supports HTML or image URLs. While this guide includes an example for an [email campaign](doc:create-message-email), you can also use SurveyMonkey content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-inapp), and other CleverTap messaging channels that support dynamic visuals. 

To integrate a SurveyMonkey survey into your CleverTap Email campaign, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   1. Select a _Basic Template_ or _Saved Template_.
   2. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the HTML Snippet copied in _step 5_ of [ Create a Survey in SurveyMonkey](doc:surveymonkey#create-a-survey-in-surveymonkey) inside the `<body>` tag.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82a52d9f81856a7df6178eae5e9d585735b7aef4410cd90c67a1250f316d9bc3-2025-05-11_21-52-41_1.gif",
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


4. Replace the `MERGE_TAG` with the appropriate [CleverTap Liquid Tag](doc:personalize-message-all#liquid-tags) for personalization. Set default values to ensure a fallback is displayed when specific data is not available (for example, `{{Profile.name | default: "User"}}` will display "User" if the name field is empty). For more information, refer to [SurveyMonkey Merge Tags](https://help.surveymonkey.com/en/getfeedback/builder/merge-fields-logic/).
5. Send a test email to verify personalization and ensure the SurveyMonkey integration functions correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02d8203166c9269b9fa1eeb2819004a173fe7b554d916caa6decaabb05df8524-image.png",
        null,
        "Send a test email"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Send a Test Email"
    }
  ]
}
[/block]


6. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured Liquid Tags and settings.

Combining SurveyMonkey's dynamic content capabilities with CleverTap’s advanced segmentation and messaging allows you to create timely, relevant interactions that resonate with every user. For more information about using personalization in CleverTap, refer to [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags).