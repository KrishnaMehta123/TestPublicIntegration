---
title: Storyly
excerpt: Understand how you can use CleverTap segments as an audience in Storyly
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

[Storyly](https://www.storyly.io/), an user engagement platform, enables brands to embed mobile-native stories in their mobile apps and websites through SDK integration. It creates an additional channel to deliver any marketing content in a full-screen and interactive format and communicate with users. This integrates helps with the following:

- Create Campaigns and Journeys to target the Past Behavior segments on CleverTap with stories or personalize their story experience
- Update your segment Storyly every time your Live Behavior segments on CleverTap are updated by their actions in your app.

For any issues regarding this integration, contact [Storyly Support Team](mailto:support@storyly.io).

# Prerequisites

The following are the prerequisites for this integration:

- Ensure that you complete the [Amazon EventBridge setup](doc:setup-amazon-eventbridge).
- Ensure that you pass Custom Parameter to the Storyly SDK. Also, ensure that the identifier you pass here is the same as that used with CleverTap, as it is used to identify the user. For more information on this, refer to [Passing Custom Parameter Recipe](https://docs.storyly.io/recipes/passing-custom-parameter).

# Connect CleverTap Audience with Storyly

This process involved the following two major steps:

1. [Set Up Amazon EventBridge](doc:storyly#set-up-amazon-eventbridge).
2. [Create an Audience for CleverTap on Storyly Dashboard](doc:storyly#create-an-audience-for-clevertap-on-storyly-dashboard).

## Set Up Amazon EventBridge

To set up Amazon EventBridge:

1. Log in to your CleverTap account and navigate to _Settings_ > _Partners_ page. Select _Amazon EventBridge_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/38cb56585d54b2d24334f5d7e5e12892cb5cd9a0bbec7b79299f7813c886418c-Amplitude_Partner_Page.png",
        "",
        "Navigating to Partners Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Navigating to Partners Page"
    }
  ]
}
[/block]


2. A popup opens on the right side of the screen. Enter the following details and click **Integrate**.

| <p>Field</p>            | <p>Description</p>                                                                                                                                                       |
| :---------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Partner Nickname</p> | <p>Enter the <em>Nickname</em> for your integration.</p>                                                                                                                 |
| <p>AWS Account ID</p>   | <ul><li>This user property is used as an identifier when sending event data to Amazon Eventbridge. </li><li>Enter <strong>374278225139</strong> in this field.</li></ul> |
| <p>Region</p>           | <ul><li>Indicates the AWS account region to which the events need to be sent.</li><li>Select <em>EU (Ireland)</em> from the dropdown.</li></ul>                          |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a9c4294-Integrate_raw_data_partner_-_Amazon_EventBridge.png",
        "Enter Amazon EventBridge Project Details and click Integrate",
        2366
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Amazon EventBridge Project Details to Integrate"
    }
  ]
}
[/block]


## Create an Audience for CleverTap on Storyly Dashboard

After setting up the Amazon EventBridge on CleverTap, you need to create a unique token on the Storyly dashboard to complete the connection. To create a unique token on the Storyly dashboard:

1. Navigate to _Settings_ from the Storyly dashboard and find _Audiences_ under _Data Management_ tab.
2. Click **+ New Audience** on the top right side and select _Create Audience for CleverTap_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/01089f0-Create_audience_for_CleverTap.png",
        "Create an audience for CleverTap",
        960
      ],
      "align": "center",
      "border": true,
      "caption": "Create an Audience for CleverTap"
    }
  ]
}
[/block]


3. Enter the _Audience Name_ to uniquely identify your audience and click **Continue**.  
   Storyly generates a _Key_ and unique _Token_ for your Audience. 
4. Copy the Key and Token values, as you will need them when creating Campaigns and Journeys on the CleverTap Dashboard.

You can now start creating Campaigns and Journeys with Amazon EventBridge on the CleverTap dashboard.

# Create Your First Campaign/Journey to Show Personalized Stories to Users

To create a campaign/journey:

1. Select _Amazon EventBridge_ as the Messaging Channel when creating a campaign/journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78c7437-Select_Amazon_EventBridge.png",
        "Create Amazon EventBridge Campaign or a Journey with Amazon EventBridge Engagement Channel",
        1852
      ],
      "align": "center",
      "border": true,
      "caption": "Create Amazon EventBridge Campaign or a Journey with Amazon EventBridge Engagement Channel"
    }
  ]
}
[/block]


2. Click **Go To Editor** under _What_ section of campaign/journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c90a214-Message_Editor_-_Campaigns.png",
        "Create Amazon EventBridge Message - For Campaigns",
        2850
      ],
      "align": "center",
      "caption": "Create Amazon EventBridge Message - For Campaigns"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/472d7ba-Message_Editor_-_Journeys.png",
        "Create Amazon EventBridge Message - For Journeys",
        1047
      ],
      "align": "center",
      "border": true,
      "caption": "Create Amazon EventBridge Message - For Journeys"
    }
  ]
}
[/block]


3. Select _Custom Profile Attributes_ and click _+ Key-Value Pair_ to add the following mandatory key-value pairs and other key-value pairs as per your requirement:

- `storyly_token`  
  Enter the token you copied from the Storyly Dashboard in _step 4_ of [Create an Audience for CleverTap on Storyly Dashboard](doc:storyly#create-an-audience-for-clevertap-on-storyly-dashboard) section.

- `operation`
  - For insert & update operations: upsert
  - To delete a user from the Audience: delete

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35d7f52-Add_Key-Value_Pairs.png",
        "Adding Key-Value Pairs for Personalized Content",
        2080
      ],
      "align": "center",
      "border": true,
      "caption": "Adding Key-Value Pairs for Personalized Content"
    }
  ]
}
[/block]


4. (Optional) Add user properties in the payload by adding new key-value pairs to personalize your content.
5. Click **Done**. 

For a detailed example of sending personalized stories, refer to this example listed in the [Storyly documentation](https://docs.storyly.io/page/connecting-clevertap-audiences-with-storyly).