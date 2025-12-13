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
   * Define qualification criteria (Past behavior, Live behavior, or Custom list).
   * Set an optional goal for conversion tracking.
   * Choose your RCS service provider.
3. [Define your target audience](doc:create-message#define-the-audience):
   * Use behavioral segmentation, user properties, demographics, and geographic filters.
   * Use advanced options like:
     * [Control Group](doc:create-message#control-group)
     * [Targeting Cap](doc:create-message#targeting-cap)
     * [Constant Event Property](doc:create-message#constant-event-property)
4. [Select the message type](doc:create-message#rcs-message-types):
   * [Single Message ](doc:create-message#single-message) 
   * [A/B Testing  ](doc:create-message#ab-testing)
   * [Split Delivery  ](doc:create-message#split-delivery)
   * [By User Property](doc:create-message#by-user-property)
5. [Define Message content](doc:create-message#define-the-message-content) using the [RCS Message Editor](doc:rcs-message-editor) with approved or freeform templates.
6. [Set up the campaign schedule](doc:create-message#define-the-campaign-schedule):
   * [Define delivery preferences](doc:create-message#delivery-preferences)
7. **Preview and publish** your campaign.

## Create a New Campaign

Create a campaign to deliver your RCS message. Follow the steps below to create a new RCS campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **SMS**.

   <Image alt="Create RCS Message Campaign" align="center" border={true} src="https://files.readme.io/0f8144329dfb657f3a0b8cf56b9ff3ee97f5c098bdff7881ea0fd07d11ba3f8b-rcs_campaigns.png">
     Create RCS Message Campaign
   </Image>

The campaign page displays. In the SMS Campaign Builder, go to the **Provider** dropdown, select **RCS Message Provider**.

<Image alt="RCS Campaign Page" align="center" border={true} src="https://files.readme.io/e9f5b0e431f3eba799c2c39fade54e34aff64fd031e3524b57bc9ce5e14ed32d-rcs_provider_in_campaigns.png">
  RCS Campaign Page
</Image>

Define all the sections and **Publish** the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Start here**: Check that the required platforms are integrated and ready for campaigns. 
* **Qualification criteria**: Deliver the notification based on *Past behavior*, [Custom list](doc:custom-list-segments), or *Live behavior* For more information about segmenting users, refer to [Segments](doc:segmentation).
* **RCS Service Provider**: Select the available RCS service provider from the list.
* **Set a goal**:  You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional.

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](https://docs.clevertap.com/docs/events).

<Image title="Goal conversion tracking" alt="Enable the conversion tracking check box to track a specific goal conversion" align="center" border={true} src="https://files.readme.io/b582a37-Push_notification_set_goal_track_conversion.png">
  Goal Conversion Tracking
</Image>

## Define the Audience

You must indicate the target audience for your RCS campaign. You can target your RCS campaign to a new user segment by clicking on the **Target Segment** section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

<Image title="Define Target Audience" alt="Segment your target audience based on the user properties and events" align="center" border={true} src="https://files.readme.io/cb455cd-WA_Who.png">
  Segment Your Target Audience
</Image>

You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

> 🚧 Delay > 24 Hours
>
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; the golden window within which most users transact on online platforms.

### Deliver Action Based RCS Notifications

You can trigger a RCS message to users when they perform a specific action. This makes notifications more contextual and increases conversion. For example, sending a cab booking link to customers who have just booked a hotel or flight.

### Deliver RCS Notifications based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a RCS notification to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 

<Image title="Filter by User properties in Whatsapp" alt="Target the audience basis their user properties like name, email, geolocation" align="center" border={true} src="https://files.readme.io/d56a113-User_properties_whatsapp.png">
  Filter by User Properties
</Image>

The following table explains the various property types:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Type
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Properties
      </td>

      <td>
        Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
      </td>

      <td>
        Customer Type = Platinum
      </td>
    </tr>

    <tr>
      <td>
        Demographics
      </td>

      <td>
        Demographics filters include *Age* and *Gender*.
      </td>

      <td>
        Age = 25 to 40 years\
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States\
        State = California\
        City = San Francisco
      </td>
    </tr>

    <tr>
      <td>
        Geography Radius
      </td>

      <td>
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.
      </td>

      <td>
        Locations = San Francisco, USA; Paris, France
      </td>
    </tr>

    <tr>
      <td>
        Reachability
      </td>

      <td>
        Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.
      </td>

      <td>
        Unsubscribed email = No
      </td>
    </tr>

    <tr>
      <td>
        App Fields
      </td>

      <td>
        App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segmentation).

### Constant event property

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image title="Control Group and Target Cap" alt="Control Group Editor" align="center" border={true} src="https://files.readme.io/0a96db9-Control_Group_and_Target_Cap.png">
  Control Group Editor
</Image>

### Targeting Cap

In certain cases, you may need to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

> 📘 Campaign Limit
>
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

## RCS Message Types

You can create the following types of messages in your RCS campaign:

* Single Message
* A/B Test
* Split Delivery
* By User Property

> 📘 Legacy UI
>
> A/B Test and Split Delivery message types are only available for new campaign UI.

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.\
You can test up to three message variants on a test group. 

<Image title="WhatsApp A/B Test" alt="The image represents a sample distribution between two variants for A/B testing" align="center" border={true} src="https://files.readme.io/6139527-WhatsApp_AB_Test.png">
  RCS A/B Tests
</Image>

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

<Image title="Whatsapp Split delivery" alt="As the image represents, you can define the percentage split for your message variants" align="center" border={true} src="https://files.readme.io/1b5d9aa-Whatsapp_Split_delivery.png">
  RCS Split Delivery
</Image>

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the *+Variant* button to add multiple variants based on a user property value. In the example below, we have used the *Language* user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language (English, Hindi, etc.)

<Image title="WhatsApp user property" alt="You can add multiple variants based on a user property value." align="center" border={true} src="https://files.readme.io/7fe4f5c-WhatsApp_user_property.png">
  Targetting Based on User Property
</Image>

## Define the Message Content

Now, you need to set up the *What* section where you have to define the content for the RCS campaign  Click *Go To Editor* to create your message. 

<Image title="Define the Message Type" alt=" Define the Message Type for the campaign creation" align="center" border={true} src="https://files.readme.io/e4cc8d9-WhatsApp_What.png">
  Define Message Type
</Image>

## RCS Message Editor

Select from the approved templates for Indian users and free form templates with placeholders for users outside of India.

## RCS Editor

Select from the approved templates.

<Image alt="Select a Template" align="center" border={true} src="https://files.readme.io/1a0c074d59e6375e32e0114d0b029e6e66988c606739400d020139da1903c908-rcs_templates.png">
  Select a Template
</Image>

Fill in the details and click **Done**. For information about using RCS Message editor, refer to [RCS editor](doc:rcs-message-editor).

## Define the Campaign Schedule

The RCS message campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your RCS campaign, you need to specify the *Start date and time* and *End date and time* under the *When* section. You also have the option to start a campaign immediately by selecting *Now*.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="Define WhatsApp Schedule" alt="In the When section, you need to define the start and end time for the campaign" align="center" border={true} src="https://files.readme.io/748dd43-WhatsApp_When.png">
  Define The Campaign Schedule
</Image>

### Delivery preferences

 In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

You can select the *Do Not Disturb* (DND) hours during which messages from this RCS campaign are prevented from going out, either by discarding them or delaying delivery after DND hours complete, such as 9 PM to 9 AM.  

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Additionally, you can check the *Cut-Off* checkbox to avoid sending messages to users after a set cut-off time. This is important for time-sensitive campaigns, for example, live events. 

<Image title="Whatsapp Delivery Preferences" alt="Under the delivery preferences, you can explicitly define the DND and cut-off timings." align="center" border={true} src="https://files.readme.io/a6cb503-Whatsapp_DP.png">
  RCS Delivery Preferences
</Image>

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="Publish Campaign" alt="After setting up the overall campaign, click the Publish Campaign button" align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish Campaign
</Image>
