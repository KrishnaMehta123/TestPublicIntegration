---
title: AppTrove by Trackier
excerpt: Attribution Partner
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

AppTrove, by Trackier,  is a comprehensive mobile marketing platform designed to monitor your app's expansion while facilitating seamless integration with various partners. By leveraging AppTrove, you can access a unified environment to collaborate with different partner networks and analyze their collective performance. This document provides essential details on integrating CleverTap and AppTrove. With this integration, you can track the following and also determine where a user was acquired from:

* **Install events**: These events can be organic install events and inorganic install events.
* **Custom events**: These can include any events (other than install events) that are provided by the attribution partner and tracked in the app. 

To learn more about these events and their default attribution settings in the CleverTap dashboard, refer to [Types of Data](https://docs.clevertap.com/docs/attribution#types-of-data).

If you have any issues with this integration, write to [support-mmp@trackier.com](mailto:support-mmp@trackier.com)

# Integrate AppTrove

To integrate AppTrove with CleverTap:

1. [Add CleverTap Credentials to AppTrove Dashboard](doc:https://docs.clevertap.com/docs/apptrove#add-clevertap-credentials-to-apptrove-dashboard).
2. [Map CleverTap ID with AppTrove](doc:apptrove#map-clevertap-id-with-apptrove)
3. [Configure In-App Event Postback](doc:apptrove#configure-in-app-event-postback)
4. [Setup for Organic Install and Custom Events](doc:apptrove#setup-for-organic-install-and-custom-events)

## Add CleverTap Credentials to AppTrove Dashboard

You must set up the AppTrove dashboard by adding CleverTap account details as follows:

1. Navigate to *Partner Integration* and search for *CleverTap* under the *Not Integrated Partners* section.

   <Image alt="Integrate AppTrove with CleverTap" align="center" border={true} src="https://files.readme.io/6e9f359-Integrate_CleverTap_with_AppTrove.png">
     Integrate AppTrove with CleverTap
   </Image>
2. Add the following CleverTap account details:

   <br />

   <Image align="center" className="border" border={true} src="https://files.readme.io/1d8b53d-Enter_CleverTap_Account_Details.png" />

To get these details, navigate to *Settings* > *Project* from the CleverTap dashboard as follows:

* **Account ID** : Access the CleverTap dashboard and locate the Project ID under *Settings > Project*.
* **Account Token**: Access the CleverTap dashboard and locate the Project Token under *Settings > Project*.
* **Account Passcode**: Access the CleverTap dashboard and locate Passcode under *Settings > Project*. To know more refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
* **Region**: Access the CleverTap dashboard and locate Region for the API endpoint you want to select under *Settings > Project*. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api).

<Image alt="CleverTap Account Details" align="center" src="https://files.readme.io/e2008a6-Screenshot_2024-08-06_at_3.32.51_PM.png">
  CleverTap Account Details
</Image>

3. Click **Save**.

## Map CleverTap ID with AppTrove

AppTrove SDK implementation requires CleverTap ID configured as Trackier `userId` or `UserAdditionaldetails`. The steps to do so vary for Android and iOS. The steps for both are listed in the sections to follow.

### For Android App

To track attribution and event data in your Android app, follow the steps listed in the [AppTrove Android SDK Integration Guide](https://github.com/trackier/android_sdk). For pushing the CleverTap ID to AppTrove, add the following code.

#### **Set the User ID**

Use the `getCleverTapID` method to get the CleverTap ID on the `OnInitCleverTapIDListener` to set the `UserId` method of AppTrove.

```java Java
 TrackierSDKConfig sdkConfig = new TrackierSDKConfig(this, "8282-382382-73239823-729382", "development");
 clevertapDefaultInstance.getCleverTapID(new OnInitCleverTapIDListener() {
            @Override
            public void onInitCleverTapID(final String CTID) {
                TrackierSDK.setUserId(CTID);
            }
        });
TrackierSDK.initialize(sdkConfig);
```
```Text Kotlin
// Fetch CleverTapID from CleverTap SDK
    cleverTapInstance?.getCleverTapID {
        // Set device alias into Airbridge SDK
        TrackierSDK.setUserId(cleverTapID);
    }
}
```

#### **Set Additional User Data**

Let's say you are already using `setUserId` to send the identity of the user to AppTrove. You can use the `setAdditionaldata` method instead of `setUserId`to push CleverTap ID.

```java
 TrackierSDKConfig sdkConfig = new TrackierSDKConfig(this, "8282-382382-73239823-729382", "development");
     clevertapDefaultInstance.getCleverTapID(new OnInitCleverTapIDListener() {
                @Override
                public void onInitCleverTapID(final String CTID) {
                HashMap hashMap1 = new HashMap();
                hashMap1.put("clevertap_uid", CTID);
                TrackierSDK.setUserAdditionalDetails(hashMap1);
                }
            });
    TrackierSDK.initialize(sdkConfig);
```
```Text Kotlin
TrackierSDK.setUserAdditionalDetails("clevertap_uid", CTID);
```

> 📘 Note
>
> The `setAdditionaldata` method always takes priority over `setUserId`.

### For iOS App

To track attribution and event data in your iOS app, perform the steps listed in [AppTrove iOS SDK Integration Guide.](https://github.com/trackier/ios-sdk)\
Set the CleverTap ID value as the AppTrove Global Property. Add the below code to your iOS app code.

```swift Swift
let config = TrackierSDKConfig(appToken: "b551b474-xxxx-xxxx-xxxx-971e5b954169", env: TrackierSDKConfig.ENV_DEVELOPMENT)
 CleverTap.autoIntegrate()
            if let attributionId = CleverTap.sharedInstance()?.profileGetID() {
                TrackierSDK.setUserAdditionalDetails(userAdditionalDetails: ["clevertap_uid":attributionId])
            }
TrackierSDK.initialize(config: config)
```

## Configure In-App Event Postback

To send all events, select *Send all In-App event postback to partner*, And in case you want to send only selected events, select *Send only selected In-App Events postback to partner (At least one mapping is required)*  and choose *Event Name* and *Event Identifier*, respectively. 

<Image alt="In-App Event Postback" align="center" border={true} src="https://files.readme.io/449035a-image-1400x900.jpg">
  In-App Event Postback
</Image>

## Setup for Organic Install and Custom Events

After successful integration, AppTrove starts pushing inorganic install events data to CleverTap. To receive in-app events (custom events) in CleverTap from AppTrove, proceed as follows: 

1. Navigate to *Settings* > *Partners* and scroll down to the *Attribution partners* section.

<Image alt="CeleverTap Attribution Partners" align="center" border={true} src="https://files.readme.io/0ffe914-screencapture-sk1-dashboard-staging-6-dashboard-clevertap-W6W-797-865Z-account-setup-exports-partner-list-2024-08-05-14_48_11.png">
  CeleverTap Attribution Partners
</Image>

2. Click on the  *AppTrove* partner.\
   On clicking, the *Attribution partner - AppTrove* popup appears on the right side of the screen.

<Image alt="AppTrove Partner Integration" align="center" border={true} src="https://files.readme.io/c4395e2-Screenshot_2024-08-06_at_3.34.59_PM.png">
  AppTrove Partner Integration
</Image>

2. Select the required option from the options below. Selecting any of these options indicates that the CleverTap accepts event data when shared by the partner.
   * Custom events
   * Organic install events

> 🚧 Duplication of Events
>
> If you select *Organic install events* for more than one attribution partner, a warning for duplication of events displays, as shown in the following figure. We strongly recommend tracking the organic install events from only one attribution partner.

<Image alt="Duplication of Events" align="center" width="70% " border={true} src="https://files.readme.io/ae820b8-screencapture-sk1-dashboard-staging-6-dashboard-clevertap-W6W-797-865Z-account-setup-exports-partner-list-2024-08-05-14_50_05.png">
  Duplication of Events
</Image>

4. Click **Save**. On clicking, the following message displays at the top of the screen: *Changes saved. Admins are notified of this via email*. 

# Viewing Data on Dashboard

You can now view the event data on the CleverTap dashboard. To do so, proceed as follows:

1. From the CleverTap dashboard, go to *Analytics > Events*.
2. Apply the required filters for the selected event. The filters vary depending on the type of event.

* **For Install Events**: All the install events are tracked under the *UTM Visited* event.

<Image alt="Install Events Filter" align="center" border={true} src="https://files.readme.io/fbf5eb7-Screenshot_2024-08-06_at_3.38.46_PM.png">
  Install Events Filter
</Image>

* **For Custom Events**: In-app revenue events received from AppTrove are prefixed with **AT** in CleverTap.
