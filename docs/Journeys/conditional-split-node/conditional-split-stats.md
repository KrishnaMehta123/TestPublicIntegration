---
title: Conditional Split Stats
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

The Conditional Split Stats provide detailed insights about how users enter and move through each defined path. Stats are displayed per path and include counts and percentages under the *Node Stats* tab.

# View Conditional Split Stats

Stats are displayed per path and include counts and percentages under the *Node Stats* tab. To view the stats, perform the following steps:

1. Click the required journey from the All Journeys page.
2. Select the *Node Stats* tab. The stats page opens to show the journey nodes.
3. Select the date range to show stats for the journey. 

<Image alt="Conditional Split Stats" align="center" border={true} src="https://files.readme.io/1ce5a488302a679a1345c047225b6fc243ea165c708e7a6fd4b02b0e03680bef-Conditional_Split_Stats.png">
  Node Stats for Conditional Split Journey
</Image>

4. Open the Conditional Split node stats by clicking the node. The following stats are displayed:

   <Image alt="Conditional Split Node Stats" align="center" border={true} src="https://files.readme.io/779d9e55ecf3fe65f096d71827abb909c50bd0646de0ce47d92b6b628cd04b14-Conditional_Split_Node_Stats.png">
     Conditional Split Node Stats
   </Image>

Conditional Split stats allow marketers to see how users are segmented across different paths, based on real-time or historical property evaluations. This reveals:

* Which conditions attract the highest volume of users
* How evenly (or unevenly) users are distributed across logic branches
* Whether fallback/default paths are being overused. For example, if 80% of users fall into the fallback path, your segmentation logic may need refining.

## Users Across Paths

This provides a visual and tabular representation of how users are distributed across each defined path over a selected time range. It helps you analyze the performance of your segmentation logic in real time and its effectiveness within the journey. 

### User Trend by Path

The line chart in the Stats tab helps you quickly analyze user distribution across each conditional path over time. It is especially useful for identifying behavioral trends, spotting anomalies, and validating the performance of your split logic.

<Image alt="Users Across Conditional Paths" align="center" border={true} src="https://files.readme.io/c5bf1baa0b112592e417d74a05f1696b053fecc28878c0ee72d506ae7734a716-Users_Across_Conditional_Paths.gif">
  Users Across Conditional Paths
</Image>

Each line in the chart corresponds to a defined path. The Y-axis represents the number of users who entered a specific path. The X-axis represents the time dimension, displayed based on the selected granularity: Day, Week, or Month. You can use the dropdown menu at the top right of the chart to toggle between:

* Day(s) (default)
* Week(s)
* Month(s)

This helps you zoom in on short-term spikes or zoom out for long-term trends. You can also toggle which paths appear in the graph.

### Tabular View of Users Across Path

A tabular view below the graph provides detailed counts of users who entered each path, broken down day-wise (based on the selected filter). You can use the checkboxes to toggle which paths are visible in the graph. The columns in the table are aligned with the date markers in the graph for accurate comparison.

<Image alt="Tabular View of Users Across Path" align="center" border={true} src="https://files.readme.io/853f684cd5efbddfafbd96048dd1ac46fa82ac03275b5e3a9f25ce8a2d82c44f-Users_Across_Conditional_Paths.gif">
  Tabular View of Users Across Path
</Image>
