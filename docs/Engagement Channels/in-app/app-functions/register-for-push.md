---
title: Push Primer
excerpt: Prompt the user to grant push notification permissions.
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

Push Primer is an In-App message that introduces the benefits of push notifications before invoking native OS permissions. It acts as a reversible, pre-permission layer that sets expectations and builds trust by helping users understand the value of enabling notifications, such as receiving timely updates or exclusive offers. By offering this context, Push Primer can improve opt-in rates and re-engage users who have yet to grant permission.

<Image alt="Push Primer using CleverTap" align="center" width="160px" border={true} src="https://files.readme.io/199c0af6337ee26538d7c6abbf1fd6b441c98f240e40b74de0fb4a2690b5618d-In-app_animation.gif">
  Push Primer using CleverTap
</Image>

# Create Push Primer Campaign

To create a push primer campaign, create a regular In-App message using with the [Advanced In-App Builder](doc:advanced-in-app-builder#container). Set the button action to *Request Push Permission*, and CleverTap automatically recognizes it as a push primer and displays the system prompt to request notification permission. 

> 📘 Note
>
> * If the users have previously denied push permission, tapping the prompt will redirect them to the app settings,
> * On iOS, the system-level push primer prompt is shown only once and cannot be triggered again.

To create a Push Primer campaign, perform the following steps:

1. Go to the *Campaigns* page and select *In-App Messages* from the messaging channels list.
2. In the *Who* section, select only the trigger event, such as *Charged*.  You do not need to specify a segment in this step. 

> 📘 Note
>
> The campaign automatically excludes users who have already granted push permission allowing you to focus on new users and those who need to be re-engaged.

3. In the *What* section, select the *Advanced In-App Builder*.   For more information, refer to [Advanced In-App Builder](doc:advanced-in-app-builder#container). 
   1. Add a button element to the layout. Create your In-App campaign. 
   2. Set the  *On Tap*  Container action of the button element to *App Function*.
   3. Select  *Request Push Permissions* from the *Action* list.

<Image alt="Push Primer Campaign" align="center" border={true} src="https://files.readme.io/8332ecbbd83f6d357e7630d31aaa05d892b2ba14e2b5d68f14e674e1635bd02a-image.png">
  Push Primer Campaign
</Image>

4. In the *When* section, select the campaign frequency and display rules to avoid overwhelming users. For example, users who reject the notification or opt for *Maybe Later*.

<Image alt="Manage Frequency Caps" align="center" width="70% " border={true} src="https://files.readme.io/5b7763c94dd4481a6545254c94bdaa1b1d2afbd5287575897380db4572ad2d57-Screenshot_2025-06-18_at_17.53.53.png">
  Manage Frequency Caps
</Image>

> 📘 Create a Segment for Users Based on Android Version
>
> Create a separate segment for Android users who use android 13 and above. Filter with the *App Field* > *OS Version* > *contains* > (Android Versions such as 13,14,15). This ensures that Push Primer messages are shown only to users on devices where notification permission is required on runtime.
>
> This will avoid sending the campaign to users on Android 12 and below, where the notifications do not require any permission and it is granted on app install itself.
>
> To do so, in the In-App Campaign, go to the *Who* section and, under Target Segment, add filters for the app field OS Version that contain values such as 13, 14, and so on.
>
> <Image align="center" className="border" width="65% " border={true} src="https://files.readme.io/83bef9b916c5b72c6dbb5e150e4a3f5433350133d28cda67723bbc904660550c-image.png" />

5. Publish the campaign.

# Push Primer Best Practices

Push primers are one-time prompts to request user consent for notifications. A well-timed and clearly worded primer significantly improves opt-in rates and long-term user engagement.

* **Display Only Once at a Strategic Moment**: Trigger the Push Primer after a high-value event (for example, completing onboarding or a first purchase), when users are more receptive to receiving notifications. *Contextual timing can almost triple push opt-ins compared to first-launch prompts*. 

* **Delay Until Value is Understood**:  Let users experience the core features before prompting. Value recognition increases the likelihood of opt-in. *Average opt-in rates can rise by 45% when shown after the third session*.

* **Communicate Clear Benefits**: Use specific, value-driven language such as:

  * *Track your delivery in real-time*
  * *Get notified of price drops instantly*

  Avoid vague text such as *Enable notifications to stay updated.*

* **Trigger After Intent-Driven Events**: Display primers after meaningful user actions such as *Added to Cart*, *Search Completed*, or *Onboarding Finished*. These events correlate with higher intent and perceived utility of notifications.

* **Keep Messaging Short and Actionable**: Use a concise headline and a one-line benefit statement. 

```
    For example: _Want delivery updates? Enable push alerts now._ 
```

* Stick to plain language and avoid any technical jargon.
* Use compelling visuals and clear reasons why the user should opt in.
* **Provide Clear, Non-Coercive Choices**: Always include two obvious options, such as *Allow Notifications* and *Not Now.* Avoid dark patterns or forced opt-ins.
* **A/B Test Message Copy and Timing**: Continuously test variations in CTA labels, tone, and trigger moments to determine what performs best for your audience.
