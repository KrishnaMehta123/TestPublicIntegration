---
title: A/B & Multivariate Testing
excerpt: Understand how to use different message types and their contents.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

Optimizing messages and campaigns is a crucial activity for any app marketer. Clevertap offers three ways to optimize everything you deliver:

* A/B & multivariate testing.
* Split message delivery.
* Sending campaigns to an audience subset.

# A/B Testing

A/B testing lets you compare up to three different versions of a message for any campaign. You can try different copy, creatives, calls to action, or any combination of these to make sure you have designed the best message for each campaign. 

Pick the test audience size to run and we do the rest. We determine the winner based on the number of clicks. In the case of email, the winner is determined based on views. We then deliver the winning variant to the rest of your target audience.

<Image title="ab1.gif" alt={1280} align="center" border={true} src="https://files.readme.io/e5353df-ab1.gif">
  Results of A/B Testing
</Image>

For any campaign, you need the content and creatives for each message. When you create a push notification campaign, you have an option to add up to three variants of any message to test which one performs best.

You can determine the size of the test to run after adding the desired number of variants.

> 📘 Ideal Audience Size for A/B Testing
>
> * For reliable A/B testing, CleverTap recommends a minimum of **5000** users base to reduce randomness in variant assignment.
> * When the user base **exceeds 10,000 users**, variant distribution becomes substantially more stable. This minimizes deviations and provides more precise insights.
> * Testing with fewer than 5,000 users increases the likelihood of inconsistent distribution and skewed performance metrics.
> * If the user base is small, consider the following practices:
>   * Limit the number of variants.
>   * Extend the test duration.\
>     Use segment-based targeting.
>   * Avoid frequent, rapid re-tests.

## Campaigns Sent to Past Behavior Segments

For campaigns sent to past behavior segments (grouping of users based on their past actions), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

<Image title="Test the Campaigns sent to Past Behaviour Segments" alt={754} align="center" border={true} src="https://files.readme.io/f8d2724-A_b_Multivariate.png">
  Test the Campaigns Sent to Past Behaviour Segments
</Image>

For example:

* You are testing three messages (Variant A, Variant B, Variant C)
* Your Campaign Reach is 2,000,000 users
* You choose a Test Population of 15% of Campaign Reach (300,000 users)

Then, we send:

* Variant A to 100,000 users
* Variant B to 100,000 users
* Variant C to 100,000 users

After the 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of views. 

We then automatically send the winning message to the remainder of your target audience which in this example is 1,700,000 users.

The following is a sample report:

<Image title="Sample Campaign Reports of A/B Variant testing" alt={1440} align="center" border={true} src="https://files.readme.io/83d9d6c6492b51e24898735579cced277e851b6266510504fb5bed477fec9b7d-AB_Stats.png">
  Sample Campaign Reports
</Image>

## Campaigns Sent to Live User Segments

With campaigns sent to live user segments, campaign (triggered) messages are delivered immediately when a user’s activity matches the criteria that you have selected. 

### Example

In this scenario, you want to send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you must decide how many of the total messages to send for A/B testing before a winner is declared.

If you select 500 users as your test audience, we alternate delivery of Variant A and Variant B as users qualify for the campaign. After 500 total messages are sent (Variant A – 250 and Variant B – 250), we decide the winner based on the number of views and only continue with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small (25 users) you will get a statistically insignificant sample. 

If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner is be declared and each message variant is alternatively delivered for the duration of the campaign.

To clarify further, here is how this process works across different channels:

* **For mobile channels:** If the campaign starts at 7 PM and has a conversion window until 7:30 PM, then Variants A and B are sent alternately during the conversion window (7 PM to 7:30 PM). Once the conversion window ends, the winner variant is declared based on the conversion metrics. The winning variant is sent from 7:31 PM onwards for the remainder of the campaign.
* **For other channels:** If the campaign starts at 7 PM, the conversion time is 30 minutes, and a sample size of 1000 is selected, then Variants A and B are sent alternately until 1000 users are reached (for example, this is achieved by 7:15 PM). At 7:15 PM, we wait for the 30-minute conversion window to complete. By 7:45 PM, the winner variant is declared based on performance metrics such as conversions. The winner variant is sent for the rest of the campaign duration.

> 📘 Same Number of Views/Clicks
>
> * For Email and WhatsApp, if all variants receive the same number of views, then Variant A is declared the winner.
> * For the rest of the channels, if all variants receive the same number of clicks, then Variant A is declared the winner.

# Split Delivery

For some campaigns, you want to send multiple variants of a message to your entire target audience without selecting a winner. With split delivery, you choose what percentage of your target audience receives each variant and we deliver them accordingly.

<Image title="Results of Split Delivery tests." alt={1200} align="center" border={true} src="https://files.readme.io/7a1a774-ab5.png">
  Results of Split Delivery Test
</Image>

> 📘 Variant Consistency in Live Campaigns
>
> For Split Delivery or A/B tests, users are consistently shown the same variant upon repeated qualifications, with one notable exception. If the event triggering the campaign is sent via API using user identity (without device information), variant assignments become random each time the user qualifies.
>
> To ensure variant consistency, CleverTap recommends sending events via SDK or through the API using object ID (refer to the following table).
>
> | Event Source        | Variant Consistency |
> | :------------------ | :------------------ |
> | SDK                 | Consistent          |
> | API (object ID)     | Consistent          |
> | API (user identity) | Random              |
>
> **Example**
>
> * Consider a trigger campaign with the two variants: Variant A and Variant B. 
>   * **Scenario 1: Event triggered via SDK** 
>     * **Outcome**: User receives Variant A initially and consistently sees Variant A upon all subsequent qualifications.
>   * **Scenario 2: Event triggered via API using user identity** 
>     * **Outcome**: User receives a random variant on each qualification. For example, the user might first see Variant A, then Variant B in subsequent triggers, and again Variant A later, due to missing device information.

**How it works**

As with A/B testing, you can add up to three variants to a campaign message. With split delivery, you can decide what percentage of your audience receives each message variant. We deliver the messages in exactly this proportion for the duration of the campaign.

<Image title="Variant Distribution for Split Delivery" alt={731} align="center" width="smart" border={true} src="https://files.readme.io/981b1db-message_type_split_delivery.png">
  Variant Distribution for Split Delivery
</Image>

After the campaign is completed, navigate to the campaign stats to compare how each message performed.

# Deliver to a Subset of the Target Audience

Sometimes you want to send a message to only a subset of the qualifying audience (target reach) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A use case is a limited offer when you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the available number of coupon codes, you can simply limit the number of users who will receive the message to the available number of coupons. 

<Image title="Deliver Campaigns to subset of users." alt={406} align="center" border={true} src="https://files.readme.io/8f35a4d-ab7.png">
  Deliver Campaigns to Subset of Users
</Image>

Here is how it works:

In the campaign creation flow, when you are determining who to send your message to under the *Limits and Control Group* section, select the option to limit delivery of the messages to the number you want.

For triggered campaigns (based on live user segments), as users qualify, they receive the message until the total specified quantity is delivered, after which the campaign ends. For campaigns based on past behavior segments, we randomly select the users who receive the message.

The campaign limits can also be configured as follows: 

* Global campaign limit: Set up at the device level. 
  * When *Send to all devices* is selected, it limits the number of messages to be sent to all the active devices of each user every day (or as per the limits in settings). For instance, if the limit for the Mobile Push channel is set to 2 messages per day, and the user has 2 active devices with push tokens. When the push campaign is sent, it is delivered to all the user's active devices, resulting in a total message count of 2 in this scenario.
  * When *Send to last active device* is selected, limits the number of messages to be sent to each user for each day (or as per the limits in settings).

* Campaign run limit: Limits the number of users for the entire campaign or each run of a campaign for a fixed time or recurring campaign. In the case of live campaigns, each day is considered as each run.

* Safety check: Prevents sending out unwanted campaigns. A campaign does not run if the number of qualified users exceeds the safety limit. The campaign creator receives an email alert for further action. 

> 👍 Target Audience Example
>
> A customer has a budget for distributing 1,000 discount coupons but the qualified user count is 10,000. If you select the safety check, the campaign does not run and prevents the sender from spending over budget.

<Image title="Control Group and Targeting Cap" alt={513} align="center" width="smart" border={true} src="https://files.readme.io/8e9304f-Message_Type_Control_Group.png">
  Control Group and Targeting Cap
</Image>

# Email A/B Testing

CleverTap's email A/B testing feature lets you compare up to three different versions of an email to find the best-performing one. You decide the size of the test audience for the A/B test, we determine the winner based on the number of views, and then deliver the winning message to the rest of your target audience.

## Setup Steps

Creating an email campaign using the A/B testing feature follows a similar pattern to creating a normal email campaign. After choosing the segment to target and frequency of communication, you can run the campaign as an A/B test using the following steps.

1. Select *A/B Test* to set up the email A/B test.

<Image title="Create a message." alt={1343} align="center" width="100%" border={true} src="https://files.readme.io/6a99abc-5_Select_AB_Test.png">
  Create a Message
</Image>

2. On the next page, build two or three different variations of the email you want to send. You can modify the email template, content, subject line, and sender name. 

3. Click **Done** after you are finished building the email variations.

<Image title="Variant distribution of emails for A/B tests." alt={804} align="center" border={true} src="https://files.readme.io/056e715-Message_Type_Email_A_B_test.png">
  Variant Distribution of Emails
</Image>

> 📘 Winner Evaluation
>
> We determine the winner based on the number of views and then deliver the winning message to the rest of your target audience. 
>
> In the above image, we are sending the A/B test to a sample size of 10% who will receive either Variant A or B. In other words, 5% of the target segment will receive email Variant A and another 5% will receive email Variant B. We will wait for 45 minutes to evaluate the winner based on the number of views. The winner variant is then automatically sent to the remaining 90% of the target segment.
>
> If there is a tie between Variant A and B, we will send the email Variant A to the remaining 90% of the audience.

You are finished with setting up the A/B test portion of building your email campaign. Now, you can complete the rest of the steps similar to a normal campaign. 

6. Click **Publish Campaign** to finalize your campaign.

<Image title="Publish the Campaign" alt={1373} align="center" border={true} src="https://files.readme.io/21481dd-6_Summary.png">
  Publish the Campaign
</Image>

# Multi-variant Campaigns

Using the message by user property type, you can create multi-variant campaigns. You can send a campaign based on the selected user property. 

For example, if you have users segregated based on languages. You can send campaign content in different languages based on their user property. You can select the language as the user property for the multivariate campaign. This allows you to create multiple messages in the same campaign, each reaching out to users based on their language preference.

You can create up to 50 such variants in the same message. The default variant engage the users who have no value against the profile property.

<Image title="Create Multi-Variant Campaigns" alt={1345} align="center" border={true} src="https://files.readme.io/567f327-7_Multivariate_campaigns.png">
  Create Multi-Variant Campaigns
</Image>

You can also perform analysis and derive insights based on the variant of the notification sent. For analysis, you can filter the information based on the event property *Variant* for the notification-based events (Notification Sent, Notification Clicked, etc.) as shown in the following figures. You can download the list of users to whom a specific notification variant was sent, as well as save this query as a segment and use it for further action.

<Image title="Filtering Variant details on Events page." alt={1784} align="center" border={true} src="https://files.readme.io/a460a51-Filtering_Variant_information_on_Events_page.png">
  Filtering Variant Details on Event Page
</Image>

<Image title="Filtering Variants on Funnels page" alt={1778} align="center" border={true} src="https://files.readme.io/4a8bae7-Filtering_Variants_on_Funnels_page.png">
  Filtering Variants on Funnels Page
</Image>
