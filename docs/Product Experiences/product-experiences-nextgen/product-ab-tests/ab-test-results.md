---
title: A/B Test Results
excerpt: Learn how to analyze your A/B Test results to conclude your experiments.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# A/B Test Results

The A/B Test Results feature provides valuable insights from your experiments, aiding data-driven decision-making. It offers comprehensive analysis, intuitive visualization, statistical significance assessment, and variant distributed reporting. This helps users uncover insights leading to product enhancement, improved user engagement, and overall success of the A/B test.

It utilizes advanced filtration methods to ensure accurate data assessment. It includes only data captured during the user's participation in the test, excluding any data from instances where the user enters and leaves the AB test multiple times (unless the test is marked as '[Sticky](doc:create-ab-tests#sticky-target)'). This ensures that all the available metric data available on the Results page is clean and based on user behavior.

You can view the A/B Test Results for a particular period by selecting the time range from the Calendar widget in the top right corner. This helps segment and analyze data based on when events or observations occurred for the defined timeframe. You can view results for a short interval, such as a day, a week, or a month, or a longer span, such as a year or multiple years. You define the timeframe to analyze your A/B Test as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/93adf9f-in-app_calendar.png",
        null,
        "Calendar Widget"
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Time Frame using the Calendar Widget"
    }
  ]
}
[/block]


You can further categorize your data based on platform attributes such as Operating system) and User Properties using the _Group by_ option (refer to the following image):

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6727cb2-group_by_os.png",
        "",
        "Group by OS Name"
      ],
      "align": "center",
      "border": true,
      "caption": "Group by OS Name"
    }
  ]
}
[/block]


This helps in getting a granular view of users, allowing you to make data-driven decisions across distinct operating systems or users with different properties.

Also, hovering over the Users icon adjacent to the _Results_ tab offers a high-level breakdown of actual users entering the A/B test across different Variants and the Control group (see the following image). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d2fa8eb-total_users.png",
        null,
        "Total users entering across the variants"
      ],
      "align": "center",
      "border": true,
      "caption": "Total users entering across the variants"
    }
  ]
}
[/block]


Now, the available metrics in the A/B test can be categorized into Common and Goal metrics.

## Common Metrics

Common metrics are accessible for every A/B test, regardless of whether you have chosen specific Event-based Goals. The common metrics include:

- **Unique Users**: This refers to the count of individual users who have interacted with a website, application, or service during a specific period. Each user is counted only once, regardless of how often they visit or use the platform within that timeframe.
- **Returning Users**: This refers to the individuals who have visited or interacted with a website, application, or service more than once during a specific period. They are distinguished from Unique Users who have engaged with the platform on multiple occasions.
- **First-time Users**: This refers to the individuals who visit or interact with a website, application, or service for the first time during a specific period. These users are new to the platform and have not engaged with it before within the defined timeframe.
- **Sessions**: This refers to the individual visits or interactions a user has with a website, application, or service during a particular timeframe. A session starts when a user accesses the app and ends after a period of inactivity or when the user leaves the app.  
  Tracking sessions are a great way to measure engagement for certain apps, such as video or music streaming, news, etc. You must enable session tracking from the CleverTap dashboard to track user sessions. To enable session tracking, navigate to _Settings_ > _Session analytics_ and toggle ON the [session tracking](doc:session-analytics#session-dashboard).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/129222c-common_metrics.png",
        "",
        "Common Metrics View"
      ],
      "align": "center",
      "border": true,
      "caption": "Common Metrics View"
    }
  ]
}
[/block]


Listed below are some key session metrics, along with their formulas and definitions:

| Metric                          | Formula                                                                         | Definition                                                                                                       |
| :------------------------------ | :------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------- |
| Returning Users                 | 100 x [(Total Unique Users) - (Total First-time users)] / (Total Unique Users)  | The percentage of users returning to your application or website.                                                |
| Total Sessions                  | Total occurrences of **"Session Concluded"** event                              | The total number of user sessions.                                                                               |
| Total Session Length            | Sum of values for the event property  _length_ of the _Session Concluded_ event | Calculated using the event property _length_ of the _Session Concluded_ event. The total length of all sessions. |
| Average Session Length          | (Total Session Length) / (Total Sessions )                                      | The average length of a session.                                                                                 |
| Average Session Length per User | (Total Session Length) / (Total Unique Users )                                  | The average length of a user session in your application/website.                                                |
| Average Sessions per User       | (Total Session ) / (Total Unique Users )                                        | The average number of sessions for a user.                                                                       |

## Goal metrics

Goal metrics are specific to the event and properties selected in the A/B test Goals. You can find these from the _Metrics_ dropdown on the left. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2492c9f-goal_event.png",
        "",
        "Goal Metrics"
      ],
      "align": "center",
      "border": true,
      "caption": "Goal Metrics"
    }
  ]
}
[/block]


Listed below are some key goal metrics, along with their formulas and definitions:

[block:parameters]
{
  "data": {
    "h-0": "Metric",
    "h-1": "Formula",
    "h-2": "Definition",
    "0-0": "Total <Goal event> occurrences",
    "0-1": "Total occurrences of \\<Goal event>",
    "0-2": "The total number of times the goal event was triggered.",
    "1-0": "Unique profile who triggered <Goal event>",
    "1-1": "Number of Users who triggered \\<Goal event>",
    "1-2": "Total number of users who triggered the goal event.",
    "2-0": "Percent of Users who triggered <Goal Event>",
    "2-1": "Percent of users who triggered the \\<Goal Event> =  \n100 x \\[(Users Who Triggered X Event) / (Total  Users)]",
    "2-2": "The percentage of users in your app that triggered the goal event.",
    "3-0": "Average occurrences of <Goal event> per Unique User",
    "3-1": "(Total occurrences of <GoalEvent> / Total Unique Users)",
    "3-2": "The average number of times a user triggers this event.",
    "4-0": "Average occurrences of <Goal event> per Session",
    "4-1": "(Total occurrences of <GoalEvent> / Total Sessions)",
    "4-2": "The average number of times the goal event is triggered in a session.",
    "5-0": "Total sum of \\< Event Property> values",
    "5-1": "(Total sum of \\<Event Property> values)",
    "5-2": "Total sum of all aggregate event property values associated with the goal event.",
    "6-0": "Average of <Event Property> values",
    "6-1": "(Total sum of \\<Event Property> values / Total Event occurrences)",
    "6-2": "The average value of each occurrence of this event.",
    "7-0": "Average of <Event Property> values per unique user ",
    "7-1": "(Total sum of \\<Event Property> values / Unique Users)",
    "7-2": "The average of <Event Property> values of the goal event per user."
  },
  "cols": 3,
  "rows": 8,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


After you select the event metric of your choice from the dropdown, you can view its data in graphical and tabular format. Let us consider a sample test where an e-commerce business wants to analyze the sales. In this case, you add an event **Charged** as a Goal with aggregate property `value`. The following image shows the set of available metrics for the  **Charged** event:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2174557-Goal_event_metrics.png",
        "",
        "Graphical view for the Coins Earned Event"
      ],
      "align": "center",
      "border": true,
      "caption": "Graphical Data View of Charged Event"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a71eb5-tabular_view.png",
        "",
        "Tabular view for the Coins Earned Event"
      ],
      "align": "center",
      "border": true,
      "caption": "Tabular data view for the Charged Event"
    }
  ]
}
[/block]


## All Time Performance

For a limited set of metrics (_Percent of users who triggered_ the \<Event>), you can see the _All Time Performance_ section. 

This feature calculates data throughout the entire duration of the A/B Test, irrespective of the time frame selected at the top of the page. Based on all the data, each variant is analyzed to identify if it is statistically significant, and an **indicator** is displayed next to the variants that helps:

- Validate the reliability of the results. 
- Assess whether any observed differences between the control and variant groups are not merely attributable to random chance.
- Provides you confidence in the decision-making process.

> 📘 Note
> 
> CleverTap uses a two-tailed Welch's t-test with a default setting of 95% confidence interval to identify the statistically significant variant.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53b013d-All_Time_Performance_Section.png",
        "",
        "All Time Performance View for Limited Set of Metrics"
      ],
      "align": "center",
      "border": true,
      "caption": "All Time Performance Section for a Limited Set of Metrics"
    }
  ]
}
[/block]