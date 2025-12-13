---
title: 'App Inbox: Troubleshooting and FAQs'
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

Find answers to the following common questions about App Inbox.

### Does the app inbox stay after the user has uninstalled the application?

The app inbox does not stay in the application after the user has uninstalled it, as the messages are stored locally. Clearing the cache or uninstalling the app deletes the app inbox from the device. CleverTap does not maintain a user's app inbox state in the backend.

### Why is my App Inbox message not delivered immediately in a live campaign?

App Inbox is a pull-based channel, meaning messages are fetched from the CleverTap ̉system during an app session. This differs from Push notifications, which are delivered instantly. This is not a system delay, but the expected behavior of the App Inbox system, designed to optimize performance and user experience.

For more information on inbox delivery behavior, refer to [Inbox Delivery Timing and Campaign Behavior](doc:app-inbox#inbox-delivery-timing-and-campaign-behavior).

### If a user opens the app after a very long time, will the SDK fetch all the pending app inbox messages for the user?

The SDK will fetch the newest ten messages only. Even though you have launched the application after a long time and have qualified for more than ten app inbox messages, you'll still see only ten messages. The messages should also be under the [Time to Live](https://docs.clevertap.com/docs/create-message-app-inbox#time-to-live-ttl).

### Are special characters supported in the filter tags for app inbox campaigns? For example, an underscore, a hyphen, Chinese characters, Vietnamese/ pinyin characters, and so on.

Yes, special Unicode-encoded characters are supported.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/47b359e-Special_characters.png",
        "Special characters.png",
        634
      ],
      "align": "center",
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]


### How can I view the notification count for a custom App Inbox?

The inbox message count for a custom App Inbox is available from the `cleverTapDefaultInstance.getInboxMessageCount()` API. For more information, refer to [Create your App-Inbox](https://developer.clevertap.com/docs/android-app-inbox#create-your-app-inbox).