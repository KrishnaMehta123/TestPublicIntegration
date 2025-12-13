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

As a prerequisite for running *Web Inbox* campaigns, you must also complete the Web Inbox *Setup*.  To complete the Web Inbox Setup, navigate to your CleverTap dashboard > *Settings* > *Channels* > *Web Inbox*.  This configuration allows you to define the overall appearance of your Web Inbox window.

<Image title="Prerequisite Setup for Web Inbox " alt={2298} align="center" border={true} src="https://files.readme.io/e067859-web_inbox_s1.png">
  Prerequisite Setup for Web Inbox
</Image>

## Web Inbox Window Configuration

Under the Content tab, define the following as per your requirements:

1. The  *Title* for Notification Panel.
2. The type of categories (maximum of ten) you wish to assign to your messages. For example, Promotional, Primary, Socials, etc.
3. The Element ID of your website's element clicking upon which opens the Web Inbox window.
4. You can also set the maximum number of messages that can be displayed in the user's inbox. The messages will be displayed on a first in first out basis.

<Image title="Configure Web Inbox Layout" alt={2312} align="center" border={true} src="https://files.readme.io/86904b2-web_inbox_setup_2.png">
  Web Inbox Window Configuration
</Image>

> 📘 Note
>
> The Element ID is a mandatory input field. It helps CleverTap locate the web element on your website where it needs to display the Web Inbox window.

## Web Inbox Window Styling

Under the *Style* tab, you get the complete flexibility to customize the colors for:

* Notification panel 
* Header
* Category tabs
* Cards
* Buttons
* Notification badge

<Image title="Customize your Web Inbox Window" alt={2202} align="center" border={true} src="https://files.readme.io/0c62096-web_inbox_style_1.png">
  Web Inbox Window Styling
</Image>

After selecting the desired colors, click *Save* to save your configurations.

<Image title="Customize your Web Inbox Window appearance" alt={1076} align="center" border={true} src="https://files.readme.io/c9b3038-web_inbox_style_3.png">
  Web Inbox Customizations
</Image>

After you save your configurations, you can start [creating Web Inbox campaigns](https://docs.clevertap.com/docs/web-inbox-create-message).
