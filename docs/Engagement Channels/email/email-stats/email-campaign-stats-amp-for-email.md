---
title: Email Campaign Stats
excerpt: Measure the performance of your Email campaign
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View Email Campaign Stats

After the email campaign is live, the following events are raised in case of email campaigns:

- _Notification Sent_, when the email campaign is sent to the user.
- _Notification Viewed_, when the user opens the email campaign.
- _Notification Clicked_, when the user clicks on the email campaign.

You can view the stats by navigating to _Campaigns_ from the CleverTap dashboard. To do so:

1. Click Campaigns from the dashboard. The All Campaigns page displays.
2. Select the email campaign you want to view the stats for. You can also filter campaigns using the **Filter** button (see figure below).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/214f660-image.png",
        null,
        "Filter Email Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Email Campaigns"
    }
  ]
}
[/block]

3. Click the campaign to open it. The Stats tab displays the following campaign stats: Sent, Viewed, Clicks, CTR, and Converted users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/856e5de-image.png",
        null,
        "Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Campaign Stats"
    }
  ]
}
[/block]

The stats card shows the total count and the percentage. You can track the following stats for your email campaign:

- **Sent**: The total number of emails sent.
- **Viewed**: It shows the open percentage for your message, which is calculated as (Viewed/Sent\*100). It also shows the total number of emails opened. 
  - **AMP for Email Viewed**: Shows the percentage of your total emails rendered as [AMP emails](https://docs.clevertap.com/docs/ampforemail). 
  - **HTML Viewed**: Shows the percentage of your total emails rendered as HTML. 
- **Clicks**: It shows the percentage of clicks from the total sent messages. It is calculated as (Clicks/Sent\*100). It also shows the number of clicks on the emails.
  - **AMP for Email Clicks**: Shows the percentage of clicks on emails rendered as AMP. 
  - **HTML Clicks**: Shows the percentage of clicks on emails rendered as HTML. 
- **CTR**: The clickthrough rate of the campaign. It is measured by (Click/Viewed\*100). 
- **Converted users**: The percentage of total users that performed the conversion event. For example, purchasing an item. It also shows the number of users that converted after receiving the campaign. 
- **Errors**: Number of errors for the campaign. These errors can be technical errors, such as email provider errors, or non-technical errors, such as message frequency exceeded. 
- **Control group**: The number of users considered part of a control group for the campaign.
- **Unsubscribes**: Displays the number of unsubscribes.

# Message Trend

Click **Message Trend** to view the message trends by _Sent_, _Viewed_, or _Clicked_. You can view the daily, weekly, or monthly trends.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/27a73a8-Email_Stats_Message_Trend.png",
        "Email_Stats_Message_Trend.png",
        2680
      ],
      "align": "center",
      "border": true,
      "caption": "Message Trend"
    }
  ]
}
[/block]

# Conversion Performance Overview

Click _Conversion Performance_ to view _Conversion performance_, _Revenue performance_, and users' _Conversion funnel_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/32d1f59-Email_stats_conversion_performance.png",
        "Email_stats_conversion_performance.png",
        2726
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Performance"
    }
  ]
}
[/block]

## Conversion Performance

The conversion performance section shows the conversion boost achieved from your campaign.  You can compare your campaign conversions with the control group conversions to see the impact of your campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7bf34ea-Email_Stats_Conversion_Conversion_hero.png",
        "Email_Stats_Conversion_Conversion_hero.png",
        1310
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Performance Stats"
    }
  ]
}
[/block]

## Revenue Performance

The Revenue Performance section shows the revenue boost achieved from your campaign.

## Users Conversion Funnel

Shows the conversion funnel, that is _Sent_ > _Viewed_ > _Clicked_ > _Converted_. You can understand the drop-offs at each step of the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e1b1ae-Email_Stats_Conversion_Performance_with_Viewed.png",
        "Email_Stats_Conversion_Performance_with_Viewed.png",
        2592
      ],
      "align": "center",
      "border": true,
      "caption": "Users' Conversion Funnel"
    }
  ]
}
[/block]

### Hide Viewed

The _Viewed_ numbers in a report can sometimes be unusually high because of virus scanners, email forwards, email groups, etc. For more information, refer to [Unusually High Email Opens and Clicks](doc:troubleshooting-open-click-tracking). In this case, you can hide the viewed step by selecting _Hide Viewed_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4954e5-Email_Stats_Conversion_Performance_No_Viewed.png",
        "Email_Stats_Conversion_Performance_No_Viewed.png",
        2698
      ],
      "align": "center",
      "border": true,
      "caption": "Hide Viewed Funnel"
    }
  ]
}
[/block]

# Split of Clicks

You can track the distribution of clicks on each link that you include in your email campaign.  For example, you want to send an email promotion for an upcoming movie on your video streaming app. You can create an email campaign and add links for reviews, promotions, movie merchandise, and so on, and then send the campaign.  We will record the clicks for each link in the email, and you can see them on the \_Campaign Stats \_page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8dc04dc-Email_Stats_Split_Clicks.png",
        "Email_Stats_Split_Clicks.png",
        2708
      ],
      "align": "center",
      "border": true,
      "caption": "Split Clicks"
    }
  ]
}
[/block]

### User Details

You can view the details of users who clicked on your email campaign using the View details of users who clicked the link present on the _Split of Clicks_ tab. You are navigated to the _Events_ page. Click the _People_ tab to view user details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d55d148-Email_stats_notification_clicked.png",
        "Email_stats_notification_clicked.png",
        1049
      ],
      "align": "center",
      "border": true,
      "caption": "Event Analysis for Notification Clicked"
    }
  ]
}
[/block]

### View Detailed Engagement Stats

You can also view the user details for notifications sent, viewed, and clicked from the _Analytics_ page of the CleverTap dashboard. Consider an example of viewing the user details for the _Notification Viewed_ event. To do so:

1. Navigate to _Analytics_ > _Events_ from the CleverTap dashboard.
2. Select the desired date range.
3. Select the Notification Viewed event and the required filter. Similarly, you can select the Notification Sent or Notification Clicked event to view the required user details of who performed that event.
4. Click **View details**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2712690-image.png",
        null,
        "Event Analysis for Notification Viewed"
      ],
      "align": "center",
      "border": true,
      "caption": "Event Analysis for Notification Viewed"
    }
  ]
}
[/block]

# Errors

You can view campaign errors from the _Stats_ > _Errors_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0711eb8-Email_campaign_error.png",
        "Email_campaign_error.png",
        2702
      ],
      "align": "center",
      "border": true,
      "caption": "Email Campaign Errors"
    }
  ]
}
[/block]

## Bounces

A bounced email is an email message that gets rejected by a mail server. There are two types of bounces:

### Soft Bounce

A soft bounce indicates that mail bounced due to one of the following reasons even though the email address was valid and the email message reached the recipient's mail server:

- The mailbox was full (the user has consumed all the quota)
- The server was down
- The message was too large for the recipient's inbox  
  CleverTap campaign reports include soft bounces and do not mark the users as unsubscribed.

### Hard Bounce

A hard bounce indicated that the email was returned to the sender and was completely undeliverable. However, common reasons it got rejected include:

- The email address is invalid
- The email address does not exist
- The recipient's email server has blocked the emails

CleverTap campaign reports include hard bounces and mark the users as unsubscribed.

> 📘 Retries for Soft Bounce
> 
> The number of retries for a soft bounce depends on the Email Service Provider.