---
title: Setting Up a Journey
excerpt: >-
  Understand how to set up your journey with settings like entry criteria,
  timelines, and timezones.
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

Set up your journey by defining: 

- [Journey Entry](https://docs.clevertap.com/docs/setup-journey#define-the-journey-entry-criteria)
- [Journey Entry Timelines](https://docs.clevertap.com/docs/setup-journey#define-the-journey-entry-timelines)
- [DND and Timezone](https://docs.clevertap.com/docs/setup-journey#dnd-and-timezone)
- [Control Group](https://docs.clevertap.com/docs/setup-journey#define-the-control-group)
- [Journey Timeout](https://docs.clevertap.com/docs/setup-journey#select-a-journey-timeout)

The first step to building a Journey is defining the Journey's configuration within the Setup node.  
Click _Journeys_ from the dashboard and click the **+Journey** button to set up a Journey. A new Journey canvas is displayed. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1ea159c-Journey_Setup.png",
        "Begin Journey creation using setup node",
        1348
      ],
      "align": "center",
      "border": true,
      "caption": "Journey Setup"
    }
  ]
}
[/block]


Click **Setup**. The _Setup_ window displays.  Enter the **Journey Name**. 

Using keyboard shortcuts, you can efficiently set up and manage journeys. Click the ![](https://files.readme.io/62eb9da-Keyboard_Shortcuts.png) icon to learn about the keyboard shortcuts.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a37fd3d-Keyboard_Shortcuts_in_Journeys.gif",
        "",
        "Keyboard Shortcuts in Journeys"
      ],
      "align": "center",
      "border": true,
      "caption": "Keyboard Shortcuts in Journeys"
    }
  ]
}
[/block]


## Define the Journey Entry Criteria

Select the _Journey entry criteria_. It can be a specific time or an event trigger. 

When you start building your Journey, you must define your _entry criteria_. This is a condition that decides if the users will be included in the Journey. The entry criteria of a Journey is essentially the segment of users you want to target. For example, 

- Track new app installs to achieve the goal of customer registrations.
- Track the type of usage on the platform to achieve the goal of enticing customers to transact.
- Track non-usage of the platform through events like uninstalls/account deletion/frequent guest use to achieve the goal of pulling users back to the platform.

The various types of segments you can use are:

- **Live User segments**: These segments qualify people as soon as they meet your specified criteria
- **Past Behavior segments**: In this type of Entry Criteria, users who match your specified entry criteria will qualify once every twenty-four hours.

Live user segments are further classified as follows: 

- **Action**: In this type of _entry criteria_, users will enter your Journey, as soon as they perform an event. For example: Enter people into your Journey, as soon as they install your application.
- **Inaction**: Users enter your Journey, as soon as they don’t do something in the future. For example: If someone adds an item to their cart, but doesn’t transact within 15 mins.
- **Property Date-time segments**: Qualify a user relative to a specific date and time in a property.
- **Page visit**: Users will qualify as soon as they reach a web page that matches your specifications.
- **Refer entry**: When users come to your website from a certain referrer, for example, Facebook, or Twitter, they will be qualified for your Journey.
- **Page count**: As soon as the user sees the specified number of pages, they will be a part of your Journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ada99a2-Journeys_setup_entry_criteria.png",
        "Set entry criteria for Journeys",
        766
      ],
      "align": "center",
      "border": true,
      "caption": "Set Journey Entry Criteria"
    }
  ]
}
[/block]


## Define the Journey Entry Timelines

We support one-time, multiple dates, and recurring Journeys. For example, for monthly payment reminders, you can schedule a Journey to start on the 1st of every month

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de68ca2-Journeys_setup_entry_timelines.png",
        "Define entry timelines for Journey",
        726
      ],
      "align": "center",
      "border": true,
      "caption": "Define Journey Entry Timelines"
    }
  ]
}
[/block]


### One Time

This Journey type runs only for one time at the start time of the journey. The option to re-enter the journey is not available to the users who have exited the journey through journey timeout, force exit, or Goal completed.  
No new users will be added after the journey runs its course on the start time.

### Multiple Dates

This Journey type runs on the selected multiple dates. Select the journey end time as per the journey's need.  
The option to allow users to re-enter the journey may be selected.

### Recurring qualification

This Journey type runs repeatedly and allows entry to new users on the criteria selected in the Repeat section. The first run is immediate on publishing the Journey. The subsequent runs are basis the selected criteria.  
The option to allow users to re-enter the journey may be selected. For more information about entry timelines for a PBS Journey, refer to the following [FAQ](https://staging.docs.user.clevertap.net/docs/faqs#q-how-does-a-past-behavior-segment-journey-work). 

#### Allow Users to Re-Enter a Journey

By default, a user will qualify for a Journey only once. However, you can optionally allow users who have exited from a Journey to re-enter it, should they meet the entry criteria at a later date.

After a user is part of a Journey, they can only re-qualify if they exit the Journey, either by matching one of the specified goals or by being forced out of the Journey and subsequently meeting the specifications of the entry criteria.

 Following is an example:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3b04e68-Journeys_setup_reenter_user.png",
        "Re-entry of users in Journeys",
        698
      ],
      "align": "center",
      "border": true,
      "caption": "Re-entry of Users in Journeys"
    }
  ]
}
[/block]


When a user makes a purchase they enter into the Journey. After a 20-minute wait time, qualifying users will receive a Push Notification with a discount promotion code.

If the Journey was set up with the default behavior (users cannot re-enter the Journey), then after they purchase and receive the push notification, they exit from the Journey. If a user makes another purchase subsequent to the initial purchase, they will not receive another promotional Push Notification since this Journey does not allow for re-entry.

However, if your intent is to allow users to receive a new promotional discount after each subsequent purchase, you’d select the option to allow a user to re-enter as follows.

## DND and Timezone

CleverTap provides an option for configuring the _Do Not Disturb_ hours for notification delivery when creating a journey. The DND feature manages message delivery via engagement nodes in Journeys so that campaigns are only sent after the DND period or discarded. To configure DND for Push, SMS, Email & Web Push journeys, select the days and enter the time when you do not want to send campaign notifications. If you will use the same time inactive period for each day, click the **Apply to all **link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a0f920cded3c563fa8f58d40ed8942f9b2940606d900d8cf9814536ff9dffc94-image.png",
        null,
        "Configure DND and Timezone for Journeys"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure DND and Timezone for Journeys"
    }
  ]
}
[/block]


When sending a message during Do Not Disturb (DND) hours, you can select one of the following options:

- _Don't send a message_: Select this option to discard the message altogether. In this case, the message is not sent to the user, and the user moves ahead in the journey along the unreachable path. If the unreachable path is not defined or drawn, the user is stuck at the engagement node.
- _Send message after DND_: Select this option to send a message after DND.

  - _Scenario 1 (Before Feature Release)_  
    DND Period: Monday 11:00 PM to Tuesday 12:00 PM  
    User qualifies for the campaign: Tuesday 11:00 AM (During DND)  
    The engagement is delayed as it falls within the user's DND period. The user receives the engagement as soon as the DND period ends, at 12:00 PM on Tuesday.
  - _Scenario 2 (After Feature Release)_  
    DND Period: Monday 11:00 PM to Tuesday 12:00 PM  
    User qualifies for the campaign: Tuesday 11:00 AM (During DND)  
    The engagement is delayed as it falls within the user's DND period. The user receives the engagement on Wednesday at 11:00 AM, which is at the time scheduled. This ensures that notifications respect the user's active and inactive times and are only sent during their designated active hours.

  [block:image]{"images":[{"image":["https://files.readme.io/d3398f19a4d62d7f24eb243c245990941d506de273e89544302344919c7635ef-Send_Message_After_DND.png","","Send Message After DND"],"align":"center","border":true,"caption":"Send Message After DND"}]}[/block]

> ❗️ DND Conflict Hours
> 
> If you schedule a message node to send out delivery during the scheduled DND hours, you will receive an error message. This error message appears at the publishing of the journey.
> 
> [block:image]{"images":[{"image":["https://files.readme.io/7ff47d7-2020-08-17_16-14-20_DND_hours_Conflict.png","Set DND conflict hours for Journeys",1206],"align":"center","border":true,"caption":"DND Conflict Hours"}]}[/block]

## Define the Control Group

Define the required control groups. For more information on control groups, see [Control Groups](doc:control-groups). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7092b2a-Journeys_setup_control_group.png",
        "Define conflict group for Journeys",
        725
      ],
      "align": "center",
      "border": true,
      "caption": "Define Conflict Group"
    }
  ]
}
[/block]


## Select a Journey Timeout

Journeys are sequences of campaigns. At each stage of a Journey, you can choose to segment your audience further and deliver campaigns across multiple channels.

While creating Journeys, you can choose to specify a Journey Timeout, which will be the maximum time a user spends in a Journey. Users exit the journey once this window is complete for them, irrespective of the journey stage.

> 🚧 
> 
> Once a user has exited the Journey, the user is free to re-qualify, if you have allowed re-entry in your setup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e182621-Journeys_setup_timeout.png",
        "Set Journey timeout",
        724
      ],
      "align": "center",
      "border": true,
      "caption": "Journey Timeout"
    }
  ]
}
[/block]


## User Exit From a Journey

Assessing a Journey's effectiveness becomes challenging when a user gets stuck in a Journey. Hence, exiting users from the Journey is crucial in various scenarios.

Users exit the Journey based on four conditions:

- If the Journey goal is set:
  - User achieves the Journey goal.
  - User times out of the Journey.
  - User is forced to exit the Journey via the **Force Exit** node.
- If the Journey goal is not set:
  - User exits the Journey through the last engagement node.