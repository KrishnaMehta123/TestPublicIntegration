---
title: Setup
excerpt: Understand how to set up Push as a channel for your marketing campaigns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Mobile Push Setup

Set up your mobile push notifications from the CleverTap dashboard.  
Navigate to _Settings > Channels > Mobile push_. 

# Android

Set up and enter credentials for all the platforms that your application supports:

1. [FCM](https://developer.clevertap.com/docs/android-push#find-your-fcm-sender-id--fcm-server-api-key)
2. [Xiaomi](https://developer.clevertap.com/docs/xiaomi-push-notifications#section-get-the-apps-package-name-app-id-app-key-app-secret)
3. [Baidu](https://developer.clevertap.com/docs/baidu-push-notifications#section-get-the-apps-api-key-secret-key)
4. [Huawei](https://developer.clevertap.com/docs/clevertap-huawei-push-integration#section-get-the-apps-app-id-app-secret)

## Notification channels

For Android 8.0 and above, you can create a group of channels for your users. The users can then turn on or off the subscription to these channels. You can create and choose from a list of these channels in campaign creation.

# iOS

You can either create and upload: 

- [APNs Auth Key](https://developer.clevertap.com/docs/how-to-create-an-ios-apns-auth-key)
- [APNs Push Certificate](https://developer.clevertap.com/docs/how-to-create-an-ios-apns-certificate)

> 📘 Our Recommendation
> 
> We recommend that you create and upload an APNs Auth Key.

# Raising Events

CleverTap SDK tracks data based on the integration setup. Refer to [CleverTap SDKs](https://developer.clevertap.com/docs/clevertap-sdks) for more information. 

The following system events can be enabled manually:

## Raising Push Impression Event

You can raise and record push notifications delivered to your users’ Android devices.

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. From the _System Events \_tab, search for \_Push Impressions_, then click on the vertical ellipsis menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f68258-push_set_push_impression.png",
        "Setup Push Impressions for Android from the Schema",
        1171
      ],
      "align": "center",
      "border": true,
      "caption": "Setup Push Impressions"
    }
  ]
}
[/block]


3. Click on **Setup push impressions**. A new window displays.
4. Turn on the _Mobile Push_ toggle. 
5. Click on **Save** to enable the option.

After the toggle is on, all the push notifications delivered are recorded under the _Push Impressions_ event. The viewed and conversion count from this event is also available under _Analytics_ > _Events_.

> 🚧 SDK Considerations
> 
> Some things to consider include:
> 
> 1. The push event can only be raised for CleverTap SDK version 3.5.1 and above for Android and version 3.5.0 and above for iOS.
> 2. If the notification channel is incorrect, the push notification is not delivered on the device and therefore, no event is raised for the push impression.

## Raising Notification Viewed Event for iOS

To raise the _Notification Viewed_ event for iOS, it is mandatory to enable the _Mutable Content_ under the iOS section of the campaign creation.

For more information on how to enable _Notification Viewed_ for your account, refer to our [developer documentation](https://developer.clevertap.com/docs/push-notifications-ios#push-impressions). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2bd5135-campaign_iOS.png",
        "Select the Mutable Content Checkbox",
        1251
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Setup Push Impressions for iOS"
    }
  ]
}
[/block]


# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under _Settings_ > _Setup_ > _Campaign Limits_. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
> 
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.

To ensure your push notifications are engaging and effective, explore our guide on [Push Notification: Best Practices](https://clevertap.com/blog/push-notification-best-practices/) for expert tips on timing, content, and personalization.