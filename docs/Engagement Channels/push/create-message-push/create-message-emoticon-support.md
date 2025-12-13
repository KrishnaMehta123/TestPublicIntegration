---
title: Create Message
excerpt: Learn how to create a Push campaign using the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Push Campaign

Create a campaign to deliver your push message.  
To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec0c217-Select_all_channel.png",
        "Campaign Button Lists All Channels",
        1360
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select Messaging Channel"
    }
  ]
}
[/block]


The campaign page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Expand Each Section",
        1404
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create Campaign"
    }
  ]
}
[/block]


4. Define all the sections and publish the campaign. 

## Start Campaign Setup

The _Start here_ section displays the setup information. 

This section has the following parts:

- **Start here**:  Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. 
- **Qualification criteria**: Deliver the notification by Past behavior/Custom list, Live behavior, or [External Trigger](doc:external-trigger). For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
- **Set a Goal**: You can track your campaign conversion by setting up a goal. This is optional. You can define your conversion goal further by selecting the Event and Conversion time. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. 

The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced to purchase an X amount?_ to _How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_ ". 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Track Conversions",
        919
      ],
      "align": "center",
      "border": true,
      "caption": "Set a Goal"
    }
  ]
}
[/block]


## Define the Audience

You must indicate the target audience for your campaign from the _Who_ section. You can specify your target audience from the _Target segment_ section. You can create a new segment or use a previously saved user segment from the _segment_ list. 

For Past Behavior segments, you also calculate the estimated reach. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/030202d-Push_notification_editor_Who.png",
        "Define Target Audience",
        1168
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Define Target Segment - Who"
    }
  ]
}
[/block]


### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

> 🚧 Delay > 24 Hours
> 
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live _Inaction within time_ campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; that is the golden window within which most users transact on iOS and Android app platforms.

On this basis, you would then set up the _Who_ by sending this campaign to all users who qualify or limit the users who qualify under _Estimated reach_. 

> 🚧 Event Source
> 
> To trigger push campaigns, the event source should be from a mobile device rather than the web.

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Deliver Messages based on Past Behavior (PBS)

You can also target users their past user behavior. For past behavior campaigns, you also have an option to calculate estimated reach. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users via mobile push.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbc719c-user_properties_all.png",
        "Add Multiple User Properties",
        486
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
    "4-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_. These filters help analyze the communication preferences of the users with the help of the following flags:  \n  \n<li> _MSG-push_: Indicates that the user has enabled push notification from the application. Works in combination with the DDND Flag.</li>  <li> _MSG-sms_: When set to true, it indicates that the user has subscribed to SMS notifications. When set to false, it indicates that the user does not want to receive SMS notifications.</li> <li> _MSG-email_: When set to true, it indicates that the user has subscribed to Email notifications. When set to false, it indicates that the user does not want to receive email notifications.</li> <li> _MSG-whatsapp_: When set to true, it indicates that the user has subscribed to WhatsApp notifications. When set to false, it indicates that the user does not want to receive WhatsApp notifications. </li>\nFor more information about each of these flags, refer to communication preferences listed under the [Manually Updating Predefined User Profile Properties](https://developer.clevertap.com/docs/concepts-user-profiles#manually-updating-predefined-user-profile-properties) section.",
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


To know more about what segments can be used, see [Segments](doc:segments).

### Constant event property

This is an advanced feature that allows you to hold a property constant across the selected events. For more information, refer to [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c730cf7-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Control Group"
      ],
      "align": "center",
      "border": true,
      "caption": "Control Group"
    }
  ]
}
[/block]


### Targeting Cap

You can limit the number of users receiving the message. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fdf9fb-Control_Campaign_Reach.png",
        "Control Campaign Reach",
        "Target Cap in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Target Cap in Campaign"
    }
  ]
}
[/block]


## Define Message Content

You can have up to four variations of message content in the _What_ section:

- [Single Message](doc:create-message-push#single-message)
- [AB Test](doc:create-message-push#ab-testing)
- [Split Delivery](doc:create-message-push#split-delivery)
- [By User Property](doc:create-message-push#split-delivery)

Click _Go To Editor_ to create your message. 

## Push Editor

The Push Editor allows you to create and edit beautiful and timely messages for your push campaign. From the _What_ section, click _Go To Editor_ to create your message. This section displays the editor to create your push message. You can see various options that will help you create a contextual and timely message. 

Enter the details. For the Title and Message fields, you can use the following options to create personalized and engaging campaigns:

- Use _@_ personalization or _{{}}_ to create more [personalized](https://docs.clevertap.com/docs/personalize-message-all)  or enticing messages. Enter the required details to create the message.
- Use emoticons (![](https://files.readme.io/9e57d16-Emoticon.png)) to create more engaging and visually appealing messages, which can capture the audience's attention more effectively than plain text. Emojis, unlike simple emoticons, can indeed be more complex and take up varying amounts of space in text.
- Use [Scribe](doc:scribe), the first and only AI-powered writing assistant that can also analyze and adjust the emotional tone of your content. It helps generate attractive and emotionally relevant messages for your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37f2b95-Create_Push_Message.png",
        "Edit,Personalize, Preview, and Test",
        971
      ],
      "align": "center",
      "border": true,
      "caption": "Message Editor"
    }
  ]
}
[/block]


You can add a fixed (or with dynamic replacements) URL for Android (Image only) and iOS (Image and video) for rich push notifications.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bfe2c44-Rich_Push_Notifications.png",
        "Message and Media",
        "Screen shows single message editor with image URL selected"
      ],
      "align": "center",
      "border": true,
      "caption": "Rich Push Notifications"
    }
  ]
}
[/block]


You can add an image carousel to your iOS push notifications, with each image having its own caption, sub-caption, and call-to-action URL (fixed or with dynamic replacements).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b0bb0ab-Push_notification_ios_advanced_editor.png",
        "Create Image Slides",
        1294
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Adding Images to Push Notifications"
    }
  ]
}
[/block]


You can add default or custom (fixed or with dynamic replacements) sound files to your Android and iOS push notifications.

You can add a deep link (fixed or with dynamic replacement) to the Android or iOS push notification and lead the users to specific screens when they click it.

### Push notification delivery

You can further increase the delivery of push notifications by sending a copy of the same message to App Inbox. For more information, see [Optimize Delivery](doc:push-optimize-delivery).

### Advanced iOS Settings

#### Rich Media

Upload, add images, or a carousel for your push notifications.

#### Interruption Level

In iOS versions earlier than 15, users could silence all calls and notifications by enabling _Do Not Disturb_ mode. Starting with iOS 15, users can customize their notification preferences for various situations, achieved by configuring notification modes such as Work, Sleep, and Personal. With iOS 15, Apple introduced four interruption levels, including time-sensitive and critical notifications, to ensure urgent alerts, like weather emergencies, reach users effectively.

These interruption levels determine the priority and delivery timing of notifications, allowing users to be in control of their device notifications. The interruption levels are designed to cater to different scenarios while respecting user preferences and focus modes. Here are the three interruption levels:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/16b0085-image.png",
        null,
        "Interruption Level"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Interruption Level"
    }
  ]
}
[/block]


- Active (default)
  - Behavior: Active notifications replicate the existing notification behavior. They trigger audible sound, vibration, and illuminate the screen upon delivery.
  - Focus Mode Compatibility: Active notifications do not break through Focus modes, ensuring that the user's selected focus settings remain undisturbed.
  - Purpose: Use this interruption level for notifications that require immediate attention and engagement.
- Time sensitive:
  - Behavior: Time-sensitive notifications share similarities with active notifications. However, they are accompanied by a distinctive yellow banner, making them visually recognizable as urgent.
  - Focus Mode Compatibility: These notifications have the capability to break through both scheduled delivery times and active Focus modes.
  - Purpose: Reserve the Time Sensitive interruption level for notifications demanding immediate user action. Their unique appearance aids users in identifying critical messages quickly.
- Passive:
  - Behavior: Passive notifications are designed for non-urgent matters. They arrive discreetly without generating sounds or vibrations.
  - Focus Mode Compatibility: Passive notifications are considerate of users' Focus modes and do not disrupt them.
  - Purpose: Employ the Passive interruption level for notifications that do not require instant attention, minimizing distractions while keeping users informed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4a900d7-image.png",
        null,
        "Time Sensitive Notifications"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Time Sensitive Notifications"
    }
  ]
}
[/block]


> 📘 Critical Interruption Level
> 
> Currently, this _Interruption level_ is not available in CleverTap dashboard. We recommend contacting your Customer Success Manager and sharing your use case if you want to send the campaign from the dashboard with _Interruption level_ set as _Critical_.

#### Relevance Score

Users have the flexibility to determine the timing of their daily summary's appearance on their iPhones. Marketers can now set up the _Relevance Score_ for every notification when creating a Push campaign. This directly impacts the order of notifications when grouped. The score ranges from 0 to 1, this score guides the system in arranging the notifications for your application. The notification with the highest score takes precedence in the summary. This feature was introduced in iOS 15 and later versions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a10efa-image.png",
        null,
        "Relevance Score"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Relevance Score"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64c07d2-image.png",
        null,
        "Mapping of Relevance Score into Summary"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Mapping of Relevance Score into Summary"
    }
  ]
}
[/block]


#### Other Media

#### Sound File

You have to specify the name of the sound file which is included in your app bundle. Apple supports .aiff, .caf and .wav extensions. 

#### Badge Count

This updates the badge count for your app to the one specified while creating the campaign. Please note that this does not increment the badge count or set the value to 0 (zero) to hide the badge number. This should be handled manually at the application level.

#### Category

You can input the name of the category while creating the campaign. Each category has to be registered with the app. Each such category is associated with actions that the user can perform when a notification of a rich media type is delivered. Each category can have up to four actions associated with it, although the number of actions actually displayed depends on the type of notification delivered. This provides users the ability to take multiple actions for the notification. 

> 👍 Multiple Buttons Example
> 
> A single media push notification can have two buttons such as, _Buy Now_ and _Save for Later_.

#### Content Available

If you include the content-available key with a value of 1 to send out a silent notification to your users. It will not alert the user in any way (update badge count/play a sound/show a notification), but it will wake your app up in the background so you can fetch new content and prepare it for the next time the user opens your app.

Key: content-available  
Value: 1

#### Deep Link/Open URL

Deep links allow you to land the user to a particular part of your app. Your app’s OpenURL method is called with the deep link specified here. If you want to use external URLs, then you have to whitelist the IPs or provide http/https before the URL so they can be handled properly by the SDK.

#### Mutable Content

Check this box if you would like to send the mutable-content flag along with your payload. This invokes your app’s notification service extension. For more information, refer to [Modifying Content in Newly Delivered Notifications](https://developer.apple.com/documentation/usernotifications/modifying_content_in_newly_delivered_notifications) in the Apple documentation.

### Advanced Android Settings

#### Add Custom Actions to Android Notifications

A simple way to urge users to respond to your calls to action is by adding button-like actions right into your Android push notifications. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/630d0b1-Push_notification_android_action_button.png",
        "Add Buttons and Deeplinks",
        "Screen shows adding button actions into your notification"
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Custom Actions for Android Notifications"
    }
  ]
}
[/block]


Once set up, the various calls to action would display below the push as displayed below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a91ddec-Push_notification_example.jpg",
        "Push Notification with CTAs",
        1080
      ],
      "align": "center",
      "caption": "Sample Push Notification"
    }
  ]
}
[/block]


#### Notification Priority

You can set these priority levels from the CleverTap dashboard as you create your Android push campaigns. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ea564e-Notification_Priority.png",
        null,
        "Notification Priority"
      ],
      "align": "center",
      "border": true,
      "caption": "Notification Priority"
    }
  ]
}
[/block]


Have your app running our latest SDK (versions v3.1.4 or higher) and follow the steps outlined above to send actionable push notifications and set notification priority on Android devices.

#### Notification Tray Priority

On Android, you can also set a priority level for each notification to influence how prominently it is displayed. The higher the priority, the more noticeable it will be.

##### Default Priority

Use most of your messages that are not time-sensitive, such as general notifications and promotional offers.

##### High Priority

Use for important communications that require extra attention, such as chat messages. These will also display as heads-up notifications and be given a higher priority in the user’s tray. Heads up notifications are notifications that pop up on your screen from the top even when you are using other apps. For example, receive a message on your chat app when you’re using the food delivery app. This feature is available for Android N (API 25) and below. For Android Oreo and above, define the priority in the _Notification Channel_.  

##### Maximum Priority

Use for urgent, time-sensitive notifications. These notifications will get higher placement inside the user’s tray and display as heads-up notifications.

#### Notification Delivery Priority

You can assign delivery priority on Android for Push messages as follows: 

- _Normal_:  The data messages with normal priority are delivered immediately when the device is active. However, if the device is inactive to conserve battery, the delivery may be delayed until the device becomes active again. You must set the priority as _Normal_ for less time-sensitive messages (such as notifications of new emails, keeping your UI in sync, or syncing app data in the background).
- _High_: The messages with high priority are delivered immediately, even if the device is asleep. It wakes the device and allows limited processing (including minimal network use) to ensure the message is received. These messages are meant to provoke user action or response to your app or its notifications. You must set the priority as _High_ for time-sensitive or user-visible content. CleverTap recommends setting the notification priority as _High_ to ensure the time-sensitive content is rendered immediately on end-user devices. If FCM detects a pattern in which messages do not result in user-facing notifications, the messages are deprioritized to normal priority.

The value for this field is set to _High_ by default. 

> 📘 Notification Priority for Cloned Campaigns
> 
> Cloned campaigns retain the priority setting from the original campaign.

#### Collapse Key

To replace an existing notification with the same collapse key, you can use the collapse notification option. For example, if push X and push Y have a collapse key A. Push X notification is present on the mobile device when push Y notification is received. The push X notification will no longer be visible (it will be collapsed), and push Y will be displayed. The collapse key must be added under the collapse notification field. For more information, see [Collapse Key](doc:collapse-key).

#### Custom key-value pair

You can send custom data with the notification payload using this option. This payload allows the app to perform any business logic preconfigured within the app. For example, you can send a push campaign that offers a 20% discount to your users who interact with the campaign. Now, if the user taps on the notification, they are directed to the discounts page that offers a 20% discount.

Also, if you select the _Send a copy of this message to the App Inbox_ option when creating a push campaign, the key-value pairs in the campaign are also included in the App Inbox message. To access this feature, ensure that you upgrade to SDK version 5.2.0 or higher.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5bc89d0-image.png",
        null,
        "Send a Copy of the Push Notification to the App Inbox"
      ],
      "align": "center",
      "border": true,
      "caption": "Send a Copy of the Push Notification to the App Inbox"
    }
  ]
}
[/block]


### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send a test push notification to any CleverTap user profile you have marked as a _Test profile_.  
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

- Single Message
- AB Test
- Split Delivery
- By User Property

### Single Message

This message type allows a single message copy to be set up for the entire audience. This message copy can be [personalized](https://docs.clevertap.com/docs/personalize-message-all) for each qualifying user. This message type is best suited for use cases where the message doesn’t vary much based on user properties such as language, geography, and so on.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

You can send up to 3 message variants to test groups to determine which campaign performs the best.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d99162-AB_Test_all.png",
        "Identify Best Variant",
        881
      ],
      "align": "center",
      "border": true,
      "caption": "A/B Test  Variant Distribution"
    }
  ]
}
[/block]


### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration. You can test up to three message variants. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/890fc40-Push_notification_split_delivery.png",
        "Control Variant Distribution",
        "Screen shows split Delivery Variant Distribution and message preview"
      ],
      "align": "center",
      "border": true,
      "caption": "Split Delivery Variant Distribution"
    }
  ]
}
[/block]


#### Split Delivery to Past Behavior Segments

For campaigns sent to _Past Behavior Segments_ (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

- If you test three messages (Variant A, Variant B, Variant C).
- Your campaign reach is 2,000,000 users.
- Your test population is 15% of the campaign reach (300,000 users).

Then, we send:

- Variant A to 100,000 users.
- Variant B to 100,000 users.
- Variant C to 100,000 users.

After delivering 300,000 messages, we calculate the winning message over this test group based on the number of click-throughs. In this example, we then automatically send the winning message to the remainder of your target audience, which is 1,700,000 users.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches your selected criteria. For example, you can send a message when the user has completed a booking or purchase. Because it is impossible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. Suppose your test group size exceeds the total number of users who ultimately qualify for that campaign. In that case, no winner will be declared, and each message variant will be alternatively delivered for the campaign's duration.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be sending a localized update to people based on their preferred language.

You can send up to 50 message variants to different users based on a user property.

Similar to creating A/B test variants, click  **+ Variant** to add multiple variants based on a user property value. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bae92cd-2022-12-22_10-18-35.png",
        "Upto 50 Message Variants",
        2780
      ],
      "align": "center",
      "caption": "Message Variant by User Property"
    }
  ]
}
[/block]


In the example below, we have used the _Customer Type_ user property so users with different customer type property values receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f61b2f-2022-12-22_10-15-38.png",
        "Different Variant for Each Customer Type",
        2532
      ],
      "align": "center",
      "caption": "Message by Customer Type"
    }
  ]
}
[/block]


## Define Campaign Schedule

You can set up the _When_ section to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

- On a specific date and time.
- On multiple specified dates and times.
- Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

- In response to a user event.
- User event/inaction combination (for example, abandoned cart scenario).
- Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

### Delivery preferences

You can apply global campaign limits to determine how many push notifications each app user receives per day. If you want to override these settings for an important campaign, you can click on the _Don’t apply global campaign limits to this campaign_ checkbox.

You can also click the _Advanced_ checkbox to specify _Do Not Disturb_ (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/60373b1-PBS_Delivery_Preferences.png",
        "Changes Based on Segment Selection",
        2214
      ],
      "align": "center",
      "border": true,
      "caption": "Message Delivery Preference"
    }
  ]
}
[/block]


> 📘 Recurring Day
> 
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

#### Time to Live

**Time to Live** is the notification's persistence sent to an end user. Push services such as FCM, APNS, XPS, Baidu, and HMS manage Time to Live. They regulate the time the system monitors user device status to deliver a push notification. Whenever the user is online during the set TTL period, the notification is delivered. Any user not coming online will not receive the push notification, and no notifications are attempted after the TTL period is over.

There are two ways to configure the TTL for push notification delivery. Conceptually, they are referred to as _Relative TTL_ or _Absolute TTL_. 

- Relative TTL: Push services attempt to send the notification only for the duration mentioned here. Specify the _duration_ you want the notification to live.  
  Select the first option to specify a TTL duration and ensure a push notification is active until the user is online if unavailable and there are no hard time limits. 
- Absolute TTL: Push services try and send the notification only _until the specified time_ here. State the time until when you want the notification to live.  
  Select the second option to specify a TTL time limit to ensure a push notification is active until that date and time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d69dc51-TTL.png",
        "Relative and Absolute TTL",
        832
      ],
      "align": "center",
      "border": true,
      "caption": "Time to Live for a Message"
    }
  ]
}
[/block]


> 📘 Note
> 
> Absolute TTL is available only for the following campaign types: 
> 
> - Send Now
> - Schedule for later except recurring schedules and _Best time for every user_. 
> 
> Relative TTL is available for all campaign types.

##### Use Cases

| Industry Type and Target Group                                                                                                  | Need                                                                                                                        | Don't Need                                                                   | TTL Selection                                                                                                                                                                                 |
| :------------------------------------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A ride-sharing app running campaigns to target office goers in the morning.                                                     | They want the push notification to be sent to the office goers in the morning peak hours. Ideally between 7:30 to 10:30 am. | Notification should not be sent in the afternoon as it  loses the relevance. | They would keep the campaign scheduled time at 7:30 am and set the **_relative_** TTL for 3 hours. This would ensure that the notification is sent between 7:30 am and 10:30 am.              |
| A cricket information app wants to provide latest updates to their users' regarding the cricket match/es scheduled for the day. | They want to send a push notification to their users advising on the coin toss of a particular match scheduled at 7pm.      | Notification should not be sent after 7:10 pm as it is no more relevant.     | Campaign will be triggered at 7 pm and the **_absolute_** TTL will be set to 7:10 pm. Any user who comes online after 7:10 pm will not get the notification even if they qualified initially. |

#### Cut-off

The campaign cut-off time ensures no notifications are sent after the specified time. Clevertap does not send notifications to the push services after the cut-off. This is useful if the campaign is time-sensitive and a later time makes the notification irrelevant.  
Select the _Cut-off_ checkbox and specify the time to stop sending the notification when the number of target users is large, causing a significant delay in processing the user queue. This ensures that after the set time, there's no notification sent. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5048266-Cut_Off.png",
        " Avoid Delay in Processing",
        456
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Campaign Cut-Off Time"
    }
  ]
}
[/block]


##### Use Case

| Industry Type and Target Group                                                                                  | Need                                                                            | Don't Need                                                                                | Usage Scenario                                                                            |
| :-------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- |
| An e-commerce app has around 10 million users and is running a 'Discount' sales offer which would end at 12 am. | They want to send the push notification to all of their users at the same time. | Notification should not be sent after 12 am as the notification would lose its relevance. | Assuming that the processing of the user queue takes 10 mins, set the cutoff to 11:50 pm. |

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Final Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]