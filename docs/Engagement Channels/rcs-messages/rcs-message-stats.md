---
title: RCS Message Stats
excerpt: Understand all the statistical information available for your RCS campaign
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

Campaign stats for the RCS channel in CleverTap provide insights into the performance of your engagement campaigns. When you create an RCS campaign on the CleverTap dashboard, messaging API requests are generated for each qualified user based on your campaign setup. These requests are then sent to the configured RCS provider, following the agreed API specifications. If the provider accepts the request successfully, CleverTap marks the message as Sent.

Once submitted, the provider is responsible for delivering the message to the user via the RCS infrastructure.

> 📘 Delivery to End User
> 
> The RCS provider manages the final message delivery process to the user. CleverTap does not directly influence this delivery

CleverTap captures Delivered, Viewed, Clicked, events separately for SMS and RCS, depending on the channel used to deliver the message. Additionally, we log error events to provide a complete view of how your users are engaging with the campaign.

These events are typically shared by the provider via callback URLs based on the agreed callback format. CleverTap uses these callbacks to register when a message is delivered (SMS or RCS), viewed, or clicked, and to log any errors encountered during message delivery.

Please note that any misconfiguration or technical issue in the callback setup may result in discrepancies in your campaign stats. For accurate reporting, it is essential to ensure your callback URLs are properly configured and functioning as expected.

## View RCS Campaign Stats

To view the statistics of your campaign, select the campaign from the campaign list page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94024e3f56a5b9f12ad0866deec3cf24081b6d1d101abc8ff6b246f68a4fc685-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


## Campaign Filters

Search for a campaign by applying the required filters.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03aecae4bd84fca551914a265ee19f9e2f5f67a9b737d85fa8dab93925b5116d-image.png",
        null,
        "RCS Campaign Filters"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Campaign Filters"
    }
  ]
}
[/block]


## Understanding RCS Campaign Stats

CleverTap provides detailed delivery and engagement metrics for RCS campaigns, helping you track performance across both RCS and SMS (in case fallback is enabled). Here’s what each metric means:

## Sent

This metric indicates the total number of message requests successfully submitted by CleverTap to the configured RCS provider. If the provider accepts the API request, the message is marked as Sent. It does not guarantee delivery to the end user but confirms that the message passed the initial delivery pipeline.

## Delivered

Tracks the number of messages successfully delivered to end users. This is bifurcated by channel:

**Via RCS**: Shows how many users received the message over the RCS channel. This is based on delivery receipts (DLRs) sent by the provider when the message reaches the user’s device.

**Via SMS**: Available only if SMS fallback is configured for the RCS campaign. This shows how many users received the fallback SMS message in case RCS delivery was not possible (e.g., due to device or carrier limitations).

## Viewed

Indicates the number of messages that were opened or seen by the user.

**Via RCS**:  Captured when the RCS message is rendered on the user’s device. This is based on read receipts sent by the provider.

**Via SMS**: Marked as N/A. SMS does not support “viewed” tracking due to technical limitations of the SMS protocol.

## Clicked

Represents the number of users who clicked on any links or action buttons within the message.

**Via RCS**: Captured when a user interacts with clickable elements in the RCS message.

**Via SMS**: Available if SMS fallback is used and if the SMS contains a trackable link. CleverTap will record clicks using standard URL click tracking methods.

## Converted Users

This metric shows the number of users who completed the defined conversion goal after receiving your RCS campaign. It helps you measure the direct impact of your campaign on user behavior.

## Control Group

Control groups consist of users who were intentionally excluded from the RCS campaign. They help measure the true effectiveness of your campaign by acting as a benchmark group.

For more details, refer to the [Control Groups documentation](https://docs.clevertap.com/docs/control-groups).

## Message Trend

This section displays trends for your RCS campaign messages—tracking metrics like Sent, Delivered, and Viewed across daily, weekly, and monthly intervals. It helps identify patterns and assess performance over time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a7dfaff1ad5a5a2e7324f74f2e5911d60e259f217588ee01a5e9fb93de6e6fb7-image.png",
        null,
        "RCS Message Trend"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Message Trend"
    }
  ]
}
[/block]


## Conversion Performance

This shows a side-by-side comparison of conversion rates between the Target Group (users who received the campaign) and the Control Group (users who were excluded). Use this to evaluate how effective your campaign was in driving conversions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4497ca366600f39e230be334e1df5360c42d56f0b9ad93903578a13986bb582-26eecaa-small-whatsapp_graph_conversion_performance.png",
        null,
        "Conversion Performance"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Conversion Performance"
    }
  ]
}
[/block]


For A/B Test, Split Delivery, and User Property-based campaigns, you can view performance breakdowns for each variant under the User Conversion Funnel.

## Revenue Performance

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a1d97033abe618f2e5161921f1ccd8b3d6412f249f5ca02f559499bf0edcc69-12b9490-revenue_performance.png",
        null,
        "RCS Revenue Performance"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "RCS Revenue Performance"
    }
  ]
}
[/block]


Tracks the overall revenue impact of your campaign, including both the total uplift and incremental revenue generated. This helps quantify the business value of your RCS engagement efforts.

# Users Conversion Funnel

The conversion funnel visualizes the journey of users through key engagement stages in an RCS campaign—Sent, Delivered, Viewed, and Converted. This provides insight into drop-offs and helps optimize future campaigns.

You can toggle off Delivered and Viewed stages to isolate and focus on conversion performance specifically.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/103ccfea4cec5a5c83030f9603fe1587fb6939e211de55ee300b078b74b82ba7-583e4e2-funnel_conversion_whatsapp_stats.png",
        null,
        "RCS Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "RCS Users Conversion Funnel"
    }
  ]
}
[/block]


> 📘 Key Points to Remember
> 
> Conversion numbers for All Variants may sometimes be lower than the sum of individual variant conversions. This can occur because:
> 
> **For Live Campaigns**, a single user might receive different variants on different devices or app installs, identified by separate GUIDs. The same user may be counted under multiple variants but only once in the combined view.
> 
> **For Recurring Campaigns**, users may qualify multiple times under different message copies due to changes in their attributes (e.g., plan upgrades). In such cases, conversions may be recorded separately for each variant but counted only once in the overall tally.

## Split Of Clicks

CleverTap tracks clicks on all individual links included in your RCS message. This helps you understand user preferences and engagement for different call-to-actions (CTAs).

For example, if your campaign includes links to "Watch Trailer," "Book Tickets," and "Read Reviews," the Split of Clicks shows how many users engaged with each link. These insights can guide you in optimizing your future messaging strategies.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a4aed4f6401e206a8b1470efbda4cd7bcc125b31c32c944b63e523d9082a3c46-8dc04dc-Email_Stats_Split_Clicks.png",
        null,
        "Split of Clicks"
      ],
      "align": "center",
      "border": true,
      "caption": "Split of Clicks"
    }
  ]
}
[/block]


## User Details of Clicks

You can view the list of users who clicked on any links in your RCS campaign by selecting View details of users who clicked in the Split of Clicks section. This redirects you to the Events page, where you can explore individual user details under the People tab.