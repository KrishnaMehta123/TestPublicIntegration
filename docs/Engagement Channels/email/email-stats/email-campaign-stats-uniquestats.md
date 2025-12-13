---
title: Email Campaign Stats
excerpt: Measure the performance of your Email campaign.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Once the campaign is published, you can view the detailed campaign stats under the _All Campaigns_ page. The _Stats_ tab displays the overall conversion performance and errors.

# View Email Campaign Stats

CleverTap provides the following key event-based metrics to help you monitor your campaign  effectiveness:

- _Notification Sent_: Raised when the email campaign is sent to the ESP.
- _Notification Viewed_: Raised when the user opens the email campaign.
- _Notification Clicked_: Raised when the user clicks on the email campaign.

You can view its stats by navigating to _Campaigns_ from the CleverTap dashboard. To do so:

1. Click _Campaigns_ from the dashboard. The _All Campaigns_ page opens.
2. Select the email campaign you want to view the stats for. You can also filter campaigns using the **Filter** button (see figure below).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ef8ad422137f9919071243c4ecfcfaaa803bea361cf851096c76eb82c5f44a6-11.png",
        "Filter Email Campaign from All Campaigns",
        "Filter Email Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Email Campaigns"
    }
  ]
}
[/block]


3. Click the campaign to open it. The _Stats_ tab displays the following campaign stats: 
   - [Overall Campaign Performance](doc:email-campaign-stats-uniquestats#overall-campaign-performance)
   - [Variant Performance](doc:email-campaign-stats-uniquestats#variant-comparison)
   - [Message Trend](doc:email-campaign-stats-uniquestats#message-trend)
   - [Conversion Performance](doc:email-campaign-stats-uniquestats#conversion-performance)
   - [User Conversion Funnel](doc:email-campaign-stats-uniquestats#users-conversion-funnel)
   - [Split of Clicks](doc:email-campaign-stats-uniquestats#split-of-clicks)
   - [Errors](doc:email-campaign-stats-uniquestats#errors)

## Overall Campaign Performance

This section displays a high-level overview of the entire email campaign performance. Each card displays the **Total** and **Unique** count and percentage for key performance indicators of your email campaign, providing a comprehensive view of engagement, and conversions across all recipients (refer to the following image): 

> 📘 Unique Metrics
> 
> Unique Metrics are currently in Private Beta. To gain access, contact your Customer Success Manager.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/07d9524a78cfa43f533c7055411a9a8e35d235934616db626ab405fc432fa251-image_52.png",
        "",
        "Overall Campaign Performance"
      ],
      "align": "center",
      "border": true,
      "caption": "Overall Campaign Performance"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Metric",
    "h-1": "Total",
    "h-2": "Unique",
    "0-0": "Sent",
    "0-1": "Displays the total number of emails sent, excluding emails sent to CC and BCC recipients. CC and BCC feature are currently in Private Beta.",
    "0-2": "Displays the total number of emails sent to unique recipients, excluding CC and BCC recipients. CC and BCC feature are currently in Private Beta.",
    "1-0": "Delivered",
    "1-1": "Displays the total emails delivered to the recipient inbox. It also displays the delivery rate, calculated as `(Total Delivered / Total Sent) * 100`. <br>Note: It is currently in Private Beta for Infobip (in the case of Advanced Email add-on) and Sendgrid email providers. To gain access, contact your Customer Success Manager, and for more details, refer to [Email Delivered Stats](doc:email-campaign-stats-delivered) . </br>",
    "1-2": "Displays the emails successfully delivered to unique recipient inboxes. Percentage calculated as `(Unique Delivered / Unique Sent) * 100`. <br> Note: It is currently in Private Beta for Infobip (in the case of Advanced Email add-on) and Sendgrid email providers. To gain access, contact your Customer Success Manager, and for more details, refer to [Email Delivered Stats](doc:email-campaign-stats-delivered) . </br>",
    "2-0": "Viewed",
    "2-1": "<li>Displays the open percentage of your email message, calculated as `(Total Viewed / Total Sent) * 100`. Includes views from CC/BCC recipients.</li><li>AMP Viewed: Displays the percentage of total emails rendered as [AMP emails](https://docs.clevertap.com/docs/ampforemail).</li><li> HTML Viewed: Displays the percentage of total emails rendered as HTML.</li>",
    "2-2": "<li>Displays the percentage and count of unique recipients who opened the email, calculated as `(Unique Viewed / Unique Sent) * 100`.</li><li>AMP for Email Viewed: Displayed for AMP Email campaigns. Displays the percentage of emails opened as [AMP emails](https://docs.clevertap.com/docs/ampforemail).</li><li>HTML Viewed: Displays the percentage of emails opened as HTML.</li>",
    "3-0": "Clicked",
    "3-1": "<li>Displays the percentage of clicks from the total messages sent, calculated as `(Total Clicks / Total Sent) * 100`. Includes clicks from CC/BCC recipients.</li><li> AMP Clicks: Displays the percentage of clicks on emails rendered as AMP. </li><li>HTML Clicks: Displays the percentage of clicks on emails rendered as HTML.</li>",
    "3-2": "<li>Displays the percentage and count of unique recipients who clicked on the email, calculated as `(Unique Clicks / Unique Sent) * 100`.</li><li>AMP for Email Clicks: Displayed for AMP Email campaigns. Displays the percentage of clicks on emails rendered as AMP.</li><li>HTML Clicks: Displays the percentage of clicks on emails rendered as HTML.</li>",
    "4-0": "CTR",
    "4-1": "Denotes the Click Through Rate of the campaign, calculated as `(Total Clicked / Total Viewed) * 100`.",
    "4-2": "Displays the unique Click through Rate of the campaign, calculated as `(Unique Clicks / Unique Viewed) * 100`.",
    "5-0": "Converted Users",
    "5-1": "Displays the percentage of total users who performed the conversion event (for example, Product Purchased) and the number of users who converted.",
    "5-2": "Displays the percentage of unique recipients who performed the conversion event (for example, Product Purchased) and the number of unique conversions."
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


This section also displays the following stats:

- _Errors_: Displays the number of errors for the campaign. These can be technical errors, such as email provider errors, or non-technical errors, such as message frequency exceeded. 
- _Control Group_: Displays the number of users to whom the campaign was not sent.
- _Global Unsubscribes_: Displays the total number of unsubscriptions. The unsubscription is attributed to the primary recipients who qualify for the campaign only if you use the `unsubscribe(isReEncode)` method to [unsubscribe from an email campaign](doc:handling-unsubscribes).
- CC (Carbon Copy) and BCC (Blind Carbon Copy) are used to send copies of emails to additional recipients. CC recipients can see all other recipients, while BCC recipients are hidden from each other and from other recipients. Note: The CC/BCC feature is currently in Private Beta. To gain access, contact your Customer Success Manager and for more details, refer to [Sender Details](doc:create-message-private-beta#sender-details).

> 📘 Note
> 
> Tracking delivery related errors such as Unsubscribes, Bounces, and Report as Spam are not available for CC/BCC recipients.

## Message Trend

Click **Message Trend** to view the the performance trends of your campaign over time. This typically visualizes key metrics such as the number of emails Sent, Viewed, or Clicked across a specified time frame.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dfbbdb769c12d042cfd8f82a8d39c78e6dcc69e763db08f04ad022682443b8d4-27a73a8-Email_Stats_Message_Trend_1.png",
        "",
        "Message Trend"
      ],
      "align": "center",
      "border": true,
      "caption": "Message Trend"
    }
  ]
}
[/block]


## Variant Comparison

This section provides detailed performance insights for each variant in multivariant campaigns, such as A/B Tests, Split Delivery, or Messages based on User Properties. Variant Performance Trend is not available for Sent in the Unique tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2cdb2056bf7930744e8264e2f266208ff74c583e259b3c1960843406a227b065-Variant_Comparison.png",
        "",
        "Variant Comparison"
      ],
      "align": "center",
      "border": true,
      "caption": "Variant Comparison"
    }
  ]
}
[/block]


You can analyze the _Total_ or _Unique_ stats for the following metrics: _Sent_, _Viewed_, or _Clicked_. The graph illustrates trends for the selected metric over the selected time period. 

The table below the graph provides a breakdown of the following metrics for each variant: Sent, Viewed, and Clicked.

## Conversion Performance

The Conversion Performance section is divided into two key insights: Conversion Performance and Revenue Performance. These metrics help track user actions and measure the impact of your campaigns on conversions and revenue.

Click _Conversion Performance_ to view Conversion performance, Revenue performance, and Users' conversion funnel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/32d1f59-Email_stats_conversion_performance.png",
        "View Conversion Stas of Email Campaign",
        2726
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Performance"
    }
  ]
}
[/block]


You can view stats for each variant under the User conversion funnel for A/B Test, Split Delivery, and Message on User Property campaigns.

**Conversion Performance**

The conversion performance section shows the conversion boost achieved from your campaign. You can compare your campaign conversions with the control group conversions to see the impact of your campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7bf34ea-Email_Stats_Conversion_Conversion_hero.png",
        "View Conversion Performance Stats of Email Campaign",
        1310
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Performance Stats"
    }
  ]
}
[/block]


**Revenue Performance**

The _Revenue Performance_ section shows the revenue boost achieved from your campaign. The following information is displayed in this section:

- _Incremental revenue due to this campaign_: Indicates the additional income directly attributed to a specific campaign. It is calculated as:  
  [(ARPU of Target Group – ARPU of Control Group) x Number of Users to whom the campaign was sent], where ARPU is calculated as: (Revenue generated / Number of users to whom the campaign was sent)
- _Boost in revenue due to this campaign_: Indicates the percentage increase in revenue achieved as a result of running the campaign compared (revenue generated from Target Group) to the baseline revenue that would have been generated without it (revenue generated from Control Group). It is calculated as:  
  {\[(Target Group ARPU – Control Group ARPU) / Control Group ARPU] x 100}
- _Target Group Revenue_: Indicates the total revenue generated by users who were targeted by the campaign.
- _Control Group Revenue_: Indicates the total revenue generated by users who were not targeted by the campaign (control group).

  [block:image]{"images":[{"image":["https://files.readme.io/07478a68a9d980cffaae04f57fbe73aa4ee73c6fc627762d07185a54379a6c2f-revenue_performance.png","","Revenue Performance"],"align":"center","sizing":"75% ","border":true,"caption":"Revenue Performance"}]}[/block]

## Users Conversion Funnel

Shows the conversion funnel, that is, _Sent_ > _Viewed_ > _Clicked_ > _Converted_. This helps you understand the drop-offs at each step more effectively.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e1b1ae-Email_Stats_Conversion_Performance_with_Viewed.png",
        "View Users Conversion Funnel of Email Campaign",
        2592
      ],
      "align": "center",
      "border": true,
      "caption": "Users' Conversion Funnel"
    }
  ]
}
[/block]


You can view stats for each variant under the User conversion funnel for A/B test, Split delivery, and Message on user property campaigns. 

Based on your tracking requirement, you can select to hide the _Viewed_ step. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4954e5-Email_Stats_Conversion_Performance_No_Viewed.png",
        "Hide Viewed Funnel of Users Conversion",
        2698
      ],
      "align": "center",
      "border": true,
      "caption": "Hide Viewed Funnel"
    }
  ]
}
[/block]


> 📘 Key Points to Remember
> 
> The Conversion Performance number for _All Variants_ may be equal to or less than the combined Conversion Performance number for each individual variant. For example, if the Conversion Performance number for All Variants is 10500, with Variant A at 5575 and Variant B at 5053, the total for Variants A and B combined is 10628, exceeding the total for _All Variants_.
> 
> This scenario can occur due to the following reasons:
> 
> - For Live campaigns, different variants are delivered to various devices, identified by different GUIDs for the same user. Consequently, the Conversion Performance number for All Variants might not match the sum of the Conversion Performance numbers for each variant. For instance, a user may receive Variant A before uninstalling the app and then receive Variant B after reinstalling it until their identity is established.
> - For Recurring campaigns (user property campaigns), the user can qualify more than once when and receive different message copy each time. For example, the user upgrades to a new plan. In this case, the message copy received by the user before and after upgrading the _Membership type_ can be different.
> 
> In both the cases, the same user is counted twice, once for Variant A and once for Variant B. However, when calculating the Conversion Performance number for _All Variants_, each user is counted only once.

## Split of Clicks

You can track the distribution of clicks on each link in your email campaign.  For example, you want to send an email promotion for an upcoming movie on your video streaming app. You can create an email campaign and add links for reviews, promotions, movie merchandise, and so on, and then send the campaign.  We will record the clicks for each link in the email, and you can see them on the Campaign Stats page. 

> 📘 Click Heat Map
> 
> Click Heat Map lets you see exactly where users are clicking within your emails through a visual, color-coded overlay. Use these insights to optimize content placement, refine CTAs, and improve campaign performance across teams. It is currently in Private Beta. To gain access, contact your Customer Success Manager. For more information, refer to [Link Clicks](doc:email-campaign-stats-heatmap#link-clicks).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8dc04dc-Email_Stats_Split_Clicks.png",
        "View Split of Clicks for Clicked Links",
        2708
      ],
      "align": "center",
      "border": true,
      "caption": "Split of Clicks"
    }
  ]
}
[/block]


### User Details of Clicks

You can view the details of users who clicked on your email campaign using the _View details of users who clicked_ link present on the _Split of Clicks_ tab. You are navigated to the _Events_ page. Select the _People_ tab to view user details. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d55d148-Email_stats_notification_clicked.png",
        "View Event Analysis for Notification Clicked",
        1049
      ],
      "align": "center",
      "border": true,
      "caption": "Event Analysis for Notification Clicked"
    }
  ]
}
[/block]


## Errors

You can view campaign errors from the _Stats_ > _Errors_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/579eaeac43e3f43aab26ed06c0762a092c6ab44a783beb1e81c23538f3e8372c-Email_-_Errors.png",
        "View Email Campaign Errors",
        2702
      ],
      "align": "center",
      "border": true,
      "caption": "Email Campaign Errors"
    }
  ]
}
[/block]


### Delivery Errors

Delivery errors occur when the ESP reports a failure in delivering the email to the recipient's inbox. These errors typically happen after the email has been successfully dispatched to the ESP but cannot be delivered to the end user. Common reasons include:

- Soft Bounce 
- Hard Bounce
- Dropped

#### Soft Bounce

A soft bounce indicates that mail bounced due to one of the following reasons even though the email address was valid and the email message reached the recipient's mail server:

- The mailbox was full (the user has exceeded their storage quota)
- The recipient server was down
- The message was rejected as spam
- The message was too large for the recipient's inbox.  
  CleverTap campaign reports include soft bounces and do not mark the users as unsubscribed.

#### Hard Bounce

A hard bounce indicated that the email was returned to the sender and was completely undeliverable. However, common reasons it got rejected include:

- The email address does not exist
- The recipient's email server has rejected the email permanently

CleverTap campaign reports include hard bounces and mark the users as unsubscribed.

> 📘 Deferred emails
> 
> The time for retrying a deferred email and the number of retries depend on the ESP. For SendGrid, the retry period is set to 72 hours.

# View Detailed Engagement Stats

You can also view the user details for notifications _sent_, _viewed_, _clicked_, and _bounced_ from the _Analytics_ page of the CleverTap dashboard. For more information about viewing such stats, refer to [Analyze an Event ](doc:events-analytics#analyze-an-event). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46340b1-Events.png",
        "View Event Analysis for Notification Viewed",
        2658
      ],
      "align": "center",
      "border": true,
      "caption": "Event Analysis for Notification Viewed"
    }
  ]
}
[/block]


# FAQ

### Why are my Viewed and Clicked numbers unusually high?

The _Viewed_ and _Clicked_ numbers in your email reports may be inflated due to spam filters, email forwards, or bot activity that automatically opens or clicks links. These interactions are not always from real users and can distort campaign performance data. To minimize false clicks, analyze engagement patterns and use CleverTap tracking tools. For more details, refer to [Unusually High Email Opens and Clicks](doc:troubleshooting-open-click-tracking).