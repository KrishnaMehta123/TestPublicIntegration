---
title: Mobile App View
excerpt: ''
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

The *Mobile App* dashboard shows various metrics related to app usage, user retention, engagement, and conversion across mobile platforms.

Navigate to *Boards* > *Mobile App*.

* *Daily Active Users*, *Weekly Active Users*, and *Monthly Active Users* represent users who have launched your application at least once during the respective *Daily*, *Weekly*, and *Monthly* time period.

<Image title="Mobile App View on Boards" alt={747} align="center" width="1000%" border={true} src="https://files.readme.io/81d29e43b7712f839f5e45b89fbc359db05e7e06004863140bc55a2f95dfe54e-Mobile_App.png">
  Boards-Mobile App View
</Image>

The *Quick View* shows:

## Active Users

1. Select the required segment under *For Segments*.
2. Select the date range.

<Image title="Select the Date Range" alt={2420} align="center" width="auto" border={true} src="https://files.readme.io/33f145e-Date_Range.png">
  Select the Date Range
</Image>

This shows: 

* *Total users*- Total number of users who launched the mobile app in the selected time period.
* *Average users*- Displays data based on the **Time Interval** selection, shown in![One](https://files.readme.io/07d4443-one.png) below.
  * For *Daily* time interval, it shows the average daily users for the selected date range.
  * For *Weekly* and *Monthly* intervals, it shows the number of users who launched the mobile app in the last 7 days and 30 days, respectively, of the selected date range. 

<Image title="Active Users Analytics" alt={2418} align="center" width="auto" border={true} src="https://files.readme.io/26fa986-Active_Users.png">
  Active Users Analytics
</Image>

## Conversions

This shows the total number of users who have performed the conversion event ( set under “Settings > Schema > Events > Conversion event ) within the selected time period.\
It also displays data based on the **Time Interval** selection, shown in![One](https://files.readme.io/07d4443-one.png) above.\
For *Daily* time interval, it shows the average daily conversion for the selected date range.\
For *Weekly* and *Monthly* intervals, it shows the total number of converted users in the last 7 days and 30 days, respectively, of the selected date range.

<Image title="Conversations Analytics" alt={2340} align="center" width="auto" border={true} src="https://files.readme.io/11d7c44-Conversions.png">
  Conversations Analytics
</Image>

> 📘 Note
>
> The number of users is displayed as NA (Not Applicable) if the selected date range is less than a week or a month and the interval filter is set as weekly or monthly, respectively.\
> If the selected date range is less than a week with the time interval as “weekly”, then both “Last 7 days’ users” and “Last 30 days’ users” will not be applicable and is displayed as NA.

## Distribution by App Version

This shows the distribution of users by the version of the App being used. 

<Image title="Distribution by App Version" alt={1169} align="center" width="auto" border={true} src="https://files.readme.io/0ea452f-Dist_app_version.png">
  Distribution by App Version
</Image>

## User Retention And Conversion

This shows detailed metrics on 1, 3, and 7-day *Retention*, *Engagement*, and *Conversion* rates. These metrics offer insights into the proportion of users who revisit your application, actively engage with it, and successfully convert into paying (or any other metrics of your choice) users within the initial 1, 3, and 7 days following the launch of your app.

For example, consider a scenario where your app is downloaded by 1,000 users on day 0. If 500 of them launch your app on day 1, the retention rate would be 50% for the day. Similarly, if 250 users meaningfully engage with your app on the same day, your engagement rate on day 1 would be 25%. Finally, if 50 users made a purchase on the same day, your 1-day conversion rate would be 5%.

<Image title="User Retention and Conversion" alt={1173} align="center" width="auto" border={true} src="https://files.readme.io/f978b4e-User_rention.png">
  User Retention and Conversion Data
</Image>

For detailed analysis, click *More*

## App Launched vs Conversions

This displays a comparison of users who have launched thez app vs users performing the conversion event.

<Image title="App Launched vs Conversions" alt={1211} align="center" width="auto" border={true} src="https://files.readme.io/84adb06-AppL-VsC.png">
  App Launched vs Conversions Data
</Image>

## Usage and Revenue Trends

This shows you the following metrics based on selection.

* *Daily Paying Users*/*Daily Active Users (DPU/DAU(%)*) and *Daily Paying Users*/*Monthly Active Users (DPU/MAU(%)*) epresent users for whom you have raised the *Charged* event (or users qualifying as per the conversion event) at least once during the relevant time period.
* *Average Revenue Per Daily Active User (ARPDAU)* which gives a sense of revenue earned on a daily basis per user from your application.
* *Average Revenue Per Daily Paying User (ARPDPU)* which gives a sense of average daily revenue from a paying user in your application.
* *Daily Active Users*/*Monthly Active Users(DAU/MAU(%)*), also known as *Sticky Quotient*, which represents the percentage of your monthly active users who visit your application daily (i.e., how many of your active users are very active users).

<Image title="Usage and Revenue Trends" alt={1194} align="center" width="auto" border={true} src="https://files.readme.io/7ae1d75-Usage_Revenue.png">
  Usage and Revenue Trends Data
</Image>
