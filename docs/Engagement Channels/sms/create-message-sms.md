---
title: Create Message
excerpt: Learn how to create an SMS campaign using the CleverTap dashboard.
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

Follow the steps below to create a new SMS campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **SMS**. 

<Image title="Click +Campaign and Select SMS" alt={2796} align="center" border={true} src="https://files.readme.io/8f48e3b4e1aac8482a265e15abe0b34cb640abc7ddf63b7399d18c6b6c14cbc2-Select_SMS_Campaign.png">
  Create SMS Campaign
</Image>

The *Campaign* page displays.

<Image title="View Campaign Page Steps" alt={1107} align="center" width="80%" border={true} src="https://files.readme.io/3afb28a-SMS_Editor_main.png">
  View Campaign Page
</Image>

Define all the sections and publish the campaign. 

## Start Campaign Setup

The *Start here* section displays the setup information.\
This section has the following parts:

* **Qualification criteria**: Here, you need to define the criteria for your target audience. You can deliver the SMS based on *Past behavior/Custom list* or *Live behavior*.
* **SMS Service Provider**:  Here, you need to select your SMS service provider or a provider group.
* **Goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign performance. This selection is optional. Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Set a Goal and Select Conversion Tracking Rules" alt={919} align="center" border={true} src="https://files.readme.io/6001c3f-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your push campaign. You can target your SMS campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the *segment* list. 

<Image title="Define the Target Segment and Click Done" alt={961} align="center" border={true} src="https://files.readme.io/074ff4c-SMS_Who.png">
  Define Target Segment
</Image>

You can also create the target based on past user behavior and user properties or live (ongoing) user behavior. the latter is useful to send out real-time, triggered SMS campaigns.

> 🚧 Delay > 24 Hours
>
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live *Inaction within time* campaign that targets users when they add a product to their cart but do not finish transacting within 10 minutes.

### Deliver Action Based SMS

You can trigger an SMS based on an action. For example, you can send an SMS with a promo code for the next purchase can be sent to a set of customers who have just completed a purchase. This makes notifications more contextual and increases conversion.

### Deliver SMS based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past by sending them attractive discount vouchers or offers. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. For example, you can send an SMS to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 

<Image title="Filter the Target Segment by User Properties" alt={2376} align="center" border={true} src="https://files.readme.io/d8f91b7-User_properties_whatsapp.png">
  Filter Segments
</Image>

To know more about what segments can be used, see [Segments](doc:segmentation).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image title="Control Group and Target Cap" alt="Set Control Group" align="center" src="https://files.readme.io/474530b-Control_Group_and_Target_Cap.png">
  Set Control Group
</Image>

### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to precisely the number of coupons that you want to distribute.

> 📘 Campaign Limit
>
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

<Image title="Subset" alt={406} align="center" border={true} src="https://files.readme.io/3aa9241-subset_image.png">
  Target Reach
</Image>

## Define the SMS Content

Now, you can set up the *What* section in the campaign content with two different options:

* Single Message
* A/B Test
* Split Delivery
* By User Property

Click **Go To Editor** to create your message. 

## Message Editor

<Image alt="Define-What" align="center" border={true} src="https://files.readme.io/c867bf1-image.png">
  Define-What
</Image>

The *Create SMS Notification* window displays. 

<Image alt="Create Message" align="center" border={true} src="https://files.readme.io/9e5877265e518d82bfec0ea9b7bbb320b67ec9d81dcca6064462a45617043f1e-Create_Message_SMS.png">
  Create Message
</Image>

For users targeted in India, you might be required to set up template IDs. For more information, refer to [SMS Regulations](https://docs.clevertap.com/docs/regulation-impact#future-campaigns).

> ❗️ Template IDs
>
> A template ID is required for the SMS campaigns targeted to Indian mobile numbers and having MSG-91 as the service provider. A template ID may or may not be required for other service providers. We recommend checking with your service provider.

This section of the campaign creation flow depends on the SMS provider selected for the campaign.

### Out-of-the-box Providers

All SMS service providers are listed on the *Personalization Setup* page (including Msg91, Nexmo, Twilio, Exotel, and Netcore). The connection with these providers is configured by default, and the mandatory input required for these providers is the message. This is only applicable for SMS campaigns in India for template ID.

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test SMS.

Click **Preview & Test** from the message editor to test a message.

## Message Types

You can create the following types of messages:

* Single Message
* By User Property
* A/B Test 
* Split Delivery

### Single Message

We send the same message to all users who qualify as your target audience in this campaign. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Test

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign's duration.

#### Split Delivery to Past Behavior Segments

For campaigns sent to *Past Behavior Segments* (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

* If you are testing three messages (e.g., Variant A, Variant B, Variant C).
* Your campaign reach is 2,000,000 users.
* You choose a test population of 15% of the campaign reach (300,000 users).

Then, we send:

* Variant A to 100,000 users.
* Variant B to 100,000 users.
* Variant C to 100,000 users.

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of clicks. We then automatically send the winning message to the remainder of your target audience, which is 1,700,000 users in this example.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches your selected criteria. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After all the messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared, and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

Suppose you want to send different message variants to your target audience based on the user properties. In that case, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

<Image alt="Select Message Type" align="center" border={true} src="https://files.readme.io/df88567-image.png">
  Select Message Type
</Image>

You can use the **+Variant** button to add multiple variants based on a user property value. In this example, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum). 

<Image title="Create Message and Its Content" alt={3476} align="center" border={true} src="https://files.readme.io/087cf49-SMS_What_User_Property_variant.png">
  Create Message Content
</Image>

## Define the Campaign Schedule

You can schedule the campaign's start and end duration using the options below:

Past behavior campaigns can be scheduled to run:

* On a specific date and time.
* On multiple specified dates and times.
* Recurring at a periodicity you set.

Live campaigns can be set up for a specific event:

* In response to a user event.
* User event/inaction combination (e.g., abandoned cart scenario).
* Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

<Image title="Select Message Date and Time to Send" alt={978} align="center" border={true} src="https://files.readme.io/8ca1af6-Push_notification_editor_when.png">
  Define - When
</Image>

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

### Delivery preferences

 To cap the number of messages delivered every 5 minutes in a campaign, check the *Global throttle limits* checkbox.

You can set the *Do Not Disturb* (DND) hours during which SMS from this campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Set Up the Different SMS Delivery Preferences" alt={838} align="center" border={true} src="https://files.readme.io/be4fee7-SMS_delivery_preferences.png">
  Set Up Delivery Preferences
</Image>

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="CLick Publish Campaign to Publish it" alt={1193} align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish
</Image>

# Click Tracking

This feature helps users track the clicks on each URL included in their SMS campaign. These stats are available under the *Campaigns* > *Stats* page. In case of multiple URLs in the same message, the click distribution data is also available under the split of clicks tab under the campaign stats page. For more information, refer to the [Split of Clicks](doc:sms-stats#split-of-clicks) section.

> 📘 TRAI Mandate
>
> As per the latest TRAI directive, only whitelisted URLs are allowed in SMS messages sent to Indian users. To continue using the SMS Click Tracking feature, whitelist CleverTap's tracking domains on your DLT platform. Failure to do so may lead to delivery errors.

## Link Shortening

This feature allows you to shorten the URLs present in your message. When a link is present in your message, the *Short URL* section displays below the *Message* section. This section shows the list of all the URLs present in your message. You can select the URLs you want to shorten if your message body includes one or more URLs.

> 📘 URL Shortening TRAI Regulation

<Image alt="Shorten URLs Included in the Message" align="center" border={true} src="https://files.readme.io/5c3dc07-Shorten_URLs_in_the_Message.gif">
  Shorten URLs Included in the Message
</Image>

In cases where the message body is empty and the providers use only template IDs, the URLs are not shortened and are sent as is.

> 📘 Character Consumption
>
> Each shortened URL may consume between 14-20 characters.

> 📘 Number of URLs to Shorten
>
> You can shorten a maximum of **five URLs** in one message. In the case of Message by user property, you can shorten a maximum of **five URLs**  per message variant.

## Domains

The URLs in the message are shortened based on the region of your account. To identify the region of your account and the shortened URL domain for your account, refer to the following table:

|                                                                                                    | Domain | Region            | Sample Short URL |
| :------------------------------------------------------------------------------------------------- | :----- | :---------------- | :--------------- |
| [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/) | ct1.io | EU                | ct1.io/25AlJz    |
| [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/) | ct3.io | IN                | ct3.io/52KlAz    |
| [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/) | ct4.io | SG                | ct4.io/25ZlAz    |
| [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/) | ct5.io | US                | ct5.io/52ZlKa    |
| [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html) | ct8.io | Middle East (UAE) | ct8.io/25ZaJz    |
| [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html) | ct9.io | Indonesia         | ct9.io/52KJz     |

### Branded Domain

CleverTap provides the capability to use your own branded domain for link shortening and click tracking in SMS campaigns. This feature allows you to replace the default CleverTap domains such as `ct3.io` with a custom domain that reflects your brand, enhancing brand recognition and trust among your users. 

<Image alt="System Domain Creation" align="center" border={true} src="https://files.readme.io/9bc74aeb0814633f881aa3b1ddaadca049e395bb61df7f9f55379bad0c76a63c-image.png">
  System Domain Creation
</Image>

To set up a branded domain, you need to configure DNS settings and SSL certificates to ensure secure and reliable link tracking. Detailed instructions on setting up and managing your branded domain can be found in the [Branded Domain documentation](doc:branded-domain).

> 📘 TRAI Regulation
>
> If you are sending SMS messages to users in India, ensure that your branded domain is whitelisted on your Distributed Ledger Technology (DLT) platform, in compliance with the Telecom Regulatory Authority of India (TRAI) regulations. Failure to do so may result in message delivery failures.

# FAQs

### Can we shorten custom links such as Appsflyer OneLinks and Branch Links?

Ans. Shortening Appsflyer OneLinks and Branch links is not recommended, as this may break the app-opening functionality. For more information, refer to the following articles:

* [Appsflyer OneLinks](https://support.appsflyer.com/hc/en-us/articles/360014821438-OneLink-troubleshooting-and-FAQ?query=onelink%20short%20url#can-i-wrap-and-shorten-onelink-custom-links)
* [Branch](https://help.branch.io/faq/docs/deep-links-do-not-open-the-app)

### Why am I experiencing 404 when I open shortened links?

Ans. The shortened URLs from the SMS campaign expire after seven days from the date the campaign is sent. If the user opens these links after the expiration date, they are redirected to a 404 page.
