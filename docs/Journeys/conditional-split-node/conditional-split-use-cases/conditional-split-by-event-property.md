---
title: Conditional Split By Event Property
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

The Conditional Split node can branch users based on event properties, such as `product_category`, `order_value`, or `device_type`. Only String and Boolean event property types are supported. You will encounter a validation error if an unsupported event property data type is used (for example, arrays or numbers). Event property–based splits are supported when the previous node is an Action or Inaction node in a Live Journey

The table below outlines where event property-based splits are supported:

| Journey Type | Trigger Type | When Split Check Happens | Event Property Support | Event Property Type |
| ------------ | ------------ | ------------------------ | ---------------------- | :------------------ |
| Live         | Action       | In real time             | Yes                    | String, Boolean     |
| Live         | Inaction     | In real time             | Yes                    | String, Boolean     |

## Target Evaluation Type: Action/Inaction Node

When an Action or Inaction node triggers a journey, the Conditional Split node can evaluate the event properties from that specific action as soon as the user reaches the node.

For example, a job search app wants to tailor the follow-up messages based on the job category a user applies to.  With Conditional Split, the journey triggered by the _Application Submitted_ event (Action node) can immediately route users by evaluating the `job_type` event property:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb2677f696b8fa65b1007ce4cf6e6c70a79d8ead473b88285273e11ff546989f-CS_by_Event_Property_Setup.png",
        "",
        "Conditional Split by Event Property Setup "
      ],
      "align": "center",
      "border": true,
      "caption": "Conditional Split by Event Property Setup "
    }
  ]
}
[/block]


- `job_type` = Tech → Sends an email highlighting tech interview prep resources, followed by a push with tech role recommendations.
- `job_type` = Marketing → Sends an email with resume tips for creatives, followed by a push featuring top marketing jobs.
- Others → Sends a general email on job search tips, followed by a push notification linking to personalized job discovery tools.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2de98fb3b3f88e2be92539e282b877e9ca2c360aeca71a537a609cb219138368-CS_by_Event_Property_Journey.png",
        "",
        "Conditional Split by Event Property Journey"
      ],
      "align": "center",
      "border": true,
      "caption": "Conditional Split by Event Property Journey"
    }
  ]
}
[/block]


Conditional Split eliminates the delay between the event and personalized engagement. It turns user actions into immediate, contextual engagement, simplifying journey design.