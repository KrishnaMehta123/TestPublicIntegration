---
title: Qonversion
excerpt: Payments
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

[Qonversion](https://qonversion.io/) is a subscription data platform that helps marketers manage in-app subscriptions, analyze user behavior, and optimize revenue. It provides tools for tracking subscription events, integrating with various services, and running experiments to improve user engagement.

Integrating CleverTap with Qonversion, you can launch user engagement campaigns, win back customers, and address billing issues. Once integrated, Qonversion sends all [subscription events](https://documentation.qonversion.io/docs/integrations-overview#tracked-events) to CleverTap, enabling targeted and timely communication with your users.

With this integration, you can:

* Renewal Reminders: Automate personalized notifications for upcoming subscription renewals to minimize churn. 
* Win-Back Opportunities: Reengage users who canceled subscriptions by offering tailored incentives to resubscribe.
* Payment Issue Alerts: Instantly notify users about failed payments and guide them in updating billing details.

> 🚧 Support For Integration
>
> This integration is managed and continuously improved by Qonversion. The CleverTap and Qonversion integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Qonversion](mailto:support@qonversion.io) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

* Ensure you have access to your Qonversion account.
* Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Qonversion with CleverTap

The integration process involves the following three steps:

1. [Setting Up the CleverTap and Qonversion SDKs](doc:qonversion#setting-up-the-clevertap-and-qonversion-sdks)
2. [Find CleverTap Project Details](doc:qonversion#find-clevertap-project-details)
3. [Set Up CleverTap in Qonversion Dashboard](doc:qonversion#set-up-clevertap-in-qonversion-dashboard)

## Setting Up the CleverTap and Qonversion SDKs

To integrate CleverTap with Qonversion effectively, ensure the SDK is properly installed and user IDs are synchronized. Synchronizing user identities allows both platforms to identify users, consistently maintaining a unified user profile. Follow these steps to integrate the SDK into your app

1. **Install the CleverTap SDK**: Add CleverTap SDK to your app. For detailed guidance, refer to the [CleverTap SDK](https://developer.clevertap.com/docs/clevertap-sdks). 

2. **Install the Qonversion SDK**: Follow Qonversion's [Installing the SDKs guide](https://documentation.qonversion.io/docs/install-sdk) to set up the Qonversion SDK in your app.

3. **Sync CleverTap ID with Qonversion**: Set the same user ID in both CleverTap and Qonversion to ensure accurate tracking of user data and revenue events. Use the appropriate code snippet based on your platform:

```swift
Qonversion.shared().setUserProperty(.userID, value: "CleverTapID")
```
```objectivec Objective-C (iOS)
[[Qonversion sharedInstance] setUserProperty:QNUserPropertyKeyUserID value:@"CleverTapID"];  
```
```java Java (Android)
Qonversion.getSharedInstance().setUserProperty(QUserPropertyKey.CustomUserId, "CleverTapID");
```
```kotlin Kotlin (Android)
Qonversion.shared.setUserProperty(QUserPropertyKey.CustomUserId, "CleverTapID")
```
```Text Flutter
Qonversion.getSharedInstance().setUserProperty(QUserPropertyKey.customUserId, 'CleverTapID');  
```
```Text React Native
Qonversion.getSharedInstance().setUserProperty(UserPropertyKey.CUSTOM_USER_ID, 'CleverTapID');  
```
```Text Unity
Qonversion.GetSharedInstance().SetUserProperty(UserPropertyKey.CustomUserId, "CleverTapID");  
```
```Text Cordova
Qonversion.getSharedInstance().setUserProperty(Qonversion.UserPropertyKey.CUSTOM_USER_ID, 'CleverTapID');  
```
```Text Capacitor
Qonversion.getSharedInstance().setUserProperty(UserPropertyKey.CUSTOM_USER_ID, 'CleverTapID');  
```

## Find CleverTap Project Details

To connect Qonversion with the CleverTap dashboard, you need the following project details:

| Field            | Description                                                                                                                                                                                                                                                                 |
| :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Access the CleverTap dashboard and locate the Project ID under *Settings* > *Project*.                                                                                                                                                                                      |
| Account Passcode | Access the CleverTap dashboard and locate the Passcode under *Settings* > *Project*. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                                                        |
| Region           | Access the CleverTap dashboard and locate *Region* for the API endpoint you want to select under *Settings* > *Project*. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

You can find these details in the *Settings > Project* section of the CleverTap dashboard:

<Image alt="CleverTap Project Details" align="center" border={true} src="https://files.readme.io/c15acc7-Project_Details.png">
  CleverTap Project Details
</Image>

## Set Up CleverTap in Qonversion Dashboard

To set up CleverTap in Qonversion dashboard:

1. Go to *Tools > Integrations* from the Qonversion dashboard.
2. Under *Email & Push Notification*, go to *CleverTap*.
3. Choose a platform *iOS* or *Android*.
4. Under *Integration Details*, enter your CleverTap Project ID, Passcode and Region. Refer to [Find CleverTap Project Details](doc:qonversion#find-clevertap-project-details).

<Image alt="Integrations" align="center" border={true} src="https://files.readme.io/0ec26febbc0135721cc640a9f78836427fc928226b15028d5f5e7b90b8ce130e-quenction.gif">
  Integrations
</Image>

5. Configure Global Event Preferences:
   * **Send Revenue Properties**: Keep this enabled to send revenue values. Disable it only if you don't need revenue data.
   * **Send Sales as Proceed**: Choose whether to send revenue values as net of App Stores' commission.
   * **Send Sandbox Events**: Optionally, Enable to receive sandbox events during testing.

<Image alt="Global Event Preferences" align="center" border={true} src="https://files.readme.io/e4c57a66a7afad4bcd47ada808c31474bf09c20427f64062f34e671bd385cfcf-image.png">
  Global Event Preferences
</Image>

6. [Event Settings](https://documentation.qonversion.io/docs/integrations-overview#switching-between-subscriptions): For each event, click **More options** to configure specific settings:
   * **Enable event**: Enable to include the event in this integration.
   * **Send Revenue**: Enable or disable sending revenue for this specific event.

<Image alt="Event Settings" align="center" border={true} src="https://files.readme.io/77089e10147facb6a94910d6ec54764ee526c1d0539a07fc2ffe3ba4aa213eae-image.png">
  Event Settings
</Image>

7. Click **Create +** to save integration details.

Qonversion will now send all the [subscription events](https://documentation.qonversion.io/docs/integrations-overview#tracked-events) to your CleverTap account.

# FAQs

### What subscription events can Qonversion send to CleverTap?

Qonversion can send events such as trial started, subscription renewed, subscription canceled, and more. Refer to the [tracked events](https://documentation.qonversion.io/docs/integrations-overview#tracked-events).

### Do I need separate SDKs for CleverTap and Qonversion?

Yes, you need to install both the CleverTap SDK and the Qonversion SDK in your app for the integration to work effectively. Refer to the guides for [CleverTap SDK](https://developer.clevertap.com/docs/clevertap-sdks) and [Qonversion SDK](https://documentation.qonversion.io/docs/install-sdk) installation.

### What is an Event Payload, and what data is sent to CleverTap?

An Event Payload contains details about user activities sent to CleverTap, such as identity, event name, timestamp, and event-specific data like platform, revenue, and device details. For details, refer to [CleverTap Event Payload](https://documentation.qonversion.io/docs/clevertap#event-payload).
