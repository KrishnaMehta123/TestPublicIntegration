---
title: RenderMax
excerpt: >-
  Understand how to improve the render rate of push messages with CleverTap
  RenderMax.
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

A delivered notification doesn't always mean a rendered notification. Some original equipment manufacturers (OEMs) suppress or bypass the Google (Firebase) push delivery service to optimize battery consumption. This configuration means low notification delivery and lower render rates to your users. Your users may never see your notifications and miss important communication. To avoid this, you may have to supplement your message with other messaging channels such as Email or SMS, which means additional cost.

CleverTap RenderMax improves mobile notification render rates significantly higher by determining the state of the device and adjusting the notification rendering accordingly. Now you can engage with users you could not before and elevate ROI from your push campaigns. For example, using RenderMax can ensure the delivery of your push notifications even if the device is in battery-saving mode on inactive devices. 

This feature enables you to use the power of the following:

* Pull Notifications
* OEM Partnerships
* RenderMax Push SDK

> 📘 OS Support
>
> The RenderMax SDK is supported only for Android.

# Improve Delivery via Pull Notifications

Mobile notifications are a great way to engage customers despite the issue of low deliverability on certain device manufacturers. 

With Pull Notifications at your disposal, you can counter this challenge by optimizing the delivery of Mobile notifications to devices that missed receiving them.

> 🚧 Toggle Pull Notifications
>
> Pull notifications are enabled for all the Mobile Notification campaigns that are created *after* toggling the Pull Notifications feature. Similarly, no new campaigns are enabled for notification delivery after you turn off the toggle.

To enable this feature, navigate to *Settings* > *Engage* > *Setup* > *Pull Notifications*. Toggle \_Enable Pull Notification \_in the dashboard to activate the feature.

<Image title="Enhance Deliverability with Pull Notifications" alt={2872} align="center" border={true} src="https://files.readme.io/bba769e-pull_notifications_settings.png">
  Enable Pull Notifications on Dashboard
</Image>

After Pull Notification is enabled, your campaigns reach more users through notifications. You can check the boost in numbers in the *Impressions* and *Clicks* uplift on your campaign *Stats* tab.

<Image title="Impressions and Clicks Uplift " alt={2898} align="center" border={true} src="https://files.readme.io/c9119f3-RenderMax_stats.png">
  Campaign Uplift
</Image>

# Maximize Rendering with OEM Partnerships

Each OEM has a unique ecosystem that impacts mobile push delivery. However, the push experience with CleverTap is seamless across all devices. It is possible because CleverTap has leveraged its state-of-the-art technology and partnerships with different OEMs such as [Xiaomi](https://developer.clevertap.com/docs/xiaomi-push-notifications), [Huawei](https://developer.clevertap.com/docs/clevertap-huawei-push-integration), and [Baidu](https://developer.clevertap.com/docs/baidu-push-notifications).

# Improve Delivery via RenderMax Push SDK

CleverTap RenderMax Push SDK is a powerful update that delivers and renders notifications on the user's device even if the Firebase Cloud Messaging (FCM) delivery fails. You can boost push notification render rates significantly higher using RenderMax. 

RenderMax solves notification rendering in the following order:

1. Understands the user's device state - Battery optimized vs. Unrestricted
2. Determines the best payload mechanism for each device state
3. Renders push notifications on users' devices even in a battery-optimized state

## Install RenderMax Push SDK

The RenderMax SDK is supported only for Android Native and React Native. To install the RenderMax SDK, refer to [RenderMax Integration with Android Native](https://developer.clevertap.com/docs/enable-rendermax-with-android) and [RenderMax Integration with React Native](https://developer.clevertap.com/docs/react-native-push-notification#integrate-rendermax-push-sdk-with-react-native)

## Enable RenderMax

When creating a Mobile Push Campaign, you can enable the RenderMax feature by navigating to *Android Advanced Settings* > *RenderMax* from the *What* section of the campaign on the CleverTap dashboard.

<Image title="RenderMax Toggle in Campaign Editor" alt={2460} align="center" border={true} src="https://files.readme.io/b96a4a4-RenderMax_campaign_UI.png">
  Enable RenderMax
</Image>

> 🚧 Custom Handling Notifications
>
> RenderMax Push SDK attempts to render the notification for all campaigns with the feature enabled. The notification is rendered by the CleverTap SDK and any custom rendering done by the app is ignored for devices where the app is Device Optimized State.
>
> For more detail on the steps,  refer to the [RenderMax Push Integration](https://developer.clevertap.com/docs/enable-rendermax-with-android).

After you send out the push campaign, you can check the uplift in your notification rendering from the [Push Campaign Stats](doc:push-campaign-stats) page. 

## RenderMax FAQs

### 1. What is the battery drain on RenderMax?

The feature has shown negligible \[\<0.1%] battery usage over two months, with eight daily notifications sent per device.

### 2. What is the increase in the SDK size?

The RenderMax SDK has a size of less than 120Kb.

### 3. How does the feature work?

The RenderMax SDK has higher level permission on the notification control hierarchy, which allows the core SDK to run for a longer duration and is of higher importance in ensuring the rendering of notifications.

### 4. What versions of the CleverTap Android SDKs are compatible with RenderMax?

The RenderMax SDK is compatible with the following SDK versions on Android 12 and below:

* Android v4.6.6 and above
* React Native v0.9.3 and above
