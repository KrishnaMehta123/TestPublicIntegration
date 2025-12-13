---
title: Email Campaign Stats
excerpt: >-
  Measure the performance of your Email campaign with the help of email campaign
  stats.
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

- Notification Sent: Raised when the email campaign is sent to the Email Service Provider (ESP).
- _Notification Delivered_: Raised when the email campaign is delivered to the end user from the ESP.

> 📘 Private Beta
> 
> Notification Delivered is currently released in Private Beta for Infobip (in the case of Advanced Email add-on) Sendgrid, and Genric (HTTP and SMTP) email providers . Contact your Account Manager for access.

- _Notification Viewed_: Raised when the user opens the email campaign.
- _Notification Clicked_: Raised when the user clicks on the links in the email campaign.

You can view campaign stats for Email by navigating to _Campaigns_ from the CleverTap dashboard. To do so:

1. Click _Campaigns_ from the dashboard. The _All Campaigns_ page opens.
2. Select the email campaign for which you want to view the stats. You can filter campaigns using the **Filter** button (refer to the following image).

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
   - [Overall Campaign Performance](doc:email-campaign-stats-delivered#overall-campaign-performance)
   - [Variant Comparison](doc:email-campaign-stats-delivered#variant-comparison)
   - [Message Trend](doc:email-campaign-stats-delivered#message-trend)
   - [Conversion Performance](doc:email-campaign-stats-delivered#conversion-performance-overview)
   - [User Conversion Funnel](doc:email-campaign-stats-delivered#users-conversion-funnel)
   - [Split of Clicks](doc:email-campaign-stats-delivered#split-of-clicks)
   - [Errors](doc:email-campaign-stats-delivered#errors)

## Overall Campaign Performance

This section displays a high-level overview of the entire email campaign performance. Each card displays the count and percentage for key performance indicators of your email campaign, providing a comprehensive view of delivery, engagement, and conversions across all recipients (refer to the following image):

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebcc106b5d8f957741c6a012daa5dcffae22d62da79ad1cb8f89107f8d09505a-image_33.png",
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


| Metric          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sent            | Displays the total number of emails sent, excluding emails sent to CC and BCC recipients.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Delivered       | Displays the total emails delivered to the recipient. It also displays the delivery rate, calculated as `(Total Delivered / Total Sent) * 100`.                                                                                                                                                                                                                                                                                                                                                                                              |
| Viewed          | <li>Displays the open percentage of your email message. It is calculated as `(Viewed / Delivered) * 100`. In case the Delivered count is 0, the percentage is calculated as `(Viewed / Sent) * 100`.</li><li>Includes views from CC/BCC recipients.</li><li>AMP for Email Viewed: Displayed for AMP Email campaigns. Displays the count and percentage of total emails rendered as [AMP emails](https://docs.clevertap.com/docs/ampforemail).</li><li> HTML Viewed: Displays the count and percentage of total emails rendered as HTML.</li> |
| Clicked         | <li>Displays the percentage of clicks from the total messages delivered, calculated as `(Clicks / Delivered) * 100`. In case the Delivered count is 0, the percentage is calculated as`(Clicks/Sent) * 100`. Includes clicks from CC/BCC recipients.</li><li> AMP for Email Clicks: Displayed for AMP Email campaigns. Displays the count and the percentage of clicks on emails rendered as AMP. </li><li>HTML Clicks: Displays the count and percentage of clicks on emails rendered as HTML.</li>                                         |
| CTR             | Denotes the Click Through Rate (CTR) of the campaign, calculated as `(Total Clicked / Total Viewed) * 100`.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Converted Users | Displays the percentage of total users who performed the conversion event (for example, Product Purchase) and the number of users who converted.                                                                                                                                                                                                                                                                                                                                                                                             |

> 📘 Sent Count and Metrics Availability
> 
> Sent count is not decremented for delivery errors. This means that even if the ESP reports a delivery failure, such as a bounce or drop, the count of emails marked as Sent remains unchanged. These metrics are also available for **cc** and **bcc** recipients.

This section also displays the following stats:

- _Errors_: Displays the number of errors for the campaign. These can be technical errors, such as email provider errors, or non-technical errors, such as message frequency exceeded. 
- _Control Group_: Displays the number of users to whom the campaign was not sent.
- _CC Sent_: Displays the total number of emails sent to recipients under the CC field.
- _BCC Sent_: Displays the total number of emails sent to recipients under the BCC field.
- _CC Errors_: Displays the total number of emails that failed to be sent to recipients under the CC field. This refers to errors encountered when sending email campaigns from CleverTap to the ESP.
- _BCC Errors_: Displays the total number of emails that failed to be sent to recipients under the BCC field. This refers to the errors encountered when sending email campaigns from CleverTap to the ESP.
- _Global Unsubscribes_: Displays the total number of unsubscriptions. The unsubscription is attributed to the primary recipients who qualify for the campaign only if you use the `unsubscribe(isReEncode)` method to [unsubscribe from an email campaign](doc:handling-unsubscribes).
- _Click-through Conversions_: Displays the number of conversions triggered by users who clicked on the email. The percentage is calculated as `(Click-through Conversions / Delivered) * 100`.  
- _View-through Conversions_: Displays the number of conversions triggered by users who viewed the email. The percentage is calculated as `(View-through Conversions / Delivered) * 100`.

> 📘 Note
> 
> - Tracking delivery-related errors such as Unsubscribes, Bounces, and Report as Spam are not available for CC/BCC recipients.
> - Adding CC BCC recipients in the email campaigns is currently released in Private Beta. Contact your Customer Success Manager for access.

## Variant Comparison

This section provides detailed performance insights for each variant in multivariant campaigns, such as A/B Tests, Split Delivery, or Messages based on User Properties. 

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


You can analyze the stats for the following metrics: _Sent_, _Viewed_, _Clicked_, or _Delivered_. The graph illustrates trends for the selected metric over the selected time period. The table below the graph shows the following metrics for each variant: Sent, Viewed, Clicked, and Delivered. 

## Message Trend

Click **Message Trend** to view your campaign's performance trends over time. It typically visualizes key metrics such as the number of emails Sent, Delivered, Viewed, or Clicked across a specified time frame.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6387f4645e645617a6d02afb1312d5498a64d7706a0c3dc263adecdd0a2b6140-Screenshot_2025-01-03_at_15.35.33.png",
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


## Conversion Performance Overview

Click _Conversion Performance_ to view Conversion performance, Revenue performance, and Users' conversion funnel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4926df710212f9c9545d540d4959288981dcc62a4ee2fb8d61b99517d6120625-conversion_Performance.png",
        "",
        "Conversion Performance"
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Performance"
    }
  ]
}
[/block]


You can view stats for each variant under the User conversion funnel for A/B Test, Split Delivery, and Message on User Property campaigns.

### Conversion Performance

The conversion performance section shows the conversion boost achieved from your campaign. You can compare your campaign conversions with the control group conversions to see the impact of your campaign. Target Group Conversions and Control Group Conversions are calculated based on **Delivered** to ensure accuracy by considering only the emails that successfully reached users inbox. 

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


### Revenue Performance

The _Revenue Performance_ section shows the revenue boost achieved from your campaign. The following information is displayed in this section:

- _Incremental revenue due to this campaign_: Indicates the additional income directly attributed to a specific campaign. It is calculated as:  
  [(ARPU of Target Group – ARPU of Control Group) x Number of Users to whom the campaign was sent], where ARPU is calculated as: (Revenue generated / Number of users to whom the campaign was sent)
- _Boost in revenue due to this campaign_: Indicates the percentage increase in revenue achieved from running the campaign compared (revenue generated from Target Group) to the baseline revenue that would have been generated without it (revenue generated from Control Group). It is calculated as:  
  {\[(Target Group ARPU – Control Group ARPU) / Control Group ARPU] x 100}
- _Target Group Revenue_: Indicates the total revenue generated by users targeted by the campaign.
- _Control Group Revenue_: Indicates the total revenue generated by users not targeted by the campaign (control group).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ff5668c4506a3f95069acb0ff8a00a64a41fe2c6984766c02d7f2e25f1e53f20-revenue_performance.png",
        "",
        "Revenue Performance"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Revenue Performance"
    }
  ]
}
[/block]


## Users Conversion Funnel

Shows the conversion funnel, that is, _Sent_ > _Delivered_ > _Viewed_ > _Clicked_ > _Converted_. This helps you understand the drop-offs at each step more effectively.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cb91b9aced4e6870e15e740cf57a73eb0a27a578340845a2267b9e872d5288bd-image_31.png",
        "",
        "Users' Conversion Funnel"
      ],
      "align": "center",
      "border": true,
      "caption": "Users' Conversion Funnel"
    }
  ]
}
[/block]


You can view stats for each variant under the User conversion funnel for A/B test, Split delivery, and Message on user property campaigns. 

The _Viewed_ numbers in a report can sometimes be unusually high because of virus scanners, email forwards, email groups, and so on. For more information, refer to [Unusually High Email Opens and Clicks](doc:troubleshooting-open-click-tracking). 

Based on your tracking requirement, you can select to hide either the _Viewed_ or _Delivered_ step. 

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