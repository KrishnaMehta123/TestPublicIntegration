---
title: Events
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

Events track what individual actions users perform in your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item. 

By tracking events in your app, you can better understand what users are doing. In CleverTap, you can analyze these events in many different ways, such as getting aggregating metrics of a specific event or measuring how a specific event type trends over time. You can also engage with your users based on these events by creating campaigns in CleverTap that are triggered by them. 

<Image title="events1.png" alt={898} align="center" className="border" width="80%" border={true} src="https://files.readme.io/40b874a-events1.png" />

## Event Categories

CleverTap has two categories of events:

* System events: Events recorded automatically after you integrate our SDK. 
* Custom events: Events you define and track with our SDK or API.

## Event Properties

Events have details that describe the action taking place called properties. 

For example, while recording the *Product viewed* event, you could also store event properties, such as product name, category, and price. Recording event properties will help you discover insights, such as which product category is more popular, and segment users based on which categories or price points they have viewed.

# System Events

> 📘 Events Changelog
>
> You can find information about the most recent changes to our existing system events or the introduction of new ones in our [Events Changelog](doc:events-changelog).

System events are events recorded automatically after you integrate our SDK. 


<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        <p>

        Event Type

        </p>
      </th>

      <th>
        <p>

        Description

        </p>
      </th>

      <th>
        <p>

        How Event is Tracked

        </p>
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
        <p>There are two cases when this event will be recorded. The first case is a fresh app launch, which is when an app is launched from a killed state. The second case is when an app is brought to the foreground after 20 minutes of inactivity in the background.</p>
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
        <p>This event is tracked by sending silent push notifications which is a type of notification that is not rendered on a user’s device. We send silent push notifications to your entire install base once every 24 hours to track uninstalls. For more information, refer to <a href="https://clevertap.com/blog/track-app-uninstalls-effectively/">App Uninstall</a>.</p>
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
        <p>This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Singular, sends this information to CleverTap.</p>
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
        <p>This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, and web push campaigns. The <em>Notification Sent</em> event is available on the <em>Event</em> dashboard but it is not displayed on the <em>User Profile</em>.</p>
      </td>

      <td>
        <p>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        Notification Failed
      </td>

      <td>
        This event logs campaign errors in CleverTap.
      </td>

      <td>
        <ul><li>Campaign ID**: ** It helps identify the specific campaign associated with the error.</li><li>Campaign Type**:**  It indicates the type of campaign (for example, WhatsApp, SMS, Email, and so on).</li><li>Error: It displays the error message for the error observed in the campaign.</li><li>Label: It denotes the specific label associated with the campaign.</li><li>Variant: It helps identify the errors for a specific campaign variant in the case of A/B, split delivery, or multi-variant campaigns.</li></ul>For detailed information on WhatsApp errors, refer to [WhatsApp Error Stats](doc:whatsapp-stats).   **Note**:  This event is currently in Private Beta for Email Campaigns. Contact your account manager to enable it.
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
        <p>The CleverTap SDK recognizes when a notification sent via CleverTap is viewed by a user.</p><p><em>Notification Viewed</em> is available for email, web push, in-app, web popup, and app inbox.</p><p>Important Properties:</p><ul><li>Variant: String value containing an A/B testing campaign's variant name.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Clicked</p>
      </td>

      <td>
        <p>This event is tracked only when a user clicks on a campaign sent via CleverTap. You can track or create a <em>Notification Clicked</em> event for every <em>UTM Visited</em> event that is tracked by CleverTap and not any other provider.  </p><p>There is no separate event storage required for the <em>Notification Clicked</em> event because it is derived from the <em>UTM Visited</em> event.</p>
      </td>

      <td>
        <p>Recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API. </p><p>The Android push notifications containing deep links to third-party apps are not tracked.</p><p>Important Properties:</p><ul><li>Variant: String value containing an A/B testing campaign's variant name.</li><li>wzrk_c2a: String value containing the action button name of notification clicked events.</li> <li> button_id: Visible only when the Notification Clicked event is tracked for button clicks associated with the Image Interstitial template.</ul> <p> The "Notification Clicked" event is triggered only for CleverTap BSP users if Click tracking is enabled when creating WhatsApp campaigns </p>
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
        <p>This event is recorded when a user replies to a SMS campaign.</p>
      </td>

      <td>
        <p>This event is raised when the brand receives a reply from the user.</p><p>Properties:</p><ul><li><p>Incoming Message Type: Represents the type of message received (text, image, document, etc.)</p></li><li><p>Channel: String value that represents the medium of the incoming message.</p></li><li><p>Incoming text: String value that represents the incoming message. In the case of an SMS campaign, it includes the reply message sent by the SMS recipient. The maximum length of the message is set to 512 characters. </p></li><li><p>Incoming Media URL: String value that represents the URL of the media included in the message.</p></li><li><p>Campaign ID: String value that represents the original campaign ID to which the user has replied</p></li><li><p>Lat: Float value that represents the latitude of the particular location.</p></li><li><p>Long: Float value that represents the longitude of the particular location.</p></li></ul>
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
        <p>Properties:</p><ol><li>Cluster ID</li><li>Cluster name</li><li>Geofence ID</li></ol><p>The event is tracked whenever a device enters a geofence.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Geocluster Exited</p>
      </td>

      <td>
        <p>This event is recorded to mark when a device exits a geofence. </p><p>The event will only be applicable for customers who have the geofence feature enabled for them.</p>
      </td>

      <td>
        <p>Properties:</p><ol><li>Cluster ID</li><li>Cluster name</li><li>Geofence ID</li></ol><p>The event is tracked whenever a device exits a geofence.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Channel Unsubscribed</p>
      </td>

      <td>
        <p>This event is raised only for Email and Push campaigns. It is raised when end-users unsubscribe from future emails and push notifications. It is also raised when the user resubscribes for the email campaigns</p>
      </td>

      <td>
        <p>Properties:</p><ol><li>Campaign ID: This is the ID of<br />the campaign from which user are updating subscriptions.<br />Campaign Type: Currently only present for Email Campaigns.</li><li>Group: Group name from which the user unsubscribed/resubscribed.</li><li>Identity: The user identity/email address.</li><li>Variant</li><li>Type: Valid values are bounced, dropped, and spam. Email IDs that bounce, drop, or are marked as spam are opted out of future emails.</li><li>Subscription Type: Account level and Profile level.<ul><li>Profile Level: The specific profile is opted out for all email campaigns in the future until they opt in again.</li><li>Account Level: The specific profile and email address are opted out of all email campaigns. Even if other profiles have that email address, they will not be sent emails in the future because that email address has been unsubscribed at the account level.</li></ul></li><li> Resubscribed: The value is true if the user has resubscribed, or else the value will be false.</li><li>Reason: Currently, present for email campaigns only. It is the same reason that was given by the email provider for the type of error. For example: "smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces."</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        Channel Subscribed
      </td>

      <td>
        This event is raised when the user subscribes to a push notification channel for devices with Android OS version 13 and above. For devices on Android 13 and above, the event is raised when the user gives permission. For devices on Android 12, the event is raised when the user resubscribes for the push campaigns.
      </td>

      <td>
        <p>Properties:</p> <ul><li>Source: Indicates if the event is raised through a device, application, or API. </li> <li> Channel: Indicates the channel for which the user has subscribed i.e. Push Notification. </li> <li>App Version: Indicates the app version from which the event is raised. </li> <li> SDK Version: Indicates the SDK version installed on the device. </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Notification Delivered
      </td>

      <td>
        This is an event raised only for Email, WhatsApp and SMS campaigns.
      </td>

      <td>
        <li> In the case of Email campaigns, it is raised when the provider confirms that the email campaign is delivered to the recipient mail server. In most cases, this indicates successful delivery to the end user. For campaigns sent via Generic SMTP, CleverTap should receive a [callback](doc:generic-smtp-v2-payload) to raise this event.  **Note**: [Notification Delivered](doc:email-campaign-stats-delivered) is currently released in Private Beta for Infobip (in the case of Advanced Email add-on) and Sendgrid email providers. Contact your Customer Success Manager for access.</li> <li> In the case of SMS campaigns, it is raised when the notification is delivered to the end user, and CleverTap receives the [callback](doc:generic-sms#sms-callbacks). It includes the `Provider` event property, a string value that represents the service through which the campaign is sent. For example, Twilio.</li> <li> In the case of WhatsApp, it is raised when the provider confirms that the notification has reached the end user (double-tick of WhatsApp). </li>
      </td>
    </tr>

    <tr>
      <td>
        App Upgraded
      </td>

      <td>
        This event is raised when a user’s current app version differs from their previous app version.
      </td>

      <td>
        This event is tracked when the *CT App version* system property for an app launch is different from the next app launch.
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
        This is an event raised only for  *Lifecycle Optimizer*.This event is recorded when a user transitions from one stage to another.
      </td>

      <td>
        This event is raised whenever a user is assigned a state or there is a transition from one state to another. It is meant for internal usage at CleverTap and therefore, unavailable for querying.
      </td>
    </tr>

    <tr>
      <td>
        AB Test Enter
      </td>

      <td>
        This event helps analyze the devices that have an A/B Test running on them. It also gives you the specific variant selected for the device.
      </td>

      <td>
        This event is raised when the device qualifies for an A/B Test as part of a Product Experience (PE).
      </td>
    </tr>

    <tr>
      <td>
        AB Test Exit
      </td>

      <td>
        This event helps analyze the devices that have exited an A/B Test.
      </td>

      <td>
        This event is raised when the goal of the A/B test is achieved.
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
        Event is raised when you are using the \_Product A/B Tests \_feature.
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
        Event is raised when you are using the \_Product A/B Tests \_feature.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Stopped
      </td>

      <td>
        This event is raised when experiment was stopped.
      </td>

      <td>
        Event is raised when you are using the \_Product A/B Tests \_feature.
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
        Event is raised when you are using the \_Product A/B Tests \_feature.
      </td>
    </tr>

    <tr>
      <td>
        Partner Sync
      </td>

      <td>
        An event raised for each user profile that is part of cohorts imported from partners like Mixpanel.
      </td>

      <td>
        The Partner Sync event is raised every time CleverTap receives a cohort sync request from partners like Mixpanel. This event is raised for each user in the cohort sync.
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Coupon Rewarded</p>
      </td>

      <td>
        This event is raised when the coupon is issued to a user through a Promo campaign.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about rewarding the coupon:<ul> <li><strong>Coupon Name</strong>: Name of the coupon configured for bulk coupon series. Applicable when using bulk coupon codes.</li> <li><strong>Coupon Code</strong>: The unique coupon code issued. Applicable for single-code coupons.</li> <li><strong>Coupon ID</strong>: A unique identifier assigned to the coupon instance.</li> <li><strong>Campaign ID</strong>: Identifier of the campaign that issued the coupon to the user.</li> <li><strong>Description</strong>: Textual description of the coupon as configured in the campaign settings.</li> <li><strong>Event Timestamp</strong>: The exact date and time when this event was recorded in CleverTap.</li> <li><strong>Terms and Condition</strong>: Promotional terms defined for coupon usage.</li> <li><strong>Coupon Start Date</strong>: Date and time when the coupon becomes valid for use. <ul><li>Format: <code>DD-MM-YYYY HH:MM:SS</code></li></ul> </li> <li><strong>Redemption Activation Date</strong>: If an activation delay is configured, this field defines when redemption becomes possible. <ul><li>Format: <code>DD-MM-YYYY HH:MM:SS</code></li></ul> </li> </ul> </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Coupon Redeemed</p>
      </td>

      <td>
        This event is raised when the user redeems the coupon through the redemption API.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about the redemption of the coupon:<ul> <li><strong>Redeemed Type</strong>: Indicates the type of benefit originally redeemed using the coupon. <ul><li>Values could include: <code>discount</code>, <code>cashback</code></li></ul> </li> <li><strong>Order ID</strong>: The ID of the order for which the coupon was applied and subsequently redeemed. Helps map the reversal back to the original transaction. </li> <li><strong>Event Timestamp</strong>: The exact date and time when the redeemed event was logged in CleverTap. Useful for auditing, ordering, and reporting. </li> <li><strong>Discount Amount</strong>: The monetary value of the discount that was redeemed. Applicable if the original reward was a discount coupon. </li> <li><strong>Coupon Name</strong>: Name of the coupon used during redemption. Typically configured at the coupon level. </li> <li><strong>Coupon ID</strong>: Unique identifier for the coupon that is being redeemed.</li> <li><strong>Coupon Code</strong>: Coupon code that was redeemed.</li> <li><strong>Cashback Points</strong>: Points value credited to the user's wallet linked to cashback when users redeem the cashback coupon.</li> <li><strong>Discount Amount</strong>: The amount of discount redeemed by the user. Applicable when the user redeems the discount coupon.</li> </ul> </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Coupon Reverted</p>
      </td>

      <td>
        This event is raised when a redeemed coupon is reversed.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about the redemption of the coupon:<ul> <li><strong>Redeemed Type</strong>: Indicates the type of benefit originally redeemed using the coupon. <ul><li>Values could include: <code>discount</code>, <code>cashback</code></li></ul> </li> <li><strong>Order ID</strong>: The ID of the order for which the coupon was applied and subsequently reverted. Helps map the reversal back to the original transaction. </li> <li><strong>Event Timestamp</strong>: The exact date and time when the reverted event was logged in CleverTap. Useful for auditing, ordering, and reporting. </li> <li><strong>Discount Amount</strong>: The monetary value of the discount that was reverted. Applicable if the original reward was a discount coupon. </li> <li><strong>Coupon Name</strong>: Name of the coupon used during reversal. Typically configured at the coupon level. </li> <li><strong>Coupon ID</strong>: Unique identifier for the coupon that is being reverted.</li> <li><strong>Coupon Code</strong>: Coupon code that was reverted.</li> <li><strong>Cashback Points</strong>: Points value debited to the user's wallet linked to cashback when users revert the cashback coupon.</li> <li><strong>Discount Amount</strong>: The amount of discount reverted by the user. Applicable when the user redeems the discount coupon.</li> </ul> </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Points Credited</p>
      </td>

      <td>
        This event is raised when points are added to the loyalty wallet.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about the credited points to the wallet: <ul> <li><strong>Points Expiry</strong>: The expiration date/time of the credited points. Defines when the awarded points will no longer be valid.</li> <ul><li>Format: <code>DD-MM-YYYY HH:MM:SS</code></li></ul> <li><strong>Wallet ID</strong>: Unique identifier for the wallet where points are being credited. Used to distinguish between multiple wallet types if applicable.</li> <li><strong>Transaction ID</strong>: Unique ID assigned to the point credit transaction. Useful for audit trails, debugging, and reporting. </li> <li><strong>Source</strong>: Identifies how the credit was initiated. <ul><li>Possible values: <code>API</code>, <code>Campaign</code>, <code>Manual</code>, <code>Cashback Coupon</code></li></ul> </li> <li><strong>Points Description</strong>: Descriptive label for the credit transaction. Configured during campaign or API call to explain why points were awarded.</li> <li><strong>Points</strong>: Number of points credited to the wallet. <ul><li>Numeric value, e.g., 25 or 100.</li></ul> </li> <li><strong>Event Timestamp</strong>: Timestamp representing when the event was logged in CleverTap. Used for tracking, filtering, and campaign attribution. </li> <li><strong>Campaign ID</strong>: The ID of the campaign responsible for the point credit. Applicable only if the source of credit is a campaign.</li>  <li><strong>Coupon Code</strong>: Indicates the specific coupon code whose redemption resulted in the crediting of points. Applicable when the source is a cashback coupon.</li> <li><strong>Coupon ID</strong>: Refers to the unique coupon ID associated with the redemption that triggered the points credit. Applicable when the source is a cashback coupon.</li> <li><strong>Sale Channel</strong>: The source channel for the transaction (e.g., Mobile, Web, POS). Applies to credit transactions created via API.</li> <li><strong>Location ID</strong>: Identifier for the transaction location (e.g., store code). Applies to credit transactions created via API.</li> <li><strong>Sale Amount</strong>: Gross order value tied to the transaction.</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Points Debited</p>
      </td>

      <td>
        This event is raised when points are deducted from the loyalty wallet.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about the debited points to the wallet:<ul> <li><strong>Wallet ID</strong>: Unique identifier for the wallet from which points are debited. Used to map the transaction to a specific reward wallet.</li> <li><strong>Transaction ID</strong>: Unique ID associated with the debit transaction. Useful for reconciliation and debugging. </li> <li><strong>Source</strong>: Indicates how the debit was triggered. <ul><li>Possible values include: <code>API</code>, <code>Manual</code>, <code>Campaign</code>, etc.</li></ul> </li> <li><strong>Points Description</strong>: Descriptive text or label explaining the context of the points debit. Configured during campaign or API setup.</li></ul> </li> <li><strong>Points</strong>: Number of points debited from the wallet. <ul><li>Numeric value, e.g., 10 or 50.</li></ul> </li> <li><strong>Event Timestamp</strong>: The exact time when the points debit action occurred and was logged in CleverTap. Auto-recorded for chronological tracking. </li> <li><strong>Campaign ID</strong>: ID of the campaign that triggered the debit (if applicable). Helps link the debit to a promotional action. </li> <li><strong>Sale Channel</strong>: The source channel for the transaction (e.g., Mobile, Web, POS). Applies to debit transactions created via API.</li> <li><strong>Location ID</strong>: Identifier for the transaction location (e.g., store code). Applies to debit transactions created via API.</li> <li><strong>Sale Amount</strong>: Gross order value tied to the transaction.</li> </ul> </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>CT Partner Voucher Rewarded</p>
      </td>

      <td>
        This event is raised when a user receives a third-party partner voucher.
      </td>

      <td>
        The following properties are captured as part of this event to provide additional context about the debited points to the wallet:<ul> <li><strong>Voucher List ID</strong>: Unique identifier assigned to the partner voucher list. Used to associate the voucher with its originating list.</li> <li><strong>Voucher Code</strong>: The actual voucher code issued to the user. Can be redeemed on a partner platform or used for benefit claims. </li> <li><strong>Source</strong>: The origin through which the voucher was issued. <ul><li>Typical values: <code>API</code>, <code>Campaign</code></li></ul> <li><strong>Partner</strong>: Name of the third-party or partner platform that provided the voucher. Used for tracking and analytics of partner-level voucher distribution. </li> <li><strong>List Tag</strong>: Tag or label associated with the voucher list. Useful for categorization, segmentation, or filtering of voucher campaigns. </li> <li><strong>List Expiry</strong>: Expiration date/time for the voucher list or voucher code. Determines the validity period of the voucher.<ul><li>Format: <code>DD-MM-YYYY HH:MM:SS</code></li></ul> <li><strong>List Description</strong>: Description of the voucher list as configured in the system. May include offer details, partner terms, or redemption instructions. </li> <li><strong>Event Timestamp</strong>: The exact date and time when the voucher was rewarded to the user. Captured automatically by CleverTap for logging and analysis.</li> <li><strong>Campaign ID</strong>: ID of the campaign that rewarded the voucher. Links the voucher issuance to the triggering promo campaign. </li> </ul>
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
        <p>This event tracks the removal of a mobile push token. It is also raised when FCM returns a 404 Unregistered error for stale tokens from devices that have not connected to FCM for 270 days or for users who uninstall the app.</p>
      </td>

      <td>
        <p>This event is raised when an existing mobile push token is removed for a profile.</p><p>Tracked for a profile when:</p><ul><li><p>A user logs out of the device, and another user logs in. Applicable only if the <code>onUserLogin()</code> method is implemented. </p></li><li><p>When a push token is removed using the <code>pushFcmRegisterationId("token",false)</code> method. Applicable only for Android.</p></li><li> FCM returns a [404 Unregistered error](https://firebase.google.com/docs/reference/fcm/rest/v1/ErrorCode) for stale tokens from devices that have not connected to FCM for 270 days or for users who have uninstalled the app. </li> </ul>
      </td>
    </tr>
  </tbody>
</Table>


# Custom Events

Custom events are events you define and track with our SDK or API. For more information, refer to the [Events](https://developer.clevertap.com/docs/events#custom-events) in the developer documentation.

## Charged Event

CleverTap also records transactions or purchases using a special event called **Charged**. Clevertap enriches this special event with additional information such as items sold, their categories, transaction amount, transaction ID, and information about your users. Recording a purchase against a user marks them as a customer in CleverTap and enables you to compare your funnel reports between customers and other users.

When recording customer purchases, you can also record the following: 

* Items Sold\
  You must use the Items collection to record a list of items sold. Along with the product name, you can add properties such as size, color, category, etc.

* Transaction Amount\
  The transaction total or subscription charge must be recorded in an event property called Amount.

For more information about recording a Charged event, refer to [Events](https://developer.clevertap.com/docs/events#recording-customer-purchases) under developer documentation.

### Advantages of the Charged Event

The following are the advantages of Charged event:

* Helps you identify your customers and how they are using your app or website
* Run campaigns to reward loyal users or get lost customers back
* Measure customer loyalty via running a cohort analysis on repeat purchases
* Analyze paid campaign performance by total revenue earned
* Get revenue insights like – total revenue, number of transactions, count of paying users, and much more

### Charged Event Personalization

You can personalize the message for customers who purchase multiple items in a single transaction. You can do so by using liquid tags from the CleverTap dashboard, as shown in the following sample codes:

* **Using for Loops in Liquid Tags** 




























































































































































































































































































* **Using Manual Indexing in Liquid Tags** 























































































































































































































































































































































































`Event.items` is a custom array property that you can use to store additional information about items associated with an event. It allows you to include item-specific details when tracking events. For example, if an event called "Charged" represents a user making a purchase, you can use the `Charged.Items` array to store information about the specific items purchased within that event. Each item in the array can have its own properties, such as name, price, quantity, and so.

You can personalize the message for any number of items in the `Event.items` array. For example, you want to send an email including order details to the customers who bought three books from your e-commerce website. The `Event.items` array, in this case, would include three items, and you can send a personalized message for all three items. 

<Image alt="Charged Event Personalization" align="center" border={true} src="https://files.readme.io/aef5e4b-Charged_Event_Personalization.png" /> Charged Event Personalization











In the case of manual indexing, you can ensure that the index is smaller than the size of the Items array using `Event.Items.size`. If the index value exceeds the size of the Items array, the message is NOT dispatched and is marked against errors.

> 📘 Charged Event Personalization for App Inbox Campaigns
>
> * In the case of App Inbox campaigns, event personalization for `Charged.Items` is not enabled. 
> * However, if you use event personalization with `Charged.Items`, the default values for the items are displayed in the case of App Inbox campaigns.
> * If you use event personalization with `Charged.Items` when creating a combination of Push Notification and App Inbox campaigns, the personalized values for the items are displayed for Push and default values are displayed for App Inbox.

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