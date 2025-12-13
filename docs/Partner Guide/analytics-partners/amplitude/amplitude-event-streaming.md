---
title: Amplitude Event Streaming
excerpt: Learn how to ingest event data from Amplitude into CleverTap.
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

[Amplitude](https://amplitude.com/) is an analytics and business intelligence platform that helps make informed decisions for targeting users. This integration allows you to import events from Amplitude into CleverTap to enhance engagement.

# Key Benefits

Event Streaming from Amplitude to CleverTap provides the following advantages: 

- **Seamless Integration**: Allows you to easily integrate in just a few steps. Once the integration is complete, data flows seamlessly from Amplitude to CleverTap in near real-time.
- **Real-Time Insights**: Allows you to access real-time insights into user behavior. This includes tracking the pages users visit, the features they engage with, and how they interact with the app. 
- **Personalized Experiences**: Allows you to craft personalized user experiences that are relevant and engaging. For example, you can send information about a user's location or language preference and use this data to tailor their messaging or content to specific needs.
- **Conversion Tracking**: Allows you to effectively measure the performance of the marketing campaigns and track user behavior throughout the funnel. For example, you can track the number of users who, after receiving a specific message from CleverTap, went on to make a purchase or complete another desired action.

# Keys Points to Remember

Remember the following when you send events to CleverTap:

- Relevant limits for CleverTap events are:
  - CleverTap does not impose any hard limits on quantity or velocity; however, requests sent too quickly return 429 responses. Amplitude handles these automatically.
  - The requests must be smaller than 2MB.
- Amplitude sends selected event properties and user properties with the event.

# Prerequisites

- Ensure you enable this integration for every Amplitude project where you intend to utilize it.
- Ensure you have the CleverTap account. 

# Configure Amplitude for Event Streaming

To configure the Amplitude dashboard for Event Streaming:

1. In **Amplitude**, go to _Data_ > _Connections_ > _Catalog_.
2. Go to _Destinations_ > Event_ Streaming_ and select **CleverTap**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84bc381-SeelctCleverTap.jpg",
        "",
        "Select Event Streaming "
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Select Event Streaming "
    }
  ]
}
[/block]


3. Enter a name in the _Sync Name_ field and click **Create Sync**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/477ae11-CreateSync.jpg",
        "",
        "Enter a Sync Name"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Enter a Sync Name"
    }
  ]
}
[/block]


   The _Destination Settings_ section appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22e4427-SettingsPage.jpg",
        "",
        "Destination Settings"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Destination Settings"
    }
  ]
}
[/block]


4. Enable the **Status** toggle.
5. Enter the CleverTap project details. You can get the details by navigating to _Settings_ > _Project_ from the dashboard: 
   - **[CleverTap Account Id](doc:amplitude-cohort-import#project-id)**: Copy and paste the _Project ID_ from the CleverTap dashboard. 
   - **[CleverTap Passcode](doc:amplitude-cohort-import#passcode)**: Copy and paste the _Passcode_ from the CleverTap dashboard.
   - **[Region](doc:amplitude-cohort-import#region)**: Enter one of the following regions: aps3, eu1, in1, sg1, mec1, or us1. 
6. Under **Mappings**, from the **Amplitude Property** dropdown list, select an Amplitude user property that corresponds to your CleverTap identity.
7. Under **Send Events**, enable the **Events are sent to CleverTap** toggle. It allows you to stream events from Amplitude to CleverTap. It automatically forwards events to CleverTap when ingested in Amplitude. Events are not sent on a schedule or on demand using this integration.
8. In **Select and filter events**, choose only the events you want to send to CleverTap. CleverTap does not support [Transformed events](https://help.amplitude.com/hc/en-us/articles/5913315221915-Transformations-Retroactively-modify-your-event-data-structure#:~:text=Amplitude%20Data%27s%20transformations%20feature%20allows,them%20to%20all%20historical%20data.). 
9. (Optional) Under **Send Users**, enable the **User updates are not sent to CleverTap** toggle to send over users and their properties in real-time whenever a user is created, or the user property is updated in Amplitude.
10. Click **Save**.

# View Amplitude Events on the CleverTap Dashboard

Once the Amplitude events are streamed into CleverTap, they can be viewed on the CleverTap dashboard. 

To view the Amplitude events on the CleverTap dashboard: 

1. Go to _Analytics_ > _Events_. 
2. Under the _System Events_ drop-down, select the desired event. For example, _Signup_. 
3. Click **+Filter by**.  
   The _CT Source_ property value distinguishes events arriving from various sources into CleverTap. In this example, the CT Source value is set to _Amplitude_ for the _Signup_ event. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b77e1a9-PartnerSync.jpg",
        "",
        "Filter Amplitude Events on CleverTap Dashboard"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Filter Amplitude Events on CleverTap Dashboard"
    }
  ]
}
[/block]


5. Click **View details**.

> 📘 Supported Messaging Channels
> 
> Amplitude events cannot be used in the following messaging channels:
> 
> - In-App Messages
> - Web Popup
> - Web Exit Intent
> - App Inbox
> - Native Display