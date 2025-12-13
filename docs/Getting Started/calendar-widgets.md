---
title: Calendar Widgets
excerpt: Explore the versatile features of CleverTap's Calendar Widget.
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

There are two types of calendar widgets available in the CleverTap dashboard: Relative Date and Calendar Date. The features and differences between these two calendar widgets are described below.

# Relative Date

When you use the Relative Date calendar widget, the data is populated based on today's date and the relative date option you select. 

For example, if you select the last 7 days option on January 15, the data is populated from January 8 to January 15. Similarly, if you select January 16 with the last 7 days option, the data is available from January 9 to January 16. 

<Image title="Select the Relative Date to View the Data" alt={320} align="center" border={true} src="https://files.readme.io/9c2fb0e-image2.png">
  Select Relative Date
</Image>

## Relative Date Options

The relative date provides the following predefined options:

* Today
* Last 7 days
* Last 15 days
* Last 30 days
* Last 90 days
* This Month
* Previous Month
* Custom: You can also set a custom relative date with the following options:
  * **In the last:** This option lets you choose the number of days (or weeks/months/years) to go back from the current date. You will be able to see data from the selected days (or weeks/months/years) to the current date.
  * **Was exactly:** This option lets you choose the exact number of days ago to populate data from.

<Image title="Select Custom Relative Date Option and Click Apply" alt={407} align="center" border={true} src="https://files.readme.io/f235979-image3.png">
  Custom Relative Date Options
</Image>

> 📘 Working of Custom Relative Date
>
> The flexible custom relative date options for user qualification functions in the following ways:
>
> * **Last 1 Day**: Encompasses data from the previous day and extends up to the campaign execution time. For example, a campaign is executed at 4 PM on January 2. In that case, all the users who performed the event between 12 AM on January 1 to 4 PM on January 2 will receive the message.
> * **Was exactly 1 Day ago**: Includes all the data from yesterday only. For example, if the goal is to target users who exclusively performed the event yesterday, this is the ideal date option to use.
> * **Last 24 hours**: Checks the last 24-hour period from the campaign execution time. For example, if campaign executes at 4 PM, it considers user activity from 4 PM the previous day until the campaign's execution time.
>
> These differences help customize campaigns to specific user behaviors within defined time periods.

# Calendar Date

When you select the calendar date range, you can choose the exact days for which you want to filter data. For example, you can filter data between April 16 and May 7 as shown in the following image: 

<Image title="Select Calendar Date Range and Click Apply" alt={573} align="center" border={true} src="https://files.readme.io/6857ae8-image1.png">
  Calendar Date
</Image>

## Calendar Date Options

The Calendar Date widget offers the following options:

* **Between**: Provides data for all dates within the selected range. For example, selecting January 14 to February 15 includes data from both the specified start and end dates, encompassing all dates in between.
* **Before**: Provides data up to the selected date, excluding the selected date. For example, selecting January 15 includes data up to and including January 14. The lower date bound is determined by either the Data Retention Policy or 10 years, whichever is earlier.
* **After**: Provides data from the selected date until today and excludes the selected date. For example, selecting January 14 excludes any data recorded on January 14 and includes the data from January 15.
* **On**: Provides data for a specific date of your choice. For example, selecting January 15 provides data specifically for January 15.

# Operators

Operator is a feature only available under the event property section. This feature gives you two options: 

* **Exists:** Filter your data based on whether the date is present for the event. For example, if you are a travel booking company, you can find data for the Charged event where the departure date you select exists.

* **Does Not Exist:** Filter your data based on whether the date is absent for the event. For example, if you are a movie streaming app, you can find data for the *Subscribed* event where the upload date you select does not exist.
