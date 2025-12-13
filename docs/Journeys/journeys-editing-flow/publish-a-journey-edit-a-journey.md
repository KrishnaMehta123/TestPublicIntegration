---
title: Publish a Journey
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

 After building your Journey, you can save it as a draft for further editing or publish it to make it live. This document offers a step-by-step guide to managing CleverTap Journeys, detailing the processes of saving drafts, publishing Journeys, and activating them effectively.

Once a Journey is published, you can still edit it to make changes. This creates a new version of the Journey without disrupting the live version. For more information, refer to [Edit a Journey](doc:edit-a-journey). 

# Save Journeys

Once you create and save a journey, the status of the Journey changes to the _[Draft state](doc:journey-states#draft-state)_. You can make more changes to it at a later date or time. Any unsaved changes in this state may be lost unless explicitly saved.

To save a journey, follow these steps:

1. Click **Save Draft** from the Journey canvas. The _Save this journey as_ popup opens. 
2. _Enter journey name_ and click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/570cbb3-Save_Journeys.png",
        "Save a Journey as a draft",
        912
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Save Journeys"
    }
  ]
}
[/block]


The other journey actions, such as _Archive_, _Stop_, and so on, are unavailable, as the journey has still not been published. 

# Publish Journeys

After setting up the Journey, click **Publish** on the Journey canvas to activate it. The _Publish journey_ popup opens. Enter or verify the Journey name. You can also update the name here if needed. Add a description or summary for your Journey to help understand its purpose and click **Publish**. For example, _This journey aims to onboard new users by sending a welcome push notification immediately after signup_. 

The description can be up to 120 characters long.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b89aa78c9ac56edb625aa80b84f6c6eeb7ebaaa1d50b9c8cf07c520bd3cc22f-Publish_a_Journey.png",
        "Publish the Journey",
        540
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Add a Description and Publish the Journey"
    }
  ]
}
[/block]


You can view the description from the Journey List page. Click the ![](https://files.readme.io/cb2b6e04c22c3145eae93b4cf2c3b463b799052b6581563c12ba4b2bf69b327c-ellipses_icon.png) icon and select _View description_ from the available actions. You can also edit the description when editing the Journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/62e0cb410bb851eabeccf029e103e6c1a967eb80db7303da785c37197de277e6-View_Description.png",
        "",
        "View Journey Description"
      ],
      "align": "center",
      "border": true,
      "caption": "View Journey Description"
    }
  ]
}
[/block]


Once you publish a journey, the journey status on the _Journey List_ page changes to _Running_ or _Scheduled_. 

You can edit any part of the published Journey, including entry criteria, paths, and content, by creating a new version. This allows you to iterate without disrupting the currently running version. You can still edit the _What_ section of a message node inline without creating a new version. For more information about how editing works, refer to [Edit a Journey](doc:edit-a-journey). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c84266b1c924ebf6f6b522818f7ca5caf558c195b510fcab67f7960ff42e6b91-Edit_Journey_Popup.png",
        "",
        "Edit a Currently Active Journey"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit a Currently Active Journey"
    }
  ]
}
[/block]


# Journey Activation, User Qualification, and Message Delivery

Once the journey is activated, users qualify, and messages are sent to the users based on the [Journey Entry Timeline](doc:setup-journey#define-the-journey-entry-timelines) as follows:

- **Activation**: Journeys activate immediately after publishing or at a scheduled start time.
- **User Qualification**: Users qualify for the Journey at midnight the day after activation. It applies to both multi-date and recurring Journeys.
- **Message Delivery**: Messages are sent to users starting from the night of publishing and continue as scheduled. It applies to both multi-date and recurring Journeys.