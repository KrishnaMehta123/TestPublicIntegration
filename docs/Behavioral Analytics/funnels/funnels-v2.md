---
title: Funnels Beta
excerpt: >-
  Learn how to use the new and improved visualization using Funnels to gain
  deeper insights into your data and make more informed decisions.
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

Funnels show users' progress through defined paths in your app and pinpoint where they drop off between steps. Funnels are a series of events a user performs in a particular order.

A typical example is a user onboarding flow, where a user progresses from the app's initial launch through activities such as registration, profile completion, and orientation. Another example is a purchase flow, where a user progresses through a shopping cart experience to a purchase event.

> 📘 Private Beta
> 
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Success Manager or the [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).

# Creating a Funnel

To create a funnel, perform the following steps:

1. Go to _Analytics_ > _Funnels Beta_. 
2. Select the events in the desired order to create up to an eight-step funnel. 
3. Select event properties for each event to constrain the analysis for the users who performed that event/property combination.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/83e833954c171c8e655df786784d081f722d5b0aca7590b1322027f72b9ba95c-image.png",
        null,
        "Create a Funnel "
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Create a Funnel "
    }
  ]
}
[/block]


4. You can also duplicate a step or add multiple events for the step by clicking the ellipsis menu. For example, you can add Mobile Login and Website Login as two events with OR logic between them in Step 1 of the Funnel to ensure you capture your entire user base.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bb245c3bd7e1c55d271354270052226658bf057accf2ee77e3a683657255db8-image.png",
        null,
        "Select Multiple Events"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Select Multiple Events"
    }
  ]
}
[/block]


## Setting Conversion Window

Funnels are calculated based on a specified conversion window (set to five days by default). The conversion window is the total elapsed time for the user to complete all the steps in the funnel (that is, to convert). Shorter duration windows generally result in fewer users completing the funnel steps, whereas longer windows result in more user conversion. 

To set a conversion window:

1. Go to _Analytics_ > _Funnels_. 
2. Select the required events. 
3. Under the _Metric_ section, select the Conversion window.

> 📘 Time Interval for Conversion Window
> 
> CleverTap recommends setting the _Conversion Window_ to a duration shorter than the _Actual Date Range_ to avoid data variance.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4b4a9c1425395ea28c7160e36f5036b4fbe26aa9060cf40d643bc2166e122df-image.png",
        null,
        "Set Conversion Window"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Set Conversion Window"
    }
  ]
}
[/block]


## Compare by Segments

You can compare your conversions across different segments \[to analyze..}. For example, compare the funnel for _App Launched_ > _Product Viewed_ > _Charged_ across the _All Users_ and the _Engaged Users_ segments. The differences in the conversion trends could reveal differences in your users' behavior in each segment and result in invaluable insight. 

To compare conversion across segments, perform the following steps:

1. Go to _Analytics_ > _Funnels_.
2. Select the steps to analyze and view the conversion funnel.
3. From the SEGMENT section, select the required segments. Select a segment from the list or create an ad-hoc segment. For more information, refer to [Segments](doc:segments).
4. Click **View Analysis**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9b8925214cf689ea3b18dce80dab48b64854c033f93eb6f3616c02eaa540eeb-image.png",
        null,
        "Segment Comparison Results"
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Comparison Results"
    }
  ]
}
[/block]


## Advanced Filtering

Advanced filters help restrict your analysis to a specific user segment. You can create a segment based on any combination of past behaviors and user properties. 

> 📘 Advanced Filters
> 
> Advanced filters is a general feature for all analytics and most campaigns. For more information, refer to [Segments](doc:segments).

# Reading Funnel Charts

Funnel charts let you quickly determine how many users progress through each funnel step. 

The default view shows cumulative conversions per step for the selected time range. It can be viewed as an absolute count of users completing each step or a percentage. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/004bcc51afc2a74579c288ffc3915fe73e0e85963c02da2f961c6939f8e346e0-image.png",
        null,
        "Funnel Charts"
      ],
      "align": "center",
      "border": true,
      "caption": "Funnel Charts"
    }
  ]
}
[/block]


## Split by Property

You can split a funnel by profile properties for sessions, geographies, and technographics or by an event property associated with any event. This lets you compare your conversion flows across product categories, geographies, devices, and more. 

To breakdown by property, perform the following steps:

1. Click **Analytics** > **Funnel**.
2. Add _Funnel_ steps and click **View Funnel**.
3. Select a user property or an event property to split the funnel. 
4. Click **View Analysis **to view the funnel. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/765e14575db123f3fbf0d28e7c1d8174c0ad9e4c4ccdbbecccbbfcea3c41dfc9-image.png",
        null,
        "Split funnel by event property"
      ],
      "align": "center",
      "caption": "Split Funnel by Event Property"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/43c847997049c7db2488cb2a08c2417a6fb9d37029765d8251a0f280e2022e1b-image.png",
        null,
        "Split Funnel by User Property"
      ],
      "align": "center",
      "border": true,
      "caption": "Split Funnel by User Property"
    }
  ]
}
[/block]


# Funnel Computation Methods

This section covers two types of funnel computation methods: the default and strict ordering methods. The strict order does not count the users who repeat a step. Conversely, the default order counts the users even if they repeat a step. 

## Default Order

By default, funnels will count all users who perform all the specified steps in order, regardless of whether they loop back to an earlier step or move forward to a later step in the funnel. 

For example, if our funnel steps are defined as:  

- Funnel Steps: Step A → Step B → Step C → Step D 

In the scenarios below, we can analyze whether different users are counted as converting depending on the order in which each progresses through the funnel steps.

- User 1: Step A → Step B → Step C → Step D
- User 2: Step A  → Step C → Step D
- User 3: Step A → Step C → Step B → Step D
- User 4:  Step A → Step B → Step A → Step C → Step D

User 1 is counted since she progresses through the funnel steps in order.  
User 2 is not counted since she did not perform Step B.  
User 3 is not counted since she completed the steps out of order.  
User 4 is counted since she completed the steps in order, although she looped back and performed Step A twice.

## Strict Order

By checking _Enforce Strict Order,_ users will only be counted if they complete the funnel steps in exactly the specified order without performing another one of the funnel steps out of order. 

Consider the same example as above where the funnel steps defined are:  

- Funnel Steps: Step A → Step B → Step C → Step D

If we analyze the users below:  

- User 1: Step A → Step B → Step C → Step D
- User 2: Step A  → Step C → Step D
- User 3: Step A → Step C → Step B → Step D
- User 4:  Step A → Step B → Step A → Step C → Step D

Here, only User 1 will be counted as converting, as the strict order restricts any deviation from the specified steps in the funnel. The other users (2, 3, and 4) are breaking the strict ordering, so they do not qualify. The advantage of strict ordering is that it can detect any deviations. For example, consider the following user actions:

- User A: App Launched, Login Attempted, Login Attempted, Login Attempted, Login Attempted, Logged In
- User B: App Launched, Login Attempted, Logged In

A strict order can help identify if users are having trouble logging in. 

# Table View

You can also view the funnel information in a table to easily compare and absorb information. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1168404ff665e17b95e472aa0d4c35eb1537a2129529fb9b7b92f6aac07f3f91-image.png",
        null,
        "Table view in funnels"
      ],
      "align": "center",
      "border": true,
      "caption": "Table View in Funnels"
    }
  ]
}
[/block]


Every funnel categorization (split by user or event property) is a row in the table. To get better insight, sort by the required column. You can refer to  the following information in each row:

- Overall % conversion from the first step to the last step. 
- Conversion % from one step to the next.

 In the current example, you can conclude after the sort that Arabic speakers have the highest conversion rate.

# Bookmark a Funnel Analysis

You can bookmark any Funnel analysis to quickly revisit it later. Bookmarks are user-specific; only the logged-in user can view their saved bookmarks on the CleverTap dashboard.

Bookmarks are especially useful for tracking frequently accessed conversion journeys. For example, if you regularly monitor funnel steps such as _App Launched_ > _Product Viewed_ >  _Charged_, bookmarking it lets you instantly return to the same setup without recreating the funnel each time.

To bookmark a Funnel, perform the following steps

1. Click **Bookmark** in the top-right corner of the dashboard after generating the Funnel analysis.
2. Enter a descriptive name to help you easily identify the analysis later.
3. Click **Save**.

You can add up to 50 bookmarks.

> 📘 **Note**
> 
> Funnels are accessible only to the user who created them. You can access all your saved bookmarks from the bookmark list under the _Funnels_ section.