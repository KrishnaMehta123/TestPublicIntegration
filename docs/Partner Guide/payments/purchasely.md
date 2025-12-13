---
title: Purchasely
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

[Purchasely](https://www.purchasely.com/) is a platform that enables businesses to manage and monetize their mobile apps through In-App purchases and subscriptions. This integration lets you send all subscription-related events and user properties from Purchasely to CleverTap. 

With this integration, you can:

- Analyze subscription events and user properties to gain deeper insights into customer behavior and trends.
- Trigger personalized messaging campaigns across channels
- Optimize revenue performance with real-time insights.

Integrating Purchasely with CleverTap empowers businesses to refine their in-app purchase strategies, increase revenue, and improve user engagement and retention.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by Purchasely. The CleverTap and Purchasely integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Purchasely](mailto:support@purchasely.com) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites: 

- Ensure you have access to your Purchasely account.
- Ensure you have a CleverTap account with a valid **Account ID**, **Passcode**, and **Region**.

# Integrate Purchasely with CleverTap

The integration process involves the following three steps:

1. [Sync CleverTap ID with Purchasely (SDK implementation)](doc:purchasely#sync-clevertap-id-with-purchasely-sdk-implementation).
2. [Find CleverTap Project Details](doc:purchasely#find-clevertap-project-details).
3. [Connect and Configure CleverTap and Purchasely Accounts](doc:purchasely#connect-and-configure-clevertap-and-purchasely-accounts).

## Sync CleverTap ID with Purchasely (SDK implementation)

To effectively integrate CleverTap with Purchasely, ensure the SDK is properly installed and user IDs are mapped. Mapping user IDs enables both platforms to recognize users, consistently maintaining a unified user profile. Use the following code in your app to map the CleverTap Distinct ID with Purchasely:

```swift
CleverTap.autoIntegrate()
if let clevertapId = CleverTap.sharedInstance()?.profileGetID() {
    Purchasely.setAttribute(.clevertapId, value: clevertapId)
}
```
```kotlin
val cleverTap = CleverTapAPI.getDefaultInstance(applicationContext)
cleverTap?.cleverTapID?.let {
    Purchasely.setAttribute(Attribute.CLEVER_TAP_ID, it)
}
```
```java
CleverTapAPI cleverTap = CleverTapAPI.getDefaultInstance(getApplicationContext());
if(cleverTap.getCleverTapID() != null) {
    Purchasely.setAttribute(Attribute.CLEVER_TAP_ID, cleverTap.getCleverTapID());
}
```
```coffeescript React Native
CleverTap.getCleverTapID((err, res) => {
    Purchasely.setAttribute(Attributes.CLEVER_TAP_ID, res);
});
```
```Text Flutter
Purchasely.setAttribute(PLYAttribute.clever_tap_id, "clever_tap_id");
```
```Text Cordova
Purchasely.setAttribute(Purchasely.Attribute.CLEVER_TAP_ID, "clever_tap_id");
```
```Text Unity
private PurchaselyRuntime.Purchasely _purchasely;

_purchasely.SetAttribute(PLYAttribute.CLEVER_TAP_ID, "clever_tap_id");
```
```objectivec Objective-C
[CleverTap autoIntegrate];

NSString *clevertapId = [[CleverTap sharedInstance] profileGetID];
if (clevertapId) {
    [Purchasely setAttribute:PurchaselyAttributeClevertapId value:clevertapId];
}
```

For more information, refer to [Set CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id).

## Find CleverTap Project Details

To connect Purchasely with the CleverTap dashboard, you need the following project details:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c15acc7-Project_Details.png",
        null,
        "CleverTap Project Details"
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap Project Details"
    }
  ]
}
[/block]


## Connect and Configure CleverTap and Purchasely Accounts

To set up CleverTap in the Purchasely dashboard, perform the following steps:

1. Go to _Settings_ > _Integrations_ from the Purchasely dashboard. The _External Integrations_ page opens.
2. Click the  ![](https://files.readme.io/f1bcbe8-Ellipsis.png) icon on the _CleverTap_ tile, and select _Edit_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c8687c9-CleverTap.png",
        null,
        "External Integrations"
      ],
      "align": "center",
      "border": true,
      "caption": "External Integrations"
    }
  ]
}
[/block]


3. Turn ON the _INTEGRATION ENABLED_ option, and enter your CleverTap Account **Region**, **Account ID**, and **Passcode** under the _Account parameters_ tab. To find these details from the CleverTap dashboard, refer to [Find CleverTap Project Details](doc:purchasely#find-clevertap-project-details).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5036c0405687f1c0708ef07bd09fb9134119b3f6e1a608ead9bb02fe50315022-image.png",
        null,
        "Account Parameters"
      ],
      "align": "center",
      "border": true,
      "caption": "Account Parameters"
    }
  ]
}
[/block]


4. Click **Save**.
5. Go to the _Server events_ tab, enable the events you want to send to CleverTap, and click **Save**. For more details about the types of supported events, refer to [Server Events](https://docs.purchasely.com/docs/server-events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a225dbb17e562a1a6c165da329d1e9b8a9162bfcbd239d4a3d7f88488803e610-image.png",
        null,
        "Server events"
      ],
      "align": "center",
      "border": true,
      "caption": "Server events"
    }
  ]
}
[/block]


6. Go to the _User Properties_ tab, enable the update of user properties to be sent to CleverTap under _User Properties_, and click **Save**. For more details about the supported User Properties, refer to [User Properties](https://docs.purchasely.com/docs/engagement-crm#leveraging-user-properties).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a5d3eff03cb4cc2fc09fe00c1ba5264ff2ab850875709fc10bc08b6fe034dbc-image.png",
        null,
        "User Properties"
      ],
      "align": "center",
      "border": true,
      "caption": "User Properties"
    }
  ]
}
[/block]


> 📘 Renaming Events
> 
> You can override the names of Events and User Properties sent to CleverTap when setting up the integration.

With a few simple steps, synchronizing user identities, configuring integration settings, and enabling event tracking, you can unlock deeper insights into user behavior and take action through CleverTap’s powerful engagement engine.