---
title: Product Experiences (Legacy) Setup
excerpt: Learn how to setup Product Experiences (Legacy)
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Create keys and segments for your app to enable product experiences. 

# Create Keys

These are the keys that you have defined in your app code. You can map these keys from the CleverTap dashboard and control the configuration of your app. Keys can be used for Product Config, Feature Flags, and A/B Tests.

To create keys:

1. Navigate to Product Experiences >  Setup > Keys
2. Click +Key to create a new key. 

> 📘 Note
> 
> The name of the key defined here must match the name of the key defined in the app. This name cannot be changed later. You can add up to 500 keys.

3. Add the Key definition. 

Let us add some sample values:

You can now activate or deactivate the dark mode based on the Keys. The default value that the app is expecting for this key is `3`.  These values are set in your app. Let us assume that the key value 3 means to activate the feature, and 4 means to deactivate the feature. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eafa5c2-product_exp_keys.png",
        "Add Key Details from CleverTap's Keys page",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Add Key Details"
    }
  ]
}
[/block]


4. Click Save. The `dark_mode` key is now listed on the Manage Keys page. 

## Edit/Archive Keys

1. Navigate to Product Experiences >  Setup > Keys. The Keys page appears. 
2. Click the ellipsis menu to edit or archive a key. Only the default value and description can be edited after saving a key.

You can view all the archived keys by selecting the Archived Keys box at the bottom of the key's list.  If a key is used in a product config or feature flag then it cannot be archived. 

# Create Segments

The segments are the target users who will receive app changes. These segments can be used for Product Config, Feature Flags, and A/B Tests.

To define the segments:

1. Navigate to Product Experiences >  Setup > Segments
2. Click +Segment to create a new segment.
3. Name the segment.
4. Create a segment by users who performed and/or did not perform an event.  You can also create segments for user properties such as demographics, geography, and so on. For our example, create a segment of iPhone users living in New York. 
5. Save the segment. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/483d933-ProductExp_Segment_Create.png",
        "Create segments who will receive app changes",
        1182
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Create Segments Who will Receive App Changes"
    }
  ]
}
[/block]


## Edit/Clone a Segment

1. Navigate to Product Experiences >  Setup > Segments. The Segments page appears. 
2. Click the ellipsis menu to edit or clone a segment. For example, you may want to edit the city and create another user segment for Miami. 

# Create Goals

Goals are used to evaluate the performance of an A/B test. It is an event and when a user performs this event, it is considered a conversion.  
Navigate to Product Experiences >  Goals. Create a goal and save it. This goal is now available for selection in Product Experiences.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8726071-AB_Goals.png",
        "Create goals to evaluate the performance of A/B tests",
        874
      ],
      "align": "center",
      "border": true,
      "caption": "Create Goals for A/B Tests"
    }
  ]
}
[/block]


## Archive Goals

- Navigate to Product Experiences >  Goals.
- Click the archive icon to archive a goal. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/169925e-AB_Segment_Goals_Archive.png",
        "Archive goals for A/B tests",
        879
      ],
      "align": "center",
      "border": true,
      "caption": "Archiving Goals for A/B Tests"
    }
  ]
}
[/block]


You can view all the archived Goals by selecting the show archived goals box at the bottom of the goals list.  If a goal is used in a product experience then it cannot be archived.

# Mutually exclusive A/B tests

This is a global setting that is applicable only to A/B tests.  You can choose to exclude your segment from all other experiments. It applies only to the new experiments that are created after this setting is enabled. For example, if it is set as disabled at a global level, you will have to enable it on each subsequent test. The users who qualify for this A/B test are unique and they are not shared across any other experiment. 

1. Navigate to Product Experiences > Settings > Mutually exclusive A/B tests.
2. Turn on the toggle.  These users will be included only in one A/B test at a time. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/463bdd2-AB_Settings_mutually_exclusive_users.png",
        "Toggle ON the Mutually exclusive A/B tests options",
        870
      ],
      "align": "center",
      "border": true,
      "caption": "Enabling Mutually exclusive A/B tests"
    }
  ]
}
[/block]


# Video Tutorial

For further information, you can watch the following video on product configs and feature flags:

[block:embed]
{
  "html": "<iframe class=\"embedly-embed\" src=\"//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2FtfHhsvWvPxk%3Ffeature%3Doembed&display_name=YouTube&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DtfHhsvWvPxk&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2FtfHhsvWvPxk%2Fhqdefault.jpg&key=7788cb384c9f4d5dbbdbeffd9fe4b92f&type=text%2Fhtml&schema=youtube\" width=\"854\" height=\"480\" scrolling=\"no\" title=\"YouTube embed\" frameborder=\"0\" allow=\"autoplay; fullscreen; encrypted-media; picture-in-picture;\" allowfullscreen=\"true\"></iframe>",
  "url": "https://www.youtube.com/watch?v=tfHhsvWvPxk",
  "title": "Product Demo: Product Configs & Feature Flags",
  "favicon": "https://www.google.com/favicon.ico",
  "image": "https://i.ytimg.com/vi/tfHhsvWvPxk/hqdefault.jpg",
  "provider": "https://www.youtube.com/",
  "href": "https://www.youtube.com/watch?v=tfHhsvWvPxk",
  "typeOfEmbed": "default"
}
[/block]