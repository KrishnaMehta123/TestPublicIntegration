---
title: RevenueCat
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

[RevenueCat](https://www.revenuecat.com/) is an In-App purchase and subscription platform for mobile apps. The RevenueCat model offers the following benefits:

- Build cross-platform In-App purchases easily.
- Manage your products and subscribers.

Integrating RevenueCat and CleverTap helps automatically send all customer subscription events from your app to CleverTap, allowing you to analyze events and monitor revenue seamlessly.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by RevenueCat. The CleverTap and RevenueCat integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [RevenueCat](https://community.revenuecat.com/get-help-5) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites: 

- Ensure you have access to your RevenueCat account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate RevenueCat with CleverTap

This process involves the following two major steps:

1. [Sync CleverTap Identity to RevenueCat (SDK implementation)](doc:revenuecat#sync-clevertap-identity-to-revenuecat).
2. [Send RevenueCat Events to CleverTap](doc:revenuecat#send-revenuecat-events-to-clevertap).

## Sync CleverTap Identity to RevenueCat

To integrate CleverTap with RevenueCat, ensure both the CleverTap and RevenueCat SDKs are installed and user IDs are synchronized correctly. This ensures both platforms consistently recognize users and maintain a unified user profile.

You can synchronize the CleverTap ID with RevenueCat in the following two ways:

- **Set CleverTap ID Manually**: Manually set up the CleverTap ID as a [RevenueCat customer attribute](https://www.revenuecat.com/docs/customers/customer-attributes).
- **Default Identifier**: If you do not set a specific property, RevenueCat uses the [App User ID](https://www.revenuecat.com/docs/customers/user-ids) as the default identifier sent to CleverTap.

### Configuration for Different Platforms

To synchronize CleverTap and RevenueCat, configure the SDKs for your platform using the following code:

- **Android**

```java
// Configure Purchases SDK
Purchases.configure(this, "public_sdk_key", "my_app_user_id"); //purchase SDK
// Configure CleverTap SDK
CleverTapAPI cleverTapInstance = CleverTapAPI.getInstance(getApplicationContext());
String cleverTapId = cleverTapInstance.getCleverTapId(); 
Map<String, String> attributes = new HashMap<>();
attributes.put("$cleverTapId", cleverTapId);
Purchases.getSharedInstance().setAttributes(attributes);
```
```coffeescript Kotlin
// Configure Purchases SDK
Purchases.configure(this, "public_sdk_key", "my_app_user_id")
// Configure CleverTap SDK
val cleverTapInstance = CleverTapAPI.getInstance(applicationContext)
val cleverTapId = cleverTapInstance?.cleverTapID
val attributes = mapOf("\$cleverTapId" to cleverTapId)
Purchases.getSharedInstance().setAttributes(attributes)
```

- **iOS**

```coffeescript Objective-C
// Configure Purchases SDK
[RCPurchases configureWithAPIKey:@"public_sdk_key" appUserID:@"my_app_user_id"];
// Configure CleverTap SDK
CleverTap *cleverTapInstance = [CleverTap sharedInstance];
NSString *cleverTapId = [cleverTapInstance profileGetCleverTapID];
NSDictionary *attributes = @{@"$cleverTapId": cleverTapId};
[[RCPurchases sharedPurchases] setAttributes:attributes];
```
```coffeescript Swift
// Configure Purchases SDK
Purchases.configure(withAPIKey: "public_sdk_key", appUserID: "my_app_user_id")
// Configure CleverTap SDK
if let cleverTapInstance = CleverTap.sharedInstance() {
    if let cleverTapId = cleverTapInstance.profileGetCleverTapID() {
        let attributes = ["$cleverTapId": cleverTapId]
        Purchases.shared.setAttributes(attributes)
    }
}
```

- **Other Platforms** 

```coffeescript React Native
//Assumes using react-native-purchases and react-native-clevertap
import Purchases from 'react-native-purchases';
import CleverTap from 'clevertap-react-native';
// Configure Purchases SDK
Purchases.configure({ apiKey: "public_sdk_key", appUserID: "my_app_user_id" });
// Configure CleverTap SDK
CleverTap.profileGetCleverTapId((cleverTapId) => {
    const attributes = { "$cleverTapId": cleverTapId };
    Purchases.setAttributes(attributes);
});
```
```coffeescript Flutter
//Assumes using purchases_flutter and clevertap_plugin
import 'package:purchases_flutter/purchases_flutter.dart';
import 'package:clevertap_plugin/clevertap_plugin.dart';
// Configure Purchases SDK
await Purchases.configure(PurchasesConfiguration("public_sdk_key")
  ..appUserID = "my_app_user_id");
// Configure CleverTap SDK
CleverTapPlugin.getCleverTapId().then((cleverTapId) {
  final attributes = {"\$cleverTapId": cleverTapId};
  Purchases.addAttributes(attributes);
});
```
```coffeescript Cordova
// Configure Purchases SDK
purchases.setup("public_sdk_key", { appUserID: "my_app_user_id" });
// Configure CleverTap SDK
clevertap.profileGetCleverTapID((cleverTapId) => {
    const attributes = { "$cleverTapId": cleverTapId };
    purchases.setAttributes(attributes);
});
```
```coffeescript Unity
using RevenueCat;
using CleverTapSDK;
// Configure Purchases SDK
Purchases.Configure("public_sdk_key", appUserID: "my_app_user_id");
// Configure CleverTap SDK
CleverTapAPI cleverTapInstance = CleverTapAPI.GetInstance();
string cleverTapId = cleverTapInstance.GetCleverTapID();
var attributes = new Dictionary<string, string> { { "$cleverTapId", cleverTapId } };
Purchases.SharedInstance.SetAttributes(attributes);
```

For more information about configuring the CleverTap SDK, refer to the [CleverTap SDK](https://developer.clevertap.com/docs/clevertap-sdks). For more information about configuring the RevenueCat SDK, refer to the [RevenueCat SDK](https://www.revenuecat.com/docs/platform-resources/sdk-reference).

## Send RevenueCat Events to CleverTap

Once the Purchases SDK and CleverTap SDK are synchronized with the same user identity, configure your mobile app or payment provider by selecting the app store and configuring the app in the RevenueCat dashboard.

1. Select your project in the RevenueCat dashboard. 
2. Go to the _Integrations_ section and click **+ New** to integrate CleverTap.
3. Choose _CleverTap_ from the _Marketing/Communications_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a2ae7de226ebecf7b3b1dd771342495d3016e9198d181f4e7fac6b9a087fcc1d-revccc.gif",
        "",
        "Integrations"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Integrations"
    }
  ]
}
[/block]


4. Enter the following CleverTap Account details:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

> 📘 Region Support
> 
> - By default, RevenueCat sends data through CleverTap EU data center. CleverTap customers with a regional data center configured can select their preferred region from the _CleverTap Region_ dropdown.
> - Currently, RevenueCat does not support the following regions: Indonesia (aps3) and Middle East (UAE - mec1).

5. (Optional) Add your _Sandbox Account ID_ and _Sandbox Passcode_ from your test account.
6. Enter the custom _Event names_ for the events you want to send to CleverTap, or click _Use default event names_ to send events with their default names. For more information about events tracked using this integration, refer to [Events](https://www.revenuecat.com/docs/integrations/third-party-integrations/clevertap#events). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64bbde26538c997d0759d26b2786a084bc0f07ef18aa45a3ecb22c4f9fb5187c-image.png",
        null,
        "CleverTap Integrations"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Send RevenueCat Events to CleverTap"
    }
  ]
}
[/block]


7. Select the required options from the _Sales Reporting_ dropdown to specify how they want the revenue information to be calculated and displayed. For more information, refer to _[Taxes and Commissions](https://www.revenuecat.com/docs/dashboard-and-metrics/taxes-and-commissions)_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/795ff437b02ad9c47324f079933ecbc7539d6eccf2cc0da66a4cd441703f3ca0-image.png",
        null,
        "Sales reporting"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Sales Reporting"
    }
  ]
}
[/block]


8. Click **ADD INTEGRATION** to complete the integration process.

# FAQs

### Which events are sent from RevenueCat to CleverTap?

The CleverTap integration tracks events such as Initial Purchase, Trial Started, and more. To learn about all the events that can be sent from RevenueCat to CleverTap, refer to [Events](https://www.revenuecat.com/docs/integrations/third-party-integrations/clevertap#events).

### Which JSON event types does RevenueCat deliver to CleverTap?

RevenueCat delivers JSONs to CleverTap for most event types, including Initial Purchase, Trial Started, Trial Converted, Trial Cancelled, Renewal, and more. To explore these sample events in detail, refer to [Sample JSON Events](https://www.revenuecat.com/docs/integrations/third-party-integrations/clevertap#sample-events).