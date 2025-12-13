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

* *Export request ID*: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
* *Timestamp of export run*: Indicates when the export was run.
* *Event name*: Indicates the event type that is included in the file.
* *File index*: We chunk the data across multiple files for larger exports. We limit file sizes to 100 MB chunks to make them more consumable. The file index indicates the file number in the file series. 
* *Database ID*: Indicates the database ID of the CleverTap from where the file was exported. 
* *File format*: Indicates the format of the file exported to the S3 bucket.

## File Data Format

### Event Export Schema

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Key
      </th>

      <th>
        Sub-Headers
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        ts
      </td>

      <td>

      </td>

      <td>
        Indicates the time when the event occurred.
      </td>
    </tr>

    <tr>
      <td>
        eventName
      </td>

      <td>

      </td>

      <td>
        Indicates the name of the exported event. 
      </td>
    </tr>

    <tr>
      <td>
        profile
      </td>

      <td>

      </td>

      <td>
        Includes the profile properties of the user who performed the event.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.identity
      </td>

      <td>
        Indicates the identity of the user.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.objectId 
      </td>

      <td>
        Indicates the CleverTap ID of the user
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.all\_identities 
      </td>

      <td>
        Indicates all the unique identities of the user present on the CleverTap.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.platform 
      </td>

      <td>
        Indicates the platform from which they have raised the event
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.phone
      </td>

      <td>
        Indicates the phone number of the user, if present.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.name 
      </td>

      <td>
        Indicates the name of the user.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.email 
      </td>

      <td>
        Indicates the email address of the user.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        profile.push\_token
      </td>

      <td>
        <li> Indicates the device token.</li>  
        <li> It is present if the user raises an event through the device having a token associated with it.</li>
      </td>
    </tr>

    <tr>
      <td>
        deviceInfo
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.make
      </td>

      <td>
        Indicates the make of the user device
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.model 
      </td>

      <td>
        Indicates the model of the user device  through which the event is raised
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.appVersion 
      </td>

      <td>
        Indicates the application version of the user device through which the event is raised
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.sdkVersion 
      </td>

      <td>
        Indicates the CleverTap SDK version installed on the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.osVersion 
      </td>

      <td>
        Indicate the OS version of the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.browser 
      </td>

      <td>
        Indicates the Browser (for example, Chrome, Firefox, etc.) on the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.dpi 
      </td>

      <td>
        Indicates the DPI of the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.dimensions.width  
      </td>

      <td>
        Indicates the width of the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.dimensions.height 
      </td>

      <td>
        Indicates the height of the user device through which the event is raised.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        deviceInfo.dimensions.unit
      </td>

      <td>
        Indicates the unit of measure for user device dimensions through which the event is raised. For example, px (pixels), etc. 
      </td>
    </tr>

    <tr>
      <td>
        controlGroupName
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps
      </td>

      <td>

      </td>

      <td>
        Indicates the properties of the event raised by the user. For more information, refer to Event Properties.
      </td>
    </tr>

    <tr>
      <td>
        sessionProps
      </td>

      <td>

      </td>

      <td>
        Includes the properties only for *UTM Visited* events.
      </td>
    </tr>
  </tbody>
</Table>

## Event Properties

### Notification Sent

This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for Email, Mobile Push, SMS, Web Push, and Facebook Audience campaigns. It is available under the *Event* page on the dashboard but not displayed under the user profile.

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

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Keys
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        eventProps.wzrk\_id
      </td>

      <td>
        Indicates the Campaign ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_animated
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pivot
      </td>

      <td>
        Indicates the campaign variants created for A/B Testing.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign id
      </td>

      <td>
        Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk\_id?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ttl
      </td>

      <td>
        Indicates the time to live for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acct\_id
      </td>

      <td>
        Indicates the CleverTap Account ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pid
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_rnv
      </td>

      <td>
        <li> A flag that indicates if the Notification Viewed event is raised. </li>  
        <li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pn
      </td>

      <td>
        Indicates that the notification is sent from the CleverTap dashboard when present.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign type
      </td>

      <td>
        Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_cid
      </td>

      <td>
        Indicates the Channel ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bc
      </td>

      <td>
        Indicates the batch count.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bi
      </td>

      <td>
        Indicates the badge icon. (@parth: Is it batch or badge?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_sound
      </td>

      <td>
        A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_dl
      </td>

      <td>
        Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acts
      </td>

      <td>
        Indicates the action button payload.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bp
      </td>

      <td>
        Indicates the Image URL included in the notification.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTAppVersion
      </td>

      <td>
        Indicates the application version. (@parth: application version of what?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTSource
      </td>

      <td>
        Indicates the mobile phone or desktop on which the user viewed the notification. (@parth: pls check the explanation.)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTLatitude
      </td>

      <td>
        Indicates the last known latitude captured by CleverTap on launching the application.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTLongitude
      </td>

      <td>
        Indicates the last known longitude captured by CleverTap on launching the application.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_c2a
      </td>

      <td>
        Indicates the value of the button clicked by the user. This button can be present for the following campaign types: In-App, Push, or Mobile In-Box.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.browser
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.CT Session Id
      </td>

      <td>
        Indicates the CleverTap Session ID. (@parth: need more information here.)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_cts
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.User Agent
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.Client Name
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.skipTCM
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.mimeType
      </td>

      <td>
        This property helps you understand the performance of your AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign name
      </td>

      <td>
        Indicates the name of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign labels
      </td>

      <td>
        Indicates the labels added for the campaign
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Journey id
      </td>

      <td>
        Helps uniquely identify the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.
      </td>
    </tr>
  </tbody>
</Table>

### Notification Clicked

This event is tracked only when a user clicks on the campaign sent via CleverTap.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Keys
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        eventProps.Campaigntype
      </td>

      <td>
        Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pivot
      </td>

      <td>
        Indicates the campaign variants created for A/B Testing.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bi
      </td>

      <td>
        Indicates the badge icon. (@parth: Is it batch or badge?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ttl
      </td>

      <td>
        Indicates the time to live for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bc
      </td>

      <td>
        Indicates the batch count.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_dt
      </td>

      <td>
        Indicates the service used to send the message. For example, Firebase, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_id
      </td>

      <td>
        Indicates the Campaign ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTSource
      </td>

      <td>
        Indicates the mobile phone or desktop on which the user viewed the notification. (@parth: pls check the explanation.)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_cid
      </td>

      <td>
        Indicates the Channel ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_push\_amp
      </td>

      <td>
        <li> Accepts the following boolean value: true or false</li>  
        <li> If true, indicates that the notification is rendered through Push amplification. </li>
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pn
      </td>

      <td>
        Indicates that the notification is sent from the CleverTap dashboard when present.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pid
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bp
      </td>

      <td>
        Indicates the Image URL included in the notification.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acct\_id
      </td>

      <td>
        Indicates the CleverTap Account ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_rnv
      </td>

      <td>
        <li> A flag that indicates if the Notification Clicked event is raised. </li>  
        <li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTAppVersion
      </td>

      <td>
        Indicates the application version. (@parth: application version of what?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ck
      </td>

      <td>
        Indicates the collapse key.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ttl\_s
      </td>

      <td>
        Indicates the time to live for the campaign in seconds.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_cts
      </td>

      <td>
        @Parth: Help here.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_dl
      </td>

      <td>
        Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_mutable\_content
      </td>

      <td>
        <li> Captured for iOS push notification. </li>  
        <li> Value is 1 if enabled and 0 if disabled. </li>  
        (@Parth: what does this property indicate?) 
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_collapsible
      </td>

      <td>
        Indicates the Collapse key (the actual key which you have provided).
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_st
      </td>

      <td>
        Indicates the Subtitle (@parth: Which subtitle is this?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_nms
      </td>

      <td>
        Indicates the summary text when sending push notifications.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_clr
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_sound
      </td>

      <td>
        A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acct\_md
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acts
      </td>

      <td>
        Indicates the action button payload.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_c2a
      </td>

      <td>
        <li> Indicates the value of the button clicked by the user. </li>  
        <li> This button can be present for the following campaign types: In-App, Push, or Mobile In-Box. </li>
      </td>
    </tr>

    <tr>
      <td>
        eventProps.mimeType
      </td>

      <td>
        Helps understand the performance of the AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign name
      </td>

      <td>
        Indicates the name of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign labels
      </td>

      <td>
        Indicates the labels added for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Journey id
      </td>

      <td>
        Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.
      </td>
    </tr>
  </tbody>
</Table>

### Push Impression

This event is raised when a push notification is delivered/rendered on the device.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Key
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        eventProps.wzrk\_acct\_id
      </td>

      <td>
        Indicates the CleverTap Account ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pivot
      </td>

      <td>
        Indicates the campaign variants created for A/B Testing.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_cid
      </td>

      <td>
        Indicates the Channel ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pid
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_rnv
      </td>

      <td>
        <li> A flag that indicates if the Notification Viewed event is raised. </li>  
        <li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ttl
      </td>

      <td>
        Indicates the time to live for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bc
      </td>

      <td>
        Indicates the batch count.
      </td>
    </tr>

    <tr>
      <td>
        feventProps.wzrk\_bi
      </td>

      <td>
        Indicated the Badge icon.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_id
      </td>

      <td>
        Indicates the Campaign ID.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_pn
      </td>

      <td>
        Indicates that the notification is sent from the CleverTap dashboard when present.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign type
      </td>

      <td>
        Indicates the type of campaign - Push, Email, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_sound
      </td>

      <td>
        A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_acts
      </td>

      <td>
        Indicates the action button payload.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_bp
      </td>

      <td>
        Indicates the Image URL included in the notification.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_dl
      </td>

      <td>
        Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ck
      </td>

      <td>
        Indicates the collapse key.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTAppVersion
      </td>

      <td>
        Indicates the Application version
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTSource
      </td>

      <td>
        Indicates the source of the event i.e. Mobile, Desktop, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTLatitude
      </td>

      <td>
        Indicates the last known latitude captured by CleverTap on launching the application.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTLongitude
      </td>

      <td>
        Indicates the last known longitude captured by CleverTap on launching the application.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_push\_amp
      </td>

      <td>
        <li> Accepts the following boolean value: true or false</li>  
        <li> If true, indicates that the notification is rendered through Push Amplification. </li>  
        (@parth: Should we use the push amp term here - we are not using that term anymore.)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_dt
      </td>

      <td>
        Indicates the service used to send the message. For example, Firebase, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_ttl\_s
      </td>

      <td>
        Indicates the time to live for the campaign in seconds.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.wzrk\_st
      </td>

      <td>
        Indicates the subtitle 
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign name
      </td>

      <td>
        Indicates the name of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Campaign labels
      </td>

      <td>
        Indicates the labels added for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.Journey id
      </td>

      <td>
        Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.
      </td>
    </tr>
  </tbody>
</Table>

### Notification Replies

This event is raised when a user replies to any WhatsApp campaign.

| Key                        | Description                                                                                                                     |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| eventProps.CTSource        | Indicates the source of the event, i.e. Mobile, Desktop, etc.                                                                   |
| eventProps.wzrk\_id        | Indicates the Campaign ID.                                                                                                      |
| eventProps.Campaign id     | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk\_id?)                                                |
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
| eventProps.wzrk\_id        | Indicates the Campaign ID.                                        |
| eventProps.wzrk\_pivot     | Indicates the campaign variants created for A/B Testing.          |
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

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Key
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        eventProps.ct\_app\_version
      </td>

      <td>
        Indicates the version of the application.\
        (@Parth: How is it different from eventProps.CTApp Version mentioned under Push Impression)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.CTSource
      </td>

      <td>
        Indicates the source of the event, i.e. Mobile, Desktop, etc.
      </td>
    </tr>

    <tr>
      <td>
        eventProps.ct\_latitude
      </td>

      <td>
        Indicates the last known latitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLatitude mentioned under Push Impression?)
      </td>
    </tr>

    <tr>
      <td>
        eventProps.ct\_longitude
      </td>

      <td>
        Indicates the last known longitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLongitude mentioned under Push Impression)
      </td>
    </tr>
  </tbody>
</Table>

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

| Key                                           | Description                                                                                                                      |
| :-------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.ContentName                        |                                                                                                                                  |
| eventProps.CT Source                          | Indicates the source of the event, i.e. Mobile, Desktop etc.                                                                     |
| eventProps.ct\_app\_version                   | Indicates the version of App (@Parth: How is it different from eventProps.CT App Version mentioned under Push Impression)        |
| eventProps.ct\_latitude                       | Indicates the Latitude of the User. (@Parth: How is it different from eventProps.CT Latitude mentioned under Push Impression)    |
| eventProps.all\_identities                    | Indicates All Identity of User                                                                                                   |
| eventProps.ct\_longitude                      | Indicates the Longitude of the User. (@Amrita, How is it different from eventProps.CT Longitude mentioned under Push Impression) |
| eventProps.session\_props \\| session\_source |                                                                                                                                  |
| eventProps.Campaign Id                        | Uniquely identifies the campaign.                                                                                                |
| eventProps.mp\_processing\_time\_ms           | Indicates the time in which we get a response from the customer API.                                                             |
| eventProps.ts                                 | Indicates the timestamp of the event.                                                                                            |

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

| Key                        | Description                                                                      |
| :------------------------- | :------------------------------------------------------------------------------- |
| eventProps.CT Source       | Indicates the source of the event i.e. Mobile, Desktop etc.                      |
| eventProps.wzrk\_id        | Indicates the Campaign ID.                                                       |
| eventProps.wzrk\_pivot     | Indicates the campaign variants created for A/B Testing.                         |
| eventProps.Campaign id     | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk\_id?) |
| eventProps.Campaign name   | Indicates the name of the campaign.                                              |
| eventProps.Campaign type   | Indicates the type of campaign - Push, Email, etc.                               |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                                     |
| eventProps.Journey id      | Helps uniquely identify the journey in which the campaign is present.            |

### System Control Group

This event is raised when a campaign is activated with a Control group.

| Key                      | Description                                                                      |
| :----------------------- | :------------------------------------------------------------------------------- |
| eventProps.CT Source     | Indicates the source of the event i.e. Mobile, Desktop etc.                      |
| eventProps.wzrk\_id      | Indicates the Campaign ID.                                                       |
| eventProps.wzrk\_pivot   | Indicates the campaign variants created for A/B Testing.                         |
| eventProps.Campaign id   | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk\_id?) |
| eventProps.Campaign name | Indicates the name of the campaign.                                              |
| eventProps.Campaign type | Indicates the type of campaign - Push, Email, etc.                               |
| eventProps.Journey id    | Helps uniquely identify the journey in which the campaign is present.            |

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

| Key                                | Description                                                     |
| :--------------------------------- | :-------------------------------------------------------------- |
| eventProps.ct\_connected\_to\_wifi | Status of Wifi on the device when event was raised (True/False) |
| eventProps.ct\_source              | Source is mobile or web                                         |
| eventProps.network\_carrier        | Network Carrier for the device                                  |
| eventProps.longitude               | Longitude                                                       |
| eventProps.latitude                | Latitude                                                        |
| eventProps.os\_version             | OS Version of device                                            |
| eventProps.application\_version    | Version of App                                                  |
| eventProps.ct\_sdk\_version        | CT SDK Verson being used by the app when event was raised       |
| eventProps.geofence\_id            | CT Geogence ID                                                  |
| eventProps.cluster\_name           | CT Geofence Cluster Name                                        |
| eventProps.cluster\_id             | CT Geofence Cluster ID                                          |
| eventProps.ct\_network\_type       | CT Network Type                                                 |

### GeoCluster Exited

This event is raised when a user enters a Geo Cluster.

| Key                                | Description                                                     |
| :--------------------------------- | :-------------------------------------------------------------- |
| eventProps.ct\_source              | Source is mobile or web                                         |
| eventProps.network\_carrier        | Network Carrier for the device                                  |
| eventProps.longitude               | Longitude                                                       |
| eventProps.latitude                | Latitude                                                        |
| eventProps.os\_version             | OS Version of device                                            |
| eventProps.application\_version    | Version of App                                                  |
| eventProps.ct\_sdk\_version        | CT SDK Verson being used by the app when event was raised       |
| eventProps.geofence\_id            | CT Geogence ID                                                  |
| eventProps.cluster\_name           | CT Geofence Cluster Name                                        |
| eventProps.cluster\_id             | CT Geofence Cluster ID                                          |
| eventProps.ct\_connected\_to\_wifi | Status of Wifi on the device when event was raised (True/False) |

### AB Experiment Stopped

This event is raised when the A/B experiment is stopped.

| Key                            | Description                   |
| :----------------------------- | :---------------------------- |
| eventProps.ct\_source          | Source is mobile or web       |
| eventProps.stickiness          | Yes/No                        |
| eventProps.mutually\_exclusive | Should show only 1 experiment |
| eventProps.variant             | Variant of Experiment         |
| eventProps.variant\_id         | Unique Variant ID             |
| eventProps.version             | Version of Experiment         |
| eventProps.experiment\_id      | Experiment ID                 |

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

| Key                        | Description                         |
| :------------------------- | :---------------------------------- |
| eventProps.Campaign id     | Campaign ID for campaigns           |
| eventProps.CT Latitude     | Latitude                            |
| eventProps.CT Longitude    | Longitude                           |
| eventProps.CT App Version  | Version of App                      |
| eventProps.CT Source       | Source is mobile or web             |
| eventProps.Campaign type   | Type of Campaign - Push, Email, SMS |
| eventProps.Install         | Y or N                              |
| eventProps.wzrk\_id        | Campaign ID for campaigns           |
| sessionProps.utm\_campaign | Campaign name                       |
| sessionProps.utm\_medium   | Medium like email , banner etc      |
| sessionProps.utm\_source   | Origination source                  |

# User Profile Export

## File Name Format

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

* **File Name Format for User Profile Export**:\
   The example below shows the file name format for user profile export:
  * *Account ID*: Indicates the integer value for your CleverTap project ID. 
  * *Request ID*: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  * *Timestamp of export run*: Indicates when the export was run.
  * *Database ID*: Indicates the database ID of the CleverTap from where the file was exported. 
  * *File format*: Indicates the format of the file exported to the S3 bucket.

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

<Image title="Sample CSV File" alt={2032} align="center" src="https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png">
  Sample CSV File
</Image>

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
