---
title: Setup
excerpt: Understand how to set up Web Push as a channel for your marketing campaigns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Check that Web Push is set up before creating campaigns. 

# Browser & OS

From the CleverTap dashboard, navigate to _Settings > Channels > Web push_. You can toggle the Web push for every browser that is integrated correctly. All the details are displayed on this page. 

1. [Chrome Browser](https://developer.clevertap.com/docs/web-push#chrome)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/088057131103893b398a4587df82c913056e4f2e09b703fb1748896336ada3e7-image.png",
        null,
        "CT Dashboard settings for Chrome"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "CT Dashboard settings for Chrome"
    }
  ]
}
[/block]


> 📘 FCM Update: Migrate to HTTP v1 API
> 
> We only support VAPID based Web Push notifications. Customers that have FCM based tokens in their account, please note the following:
> 
> - Firebase will deprecate its legacy APIs starting June 20, 2023, and discontinue them from June 2024.
> - To avoid disruptions in web push notifications, you must migrate to the new HTTP v1 API by June 20, 2024. For more information, refer to [Integrate FCM and CleverTap](https://developer.clevertap.com/docs/web-push#integrate-fcm-and-clevertap).

2. [Firefox Browser](https://developer.clevertap.com/docs/web-push#firefox)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2acbfaa52a58b6885477b6eedb1973bfa882d6599223ca8a6249f527e04df9fa-image.png",
        null,
        "CT Dashboard settings for Firefox"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "CT Dashboard settings for Firefox"
    }
  ]
}
[/block]


3. [Safari Browser](https://developer.clevertap.com/docs/web-push#safari)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a8d528-safari_web_push.png",
        "Provide APNS details",
        1080
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "CT Dashboard Settings for Safari"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae85eb6ccca13e038f60419af6de9a861ee4412c489e0993e2b067ab0dd54abf-2025-01-30_15-11-05.png",
        "",
        "CT Dashboard Settings for Safari"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "CT Dashboard Settings for Safari"
    }
  ]
}
[/block]


4. [Kai OS](https://developer.clevertap.com/docs/kaios)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/231f7b6c446d06b3ce1e0b67bc2a335b2327d7b625afa039bbbf6c7ba4030aa5-image.png",
        null,
        "CT Dashboard Settings for KaiOS"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "CT Dashboard Settings for KaiOS"
    }
  ]
}
[/block]


# Soft Prompt

The Soft Prompt feature improves the Web Push opt-in process by displaying a timely and contextual prompt before triggering the browser’s native opt-in prompt.

Instead of immediately giving control to the browser, which offers users an option to allow or deny requests, a soft prompt acts as the initial step to guide users. It allows marketers to prepare users by explaining the benefits of subscribing, thereby increasing the chances of a positive response. This strategic approach helps to prevent permanent opt-out decisions and improves overall opt-in rates.

This update allows you to fully customize the content, style, and placement of the Web Push Soft Prompt enhancing user experience and increasing opt-in rates. There are two types of Soft Prompt opt-ins:

- [Card Popup](doc:setup-web-push#card-popup): A visually engaging prompt that appears on the website, encouraging users to subscribe immediately.
- [Bell Icon](doc:setup-web-push#bell-icon): A persistent opt-in option that ensures continuous visibility for the opt-in without disrupting the user experience. It allows users to subscribe to notifications at their convenience.

By using both the Card Popup and the Bell Icon, marketers can provide greater flexibility in how users opt-in. The Card Popup offers an immediate and engaging prompt, while the Bell Icon ensures that users who dismiss the initial prompt still have an option to subscribe later. 

## Card Popup

To use this feature, enable the Card Popup toggle from the CleverTap dashboard, in the _Soft Prompt_ section of Web Push.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e90476e1e7ceb662f7743c863e0aca05e575b3719ffac979bb799efff3ae094-image.png",
        null,
        "Soft Prompt"
      ],
      "align": "center",
      "border": true,
      "caption": "Soft Prompt"
    }
  ]
}
[/block]


> 📘 Note
> 
> You will see two options: New and Old designs. By default, the old designs are selected. We recommend selecting the new design as it allows complete customization of the Soft Prompt as per your branding guidelines.

To enable New Design Soft Prompt from your dashboard:

1. From the CleverTap dashboard, go to _Settings > Channels > Web push_. Click **Soft Prompt**.
2. Toggle the _Card Popup_ feature.
3. Select _New Design_ and click **Edit** to modify the design details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d2d4936cb51307871057e8c28e9c6c072092e64793996b298038d5117bc2c376-2025-01-30_14-56-21.png",
        "",
        "Edit the New Design"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit the New Design"
    }
  ]
}
[/block]


4. Edit the content and style of the popup. This includes the title, body, background color, icons, buttons, and so on. 
5. Once done, click **Preview** to view the appearance of the customized Card Popup and finalize the design before deploying it. Click **Save** to save the changes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb5eccc9ef73c662d92e836d7249e776a38bd4331e8d1ea7fc03f28194996bb3-image.png",
        null,
        "Edit options for Card Popup"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit options for Card Popup"
    }
  ]
}
[/block]


## Bell Icon

To enable the Bell Icon feature from the CleverTap dashboard:

1. Enable the Bell Icon toggle in the _Soft Prompt_ section of the Web Push page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/00250a20f999653cb375d1cfef09db4c09aaf0ae11f93d0a0497ca0fb324235e-2025-01-30_14-56-43.png",
        null,
        "Bell Icon"
      ],
      "align": "center",
      "border": true,
      "caption": "Bell Icon - show ON"
    }
  ]
}
[/block]


2. Click **Edit** to modify the design details.
3. Edit the content and style of the Bell Icon. This includes the icon image, position, background color, hover text, and so on. 
4. Once done, click **Preview** to view the appearance of the customized Bell Icon. 
5. Click **Save** to save the changes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73352587661a90d174ea0aec7c4cb10b0798c534f73db241443ee0e6f4e1c7fb-2025-01-30_14-57-43.png",
        null,
        "Edit options for Bell Icon"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit options for Bell Icon"
    }
  ]
}
[/block]


# FAQ

### Can users enable both the Card Popup and the Bell Icon at the same time?

Yes. Users can enable both features simultaneously.

### What happens to the bell icon if the user accepts notifications via Card Popup?

If the user accepts notifications, the bell icon will no longer appear, as notifications have already been allowed. 

### What happens if the user blocks the native prompt?

If the user blocks the native prompt (the browser’s built-in opt-in request), the card popup will not be shown again. The bell icon will remain visible and when the user clicks on the bell icon, a GIF will be displayed to nudge users to opt-in notifications.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5c507fa47add574c6d463b103db2aaa4b5c35c5289d06beebad8a41791bc4416-newgif.gif",
        "",
        "Native Prompt Blocked"
      ],
      "align": "center",
      "border": true,
      "caption": "Native Prompt Blocked"
    }
  ]
}
[/block]