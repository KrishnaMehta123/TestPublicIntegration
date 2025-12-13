---
title: View Segments
excerpt: Learn how to view Segment details from the CleverTap dashboard.
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

You can view the details of a segment to understand more about the underlying query. These details help you understand the following:

- Segment triggers and rules based on behavior and interests
- Frequency of users qualifying in a segment
- Reachability of qualified users with different engagement channels
- Qualified user profiles

# View Segment Details

You can view Past Behavior and Live Segment details from the dashboard. To view segment details:

1. Navigate to _Segments_ > _Segments_.
2. Search for the segment you are looking for, then click on it.

On clicking, it displays the following details:

- **Segment Trend**: Displays the number of users who qualified for the segment going forward, starting from the first full day after the segment creation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eeb00ea-Segment_Trend.png",
        "",
        "View Segment Trend"
      ],
      "align": "center",
      "border": true,
      "caption": "View Segment Trend"
    }
  ]
}
[/block]


- **Insights**

Displays the number of users reachable via different messaging channels and sample user profiles who qualify for the segment.

You can now view Segment Insights in two modes:

- **Estimate (Default): **Shows approximate statistics for the segment to enable faster loading and quicker reachability insights.
- **Exact:** Displays precise data for the segment after complete processing, providing the most accurate user counts across all channels.

You can use Estimate to quickly preview reachability and switch to Exact when you need accurate data before taking action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dc297a5488daa78627ae612e673309de9654066bb724ca6903fe23e4d1c9f491-image.png",
        null,
        "View Segment Insights"
      ],
      "align": "center",
      "border": true,
      "caption": "View Segment Insights"
    }
  ]
}
[/block]


# Export User Profiles

The _Insights_ section allows you to export the users in the CSV format from any segment that you have created. 

To export the users in CSV format:

1. Click the![](https://files.readme.io/758da8c-Export_User_Profiles.png) icon under the _Insights_  section. 
2. Select the fields that you may want to export and click **Export**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f2f69a-Export_User_Profiles.png",
        null,
        "Export User Profiles"
      ],
      "align": "center",
      "border": true,
      "caption": "Export User Profiles"
    }
  ]
}
[/block]


> 📘 Mismatch in Segment Size and Number of Users Exported to CSV File
> 
> The number of users displayed under the _Segment size and reachability_ section may vary from the number of users exported to the CSV file. This variation is due to the inclusion of blacklisted users under the _Segment size and reachability_ section.

# View Custom - List Based Segment Details

The Custom - List Based Segment details page displays all the available information for the segment, such as:

- **Segment trend**: If the users have increased or decreased over time. 
- **Campaigns and journeys**: The number of campaigns and Journeys currently using the custom list segment. 
- **Segment size and reachability**: The total number of users in the segment and their reachability across various engagement channels. 
- **Sample users**: These are samples from your list. You can open any of them to check their details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81840d5-Segments_Custom_lists_report.png",
        "Click to Hide/Show the Segment or Download the Segment CSV File",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Hide/Show Segment or Download as CSV"
    }
  ]
}
[/block]


> 📘 Download in CSV
> 
> Click the ![](https://files.readme.io/8967517-Download_Segment_Icon.png) download icon to download all the users in your segment.