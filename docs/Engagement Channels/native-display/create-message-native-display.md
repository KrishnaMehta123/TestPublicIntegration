---
title: Create Message
excerpt: Learn how to create a Native Display campaign using the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel. 

<Image title="Click +Campaign and Select Web Native Display" alt={1360} align="center" width="80%" border={true} src="https://files.readme.io/7c22c2d739e4ab963bad5c7a8bfcc5a38da26fe1f120aee0dbad90ced26a7a46-Native_Display.png">
  Select Native Display Campaign
</Image>

The campaign page displays.

<Image title="Create a new native display campaign" alt={1404} align="center" width="80%" border={true} src="https://files.readme.io/a805f56-Campaign_Creation_Page.jpg">
  Creating a Native Display Campaign
</Image>

Define all the sections and publish the campaign. 

## Start Campaign

The *Start here* section displays the setup information. 

This section has the following parts:

* **Set a goal**: Tracks your campaign conversions by setting a goal. This step is optional, but it helps you measure how effectively your campaign meets its goal.\
  You can define your conversion goal by selecting the *Event* and specifying the *Conversion Time*. The *Conversion Time* field accepts any numeric value along with a time unit such as Minutes, Hours, Days, Weeks, or Months. This allows you to define conversion windows such as 10 days, 72 hours, or 2 months. The value can range from a minimum of 1 minute to a maximum of 5 months.\
  For example, if you set the conversion time to 5 Minutes, the system counts conversions within 5 minutes of the goal event.\
  Your campaign goal can be as broad or as specific as you want. For example, you can answer questions such as: *How many users were influenced to purchase an X amount?* or *How many first-time visitors purchased red shoes worth at least X and blue jackets worth at least Y?*

<Image alt="Set Conversion Time" align="center" width="75% " border={true} src="https://files.readme.io/d960f90056d978b5c9f8832e66c2b3c15b6e387d3caa38ea6bc0b138c57d6b29-Conversion_Tracking.png">
  Set Conversion Time
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

<Image alt="Define the Target Audience" align="center" border={true} src="https://files.readme.io/851a35802697f148e8e133ccabd54afba9d2ba01e4a2be414a690088bd0dca68-image.png">
  Define the Target Audience
</Image>

> ❗️ Source Event Property
>
> The CleverTap source event property is not supported for web pop-up and mobile in-app campaigns.

> 🚧 Warning
>
> When multiple Native Display campaigns are created for a single event scheduled to run simultaneously, CleverTap delivers the first campaign that was created.

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Ad-hoc Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your In-App campaign. You can create the target on the basis of user properties, or live (ongoing) user behavior (the latter is useful to send out real-time, triggered In-App campaigns).

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

<Image title="Filter By User Properties" alt={486} align="center" border={true} src="https://files.readme.io/3d4faa2-Filter_By_User_Properties.png">
  Filter by User Properties
</Image>

To know more about what segments can be used, see [Segments](doc:segmentation).

### Calculate Estimated Reach

The Estimated Reach option allows you to preview how many users meet your targeting criteria in an online trigger campaign before publishing it. This helps you validate audience size and adjust filters to ensure the campaign reaches the intended users. 

Estimated Reach is particularly useful when you select the *Filter on past behavior and user properties* option. You can view both the estimated user count and device count. 

To calculate the estimated reach, perform the steps below: 

1. Select **Filter on past behavior and user properties**. 
2. Click **Calculate** in the right panel. The result shows the estimated number of users or devices for that segment. You can view the following: 
   * **Total Users**: The number of users that match the filters. 
   * **Breakdown by Platform and Devices**: The users count on Android, iOS, or both, and on different devices. 
   * **Visual Indicator**: A chart summarizing the share by operating system.\
     The estimate, based on the latest available event data, updates each time you apply or modify filters. It reflects stored event data and is not a real-time count. This helps you plan and refine your audience before sending the campaign. 

<Image alt="Calculate Estimate Reach" align="center" width="85% " border={true} src="https://files.readme.io/44bb9f5c34466e181b1934a67365951c488221905a4373e546dfa48b7b152db8-2025-09-08_16-57-15_1.gif">
  Calculate Estimate Reach
</Image>

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image alt="Set a Control Group" align="center" border={true} src="https://files.readme.io/29b0606c8b4473cbc0f14df43725f1df5964f370c1b3c523af38831b5cf447ff-image.png">
  Set a Control Group
</Image>

## Define the Message Content

Now, you can set up the *What*, which is the campaign content, with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

### Native Display Templates

<Image alt="Native Display Templates" align="center" border={true} src="https://files.readme.io/0ed2991caf33177b12a18dc69e93fadd44ff915f07d70febf8d17655b580b64b-image.png">
  Native Display Templates
</Image>

You have the following types of message templates:

#### Content with image notifications

1. Simple Message 
2. Carousel Message
3. Message with icon
4. Custom key-value

#### Image only notifications

1. Carousel Message 
2. Simple Message

#### Simple Message

A simple message consists of the following elements:\
(a) Title.\
(b) Message.\
(c) Media (optional): jpg, gif, mp4 video, and mp3 formats are supported.\
(d) Call to action (optional\
(e) Custom key-value pairs

#### Carousel Message with Content

This template is a multi-slide template where you can draft up to five slides containing images with content. The carousel in the user app displays in the form of right and left scrolls. This is a rich template that can be used to promote a list of products or movies that will release this weekend.

#### Carousel Message without Content (Image Only)

This template is similar to the *Carousel Message with Content* template but without a title, text, and messages. 

#### Message with Icon

This template is similar to the *Simple Message* template with the extra ability to include an additional icon placeholder.

#### Custom Key Value

The custom key-value can have any value. 

For example, if you want to change the carousel images for your users based on their language and favorite food, you can set the custom key-value pairs for this change.

<Image title="Define Custom key-value pairs for Native Display campaign" alt={695} align="center" border={true} src="https://files.readme.io/7d13320-Native_display_custom_key_value_pairs.png">
  Custom Key-Value Pairs
</Image>

### Supported File Formats

The supported file formats include .jpg, .jpeg, .png, .gif, .mp3, .mp4 (.png's convert to .jpeg using selected background color).

The following are the supported media types: 

| Template          | Template Category                 |
| :---------------- | :-------------------------------- |
| Simple Message    | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Carousel Message  | Media (images, gif) only          |
|                   | Media (images, gif) + Text        |
| Message with icon | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Custom key value  | Any                               |

### Native Display Editor

The message builder for *Native Display* is where you can create a rich message to engage your targeted audience.

Enter your text and message.

<Image alt="Native Display Editor" align="center" border={true} src="https://files.readme.io/20202472bd346ee3dbf1ab4168bd51dfbeb4c33c74ede38aeb47453687bf2355-image.png">
  Native Display Editor
</Image>

#### Compose

You can upload media from your image library or use personalized media to compose your messages. 

Enter the title and message, and upload or personalize media as required. 

*Native Display* enables various types of call to action (CTA) to cater to different use cases.

 Choose from one of the following  actions (Optional):

 On-message CTA URL: A click on this URL opens a deep link when you click anywhere on the message (text or image or both).

* Open URL CTA: The user can open deep links for iOS or Android. 
* Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the *Native Display* button. This data is not visible to the user. 

#### Style

Select the style for your notification, such as background color, text color, and message color. 

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*\
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

* Single Message
* AB Test
* Split Delivery
* By User Property

#### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign. You can test up to three message variants.

<Image title="Configure Split Delivery for Native Display Campaign" alt={577} align="center" border={true} src="https://files.readme.io/73d579a-campaign_split_delivery.png">
  Split Delivery in Native Display
</Image>

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared, and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, click **+ Variant** to add multiple variants based on a user property value. You can send up to 50 message variants to different users based on a user property. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum). 

<Image title="Define User Properties" alt={486} align="center" border={true} src="https://files.readme.io/6db3703-user_properties_all.png">
  Define User Properties
</Image>

## Define the Campaign Schedule

The delivery preferences for Live campaigns can be set as follows:

* Start Date and Time
* End Date and Time
* Set Delay

<Image title="Define the Campaign Schedule" alt={974} align="center" border={true} src="https://files.readme.io/0637733-Campaign_When_Live_segment.png">
  Define Campaign Schedule
</Image>

### Delivery preferences

#### Set frequency

From the Delivery preferences section, select the days and the time frame to deliver the message.\
Click *Apply to all* to copy the choices from the selected day to all other days. 

<Image title="Set the Delivery Preferences" alt={1085} align="center" border={true} src="https://files.readme.io/1cdcf37-Delivery_preferences_-_Native_Display.png">
  Set Delivery Preferences
</Image>

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

<Image title="Publish the Campaign" alt={1193} align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish Campaign
</Image>
