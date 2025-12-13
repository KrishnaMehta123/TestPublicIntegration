---
title: Apxor
excerpt: Workflow Automation
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

[Apxor](https://www.apxor.com/) is an app intelligence platform that enables mobile apps to deliver hyper-contextual In-App experiences such as walkthroughs, tooltips, coachmarks, spotlights, In-App messages, and surveys. By integrating Apxor with CleverTap, product and marketing teams can sync user segments from CleverTap to Apxor and trigger targeted, personalized In-App interactions for onboarding, feature adoption, activation, and announcements, driving measurable product-led growth.

With this integration, for example, a product manager can identify users who have not tried a new feature in CleverTap, sync that segment to Apxor, and automatically launch a contextual walkthrough inside the app to encourage adoption.

# Prerequisites for Integration

Ensure you have the following before setting up the integration:

- Access to the [Apxor Dashboard](https://apxor.com/).
- [Apxor Android SDK](https://guides.apxor.com/getting-started-with-apxor/sdk/android-x) is integrated into your app.
- Access to your CleverTap account.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Apxor. The CleverTap and Apxor integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Apxor](mailto:contact@apxor.com) for support and resolution.

# Integrate CleverTap with Apxor

To integrate Apxor with CleverTap, perform the following three major steps:

1. [Set Up Apxor for Integration](doc:apxor#set-up-apxor-for-integration).
2. [Set Up Webhook in CleverTap](doc:apxor#set-up-webhook-in-clevertap).
3. [Create Webhook Campaign in CleverTap](doc:apxor#create-webhook-campaign-in-clevertap).

## Set Up Apxor for Integration

Ensure Apxor is fully set up to receive cohort data by completing its initial setup. Proper configuration at this stage helps guarantee a smooth, error-free sync when you connect the two platforms. To do so, follow these steps:

1. Log in to your [Apxor Dashboard](https://apxor.com/).
2. Verify that the Android SDK integration is complete and active. If not, refer to [Apxor Android SDK](https://guides.apxor.com/getting-started-with-apxor/sdk/android-x).
3. Locate your App ID, which will be required during the CleverTap setup.
4. (Optional) Review [Apxor API Guides](https://guides.apxor.com/getting-started-with-apxor/api-guides) for advanced customization.

## Set Up Webhook in CleverTap

To send data to your Apxor account, set up a webhook in CleverTap:

1. Go to _Settings_ > _Channels_ > _Webhooks_ from the CleverTap dashboard.
2. Click **Add Webhook** and provide a meaningful name for the webhook.
3. In the _Create webhook template_ popup, enter the following details:

   [block:image]{"images":[{"image":["https://files.readme.io/199136f60ef9126ef7335a1b29dbf260229ae1feb4defdf30beb972e0f3fad39-image.png",null,"Create Webhook"],"align":"center","sizing":"60% ","border":true,"caption":"Create Webhook"}]}[/block]

   [block:parameters]{"data":{"h-0":"Field","h-1":"Description","0-0":"Name","0-1":"Enter the name for your webhook.","1-0":"HTTP Method","1-1":"Set the HTTP Method to _POST_.","2-0":"Destination URL","2-1":"Enter the following destination URL: `<https://server.apxor.com/v1/track/external/clever-tap/sync/<app-id>>`  \n  \nReplace <app-id> with your  Apxor App ID. For more information about your App ID, refer to  [Apxor Application Identifier](https://guides.apxor.com/getting-started-with-apxor/adding-a-new-app#step-5-copy-the-application-identifier)."},"cols":2,"rows":3,"align":["left","left"]}[/block]
4. Enable **Basic Authorization** and enter the username and password provided by Apxor.
5. Click **Save**.

The webhook can now sync CleverTap segments with Apxor cohorts.

## Create Webhook Campaign in CleverTap

Once the webhook is ready, configure a campaign to send user data to Apxor.

1. Go to _Campaigns_ on the CleverTap dashboard, click **+ Campaign** and select _Webhook_ from the list of messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7385f799646e6e0bd1514d5f53cd2661f27b6c09e575a326990c9377a5f24e92-image.png",
        null,
        "Create Webhook Campaign"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Create Webhook Campaign"
    }
  ]
}
[/block]


2. Configure the following campaign settings: qualification criteria, target segment, and delivery preferences.
3. Under the _What_ section, select the webhook created in [Set Up Webhook in CleverTap](doc:apxor#set-up-webhook-in-clevertap).
4. Click **Go to Editor**, select Custom Profile Attributes under the _Webhook Content_ and enter the following details:
   - Key: `apx_cohort_name`
   - Value: The name of the cohort in Apxor. You can also insert a dynamic variable (for example, `{{Cohort Name}}`) to send personalized cohort data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/59c582a46fd495aa0bce988fe98ade7348351d12f55219a92109fc5a3711b525-image.png",
        null,
        "Webhook Content"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Webhook Content"
    }
  ]
}
[/block]


6. Click **Preview & Test** to validate that the data sync works correctly.
7. Once verified, click **Publish**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe0b1bc4f485eb6760fa965b93acec9c1fe00d55f360aeefe65ea099cc9a4caa-image.png",
        null,
        "Publish"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Publish"
    }
  ]
}
[/block]


A dynamic cohort appears in your Apxor dashboard, ready to be targeted for In-App experiences. Completing this integration establishes a seamless connection between CleverTap’s segmentation power and Apxor’s personalization capabilities. This helps deliver the right experience to the right user at the right time.