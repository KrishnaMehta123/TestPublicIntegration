---
title: Engagement Stats
excerpt: >-
  Track and manage campaign performance across all journey channels with unified
  Engagement Stats.
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

Engagement Stats provide a unified view of how each messaging node performs across all versions of a journey, helping marketers make data-driven decisions.

For instance, a lifecycle marketing team may iterate on a welcome journey to improve user onboarding, testing different message sequences, timings, or channels in each version. With Engagement Stats, they can easily evaluate how each version performs in terms of overall engagement, delivery, and conversions, helping them identify the most effective strategy and continuously optimize user experiences across the funnel.

# View Engagement Stats

To view engagement stats: 

1. Go to **Journeys**. Click the desired Journey and click **Engagement Stats**.
2. Select the version from the Version dropdown to view the stats for the specific version of the Journey.

<Image alt="Engagement Stats" align="center" border={true} src="https://files.readme.io/0695e07a69b4b1874f22fcef844ad3b9cfa2b57323547aa789b37a747ebac0cc-View_Engagement_Stats.png">
  Engagement Stats
</Image>

The following stats for each engagement node are displayed: 

| Columns                  | Description                                                                                          |
| :----------------------- | :--------------------------------------------------------------------------------------------------- |
| **Engagement node name** | Name of the engagement node.                                                                         |
| **Node ID**              | Unique identifier of the journey node.                                                               |
| **Campaign ID**          | Unique ID for the campaign.                                                                          |
| **Channel**              | Type of messaging channel used. For example, SMS, Push, etc.                                         |
| **Engagement**           | The engagement achieved by the channel varies based on different calculation rules for each channel. |
| **Rate**                 | Rate of engagement for the node. For example, click percentage.                                      |

You can also view the campaign stats for each engagement node by hovering over the engagement and then clicking the ![](https://files.readme.io/ae4f09b7b09fc99539e01a77b22398ea2804e432ef51a052a5d491d9d3cba7b2-Screenshot_2025-07-02_at_1.13.57_PM.png)icon. To learn more about the stats of each messaging channel, refer to the Stats document for each channel.

<Image alt="Campaign Stats" align="center" border={true} src="https://files.readme.io/a905ed06f6f180f2f88974da68b2aa66e741ba0a94e293aaabcee3c6ac5a47a3-Enagagement_Stats_-_Push_Message.png">
  Campaign Stats
</Image>

# Manage Engagement Stats

This section provides steps for managing engagement statistics. It describes how to filter data, search data, edit columns, set pagination, and download data as a CSV file.

## Filter Engagement Stats

You can filter the engagement stats by channel. Click the **Filters** button at the top right corner and select the required channel. To clear the filter, click **Reset all**.

<Image alt="Select the required channels" align="center" border={true} src="https://files.readme.io/6f244070021029f466db6eb3906e70a594fc1e2806c28d9b8bc9d5a28c816ab5-Filter_by_Channel.png">
  Select the Required Channels
</Image>

## Search Engagement Stats

Enter the name or the node ID to search for a particular engagement in the search box.  (@amrita to change to a good image)

<Image alt="Search by Node ID" align="center" border={true} src="https://files.readme.io/41654da889c7fad2db2a97f2277d5a89426aa7a8ea7d1ccb3e247eb4439ebdcd-Search_by_Node_ID.gif">
  Search by Node ID
</Image>

## Edit Columns

While the table layout is fixed by default, you can still sort and filter the data to focus on the metrics that matter most. To sort and manage the engagement data effectively, perform the following steps:

1. Click ![](https://files.readme.io/f68f358198ebefc6d706e68c697e962b7e4467d00b47510ce0a8fdb8bae85781-Edit_Columns_icon.png) in the top right corner. The *Edit Columns* popup opens.
2. Toggle ON to show the required column on the Engagements tab page. 
3. Drag and drop the columns to change their order. 
4. Click **Apply Changes**. 

## Download CSV for Engagement Stats

You can export engagement data from the Engagements tab of a Journey as a CSV file. The downloaded file includes key metrics such as Engagement Node Name, Node ID, Campaign ID, Channel, Impressions, Clicks, and Engagement Rate. This is useful for audits, offline analysis, or sharing performance reports. 

To download the engagement stats CSV: 

1. Select the desired engagement nodes. 
2. Click the ![](https://files.readme.io/dc353d489783c14e9f6fbb342fbbe86b1f4fa7da36ec311e770d3be748d4d8d9-download_icon_png.png) icon at the top of the table.

The CSV file downloads automatically. All the columns displayed on the screen are included in the CSV file.

<Image alt="CSV Download" align="center" border={true} src="https://files.readme.io/7b03dca97f806f68ea1bffef88aa97fb133f2e351374fbb306f4ce4c14d4c1ec-Download_a_CSV.png">
  CSV Download
</Image>
