---
title: Notification Delivery Options
excerpt: Learn to select from various timezone options.
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

The Notification Delivery Options allow you to effectively schedule and manage notifications across various timezones. Timezone options, such as Account Timezone, User Timezone, and Ad hoc Timezone, offer businesses the flexibility to target users based on their local timezones, thereby optimizing engagement and effectiveness. This is especially beneficial for businesses with a global user base, ensuring that time-sensitive notifications are delivered at the most appropriate time for each user.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e5557ffbb341dffe4f0ebb2610bfc5e3e31583ab93cb2dd8311feb0458545b1-Select_Timezone.png",
        "Select timezone for scheduling campaign and journeys.",
        1020
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Select Timezone"
    }
  ]
}
[/block]


# Account Timezone

This is the default timezone set for your CleverTap account. All timestamps and campaign schedules default to this timezone unless a different option is explicitly selected. If you use the account timezone when sending the campaigns, the message is delivered as per _Account Timezone_ set from your dashboard.

For example, if the campaign promotes a local event, such as a concert, and the attendees are primarily located within the same geographical region as your business, using the same timezone as that of your account simplifies the process with effective communication timing. The notifications thus align with the local time, ensuring they are received at an appropriate and relevant moment creating a delightful impact.

## Set Up Account Timezone

To set up the Account Timezone:

1. Go to _Settings_ > _Project_ and click the _Edit Icon_ for Timezone.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c43440c-Timezone.png",
        "Timezone.png",
        2510
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Account Timezone"
    }
  ]
}
[/block]


2. Select the timezone of your account and click **Change**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7a572f8-Change_Timezone.png",
        "Change Timezone.png",
        2114
      ],
      "align": "center",
      "border": true,
      "caption": "Select Timezone"
    }
  ]
}
[/block]


# User Timezone - Adapting to Local Timezone

This option ensures that notifications and campaigns are scheduled based on each user’s local timezone. This approach personalizes the delivery timing, making it more relevant and effective for a globally distributed audience. CleverTap determines a user's timezone based on their device location settings. When you select User Timezone for a campaign, the platform staggers the notification delivery to match the selected time in each user’s local timezone.

For example, a business is launching a new feature and wants to notify all users at 6:00 PM local time. With User Timezone, here’s how the campaign is delivered across different regions: 

- Users in New York (Eastern Time Zone): New York is in the Eastern Standard Time (EST) zone, so these users will receive the notification at 6:00 PM EST.
- Users in London (Greenwich Mean Time Zone): London is in the Greenwich Mean Time (GMT) zone, so these users will receive the notification at 6:00 PM GMT.
- Users in Paris (Central European Time Zone): Paris operates on Central European Time (CET), so users there will get the notification at 6:00 PM CET.
- Users in Tokyo (Japan Standard Time Zone): Tokyo is in Japan Standard Time (JST), so the notification will reach them at 6:00 PM JST.
- Users in Sydney (Australian Eastern Daylight Time Zone): Users in Sydney, which follows Australian Eastern Daylight Time (AEDT), will receive the notification at 6:00 PM AEDT.

Businesses can use the User Timezone to ensure their messages resonate with users, regardless of where they are in the world.

> 📘 Note
> 
> You can set up the users' timezone via the `Tz` key in the `profileUpdate`method.

## Set Up User Timezone

You can set up the user timezone from the _Date and time_ section under the _When_ section. When you select the user timezone, you have the following two options to address the situation when the user whose timezone has already passed:

- _Drop the campaign_:  When you select this option, any user whose timezone has already passed when the campaign kicked off does not receive this campaign.
- _Deliver the campaign the next day_: When you select this option, any user whose timezone has already passed receives the notification at the same time on the next local day.

> 📘 Critical Delivery Dates
> 
> If it is critical for a campaign to be delivered on a certain calendar day (for example, an Easter Day campaign) and the message has to arrive on Easter Sunday or not at all, choose the _Drop the campaign_ option.

# Ad hoc Timezone - Set Up Specific Timezone

> 📘 Private Beta
> 
> Currently, this feature is Private Beta. If you want to access this feature, contact your Customer Success Manager (CSM).

The option allows you to schedule campaigns to align with a specific timezone of your choice, irrespective of the account timezone or the user’s local timezone. This option is particularly useful when targeting users in a specific region.

For example, you are hosting a webinar for users in the Eastern Standard Time (EST) zone at 3:00 PM. To ensure all participants receive a reminder email or notification at 2:00 PM EST, you can select Custom Timezone and set it to EST.

## Set Up Ad hoc Timezone

You can set up an Ad hoc timezone for your campaigns from the _Date and time_ section under the _When_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cfde662f0bab5b4e3d855b825c078db21232c14d747de645b83be7f0a31517ab-Set_Up_Ad_hoc_Timezone.png",
        "",
        "Set Up Ad hoc Timezone For Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Ad hoc Timezone For Campaign"
    }
  ]
}
[/block]


After selecting the custom timezone for the campaign, you need to define the specific date and time at which you want to send the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0d2b86e722b596b7a1640138f59148900fd635ffa9b9c98ffc7ca690752f1fd-Select_A_Fixed_Date_and_Time_.png",
        "",
        "Define A Specific Date and Time For Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Define A Specific Date and Time For Campaign"
    }
  ]
}
[/block]


## Ad hoc Timezone Support for Notification Types

All the following notification types support Ad hoc Timezone for both Send Later/Multiple Dates and Send Recurring scheduling options: Push, Email, SMS, Inbox, App Inbox, Web Push, Webhooks, Amazon EventBridge, Segment, and mParticle.

> 📘 Impact of Ad hoc Timezone on Cut Off, Absolute TTL, and Best Time
> 
> - **Best Time**  
>   The campaign is sent at the exact time you specify during the setup of the Ad hoc Timezone, without adjusting for the Best Time based on user behavior.
> - **Cut Off**  
>   The Cut Off Time for the campaign is determined based on the Ad hoc Timezone you select. This ensures the campaign stops sending notifications at the correct time for that specific timezone.
> - **Time to Live**  
>   TTL is set according to the Ad hoc Timezone, meaning the campaign expires at the specified time in that timezone, not based on the User or Account timezone.

# Do Not Disturb Hours

CleverTap allows setting the Do Not Disturb hours for notification delivery while creating a campaign. You can set this to ensure that the users who qualify for the campaign are not disturbed during the specified DND hours.

If a user qualifies for a notification during DND hours, you can decide to discard it completely or specify that you will deliver it to the user after the end of DND hours.

> 📘 DND Timezone
> 
> DND is set based on the respective timezone of every user by default. If the timezone is not available for any user, DND will be applied as per the account timezone.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d436c32-DND_doc.png",
        "Select the DND timezone",
        1766
      ],
      "align": "center",
      "border": true,
      "caption": "Select DND Timezone"
    }
  ]
}
[/block]


## Set Up DND for Campaign

To set DND for the campaign:

1. Go to _Delivery Preferences_ under the _When_ section from the new campaign page.
2. Select _Do Not Disturb (DND)_  to view the DND options. 
3. Select the days and input the times you do not want to send campaign notifications. If you want to use the same inactive period daily, click the _Copy Time To All_ link.
4. Select the Message handling during DND option as per your use case and click **Done**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1bd274-DND_Options.png",
        "Select DND preferences",
        446
      ],
      "align": "center",
      "border": true,
      "caption": "Select DND Preferences"
    }
  ]
}
[/block]


# Campaign Frequency Limits and Display Rules

Campaign frequency allows you to define when a user qualifies for a message. If a user qualifies outside this window, the message campaign is discarded. This feature is available for Mobile In-App or Web Popup campaigns.

In the case of Mobile In-App, it offers the additional flexibility of specifying the frequency at which the campaign is delivered based on a defined trigger count.

To set up campaign frequency: 

1. Go to _Delivery Preferences_ under the _When_ section from the new campaign page.

2. Select _Set frequency_, select the days, and enter the time slots you do not want to send campaign notifications. If you want to use the same time inactive period for each day, click **Apply to all**.

3. Select from the _Deliver how often?_ dropdown to set up how frequently you want to send the notification and click **Done**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fce5d09-Campaign_frequency.png",
        "Set frequency to qualify users",
        617
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Frequency to Qualify Users"
    }
  ]
}
[/block]


# Campaign Cut-off

The campaign cut-off time ensures no notifications are sent after the specified time. This is useful if the campaign is time-sensitive and a later time makes the notification irrelevant.  
Select the _Cut-off_ checkbox and specify the time to stop sending the notification when the number of target users is large, causing a significant delay in processing the user queue. This ensures that after the set time, there is no notification sent. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a38d84-Campaign_Cut_Off.png",
        "Campaign Cut-Off Time",
        472
      ],
      "align": "center",
      "border": true,
      "caption": "Campaign Cut-Off Time"
    }
  ]
}
[/block]


# Time To Live

**Time to Live** is the notification's persistence sent to an end user. It regulates the time that the system monitors user device status to deliver a push notification. Whenever the user is online during the set TTL period, the notification is delivered. Any user not coming online will not receive the push notification, and there are no notifications attempted after the TTL period is over. For more information, refer to [Time to LIve](doc:create-message-push#time-to-live).

# Message Frequency Caps

If you have multiple marketing campaigns running simultaneously for any one channel, the same user may qualify to receive a message from more than one campaign in a given day, week, or month. Frequency caps provide you the capability to limit the number of notifications a user will receive from all the campaigns running for that channel.

Frequency is channel-specific. Frequency caps let you limit the total number of notifications received in a given timeframe for one delivery channel, not across all channels. You can set up channel-specific limits. For more information, refer to [Messaging Frequency Caps](doc:messaging-frequency-caps).

## Error Reporting with Frequency Caps

The error reporting section of the campaign report displays the number of users who were excluded from receiving the campaign due to the frequency cap setting.

| Non-technical Errors    | Android | iOS |
| :---------------------- | :------ | :-- |
| Frequency Caps Exceeded | 1158    | 73  |