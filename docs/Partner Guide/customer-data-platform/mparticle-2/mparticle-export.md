---
title: mParticle Export
excerpt: Customer Data Platform
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

[mParticle](https://www.mparticle.com/) is a customer data platform that manages data quality and drives better customer interactions. Integrating CleverTap with mParticle allows you to export your CleverTap event data to your mParticle dashboard. You can use this event data for further analysis.

# Integrate mParticle with CleverTap

This process involves the following two steps:

1. [Find mParticle Project Details](doc:mparticle-export#find-mparticle-project-details).
2. [Configure CleverTap Dashboard](doc:mparticle-export#configure-clevertap-dashboard).

## Find mParticle Project Details

To find your project details:

1. Log in to your mParticle account.
2. Navigate to *Setup* > *Inputs* > *Feeds*.
3. Click **Add Feed Input** and select *CleverTap* from the dropdown list. The *Input: Feed Configuration* popup opens.

<Image title="Click Add Feed Input" alt={2862} align="center" width="90% " border={true} src="https://files.readme.io/d09bae1-Add_Feed_Input.png">
  Click Add Feed Input
</Image>

4. Enter the *Configuration Name* and turn **ON** the *Feed Status* toggle. 

<Image title="Enter Configuration Name and toggle ON Feed Status" alt={2818} align="center" width="90% " border={true} src="https://files.readme.io/1a0fc12-Feed_Config_popup.png">
  Enter Configuration Name and Toggle ON Feed Status
</Image>

5. Click **Save**. The *Server to Server Key* and *Server to Server Secret* are displayed.

<Image title="Copy Key and Secret for configuring the CleverTap dashboard" alt={2806} align="center" width="90% " border={true} src="https://files.readme.io/af1581a-Key_and_Secret_Details.png">
  Copy Project Details
</Image>

5. Copy the project details. You will need them when configuring the CleverTap dashboard.

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Log in to your CleverTap account and navigate to the *Settings* > *Partners* > *Partner List* page. Select *mParticle* from the list.

<Image alt="Navigating to the Partners Page" align="center" border={true} src="https://files.readme.io/0f5a42d7706085839929e3d0438c808e6922d942e85057213e91ee10ebceed88-Amplitude_Partner_Page.png">
  Navigating to the Partners Page
</Image>

2. A popup opens on the right side of the screen. Enter the following details and click **Integrate**.

| Field                  | Description                                                                                                                                                                                                              |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Partner Nickname       | Enter the *Nickname* for your integration.                                                                                                                                                                               |
| API key and API secret | These are the unique codes passed to mParticle to verify your credentials. For more information about obtaining the key, refer to [Find mParticle Project Details](doc:mparticle-export#find-mparticle-project-details). |
| Customer ID Mapping    | This is used as an identifier when sending event data to mParticle.                                                                                                                                                      |

<Image alt="Enter mParticle Project Details to Integrate" align="center" width="70% " border={true} src="https://files.readme.io/00f9e5c-image.png">
  Enter mParticle Project Details to Integrate
</Image>

After successful integration, navigate to the the *Export* tab on the *Partner List* page.

<Image alt="Create Export" align="center" src="https://files.readme.io/3a1ff088b8dcf9b0546a982453df0a38ef2b7f9bce04da79b28c9bda3692fefe-mparticle_export.png">
  Create Export
</Image>

# Create New Export

To create a new export:

1. Navigate to **Settings** > **Partners** > **Exports** from the CleverTap dashboard.
2. Click **Create Export** and select **mParticle**.

<Image title="Click + Export and select mParticle from the Partner dropdown" alt={2376} align="center" width="smart" border={true} src="https://files.readme.io/c3c9fbc-CreatemParticleExport.jpg">
  Create Export
</Image>

The **Export to mParticle** pop-up displays.

<Image alt="Enter Export Details" align="center" width="80% " border={true} src="https://files.readme.io/2207974-mixpanel_live_streaming.png">
  Enter Export Details
</Image>

3. Configure the following settings:
   * **Partner Nickname**: Nickname for the partner. To edit the nickname, go to **Partner List**. 
   * **DATA TYPE & IDENTIFIER PRIORITY**: Select the type of data that you want to export from the available options. For more information, refer to [Export Details](doc:mparticle-export#export-details).
   * **FREQUENCY**: Select from one of the following options:
     * **One time**: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     * **Recurring**: Set up a recurring frequency to export all the new events/user properties captured in the last window. You can export event data as frequently as every 4 hours and up to once every 24 hours. You can export user properties only once every 24 hours. 
     * **Date to export data**: The export starts at 12:00 a.m. on the specified date by default.
4. Click **Export**. The popup closes, and the following message displays at the top of the **Exports** page:

<Image title="mParticle export has initiated message displays at the top" alt={2284} align="center" width="90% " border={true} src="https://files.readme.io/aefe720-mParticleExportCreated.jpg">
  mParticle Export Initiated
</Image>

CleverTap processes the export, and you can now see the newly created export for mParticle.

<Image title="New mParticle export displays on Exports page after processing" alt={2372} align="center" width="90% " border={true} src="https://files.readme.io/6618e18-mParticlePending.jpg">
  New mParticle Export Displays on Exports Page
</Image>

The status for each export is displayed as **PENDING** as soon as the export is created. The status changes to **RUNNING** after the processing starts. It changes to **DONE** when the export is complete.

# Stop Export

You can also stop the export that you have created. Hover over the export. Click the **Stop**  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

<Image title="Click the Stop icon to stop the ongoing mParticle export" alt={2372} align="center" width="90% " border={true} src="https://files.readme.io/0ffce76-mParticleExportStopButton.jpg">
  Stop mParticle Export
</Image>

The **Stop export?** window appears. Click **Stop** to confirm your action.

<Image align="center" className="border" width="60% " border={true} src="https://files.readme.io/7dcac67-StopMParticleButton.jpg" />

You are navigated back to the **Exports** page, and the *mParticle data export stopped* message displays at the top. The status for the data export now displays as **STOPPED**.

<Image title="mParticle export has initiated message displays at the top" alt={2340} align="center" width="90% " border={true} src="https://files.readme.io/afe1fb4-StoppedMParticle.jpg">
  mParticle Export Stopped
</Image>

# Edit an Export

You might need to modify an export to meet specific business requirements or while waiting for the next run. This section describes editing a Recurring export in the **RUNNING** and **PENDING** (awaiting next run) state. 

> 📘 Points to Remember
>
> * In the case of running exports, the new changes will apply to the next run.
> * You cannot edit a One-time export, regardless its status (RUNNING, PENDING, DONE, or STOPPED).
> * You cannot change the export from User Profile to Event and vice-versa.
> * You cannot modify exports marked as **DONE** or **STOPPED**.

To edit an export: 

1. On the CleverTap dashboard, go to **Partners** > **Exports**.
2. Hover over the required export. The **View**, **Edit**, and the **Stop** buttons appear.

<Image alt="Click the Edit Export Icon" align="center" width="90% " border={true} src="https://files.readme.io/a033c60-EditMParticle.jpg">
  Click the Edit Export Icon
</Image>

3. Click the **Edit** button. The **Export to mPartcile** section appears.

<Image alt="Edit the Export" align="center" width="90% " border={true} src="https://files.readme.io/a23dd27-UpdateMPartcileExport.jpg">
  Edit the Export
</Image>

4. Edit the export details and click **Update export**.

# Filter Exports

This section describes the different ways you can filter exports.

## Filter by Export Details

To filter by export details: 

1. Click the **Filter** button at the top right corner. 
2. You can filter exports by **Partner**, **Type**, **Format**, **Status**, or **Frequency**. 
3. To clear the filter, click **Reset all**.

<Image alt="Filter Exports" align="center" width="90% " border={true} src="https://files.readme.io/6499e90-FilterButton.jpg">
  Filter Exports
</Image>

## Filter Exports by Date Range

You can also filter the exports based on the export date. 

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.\
   The **Calendar** widget appears. 

<Image alt="Calendar Widget" align="center" width="90% " border={true} src="https://files.readme.io/74ce34b-Amplitude_Exports_-_Calendar_Widget.png">
  Calendar Widget
</Image>

1. Choose the custom date range and click **Apply**.\
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Options include 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

# Export Details

Select from one of the following options to export events from CleverTap to the mParticle dashboard:

* [All system events](doc:mparticle-export#all-events)
* [Selected events](doc:mparticle-export#selected-events)
* [Engagement events](doc:mparticle-export#engagement-events)
* [User properties](doc:mparticle-export#user-properties)

## All System Events

When you select this option, the following defined system events are exported:

| CleverTap Event Name       | Event Description                                                                                                                                                                                                                            |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Notification Sent          | The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.                                                                                                    |
| Notification Viewed        | This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.                                                                                                                            |
| Notification Clicked       | This event is tracked only when a user clicks on a notification sent via CleverTap.Recorded when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API. |
| Push Impressions           | This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.                                                                                                                                          |
| Notification Replied       | This event is recorded when a user replies to a WhatsApp message.                                                                                                                                                                            |
| Control Group              | The event raised when a campaign is activated with a Control group.                                                                                                                                                                          |
| Channel Unsubscribed       | The event raised when a user Unsubscribes to receive further communication through a channel                                                                                                                                                 |
| Push Impressions           | This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.                                                       |
| AB Experiment Stopped      | This event is recorded when AB experiment is stopped.                                                                                                                                                                                        |
| AB Experiment Rolled Out   | This event is recorded when AB experiment is started                                                                                                                                                                                         |
| AB Experiment Disqualified | This event is raised when the device is disqualified.                                                                                                                                                                                        |
| Geocluster Entered         | This event is recorded to mark when a device enters a geofence.                                                                                                                                                                              |
| Geocluster Exited          | This event is recorded to mark when a device exits a geofence.                                                                                                                                                                               |
| Reply Sent                 | This event is recorded when an agent (CleverTap user) replies to a message from the end-user.                                                                                                                                                |
| App Version Changed        | This event is raised when a user’s current app version is different from the user’s previous app version.                                                                                                                                    |
| App Launched               | This event is recorded every time a user launches your application.                                                                                                                                                                          |
| App Installed              | The event is raised when the user launches the app for the first time.                                                                                                                                                                       |
| App Uninstalled            | This event is recorded when a user uninstalls your application.                                                                                                                                                                              |
| UTM Visited                | This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.                                                                                                                         |

For more information about these events, refer to [Events](doc:events).

## Selected Events

With this option, you can select the specific system events (from those listed in the above table) that you want to export from CleverTap to the mParticle dashboard.

## Engagement Events

When you select this option, the following engagement events are exported:

* Notification Sent
* Notification Viewed
* Notification Clicked
* Push Impressions
* Notification Replied
* Control Group
* Channel Unsubscribed
* Push Impressions
* Notification Delivered
* AB Experiment Rendered
* AB Experiment Stopped
* AB Experiment Rolled Out
* Geocluster Entered
* Geocluster Exited
* Reply Sent
* App Uninstalled
* Webhook Delivered
* State Transitioned
* UTM Visited

For more information about these events, refer to [Events](doc:events).

## User Properties

When you select this option, the following user profile attributes are exported:

| Field                        | Description                                                    |
| :--------------------------- | :------------------------------------------------------------- |
| Name                         | Indicates the name of the user.                                |
| Gender                       | Indicates the gender of the user.                              |
| DOB                          | Indicates the date of birth of the user.                       |
| All communication preference | Flags that determine the communication preference of the user. |

> 📘 Availability of Feature
>
> If you are a CleverTap for Enterprises user, contact your sales account manager to activate this feature at your end. In the case of CleverTap for Startups, it is available as a paid add-on.

# FAQs

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

* CleverTap's export system supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
* It replaces the following characters with a hyphen to avoid issues in output file generation:
  * Whitespace
  * Tab
  * Slash
  * null (\\0)
* Control characters are replaced with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
* Supports emoji characters; however, some emojis (UTF-16) may not render properly.
