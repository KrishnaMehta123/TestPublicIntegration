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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26ae02a4006837d6073938f62264fa762b71e55791ee2295694756cfe5ea676d-image.png",
        null,
        "App Rating Primer using CleverTap"
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "App Rating Primer using CleverTap"
    }
  ]
}
[/block]


> 📘 Tip
> 
> Precede the OS rating prompt with a message that highlights the value of feedback. This is especially effective after a purchase, milestone achievement, or renewal.

# Create App Rating Primer Campaign

You can use App Functions to trigger the native app store rating prompt. This campaign excludes users who have already seen the prompt, focusing on engaged users likely to provide feedback. Follow the steps below:

1. Go to the _Campaigns_ page and select _In-App Messages_ from the list of messaging channels.
2. In the _Who_ section, select a trigger event such as _Onboarding Complete_, _Purchased_, or _Subscribed_.
3. \`In the _What_ section, select the _Advanced In-App Builder_. For more information, refer to [Advanced In-App Builder](doc:advanced-in-app-builder#container).
   1. Add a button element to the layout. 
   2. Set the _On Tap_  Container action of the button element to _App Function_.
   3. Select  _Request App Rating_ from the _Action_ list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6b0c6af7c87e1fb1d54a1ce6fcd3ba58a71c9bae819db2410dd4aecb04d5460-image.png",
        null,
        "App Rating Primer Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "App Rating Primer Campaign"
    }
  ]
}
[/block]


4. In the _When_ section, define the schedule for message delivery.  You must be mindful of the frequency of messaging to the user. For more information, refer to [Using Frequency Caps in CleverTap](https://docs.clevertap.com/docs/messaging-frequency-caps).  It is recommended to use the following options to optimize your messaging: 

- Exclude from Global campaign limits
- Deliver upto X times ever 
- Deliver upto X times in the Y period of time

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b7763c94dd4481a6545254c94bdaa1b1d2afbd5287575897380db4572ad2d57-Screenshot_2025-06-18_at_17.53.53.png",
        null,
        "Manage Frequency Caps"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Manage Frequency Caps"
    }
  ]
}
[/block]


7. Publish your campaign.

# Considerations

- The app store rating prompt is _controlled by the OS_.
- _Prompt visibility is not guaranteed_; the system may suppress repeated prompts.
- You _cannot track_ rating submissions or view outcome data due to OS restrictions.

# App Rating Primer Best Practices

A well-placed app rating prompt can significantly increase your average store rating. Keep these guidelines in mind:

- **Time It Right**: Ask for ratings after users complete a valuable action. For example, _Completed Purchase_, _Renewed Subscription_.
- **Avoid Cold Prompts**: Don’t ask for a rating on first app launch or before users have experienced value.
- **Use Friendly Messaging First**: Instead of immediately triggering the system prompt, use a custom message that asks for feedback politely.
- **Always Offer a Choice**: Include both _Rate Now_ and _Not Now_ buttons to maintain user trust.
- **A/B Test for Performance**: Run tests with different messaging styles, CTAs, and event triggers to optimize for conversion.