---
title: Journey Concepts
excerpt: >-
  Understand how to define Journey constituents like nodes, links, and sleep
  time.
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

This section covers the following Journey concepts: 

* [Journey States](doc:journey-states)
* [Journey Components](https://docs.clevertap.com/docs/journey-concepts#journey-components)
* [Journey Procedures and Outcomes](https://docs.clevertap.com/docs/journey-components#journey-procedures-and-outcomes)

# Journey Components

A Journey is configured using a combination of the following components: 

* [Journey Nodes](https://docs.clevertap.com/docs/journey-components#journey-nodes-nodes)
  * [Segment Nodes](https://docs.clevertap.com/docs/journey-concepts#segment-nodes)
  * [Engagement Nodes](https://docs.clevertap.com/docs/journey-concepts#engagement-nodes)
    * [Engagement Node Actions](https://docs.clevertap.com/docs/journey-concepts#engagement-node-actions)
  * [Controller Nodes](https://docs.clevertap.com/docs/journey-concepts#controller-nodes)
* [Journey Connections](https://docs.clevertap.com/docs/journey-concepts#journey-connections)
  * [Journey Links](https://docs.clevertap.com/docs/journey-concepts#journey-links)
  * [Sleep Time](https://docs.clevertap.com/docs/journey-concepts#sleep-time)

## Journey Nodes

Nodes are different entry and exit points for user navigation.\
The user navigates from a milestone to the intended one through different nodes, depending on the route they take.\
For example, you want the user to register and purchase a product on your platform after installing the app. When the user registers on your platform after app installation, a journey to purchase a product activates. However, if the user does not register on your platform even after app installation, you can activate a journey that nudges them to register on the platform.\
Nodes make it possible to automatically detect the route that the user takes, in order to steer them to the next relevant node.

A Journey is a combination of *Segment* nodes and *Engagement* nodes. You can connect *Segment* nodes and *Engagement* nodes to each other to create powerful automation.\
When compared with Campaigns, the *Segment* nodes define the audience, and *Engagement* nodes define the target. 

### Segment Nodes

*Segment* nodes are various points in a journey to qualify users based on certain events.\
The events may be either entry or navigation points based on the user's action/inaction.\
In case of users not qualifying for a *Segment*, they may either be waiting for qualification or exit the journey, if entered.\
For example, on a successful login creation after installing the app, the user qualifies for a *registered* event. In cases where the user does not create a login, they do not qualify, and based on the journey parameters, they either wait to enter the node or exit the journey.

<Image title="Various segment nodes in Journeys" alt={203} align="center" border={true} src="https://files.readme.io/df13128-Segments_Journey_Components.png">
  Segment Nodes
</Image>

#### Types of Segment Nodes

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Segment Node
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Action
      </td>

      <td>
        Qualification to this node occurs as soon as the user performs the said event.
      </td>

      <td>
        Qualify users as soon as they do *app install*.
      </td>
    </tr>

    <tr>
      <td>
        Inaction
      </td>

      <td>
        Segment users who did the first/initial event, but did not do the second event within a specified time interval.
      </td>

      <td>
        Qualify users who *added to cart*, but did not purchase within five mins.
      </td>
    </tr>

    <tr>
      <td>
        Past Behavior
      </td>

      <td>
        Segment users who performed one event AND did not perform another in the past *n* days.
      </td>

      <td>
        Qualify users who performed *Video Watched* AND did not do *Subscription Paid* in the last 30 days.
      </td>
    </tr>

    <tr>
      <td>
        Date Time
      </td>

      <td>
        Segment users based on a *date time* property value like flight time, due date, travel time, and so on.
      </td>

      <td>
        Qualify users who have their credit card due date in the upcoming week.
      </td>
    </tr>

    <tr>
      <td>
        Journey Trigger
      </td>

      <td>
        * \*Use this node only in the entry criteria\*\*.\
          Segment users based on a different user journey node.
      </td>

      <td>
        Qualify users in current journey when they enter *X* node of another journey.\
        For instance, all users who have received nudges based on *Video Watched* and *Subscription not paid* enter the current journey that offers discount codes for subscribing.̧
      </td>
    </tr>

    <tr>
      <td>
        Custom list
      </td>

      <td>
        * \*Use this node only in the entry criteria\*\*.\
          Upload custom list of users for entry to the Journey.
      </td>

      <td>
        Qualify users based on an uploaded list from your Retail Point of Sale (POS).
      </td>
    </tr>

    <tr>
      <td>
        Page Visit
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users as soon as they visit a specific page.
      </td>

      <td>
        Qualify users as soon as they visit a specific page.
      </td>
    </tr>

    <tr>
      <td>
        Referrer Entry
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users based on a referring website or campaign.
      </td>

      <td>
        Qualify users as soon as they enter your website based on a referring website or campaign.
      </td>
    </tr>

    <tr>
      <td>
        Page Count
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users based on the number of pages visited by them.
      </td>

      <td>
        Qualify users as soon as they visit *X* pages.
      </td>
    </tr>
  </tbody>
</Table>

### Engagement Nodes

*Engagement* nodes are interaction points in a user journey that determine the channel and its message contents. The interaction points are users engaging with nudges/notifications sent to them. Users that do not interact with engagements do not qualify.\
For example, you can qualify users when they click a link in an email to indicate interaction. This enables further engagement to prompt certain user actions.

<Image title="Various engagement nodes in Journeys" alt={406} align="center" width="smart" border={true} src="https://files.readme.io/de9c6a32f3c1859a555eee62f5f9db03f87518731adb3cd2ad553ed8006ecfc9-Engagement_Nodes.png">
  Engagement Nodes
</Image>

#### Types of Engagement Nodes

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Engagement Node
      </th>

      <th>
        Description
      </th>

      <th>
        Node Actions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Push
      </td>

      <td>
        Send push notifications that display in the users' notification tray or the notification inbox.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Clicked</li> <li>Unreachable </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        SMS
      </td>

      <td>
        Send text messages to your app or website users even outside of the app.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Email
      </td>

      <td>
        Send emails to your app or website users
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Viewed</li> <li>Clicked</li> <li>Unreachable </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Webhook
      </td>

      <td>
        Use it to receive push notifications on the app server and track events in a system. You can also connect with an external source (e.g., Chatbots and virtual assistants) to send something via API.
      </td>

      <td>
        <ul> <li>Sent</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Web Push
      </td>

      <td>
        Send browser-based messages to your website users even outside of your website.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Viewed</li> <li>Clicked</li> <li>Unreachable</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Web Pop-up
      </td>

      <td>
        Display pop-up messages on desktop or mobile websites.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        WhatsApp
      </td>

      <td>
        Send WhatsApp messages to your app or website users even outside of the app.To know more, refer 

        [Engagement Nodes - WhatsApp](doc:engagement-nodes-whatsapp)
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Delivered</li> <li>Unreachable </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Exit Intent
      </td>

      <td>
        Display pop-up messages before users leave your website
      </td>

      <td>
        <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        In-app
      </td>

      <td>
        Display pop-up messages while a user is in the app. An In-App renders as soon as the user performs an event.
      </td>

      <td>
        <ul> <li>Viewed</li> <li>Clicked</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Web Native Display
      </td>

      <td>
        Display content on your website without interrupting the user journey.
      </td>

      <td>
        <ul> <li>Viewed</li> <li>Clicked</li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Inbox
      </td>

      <td>
        Send messages that remain accessible after they’re received in the app.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Facebook
      </td>

      <td>
        Send messages to users outside of your app or website via ads on Facebook.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Google
      </td>

      <td>
        Send messages to users outside of your app or website, via ads on Google apps.
      </td>

      <td>
        <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable </li> </ul>
      </td>
    </tr>

    <tr>
      <td>
        Amazon event bridge
      </td>

      <td>
        Interact with Amazon EventBridge(if integrated) to send user action-based notifications.
      </td>

      <td>
        Sent
      </td>
    </tr>

    <tr>
      <td>
        Segment
      </td>

      <td>
        Interact with Segment(if integrated) to personalize engagements based on user actions.
      </td>

      <td>
        Sent
      </td>
    </tr>

    <tr>
      <td>
        mParticle
      </td>

      <td>
        Interact with mParticle(if integrated) to collect user data for rich engagements.
      </td>

      <td>
        Sent
      </td>
    </tr>
  </tbody>
</Table>

#### Engagement Node Actions

This section explains the status of the message delivery and the actions a user may perform on the engagement node. 

| Node Actions    | Description                                                                                                                                                                                                                |
| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sent**        | Indicates that the message is sent from CleverTap and has reached the recipient's device. In the case of a Webhook, the recipient is the system server.                                                                    |
| **Failed**      | Indicates that the sent message could not be delivered to its intended recipient due to specific errors. For example, third-party provider issues.                                                                         |
| **Unreachable** | Indicates that the sent message could not be delivered because the recipient's device or contact information is unavailable. For example, a push token or phone number does not exist.                                     |
| **Viewed**      | Indicates that the user viewed the message sent from CleverTap. For example, the user views an Email or In-App notification.                                                                                               |
| **Clicked**     | Indicates that the user clicked the message sent from CleverTap. For example, the user clicks a Push, In-App, Email, Web Popup, or Web Push message.                                                                       |
| **Delivered**   | In WhatsApp, *Sent* indicates that the message is on its way to the user's device, and *Delivered* indicates that the message has reached the recipient's device. If the user blocks you, the message does not reach them. |

### Controller Nodes

*Controller* Nodes are points in a user journey that perform certain actions. For example, you may exit a user from a journey after completing an *Email Engagement*.

<Image alt="Journey Controllers" align="center" width="40% " border={true} src="https://files.readme.io/3a247ad8c4fb1f2c20c1e25b4862afbb9290663e410d19eff8fc25d499f1eaa9-Journey_Controllers.png">
  Journey Controllers
</Image>

#### Types of Controller Nodes

| Controller Node                                                                                           | Description                                                                                                                                                                                                                                                   |
| :-------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Force exit                                                                                                | Exit a user from a journey.                                                                                                                                                                                                                                   |
| [User profile update](https://docs.clevertap.com/docs/construct-a-journey#using-user-profile-update-node) | Updates a system or custom property. If the user property for the user doesn’t exist in the profile, then the property is created for that user profile. Irrespective of whether the update fails or succeeds, the user moves ahead via the **Updated** path. |
| [IntelliNODE](https://docs.clevertap.com/docs/intellinode)                                                | Define and compare multiple journey variations within a single journey.                                                                                                                                                                                       |

## Journey Connections

You can connect your journey nodes through *links* and specify a *sleep time* before an action. 

### Journey Links

Journey links are routing rules between different nodes. Based on user behavior or action, you can create a connection between a node and link it to distinct nodes.\
For example, when you send push notifications to nudge buying for a segment of new users within the past year but have not purchased anything in the past month, you create a link between the segment node *Past behavior* and the engagement node *Push*.

<Image title="Journey links used to connect different nodes" alt={596} align="center" border={true} src="https://files.readme.io/ddd50bf-Link_Sleep_Time.png">
  Journey Links
</Image>

### Sleep Time

When you choose a journey link and connect it to the engagement node, the **hourglass** ![\*\*hourglass\*\*](https://files.readme.io/edc6717-Hourglass.png) icon appears on the link. Click the **hourglass** ![\*\*hourglass\*\*](https://files.readme.io/edc6717-Hourglass.png) to modify the sleep time. By default, there's no sleep time.

Sleep Time enables you to specify whether to do the specified action immediately or after a gap. You may define the gap in minutes, hours or days.\
In the below figure, you may choose to send the nudge either immediately, as soon as the user qualifies, or wait for a few days before nudging the user.

<Image title="Sleep time component in Journey" alt={449} align="center" border={true} src="https://files.readme.io/1c0073a-Sleep_Time_Journey_Components.png">
  Sleep Time
</Image>

> 📘 Note
>
> The In-App renders as soon as the user performs an event. Hence, sleep time does not apply to In-App. However, to add a delay, add a segment node followed by the In-App node.

# Journey Procedures and Outcomes

The following table describes the procedures and outcomes involved in a Journey: 

| Concept                           | Description                                                                                                                                                                                                                   |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Publish the Journey**           | Makes your journey live.                                                                                                                                                                                                      |
| **Schedule the Journey**          | Activates the journey (users begin entering the journey) at a specified time—either now or at a later date.                                                                                                                   |
| **Initial Run of the Journey**    | The initial run of the journey occurs as soon as it is activated based on the scheduled date and time.                                                                                                                        |
| **Subsequent Run of the Journey** | In the case of a PBS journey, after the initial run, if the journey is set to recurring, subsequent runs occur at 12:00 a.m. the following day. Assuming the recurring day is set to T, the subsequent run occurs on T+1 day. |
