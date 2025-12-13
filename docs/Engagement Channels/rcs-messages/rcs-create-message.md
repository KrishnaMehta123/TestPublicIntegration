---
title: Create Message
excerpt: Learn how to create an RCS Message campaign using the CleverTap dashboard
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

RCS (Rich Communication Services) campaigns in CleverTap allow you to engage users with rich, interactive messaging experiences. This guide walks you through the step-by-step process of creating, configuring, and launching an RCS campaign—from selecting the provider and defining your audience to crafting message content, scheduling delivery, and publishing the campaign.

1. [Create a new campaign](doc:create-message#create-a-new-campaign) from the CleverTap dashboard and select **RCS** as the message provider.  
2. [Configure the campaign setup](doc:create-message#start-campaign-setup):
   - Define qualification criteria (Past behavior, Live behavior, or Custom list).
   - Set an optional goal for conversion tracking.
   - Choose your RCS service provider.
3. [Define your target audience](doc:create-message#define-the-audience):
   - Use behavioral segmentation, user properties, demographics, and geographic filters.
   - Use advanced options like:
     - [Control Group](doc:create-message#control-group)
     - [Targeting Cap](doc:create-message#targeting-cap)
     - [Constant Event Property](doc:create-message#constant-event-property)
4. [Select the message type](doc:create-message#rcs-message-types):
   - [Single Message ](doc:create-message#single-message) 
   - [A/B Testing  ](doc:create-message#ab-testing)
   - [Split Delivery  ](doc:create-message#split-delivery)
   - [By User Property](doc:create-message#by-user-property)
5. [Define Message content](doc:create-message#define-the-message-content) using the [RCS Message Editor](doc:rcs-message-editor) with approved or freeform templates.
6. [Set up the campaign schedule](doc:create-message#define-the-campaign-schedule):
   - [Define delivery preferences](doc:create-message#delivery-preferences)
7. **Preview and publish** your campaign.

## Create a New Campaign

Create a campaign to deliver your RCS message. Follow the steps below to create a new RCS campaign:

1. From the CleverTap dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **SMS**.

   [block:image]{"images":[{"image":["https://files.readme.io/0f8144329dfb657f3a0b8cf56b9ff3ee97f5c098bdff7881ea0fd07d11ba3f8b-rcs_campaigns.png","","Create RCS Message Campaign"],"align":"center","border":true,"caption":"Create RCS Message Campaign"}]}[/block]

The campaign page displays. In the SMS Campaign Builder, go to the **Provider** dropdown, select **RCS Message Provider**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9f5b0e431f3eba799c2c39fade54e34aff64fd031e3524b57bc9ce5e14ed32d-rcs_provider_in_campaigns.png",
        "",
        "RCS Campaign Page"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Campaign Page"
    }
  ]
}
[/block]


Define all the sections and **Publish** the campaign.

## Start Campaign Setup

The _Start here_ section displays the setup information. 

This section has the following parts:

- **Start here**: Check that the required platforms are integrated and ready for campaigns. 
- **Qualification criteria**: Deliver the notification based on _Past behavior_, [Custom list](doc:custom-list-segments), or _Live behavior_ For more information about segmenting users, refer to [Segments](doc:segmentation).
- **RCS Service Provider**: Select the available RCS service provider from the list.
- **Set a goal**:  You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional.

Define the conversion period by selecting the _Conversion Time_. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](https://docs.clevertap.com/docs/events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b582a37-Push_notification_set_goal_track_conversion.png",
        "Goal conversion tracking",
        "Enable the conversion tracking check box to track a specific goal conversion"
      ],
      "align": "center",
      "border": true,
      "caption": "Goal Conversion Tracking"
    }
  ]
}
[/block]


## Define the Audience

You must indicate the target audience for your RCS campaign. You can target your RCS campaign to a new user segment by clicking on the **Target Segment** section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cb455cd-WA_Who.png",
        "Define Target Audience",
        "Segment your target audience based on the user properties and events"
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Your Target Audience"
    }
  ]
}
[/block]


You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

> 🚧 Delay > 24 Hours
> 
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live _Inaction within time_ campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; the golden window within which most users transact on online platforms.

### Deliver Action Based RCS Notifications

You can trigger a RCS message to users when they perform a specific action. This makes notifications more contextual and increases conversion. For example, sending a cab booking link to customers who have just booked a hotel or flight.

### Deliver RCS Notifications based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a RCS notification to all the customers from **Mumbai** who are currently subscribed to _Platinum_ membership. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d56a113-User_properties_whatsapp.png",
        "Filter by User properties in Whatsapp",
        "Target the audience basis their user properties like name, email, geolocation"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]


The following table explains the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Geography Radius",
    "3-1": "User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.",
    "3-2": "Locations = San Francisco, USA; Paris, France",
    "4-0": "Reachability",
    "4-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "4-2": "Unsubscribed email = No",
    "5-0": "App Fields",
    "5-1": "App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "5-2": "OS Version = 10"
  },
  "cols": 3,
  "rows": 6,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


To know more about what segments can be used, see [Segments](doc:segmentation).

### Constant event property

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0a96db9-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Control Group Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Control Group Editor"
    }
  ]
}
[/block]


### Targeting Cap

In certain cases, you may need to send a message to only a subset of the qualifying audience (_Target Reach_) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

## RCS Message Types

You can create the following types of messages in your RCS campaign:

- Single Message
- A/B Test
- Split Delivery
- By User Property

> 📘 Legacy UI
> 
> A/B Test and Split Delivery message types are only available for new campaign UI.

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.  
You can test up to three message variants on a test group. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6139527-WhatsApp_AB_Test.png",
        "WhatsApp A/B Test",
        "The image represents a sample distribution between two variants for A/B testing"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS A/B Tests"
    }
  ]
}
[/block]


> 📘 Winning Variant
> 
> The variant that gets the most views is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants (max: 3 variants) for a campaign, you can also auto-copy the content present in the current variant. Further, let us understand A/B Test delivery for Live user segments.

#### A/B Test Delivery To Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of views and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b5d9aa-Whatsapp_Split_delivery.png",
        "Whatsapp Split delivery",
        "As the image represents, you can define the percentage split for your message variants"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Split Delivery"
    }
  ]
}
[/block]


### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the _+Variant_ button to add multiple variants based on a user property value. In the example below, we have used the _Language_ user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language (English, Hindi, etc.)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7fe4f5c-WhatsApp_user_property.png",
        "WhatsApp user property",
        "You can add multiple variants based on a user property value."
      ],
      "align": "center",
      "border": true,
      "caption": "Targetting Based on User Property"
    }
  ]
}
[/block]


## Define the Message Content

Now, you need to set up the _What_ section where you have to define the content for the RCS campaign  Click _Go To Editor_ to create your message. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e4cc8d9-WhatsApp_What.png",
        "Define the Message Type",
        " Define the Message Type for the campaign creation"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Message Type"
    }
  ]
}
[/block]


## RCS Message Editor

Select from the approved templates for Indian users and free form templates with placeholders for users outside of India.

## RCS Editor

Select from the approved templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a0c074d59e6375e32e0114d0b029e6e66988c606739400d020139da1903c908-rcs_templates.png",
        "",
        "Select a Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Select a Template"
    }
  ]
}
[/block]


Fill in the details and click **Done**. For information about using RCS Message editor, refer to [RCS editor](doc:rcs-message-editor).

## Define the Campaign Schedule

The RCS message campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your RCS campaign, you need to specify the _Start date and time_ and _End date and time_ under the _When_ section. You also have the option to start a campaign immediately by selecting _Now_.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on _Done_, the campaign will be triggered and terminated as per the defined timings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/748dd43-WhatsApp_When.png",
        "Define WhatsApp Schedule",
        "In the When section, you need to define the start and end time for the campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Define The Campaign Schedule"
    }
  ]
}
[/block]


### Delivery preferences

 In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

You can select the _Do Not Disturb_ (DND) hours during which messages from this RCS campaign are prevented from going out, either by discarding them or delaying delivery after DND hours complete, such as 9 PM to 9 AM.  

If you want your campaign to adapt delivery times according to the user’s timezone, check the _Timezone_ checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Additionally, you can check the _Cut-Off_ checkbox to avoid sending messages to users after a set cut-off time. This is important for time-sensitive campaigns, for example, live events. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6cb503-Whatsapp_DP.png",
        "Whatsapp Delivery Preferences",
        "Under the delivery preferences, you can explicitly define the DND and cut-off timings."
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Delivery Preferences"
    }
  ]
}
[/block]


## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Campaign",
        "After setting up the overall campaign, click the Publish Campaign button"
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]