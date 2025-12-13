---
title: Amplitude Export
excerpt: Analytics Partner
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

[Amplitude](https://amplitude.com/), an analytics and business intelligence platform, helps make informed decisions for targeting users. Integration CleverTap with Amplitude allows you to export your CleverTap event data to your Amplitude dashboard. You can use this event data for further analysis.

# Integrate Amplitude with CleverTap

This process involves the following two steps:

1. [Find Amplitude Project Details](doc:amplitude-export#find-amplitude-project-details).
2. [Configure CleverTap Dashboard](doc:amplitude-export#configure-clevertap-dashboard).

## Find Amplitude Project Details

1. Log in to your Amplitude account.
2. Navigate to the _Settings_ page. 
3. Navigate to _Org Settings_ > _Projects_. 
4. Click on a project to find the _API Key_ under the _General_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75bc618-Finding_API_key.png",
        "Finding API key from the Amplitude Dashboard",
        3552
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Finding API Key"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Partners_ > _Partner List_ from the CleverTap dashboard. Select _Amplitude_ from the list.

   [block:image]{"images":[{"image":["https://files.readme.io/b728365fdcad7a78f12a72361bc625a502910e436d5a46f097420fdd7257643e-Amplitude_Partner_Page.png","","Navigate to the Partner Page"],"align":"center","border":true,"caption":"Navigate to the Partner Page"}]}[/block]
2. A popup opens on the right side of the screen. Enter the following details and click **Integrate**:

| <p>Field</p>            | <p>Description</p>                                                                                                                                                                                                  |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p>Partner Nickname</p> | <p>Enter the <em>Nickname</em> for your integration.</p>                                                                                                                                                            |
| <p>API key</p>          | <p>The unique code for Amplitude to verify your credentials. For more information about obtaining the key, refer to <a href="doc:amplitude-export#find-amplitude-project-details">Find Amplitude Details</a>.</p>   |
| <p>Data Residency</p>   | <p>The Data Residency is the physical/geographical storage location of data for each project. </p><ul><li>Select from the following available options:<ul><li>Europe (default)</li><li>Standard</li></ul></li></ul> |
| Device ID Mapping       | This field is mapped to Amplitude's `device_id` field for identification when sending data from CleverTap to Amplitude.                                                                                             |
| User ID Mapping         | This field is mapped to Amplitude's `user_id` field for identification when sending data from CleverTap to Amplitude.                                                                                               |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fe4633-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true
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
        "https://files.readme.io/d6bfc1f64309cb1a4d596818e2a141699c5ae32d7ddc9c141200df7da5218ad7-Amplitude_Export.png",
        "",
        ""
      ],
      "align": "center",
      "border": true,
      "caption": "Amplitude Export"
    }
  ]
}
[/block]


# Create New Export

This section lists steps to create a new export from the CleverTap dashboard.

To create a new export:

1. Navigate to **Settings** > **Partners** > **Exports** from the CleverTap dashboard.
2. Click **Create Export** and select **Amplitude**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa7e1ef-image.png",
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


The **Export to Amplitude** window displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5331f5-image.png",
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
   - **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. For more information, refer to [Export Details](doc:amplitude-export#export-details).
   - **FREQUENCY**: Select from one of the following options:
     - **One time**: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     - **Recurring**: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
     - **Date to export data**: The export starts at 12:00 a.m. on the specified date by default.
4. Click **Export**. The **Export to Amplitude** window closes, and the following message displays at the top of the _Exports_ page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/333f81c-image.png",
        null,
        "Amplitude Export Initiated"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Amplitude Export Initiated"
    }
  ]
}
[/block]


CleverTap processes the export, and you can now see the newly created export for Amplitude.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f58b2f-image.png",
        null,
        "New Amplitude Export Displays on Export Page"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "New Amplitude Export Displays on Export Page"
    }
  ]
}
[/block]


The status for each export is displayed as **PENDING** as soon as the export is created. The status changes to **RUNNING** after the processing starts. In the case of **One time** export, the status changes to **DONE** when the export is complete.

# Stop Export

You can also stop the export that you have created. Hover over the export. The **Stop** button appears. Click the **Stop**  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19237ef-image.png",
        null,
        "Stop Amplitude Export"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Stop Amplitude Export"
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
        "https://files.readme.io/7067554-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true
    }
  ]
}
[/block]


You now return to the **Exports** page, and the _Amplitude data export stopped_ message displays at the top. The status of the export is displayed as **STOPPED**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e8ff5a-AmplitudeStopped.jpg",
        null,
        "Amplitude Export Stopped"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Amplitude Export Stopped"
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
        "https://files.readme.io/7e95e07-EditAmplitudeExport.jpg",
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


3. Click the **Edit** button. The **Export to Amplitude** section appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/945fb85-UpdateAmplitudeExport.jpg",
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

> 📘 Modify Export Frequency
> 
> When you change the export frequency, the export cycle resets and begins at midnight (12:00 a.m.) on the specified date following the new schedule.
> 
> For example, if the last export occurred at 4:00 p.m., the next export cycle will start at midnight (12:00 a.m.) and continue according to the new 12-hour schedule thereafter.

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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74ce34b-Amplitude_Exports_-_Calendar_Widget.png",
        "",
        "Calendar Widget"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Calendar Widget"
    }
  ]
}
[/block]


1. Choose the custom date range and click **Apply**.  
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Options include 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

# Export Details

Select from one of the following options to export events from CleverTap to the Amplitude dashboard:

- [All events](doc:amplitude-export#all-events)
- [Selected events](doc:amplitude-export#selected-events)
- [Engagement events](doc:amplitude-export#engagement-events)

## All events

Export data for all defined events, including System and Custom events.

## Selected events

Select the specific events you want to export from CleverTap to the Amplitude dashboard.

## Engagement Events

Select this option to export the following engagement events:

| <p>CleverTap Event Name</p> | <p>Event Description</p>                                                                                                                                                                                                                                                                                                                                                |
| :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Notification Sent</p>    | <p>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.</p>                                                                                                                                                                                                                        |
| <p>Notification Viewed</p>  | <p>This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.</p>                                                                                                                                                                                                                                                |
| <p>Notification Clicked</p> | <p>This event is tracked only when a user clicks on a notification sent via CleverTap. It is recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API.</p>                                                                                                              |
| <p>Push Impressions</p>     | <p>This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.</p>                                                                                                                                                                                                                                                              |
| <p>Notification Replied</p> | <p>This event is tracked when a user replies to a WhatsApp message.</p>                                                                                                                                                                                                                                                                                                 |
| <p>Push Unregistered</p>    | <p>The event is raised when the user unregisters to receive Push Notifications.</p>                                                                                                                                                                                                                                                                                     |
| <p>Control Group</p>        | <p>The event is raised when a campaign is activated with a Control group.</p>                                                                                                                                                                                                                                                                                           |
| <p>Channel Unsubscribed</p> | <p>The event is raised when a user unsubscribes to receive further communication through a channel.</p>                                                                                                                                                                                                                                                                 |
| <p>Reachable By</p>         | <ul><li>The debug event is raised when the user becomes reachable by a communication channel such as SMS, email, or mobile push, or when there are changes to the existing communication channel.</li><li>Tracked for a profile when:<ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed.</li></ul></li></ul> |
| Push Impressions            | This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.                                                                                                                                                                                  |
| Notification Delivered      | This event is recorded when communication is delivered to the user's device                                                                                                                                                                                                                                                                                             |
| AB Experiment Rendered      | This event is recorded when communication is delivered to the user who is part of an A/B experiment campaign                                                                                                                                                                                                                                                            |
| AB Experiment Stopped       | This event is recorded when AB experiment is stopped.                                                                                                                                                                                                                                                                                                                   |
| AB Experiment Rolled Out    | This event is recorded when AB experiment is started                                                                                                                                                                                                                                                                                                                    |
| Geocluster Entered          | This event is recorded to mark when a device enters a geofence.                                                                                                                                                                                                                                                                                                         |
| Geocluster Exited           | This event is recorded to mark when a device exits a geofence.                                                                                                                                                                                                                                                                                                          |
| Reply Sent                  | This event is recorded when an agent (CleverTap user) replies to a message from the end-user.                                                                                                                                                                                                                                                                           |
| App Uninstalled             | This event is recorded when a user uninstalls your application.                                                                                                                                                                                                                                                                                                         |
| Webhook Delivered           | This event is recorded when a Webhook campaign is delivered successfully                                                                                                                                                                                                                                                                                                |
| State Transitioned          | This event is recorded for Lifecycle Optimizer when a user transitions from one stage to another.                                                                                                                                                                                                                                                                       |
| UTM Visited                 | This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.                                                                                                                                                                                                                                                    |

# FAQs

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

- CleverTap's export system supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
- It replaces the following characters with a hyphen to avoid issues in output file generation:
  - Whitespace
  - Tab
  - Slash
  - null (\\0)
- Control characters are replaced with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
- Supports emoji characters; however, some emojis (UTF-16) may not render properly.