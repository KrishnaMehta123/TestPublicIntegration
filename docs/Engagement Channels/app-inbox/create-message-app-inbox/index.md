---
title: Create Message
excerpt: Learn how to create an App Inbox campaign using the CleverTap dashboard.
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

To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.

<Image align="center" alt={2720} border={true} caption="Select Messaging Channel" title="Click +Campaign to Create a New App Inbox Campaign" src="https://files.readme.io/cb65ccd2db4e37aaf774be6af24b14c0d55fce0622c5bac39152b987466aa15b-Select_a_Campaign_from_Campaign.png" width="smart" />

The campaign page displays.

<Image align="center" alt={1404} border={true} caption="Create App Inbox Campaign" title="Create a new App Inbox Campaign" src="https://files.readme.io/a805f56-Campaign_Creation_Page.jpg" width="80%" />

Define all the sections and publish the campaign.

## Start Campaign

The _Start here_ section displays the setup information.

This section has the following parts:

* Qualification criteria: Deliver the notification by Past Behavior, Custom List, or Live behavior. For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* **Set a goal**: Tracks your campaign conversions by setting a goal. This step is optional, but it helps you measure how effectively your campaign meets its goal.  
  You can define your conversion goal by selecting the _Event_ and specifying the _Conversion Time_. The _Conversion Time_ field accepts any numeric value along with a time unit such as Minutes, Hours, Days, Weeks, or Months. This allows you to define conversion windows such as 10 days, 72 hours, or 2 months. The value can range from a minimum of 1 minute to a maximum of 5 months.  
  For example, if you set the conversion time to 5 Minutes, the system counts conversions within 5 minutes of the goal event.  
  Your campaign goal can be as broad or as specific as you want. For example, you can answer questions such as: _How many users were influenced to purchase an X amount?_ or _How many first-time visitors purchased red shoes worth at least X and blue jackets worth at least Y?_

<Image align="center" alt="Set Conversion Time" border={true} caption="Set Conversion Time" src="https://files.readme.io/d960f90056d978b5c9f8832e66c2b3c15b6e387d3caa38ea6bc0b138c57d6b29-Conversion_Tracking.png" width="75% " />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list.

For Past Behavior segments, you also calculate the estimated reach.

<Image align="center" alt="Define Target Audience" border={true} caption="Define Target Audience" src="https://files.readme.io/20e64c1f82b3e0eec429fbe0a62b34b40057921de401e9b49a2ecb9b124f1522-image.png" width="80% " />

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

> 🚧 Delay > 24 Hours
>
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live _Inaction within time_ campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes.

On this basis, you would then set up the _Who_ by sending this campaign to all users who qualify or limit the users who qualify under _Estimated reach_.

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

> 🚧 Warning
>
> When multiple Triggered App Inbox campaigns are created for a single event scheduled to run simultaneously, CleverTap delivers the first campaign that was created.

### Deliver Messages based on Past Behavior (PBS)

You can also target users basis their past behavior. For past behavior campaigns, you also have an option to calculate estimated reach to view how many:

* Number of users that qualify for the campaign criteria.
* Number of users that are reachable via mobile push as of now.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria.

For example, you can send a push notification to English-speaking female users who live in the United States.

<Image align="center" alt={486} border={true} caption="Filter by User Properties" title="Filter By User Properties" src="https://files.readme.io/cbc719c-user_properties_all.png" />

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
        Demographics filters include _Age_ and _Gender_.
      </td>

      <td>
        Age = 25 to 40 years  
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States  
        State = California  
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
        Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.
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
        App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
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

### Calculate Estimated Reach

The Estimated Reach option allows you to preview how many users meet your targeting criteria in an online trigger campaign before publishing it. This helps you validate audience size and adjust filters to ensure the campaign reaches the intended users.

Estimated Reach is particularly useful when you select the _Filter on past behavior and user properties_ option. You can view both the estimated user count and device count.

To calculate the estimated reach, perform the steps below:

1. Select **Filter on past behavior and user properties**.
2. Click **Calculate** in the right panel. The result shows the estimated number of users or devices for that segment. You can view the following:
   * **Total Users**: The number of users that match the filters.
   * **Breakdown by Platform and Devices**: The users count on Android, iOS, or both, and on different devices.
   * **Visual Indicator**: A chart summarizing the share by operating system.  
     The estimate, based on the latest available event data, updates each time you apply or modify filters. It reflects stored event data and is not a real-time count. This helps you plan and refine your audience before sending the campaign.

<Image align="center" border={true} caption="Calculate Estimate Reach" src="https://files.readme.io/da8061b11683530657139eade7dd9c353fa3ac7656613e56e36eb74af910963e-2026-01-30_19-12-06_1.gif" width="85% " />

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image align="center" alt="Define Control Group" border={true} caption="Define Control Group" title="Control Group and Target Cap" src="https://files.readme.io/b22a399-Control_Group_and_Target_Cap.png" />

### Targeting Cap

You can limit the number of users receiving the message.

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
>
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

<Image align="center" alt="Set a Target Cap" border={true} caption="Set a Target Cap" src="https://files.readme.io/d7f1544-Control_Campaign_Reach.png" />

## Define the Message Content

Now, you can set up the _What_, which is the campaign content with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click _Go To Editor_ to create your message.

### App Inbox Templates

You have the following four choices of message templates to create your message:

<Image align="center" alt={807} border={true} caption="App Inbox Message Templates" title="Select an App Inbox template" src="https://files.readme.io/63a8c31-App_Inbox_templates.png" />

#### Simple Message

A simple message consists of the following elements:  
(a) Title.  
(b) Message.  
(c) Media (optional): jpg, gif, mp4 video, and mp3 formats are supported.  
(c) Call to action (optional).

For example, the user receives the app inbox message stating "Your order has been accepted by the restaurant after placing an order.

<Image align="center" alt={232} border={true} caption="App Inbox Notification - Simple Message" title="Sample App Inbox Message" src="https://files.readme.io/6ee6624-app_inbox_simple_message.png" width="sma% " />

#### Carousel Message with Content

This is a multi-slide template where you can draft up to five slides containing images with content. The carousel in the user app displays in the form of right and left scrolls. This is a rich template that can be used in situations such as promoting a list of products or movies that will release this weekend.  
You can also add a link for each carousel message to navigate the users to that particular page.

<Image align="center" alt={222} border={true} caption="App Inbox Notification - Carousel Message with Content" title="Sample App Inbox Carousel with Content" src="https://files.readme.io/cc1b308-app_inbox_carousel-1.png" width="smart" />

Along with the advertising images, you can add the related headline in the message content and use personalization in these messages.

#### Carousel Message without Content

This template is similar to the one right above but without a title text and messages. Carousel messages without content can be made attractive to grab the user's attention and convey your purpose for the campaign. You can add promotional campaign creatives about your products as an image without any text message.

#### Message with Icon

This template is similar to the simple message with the extra ability to include an additional icon placeholder. You can add a single image in the given format along with any personalized or generic title and text that you would like to send to the users.

<Image align="center" alt={245} border={true} src="https://files.readme.io/6a9e5c2-message_with_icon.png" title="Sample Message with Icon" className="border" />

### App Inbox Editor

The message builder for _App Inbox_ is where you can create a rich message to engage your targeted audience.

Enter your text and message.

<Image align="center" alt="App Inbox Editor" border={true} caption="App Inbox Editor" src="https://files.readme.io/32cce94268fc32db803ec34d3083de4deb6f2fca94c6c5d63954e4e5c6a9ba32-image.png" width="80% " />

#### Call to Action

_App Inbox_ enables various types of call to action (CTA) to cater to different use cases for the client.

Choose from one of the following five types (Optional):

* Click-on-message CTA: This opens a deep link when you click anywhere on the message (text, image, or both).
* Click-on-link CTA: You can add additional, colored links at the bottom of your message to attract the user's attention.
* Copy to clipboard CTA: The user can copy text to their clipboard such as, copying discount codes to your products and applying them at the time of checkout.
* Open URL CTA: The user can open deep links for iOS or Android.
* Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the _App Inbox_ button. This data is not visible to the user. This feature is available for apps that use Clevertap Android SDK version 3.6.1 or above and iOS SDK version 3.7.1 or above.

<Image align="center" alt={681} border={true} caption="Configuring CTAs" title="Define CTAs for App Inbox" src="https://files.readme.io/3f0fd39-App_Inbox_editor_call_to_action.png" width="80%" />

#### Message Tags

You can tag an inbox message with one or more comma-separated strings (Optional).

These tags help you identify the messages inside the user's device. Also, these tags help you classify your messages into different tabs in your app.

<Image align="center" alt={678} border={true} caption="Define Message Tags" title="App Inbox Message Tags" src="https://files.readme.io/19799ac-App_Inbox_editor_message_tags.png" />

> 📘 Using Message Tags
>
> Message tags are an excellent way to engage your users contextually. For example, some of your app users might be interested in offers while others in news updates. You can have two separate tabs to categorize your inbox messages into those two buckets. Note that it is not compulsory to have tabs.
>
> You can define the names of the inbox tabs during the configuration of _App Inbox_ with your app. The same names should be entered as tags. In case you do not specify any tag, the message will go into the default bucket _All_.

#### Custom Key-Value Pairs

If you have a custom inbox and want to configure the message within CleverTap, you can define the parameters specific to your app and usage using these key-value pairs. For example, you can send an inbox campaign that offers a 20% discount to your users who interact with the campaign. Now, if the user taps on the notification, they are directed to the discounts page that offers a 20% discount. The following is an image that displays defining custom key-value pairs from the dashboard:

<Image align="center" alt="Define Custom Key-Value Pairs" border={true} caption="Define Custom Key-Value Pairs" src="https://files.readme.io/3d5da20-image.png" />

> 📘 SDK Version
>
> To access this feature, ensure that you upgrade to SDK version 5.2.0 or higher.

### Time to Live (TTL)

_App Inbox_ campaigns are by design persisted on the user device for a number of days.

1. You can configure the number of days (or hours) to keep the message on the user's device by setting the _time to live_.

<Image align="center" alt={710} border={true} caption="Define Message Time to Live" title="Define Message Time To Live" src="https://files.readme.io/bbd5393-Campaigns_message_time_to_live.png" />

The TTL can range from 1 day to 60 days. The default value for TTL is 2 days. You can define the TTL for a maximum of 60 days. The message on the user's device stays there for the specified TTL after which it is automatically removed. You can also have _Infinite TTL_ which means the message will never be deleted from the user's device.

> 🚧 Choosing the Right TTL
>
> * You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).
> * The TTL is considered based on campaign sent time.

> 📘 How a Message is Accounted For
>
> Each message stored on the CleverTap platform for _App Inbox_ is accounted for as a user event.

> ❗️ Events via API
>
> For live action campaigns, messages do not get delivered to the App inbox if the qualifying event is sent via API. This only applies to standalone App Inbox campaigns and not Push + App inbox campaigns.

### Supported Media Types

The supported media types include:

| Media Type            | 16:9 Aspect Ratio | 1:1 Aspect Ratio | Max Size |
| :-------------------- | :---------------- | :--------------- | :------- |
| Image (jpg, png, gif) | Yes               | Yes              | 500 KB   |
| Video (mp4)           | Yes               | Yes              | 50 MB    |
| Audio (mp3)           | N/A               | N/A              | 5 MB     |

> 📘 Video Messages
>
> When adding video messages to In-App, ensure an audio track is always present. If required, insert a blank audio track to the video.

### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send a test notification to any CleverTap user profile you have marked as a _Test profile_  
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

* Single Message
* A/B Test
* Split Delivery
* By User Property

### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration. You can test up to three message variants.

<Image align="center" alt={992} border={true} caption="Split Delivery in App Inbox" title="Split Delivery in App Inbox" src="https://files.readme.io/890fc40-Push_notification_split_delivery.png" />

#### Split Delivery to Past Behavior Segments

For campaigns sent to _Past Behavior Segments_ (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

* If you are testing three messages (e.g., Variant A, Variant B, Variant C).
* Your campaign reach is 2,000,000 users.
* You choose a test population of 15% of campaign reach (300,000 users).

Then, we send:

* Variant A to 100,000 users.
* Variant B to 100,000 users.
* Variant C to 100,000 users.

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of click-throughs. We then automatically send the winning message to the remainder of your target audience which is 1,700,000 users in this example.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. You can send up to 50 message variants to different users based on a user property. In the example below, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

## Define the Campaign Schedule

You can set up the _When_ to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

* On a specific date and time.
* On multiple specified dates and times.
* Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

* In response to a user event.
* User event/inaction combination (e.g., abandoned cart scenario).
* Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

<Image align="center" alt="Define Campaign Schedule" border={true} caption="Define Campaign Schedule" src="https://files.readme.io/cdb9dda90862924892201b264e372334f28c7de08d18c092dd5d83b863ae114f-image.png" />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

<Image align="center" alt={1193} border={true} caption="Publish App Inbox Campaign" title="Publish Campaign" src="https://files.readme.io/b521e92-campaign_Publish.png" />
