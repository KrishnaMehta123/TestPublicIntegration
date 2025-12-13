---
title: Create Message
excerpt: Learn how to create an Inbox campaign using the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Create a New Campaign

To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ce73e76-Create_a_New_Inbox_Campaign.png",
        "Click +Campaign to Create a New App Inbox Campaign",
        2720
      ],
      "align": "center",
      "sizing": "smart",
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
        "https://files.readme.io/62c6129-Inbox_Campaign_Page.png",
        "Create a new App Inbox Campaign",
        1404
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create App Inbox Campaign"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign

The _Start here_ section displays the setup information. 

This section has the following parts:

- Qualification criteria: Deliver the notification based on the following
  - _Past behavior/Custom list_: Qualify users based on an activity they performed or have been performing in the past.
  - _External Trigger_: trigger the campaign delivery based on API calls or external events. The API determines the _Who_ and _When_ sections.
- Set a goal: Setting a goal is optional. It allows you to measure your campaign effectively. You can define your conversion goal further by selecting the Event and Conversion time. For more information on event properties, see [Events](doc:events).  
  The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced to purchase an X amount?_ to _How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_ ". 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Enable Conversion Tracking",
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

You must indicate the target audience for your campaign. You can specify your target audience from the  _Target segment_ section. You can create a new segment or use a previously saved user segment from the _segment_ list.  

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties.

### For Past Behavior/Custom List Campaigns

You can also target users based on their past behavior. For past behavior campaigns, you can calculate estimated reach to view the number of users who qualify for the campaign criteria.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8430c10-Define_Target_Audience_-_PBS.png",
        "Define the target audience for your campaign",
        1168
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Define Target Audience For Past Behavior/Custom List Campaign"
    }
  ]
}
[/block]


### For External Trigger Campaigns

External Trigger campaigns are triggered against the user ID. However, marketers can further filter the segment based on past behavior and user properties.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f140cdf-Define_Target_Audience_-_External_Trigger.png",
        null,
        "Define Target Audience For External Trigger Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Target Audience For External Trigger Campaign"
    }
  ]
}
[/block]


For example, an e-commerce portal wants to send order confirmation to the buyer with all the product details. In this case, the users qualify as soon as they purchase, and the External Trigger campaign is sent to the user. Though the trigger remains the same, you can further narrow your target audience by selecting the Filter on past behavior and user properties option. For example, you want to send your Gold members an order summary and a discount code. Here, you are filtering your target audience with the user property Customer Type = "Gold".

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b22a399-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Define Control Group"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Control Group"
    }
  ]
}
[/block]


### Targeting Cap

You can limit the number of users receiving the message. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more users, regardless of the qualified user segment size. If the limit specified is less than 100 users, an error occurs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d7f1544-Control_Campaign_Reach.png",
        null,
        "Set a Target Cap"
      ],
      "align": "center",
      "border": true,
      "caption": "Set a Target Cap"
    }
  ]
}
[/block]


## Define the Message Content

Now, you can set up the _What_, which is the campaign content with four different options:

- Single Message
- A/B Test
- Split Delivery
- By User Property

Click _Go To Editor_ to create your message. 

### Inbox Templates

You have the following four choices of message templates to create your message:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/01da166-Inbox_Message_Templates.png",
        "Select an App Inbox template",
        807
      ],
      "align": "center",
      "border": true,
      "caption": "Inbox Message Templates"
    }
  ]
}
[/block]


#### Simple Message

A simple message consists of the following elements:  
(a) Title.  
(b) Message.  
(c) Media (optional): jpg, gif, mp4 video, and mp3 formats are supported.  
(d) Call to action (optional).

For example, the user receives the inbox message on the mobile app stating "Your order has been accepted by the restaurant after placing an order. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6ee6624-app_inbox_simple_message.png",
        "Sample App Inbox Message",
        232
      ],
      "align": "center",
      "sizing": "sma% ",
      "border": true,
      "caption": "Inbox Notification on the Mobile App - Simple Message"
    }
  ]
}
[/block]


#### Carousel Message with Content

This is a multi-slide template where you can draft up to five slides containing images with content. The carousel in the user app displays in the form of right and left scrolls. This is a rich template that can be used in situations such as promoting a list of products or movies that will be released this weekend.  
You can also add a link for each carousel message to navigate the users to that particular page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc1b308-app_inbox_carousel-1.png",
        "Sample App Inbox Carousel with Content",
        222
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": " Inbox Notification on the Mobile App - Carousel Message with Content"
    }
  ]
}
[/block]


Along with the advertising images, you can add the related headline in the message content and use personalization in these messages.

#### Carousel Message without Content

This template is similar to the above template but without a title text and message. Carousel messages without content can be made attractive to grab the user's attention and convey the purpose of your campaign. You can add promotional campaign creatives about your products as an image without any text message. 

#### Message with Icon

This template is similar to the simple message with the extra ability to include an additional icon placeholder. You can add a single image in the given format along with any personalized or generic title and text that you would like to send to the users. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a9e5c2-message_with_icon.png",
        "Sample Message with Icon",
        245
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Inbox Editor

The message builder for Inbox allows you to create a rich message to engage your targeted audience. Enter the text and message for your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cfa89ec-Inbox_Editor.png",
        "Craft an App Inbox Message using the App Inbox Editor",
        1205
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Inbox Editor"
    }
  ]
}
[/block]


#### Call to Action

_Inbox_ enables various types of Call To Action (CTA) to cater to different use cases for the customer.

 Choose from one of the following five types (Optional):

- Click-on-message CTA: This opens a deep link when you click anywhere on the message (text, image, or both).
- Click-on-link CTA: You can add additional, colored links at the bottom of your message to attract the user's attention. 
- Copy to clipboard CTA: The user can copy text to their clipboard, such as discount codes for your products, and apply them at the time of checkout.
- Open URL CTA: The user can open deep links for iOS, Android, or Web.
- Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the  _Inbox_ button. This data is not visible to the user.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4b8c01e-Configuring_CTAs.png",
        "Define CTAs for App Inbox",
        681
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Configuring CTAs"
    }
  ]
}
[/block]


#### Message Tags

This is an optional setting. You can tag your inbox message with one or more comma-separated strings. These tags help you identify messages inside the user's inbox and classify messages into different tabs in your inbox. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19799ac-App_Inbox_editor_message_tags.png",
        "App Inbox Message Tags",
        678
      ],
      "align": "center",
      "border": true,
      "caption": "Define Message Tags"
    }
  ]
}
[/block]


> 📘 Using Message Tags
> 
> Message tags are an excellent way to engage your users contextually. For example, some of your app users might be interested in offers while others in news updates. You can have two separate tabs to categorize your inbox messages into those two buckets. Note that it is not compulsory to have tabs.
> 
> You can define the names of the inbox tabs during the configuration of  _Inbox_ with your app. The same names must be entered as tags. In case you do not specify any tag, the message qualifies for the default bucket i.e. _All_.

#### Custom Key-Value Pairs

If you have a custom inbox and want to configure the message within CleverTap, you can define the parameters specific to your app and usage using these key-value pairs. For example, you can send an inbox campaign that offers a 20% discount to your users who interact with the campaign. Now, if the user taps on the notification, they are directed to the discounts page that offers a 20% discount. The following is an image that displays defining custom key-value pairs from the dashboard:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d5da20-image.png",
        null,
        "Define Custom Key-Value Pairs"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Custom Key-Value Pairs"
    }
  ]
}
[/block]


> 📘 SDK Version
> 
> To access this feature, ensure that you upgrade to SDK version 5.2.0 or higher.

### Time to Live (TTL)

_Inbox_ campaigns are, by design, persisted in the user inbox for a number of days. You can configure the number of days (or hours) to keep the message in the user's inbox by setting the _time to live_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e83cced-Message_Time_to_Live_-_Inbox_Campaign.png",
        "Define Message Time To Live",
        710
      ],
      "align": "center",
      "border": true,
      "caption": "Define Message Time to Live"
    }
  ]
}
[/block]


The TTL can range from 1 day to 60 days. The default value for TTL is 2 days. You can define the TTL for a maximum of 60 days. The message on the user's device stays there for the specified TTL after which it is automatically removed. You can also have _Infinite TTL_, which means the message will never be deleted from the user's inbox. 

> 🚧 Choosing the Right TTL
> 
> - You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay in the user's inbox for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers). 
> - The TTL is considered based on campaign sent time.

> 📘 How a Message is Accounted For?
> 
> Each message stored on the CleverTap platform for  _Inbox_ campaign is accounted for as a user event.### Supported Media Types

The supported media types include:

| Media Type            | 16:9 Aspect Ratio | 1:1 Aspect Ratio | Max Size |
| :-------------------- | :---------------- | :--------------- | :------- |
| Image (jpg, png, gif) | Yes               | Yes              | 500 KB   |
| Video (mp4)           | Yes               | Yes              | 50 MB    |
| Audio (mp3)           | N/A               | N/A              | 5 MB     |

### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send a test notification to any CleverTap user profile you have marked as a _Test profile_  
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

- Single Message
- A/B Test 
- Split Delivery
- By User Property

### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration. You can test up to three message variants.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30be644-Split_Delivery_in_Inbox.png",
        "Split Delivery in App Inbox",
        992
      ],
      "align": "center",
      "border": true,
      "caption": "Split Delivery in Inbox"
    }
  ]
}
[/block]


#### Split Delivery to Past Behavior Segments

For campaigns sent to _Past Behavior Segments_ (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

- If you are testing three messages (e.g., Variant A, Variant B, Variant C).
- Your campaign reach is 2,000,000 users.
- You choose a test population of 15% of the campaign reach (300,000 users).

Then, we send:

- Variant A to 100,000 users.
- Variant B to 100,000 users.
- Variant C to 100,000 users.

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of click-throughs. We then automatically send the winning message to the remainder of your target audience which is 1,700,000 users in this example.

> 📘 Note
> 
> For A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, click **+ Variant** to add multiple variants based on a user property value. You can send up to 50 message variants to different users based on a user property. In the example below, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

## Define the Campaign Schedule

### Date and time

You can set up the _When_ to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

- On a specific date and time.
- On multiple specified dates and times.
- Recurring at a periodicity you set.

> 📘 Recurring Day
> 
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6b4561-Delivery_Preferences_-_Inbox.png",
        null,
        "Define Campaign Schedule"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Campaign Schedule - Past Behavior/Custom List Campaign"
    }
  ]
}
[/block]


External Trigger campaigns can be scheduled to run:

- Start date and time
- End date and time
- Set delay

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0881cf2-Delivery_Preferences_-_External_Trigger.png",
        "",
        "Delivery Preference - External Trigger Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Campaign Schedule - External Trigger Campaign"
    }
  ]
}
[/block]


### Delivery Preferences

You can apply global campaign limits to determine how many notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the _Don’t apply global campaign limits to this campaign_ checkbox.

You can also select the _Advanced_ checkbox to specify Do Not Disturb (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f90b21-image.png",
        null,
        "Message Delivery Preferences"
      ],
      "align": "center",
      "border": true,
      "caption": "Message Delivery Preferences"
    }
  ]
}
[/block]


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
        "Publish Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish App Inbox Campai"
    }
  ]
}
[/block]