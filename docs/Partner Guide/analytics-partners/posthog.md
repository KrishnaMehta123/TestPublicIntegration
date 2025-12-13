---
title: PostHog
excerpt: Analytics Partner
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

[PostHog](https://posthog.com) offers a comprehensive suite of product analytics tools, including funnels, heat maps, session recording, and more, all in a single platform. It enables product and growth teams to track user behavior, measure feature adoption, and optimize product experiences.  
With the CleverTap and PostHog integration, you can:

- Send _Events_ from CleverTap to your PostHog dashboard for detailed product analytics.
- Send _User Profiles_ from CleverTap to PostHog to enrich analytics with behavioral and attribute data.

This integration combines CleverTap’s engagement intelligence with PostHog’s behavioral analytics, giving you a holistic view of the user journey.

# Prerequisites for Integration

Before setting up this integration, ensure you have:

- A valid [PostHog project API key](https://posthog.com/docs/api).
- A CleverTap account with Webhook Campaigns enabled.

# Integrating PostHog with CleverTap

You can integrate PostHog with CleverTap in the following two ways:

- [Send Events from CleverTap to PostHog](doc:posthog#send-events-from-clevertap-to-posthog) OR
- [Send Users from CleverTap to PostHog](doc:posthog#send-users-from-clevertap-to-posthog)

> 🚧 PostHog Webhooks
> 
> Use CleverTap's Webhook Campaigns to forward user events to PostHog when users perform actions on your app or website.
> 
> To set this up, you'll need to configure a webhook on CleverTap using the `POST` HTTP method. This webhook must be configured by the CleverTap team.
> 
> - Contact [CleverTap Support](https://help.clevertap.com/hc/en-us) to enable this webhook for PostHog integration.

## Send Events from CleverTap to PostHog

Events tracked in CleverTap, such as purchases, logins, or custom actions, can be sent to PostHog using Webhook Campaigns so that you can measure funnels, analyze drop-offs, and understand user behavior patterns. To do so, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Webhook_ from the list of messaging channels.
2. Configure campaign details as required and proceed to the _What_ section.
3. In the _Webhook Content_ section, select Content Format as `JSON` and select _Custom Body_.
4. Add the payload for the event you want to upload (example for a purchase event):

```json
{
   "event": "Purchase",
   "api_key": "<ph_project_api_key>",
   "distinct_id": "{{ Profile.Email | default: "test@gmail.com" }}",
   "properties": {
       "item_names": "{{ Profile.MyStuff | default: "Shampoo" }}",
       "value": "{{ Profile.wallet_balance | default: "100" }}"
   }
}
```

Use `{{ }}` or the personalization button in CleverTap to dynamically insert profile properties. For details on accepted parameters, refer to the [PostHog API documentation](https://posthog.com/docs/api).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a21c4b5db73de25ae294727d150fd42b9d258737774e972318f15f3799471f3f-image.png",
        null,
        "Webhook Content"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Webhook Content"
    }
  ]
}
[/block]


5. Click **Preview & Test**  to verify that the event data is being sent.

   [block:image]{"images":[{"image":["https://files.readme.io/99d4dcd20baa52ca50d3c814ec50e2d236eb6ae98dc8e1fceda91bd6f39682b9-image.png",null,"Preview & Test"],"align":"center","sizing":"75% ","border":true,"caption":"Preview & Test"}]}[/block]
6. Once configured correctly, you can see the events reflected in the PostHog dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a77104e8689cb3837faee92e6a218e9d012424193714cc22ff50b6ed8c7de2e-image.png",
        null,
        "PostHog dashboard"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "PostHog dashboard"
    }
  ]
}
[/block]


## Send Users from CleverTap to PostHog

User profile data, such as email, location, or preferences, can also be sent from CleverTap to PostHog, allowing you to combine profile attributes with behavioral events for deeper analytics. This is done through the PostHog _Identify API_ using a Webhook Campaign. To do so, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Webhook_.
2. Configure campaign details as required and proceed to the _What_ section.
3. In the _Webhook Content_ section, select Content Format as `JSON` and select _Custom Body_.
4. Add the following _Identify API_ Payload:

```json
{
  "api_key": "<project_API_key>",
  "event": "$identify",
  "distinct_id": "user distinct id",
  "properties": {
    "$set": {
      "is_cool": "true"
    }
  },
  "timestamp": "2020-08-16T09:03:11.913767"
}
```

Replace `user distinct id` with a CleverTap profile property, such as:

```json
"user distinct_id": "{{ Profile.Email | default: "test@gmail.com" }}"
```

5. In CleverTap, click **Preview & Test** to send a test payload to PostHog.
6. Verify that the user profile is successfully created or updated in your PostHog dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea47c31a1e77215570776ebe86f260c0e950e97e967642eea420a06faee80c92-image.png",
        null,
        "PostHog dashboard"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "PostHog dashboard"
    }
  ]
}
[/block]


# Verify Integration

Once configured:

- _Events_ triggered in CleverTap (such as app purchases or sign-ups) flow into PostHog for funnel and session analysis.
- _User profiles_ from CleverTap enrich PostHog with attributes that can be used in segmentation and retention analysis.
- Changes made to campaigns or payloads in CleverTap are automatically reflected in PostHog data ingestion.

This integration creates a seamless connection between CleverTap engagement and PostHog analytics, enabling product teams to measure, iterate, and optimize experiences faster.