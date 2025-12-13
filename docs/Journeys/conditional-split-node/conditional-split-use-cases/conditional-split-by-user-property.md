---
title: Conditional Split By User Property
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

The Conditional Split node can be used to branch users based on user properties such as `plan_type`, `location`, `subscription_status`, or any other attribute stored in the user profile. You can use user properties with _String_ or _Boolean_ values for your conditions. You will encounter validation errors if unsupported user property types (arrays or objects) are selected.

Conditional split evaluation for target users is closely related to the criteria of target evaluation.

## Target Evaluation Type: Live Node

If you choose Action, Inaction, or Date/Time as the target evaluation criteria, the Conditional Split node instantly checks user properties to determine the next path in the journey. As soon as the user reaches the Conditional Split node, CleverTap checks the latest value of the selected user property and routes the user down the first matching path.

For example, a music streaming app wants to split users based on their favorite music genre and personalize recommendations. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3cd26775e2839146fa52b99da6e1ea0591329a495723dd8b78abb0c9890ffb9f-CS_Setup_for_split_by_User_Property_.png",
        "",
        "Conditional Split by User Property Setup for Trigger Type Action Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Conditional Split by User Property Setup for Trigger Type Action Node"
    }
  ]
}
[/block]


The Action node (here, Onboarding Complete) triggers the journey, and users are split immediately based on the `preferred_genre` user property as follows:

- `preferred_genre` = Pop → Sends an email with trending pop playlists, followed by a push notification after 2 days to nudge engagement.
- `preferred_genre` = Jazz → Sends an email with a curated jazz essentials collection, followed by a push notification after 2 days.
- Others → Sends an email with Trending Chartbusters, followed by a push notification after 2 days.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dc72141885fbe5763de04f6564ac2fb8a2166cd6531d365d526ac9b3c11c9f11-CS_by_User_Property_Journey.png",
        "",
        "Conditional Split by User Property for Trigger Type Action Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Conditional Split by User Property for Trigger Type Action Node"
    }
  ]
}
[/block]


## Target Evaluation Type: Past Behavior Node

CleverTap uses a unified view of user profile and behavior to determine the correct path, enabling precise and contextual targeting. When the target evaluation is of a past behavior segment type, the conditional split node evaluates user properties based on how the PBS node is configured.

- **PBS as Entry Node**  
  If the journey’s entry node is a Past Behavior Segment (PBS) followed by a Conditional Split node, the Conditional Split evaluates users daily at midnight. This allows newly qualifying users (based on updated properties or behaviors) to enter the appropriate path from that day onward.
- **PBS Within Journey Flow**  
  If a PBS node is used mid-journey (within the journey flow) and is followed by a conditional split node, user property evaluation still happens at midnight as per the scheduled PBS run. Conditional split evaluation happens as soon as users reach the conditional split node after completing any intermediate nodes (for example, Delay Node or other logic nodes). The Conditional Split does not re-evaluate; it uses the user property values available during PBS evaluation.

For example, an electronics retail brand wants to re-engage users who showed interest in specific product categories (such as TVs, mobiles, or ACs) but have not returned in the past 14 days.

- Trigger: PBS segment with conditions:
  - `last_browsed_category` = Electronics
  - `last_active_date` > 14 days ago

When the journey starts, users are split based on their `preferred_device_type` user property:

- `preferred_device_type` = TV → Sends an email with trending Smart TV deals, followed by a push after 2 days.
- `preferred_device_type` = Mobile → Sends mobile deals via email, followed by a WhatsApp message.
- No Preference → Sends a fallback email with a coupon, followed by a promotional push notification

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b906596199cbdd7e125ef53cb89887160037f39373078c3285368eed4b38834-CS_by_User_Property_PBS_Journey.png",
        "",
        "Conditional Split by User Property for Trigger Type PBS Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Conditional Split by User Property for Trigger Type PBS Node"
    }
  ]
}
[/block]