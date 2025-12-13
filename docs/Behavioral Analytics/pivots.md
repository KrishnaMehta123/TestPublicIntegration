---
title: Pivots
excerpt: Understand what are Pivots in CleverTap.
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

Pivots provide the capability to derive significance and insights from your user data. The pivot analysis tool summarizes your data with the help of tables and other data visualizations. When dealing with a large volume of data, this useful tool helps marketers create incisive summaries and view custom reports to glean user insights.

A pivot analysis helps answer questions, such as:

- Which categories of my products are selling best, and at what time of the day?
- In which city are my sales for Nike shoes the lowest?
- How many minutes of sports content do my platinum customers consume each day of the week?

# Pivot Video Tutorial

Discover the video tutorial for the Pivot overview and a sample use case.

[block:html]
{
  "html": "<div style=\" position: relative; padding-bottom: 56.25%; height: 0; border-radius: 0; box-shadow: 0 15px 40px rgba(63,58,79,.3); overflow: hidden; min-width:320px\"><iframe src=\"https://clevertap.portal.trainn.co/share/U5SSOkOXuV6Cg17hr43l7w/embed?autoplay=false\" frameborder=\"0\" webkitallowfullscreen mozallowfullscreen allowfullscreen allow=\"autoplay; fullscreen\" style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe></div>"
}
[/block]


# Getting Started with Pivots

Let's start exploring Pivots together. To do so:

## Pick Your Event

To pick your event:

1. Navigate to _Analytics_ > _Pivots_.
2. Select the event you want to analyze. 

This event forms the basis of your analytics that can be coupled with its properties along with all the information CleverTap has for your users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f2319fd-Pivots_select_event.png",
        "Select Pivot Options and Click Calculate Button",
        1189
      ],
      "align": "center",
      "border": true,
      "caption": "Select Pivot Calculation Options"
    }
  ]
}
[/block]


## Select Your Segment

After you have selected the event to analyze, decide if you want to analyze this event for all your users or for a particular segment of users. This feature is useful as the behavior of users varies across segments. 

> 👍 Content Consumption Example
> 
> The content consumption for a new user segment will be very different from the consumption of people who have already consumed at least 50 hours of content.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ed3243-Pivots_segments_create.png",
        "Create Segment for Pivot Analysis",
        870
      ],
      "align": "center",
      "border": true,
      "caption": "Select Segment"
    }
  ]
}
[/block]


## Picking the Properties to Pivot On

Select the properties to analyze, such as:

- Event properties
- User properties
- Geography
- Technographics
- App fields 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e943721-Picking_the_Properties_to_Pivot_On.png",
        "Pick the Properties to Pivot On",
        866
      ],
      "align": "center",
      "border": true,
      "caption": "Select Pivot On Properties"
    }
  ]
}
[/block]


## Aggregating Your Query by Count vs. Conversion Property

You can group your data by the occurrences of an event which are the number of times this event has happened. 

If the event you are analyzing is your conversion event and your conversion property is an integer, you can group your data by the sum of this property. 

> 👍 Flight Aggregator Example
> 
> A flight aggregator can view data by the count of flight booked event or by the sum of the amount property.

## Understanding the Pivot Analysis

The pivot analysis consists of:

- Pool of available properties: This is a list of properties you selected while creating the pivot table. You can use these properties in any combination to slice and dice your data to derive insights. These properties could act as rows or columns in the tabular view and as cartesian axes in the graphical view.
- Row(s): The properties you select as rows in your tabular views.
- Column(s): The properties you select as columns in your tabular views.
- Data visualizations: You can select what visualization you want to see the data you have sliced and diced in.

# Example Analysis

For example, with a video application, we can use the pivot analysis to understand its output and content consumption patterns in our platform. To do so, we have selected the event _video watched_ which is raised after someone is done watching a video.

For this pivot analysis, we select the following properties:

- Hour of the day
- Day of the week
- Video name

We also pick our measurement property as _video duration watched_ since it is critical for us to measure video performance, not just by the number of views, but also by the duration of content consumption.

Now, we explain each view and tell you what insights can be drawn for each view supported by our pivot analysis.

## Table

This is best for getting a quick overview of selected data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6f678ed-Pivots_result_table.png",
        "View Pivot Results in Table Form",
        1197
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot Table"
    }
  ]
}
[/block]


## Table Heat Map

This is best for analyzing highest contributor in a given data set. 

For example, if your row is day of the week and your column is video name, this heat map tells you which video was played the most and on which day of the week it happened.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5258a1a-Pivots_heat_map.png",
        "View Pivot Results in Table Heat Map Form",
        1194
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot Table - Heat Map"
    }
  ]
}
[/block]


## Columnar Heatmap

This is best for analyzing outliers in any column. 

For example, if your row is day of the week and your column is video name, this heat map tells you which video was played the most on each day of the week.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/631d4e0-Pivots_heat_map_columnar.png",
        "View Pivot Results in Table Columnar Heatmap Form",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot Table - Columnar Heatmap"
    }
  ]
}
[/block]


## Row-wise Heatmap

This is best for analyzing outliers in any row. 

For example, if your row is day of the week and and your column is video name, this heat map tells you on which day of the week each video has performed well. _Game of Thrones_ performs best on Sundays whereas _Friends_ works best on Saturdays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebb44ce-Pivots_heat_map_row.png",
        "View Pivot Results in Table Row-wise Heatmap Form",
        1199
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot Table - Row-wise Heatmap"
    }
  ]
}
[/block]


> 📘 Zero Event Occurrences
> 
> In case of zero event occurrences for a given time, the Table, Columnar, and Row-wise heatmaps indicate whitespaces.

## Stacked Bar Chart

This is best best for visualizing the change in performance of one variable over time when compared to several other variables. 

For example, if your row is day of the week and your column is video name, you might see that the performance of _Game of Thrones_ peaks around Sunday/Monday. _Game of Thrones_ is a lot lower for the rest of the week as compared to the consumption of _Friends_, _Prison Break_, and _Breaking Bad_ which are all consistent across the week.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29a3b30-Pivots_heat_map_stacked_bar.png",
        "View Pivot Results in Stacked Bar Chart Form",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot - Stacked Bar Chart"
    }
  ]
}
[/block]


## Bar Chart

This is best for visualizing categorical or qualitative data over time. 

For example, if your row is day of the week and your column is video name, you can see how the consumption of _Game of Thrones_ has been over the week.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23868d6-Pivots_heat_map_bar_chart.png",
        "View Pivot Results in Bar Chart Form",
        1198
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot - Bar Chart"
    }
  ]
}
[/block]


## Line Chart

This is best for visualizing the change of variables over time. Since all lines are plotted on the same graph, this visualization helps you determine the relationship between different variables.

For example, if your row is day of the week and your column is video name, you might see that _Breaking Bad_ and _Prison Break_ follow the same trend across the week. This implies that the demand for these videos is consistent.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bcf83e5-Pivots_heat_map_line_chart.png",
        "View Pivot Results in Line Chart Form",
        1198
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot - Line Chart"
    }
  ]
}
[/block]


## Area Chart

While similar to line charts, this is better for analyzing part to whole relationships. 

For example, if your row is day of the week and your column is show name, the area chart will not only show you the trend variation of _Game of Thrones_ over the week, but it will also show you the contribution of _Game of Thrones_ to your total video views as compared to the rest of your titles.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/49659b9-Pivots_heat_map_area_chart.png",
        "View Pivot Results in Area Chart Form",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "View Pivot - Area Chart"
    }
  ]
}
[/block]


> 📘 Note
> 
> We sample your data to ensure that results load faster, so you might see a minor difference in counts when you compare these numbers to the numbers on the rest of your dashboard. 
> 
> This sampling has been optimized for accuracy and your numbers will be directionally correct. Sampling kicks in if the query contains more than 100,000 events, and the sample rate beyond 100,000 events is 10%.