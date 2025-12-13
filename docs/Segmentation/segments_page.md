---
title: Segments
excerpt: ''
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

A segment in CleverTap is a group of users that share the same characteristics such as actions performed, actions not performed, or user profile properties based on the defined criteria. For example, a segment can be users who launched the app for the first time in the past 30 days. A more complex segment could be users who live in New York, were acquired via a Facebook campaign in April, transacted three or more times in May and June, and have not transacted in the past two weeks. 

The *Segments* page lets you create segments, perform different operations on the segments, and view segment trends over time to understand how a segment behaves in response to your marketing initiatives. The entire CleverTap dashboard can be filtered by any segment you create, including any of our analytics features.

<Image title="Segments page navigation.png" alt={2878} align="center" className="border" border={true} src="https://files.readme.io/d4502bd-Segments_page_navigation.png" />

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Field</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Segment details</p>
      </td>

      <td>
        <p>Displays the details like segment name, ID, and email ID of the user who created the segment.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Type</p>
      </td>

      <td>
        <ul><li>Displays the type of segment. </li><li>The following are the options available:<ul><li>Past Behavior Segment</li><li>Live User Segment</li><li>Precomputed Segment</li><li>Custom List</li><li>Partner - Mixpanel</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Created on</p>
      </td>

      <td>
        <p>Displays the date on which the segment was created</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Updated on</p>
      </td>

      <td>
        <p>Displays the date on which the segment was last updated.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Updated by</p>
      </td>

      <td>
        <p>Displays the email ID of the user who last updated the segment.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Goals</p>
      </td>

      <td>
        <p>Displays the number of goals that are running on the segment.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IBS Goals</p>
      </td>

      <td>
        <p>Displays the number of goals running with Intent-Based Segment.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Engagement</p>
      </td>

      <td>
        <ul><li>Displays the number of active and scheduled customer engagements such as campaigns and journeys that use the segment within <a href="doc:segments_page#include-and-exclude-segments">include/exclude</a> filters.</li><li>On clicking the number, it displays the list of campaigns and journeys where the segment is being used. You can also click on a particular campaign/journey from this list to view the campaign details.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Dependent Segments</p>
      </td>

      <td>
        <ul><li>Displays the number of other segments that include or exclude the selected segment.</li><li>On clicking the number, it displays the list of segments that include/exclude the selected segment. You can also click on a particular segment from this list to view the segment details.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

# Types of Segments

There are two types of behavioral segments in CleverTap, which are explained in the following sections.

## Past Behavior Segments

Past behavior segments are users grouped by their actions in the past.\
You can group users based on a single activity to complex combinations of actions, inactions, and user properties.

> 👍 Past Behavior Segments Example
>
> An example would be to segment by all my users who launched the app in the past 30 days.

## Live User Segments

While past behavior segments let you evaluate users based on historic criteria, live user segments let you track what is happening in your app right now.\
When you define a set of behaviors of interest, CleverTap monitors for these behaviors as they happen in your app and immediately adds a user to a segment the moment their behavior matches your action criteria.\
You can create live user segments for a single activity (booked a movie ticket), inaction (did not buy a movie ticket in a certain time), On a date/time properties of events, or website-related actions, such as page visit, count, or referrer.

## System User Segments

The following are the system-defined user segments that are available for your use: 

* **All Users**: This user segment contains all the users available to your account.
* **Test Users**: This user segment contains the users who you can test for your campaign response. A campaign or journey can now be tested on this *Test Users* segment before it is sent to an actual segment. The *Test User* segment is available by default for engagement and UI experiences. 

<Image title="Segments page.png" alt={2374} align="center" className="border" border={true} src="https://files.readme.io/7afa1c6-Segments_page.png" />

# Create Segments

The steps vary based on the type of segment you want to create.

## Create Live User Segments

To create a new segment, perform the following steps:

1. From the dashboard, navigate to *Understand* > *Segments* > *Segments*.
2. Click **+ Segment**. On clicking, *Create New* page opens.

<Image title="PBS.png" alt={582} align="center" className="border" border={true} src="https://files.readme.io/9e34a1c-PBS.png" />

3. Select from the following available options based on the requirement:\
   *Single action (for example, users who have added a product to the cart)\&#xA;* Inaction within time (for example, users who have added a product to the cart but did not purchase within 10 minutes of adding the product to the cart)\
   *On a date/time (for example, users who have an appointment five days from today)\&#xA;* Page visit (for example, users who have visited a specific URL on your website)\
   *Referrer entry (for example, users who have visited your website via a specific external referrer URL)\&#xA;* Page count (for example, users who have visited a certain number of pages on your website)

  Consider the example of creating an *Inaction within time* segment for which users will qualify in real-time as soon as they add a product to the cart but do not purchase it within 10 minutes.

> 📘 Golden Window for Mobile Transactions
>
> The golden window within which most users transact on our iOS and Android app platforms is within 10 minutes.

4. Select the appropriate properties for your live user segment.\
   You may choose to select the *Filter on past user behavior and common properties* checkbox to apply past action, inaction, or common user property filters.
5. Click **Save segment**.

<Image title="Create_new.png" alt={688} align="center" className="border" border={true} src="https://files.readme.io/7bd9343-Create_new.png" />

6. Enter the *Segment name* and click **Save**.

> 📘 Segment Naming Best Practices
>
> Convey the core meaning of the segment while keeping the name brief.

You can now see your new segment in the main section as *Added to cart but no charge within 10 minutes*.

## Create Past Behavior Segments

To create a past behavior segment, perform the following steps: 

1. From the dashboard, navigate to *Segments* > *Segments*.
2. Click *+Segment*
3. Select from the following available options based on the requirement:

   * Past user actions (for example, users who added a product to the cart in the past 30 days)
   * Past user action/inaction combination (for example, users who added a product to the cart but did not purchase it in the last 30 days)
   * Past user action/inaction combination along with common user properties (for example, platinum-level users who added a product to the cart but did not purchase in the last 30 days)\
     from the main segment creation page.

      Consider the example of creating an action-based segment where users qualify if they applied a payment offer at least one time in the past 30 days.
4. Select *Actions* that take you to the *Create New* page.

<Image title="PBS_Action.png" alt={893} align="center" className="border" border={true} src="https://files.readme.io/eed64c6-PBS_Action.png" />

5. Click **Save segment**. 
6. Enter the *Segment name* and click **Save**.

# View Segment Details

To view segment details, navigate to *Segments* > *Segments*, search for the segment you are looking for and then click on it. On clicking, segment details are displayed. At the top of the page, you can click *View segment definition* to understand more about the underlying query. 

## Live User Segment Details

It displays the following information:

* **Segment trend**: Displays the number of users who qualified for the segment going forward from the first complete day after creating the segment.
* **Today's Event Flow**: The right-hand side shows the real-time rate at which users are qualifying for the segment vs. all user activity on your app/website. 

<Image title="View Live Segment Details.png" alt={2446} align="center" className="border" border={true} src="https://files.readme.io/929f703-View_Live_Segment_Details.png" />

* **Segment size and reachability**: Displays the list of sample users trickling into your segment in real-time on the right-hand side. It also shows the reachability percentages for these users within each messaging channel on the left-hand side.
* **Do more with this segment**: Displays how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

## Past Behavior Segment Details

It displays the following information:

* **Segment trend**: Displays the number of users who qualified for the segment going forward from the first complete day post-segment creation. 
* **Segment size and reachability**: The lower portion of the past behavior segment details consists of reachability percentages for these users within each messaging channel. 
* **Do more with this segment**: The lower-most part of the page shows you how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.
* Goals: Displays the goals running on the segment.

<Image title="View Past Behavior Segment Details.png" alt={2448} align="center" className="border" border={true} src="https://files.readme.io/b7cd6b0-View_Past_Behavior_Segment_Details.png" />

# View Analytics Filtered by Segment

Under the *Do more with this segment section,* you have the option to view an analytics report. This is for the chosen segment alone and not your entire user base.\
Analysis dashboard views have the following filter at the top to enable this:

<Image title="Analytics_FIltered.png" alt={1242} align="center" className="border" border={true} src="https://files.readme.io/99dbb38-Analytics_FIltered.png" />

Real-time dashboard views such as the *Today* dashboard enable filtering by live user segments. Analytics based on past behavior such as mobile apps, revenue, funnels, cohorts, trends, and events enable filtering their stats by past behavior segments.

# Create Campaigns for a Chosen Segment

Under the *Do more with this segment* section, under *Engage*, you have the option to create a campaign to message a specific segment.\
This immediately takes you to the messaging channel with your segment criteria pre-populated in the target.

<Image title="Segments_Do_More_Campaign.png" alt={617} align="center" className="border" border={true} src="https://files.readme.io/3c7905e-Segments_Do_More_Campaign.png" />

# Include and Exclude Segments

You can simplify complex queries by including or excluding the existing user segments. Create segments with complex conditions once and then reuse them in different scenarios. 

You can create powerful segmentation that is valid for a variety of scenarios. 

<Image title="0fd3c96-Find_people_include_exclude_segments.png" alt={715} align="center" className="border" border={true} src="https://files.readme.io/30d054b-0fd3c96-Find_people_include_exclude_segments.png" />

## Exclude Segments

There may be instances when you want to exclude some users based on specific criteria.\
For example, you want to offer discounts to all the users who have expressed interest by adding the product to the cart in the past 30 days; however, you want to save your engagement dollars by excluding the power users.\
The parameters for these power users can be the following:

* Users who have charged three times in the past three months, and 
* Users who have launched the app 15 times in the past month, and
* Users who rated a product 10 times in the past year

Now, you can create a segment with these criteria called *Power Users* and use it every time rather than creating a complex query each time. You can save all these parameters in a segment called *Power Users* and exclude them from the discount message. 

The following is a campaign query for an e-commerce app that excludes the *Power Users* segment.

<Image title="exclude_segments_campaign.png" alt={1050} align="center" className="border" width="100%" border={true} src="https://files.readme.io/2fb7f6a-exclude_segments_campaign.png" />

## Include Segments

There may be instances when you want to include some users based on specific criteria.\
Consider the example of a ride-hailing app. You want to nudge your users to enroll for a monthly pass as soon as they open the app. The parameters for these users can be the following:

* The users must be power users, and
* The users have booked more than five rides in a month, and
* They belong to select cities in the country

Now, you can create a segment with these criteria called *Power Users* and using it repeatedly rather than creating a complex query each time. 

The following is a campaign query for a ride-hailing app that includes the *Power Users* segment.

<Image title="include_segments_campaign.png" alt={1067} align="center" className="border" width="100%" border={true} src="https://files.readme.io/f9f341a-include_segments_campaign.png" />

> 📘 Include and Exclude Segments
>
> * You can include and exclude segments in the same query. It is considered as an *AND* condition between the Included and the Excluded segments.
>   * The include and exclude segments are currently unavailable for bulletins and A/B Testing.
>   * The segments available for including or excluding users can only be of the type [PBS](https://docs.clevertap.com/docs/segments#section-past-behavior-segments) and [Custom List](https://docs.clevertap.com/docs/custom-list-segments) segment.

# Additional AND By Behavior Filters

*AND By behavior* filters provide customers the ability to segment users based on the count, average, or total sum of a property value.

### Count

The count filter allows customers to filter users by event count. The query finds all users who performed a *Charged* event greater than 5 times in the past 30 days. 

<Image title="2020-11-24_17-51-01_Count.png" alt={1192} align="center" className="border" border={true} src="https://files.readme.io/0678593-2020-11-24_17-51-01_Count.png" />

### Average of Property Filter

The *Average of property* filter allows customers to filter users by the average of a chosen event property. The query finds all users who performed a *Charged* event such that the average *Revenue* event property per event is greater than $10. 

The *Average of property* filter allows averaging the value of the selected event property. For example, you can find out the average revenue earned from all users who performed purchases worth $10 or less. Let us assume that 5 users charged for each for $3, $5, $7, $2, and $8. The average value of all the purchases lower than $10 is ($ 3+ 5 +7+2+8)/5 events = 25/5= $5 per event. 

Let us assume that the value for 2 charged events is missing. The charged event values received are $3, $5, and $7. The value of the missing events will be considered as 0. The average of property is now ($3 + 5 +7 +0 +0)/5 events = 15/5 =$3 per event. 

If you want to exclude all the events that do not have event properties, you can select the property that exists a condition in the *Filter by* section.

<Image title="2020-11-24_17-52-22_Average of property.png" alt={1192} align="center" className="border" border={true} src="https://files.readme.io/09c3239-2020-11-24_17-52-22_Average_of_property.png" />

### Total Sum of Property

The *Total sum of property* filter allows customers to filter users by the sum of a chosen event property. The query finds all users who performed a *Charged* event such that the *Revenue* event property is greater than $10.

<Image title="2020-11-24_17-53-50_Total sum of property.png" alt={1194} align="center" className="border" border={true} src="https://files.readme.io/d973ab4-2020-11-24_17-53-50_Total_sum_of_property.png" />

> 📘 Include Users Who Did Not Do the Event
>
> If the query is to find people who performed the charged event fewer than five times, by default, the users who have not performed the charged event are not included in the result set. Only the users who did the charged event but did it fewer than five times are included; however, if the checkbox for *Include users who didn’t do the event* is selected, those users are also included in the result set. The same is true for sum and average.

<Image title="2020-11-24_17-56-46_Checkbox message.png" alt={1187} align="center" className="border" border={true} src="https://files.readme.io/db44a26-2020-11-24_17-56-46_Checkbox_message.png" />

# Segment Operations

You can perform different actions on the segments from the *Segments* page. Each of them is explained in the sections to follow

## Search Segment

You can search segments by their Name or ID from the *Segments* page.

<Image title="Search Segment.png" alt={2396} align="center" className="border" border={true} src="https://files.readme.io/1251882-Search_Segment.png" />

## Copy Segment Name and ID

To copy segment name and ID:

1. From *Segments* page, hover on the *name* or *ID* of the required segment.
2. Click the ![Copy](https://files.readme.io/0e1c106-Copy_icon.png) icon against the respective segment.

<Image title="Copy Segment name and ID .png" alt={2402} align="center" className="border" border={true} src="https://files.readme.io/0455ea5-Copy_Segment_name_and_ID_.png" />

## Engage with Segment

To engage with a segment directly from the *Segments* page:

1. Click ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the *Segment details* column and click **Engage**.

<Image title="Engage from Segments page.png" alt={2394} align="center" className="border" border={true} src="https://files.readme.io/e73666c-Engage_from_Segments_page.png" />

   On clicking, *Messaging Channels* popup displays.

2. Select the *Messaging Channel*. 

<Image title="Messaging Channels popup.png" alt={2376} align="center" className="border" border={true} src="https://files.readme.io/6d679c6-Messaging_Channels_popup.png" />

On selecting the channel, you are navigated to the messaging channel with your segment criteria pre-populated under the *Who* section of the *New Campaign* page.

<Image title="Who section prepopulated.png" alt={2752} align="center" className="border" border={true} src="https://files.readme.io/4ebf6d1-Who_section_prepopulated.png" />

## Clone a Segment

This operation helps to create a new segment from an already existing segment with minor or no modifications to the qualification criteria of the segment. To clone a segment directly from the *Segments* page:

1. Click the ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the *Segment details* column and click **Clone**.

<Image title="Clone Segment.png" alt={2394} align="center" className="border" border={true} src="https://files.readme.io/d3fba76-Clone_Segment.png" />

  On clicking, the *Create New* page opens with prepopulated qualification criteria.

2. Make the necessary modifications to the qualification criteria, if required.
3. Click **Save segment**.
4. Enter the *Segment name* and click **Save**.

## Delete

There may be times when you may need to delete unused segments. You can do so in the following ways:

### One by One

To delete the unused segments one by one:

1. Click ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the *Segment details* column and click **Delete**.

<Image title="Delete Segment.png" alt={2394} align="center" className="border" border={true} src="https://files.readme.io/c9ab0c2-Delete_Segment.png" />

On clicking, the *Delete Segment?* popup is displayed on the right side of the screen.

2. Click **Delete** to confirm your action.

### Delete Segments in Bulk

To delete more than one segment at one time:

1. Select the checkbox for the segments you wish to delete and click![Delete\_segment](https://files.readme.io/67c524b-Delete_icon.png). 

<Image title="Bulk_delete.png" alt={1107} align="center" className="border" width="80%" border={true} src="https://files.readme.io/1699a28-Bulk_delete.png" />

  On clicking, the *Delete Segment?* popup is displayed on the right side of the screen.

2. Click **Delete** to confirm your action. 

<Image title="Confirm_delete.png" alt={2878} align="center" className="border" width="80%" border={true} src="https://files.readme.io/8705265-Confirm_delete.png" />

> 📘 Note
>
> If your account's total number of segments exceeds 1000, you can view up to 500 segments on a single page and delete a maximum of 500 segments at a time. If the number of segments is less than 1000, you can view up to 50 segments on a single page and delete a maximum of 50 segments at a time.

## Sort

You can sort segments based on the following columns under *Segments* page by clicking the arrows against the respective columns :

* Segment details
* Created on
* Updated On
* Engagement
* Dependent Segments

<Image title="Sort Segments.gif" alt={1188} align="center" className="border" border={true} src="https://files.readme.io/ab3b2c8-Sort_Segments.gif" />

## Filter Segments

You can filter out segments based on the following fields by clicking the ![Filter](https://files.readme.io/9cb6680-Filter_icon.png) icon:

* Type: Indicates the type of segment. 
* Goals. Indicates the goals running on the segment.
* Created by: Indicates the name of the user who created the segment.
* Updated by: Indicates the name of the user who last updated the segment.

<Image title="Filter Segments.gif" alt={1196} align="center" className="border" border={true} src="https://files.readme.io/2382971-Filter_Segments.gif" />

You can also filter segments based on the date on which the segments were created. To do so, select the date range, available at the top, for which you want to view the segment.

<Image title="Filter Segments by creation date.png" alt={2398} align="center" className="border" border={true} src="https://files.readme.io/6a92678-Filter_Segments_by_creation_date.png" />
