---
title: Events
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

Events track what individual actions users perform in your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item.

By tracking events in your app, you can better understand what users are doing. In CleverTap, you can analyze these events in many different ways, such as getting aggregating metrics of a specific event or measuring how a specific event type trends over time. You can also engage with your users based on these events by creating campaigns in CleverTap that are triggered by them. 

<Image title="events1.png" alt={898} align="center" className="border" width="80%" border={true} src="https://files.readme.io/40b874a-events1.png" />

## Event Categories

CleverTap has two categories of events:

* System events: Events recorded automatically after you integrate our SDK. 
* Custom events: Events you define and track with our SDK or API.

## Event Properties

Events have details that describe the action taking place called properties. 

For example, while recording the *Product viewed* event, you could also store event properties, such as product name, category, and price. Recording event properties will help you discover insights, such as which category of products are more popular, and help you segment users based on which categories or price points they have viewed.

# System Events

System events are events recorded automatically after you integrate our SDK. 


<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Event Type</p>
      </th>

      <th>
        <p>Description</p>
      </th>

      <th>
        <p>How Event is Tracked</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>App Installed</p>
      </td>

      <td>
        <p>The event is raised when the user launches the app for the first time</p>
      </td>

      <td>
        <p>The event is raised when the user launches the app for the first time on any mobile device. </p><p>There are two cases when this event will be recorded multiple times for a single user. The first case is when a user installs your app, uninstalls it, and then reinstalls it. The second case is when a user clears your app's memory and relaunches it.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>App Launched</p>
      </td>

      <td>
        <p>This event is recorded every time a user launches your application.</p>
      </td>

      <td>
        <p>There are two cases when this event will recorded. The first case is a fresh app launch, which is when an app is launched from a killed state. The second case is when an app is brought to the foreground after 20 minutes of inactivity in the background.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>App Uninstalled</p>
      </td>

      <td>
        <p>This event is recorded when a user uninstalls your application.</p>
      </td>

      <td>
        <p>This event is tracked by sending silent push notifications which is a type of notifications that is not rendered on a user’s device. We send silent push notifications to your entire install base once every 24 hours to track uninstalls. For more information, refer to <a href="https://clevertap.com/blog/track-app-uninstalls-effectively/">App Uninstall</a>.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Web Session Started</p>
      </td>

      <td>
        <p>This is a web entry event similar to the App launched event. This event refers to the event triggered when a user starts a session or engages with your website.</p>
      </td>

      <td>
        <p>This event will be recorded in two cases: when a user opens a webpage and when a user reloads the browser after 20 minutes of inactivity.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>UTM Visited</p>
      </td>

      <td>
        <p>This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.</p>
      </td>

      <td>
        <p>The <em>UTM Visited</em> event is recorded for your marketing campaigns from external sources, such as Google Adwords or AdRoll.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Sent</p>
      </td>

      <td>
        <p>This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS and web push, campaigns. The <em>Notification Sent</em> event is available on the <em>Event</em> dashboard but it is not displayed on the <em>User Profile</em>.</p>
      </td>

      <td>
        <p>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Viewed</p>
      </td>

      <td>
        <p>This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.</p>
      </td>

      <td>
        <p>The CleverTap SDK recognizes when a notification sent via CleverTap is viewed by a user.</p><p><em>Notification Viewed</em> is available for email, web push, in-app, web popup, and app inbox.</p><p>Important Properties:</p><ul><li>wzrk\_pivot: String value containing an A/B testing campaign's variant name.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Clicked</p>
      </td>

      <td>
        <p>This event is tracked only when a user clicks on a campaign sent via CleverTap. You can track or create a <em>Notification Clicked</em> event for every <em>UTM Visited</em> event that is tracked by CleverTap and not any other provider. There is no separate event storage required for the <em>Notification Clicked</em> event because it is derived from the <em>UTM Visited</em> event.</p>
      </td>

      <td>
        <p>Recorded when a user clicks on a mobile push, in-app, email, web-popup, a CleverTap shortened link, or web push message sent via the CleverTap dashboard or through the campaign API. </p><p>The Android push notifications containing deep links to third-party apps are not tracked.</p><p>Important Properties:</p><ul><li>wzrk\_pivot: String value containing an A/B testing campaign's variant name.</li><li>wzrk\_c2a: String value containing the action button name of notification clicked events. In the case of SMS, this would contain the original unshortened deep link. </li><li>wzrk\_c2a\_short\_url: String value containing the short URL, shortened using CleverTap link shortening.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Impressions</p>
      </td>

      <td>
        <p>This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the <em>Push</em> campaign statistics page reflects the count for this event.</p>
      </td>

      <td>
        <p>After the toggle for <em>Push Impressions</em> is turned on/setup from settings, the CleverTap SDK starts recording an event whenever a push notification sent via CleverTap is delivered to the user’s device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>App Version Changed</p>
      </td>

      <td>
        <p>This event is raised when a user’s current app version is different from the user’s previous app version.</p>
      </td>

      <td>
        <p>This event is tracked when the <em>CT App version</em> system property differs from one <em>App Launched</em> event to another.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Replied</p>
      </td>

      <td>
        <p>This event is recorded when a user replies to a WhatsApp message.</p>
      </td>

      <td>
        <p>This event is raised when the brand receives a reply from the user.</p><p>Properties:</p><ul><li><p>Incoming Message Type: Represents the type of message received (text, image, document etc.)</p></li><li><p>Channel: String value that represents the medium of incoming message.</p></li><li><p>Incoming text: String value that  represents the incoming message The maximum length of message is set to 256 characters. </p></li><li><p>Incoming Media URL: String value that represents the URL of the media included in the message.</p></li><li><p>Destination WABA number:  String value that represents the  WABA number to which message was sent.</p></li><li><p>Source WABA number: String value that represents the WABA number from which the user replied.</p></li><li><p>Campaign ID: String value that represents the original campaign ID to which the user has replied</p></li><li><p>Provider: String value that represents the source WABA number provider</p></li><li><p>Lat: Float value that represents latitude of the particular location.</p></li><li><p>Long: Float value that represents longitude of the particular location.</p></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reply Sent</p>
      </td>

      <td>
        <p>This event is recorded when an agent (CleverTap user) replies to a message from the end user.</p>
      </td>

      <td>
        <p>This event is raised against the user profile of the end user.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>State Transitioned</p>
      </td>

      <td>
        <p>This event is recorded for lifecycle optimizer when a user transitions from one stage to another.</p>
      </td>

      <td>
        <p>This event is raised whenever a user transitions from one state to another or from unmapped to one of the states in the lifecycle optimization framework. It is meant for internal usage at CleverTap and therefore, unavailable for querying.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Session Concluded</p>
      </td>

      <td>
        <p>This event is recorded to mark the end of a session. Session tracking must be enabled for the event to be tracked.</p>
      </td>

      <td>
        <p>This event is raised when there is 20 minutes of inactivity after an event is raised for a user.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Geocluster Entered</p>
      </td>

      <td>
        <p>This event is recorded to mark when a device enters a geofence. </p><p>The event will only be applicable for customers who have the geofence feature enabled for them.</p>
      </td>

      <td>
        <p>Properties:</p><ol><li>Cluster ID</li><li>Cluster name</li><li>Geofence ID</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        <p>Geocluster Exited</p>
      </td>

      <td>
        <p>This event is recorded to mark when a device exits a geofence.<br />The event will only be applicable for customers who have the geofence feature enabled for them.</p>
      </td>

      <td>
        <p>Properties:</p><ol><li>Cluster ID</li><li>Cluster name</li><li>Geofence ID</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        <p>Channel Unsubscribed</p>
      </td>

      <td>
        <p>This event is raised when an email is not acknowledged.</p>
      </td>

      <td>
        <p>Properties:</p><ol><li>Campaign ID: This is the ID of<br />the campaign from which user are updating subscriptions.<br />Campaign Type: Currently only email.</li><li>Group: Group name from which the user unsubscribed/resubscribed.</li><li>Identity: The user identity/email address.</li><li>Variant</li><li>Type: Valid values are bounced, dropped, and spam. Email IDs which bounce, drop or marked as spam are opted out from future emails.</li><li>Subscription Type: Account level and Profile level.<ul><li>Profile Level: The specific profile is opted out for all email campaigns in the future until they opt in again.</li><li>Account Level: The specific profile and email address is opted out from all email campaigns. Even if other profiles have that email address, they will not be sent emails in the future because that email address has been unsubscribed at the account level.</li></ul></li><li>Reason: Reason which was given by the email provider for the type of the error. For example: "smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces."</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        Notification Replied
      </td>

      <td>
        This event is recorded when a user replies to a WhatsApp message.
      </td>

      <td>
        This event is raised when the brand receives a reply from the user.
      </td>
    </tr>

    <tr>
      <td>
        Notification Delivered
      </td>

      <td>
        This is an event raised only for  WhatsApp. It checks if the WhatsApp notification has reached the end-user.
      </td>

      <td>
        It is raised when the WhatsApp provider confirms that the notification has reached the end user (double-tick of WhatsApp).
      </td>
    </tr>

    <tr>
      <td>
        Reply Sent
      </td>

      <td>
        This is an event raised only for  WhatsApp. This event is recorded when an agent (CleverTap user) replies to a WhatsApp message from the end user.
      </td>

      <td>
        This event is raised against the user profile of the end user.
      </td>
    </tr>

    <tr>
      <td>
        App Upgraded
      </td>

      <td>
        This event is raised when a user’s current app version is different from the user’s previous app version.
      </td>

      <td>
        This event is tracked when the 

        *CT App version*

         system property for an app launch is different from the next app launch.
      </td>
    </tr>

    <tr>
      <td>
        Session Concluded
      </td>

      <td>
        This event is recorded to mark the end of a session. Session tracking must be enabled for the event to be tracked.
      </td>

      <td>
        This event is raised when there is 20 minutes of inactivity after an event is raised for a user.
      </td>
    </tr>

    <tr>
      <td>
        State Transitioned
      </td>

      <td>
        This is an event raised only for  

        *Lifecycle Optimizer*

        . This event is recorded when a user transitions from one stage to another.
      </td>

      <td>
        This event is raised whenever a user is assigned a state or there is a transition from one state to another. It is meant for internal usage at CleverTap and, therefore, unavailable for querying.
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Entered
      </td>

      <td>
        The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device enters a geofence.
      </td>

      <td>
        The event is tracked whenever a device enters a geofence.
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Exited
      </td>

      <td>
        The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device exits a geofence.
      </td>

      <td>
        The event is tracked whenever a device exits a geofence.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rendered
      </td>

      <td>
        This event indicates that the variant has reached the device.
      </td>

      <td>
        Event is raised when you are using the 

        *Product A/B Tests*

         feature.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rolled Out
      </td>

      <td>
        This event is raised when the winner variant is sent to all devices.
      </td>

      <td>
        Event is raised when you are using the 

        *Product A/B Tests*

         feature.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Stopped
      </td>

      <td>
        This event is raised when the experiment was stopped.
      </td>

      <td>
        Event is raised when you are using the 

        *Product A/B Tests*

         feature.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Disqualified
      </td>

      <td>
        This event is raised when the device is disqualified.
      </td>

      <td>
        Event is raised when you are using the 

        *Product A/B Tests*

         feature.
      </td>
    </tr>

    <tr>
      <td>
        Partner Sync
      </td>

      <td>
        An event is raised for each user profile that is part of cohorts imported from partners like Mixpanel.
      </td>

      <td>
        The Partner Sync event is raised every time CleverTap receives a cohort sync request from partners like Mixpanel. This event is raised for each user in the cohort sync.
      </td>
    </tr>
  </tbody>
</Table>
# Debug Events

Debug events are events recorded automatically after you integrate our SDK. These events are raised at certain lifecycle stages in your integration and help you track and manage your integration. These events are available on any profile page and *Find People* page by adding a parameter to the end of the URL `?showDebugEvents=true`.  


<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Event Name</p>
      </th>

      <th>
        <p>Description</p>
      </th>

      <th>
        <p>When is it raised</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Identity Set</p>
      </td>

      <td>
        <p>This debug event is raised when a new user is identified on a customer’s app or an identified user pushes another identity.</p>
      </td>

      <td>
        <p>This event monitors the status and data points that are important for the identification and engagement of users. This event is for monitoring and debugging only.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Identity Reset</p>
      </td>

      <td>
        <p>This debug event is raised when a profile is demerged (after demerged, a new profile for every device is created and identities are dropped) either from the dashboard (click on the <em>Profile</em> page to reset identities) or through the <em>Demerge Profile API</em>.</p>
      </td>

      <td>
        <p>It monitors the reset of identities and handles unnecessary merges. This event is used for monitoring and debugging only.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Identity Error</p>
      </td>

      <td>
        <p>This debug event is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile.</p>
      </td>

      <td>
        <p>This event is for monitoring and debugging when identity merges are invalid.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reachable By</p>
      </td>

      <td>
        <p>This debug event is raised when a user becomes reachable by a communication channel such as SMS, email, mobile push, or when there are changes to the existing communication channel.</p>
      </td>

      <td>
        <p>Tracked for a profile when:</p><ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed. </li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Unregistered</p>
      </td>

      <td>
        <p>This event tracks the removal of a mobile push token.</p>
      </td>

      <td>
        <p>This debug event is raised when an existing mobile push token is removed for a profile.</p><p>Tracked for a profile when:</p><ul><li><p>A user logs out of the device and another user logs in. Applicable only if the <code>onUserLogin()</code> method is implemented. </p></li><li><p>When a push token is removed using the <code>pushFcmRegisterationId("token",false)</code> method. Applicable only for Android.</p></li></ul>
      </td>
    </tr>
  </tbody>
</Table>


# Custom Events

Custom events are events you define and track with our SDK or API. For more information, refer to the [Events](https://developer.clevertap.com/docs/events#custom-events) in the developer documentation.

# Event Data Types

CleverTap supports the following data types:

* String
* Integer
* Float
* Boolean
* Mixed

You can use an array only with the Charged event. All others will return an incorrect data type if using an array.

# Event Metadata Recorded Automatically

For every recorded event, CleverTap records the following standard metadata:

* Information about the user who performed the event.
* Date and time when the event was recorded.
* The number of screens viewed by the user before performing the action.
* The referring site and the source of the user visit if it was from an external source.

In addition, CleverTap keeps the user profiles updated with the latest:

* Geographic information like their city, region, country, and latitude/longitude (if available).
* Browser, device make, or model used to access the website or app.

# System Properties

CleverTap tracks the following system properties automatically from the mobile SDK. All the system properties are prefixed by *CT* indicating that they are provided by CleverTap. 

The following properties are tracked automatically on all events:


<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>System Property</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>CT App Version</p>
      </td>

      <td>
        <p>This is the current version of your application installed on the user device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Latitude</p>
      </td>

      <td>
        <p>The user location identified by the latitude.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Longitude</p>
      </td>

      <td>
        <p>The user location identified by the longitude.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Source</p>
      </td>

      <td>
        <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

The following properties are available on the *App Launched* event:


<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>System Property</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>CT App Version</p>
      </td>

      <td>
        <p>This is the current version of your application installed on the user device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Latitude</p>
      </td>

      <td>
        <p>The user location identified by the latitude.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Longitude</p>
      </td>

      <td>
        <p>The user location identified by the longitude.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT OS Version</p>
      </td>

      <td>
        <p>The operating system of the device.<br />For example,  1.0.0.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT SDK Version</p>
      </td>

      <td>
        <p>The CleverTap SDK version. For example, 30501.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Network Carrier</p>
      </td>

      <td>
        <p>The network carrier of the device.<br />For example, AT\&T, Vodafone.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Network Type</p>
      </td>

      <td>
        <p>The network type of the device.<br />For example, 4G.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Connected To WiFi</p>
      </td>

      <td>
        <p>Indicates if the device is connected to the Wi-FI.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Bluetooth Version</p>
      </td>

      <td>
        <p>The Bluetooth version of the device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Bluetooth Enabled</p>
      </td>

      <td>
        <p>Indicates if Bluetooth is enabled on the device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Source</p>
      </td>

      <td>
        <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul>
      </td>
    </tr>
  </tbody>
</Table>


> 📘 Latitude and Longitude
>
> The system properties *latitude* and *longitude* are captured and sent from the SDK only if the user gives consent on your app.