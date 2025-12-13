---
title: Segments Operations
excerpt: Understand the types of operations you can perform on the Segments page.
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

This document provides information about the types of operations you can perform on the segments from the CleverTap dashboard.

# Operations

You can perform different actions on the segments from the *Segments* page. Each of them is explained in the sections to follow:

## Search

You can search segments by their *Name* or *ID* from the *Segments* page.

<Image title="Search Segment.png" alt={2396} align="center" border={true} src="https://files.readme.io/7edebc5-Search_Operation.png">
  Search Segments
</Image>

## Copy Segment Name and ID

To copy the segment name and ID, click the ![Copy](https://files.readme.io/0e1c106-Copy_icon.png) icon against the respective segment from the *Segments* page.

<Image title="Copy Segment name and ID .png" alt={2402} align="center" border={true} src="https://files.readme.io/907f602-Copy_Operation.png">
  Copy Segment Name and ID
</Image>

## Engage

To engage with a segment directly from the *Segments* page:

1. Click the ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the *Segment details* column and click **Engage**.

<Image title="Engage from Segments page.png" alt={2394} align="center" border={true} src="https://files.readme.io/304a75e-Engage_Users.png">
  Engage with a Segment
</Image>

   The *Messaging Channels* popup displays.

2. Select the *Messaging Channel*. 

<Image title="Messaging Channels popup.png" alt={2376} align="center" border={true} src="https://files.readme.io/6d679c6-Messaging_Channels_popup.png">
  Select an Engagement Channel
</Image>

You are navigated to the campaign creation page with your segment criteria pre-populated under the *Who* section of the *New Campaign* page.

<Image title="Who section prepopulated.png" alt={2752} align="center" border={true} src="https://files.readme.io/ab8d24d-Target_Segment_in_Campaigns.png">
  Select Target Segment
</Image>

## Clone

This operation helps to create a new segment from an already existing segment with minor or no modifications to the qualification criteria of the segment. To clone a segment directly from the *Segments* page:

1. Click the ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the *Segment details* column and click **Clone**.

<Image title="Clone Segment.png" alt={2394} align="center" className="border" border={true} src="https://files.readme.io/7208305-Clone_Users.png" />

  The *Create New* page opens with prepopulated qualification criteria.

2. Make the necessary modifications to the qualification criteria, if required.
3. Click **Save segment**.
4. Enter the *Segment name* and click **Save**.

## Delete

At times, you might need to delete unused segments, either individually or in bulk. To delete the unused segments, follow these steps:

1. Select the segments you want to delete.
2. Click the icon. The *Delete Segment?* popup appears, listing the selected segments and their dependencies.
3. Click **Refresh** and then **Delete** to confirm deletion.

<Image align="center" className="border" border={true} src="https://files.readme.io/1812fa3cd4ecd35d0f9b61f5ade6d3d321369eff491f494e01d5a24fadf3575a-Delete_a_Segment.gif" />

> ❗️ Deletion Dependency
>
> A segment that is part of an active engagement cannot be deleted. To know more about segment deletion handling, refer to [Delete Segments](doc:delete-segments).

## Sort

You can sort segments in ascending or descending order for the following columns under *Segments* page:

* Segment details
* Created on
* Updated On

To sort, click the arrows against the respective columns:

<Image title="Sort Segments.gif" alt={1188} align="center" className="border" border={true} src="https://files.readme.io/625e912-Sort_Segments.gif" />

## Filter

You can filter out segments based on the following fields by clicking the ![Filter](https://files.readme.io/711f8d8-Filter_Icon.png) icon:

* **Type:** Indicates the type of segment, such as Past behavior, Live, Custom list, and Partner segment.
* **Created by:** Indicates the name of the user who created the segment.
* **Updated by:** Indicates the name of the user who last updated the segment.
* **Goals:** Indicates the goals running on the segment. This aids in filtering segments based on the active goals or intents currently running within them.

<Image title="Filter Segments.gif" alt={1196} align="center" className="border" border={true} src="https://files.readme.io/9a4aefa-Filter_Segments.gif" />

You can also filter segments based on the date on which the segments were created. To do so, select the date range, available at the top, for which you want to view the segment.
