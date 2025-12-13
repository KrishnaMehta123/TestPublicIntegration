---
title: Events Changelog
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
Welcome to the Events changelog document for CleverTap. This changelog provides insights about the system event updates in CleverTap, ensuring you use CleverTap effectively and monitor your metrics with greater accuracy.

We are dedicated to empowering businesses with advanced mobile marketing and analytics capabilities and delivering continuous improvements to meet our users' evolving needs. Stay tuned as we update this changelog regularly, informing our customers about any changes to existing system events or the introduction of new ones.

<br />

# February 2025

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "February 5th, 2025",
    "0-1": "Notification Delivered",
    "0-2": "-",
    "0-3": "Others",
    "0-4": "Now, this event is raised for Email campaigns, indicating the successful delivery to the end user. For more information, refer to [Email Campaign Stats](doc:email-campaign-stats-delivered).  \n  \n**Note**: Delivered is currently released in Private Beta. Contact your Customer Success Manager to enable this for email campaigns."
  },
  "cols": 5,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# October

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "October 11th, 2024",
    "0-1": "Notification Failed",
    "0-2": "",
    "0-3": "Others",
    "0-4": "Now, this event also captures the errors that occur in email campaigns. For more information, refer to [Events](doc:events).  \n  \n**Note**: This event is currently in Private Beta. Contact your account manager to enable this event."
  },
  "cols": 5,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# June

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "June 19th, 2024",
    "0-1": "Notification Failed",
    "0-2": "",
    "0-3": "Event Added",
    "0-4": "This event captures the errors that occurred in the campaign.  \n  \nThis event is currently in private beta and can be enabled upon request. Contact your account manager if you need access to this event.",
    "1-0": "",
    "1-1": "",
    "1-2": "Campaign ID",
    "1-3": "",
    "1-4": "The property helps identify the specific campaign associated with the error.",
    "2-0": "",
    "2-1": "",
    "2-2": "Campaign Type",
    "2-3": "",
    "2-4": "The property indicates the type of campaign (e.g., WhatsApp, SMS).",
    "3-0": "",
    "3-1": "",
    "3-2": "Error",
    "3-3": "",
    "3-4": "The property describes the title of the error observed in the campaign.",
    "4-0": "",
    "4-1": "",
    "4-2": "Label",
    "4-3": "",
    "4-4": "The property denotes the specific label associated with the error.",
    "5-0": "",
    "5-1": "",
    "5-2": "Variant",
    "5-3": "",
    "5-4": "The property helps identify the errors for a specific campaign variant in the case of A/B, split delivery, or multi-variant campaigns."
  },
  "cols": 5,
  "rows": 6,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# May

| Change Release Date | Event Name        | Property Name | Update Type      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :------------------ | :---------------- | :------------ | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| May 15, 2024        | Push Unregistered |               | Properties Added |                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|                     |                   | Source        |                  | <ul><li> **CT_Push**: Indicating that the event is raised via silent Push. In this case, FCM returns a [404 Unregistered error]() for stale tokens from devices that have not connected to FCM for 270 days or for users who have uninstalled the app. </li> <li> **CT_SDK**: Indicating that the event is raised via OnUserLogin() method.</li> <li> **CT_Target**: Indicating that the event is raised via campaigns or journeys. </li></ul> |
|                     |                   | Token Value   |                  | The property contains the actual value of the token.                                                                                                                                                                                                                                                                                                                                                                                           |
|                     |                   | Token Type    |                  | <ul><li> FCM </li> <li> Baidu </li> <li> Huawei </li></ul>                                                                                                                                                                                                                                                                                                                                                                                     |
|                     |                   | targetId      |                  | The property denotes the ID of the campaign or journey.                                                                                                                                                                                                                                                                                                                                                                                        |

# April

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "April 2, 2024",
    "0-1": "Notification Clicked",
    "0-2": "",
    "0-3": "Property Added",
    "0-4": "",
    "1-0": "",
    "1-1": "",
    "1-2": "button_id",
    "1-3": "",
    "1-4": "The property is visible for the event if the _Notification Clicked_ event is tracked for button clicks associated with the new Image Interstitial template. Therefore, the customers adopting this template will see this new property.  \n  \nFor more information, refer to [In-App Image Interstitial Template](doc:in-app-editor#image-interstitial)."
  },
  "cols": 5,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]