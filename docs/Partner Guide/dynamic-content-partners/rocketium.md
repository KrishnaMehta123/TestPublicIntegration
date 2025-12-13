---
title: Rocketium
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

[Rocketium](https://rocketium.com/) is a creative automation platform that helps marketers and designers scale personalized visual content for websites, apps, and ads. By integrating Rocketium with CleverTap, you can:

- Embed static or personalized dynamic creatives from your Rocketium dashboard into CleverTap campaigns
- Improve conversion rates by delivering relevant creatives

# Prerequisites for Integration

The following are the prerequisites for Rocketium and CleverTap integration:

- Ensure you have access to your Rocketium account.
- Ensure you have a CleverTap account with access to campaign creation.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Rocketium. The CleverTap and Rocketium integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Rocketium](https://rocketium.com/contact-us.html) for support and resolution.

# Integrate CleverTap with Rocketium

Rocketium enables you to create two types of visual creatives that can be embedded into CleverTap campaigns:

- **Static Creatives**  
  Design image-based creatives in Rocketium and use their static URLs directly within your CleverTap campaigns. For detailed integration steps, refer to [Embed Static Rocketium Images into Campaigns](doc:rocketium#embed-static-rocketium-images-into-campaigns).
- **Dynamic (Personalized) Creatives**  
  Pass dynamic parameters via linked content in CleverTap to generate personalized images based on user profile attributes. For detailed integration steps, refer to [Add Personalized Rocketium Creatives Using Dynamic URLs](doc:rocketium#add-personalized-creatives-using-dynamic-urls).

## Embed Static Rocketium Images into Campaigns

Add personalized static Rocketium creatives to your CleverTap campaigns by embedding image URLs directly from your Rocketium project. To do so, follow these steps:

1. [Design a Static Creative in Rocketium](doc:rocketium#design-static-creative-on-rocketium).
2. [Add a Static Image to CleverTap's In-App Campaign](doc:rocketium#add-static-image-to-in-app-campaign).

### Design Static Creative on Rocketium

Design a static image using a Rocketium template and customize it with your campaign visuals and messaging. To do so, perform the following steps:

1. Create a new project in your Rocketium account.
   1. Assign an appropriate project name.
   2. Add or select a template to use in this project.
   3. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e9b17ff7db0b74b69be55ebe54523880c6fd480568eb62fa34bb392ff61b3a7-image.png",
        null,
        "Create New Project"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create New Project"
    }
  ]
}
[/block]


2. Click **Save** again, after customizing your template, to finalize it.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a5a305c726cbd3191a302ab899b5bd4a75365a0a160212ce2b767dfb11546b6-image.png",
        null,
        "Customize template"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Customize template"
    }
  ]
}
[/block]


3. Generate the Share Link

   1. Go to the _Projects_ section.
   2. Hover over the project name and click the More Options icon.
   3. Select Share ![Edit Icon](https://files.readme.io/42484fdfc0d6c79ffa0ef5eddf9e26745c0f46bd50b64665642c26c360ef244d-2025-05-15_09-37-17.png) icon and click **Copy Link** to copy the generated link.
4. [block:image]{"images":[{"image":["https://files.readme.io/e56039dea2cd22838774a6b372a5b281407201743d5af32dd458951ca95fe106-image.png",null,"Copy Link"],"align":"center","sizing":"75% ","border":true}]}[/block]

   To preview your image, paste the link in your browser and copy the URL. You can now use your image inside CleverTap campaigns.

### Add Static Image to In-App Campaign

Set up and personalize your In-App campaigns in CleverTap to engage users effectively. To do so, perform the following steps:

1. Go to _Campaigns_ from the CleverTap dashboard. 
2. Click **+ Campaign** and select _In-App Messages_ from the dropdown.
3. Click **Go to Editor** under the _What_ section.
4. Select the template of your choice. For this example, we are using _Custom HTML Templates_.

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


5. Paste the URL copied in _Step 4_ of [Design Static Creative on Rocketium](doc:rocketium#design-static-creative-on-rocketium).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a8a44c41a18ad53ecc6ef43e2290a4045acc4015b9e09ec49ac72fba8653bef9-image.png",
        null,
        "Paste the URL"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Paste the URL"
    }
  ]
}
[/block]


6. Click **Save** and **Publish** to send your In-App campaign.

Once published, your In-App campaign will be sent to targeted users based on your segmentation and scheduling settings. You can also use the same Rocketium design in an Email campaign. For detailed instructions,  refer to [CleverTap Email Campaigns](doc:create-message-email).

## Add Personalized Creatives Using Dynamic URLs

With Rocketium, you can display different creatives based on user profile properties in campaigns. To build and publish a project, refer to [Rocketium's guide on spreadsheet imports](https://docs.rocketium.com/campaign/scale/spreadsheet-import). These personalized creatives can then be used in CleverTap campaigns. Rocketium generates creative variants based on your imported data when you complete the spreadsheet setup.

> 📘 Note
> 
> Use this approach if you plan to display different creatives based on user profile properties in campaigns.

To add personalized creatives using dynamic URLs, perform the following steps:

1. [Configure the Linked Content API in CleverTap.](doc:rocketium#configure-linked-content-api-in-clevertap)
2. [Create a Personalized Campaign Using Linked Content.](doc:rocketium#create-personalized-campaign-using-linked-content)

### Configure Linked Content API in CleverTap

To display the personalized images in CleverTap campaigns, you must configure Linked Content. To do so, follow these steps:

1. Go to _Settings_ > _Setup_ > _Linked Content_ from the CleverTap dashboard.
2. Click **+ Linked Content**.
3. Enter a suitable name for the API.
4. Paste the Rocketium Image URL, which you copied from _Step 4_ of [ Design Static Creative on Rocketium](doc:rocketium#design-static-creative-on-rocketium), in the **Endpoint URL** field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a179c1e39a615f60b441392068825a51c5c44db43b7ad72aacf9f3d2db7d799-2025-05-09_19-41-03_1.gif",
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


5. Define URL Parameters: Specify the dynamic parameters using `{{ }}`. These parameters must match the column names in your Rocketium spreadsheet.  
   Example Format:

```html
<ROCKETIUM_URL>?Name={{Profile.name}}&City={{Profile.city}})
```

6. Test the Linked Content to ensure it returns the expected output.
7. Autofill the object using the response.
8. Click **Save** to finalize the Linked Content configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/286d3f147b09f8906d49d81beb38f86b207221ccc0ae0c549b7b0a892d1fa755-Screen_Recording_2025-02-27_at_1.51.59_PM_1.gif",
        "",
        "Linked Content configuration"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Linked Content configuration"
    }
  ]
}
[/block]


Once your Linked Content is configured, you can use it in any messaging channel that supports dynamic content.

### Create Personalized Campaign Using Linked Content

With Rocketium connected to CleverTap via Linked Content, you can now add personalized content to your CleverTap campaigns. To do so, perform the following steps:

1. Go to _Campaigns_  from the CleverTap dashboard and click **+ Campaign**.

2. Select _Push Notification_ from the _Messaging Channels_ list.

3. Configure all the campaign settings and then go to the _What_ section:
   1. Click **Personalization**. 
   2. Select the _Linked Content_ configured under [Configure Linked Content API in CleverTap](doc:rocketium#configure-linked-content-api-in-clevertap) and click **Apply**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a3374c8a1e5bc30a31aa7a3a306e8af5223cd4605cae1af3d3fc8d4c420c545f-2025-05-09_19-59-27_1.gif",
        "",
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


4. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid tag](doc:personalize-message-all).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b969f8819a9aa43a6fcb6e912fe57a58c7c94ca6acf43efba256cff229449481-image.png",
        null,
        "Create Personalized Message Using Linked Content"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Personalized Message Using Linked Content"
    }
  ]
}
[/block]


This will fetch the image variant corresponding to the parameters we passed and show it to the user.

5. Click **Preview & Test** to verify if the campaign pushes the default values you configured. 
6. Click **Publish** to launch the campaign. Verify if everything works as intended. Users will receive a push notification such as the one below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d121294c838907feaf053f8e8669cc69fa7d6ffa22b36df0a4d61f5e434a4636-image.png",
        null,
        "Push Notifications"
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Push Notifications"
    }
  ]
}
[/block]


By integrating Rocketium with CleverTap, you can deliver real-time personalized visuals at scale across the following channels: [Push Notifications](doc:create-message-push), [Email](doc:create-message-email), [In-App Messages](doc:create-message-in-app), or [Web Popups](doc:create-message-web-popup#campaign-priority), Rocketium empowers you to deliver highly relevant, personalized messaging at scale.