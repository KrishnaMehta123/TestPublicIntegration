---
title: Real Impact
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
## Overview

_Real Impact_ is a reporting dashboard that shows how and by what extent users respond to your CleverTap marketing campaigns—everything from the revenue generated to churn. With _Real Impact_, you can move beyond vanity metrics and optimize your campaigns based on which campaigns are driving business results.

> 🚧 System Control Group Requirement and Performance
> 
> To view _Real Impact_ performance metrics, you need to enable a system control group for your account; this system control group is an account-level categorization of profiles that will never receive any of your campaigns. For more information, refer to [Control Groups](doc:control-groups).
> 
> It might take some time for target groups to show a marked improvement in performance over a system control group. For instance, if you have created a system control group 5 to 10 days ago, your performance numbers might not be as distinctive. 
> 
> It is recommended to wait for a few weeks after creating a system control group to visualize accurate figures in the _Real Impact_ dashboard.

_Real Impact_ helps you measure the impact of your campaigns:

- Visualize the boost in performance in your target segments as compared to users who have not received any campaigns.
- Estimate what percentage of users have churned in the target group by contrasting it with control groups.
- Calculate the segment-wise impact of essential business metrics and know which segments have been performing better compared to others.
- Visualize user movement from one RFM segment to another.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af4e987-Screenshot_2019-03-13_at_9.23.03_PM.png",
        "Click Revenue Per User and Select the Options",
        1216
      ],
      "align": "center",
      "border": true,
      "caption": "View Real Impact"
    }
  ]
}
[/block]


To access _Real Impact_, navigate to _Analytics_ > _Real Impact_. _Real Impact_ deals with boost/drop percentage.

## How is Real Impact Calculated

As mentioned above in order to calculate _Real Impact_, we use system control groups and the calculation is done on the basis of comparison of the performance of target group vs. system control groups.

> 📘 Formula
> 
> The formula consists of:
> 
> - TG = Target group metric value
> - SCG = System control group metric value
> 
> Boost or drop % = (TG-SCG) / SCG \* 100

## Performance Metrics

You can check performance metrics for any segment at any date range. CleverTap offers the capability to measure the following performance metrics out of the box:

[block:parameters]
{
  "data": {
    "h-0": "Performance Metrics",
    "h-1": "Interpretation",
    "h-2": "Derivation",
    "0-0": "Sticky Quotient",
    "0-1": "How often your audience engages with your product after receiving your campaign over a given duration.",
    "0-2": "Daily active users / Monthly active users.",
    "1-0": "Retention",
    "1-1": "Indicates how many users come back to your product to perform a set of actions based on your marketing efforts over a given period. For example, what percentage of users who made a purchase came back for a repeat purchase in the last 30 days?",
    "1-2": "Similar to [Cohorts](doc:cohorts).",
    "2-0": "Conversion",
    "2-1": "Measures the real impact of your campaigns on a target group for a conversion event. This metric tells you what percentage of target group users converted on your product as compared to the conversion rate of control group users.",
    "2-2": "Similar to [Funnels](doc:funnels).",
    "3-0": "Revenue per User",
    "3-1": "Select an event used to calculate the accumulated revenue for a particular day and its corresponding property used to identify active users (App Launched).  This metric helps compare the average revenue per user in the target group who received campaigns and the control group who did not receive campaigns for a particular period of time.  \n  \nNOTE: Consider a scenario where the DRP of the selected event is more than that of the App Launched event (used to derive the active users). In this case, you can only view data for real impact on revenue per user for the duration, which is the minimum of both the DRPs.",
    "3-2": "Total revenue for the selected period / Active user for the same period",
    "4-0": "RFM Segments: RFM Score",
    "4-1": "This _Real Impact_ metric gives a boost in the health score of the target group based on recency, frequency, and monetary parameters.  \n  \nFor example, what is the RFM health score for all users who launched an app and made a purchase in the last 30 days?",
    "4-2": "Refer to [RFM Score](https://docs.clevertap.com/docs/real_impact#section-rfm-score) below.",
    "5-0": "RFM Segments: Matrix",
    "5-1": "Increases/decreases the percentage of users in each of RFM sub-segments from two consecutive date ranges.",
    "5-2": "Visualization.",
    "6-0": "RFM Segments: Transitions",
    "6-1": "Views user's movements from one sub-segment to another.",
    "6-2": "Visualization.",
    "7-0": "Recency",
    "7-1": "Tracks how recently target users visited your product in the last 30 days as compared to the control group.",
    "7-2": "Median number of days users have been recent.",
    "8-0": "Frequency",
    "8-1": "Frequency of an event being done on the app by users.",
    "8-2": "Median number of times an event is performed within the time range."
  },
  "cols": 3,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## RFM Score

RFM scores denote the value of your app/website's users. The value of the user is measured across three dimensions, including, recency, frequency, and monetary, then the user is automatically assigned a score.

> 📘 How RFM Score is Calculated
> 
> CleverTap uses a unique method to calculate RFM scores. Recency, frequency, and monetary values are calculated for all users. Users are divided into five different sections according to their percentiles. Therefore, the bottom 20% will be in the first percentile and get a score of 1. The next 20% get a score of 2 and so on up to a score of 5. 
> 
> The scores are calculated for all the three dimensions including, recency (R), frequency (F), and monetary (M). Finally, the RFM score is also calculated by taking into considerations the weights of the individual dimensions.
> 
> RFM Score = 4xR + 2xF + M

A well-designed campaign or journey keeps users engaged and improves retention over time. By understanding key metrics like the retention rate formula and using a retention rate calculator, you can measure and enhance user loyalty. Check out [Retention Rate: Definition, Formula & Best Practices](https://clevertap.com/blog/retention-rate/) to learn how to track and improve your retention rate effectively.