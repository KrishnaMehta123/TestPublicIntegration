---
title: App Rating Primer
excerpt: >-
  Learn how to trigger app store ratings at peak user satisfaction using
  CleverTap In-App App Rating Primers.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
App Rating Primers are contextual In-App messages that prompt users to rate your app during moments of high satisfaction. These prompts are most effective after a milestone, such as a successful transaction or subscription renewal, when users are more likely to leave a positive review. Such timely prompts improve your app store rating, increase visibility, and boost credibility without interrupting user experience.

<Image alt="App Rating Primer using CleverTap" align="center" width="25% " border={true} src="https://files.readme.io/26ae02a4006837d6073938f62264fa762b71e55791ee2295694756cfe5ea676d-image.png">
  App Rating Primer using CleverTap
</Image>

> 📘 Tip
>
> Precede the OS rating prompt with a message that highlights the value of feedback. This is especially effective after a purchase, milestone achievement, or renewal.

# Create App Rating Primer Campaign

You can use App Functions to trigger the native app store rating prompt. This campaign excludes users who have already seen the prompt, focusing on engaged users likely to provide feedback. Follow the steps below:

1. Go to the *Campaigns* page and select *In-App Messages* from the list of messaging channels.
2. In the *Who* section, select a trigger event such as *Onboarding Complete*, *Purchased*, or *Subscribed*.
3. \`In the *What* section, select the *Advanced In-App Builder*. For more information, refer to [Advanced In-App Builder](doc:advanced-in-app-builder#container).
   1. Add a button element to the layout. 
   2. Set the *On Tap*  Container action of the button element to *App Function*.
   3. Select  *Request App Rating* from the *Action* list.

<Image alt="App Rating Primer Campaign" align="center" border={true} src="https://files.readme.io/e6b0c6af7c87e1fb1d54a1ce6fcd3ba58a71c9bae819db2410dd4aecb04d5460-image.png">
  App Rating Primer Campaign
</Image>

4. In the *When* section, define the schedule for message delivery.  You must be mindful of the frequency of messaging to the user. For more information, refer to [Using Frequency Caps in CleverTap](https://docs.clevertap.com/docs/messaging-frequency-caps).  It is recommended to use the following options to optimize your messaging: 

* Exclude from Global campaign limits
* Deliver upto X times ever 
* Deliver upto X times in the Y period of time

<Image alt="Manage Frequency Caps" align="center" width="70% " border={true} src="https://files.readme.io/5b7763c94dd4481a6545254c94bdaa1b1d2afbd5287575897380db4572ad2d57-Screenshot_2025-06-18_at_17.53.53.png">
  Manage Frequency Caps
</Image>

7. Publish your campaign.

# Considerations

* The app store rating prompt is *controlled by the OS*.
* *Prompt visibility is not guaranteed*; the system may suppress repeated prompts.
* You *cannot track* rating submissions or view outcome data due to OS restrictions.

# App Rating Primer Best Practices

A well-placed app rating prompt can significantly increase your average store rating. Keep these guidelines in mind:

* **Time It Right**: Ask for ratings after users complete a valuable action. For example, *Completed Purchase*, *Renewed Subscription*.
* **Avoid Cold Prompts**: Don’t ask for a rating on first app launch or before users have experienced value.
* **Use Friendly Messaging First**: Instead of immediately triggering the system prompt, use a custom message that asks for feedback politely.
* **Always Offer a Choice**: Include both *Rate Now* and *Not Now* buttons to maintain user trust.
* **A/B Test for Performance**: Run tests with different messaging styles, CTAs, and event triggers to optimize for conversion.
