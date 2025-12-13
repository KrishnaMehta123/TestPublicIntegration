---
title: Segments
excerpt: Understand what are CleverTap Segments and how it works.
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

The _Segments_ page lets you create segments, perform different operations on the segments, and view segment trends over time to understand how a segment behaves in response to your marketing initiatives. The entire CleverTap dashboard can be filtered by any segment you create, including any of our analytics features.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a2d5bd-Segment_List_Page.gif",
        null,
        "Segment List"
      ],
      "align": "center",
      "border": true,
      "caption": "View List of Created Segments"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "<p>Field</p>",
    "h-1": "<p>Description</p>",
    "0-0": "<p>Segment details</p>",
    "0-1": "<p>Displays the details like segment name, ID, and email ID of the user who created the segment.</p>",
    "1-0": "<p>Type</p>",
    "1-1": "Displays the type of segment. The following are the options available:  \n  \n<li>Past Behavior Segment</li><li>Live User Segment</li><li>Custom List Segment</li><li>Partner Segment (where Partner Name can be Amplitude, Mixpanel)</li>",
    "2-0": "<p>Created on</p>",
    "2-1": "<p>Displays the date on which the segment was created.</p>",
    "3-0": "<p>Updated on</p>",
    "3-1": "<p>Displays the date on which the segment was last updated.</p>",
    "4-0": "<p>Updated by</p>",
    "4-1": "<p>Displays the email ID of the user who last updated the segment.</p>",
    "5-0": "<p>Goals</p>",
    "5-1": "<p>Displays the number of goals that are running on the segment.</p>",
    "6-0": "<p>IBS Goals</p>",
    "6-1": "<p>Displays the number of goals running with Intent-Based Segment.</p>",
    "7-0": "<p>Engagement</p>",
    "7-1": "<ul><li>Displays the number of active and scheduled customer engagements such as campaigns and journeys that use the segment within <a href=\"doc:segments#include-and-exclude-segments\">include/exclude</a> filters.</li><li>On clicking the number, it displays the list of campaigns and journeys where the segment is being used. You can also click on a particular campaign/journey from this list to view the campaign details.</li></ul>",
    "8-0": "<p>Dependent Segments</p>",
    "8-1": "<ul><li>Displays the number of other segments that include or exclude the selected segment.</li><li>On clicking the number, it displays the list of segments that include/exclude the selected segment. You can also click on a particular segment from this list to view the segment details.</li></ul>"
  },
  "cols": 2,
  "rows": 9,
  "align": [
    "left",
    "left"
  ]
}
[/block]


# System User Segments

Before creating any segment on the CleverTap dashboard, there are default system segments already present on the dashboard. The following are the system-defined user segments that are available for your use: 

- **All Users**: This user segment contains all the users added to your project.
- **Test Users**: The Test User segment is a default user segment in CleverTap that businesses can use to test their campaigns, journeys, and product experiences before sending them to actual users. This segment allows businesses to experiment with new features, messaging, and campaigns in a safe and controlled environment. Using Test Users helps businesses measure the effectiveness of their ideas before rolling them out to a larger audience. Test Users can be manually created from the CleverTap dashboard or imported through a CSV file and segmented based on various criteria. For more information, refer to [Mark a User Profile as a Test Profile](doc:user-profiles#mark-a-user-profile-as-a-test-profile).

# Types of Segments

There are three types of segments in CleverTap, which are explained in the following sections:

- [Past Behavior Segments](doc:segments#past-behavior-segments)
- [Live User Segments](doc:segments#live-user-segments)
- [Custom List Segments](doc:segments#custom-list-segments)

## Past Behavior Segments

Past behavior segments include users grouped by their actions in the past. You can group users based on a single activity or do complex combinations of actions, inactions, and user properties.

For example, you can create a segment of users from California, who are females, launched the application in the last 30 days, and have not purchased anything from the app.

Past behavior segments can be based on:

- **Actions**: Add users to a segment if they have performed an event. For example, users who added a product to the cart in the past 30 days.
- **Inaction**: Add users to a segment if they have performed an event but did not perform another event within a certain time. For example, users who added a product to the cart but did not purchase in the last 30 days.
- **Actions with user properties**: Add users to a segment if they did or did not perform an event and have a common user property. For example, platinum-level users who added a product to the cart but did not purchase in the last 30 days.

## Live User Segments

While past behavior segments let you evaluate users based on historic criteria, live user segments let you track what is happening in your app right now. When you define a set of behaviors of interest, CleverTap monitors for these behaviors as they happen in your app and immediately adds a user to a segment the moment their behavior matches your action criteria. You can create live user segments for the following:

- **Single action**: Add users to a segment as soon as they perform an event. For example, users who booked a movie ticket from your app.
- **Inaction within time**: Add users to a segment when they perform a particular event but did not perform another event within a certain time. For example, users who have added a product to the cart but did not purchase it within 10 minutes of adding the product to the cart.
- **On a date/time**: Add users to a segment based on date and time property value. For example, users who have an appointment five days from the current date.
- **Page visit**: Add users to a segment as soon as they visit a specific URL on your website. For example, users who have visited the Resources page of your website.
- **Referrer entry**: Add users to a segment based on a referring website or campaign. For example, users who have visited your website via a specific external referrer URL.
- **Page count**: Add users to a segment based on the number of pages visited by them. For example, users who have visited five web pages on your website.

## Custom List Segments

A custom list segment is a list of users from any source, including third-party tools or internal databases. You can deliver personalized messages to these users based on their past or real-time behavior in the app. For more information, refer to [Custom List Segment](doc:custom-list-segments).

# Create Segments

The steps vary based on the type of segment you want to create.

## Create Past Behavior Segments

In this example, we can create an action-based segment where users will qualify if they have applied for a payment offer at least one time in the past 30 days.

To create a past behavior segment, perform the following steps:

1. Navigate to _Segments_ > _Segments_ from the dashboard.
2. Click **+Segment**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b89f6b6-Create_Segments.png",
        null,
        "Create a New Segment"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Segment"
    }
  ]
}
[/block]


3. Select the box _Actions_ underneath _Past behavior segments_ from the main segment creation page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e12f3df-Past_Behavior_Segments.png",
        null,
        "Past Behavior Segments"
      ],
      "align": "center",
      "border": true,
      "caption": "Past Behavior Segments"
    }
  ]
}
[/block]


4. Define the segment rule as shown below on the segment query page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6f6d353-Segments_PSB_Create_New.png",
        "Set Up Segment Options to Create a Past Behavior Segment",
        1228
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Past Behavior Segment"
    }
  ]
}
[/block]


5. Click **Save segment** and name the segment.

You can now view your new segment on the _Segment List_ page.

## Create Live User Segments

In this example, we can create an _Inaction within time_ segment for which users will qualify in real-time as soon as they add a product to their cart but do not purchase the product within 10 minutes.

> 📘 Golden Window for Mobile Transactions
> 
> The golden window within which most users transact on our iOS and Android app platforms is within 10 minutes.

To create a live segment with CleverTap, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Click **+ Segment**.
3. Under _Live user segments_, select the _Inaction within time_ box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21b8b4d-Inaction_Within_Time_Segment.png",
        null,
        "Create Live User Segment"
      ],
      "align": "center",
      "border": true,
      "caption": "Live User Segments"
    }
  ]
}
[/block]


4. Select the appropriate properties for your live user segment. 

You may choose to select the _Filter on past user behavior and common properties_ checkbox to apply past action, inaction, or common user property filters.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/033db1c-2_set_up_Live_user_segment_-_Inaction_within_time.png",
        "Set Up Segment Options and Click Save Segment",
        1403
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Live User Segment"
    }
  ]
}
[/block]


5. Click **Save segment** and name the segment.

> 📘 Segment Naming Best Practices
> 
> Convey the core meaning of the segment while keeping the name brief.

You can now see your new segment in the main section as _Added to cart but no charge within 10 minutes_.

# View Segment Details

To view segment details, navigate to _Segments_ > _Segments_, search for the segment you are looking for and then click on it. On clicking, segment details are displayed. At the top of the page, you can click _View segment definition_ to understand more about the underlying query.

## Past Behavior Segment Details

The top portion of the past behavior user segment report consists of a way to first view the segment definition to understand its underlying query. There are graphs on the left-hand side showing the plot of the number of users who qualified for the segment going forward from the first complete day post-segment creation. The list on the right-hand side shows the sample list of users who qualified for the segment on this day.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1225063-report.png",
        "View Segment Trend Report",
        1204
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Trend"
    }
  ]
}
[/block]


The past behavior segment statistics are computed daily. However, when these segments are used in campaigns, the users who qualify for these segments are computed in real time. This ensures that users meeting the segment criteria during campaign execution reflect the most recent user activity data.

The lower portion of the past behavior segment report consists of reachability percentages for these users within each messaging channel. The lower-most part of the report shows you how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f416de-lower_report.png",
        "View Segment Size and Reachability Report",
        1206
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Size and Reachability"
    }
  ]
}
[/block]


## Live User Segment Details

To view a live user segment report, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Search for the segment you are looking for, then click on it.  

At the top of the report, you can click _View segment definition_ to understand more about the underlying query. 

The two graphs describe the following:

- The left-hand side shows the plot of the number of users who qualified for the segment going forward from the first complete day after creating the segment.
- The right-hand side shows the real-time rate at which users are qualifying for the segment vs. all user activity on your app/website. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/821380f-4a_top_report.png",
        "View Live User Segment Reports",
        1272
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Reports"
    }
  ]
}
[/block]


- The lower portion of the live user segment report consists of a list of sample users trickling into your segment in real time on the right-hand side. It also shows the reachability percentages for these users within each messaging channel on the left-hand side.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25d5194-4b_middle_report.png",
        "View Segment Size and Reachability",
        1269
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Size and Reachability"
    }
  ]
}
[/block]


- The lower-most part of the report shows how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44308a1-4c_bottom_report.png",
        "View Sample Users for an Event",
        1266
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Users"
    }
  ]
}
[/block]


# Export Users in a Segment

CleverTap allows you to export the users from any segment in the CSV format. To do so:

1. From the _Segments_ page, select the segment from which you may want to export the users. You can also filter out the segments using the _Type_ and _Goals_ filters. The page opens where all the segment details are displayed.
2. Scroll down and navigate to the _Sample users_ section and click **Download**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/00397d4-small-Download_All_Users.png",
        null,
        "Download Sample Users"
      ],
      "align": "center",
      "border": true,
      "caption": "Download Sample Users"
    }
  ]
}
[/block]


3. Select the fields you want to export and click **Proceed**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4cab592-small-Include_the_Required_Fields_and_Click_Proceed.png",
        null,
        "Select the User Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Select the User Details"
    }
  ]
}
[/block]


> 📘 Mismatch in Segment Size and Number of Users Exported to CSV File
> 
> The number of users displayed under the _Segment size and reachability_ section may vary from the number of users exported to the CSV file. This variation is due to the inclusion of blacklisted users under the _Segment size and reachability_ section.

# View Analytics Filtered by Segment

Under the _Do more with this segment section,_ you have the option to view an analytics report. This is for the chosen segment alone and not your entire user base. 

Real-time dashboard views such as the _Today_ dashboard only enable filtering by live user segments. Analytics based on past behavior such as mobile app, revenue, funnels, cohorts, trends, and events will only enable filtering their stats by past behavior segments.

# Create Campaigns for a Chosen Segment

Under the _Do more with this segment_ section, under _Engage_, you have the option to create a campaign to message a specific segment.

This immediately takes you to the messaging channel with your segment criteria pre-populated in the target.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c7905e-Segments_Do_More_Campaign.png",
        "Click Campaign from the Do More with this Segment option",
        617
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Campaign from the Segment"
    }
  ]
}
[/block]


# Include and Exclude Segments

You can simplify complex queries by including or excluding the existing user segments. Create segments with complex conditions once and then reuse them in different scenarios. 

You can create powerful segmentation that is valid for a variety of scenarios. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30d054b-0fd3c96-Find_people_include_exclude_segments.png",
        "Create Segments with Complex Conditions",
        715
      ],
      "align": "center",
      "border": true,
      "caption": "Include and Exclude Segments"
    }
  ]
}
[/block]


## Exclude Segments

There may be instances when you want to exclude some users based on specific criteria. 

For example, you want to offer discounts to all the users who have expressed interest by adding the product to the cart in the past 30 days; however, you want to save your engagement dollars by excluding the power users.  
The parameters for these power users can be the following:

- Users who have charged three times in the past three months, and 
- Users who have launched the app 15 times in the past month, and
- Users who rated a product 10 times in the past year

Now, you can create a segment with these criteria called _Power Users_ and use it every time rather than creating a complex query each time. You can save all these parameters in a segment called _Power Users_ and exclude them from the discount message. 

The following is a campaign query for an e-commerce app that excludes the _Power Users_ segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2fb7f6a-exclude_segments_campaign.png",
        "Set Up the Options to Exclude a Segment from Campaign",
        1050
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Exclude Segments"
    }
  ]
}
[/block]


## Include Segments

There may be instances when you want to include some users based on specific criteria. 

Consider the example of a ride-hailing app. You want to nudge your users to enroll for a monthly pass as soon as they open the app. The parameters for these users can be the following:

- The users must be power users, and
- The users have booked more than five rides in a month, and
- They belong to select cities in the country

Now, you can create a segment with these criteria called _Power Users_ and using it repeatedly rather than creating a complex query each time. 

The following is a campaign query for a ride-hailing app that includes the _Power Users_ segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f9f341a-include_segments_campaign.png",
        "Set Up the Options to Include a Segment from Campaign",
        1067
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Include Segment"
    }
  ]
}
[/block]


> 📘 Include and Exclude Segments
> 
> - You can include and exclude segments in the same query. It is considered as an _AND_ condition between the Included and the Excluded segments.
>   - The include and exclude segments are currently unavailable for bulletins and A/B Testing.
>   - The segments available for including or excluding users can only be of the type [PBS](doc:segments#section-past-behavior-segments) segment.

# Additional AND By Behavior Filters

_AND By behavior_ filters provide customers the ability to segment users based on the count, average, or total sum of a property value.

### Count

The count filter allows customers to filter users by event count. The query finds all users who performed a _Charged_ event greater than 5 times in the past 30 days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0678593-2020-11-24_17-51-01_Count.png",
        "Select Count to Filter Users by Count",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "Count Filter"
    }
  ]
}
[/block]


### Average of Property Filter

The _Average of property_ filter allows customers to filter users by the average of a chosen event property. The query finds all users who performed a _Charged_ event such that the average _Revenue_ event property per event is greater than $10. 

The _Average of property_ filter allows averaging the value of the selected event property. For example, you can find out the average revenue earned from all users who performed purchases worth $10 or less. Let us assume that 5 users charged for each for $3, $5, $7, $2, and $8. The average value of all the purchases lower than $10 is ($ 3+ 5 +7+2+8)/5 events = 25/5= $5 per event. 

Let us assume that the value for 2 charged events is missing. The charged event values received are $3, $5, and $7. The value of the missing events will be considered as 0. The average of property is now ($3 + 5 +7 +0 +0)/5 events = 15/5 =$3 per event. 

If you want to exclude all the events that do not have event properties, you can select the property that exists a condition in the _Filter by_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09c3239-2020-11-24_17-52-22_Average_of_property.png",
        "Select Average of Property Filter",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "Average of Property Filter"
    }
  ]
}
[/block]


### Total Sum of Property

The _Total sum of property_ filter allows customers to filter users by the sum of a chosen event property. The query finds all users who performed a _Charged_ event such that the _Revenue_ event property is greater than $10.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d973ab4-2020-11-24_17-53-50_Total_sum_of_property.png",
        "Select Total Sum of Property Filter",
        1194
      ],
      "align": "center",
      "border": true,
      "caption": "Total Sum of Property Filter"
    }
  ]
}
[/block]


> 📘 Include Users Who Did Not Do the Event
> 
> If the query is to find people who performed the charged event fewer than five times, by default, the users who have not performed the charged event are not included in the result set. Only the users who did the charged event but did it fewer than five times are included; however, if the checkbox for _Include users who didn’t do the event_ is selected, those users are also included in the result set. The same is true for sum and average.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db44a26-2020-11-24_17-56-46_Checkbox_message.png",
        "Select the Checkmark to Include Users Who Did Not Do an Event",
        1187
      ],
      "align": "center",
      "border": true,
      "caption": "Include Users Who Did Not Do an Event"
    }
  ]
}
[/block]


# Segment Operations

You can perform different actions on the segments from the _Segments_ page. Each of them is explained in the sections to follow

## Search Segment

You can search segments by their Name or ID from the _Segments_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1251882-Search_Segment.png",
        "Search Segment.png",
        2396
      ],
      "align": "center",
      "border": true,
      "caption": "Search a Segment"
    }
  ]
}
[/block]


## Copy Segment Name and ID

To copy segment name and ID:

1. From _Segments_ page, hover on the _name_ or _ID_ of the required segment.
2. Click the ![Copy](https://files.readme.io/0e1c106-Copy_icon.png) icon against the respective segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0455ea5-Copy_Segment_name_and_ID_.png",
        "Copy Segment name and ID .png",
        2402
      ],
      "align": "center",
      "border": true,
      "caption": "Copy a Segment Name and ID"
    }
  ]
}
[/block]


## Engage with Segment

To engage with a segment directly from the _Segments_ page:

1. Click ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the _Segment details_ column and click **Engage**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e73666c-Engage_from_Segments_page.png",
        "Engage from Segments page.png",
        2394
      ],
      "align": "center",
      "border": true,
      "caption": "Engage with a Segment"
    }
  ]
}
[/block]


   On clicking, _Messaging Channels_ popup displays.

2. Select the _Messaging Channel_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6d679c6-Messaging_Channels_popup.png",
        "Messaging Channels popup.png",
        2376
      ],
      "align": "center",
      "border": true,
      "caption": "Select a Messaging Channel"
    }
  ]
}
[/block]


On selecting the channel, you are navigated to the messaging channel with your segment criteria pre-populated under the _Who_ section of the _New Campaign_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ebf6d1-Who_section_prepopulated.png",
        "Who section prepopulated.png",
        2752
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Campaign"
    }
  ]
}
[/block]


## Clone a Segment

This operation helps to create a new segment from an already existing segment with minor or no modifications to the qualification criteria of the segment. To clone a segment directly from the _Segments_ page:

1. Click the ![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the _Segment details_ column and click **Clone**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3fba76-Clone_Segment.png",
        "Clone Segment.png",
        2394
      ],
      "align": "center",
      "border": true,
      "caption": "Clone a Segment"
    }
  ]
}
[/block]


  On clicking, the _Create New_ page opens with prepopulated qualification criteria.

2. Make the necessary modifications to the qualification criteria, if required.
3. Click **Save segment**.
4. Enter the _Segment name_ and click **Save**.

## Delete

There may be times when you may need to delete unused segments. To delete the unused segments:

1. Click![Ellipses](https://files.readme.io/b15093f-ellipses_icon.png) icon displayed against the segment name under the _Segment details_ column and click **Delete**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9ab0c2-Delete_Segment.png",
        "Delete Segment.png",
        2394
      ],
      "align": "center",
      "border": true,
      "caption": "Delete a Segment"
    }
  ]
}
[/block]


On clicking, the _Delete Segment?_ popup is displayed on the right side of the screen.

2. Click **Delete** to confirm your action.

> 📘 Note
> 
> If your account's total number of segments exceeds 1000, you can view up to 500 segments on a single page and delete a maximum of 500 segments at a time. If the number of segments is less than 1000, you can view up to 50 segments on a single page and delete a maximum of 50 segments at a time.

## Sort

You can sort segments based on the following columns under _Segments_ page by clicking the arrows against the respective columns :

- Segment details
- Created on
- Updated On
- Engagement
- Dependent Segments

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ab3b2c8-Sort_Segments.gif",
        "Sort Segments.gif",
        1188
      ],
      "align": "center",
      "border": true,
      "caption": "Sort Segments"
    }
  ]
}
[/block]


## Filter Segments

You can filter out segments based on the following fields by clicking the ![Filter](https://files.readme.io/9cb6680-Filter_icon.png) icon:

- Type: Indicates the type of segment. 
- Goals. Indicates the goals running on the segment.
- Created by: Indicates the name of the user who created the segment.
- Updated by: Indicates the name of the user who last updated the segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2382971-Filter_Segments.gif",
        "Filter Segments.gif",
        1196
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Segments"
    }
  ]
}
[/block]


You can also filter segments based on the date on which the segments were created. To do so, select the date range, available at the top, for which you want to view the segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a92678-Filter_Segments_by_creation_date.png",
        "Filter Segments by creation date.png",
        2398
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Segments by Date"
    }
  ]
}
[/block]