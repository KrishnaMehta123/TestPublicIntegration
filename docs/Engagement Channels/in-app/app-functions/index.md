---
title: App Functions
excerpt: Learn how to use App Functions in In-App
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

CleverTap's App Functions enable you to trigger native OS-level prompts, such as requesting app ratings, push notification permissions, or opening URLs. These functions can be embedded in In-App campaigns or triggered as standalone campaigns to engage users contextually and effectively.

> 📘 Private Beta
>
> App Functions is currently released in Private Beta. If you want access to this feature, contact your Customer Success Manager.

# System App Functions

System App Functions enable direct interaction with native device capabilities through OS-level prompts. These prebuilt functions drive user engagement by requesting critical permissions, collecting feedback, or deep-linking users to relevant destinations.

## Request Push Permission

[Request Push Permission](doc:register-for-push) - Prompt users to enable push notifications using a native OS dialog. This function is essential for re-engagement and retention, as push notifications can send timely and personalized messages without opening the app. 

<Image title="In App Alert Notification" alt="Register for Push In-App" align="center" width="smart" border={true} src="https://files.readme.io/b711a89-Alert_push_primer.png">
  Register for Push In-App
</Image>

## Request App Rating

[Request App Rating](doc:app-rating-primer) - Trigger a native app review prompt integrated with the App Store (iOS) and Google Play (Android). Use this function to encourage satisfied users to leave positive reviews, boosting your app's visibility and credibility.

<Image alt="App Rating In-App" align="center" width="40% " src="https://files.readme.io/dcc93b8ca32a13a7ba12c0a02d2403342daac6c6431b49084b50c3e271763ae6-ChatGPT_Image_Jun_17_2025_08_11_13_PM.png">
  App Rating In-App
</Image>

## Open URL

[Open URL](doc:open-url) - Open a secure web page in the default device browser or use deeplinks to direct users to specific sections within your app. This function is ideal for directing users to external content, such as offers and partner pages, or internal In-app content.

# Use App Functions

You can use App Functions in your in-app campaign in the following two ways: 

* As a *button action* within a message
* As *standalone campaign*. 

## Button Action in In-App Campaign

You can attach an App Function to a button using the [Advanced In-App Builder](doc:advanced-in-app-builder) as follows: 

1. Create an In-App campaign.
2. Go to *What > Advanced In-App Builder*.
3. Add a button element to the layout. 
4. From the *On Tap* list, select *App Function*.
5. Select one of the available functions: [Request App Rating](doc:app-rating-primer)  or [Request Push Permission](doc:register-for-push).   

This will help you set context by displaying a lead-in message before invoking the system prompt.

## Standalone Campaign

You can use App Functions as stand-alone campaigns. It will trigger the system prompt on the user's device. Follow the steps below:

1. Create an In-App campaign.
2. In the **What** section, select the  *App Functions* tab.
3. Select a function from the list, such as Request App Rating, Request Push Permission, or Open URL.
4. Define campaign targeting and scheduling as usual.

> 📘 Open URL System Prompt
>
> When an Open URL prompt is triggered from a stand-alone campaign, it opens the link directly in the device’s browser, which may interrupt the in-app experience.

# Event Tracking Matrix

CleverTap tracks user interactions only within its In-App campaigns, such as button clicks and other campaign-driven actions. Due to OS limitations, access to interactions with native system prompts (such as permission popups managed by the device’s operating system) is unavailable. 

Refer to the following matrix to understand which events can and cannot be tracked.

| **App Function**            | **Used As**   | **What's Tracked**               | **Notes**                                                                                          |
| --------------------------- | ------------- | -------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Request App Rating**      | Button Action | Viewed, Clicked (on In-App only) | OS controls the actual rating prompt. No way to track if the user completed the rating.            |
|                             | Standalone    | None                             | Interaction tracking is limited by the OS.                                                         |
| **Request Push Permission** | Button Action | Viewed, Clicked (on In-App only) | OS controls the actual push permission prompt. No way to track if the user granted the permission. |
|                             | Standalone    | Viewed                           | You can only track if the In-App prompt was displayed.                                             |
| **Open URL**                | Button Action | Viewed, Clicked                  | Tracks CTA clicks, not the destination URL.                                                        |
|                             | Standalone    | Viewed                           | Tracks the impression, not clicks.                                                                 |
