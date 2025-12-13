---
title: Segment.io Export
excerpt: Customer Data Platform
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

[Segment.io](https://www.segment.io/), a Customer Data Platform service provider, provides the capability that simplifies collecting and using data from the users of your digital properties (websites, apps, etc.). With Segment, you can collect, transform, send, and archive your first-party customer data.

# Integrate Segment with CleverTap

This process involves the following two steps:

1. [Find Segment Project Details](doc:segmentcom-export#find-segment-project-details).
2. [Configure CleverTap Dashboard](doc:segmentcom-export#configure-clevertap-dashboard).

## Find Segment Project Details

To find your project details:

1. From your workspace, navigate to _Connections_ > _Catalog_.
2. Search for _CleverTap_ in the _Sources Catalog_, select _CleverTap_, and click **Add Source**.
3. Enter a nickname for the _Source_ and configure any other required settings. The nickname is used as a label in the Segment app, and Segment creates a related schema name in your warehouse. The nickname can be anything, but Segment recommends using something that reflects the source itself and distinguishes amongst your environments (like CleverTap_Prod, CleverTap_Staging, or CleverTap_Dev).
4. Click **Add Source** to save your settings.
5. Copy the _Write key_ from the Segment dashboard. You will need it when configuring the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5dbbd2-Segment.io_export_setup.gif",
        null,
        "Find Segment.io Project Details "
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

1. Log in to your CleverTap account and navigate to the _Settings_ > _Partners_ page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa0c666-Navigating_to_Partners_page.png",
        null,
        "Navigating to Partners Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Navigating to Partners Page"
    }
  ]
}
[/block]

2. Hover on the _Segment_ icon and click **Integrate**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/115f8f4-Integrate_Segment.png",
        null,
        "Integrate Segment"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate Segment"
    }
  ]
}
[/block]

   On clicking, _Integrate raw data partner - Segment_ popup opens on the right side of the screen.

3. Enter the following details and click **Integrate**. 

| Field            | Description                                                                                                                                                                                             |
| :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Partner Nickname | Enter the _Nickname_ for your integration.                                                                                                                                                              |
| Write Key        | Helps identify CleverTap as a unique data source on Segment. For more information about obtaining the key, refer to [Find Segment Project Details](doc:segmentcom-export#find-segment-project-details). |
| Region           | <li> Enter the region of your Segment account. </li> <li>The following are the two options: <ul> <li> US Region (default) </li> <li> EU Region </li> </ul></li>                                         |
| User ID          | Used as an identifier to track the user on Segment.                                                                                                                                                     |
| Anonymous ID     | Used as an identifier to track anonymous user on Segment.                                                                                                                                               |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/52a3e03-Enter_mParticle_Project_Details_to_Integrate.png",
        null,
        "Enter Segment Project Details to Integrate"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Segment Project Details to Integrate"
    }
  ]
}
[/block]

   After successful integration, the _Integrated_ tag displays against _Segment_ on the _Partner List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/130f8fc-Segment_Integration_Successful.png",
        null,
        "Segment Integration Successful"
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Integration Successful"
    }
  ]
}
[/block]

# Create New Export

To create a new export:

1. Navigate to _Settings_ > _Partners_ > _Exports_ from the CleverTap dashboard.
2. Click **+ Export** and select _Segment_ from the _Partners_ list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ed14f8-Create_Export.png",
        null,
        "Create Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]

On clicking, the _Export to Segment_ pop-up displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6329f3c-Enter_Export_Details.png",
        null,
        "Enter Export Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Export Details"
    }
  ]
}
[/block]

3. Configure the following settings:
   - **Type**: Select the type of data that you want to export from the available options. For more information, refer to [Export Details](doc:segmentcom-export#export-details).
   - **Frequency**: Select from one of the following options:
     - _Once only_: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     - _Recurring_: Set up a recurring frequency to export all the new events/user properties captured in the last window. You can export event data as frequently as every 4 hours and up to once every 24 hours. You can export user properties only once every 24 hours. 
4. Click **Export**. The _Segment export has initiated_ message displays at the top of the _Exports_ page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/798a9f1-Segment_Export_Initiated.png",
        null,
        "Segment Export Initiated"
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Export Initiated"
    }
  ]
}
[/block]

CleverTap processes the export, and you can now see the newly-created export for Segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b054bdd-New_Segment_Export_Displays_on_Exports_Page.png",
        null,
        "New Segment Export Displays on Exports Page"
      ],
      "align": "center",
      "border": true,
      "caption": "New Segment Export Displays on Exports Page"
    }
  ]
}
[/block]

The status for each export is displayed as _Pending_ as soon as the export is created. The status changes to _Running_ after the processing starts. And it changes to _Done_ when the export is complete.

# Stop Export

You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/437ad4c-Stop_export_icon.png) icon for the export request you want to stop and then click **Stop** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a00ffe-Stop_Segment_Export.png",
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

You are navigated back to the _Exports_ page, and the _Segment data export stopped_ message displays at the top. The status for the data export now displays as _Stopped_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/abcf4ff-Segment_Data_Export_Stopped.png",
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

# Export Details

Select from one of the following options to export events from CleverTap to the Segment dashboard:

- [All events](doc:segmentcom-export#all-events)
- [Selected events](doc:segmentcom-export#selected-events)
- [Engagement events](doc:segmentcom-export#engagement-events)

## All Events

When you select this option, the following defined system events are exported:

| CleverTap Event Name       | Event Description                                                                                                                                                                                                                            |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Notification Sent          | The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.                                                                                                    |
| Notification Viewed        | This event is tracked when a user views an email, in-app notification, or web notification sent from CleverTap.                                                                                                                              |
| Notification Clicked       | This event is tracked only when a user clicks on a notification sent via CleverTap.Recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API. |
| Push Impressions           | This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.                                                                                                                                          |
| Notification Replied       | This event is recorded when a user replies to a WhatsApp message.                                                                                                                                                                            |
| Control Group              | The event is raised when a campaign is activated with a Control group.                                                                                                                                                                       |
| Channel Unsubscribed       | The event is raised when a user Unsubscribes to receive further communication through a channel                                                                                                                                              |
| Push Impressions           | This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.                                                       |
| AB Experiment Stopped      | This event is recorded when the A/B experiment is stopped.                                                                                                                                                                                   |
| AB Experiment Rolled Out   | This event is recorded when the A/B experiment is started                                                                                                                                                                                    |
| AB Experiment Disqualified | This event is raised when the device is disqualified.                                                                                                                                                                                        |
| Geocluster Entered         | This event is recorded to mark when a device enters a geofence.                                                                                                                                                                              |
| Geocluster Exited          | This event is recorded to mark when a device exits a geofence.                                                                                                                                                                               |
| Reply Sent                 | This event is recorded when an agent (CleverTap user) replies to a message from the end user.                                                                                                                                                |
| App Version Changed        | This event is raised when a user’s current app version is different from the user’s previous app version.                                                                                                                                    |
| App Launched               | This event is recorded every time a user launches your application.                                                                                                                                                                          |
| App Installed              | The event is raised when the user launches the app for the first time.                                                                                                                                                                       |
| App Uninstalled            | This event is recorded when a user uninstalls your application.                                                                                                                                                                              |
| UTM Visited                | This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.                                                                                                                         |

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