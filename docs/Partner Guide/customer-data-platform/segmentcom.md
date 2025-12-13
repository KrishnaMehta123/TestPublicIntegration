---
title: Segment
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

[Segment.io](https://www.segment.io/), a Customer Data Platform service provider, provides the capability that simplifies collecting and using data from the users of your digital properties (websites, apps, and so on). With Segment, you can collect, transform, send, and archive your first-party customer data.

# Integrate Segment with CleverTap

This process involves the following two steps:

1. [Find Segment Project Details](doc:segmentcom#find-segment-project-details).
2. [Configure CleverTap Dashboard](doc:segmentcom#configure-clevertap-dashboard).

## Find Segment Project Details

To find your project details:

1. From your Segment.io workspace, navigate to _Connections_ > _Catalog_.
2. Search for _CleverTap_ in the _Sources Catalog_, select _CleverTap_, and click **Add Source**.
3. Enter a nickname for the _Source_ and configure any other required settings. The nickname is used as a label in the Segment app. And, Segment creates a related schema name in your warehouse. Segment suggests using a nickname that reflects the source and distinguishes environments, such as CleverTap_Prod, CleverTap_Staging, or CleverTap_Dev, though it can be anything.
4. Click **Add Source** to save your settings.
5. Copy the _Write key_ from the Segment dashboard. You will need it when configuring the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5dbbd2-Segment.io_export_setup.gif",
        null,
        "Find Segment.io Project Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Find Segment.io Project Details "
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Log in to your CleverTap account and navigate to the _Settings_ > _Partners_  > _Partner List_ page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6c967ddd3f9eee2a9193ad11be6350936955c4520d83dfc78aa760161bc1908-Amplitude_Partner_Page.png",
        "",
        "Navigating to the Partners Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Navigating to the Partners Page"
    }
  ]
}
[/block]


2. A popup opens on the right side of the screen. Enter the following details and click **Integrate**.

| Field            | Description                                                                                                                                                                                      |
| :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Partner Nickname | Enter the _Nickname_ for your integration.                                                                                                                                                       |
| Write Key        | Helps identify CleverTap as a unique data source on Segment. For more information about obtaining the key, refer to [Find Segment Project Details](doc:segmentcom#find-segment-project-details). |
| Region           | <li> Enter the region of your Segment account. </li> <li>The following are the two options: <ul> <li> US Region (default) </li> <li> EU Region </li> </ul></li>                                  |
| User ID          | Used as an identifier to track the user on Segment.                                                                                                                                              |
| Anonymous ID     | Used as an identifier to track anonymous users on Segment.                                                                                                                                       |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4c2cbe-image.png",
        null,
        "Enter Segment Project Details to Integrate"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Enter Segment Project Details to Integrate"
    }
  ]
}
[/block]


After successful integration, navigate to the the _Export_ tab on the _Partner List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f5d3ecc2c92b80b30482f24fb853f96fe35652b1904cdad1c44d7085523bb56-Segment_export.png",
        "",
        ""
      ],
      "align": "center",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]


# Create New Export

To create a new export:

1. Navigate to **Settings** > **Partners** > **Exports** from the CleverTap dashboard.
2. Click **Create Export** and select **Segment**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6d2c8e1-CrteateSegmentExport.jpg",
        null,
        "Create Export"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]


The **Export to Segment** pop-up displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/48f4063-ExportToSegment.jpg",
        null,
        "Enter Export Details"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Enter Export Details"
    }
  ]
}
[/block]


3. Configure the following settings:
   - **Partner Nickname**: Nickname for the partner. To edit the nickname, go to **Partner List**. 
   - **DATA TYPE & IDENTIFIER PRIORITY**: Select the type of data that you want to export from the available options. For more information, refer to [Export Details](doc:segmentcom#export-details).
   - **FREQUENCY**: Select from one of the following options:
     - **One time**: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     - **Recurring**: Set up a recurring frequency to export all the new events at regular intervals. You can export event data as frequently as every 4 hours and up to once every 24 hours.
     - **Date to export data**: The export starts at 12:00 a.m. on the specified date by default.
4. Click **Export**. The _Segment export has initiated_ message displays at the top of the **Exports** page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7fea73f-SegementExportInitiated.jpg",
        null,
        "Segment Export Initiated"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Segment Export Initiated"
    }
  ]
}
[/block]


CleverTap processes the export, and you can now see the newly created export for Segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37a6b4f-SegmentPending.jpg",
        null,
        "New Segment Export Displays on Exports Page"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "New Segment Export Displays on Exports Page"
    }
  ]
}
[/block]


The status for a newly-created export is displayed as **PENDING**. The status changes to **RUNNING** after the processing starts and **DONE** when the export is complete.

# Stop Export

You can also stop the export that you have created. Hover over the export. Click the **Stop** ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a794b7-SegmentStopButton.jpg",
        null,
        "Stop Segment Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Stop Segment Export"
    }
  ]
}
[/block]


The **Stop export?** window appears. Click **Stop** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f596af9-StopSegmentWindow.jpg",
        "",
        ""
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true
    }
  ]
}
[/block]


You are navigated back to the **Exports** page, and the _Segment data export stopped_ message displays at the top. The status for the data export now displays as **STOPPED**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dda09e5-SegmentExportStopped.jpg",
        null,
        "Segment Export Stopped"
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Export Stopped"
    }
  ]
}
[/block]


# Edit an Export

You might need to modify an export to meet specific business requirements or while waiting for the next run. This section describes editing a Live Data Streaming and Recurring export in the **RUNNING** and **PENDING** (awaiting next run) state. 

> 📘 Points to Remember
> 
> - In case of running exports, the new changes will apply to the next run.
> - You cannot edit a One-time export, regardless its status (RUNNING, PENDING, DONE, or STOPPED).
> - You cannot change the export from User Profile to Event and vice-versa.
> - You cannot modify exports marked as **DONE** or **STOPPED**.
> - Export changes for Live DataStreaming take 10-15 minutes to take effect.

To edit an export: 

1. On the CleverTap dashboard, go to **Partners** > **Exports**.
2. Hover over the required export. The **View**, **Edit**, and the **Stop** buttons appear.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f78cd16-EditSegment.jpg",
        null,
        "Click the Edit Export Icon"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Click the Edit Export Icon"
    }
  ]
}
[/block]


3. Click the **Edit** button. The **Export to Segment** section appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3af3990-ClickUpdateExport.jpg",
        null,
        "Edit the Export"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Edit the Export"
    }
  ]
}
[/block]


4. Edit the export details and click **Update export**.

# Filter Exports

This section describes the different ways you can filter exports.

## Filter by Export Details

To filter by export details: 

1. Click the **Filter** button at the top right corner. 
2. You can filter exports by **Partner**, **Type**, **Format**, **Status**, or **Frequency**. 
3. To clear the filter, click **Reset all**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6499e90-FilterButton.jpg",
        "",
        "Filter Exports"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Filter Exports"
    }
  ]
}
[/block]


## Filter Exports by Date Range

You can also filter the exports based on the export date. 

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.  
   The **Calendar** widget appears. 

   [block:image]{"images":[{"image":["https://files.readme.io/0cf145e-CalendarWidget.jpg","",""],"align":"center","sizing":"80% ","border":true}]}[/block]
3. Choose the custom date range and click **Apply**.  
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Options include 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

# Export Details

Select from one of the following options to export events from CleverTap to the Segment dashboard:

- [All system events](doc:segmentcom#all-system-events)
- [Selected events](doc:segmentcom#selected-events)
- [Engagement events](doc:segmentcom#engagement-events)

## All System Events

When you select this option, the following defined system events are exported:

| CleverTap Event Name       | Event Description                                                                                                                                                                                                                                   |
| :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Notification Sent          | The event is tracked when the notification is successfully sent from CleverTap to the communication channel selected for your campaign.                                                                                                             |
| Notification Viewed        | This event is tracked when a user views an email, in-app notification, or web notification sent from CleverTap.                                                                                                                                     |
| Notification Clicked       | This event is tracked only when a user clicks on a notification sent via CleverTap. It is recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API. |
| Push Impressions           | This event is tracked when a Push notification sent from CleverTap is delivered to a user’s device.                                                                                                                                                 |
| Notification Replied       | This event is recorded when a user replies to a WhatsApp message.                                                                                                                                                                                   |
| Control Group              | The event is raised when a campaign is activated with a Control group.                                                                                                                                                                              |
| Channel Unsubscribed       | The event is raised when a user unsubscribes from any further communication through a channel                                                                                                                                                       |
| Push Impressions           | This event is tracked when a push notification sent from CleverTap is delivered to a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.                                                              |
| Session Concluded          | This event is recorded to mark the end of a session. Session tracking must be enabled for the event to be tracked.                                                                                                                                  |
| State Transitioned         | This is an event raised only for Lifecycle Optimizer. This event is recorded when a user transitions from one stage to another.                                                                                                                     |
| AB Experiment Rendered     | This event indicates that the variant has reached the device.                                                                                                                                                                                       |
| AB Experiment Stopped      | This event is recorded when the A/B experiment is stopped.                                                                                                                                                                                          |
| AB Experiment Rolled Out   | This event is recorded when the A/B experiment is started                                                                                                                                                                                           |
| AB Experiment Disqualified | This event is raised when the device is disqualified.                                                                                                                                                                                               |
| Geocluster Entered         | This event is recorded to mark when a device enters a geofence.                                                                                                                                                                                     |
| Geocluster Exited          | This event is recorded to mark when a device exits a geofence.                                                                                                                                                                                      |
| Reply Sent                 | This event is recorded when an agent (CleverTap user) replies to a message from the end user.                                                                                                                                                       |
| App Version Changed        | This event is raised when a user’s current app version is different from the user’s previous app version.                                                                                                                                           |
| App Launched               | This event is recorded every time a user launches your application.                                                                                                                                                                                 |
| App Installed              | The event is raised when the user launches the app for the first time.                                                                                                                                                                              |
| App Uninstalled            | This event is recorded when a user uninstalls your application.                                                                                                                                                                                     |
| UTM Visited                | This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.                                                                                                                                |

For more information about these events, refer to [Events](doc:events).

## Selected Events

With this option, you can select the specific system events (from those listed in the above table) that you want to export from CleverTap to the Segment dashboard.

## Engagement Events

When you select this option, the following engagement events are exported:

- Notification Sent
- Notification Viewed
- Notification Clicked
- Push Impressions
- Notification Replied
- Control Group
- Channel Unsubscribed
- Push Impressions
- Notification Delivered
- AB Experiment Rendered
- AB Experiment Stopped
- AB Experiment Rolled Out
- Geocluster Entered
- Geocluster Exited
- Reply Sent
- App Uninstalled
- Webhook Delivered
- State Transitioned
- UTM Visited

For more information about these events, refer to [Events](doc:events).