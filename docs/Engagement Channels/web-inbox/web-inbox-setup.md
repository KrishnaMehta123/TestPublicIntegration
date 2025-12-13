---
title: Web Inbox Setup
excerpt: Learn about the configurations required to set up Web Inbox on your website
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> ❗️ Prerequisite
> 
> 1. Ensure that you have integrated CleverTap's new [Web SDK](https://developer.clevertap.com/docs/web-quickstart-guide#option-a-add-the-clevertap-javascript-library-manually-to-your-website).
> 2. Follow the steps for integration mentioned in the [Web Inbox developer guide](https://developer.clevertap.com/docs/web-inbox).

As a prerequisite for running _Web Inbox_ campaigns, you must also complete the Web Inbox _Setup_.  To complete the Web Inbox Setup, navigate to your CleverTap dashboard > _Settings_ > _Channels_ > _Web Inbox_.  This configuration allows you to define the overall appearance of your Web Inbox window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e067859-web_inbox_s1.png",
        "Prerequisite Setup for Web Inbox ",
        2298
      ],
      "align": "center",
      "border": true,
      "caption": "Prerequisite Setup for Web Inbox"
    }
  ]
}
[/block]

## Web Inbox Window Configuration

Under the Content tab, define the following as per your requirements:

1. The  _Title_ for Notification Panel.
2. The type of categories (maximum of ten) you wish to assign to your messages. For example, Promotional, Primary, Socials, etc.
3. The Element ID of your website's element clicking upon which opens the Web Inbox window.
4. You can also set the maximum number of messages that can be displayed in the user's inbox. The messages will be displayed on a first in first out basis.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/86904b2-web_inbox_setup_2.png",
        "Configure Web Inbox Layout",
        2312
      ],
      "align": "center",
      "border": true,
      "caption": "Web Inbox Window Configuration"
    }
  ]
}
[/block]

> 📘 Note
> 
> The Element ID is a mandatory input field. It helps CleverTap locate the web element on your website where it needs to display the Web Inbox window.

## Web Inbox Window Styling

Under the _Style_ tab, you get the complete flexibility to customize the colors for:

- Notification panel 
- Header
- Category tabs
- Cards
- Buttons
- Notification badge

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c62096-web_inbox_style_1.png",
        "Customize your Web Inbox Window",
        2202
      ],
      "align": "center",
      "border": true,
      "caption": "Web Inbox Window Styling"
    }
  ]
}
[/block]

After selecting the desired colors, click _Save_ to save your configurations.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9b3038-web_inbox_style_3.png",
        "Customize your Web Inbox Window appearance",
        1076
      ],
      "align": "center",
      "border": true,
      "caption": "Web Inbox Customizations"
    }
  ]
}
[/block]

After you save your configurations, you can start [creating Web Inbox campaigns](https://docs.clevertap.com/docs/web-inbox-create-message).