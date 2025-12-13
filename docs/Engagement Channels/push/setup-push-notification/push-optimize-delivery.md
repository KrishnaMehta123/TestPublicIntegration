---
title: Optimize Delivery
excerpt: >-
  Understand how to optimize push messages with Pull Notifications and App
  Inbox.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

You can optimize push delivery using the following two features: 

* Pull Notification 
* Sending the push message to App Inbox 

You can optimize the delivery rate by retrying the *Push* message as is (where messages are suppressed by the device) or by sending it to *App Inbox* when the user enables DND for push messages.

## Optimize Delivery via Pull Notification

Push notifications are a great way to engage customers despite the issue of low deliverability on certain device manufacturers. 

With Pull Notification at your disposal, you can counter this challenge by optimizing the delivery of push notifications to devices that missed receiving them.

To enable this feature, navigate to *Settings* > *Engage* > *Setup* > *Pull Notification*. Toggle ON the Pull Notification as shown in the following figure:

<Image title="Increase Deliverability of Push Notifications" alt={2514} border={true} src="https://files.readme.io/ba8fa22-pull_notification.png">
  Toggle Pull Notification
</Image>

> 🚧 Toggle Pull Notification
>
> All the push campaigns that are created *after* turning on the Pull Notification toggle are enhanced. Similarly, no new campaigns are enhanced after the Pull Notification toggle is turned off.

After Pull Notification is turned ON, your campaigns reach more users through your notifications. You can check these boost numbers on your campaign *Stats* page.

<Image title="Push Uplift" alt={2672} border={true} src="https://files.readme.io/2e7757d-enhanced_push_deliver.png">
  Enhanced Delivery Stats
</Image>

> 📘 Support for Optimize Delivery via Inbox
>
> We support *Optimize Delivery via Inbox* and retry notifications due to delivery issues with certain OEMs. 
>
> If the app is online when *Push* is delivered, the Inbox delivery is done on the next *App Launch* and not immediately after the *Push* is delivered.

## Optimize Delivery via App Inbox

You can further increase the delivery of push notifications by sending a copy of the same message to *App Inbox*. 

To send a copy of the push message to **App Inbox**, select *Send a copy of this message to the App Inbox* that appears at the bottom of the message builder of push notification in the *What* section.

<Image title="Copy of Push Message in App Inbox" alt={746} src="https://files.readme.io/d3fa57a-campaign_push_app_inbox.png">
  Delivery via App Inbox
</Image>

> 📘 App Inbox as its Own Channel
>
> *App Inbox* also exists as a stand-alone channel. For more information, refer to [App Inbox](doc:app-inbox-overview).

  From this screen, you can do the following:

* You can customize the same push message for *App Inbox*. 
* You can change the title color, message color, and background color and add filter tags that classify your message into tabs. For more information, refer to [Message Tags](doc:create-message-app-inbox#define-the-message-content). 
* You can set a Time To Live (TTL) for the *App Inbox* message in the *Setup* section. For more information on setting up TTL, refer to [Time to Live](doc:create-message-app-inbox#define-the-message-content).

## Pull Notification and App Inbox Stats

You can view the stats for messages copied to *App Inbox* on the *Push Stats* page. The percentage boost represents the percentage of messages boosted by *App Inbox* compared to the total of messages sent via *App Inbox* and *Pull Notification*.

To view the stats for the copied messages, navigate to *App Inbox stats* tab.

<Image title="Push Uplift with App Inbox" alt={5344} border={true} src="https://files.readme.io/a2437a9-enhanced_push_deliver_2.png">
  Pull Notification and App Inbox Stats
</Image>

# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under *Settings* > *Setup* > *Campaign Limits*. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
>
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.
