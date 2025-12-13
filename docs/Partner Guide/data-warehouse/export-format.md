---
title: Export Format
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

This document provides information about the file format and the name format of the files exported to different Datawarehouse partners.

# Event Export

## File Name Format

The example below shows the file name format for event export:

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- _Export request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
- _Timestamp of export run_: Indicates when the export was run.
- _Event name_: Indicates the event type that is included in the file.
- _File index_: We chunk the data across multiple files for larger exports. We limit file sizes to 100 MB chunks to make them more consumable. The file index indicates the file number in the file series. 
- _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
- _File format_: Indicates the format of the file exported to the S3 bucket.

## File Data Format

### Event Export Schema

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Sub-Headers",
    "h-2": "Description",
    "0-0": "ts",
    "0-1": "",
    "0-2": "Indicates the time when the event occurred.",
    "1-0": "eventName",
    "1-1": "",
    "1-2": "Indicates the name of the exported event. ",
    "2-0": "profile",
    "2-1": "",
    "2-2": "Includes the profile properties of the user who performed the event.",
    "3-0": "",
    "3-1": "profile.identity",
    "3-2": "Indicates the identity of the user.",
    "4-0": "",
    "4-1": "profile.objectId ",
    "4-2": "Indicates the CleverTap ID of the user",
    "5-0": "",
    "5-1": "profile.all_identities ",
    "5-2": "Indicates all the unique identities of the user present on the CleverTap.",
    "6-0": "",
    "6-1": "profile.platform ",
    "6-2": "Indicates the platform from which they have raised the event",
    "7-0": "",
    "7-1": "profile.phone",
    "7-2": "Indicates the phone number of the user, if present.",
    "8-0": "",
    "8-1": "profile.name ",
    "8-2": "Indicates the name of the user.",
    "9-0": "",
    "9-1": "profile.email ",
    "9-2": "Indicates the email address of the user.",
    "10-0": "",
    "10-1": "profile.push_token",
    "10-2": "<li> Indicates the device token.</li>  \n<li> It is present if the user raises an event through the device having a token associated with it.</li>",
    "11-0": "deviceInfo",
    "11-1": "",
    "11-2": "",
    "12-0": "",
    "12-1": "deviceInfo.make",
    "12-2": "Indicates the make of the user device",
    "13-0": "",
    "13-1": "deviceInfo.model ",
    "13-2": "Indicates the model of the user device  through which the event is raised",
    "14-0": "",
    "14-1": "deviceInfo.appVersion ",
    "14-2": "Indicates the application version of the user device through which the event is raised",
    "15-0": "",
    "15-1": "deviceInfo.sdkVersion ",
    "15-2": "Indicates the CleverTap SDK version installed on the user device through which the event is raised.",
    "16-0": "",
    "16-1": "deviceInfo.osVersion ",
    "16-2": "Indicate the OS version of the user device through which the event is raised.",
    "17-0": "",
    "17-1": "deviceInfo.browser ",
    "17-2": "Indicates the Browser (for example, Chrome, Firefox, etc.) on the user device through which the event is raised.",
    "18-0": "",
    "18-1": "deviceInfo.dpi ",
    "18-2": "Indicates the DPI of the user device through which the event is raised.",
    "19-0": "",
    "19-1": "deviceInfo.dimensions.width  ",
    "19-2": "Indicates the width of the user device through which the event is raised.",
    "20-0": "",
    "20-1": "deviceInfo.dimensions.height ",
    "20-2": "Indicates the height of the user device through which the event is raised.",
    "21-0": "",
    "21-1": "deviceInfo.dimensions.unit",
    "21-2": "Indicates the unit of measure for user device dimensions through which the event is raised. For example, px (pixels), etc. ",
    "22-0": "controlGroupName",
    "22-1": "",
    "22-2": "",
    "23-0": "eventProps",
    "23-1": "",
    "23-2": "Indicates the properties of the event raised by the user. For more information, refer to Event Properties.",
    "24-0": "sessionProps",
    "24-1": "",
    "24-2": "Includes the properties only for _UTM Visited_ events."
  },
  "cols": 3,
  "rows": 25,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

## Event Properties

### Notification Sent

This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for Email, Mobile Push, SMS, Web Push, and Facebook Audience campaigns. It is available under the _Event_ page on the dashboard but not displayed under the user profile.

| Keys                       | Description                                                           |
| :------------------------- | :-------------------------------------------------------------------- |
| eventProps.Campaign id     | Helps uniquely identify the campaign.                                 |
| eventProps.Campaign type   | Indicates the type of campaign - Push, Email, etc.                    |
| eventProps.Campaign name   | Indicates the name of the campaign.                                   |
| eventProps.Variant         | Indicates the campaign variants created for A/B Testing.              |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                          |
| eventProps.Journey id      | Helps uniquely identify the journey in which the campaign is present. |

### Notification Viewed

This event is tracked when a user views an Email, In-App notification, or Web notification sent from the CleverTap dashboard.

[block:parameters]
{
  "data": {
    "h-0": "Keys",
    "h-1": "Description",
    "0-0": "eventProps.wzrk_id",
    "0-1": "Indicates the Campaign ID.",
    "1-0": "eventProps.wzrk_animated",
    "1-1": "",
    "2-0": "eventProps.wzrk_pivot",
    "2-1": "Indicates the campaign variants created for A/B Testing.",
    "3-0": "eventProps.Campaign id",
    "3-1": "Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk_id?)",
    "4-0": "eventProps.wzrk_ttl",
    "4-1": "Indicates the time to live for the campaign.",
    "5-0": "eventProps.wzrk_acct_id",
    "5-1": "Indicates the CleverTap Account ID.",
    "6-0": "eventProps.wzrk_pid",
    "6-1": "",
    "7-0": "eventProps.wzrk_rnv",
    "7-1": "<li> A flag that indicates if the Notification Viewed event is raised. </li>  \n<li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "8-0": "eventProps.wzrk_pn",
    "8-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "9-0": "eventProps.Campaign type",
    "9-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "10-0": "eventProps.wzrk_cid",
    "10-1": "Indicates the Channel ID.",
    "11-0": "eventProps.wzrk_bc",
    "11-1": "Indicates the batch count.",
    "12-0": "eventProps.wzrk_bi",
    "12-1": "Indicates the badge icon. (@parth: Is it batch or badge?)",
    "13-0": "eventProps.wzrk_sound",
    "13-1": "A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)",
    "14-0": "eventProps.wzrk_dl",
    "14-1": "Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)",
    "15-0": "eventProps.wzrk_acts",
    "15-1": "Indicates the action button payload.",
    "16-0": "eventProps.wzrk_bp",
    "16-1": "Indicates the Image URL included in the notification.",
    "17-0": "eventProps.CTAppVersion",
    "17-1": "Indicates the application version. (@parth: application version of what?)",
    "18-0": "eventProps.CTSource",
    "18-1": "Indicates the mobile phone or desktop on which the user viewed the notification. (@parth: pls check the explanation.)",
    "19-0": "eventProps.CTLatitude",
    "19-1": "Indicates the last known latitude captured by CleverTap on launching the application.",
    "20-0": "eventProps.CTLongitude",
    "20-1": "Indicates the last known longitude captured by CleverTap on launching the application.",
    "21-0": "eventProps.wzrk_c2a",
    "21-1": "Indicates the value of the button clicked by the user. This button can be present for the following campaign types: In-App, Push, or Mobile In-Box.",
    "22-0": "eventProps.browser",
    "22-1": "",
    "23-0": "eventProps.CT Session Id",
    "23-1": "Indicates the CleverTap Session ID. (@parth: need more information here.)",
    "24-0": "eventProps.wzrk_cts",
    "24-1": "",
    "25-0": "eventProps.User Agent",
    "25-1": "",
    "26-0": "eventProps.Client Name",
    "26-1": "",
    "27-0": "eventProps.skipTCM",
    "27-1": "",
    "28-0": "eventProps.mimeType",
    "28-1": "This property helps you understand the performance of your AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).",
    "29-0": "eventProps.Campaign name",
    "29-1": "Indicates the name of the campaign.",
    "30-0": "eventProps.Campaign labels",
    "30-1": "Indicates the labels added for the campaign",
    "31-0": "eventProps.Journey id",
    "31-1": "Helps uniquely identify the journey in which the campaign is present. This is recorded only if the campaign is part of any journey."
  },
  "cols": 2,
  "rows": 32,
  "align": [
    "left",
    "left"
  ]
}
[/block]

### Notification Clicked

This event is tracked only when a user clicks on the campaign sent via CleverTap.

[block:parameters]
{
  "data": {
    "h-0": "Keys",
    "h-1": "Description",
    "0-0": "eventProps.Campaigntype",
    "0-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "1-0": "eventProps.wzrk_pivot",
    "1-1": "Indicates the campaign variants created for A/B Testing.",
    "2-0": "eventProps.wzrk_bi",
    "2-1": "Indicates the badge icon. (@parth: Is it batch or badge?)",
    "3-0": "eventProps.wzrk_ttl",
    "3-1": "Indicates the time to live for the campaign.",
    "4-0": "eventProps.wzrk_bc",
    "4-1": "Indicates the batch count.",
    "5-0": "eventProps.wzrk_dt",
    "5-1": "Indicates the service used to send the message. For example, Firebase, etc.",
    "6-0": "eventProps.wzrk_id",
    "6-1": "Indicates the Campaign ID.",
    "7-0": "eventProps.CTSource",
    "7-1": "Indicates the mobile phone or desktop on which the user viewed the notification. (@parth: pls check the explanation.)",
    "8-0": "eventProps.wzrk_cid",
    "8-1": "Indicates the Channel ID.",
    "9-0": "eventProps.wzrk_push_amp",
    "9-1": "<li> Accepts the following boolean value: true or false</li>  \n<li> If true, indicates that the notification is rendered through Push amplification. </li>",
    "10-0": "eventProps.wzrk_pn",
    "10-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "11-0": "eventProps.wzrk_pid",
    "11-1": "",
    "12-0": "eventProps.wzrk_bp",
    "12-1": "Indicates the Image URL included in the notification.",
    "13-0": "eventProps.wzrk_acct_id",
    "13-1": "Indicates the CleverTap Account ID.",
    "14-0": "eventProps.wzrk_rnv",
    "14-1": "<li> A flag that indicates if the Notification Clicked event is raised. </li>  \n<li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "15-0": "eventProps.CTAppVersion",
    "15-1": "Indicates the application version. (@parth: application version of what?)",
    "16-0": "eventProps.wzrk_ck",
    "16-1": "Indicates the collapse key.",
    "17-0": "eventProps.wzrk_ttl_s",
    "17-1": "Indicates the time to live for the campaign in seconds.",
    "18-0": "eventProps.wzrk_cts",
    "18-1": "@Parth: Help here.",
    "19-0": "eventProps.wzrk_dl",
    "19-1": "Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)",
    "20-0": "eventProps.wzrk_mutable_content",
    "20-1": "<li> Captured for iOS push notification. </li>  \n<li> Value is 1 if enabled and 0 if disabled. </li>  \n(@Parth: what does this property indicate?) ",
    "21-0": "eventProps.wzrk_collapsible",
    "21-1": "Indicates the Collapse key (the actual key which you have provided).",
    "22-0": "eventProps.wzrk_st",
    "22-1": "Indicates the Subtitle (@parth: Which subtitle is this?)",
    "23-0": "eventProps.wzrk_nms",
    "23-1": "Indicates the summary text when sending push notifications.",
    "24-0": "eventProps.wzrk_clr",
    "24-1": "",
    "25-0": "eventProps.wzrk_sound",
    "25-1": "A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)",
    "26-0": "eventProps.wzrk_acct_md",
    "26-1": "",
    "27-0": "eventProps.wzrk_acts",
    "27-1": "Indicates the action button payload.",
    "28-0": "eventProps.wzrk_c2a",
    "28-1": "<li> Indicates the value of the button clicked by the user. </li>  \n<li> This button can be present for the following campaign types: In-App, Push, or Mobile In-Box. </li>",
    "29-0": "eventProps.mimeType",
    "29-1": "Helps understand the performance of the AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).",
    "30-0": "eventProps.Campaign name",
    "30-1": "Indicates the name of the campaign.",
    "31-0": "eventProps.Campaign labels",
    "31-1": "Indicates the labels added for the campaign.",
    "32-0": "eventProps.Journey id",
    "32-1": "Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey."
  },
  "cols": 2,
  "rows": 33,
  "align": [
    "left",
    "left"
  ]
}
[/block]

### Push Impression

This event is raised when a push notification is delivered/rendered on the device.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.wzrk_acct_id",
    "0-1": "Indicates the CleverTap Account ID.",
    "1-0": "eventProps.wzrk_pivot",
    "1-1": "Indicates the campaign variants created for A/B Testing.",
    "2-0": "eventProps.wzrk_cid",
    "2-1": "Indicates the Channel ID.",
    "3-0": "eventProps.wzrk_pid",
    "3-1": "",
    "4-0": "eventProps.wzrk_rnv",
    "4-1": "<li> A flag that indicates if the Notification Viewed event is raised. </li>  \n<li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "5-0": "eventProps.wzrk_ttl",
    "5-1": "Indicates the time to live for the campaign.",
    "6-0": "eventProps.wzrk_bc",
    "6-1": "Indicates the batch count.",
    "7-0": "feventProps.wzrk_bi",
    "7-1": "Indicated the Badge icon.",
    "8-0": "eventProps.wzrk_id",
    "8-1": "Indicates the Campaign ID.",
    "9-0": "eventProps.wzrk_pn",
    "9-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "10-0": "eventProps.Campaign type",
    "10-1": "Indicates the type of campaign - Push, Email, etc.",
    "11-0": "eventProps.wzrk_sound",
    "11-1": "A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)",
    "12-0": "eventProps.wzrk_acts",
    "12-1": "Indicates the action button payload.",
    "13-0": "eventProps.wzrk_bp",
    "13-1": "Indicates the Image URL included in the notification.",
    "14-0": "eventProps.wzrk_dl",
    "14-1": "Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)",
    "15-0": "eventProps.wzrk_ck",
    "15-1": "Indicates the collapse key.",
    "16-0": "eventProps.CTAppVersion",
    "16-1": "Indicates the Application version",
    "17-0": "eventProps.CTSource",
    "17-1": "Indicates the source of the event i.e. Mobile, Desktop, etc.",
    "18-0": "eventProps.CTLatitude",
    "18-1": "Indicates the last known latitude captured by CleverTap on launching the application.",
    "19-0": "eventProps.CTLongitude",
    "19-1": "Indicates the last known longitude captured by CleverTap on launching the application.",
    "20-0": "eventProps.wzrk_push_amp",
    "20-1": "<li> Accepts the following boolean value: true or false</li>  \n<li> If true, indicates that the notification is rendered through Push Amplification. </li>  \n(@parth: Should we use the push amp term here - we are not using that term anymore.)",
    "21-0": "eventProps.wzrk_dt",
    "21-1": "Indicates the service used to send the message. For example, Firebase, etc.",
    "22-0": "eventProps.wzrk_ttl_s",
    "22-1": "Indicates the time to live for the campaign in seconds.",
    "23-0": "eventProps.wzrk_st",
    "23-1": "Indicates the subtitle ",
    "24-0": "eventProps.Campaign name",
    "24-1": "Indicates the name of the campaign.",
    "25-0": "eventProps.Campaign labels",
    "25-1": "Indicates the labels added for the campaign.",
    "26-0": "eventProps.Journey id",
    "26-1": "Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey."
  },
  "cols": 2,
  "rows": 27,
  "align": [
    "left",
    "left"
  ]
}
[/block]

### Notification Replies

This event is raised when a user replies to any WhatsApp campaign.

| Key                        | Description                                                                                                                     |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| eventProps.CTSource        | Indicates the source of the event, i.e. Mobile, Desktop, etc.                                                                   |
| eventProps.wzrk_id         | Indicates the Campaign ID.                                                                                                      |
| eventProps.Campaign id     | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk_id?)                                                 |
| eventProps.Campaign type   | Indicates the type of campaign - Push, Email, etc.                                                                              |
| eventProps.Campaign name   | Indicates the name of the campaign.                                                                                             |
| eventProps.Variant         | Indicates the campaign variants created for A/B Testing.                                                                        |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                                                                                    |
| eventProps.Journey id      | Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey. |

### Notification Delivered

This event is captured when messages get delivered to the user's WhatsApp app. (Raised only for WhatsApp).

| Key                        | Description                                                       |
| :------------------------- | :---------------------------------------------------------------- |
| eventProps.Campaign type   | Indicates the type of Campaign.                                   |
| eventProps.CTSource        | Indicates the source of the event, i.e. Mobile, Desktop, etc.     |
| eventProps.wzrk_id         | Indicates the Campaign ID.                                        |
| eventProps.wzrk_pivot      | Indicates the campaign variants created for A/B Testing.          |
| eventProps.skipTCM         |                                                                   |
| eventProps.Campaign name   | Indicates the name of the campaign.                               |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                      |
| eventProps.Journey id      | Uniquely identifies the journey in which the campaign is present. |

### Reply Sent

This event is recorded when an agent (CleverTap user) replies to a message from the end user.

| Key                      | Description                                                   |
| :----------------------- | :------------------------------------------------------------ |
| eventProps.CT Source     | Indicates the source of the event, i.e. Mobile, Desktop, etc. |
| eventProps.Campaign id   | Indicates the campaign ID to uniquely identify the campaign.  |
| eventProps.Campaign type | Indicates the type of campaign.                               |

### App Installed

This event is recorded when the user installs the application.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.ct_app_version",
    "0-1": "Indicates the version of the application.  \n(@Parth: How is it different from eventProps.CTApp Version mentioned under Push Impression)",
    "1-0": "eventProps.CTSource",
    "1-1": "Indicates the source of the event, i.e. Mobile, Desktop, etc.",
    "2-0": "eventProps.ct_latitude",
    "2-1": "Indicates the last known latitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLatitude mentioned under Push Impression?)",
    "3-0": "eventProps.ct_longitude",
    "3-1": "Indicates the last known longitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLongitude mentioned under Push Impression)"
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]

### App Launched

This event is recorded every time the user launches the application.

| Key                            | Description                                                                                                  |
| :----------------------------- | :----------------------------------------------------------------------------------------------------------- |
| eventProps.CTNetworkCarrier    | Indicates the network carrier for the user's device.                                                         |
| eventProps.CTSource            | Indicates the source of the event i.e. Mobile, Desktop, etc.                                                 |
| eventProps.CTBluetoothVersion  | Indicates the Bluetooth version of the user's device.                                                        |
| eventProps.CTSDKVersion        | Indicates CleverTap SDK version which is used (@parth: where is the SDK version used?)                       |
| eventProps.CT BluetoothEnabled | Indicates if Bluetooth is enabled for the user's device.                                                     |
| eventProps.CTOSVersion         | Indicates the OS version of the user's device.                                                               |
| eventProps.CTNetworkType       | Indicates the type of network being used on the user's device. For example, Wifi, 4G, etc.                   |
| eventProps.Model               | Indicates the model of the user's device.                                                                    |
| eventProps.CT Longitude        | Indicates the last known longitude captured by CleverTap on launching the application.                       |
| eventProps.CT Latitude         | Indicates the last known latitude captured by CleverTap on launching the application.                        |
| eventProps.CTConnectedToWiFi   | Indicates if the user's device is connected to Wifi.                                                         |
| eventProps.CT Session Id       | Indicates the CleverTap session ID. (@parth: need more information here.)                                    |
| eventProps.CTAppVersion        | Indicates the version of the application installed on the user's device. (@parth: check if this is correct.) |

### App Uninstalled

This event is recorded every time the user uninstalls the application.

| Key                    | Description                                                                                                                                                      |
| :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT Source   | Indicates the source of the event i.e. Mobile, Desktop, etc.                                                                                                     |
| eventProps.clevertapId | Indicates the unique device identifier. This is assigned to all the users when they launch the app for the first time. (@parth: Pls confirm if this is correct.) |
| eventProps.token       | Indicates the Device token of the event                                                                                                                          |
| eventProps.source      | Indicates the source of event i.e. FCM or API                                                                                                                    |

### Webhook Delivered

This event is recorded when a Webhook campaign is delivered successfully.

| Key                                        | Description                                                                                                                      |
| :----------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.ContentName                     |                                                                                                                                  |
| eventProps.CT Source                       | Indicates the source of the event, i.e. Mobile, Desktop etc.                                                                     |
| eventProps.ct_app_version                  | Indicates the version of App (@Parth: How is it different from eventProps.CT App Version mentioned under Push Impression)        |
| eventProps.ct_latitude                     | Indicates the Latitude of the User. (@Parth: How is it different from eventProps.CT Latitude mentioned under Push Impression)    |
| eventProps.all_identities                  | Indicates All Identity of User                                                                                                   |
| eventProps.ct_longitude                    | Indicates the Longitude of the User. (@Amrita, How is it different from eventProps.CT Longitude mentioned under Push Impression) |
| eventProps.session_props \| session_source |                                                                                                                                  |
| eventProps.Campaign Id                     | Uniquely identifies the campaign.                                                                                                |
| eventProps.mp_processing_time_ms           | Indicates the time in which we get a response from the customer API.                                                             |
| eventProps.ts                              | Indicates the timestamp of the event.                                                                                            |

### Channel Unsubscribed

This event is raised when a user unsubscribe from any groups in an Email.

| Key                          | Description                                                                                                     |
| :--------------------------- | :-------------------------------------------------------------------------------------------------------------- |
| eventProps.Variant           | Indicates the campaign variants created for A/B Testing.                                                        |
| eventProps.Resubscribed      | Yes/No                                                                                                          |
| eventProps.Group             | Subscription Group                                                                                              |
| eventProps.Type              | Indicates the type of campaign - Push, Email, etc. (@Parth, how is it different from eventProps.Campaign type?) |
| eventProps.Campaign id       | Helps uniquely identify the campaign.                                                                           |
| eventProps.Subscription Type | Indicates the type of Subscription                                                                              |
| eventProps.Identity          | Indicates the Unique Identity of the User                                                                       |
| eventProps.Reason            | Indicates the reason for Unsubscribing/Resubscribing                                                            |
| eventProps.Campaign type     | @Parth, How is it different from eventProps.Type ?                                                              |

### Custom Control Group

This event is raised when a campaign is activated with a Control group.

| Key                        | Description                                                                     |
| :------------------------- | :------------------------------------------------------------------------------ |
| eventProps.CT Source       | Indicates the source of the event i.e. Mobile, Desktop etc.                     |
| eventProps.wzrk_id         | Indicates the Campaign ID.                                                      |
| eventProps.wzrk_pivot      | Indicates the campaign variants created for A/B Testing.                        |
| eventProps.Campaign id     | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk_id?) |
| eventProps.Campaign name   | Indicates the name of the campaign.                                             |
| eventProps.Campaign type   | Indicates the type of campaign - Push, Email, etc.                              |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                                    |
| eventProps.Journey id      | Helps uniquely identify the journey in which the campaign is present.           |

### System Control Group

This event is raised when a campaign is activated with a Control group.

| Key                      | Description                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| eventProps.CT Source     | Indicates the source of the event i.e. Mobile, Desktop etc.                     |
| eventProps.wzrk_id       | Indicates the Campaign ID.                                                      |
| eventProps.wzrk_pivot    | Indicates the campaign variants created for A/B Testing.                        |
| eventProps.Campaign id   | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk_id?) |
| eventProps.Campaign name | Indicates the name of the campaign.                                             |
| eventProps.Campaign type | Indicates the type of campaign - Push, Email, etc.                              |
| eventProps.Journey id    | Helps uniquely identify the journey in which the campaign is present.           |

### Custom & Journey Control Group (Journeys)

This event is raised when a Journey Campaign is activated with a Control group.

| Key                     | Description                                                                                   |
| :---------------------- | :-------------------------------------------------------------------------------------------- |
| eventProps.Journey id   | Helps uniquely identify the journey in which the campaign is present.                         |
| eventProps.Journey name | Indicates Unique Journey identifier (@Parth, how is it different from eventProps.Journey id?) |

### System Control Group (Journeys)

This event is raised when a Journey Campaign is activated with a Control group.

| Key                     | Description                                                                                   |
| :---------------------- | :-------------------------------------------------------------------------------------------- |
| eventProps.Journey id   | Helps uniquely identify the journey in which the campaign is present.                         |
| eventProps.Journey name | Indicates Unique Journey identifier (@Parth, how is it different from eventProps.Journey id?) |

### Geocluster Entered

This event is raised when a user enters a Geo Cluster.

| Key                             | Description                                                     |
| :------------------------------ | :-------------------------------------------------------------- |
| eventProps.ct_connected_to_wifi | Status of Wifi on the device when event was raised (True/False) |
| eventProps.ct_source            | Source is mobile or web                                         |
| eventProps.network_carrier      | Network Carrier for the device                                  |
| eventProps.longitude            | Longitude                                                       |
| eventProps.latitude             | Latitude                                                        |
| eventProps.os_version           | OS Version of device                                            |
| eventProps.application_version  | Version of App                                                  |
| eventProps.ct_sdk_version       | CT SDK Verson being used by the app when event was raised       |
| eventProps.geofence_id          | CT Geogence ID                                                  |
| eventProps.cluster_name         | CT Geofence Cluster Name                                        |
| eventProps.cluster_id           | CT Geofence Cluster ID                                          |
| eventProps.ct_network_type      | CT Network Type                                                 |

### GeoCluster Exited

This event is raised when a user enters a Geo Cluster.

| Key                             | Description                                                     |
| :------------------------------ | :-------------------------------------------------------------- |
| eventProps.ct_source            | Source is mobile or web                                         |
| eventProps.network_carrier      | Network Carrier for the device                                  |
| eventProps.longitude            | Longitude                                                       |
| eventProps.latitude             | Latitude                                                        |
| eventProps.os_version           | OS Version of device                                            |
| eventProps.application_version  | Version of App                                                  |
| eventProps.ct_sdk_version       | CT SDK Verson being used by the app when event was raised       |
| eventProps.geofence_id          | CT Geogence ID                                                  |
| eventProps.cluster_name         | CT Geofence Cluster Name                                        |
| eventProps.cluster_id           | CT Geofence Cluster ID                                          |
| eventProps.ct_connected_to_wifi | Status of Wifi on the device when event was raised (True/False) |

### AB Experiment Stopped

This event is raised when the A/B experiment is stopped.

| Key                           | Description                   |
| :---------------------------- | :---------------------------- |
| eventProps.ct_source          | Source is mobile or web       |
| eventProps.stickiness         | Yes/No                        |
| eventProps.mutually_exclusive | Should show only 1 experiment |
| eventProps.variant            | Variant of Experiment         |
| eventProps.variant_id         | Unique Variant ID             |
| eventProps.version            | Version of Experiment         |
| eventProps.experiment_id      | Experiment ID                 |

### AB Experiment Rolled Out

This event is raised when the A/B experiment is sent to users.

| Key                           | Description                   |
| :---------------------------- | :---------------------------- |
| eventProps.Variant            | Variant of Experiment         |
| eventProps.Variant Id         | Unique Variant ID             |
| eventProps.CT Source          | Source is mobile or web       |
| eventProps.Version            | Version of Experiment         |
| eventProps.Experiment Id      | Experiment ID                 |
| eventProps.Stickiness         | Yes/No                        |
| eventProps.Mutually Exclusive | Should show only 1 experiment |

### AB Experiment Disqualified

This event is raised when a user is disqualified from the A/B experiment.

### AB Experiment Rendered

This event is raised when the A/B experiment is rendered to a user.

| Key                           | Description                   |
| :---------------------------- | :---------------------------- |
| eventProps.Variant            | Variant of Experiment         |
| eventProps.Variant Id         | Unique Variant ID             |
| eventProps.CT Source          | Source is mobile or web       |
| eventProps.Version            | Version of Experiment         |
| eventProps.Experiment Id      | Experiment ID                 |
| eventProps.Stickiness         | Yes/No                        |
| eventProps.Mutually Exclusive | Should show only 1 experiment |

### State Transitioned

This event is recorded for lifecycle optimizer when a user transitions from one stage to another.

| Key                    | Description             |
| :--------------------- | :---------------------- |
| eventProps.Destination | Destination Value       |
| eventProps.Type        | Type Value of Lifecycle |
| eventProps.Model       | Model Value             |
| eventProps.Source      | Value of Source         |

### Session Concluded

This event is raised when a user session is completed.

| Key                       | Description                        |
| :------------------------ | :--------------------------------- |
| eventProps.Session Length | Time for which user was using apps |
| eventProps.Session Id     | Unique CT Session identifier       |

### UTM Visited

This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.

| Key                       | Description                         |
| :------------------------ | :---------------------------------- |
| eventProps.Campaign id    | Campaign ID for campaigns           |
| eventProps.CT Latitude    | Latitude                            |
| eventProps.CT Longitude   | Longitude                           |
| eventProps.CT App Version | Version of App                      |
| eventProps.CT Source      | Source is mobile or web             |
| eventProps.Campaign type  | Type of Campaign - Push, Email, SMS |
| eventProps.Install        | Y or N                              |
| eventProps.wzrk_id        | Campaign ID for campaigns           |
| sessionProps.utm_campaign | Campaign name                       |
| sessionProps.utm_medium   | Medium like email , banner etc      |
| sessionProps.utm_source   | Origination source                  |

# User Profile Export

## File Name Format

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- **File Name Format for User Profile Export**:  
   The example below shows the file name format for user profile export:
  - _Account ID_: Indicates the integer value for your CleverTap project ID. 
  - _Request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of export run_: Indicates when the export was run.
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the format of the file exported to the S3 bucket.

```text
<account id>-<request id>-<timestamp of the export run>-<database-id>-<file format>.gz
```

## File Data Format

Files are split by event names for event exports and each file will have all event data for the given period for the event.

### JSON

The first line of the file contains the event name. After the first line, each line in JSON describes the timestamp, object id, and event properties.

```json
{
	"profile": {
		"identity": "dqsndckfk234"
	},
	"ts": 20171109000015,
	"eventProps": {
		"ct_connected_to_wifi": "false",
		"ct_bluetooth_version": "ble",
		"ct_bluetooth_enabled": "false",
		"ct_sdk_version": 30107,
		"ct_latitude": -6.1975594,
		"ct_longitude": 106.52913,
		"ct_os_version": "5.1.1",
		"ct_app_version": "2.30.1",
		"ct_network_carrier": "3",
		"ct_network_type": "4G"
	}
}
```

### CSV

CSV files are comma-delimited and have each event in separate rows.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png",
        "Sample CSV File",
        2032
      ],
      "align": "center",
      "caption": "Sample CSV File"
    }
  ]
}
[/block]

### XML

XML has the timeStamp, eventName, followed by eventProperties.

```typescript
<Event>
    <ts>20200220130735</ts>
    <eventName>Export Custom Event</eventName>
    <profile>
        <all_identities>exportProfile+81@clevertap.com</all_identities>
        <platform>Web</platform>
        <email>exportProfile+81@clevertap.com</email>
    </profile>
    <deviceInfo>
        <browser>Others</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>API</value>
        </entry>
        <entry>
            <key>Category</key>
            <value>Mens Watch</value>
        </entry>
        <entry>
            <key>Product name</key>
            <value>Casio Chronograph Watch</value>
        </entry>
        <entry>
            <key>Price</key>
            <value>59.99</value>
        </entry>
        <entry>
            <key>Currency</key>
            <value>USD</value>
        </entry>
    </eventProps>
</Event>
```

### Parquet

Parquet has a timestamp, eventName, and eventProperties for each event. 

> 📘 Parquet File Format
> 
> Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.

| Event             | Description                                                                                                                                                                                                                                                                                                                                                          | Event Properties       | Description                |
| :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------- | :------------------------- |
| Notification Sent | This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, web push, and Facebook Audience campaigns. The Notification Sent event is available on the Event dashboard, but it is not displayed on the User Profile. |                        |                            |
|                   |                                                                                                                                                                                                                                                                                                                                                                      | eventProps.Campaign id | Campaign unique identifier |