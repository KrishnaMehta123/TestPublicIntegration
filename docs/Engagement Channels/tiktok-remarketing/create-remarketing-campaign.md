---
title: Create TikTok Remarketing Campaign
excerpt: Learn how to set up the TikTok Remarketing campaign for TikTok
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Create a TikTok Remarketing Campaign

Follow these steps to create a new remarketing campaign on TikTok:

1. From the dashboard, navigate to _Campaigns_. 
2. Click **+ Campaign** button.
3. From the _Messaging Channels_ list, select _TikTok._ 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c8f07ab0cd9b2a13bbbb44b0136e0d334d99bb35d2ed00bfb4a89f16693d9808-tik1.jpg",
        "",
        "TikTok Create Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "TikTok Create Campaign"
    }
  ]
}
[/block]


The campaign page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/33f32f21d5583b5f272027a0664c3811d826bcfd22a0fdacb603bdeb62f63029-tiktok_campaigns.png",
        "",
        "TikTok Campaign"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "TikTok Campaign"
    }
  ]
}
[/block]


## Start Campaign Setup

The _Start here_ section displays the setup information. 

**Qualification criteria**: Here, you must define the criteria for your target audience. You can deliver the TikTok ad based on the user's past or live behavior.

**Ad Account**: From the Ad Account drop-down, select the linked TikTok account to which you want to export the audience. 

**Set a Goal:**  You can track your campaign conversion by setting a specific conversion goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional. For example, you can set a conversion goal to analyze the users who purchased within 5 days of publishing the campaign.

## Define the Target Audience

Under the **Who** section, you must define the target audience for your campaign. You can create a [new segment ](doc:setup-segment)or use a previously saved user segment from the segment list. Define the audience according to your use case. A sample use case is Re-targeting users who have viewed a particular product but have not purchased it in the last 30 days. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign only to reach users who meet specific criteria. 

For example, you can display TikTok Ads to users who live in the United States and are over twenty years old. The following image represents a sample target segment filtered using additional user properties, such as location and age, to reach the required audience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bfc0fd496126aa45270c77e26cf6ce8d711288322277e428f2e03ddf0e46d40a-Segment.jpg",
        "Add Multiple User Properties",
        2202
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]


The following table provides a description for the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Reachability",
    "3-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "3-2": "Unsubscribed email = No",
    "4-0": "App Fields",
    "4-1": "App field filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. CleverTap's SDK sends this information for each device that has your app, which means a single user can have multiple devices associated with their user profile.",
    "4-2": "OS Version = 10"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


### Control Group and Target Cap

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups)

You can limit the number of users receiving the Ad.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/475e7c73530164dc22d679d881f098cf001ad3c80a34854f937a1fed704109d4-control_group_and_target_cap.jpg",
        "",
        "Control Group and Target Cap."
      ],
      "align": "center",
      "border": true,
      "caption": "Control Group and Target Cap."
    }
  ]
}
[/block]


A relevant use case is distributing a limited-time offer to specific users. If your campaign's total reach exceeds the number of available coupon codes, you can limit the number of users who will receive the message.

## What Section

The What section allows you to export an audience based on criteria defined in the Who section.

### Export Audience

The What section enables you to export the audience based on the criteria you define for your target audience in the Who section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/99fc9109ca2a9c08f4f99fe3b6d5e001785dcdb24b80263a5064940bf206e296-Tikitok_what.jpg",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


Here are two ways to define the export behavior:

- **Modify Existing Audience** -  If an existing audience qualifies the criteria, select this option to add qualified users to that audience.
- **Create New Audience** - Choose this option to target a new audience based on the selected qualification criteria. If you are creating a new audience, define the following:
  - **Audience Name:**  
    Enter a unique name for the audience you’re creating or updating. This name must be specific enough to quickly identify the audience later.
  - **Audience Description:**  
    Provide a brief description (up to 200 characters) of the audience, explaining the common characteristics or behaviors that define this group. This description helps maintain clarity when managing multiple audiences.

You can also select the user properties that you want to export for the target segment, such as (you can pick either one or both): 

- **Email:** Target users based on their registered email addresses.
- **Phone**: Use phone numbers for targeting.

## Define the Remarketing Campaign Schedule

Under the When section, you must define the timeframe for your campaign to start and end. 

Past behavior campaigns can be scheduled to run:

- On a specific date and time.
- On multiple specified dates and times.
- Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

- In response to a user event.
- User event/inaction combination (for example, abandoned cart scenario).

You can set specific dates and times to control when your ads will be live. Depending on the campaign's goals, you can also set recurring schedules or specific time windows when the ads will be shown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3b7485479f9e0354b103297cd4fb617954fb5955ad392d9d116af8b6493e20d9-WHEN.jpg",
        "",
        "Define the Remarketing Schedule"
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Remarketing Schedule"
    }
  ]
}
[/block]


## Publish Campaign

After previewing the overall configuration of your remarketing campaign, finalize your campaign by clicking **Publish Campaign.**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Final Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]