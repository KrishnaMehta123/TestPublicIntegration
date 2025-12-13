---
title: Inbox Stats
excerpt: Measure the performance of your App Inbox campaign.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View App Inbox Stats

You can use the Campaign Filters to find your campaigns. Once the campaign is live, you can view its stats by selecting an _Inbox_ campaign from the _Campaigns_ page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d112a06-Filter_Inbox_Campaigns.png",
        "",
        "Filter Inbox Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Inbox Campaign"
    }
  ]
}
[/block]


Click to open the selected campaign. The campaign stats page displays.

You can track the following stats:

- Sent: The total number of notifications sent to the inbox for the user.
- Viewed: The total number of times the messages have been viewed by the user. Whenever the message is viewed by the user, `markMessagesAsRead` API is called. Calculated as [(Viewed/Sent) * 100].
- Clicks: Number of times the messages have been clicked by the user. Whenever the message is viewed by the user, `markMessagesAsClicked` API is called. Calculated as [(Clicks/Viewed) * 100]. 
- CTR: The clickthrough rate of the campaign. It is calculated as [(Click/Viewed) * 100].
- Converted users: The percentage of total users who performed the conversion event after receiving the campaign.
- Errors: The number of messages not delivered to the user. These errors can be technical, such as FCM-related, or non-technical, such as message frequency exceeded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/826d27e-Inbox_Statistics_Overview.png",
        "",
        "Inbox Campaign Statistics"
      ],
      "align": "center",
      "border": true,
      "caption": "Inbox Campaign Statistics"
    }
  ]
}
[/block]


# Message Trend

Shows the daily, weekly, and monthly trends for the following events: Sent, Viewed, and Clicked.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/43faec3-Performance_Trend_-_Inbox_Campaign.png",
        "",
        "Performance Trend for Sample Inbox Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Performance Trend for Sample Inbox Campaign"
    }
  ]
}
[/block]


# Conversion Performance

## Conversion Performance

Shows the Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel.

## Revenue Performance

Shows the incremental and boosted revenue due to the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0d86a4b-image.png",
        null,
        "Conversion and Revenue Performance"
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion and Revenue Performance"
    }
  ]
}
[/block]


## User Conversion Funnel

Displays the conversion funnel for the Inbox campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/89f170d-User_Conversion_Funnel.png",
        "",
        "User Conversion Funnel"
      ],
      "align": "center",
      "border": true,
      "caption": "User Conversion Funnel"
    }
  ]
}
[/block]


## User Details

Click _View details of users who clicked the notification_. The event analytics is displayed. Select the _People_ tab to view user details.

# Errors

You can view campaign errors from the Stats > Errors tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/04bedbc-Campaign_Error_Stats.png",
        "",
        "Inbox Campaign Error Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Inbox Campaign Error Stats"
    }
  ]
}
[/block]