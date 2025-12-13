---
title: Amplitude Import (Cohort)
excerpt: Understand how to import cohorts from Amplitude to CleverTap.
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

[Amplitude](https://amplitude.com/), an analytics and business intelligence platform, helps make informed decisions for targeting users. This integration allows you to import cohorts (segments) from Amplitude into CleverTap and provides different benefits described in the below section.

# Key Benefits

Here are some of the key benefits of this integration:

- **Enhanced Cohort Management**: Leverage Amplitude's product analytics to create targeted cohorts (segments) in CleverTap for personalized messaging and engagement campaigns based on user behaviors and preferences captured in Amplitude.
- **Comprehensive Event Tracking**: Capture and analyze user interactions within CleverTap, such as app installs, uninstallations, push notifications, and in-app messages, in Amplitude for a holistic view of user engagement across both platforms.
- **Data-Driven Decision Making**: Make informed decisions and optimize your customer engagement strategies by leveraging the combined insights from CleverTap and Amplitude's powerful analytics engines.
- **Personalized and Relevant Campaigns**: Deliver contextual and personalized messaging to your users based on their behaviors and preferences captured in Amplitude, leading to higher engagement and conversion rates.
- **Streamlined Workflow**: Seamlessly push cohorts (segments) and system events between CleverTap and Amplitude with a simple and intuitive setup, saving you time and effort in managing your marketing campaigns.

# Prerequisites

Before you begin the integration, ensure that you have:

- Correctly map the Amplitude Cohorts (segments) to CleverTap Segments
- The required permission to create cohorts (segments) in the Amplitude account

# Set Up

This procedure involves the following four major steps:

1. [Map User Identities for Amplitude Cohorts to CleverTap Segments](doc:amplitude-cohort-import#map-user-identities-for-amplitude-cohorts-to-clevertap-segments)
2. [Find CleverTap Project Details](doc:amplitude-cohort-import#find-clevertap-project-details)
3. [Configure CleverTap as a Destination in Amplitude](doc:amplitude-cohort-import#configure-clevertap-integration-in-amplitude)
4. [Import Cohorts from Amplitude](doc:amplitude-cohort-import#import-cohorts-from-amplitude)

## Map User Identities for Amplitude Cohorts to CleverTap Segments

Amplitude exports all users to CleverTap, including anonymous users. A common identifier is used to match users when syncing cohorts (segments) from Amplitude to CleverTap. The following are the key points to remember when setting up an identifier on the Amplitude dashboard:

- Amplitude captures `User ID` and `Device ID` as an identifier for every profile. The `User ID` is for identified profiles, whereas the `Device ID` is for every profile.
- CleverTap allows `identity`, `email` or `phone` as an identifier for the users. It captures `Device ID` as the CleverTap ID (Object ID) for every profile.

For more information about how users are identified, refer to the following section.

### User Identity Management

The CleverTap User ID is a unique identifier assigned to the user in Amplitude. This identifier enables the mapping of user data between CleverTap and Amplitude, allowing for a more comprehensive understanding of user behavior and engagement across different channels. When importing cohorts (segments) from Amplitude, the user identity is matched in the following manner:

- If the CleverTap User ID is present in Amplitude, it is matched with the identity value of all the users present in CleverTap. If a match is found, the profile becomes part of the segment.
- If the CleverTap User ID is not present in Amplitude, the Device Id (Anonymous Id) value is used as CleverTap ID, and a new profile is created in CleverTap. This new profile becomes part of the segment.

To understand this better, refer to the following diagram:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2299ef2-Amplitude_User_Identity_Mapping.png",
        null,
        "User Identity Mapping When Importing Cohorts (segments) to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "User Identity Mapping When Importing Cohorts (segments) to CleverTap"
    }
  ]
}
[/block]

To understand how users are identified in different scenarios, read the following information:

**Scenario 1: When a user's identity is the same in both Amplitude and CleverTap**

Consider a scenario where user A is assigned the CleverTap User ID `Clevertap1` in Amplitude, and the same user's identity is set as `clevertap1` in CleverTap.

In this scenario, CleverTap raises a _Partner Sync_ event for the user in CleverTap and includes the user in the segment (cohort).

**Scenario 2: When a user's identity is different in Amplitude and CleverTap**

Consider a scenario where user A is assigned the CleverTap User ID `CleverTap1` in Amplitude, and the same user is identified with a different user identity in CleverTap, which is `CleverTap2`.

In this case, the CleverTap creates a new profile for the same user with a new identity as `CleverTap1` and raises a _Partner Sync_ event to include the new profile in the segment (cohort).

To avoid this scenario, CleverTap recommends you push the _CleverTap_Identity_ as the identity in Amplitude and use this identity when setting up CleverTap as a cohort (segment) destination. For more information, refer to [Set Up Common User Identifier](doc:amplitude-cohort-import#set-up-common-user-identifier-between-clevertap-and-amplitude).

**Scenario 3: When User A with Device ID is not identified in Amplitude**

Consider a scenario where a user with Device ID `543C-3455-4555-3SRD` is not identified in Amplitude. In this scenario, CleverTap captures this Device ID (`543C-3455-4555-3SRD`) as CleverTap ID (Object ID) and creates a new profile. After the new profile is created, CleverTap raises a _Partner Sync_ event for this profile and includes the user in the segment (cohort).

### Set Up Common User Identifier between CleverTap and Amplitude

When a user's identity differs between Amplitude and CleverTap, the common user identifier must be set up to identify and include the user in the cohort (segment). The following are two different ways of setting up a common identifier between the two platforms:

#### Using Amplitude APIs

The value that is passed in `CleverTap_Identity` must be the same as that passed as identity in CleverTap.

```curl
curl --location --request POST 'https://api2.amplitude.com/identify' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'api_key=a0ccac7656a6e187b597f44476dd031e' \
--data-urlencode 'identification=[{"user_id":"amplitude_id", "user_properties":{"CleverTap_Identity":"integrations@clevertap.com"}}]'

```

> 📘 Set Up Identity
> 
> You must replace the value of `CleverTap_Identity` with the user identity value set in CleverTap for the profile. For example, `integrations@clevertap.com` is the identity set in CleverTap, so we must pass that value to Amplitude. If the value of the identity was `12345`, we must pass the value as `12345`.

#### Using Amplitude SDKs

The value that is passed in `CleverTap_user_Id` must be the same as that passed in CleverTap.

```java
val identify = Identify()  
identify.set("CleverTap_Identity", "integrations@clevertap.com")  
amplitude.identify(identify)
```
```objectivec
AMPIdentify *identify = [[[AMPIdentify identify] set:@"CleverTap_Identity" value:@"[integrations@clevertap.com]]];  
[[Amplitude instance] identify:identify];
```
```swift
let identify = AMPIdentify()  
.set("CleverTap_Identity", value: "integrations@clevertap.com")  
Amplitude.instance().identify(identify)
```

## Find CleverTap Project Details

Find the following project details to authorize the CleverTap integration in the Amplitude dashboard:

- [Project ID](https://docs.clevertap.com/docs/amplitude-cohort-import#project-id)
- [Passcode](https://docs.clevertap.com/docs/amplitude-cohort-import#passcode)
- [Region](https://docs.clevertap.com/docs/amplitude-cohort-import#region)

> 📘 Project Details
> 
> CleverTap suggests keeping the above details handy, as you will need them to configure the Amplitude dashboard.

### Project ID

The Project ID can be obtained by navigating to the _Settings_ > _Project_ page of the CleverTap dashboard (see figure below):

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ca0240-Project_Details.png",
        null,
        "CleverTap Project Details"
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap Project Details"
    }
  ]
}
[/block]

### Passcode

To find the passcode for your Amplitude Import project, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

> 📘 Account Passcode
> 
> When generating account passcode, we recommend you set the expiry date for passcode as _Forever_.

### Region

 To identify the region for your account, refer to the following table:

| Region                  | API Endpoint           | CleverTap Dashboard URL                                                                                                                              |
| :---------------------- | :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| Europe (Default region) | api.clevertap.com      | <https://eu1.dashboard.clevertap.com/login.html>                                                                                                     |
| India                   | in1.api.clevertap.com  | <https://in1.dashboard.clevertap.com/login.html>                                                                                                     |
| Indonesia               | aps3.api.clevertap.com | [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html)) |
| Middle East (UAE)       | mec1.api.clevertap.com | <https://mec1.dashboard.clevertap.com/login.html>                                                                                                    |
| Singapore               | sg1.api.clevertap.com  | <https://sg1.dashboard.clevertap.com/login.html>                                                                                                     |
| South Korea             | sk1.api.clevertap.com  | <https://sk1.dashboard.clevertap.com/login.html>                                                                                                     |
| United States (USA)     | us1.api.clevertap.com  | <https://us1.dashboard.clevertap.com/login.html>                                                                                                     |

## Configure CleverTap as a Destination in Amplitude

To configure the Amplitude dashboard:

1. Navigate to _Destinations_ from the Amplitude dashboard and click **+ Add Destination**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4c7c17b-small-Add_Destination_Amplitude.png",
        "Click Add Destination",
        "Destinations in Amplitude Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Destinations in Amplitude Dashboard"
    }
  ]
}
[/block]

2. Click **CleverTap** from the _MESSAGING DESTINATIONS_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/83ea665-small-CleverTap_Destination_Amplitude.png",
        "Click CleverTap from Messaging Destinations",
        "Messaging Destinations in Amplitude"
      ],
      "align": "center",
      "border": true,
      "caption": "Messaging Destinations in Amplitude"
    }
  ]
}
[/block]

3. Enter the following details in the _Connect to CleverTap_ form:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/05dec70-small-Connect_to_CleverTap_Amplitude_Import.png",
        null,
        "Add Destination Details to Connect CleverTap"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Add Destination Details to Connect CleverTap"
    }
  ]
}
[/block]

| Field                     | Description                                                                                                                                                                                                                                         |
| :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                      | Enter the name to uniquely identify the integration.                                                                                                                                                                                                |
| CleverTap Region          | Select the [Region](https://docs.clevertap.com/docs/amplitude-cohort-import#region) of your CleverTap account from the dropdown.                                                                                                                    |
| Account ID                | Enter the [Project ID](https://docs.clevertap.com/docs/amplitude-cohort-import#project-id) of your CleverTap account.                                                                                                                               |
| Account Passcode          | Enter the [Passcode](https://docs.clevertap.com/docs/amplitude-cohort-import#passcode) of your CleverTap account.                                                                                                                                   |
| Anonymous ID Mapping      | Select _Device ID_ as an identity to map anonymous users in CleverTap. For more information, refer to [Map User Identity](https://docs.clevertap.com/docs/amplitude-cohort-import#map-user-identities-for-amplitude-cohorts-to-clevertap-segments). |
| CleverTap User ID Mapping | Select _identity_ to map the identified users in CleverTap User ID. For more information, refer to [Map User Identity](https://docs.clevertap.com/docs/amplitude-cohort-import#map-user-identities-for-amplitude-cohorts-to-clevertap-segments).    |

4. Click **Save**. CleverTap is now displayed on the _Destinations_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f09006b-small-Destination_CleverTap_Amplitude.png",
        "Click Save and View CleverTap as a Destination in Amplitude",
        "Add CleverTap as a Destination in Amplitude"
      ],
      "align": "center",
      "border": true,
      "caption": "Add CleverTap as a Destination in Amplitude"
    }
  ]
}
[/block]

## Import Cohorts from Amplitude

> 📘 Verify User Identifications
> 
> To ensure that the user profiles imported from Amplitude are correctly identified in CleverTap, we recommend importing a smaller cohort (segment) before proceeding with larger cohorts.

To import the cohorts (segments) from Amplitude to CleverTap:

1. Navigate to _Cohorts_ from the Amplitude dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6684986-small-Cohorts_Amplitude_Import.png",
        null,
        "Cohorts Page in Amplitude Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Cohorts Page in Amplitude Dashboard"
    }
  ]
}
[/block]

2. Select the cohort (segment) you want to import and click **Sync**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b68cfef-small-Cohort_Definition_Amplitude_Import.png",
        null,
        "Sync a Cohort (segment) from Amplitude Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync a Cohort (segment) from Amplitude Dashboard"
    }
  ]
}
[/block]

3. Select the destination as _CleverTap_ and click **Next**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a9e9a8c-small-Select_Destination_Amplitude.png",
        "Select CleverTap as a Destination and Click Next",
        "Select CleverTap as a Destination for Sync"
      ],
      "align": "center",
      "border": true,
      "caption": "Select CleverTap as a Destination for Sync"
    }
  ]
}
[/block]

4. Select the API target to sync to your CleverTap project and click **Next**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98d3af4-small-API_Target_Amplitude.png",
        "Select API Target and Click Next",
        "Select API Target as CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Select API Target as CleverTap"
    }
  ]
}
[/block]

5. Select one of the sync types and click **Sync**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ad3d20-small-Define_Cadence_Amplitude.png",
        "Select Scheduled Sync and Click Sync",
        "Define the Cadence for Cohort Sync from Amplitude"
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Cadence for Cohort Sync from Amplitude"
    }
  ]
}
[/block]

- **One-time Sync**: In the case of one-time sync, Amplitude sends a one-time list of users who are currently part of the cohort to CleverTap.
- **Scheduled Sync**: In the case of scheduled sync, Amplitude initiates sync between a cohort and CleverTap on an hourly or daily basis. The imported segment is updated as per the chosen sync type to reflect the most recent list of users in the segment.
- **Real-Time**: In the case of real-time sync, Amplitude sends a list of users in the cohort every minute to CleverTap. The real-time sync feature is available on request. To avail of this feature, contact your Amplitude team to enable it for your account.

> 📘 Amplitude Cohort Sync
> 
> Every cohort sync from Amplitude includes only the users added or removed from the cohort after the last sync.

# View Amplitude Cohorts in CleverTap

The cohort name defined in the Amplitude dashboard appears as the segment under the _Segments_ list page of the CleverTap dashboard. The _Type_ column under the _Segments_ list page for the exported cohort is displayed as _Partner - Amplitude_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/42f595b-small-Segments_List_Amplitude_Import.png",
        null,
        "View Synced Cohort in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "View Synced Cohort in CleverTap"
    }
  ]
}
[/block]

Click the segment to view the statistics for this segment, like any other segment on the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ac966d-small-View_Segments_Amplitude_Import.png",
        null,
        "View Segment Details"
      ],
      "align": "center",
      "border": true,
      "caption": "View Segment Details"
    }
  ]
}
[/block]

You can also validate a user profile ingested from Amplitude using the Partner Sync event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f323e91-small-User_Profile_Amplitude_Import.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

# Engage with Amplitude Cohort on CleverTap

You can also engage with the cohorts (segments) imported from Amplitude by creating different campaigns and journeys. The process of creating campaigns for the Past Behavior Segment and Live Behavior Segment is the same except for where we need to select the segment.

## For Past Behavior Campaigns/Journeys

To select the segment:

1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.
4. Click **Who** and filter the target audience by selecting _With user properties_ > _Segments_.
5. Select the imported user segment from the available list of segments.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e94d4dc-small-With_User_Properties_Past_Behavior.png",
        null,
        "Select the Imported Segment for Past Behavior Campaigns/Journeys"
      ],
      "align": "center",
      "border": true,
      "caption": "Select the Imported Segment for Past Behavior Campaigns/Journeys"
    }
  ]
}
[/block]

**Scenario: Customer wants to send an In-App Message campaign to the user from Bangalore city when they launch the mobile application.** 

In this case, the customer will create a cohort (segment) in the Amplitude dashboard and initiate a one-time export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create an In-App campaign for this cohort of users. 

To create the campaign, the customer will navigate to In-App Campaign and select the segment under the **Who** segment section in the following way:

1. Select **App Launched **event under _As soon as the user does_ section.
2. Select _Filter on past behavior and user properties_ checkbox.
3. Select _With user properties_ > _Segments_ and then select the segment name from the list.

## For Live Campaigns/Journeys

To select the segment:

1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.
4. Click **Who** and then select _Partner Sync_ event from the list.
5. Click _Filter_ and then select _Event Property Action_ = Added.

> 📘 Partner Sync Event
> 
> The _Partner Sync_ event is raised every time CleverTap receives a cohort sync request from Amplitude.

6. Filter the target audience by selecting **Segments** under _With User Properties_.
7. Select the imported user segment from the available list of segments.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6cdf46e-small-With_User_Properties_Live_Behavior.png",
        null,
        "Select the Imported Segment for Live Campaign/Journeys "
      ],
      "align": "center",
      "border": true,
      "caption": "Select the Imported Segment for Live Campaign/Journeys "
    }
  ]
}
[/block]

**Scenario: Customer wants to send a recurring Email campaign to the users that added an item to the cart but did not purchase the item.**  
In this case, the customer will create a cohort (segment) in the Amplitude dashboard and initiate a recurring export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create a recurring Email campaign for this cohort of users. To create the campaign, the customer will navigate to Email Campaign and create the campaign in the following way:

1. Select _Start here_ > _Live Behavior_.
2. Select **Partner Sync** event under the _As soon as the user does_ section.
3. Click _Filter_ and then select Event Property _Action_ = _Added_.
4. Select _Filter on past behavior and user properties_ checkbox.
5. Select _Segments_ under _With user properties_ and then select the segment name from the list.

## Find Amplitude Cohort from CleverTap Dashboard

To find the Amplitude cohort:

1. Navigate to Segments > Find People from the CleverTap dashboard.
2. Select the **Partner Sync** event from the _Users who did_ section.
3. Select _Segments_ under _Display common properties such as_ and select the segment name from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37604c0-small-Find_People_Amplitude_Import.png",
        null,
        "View the Imported Cohort from Find People"
      ],
      "align": "center",
      "border": true,
      "caption": "View the Imported Cohort from Find People"
    }
  ]
}
[/block]

# Partner Sync Event

The _Partner Sync_ event is raised for all the users who are part of different partner segments. The following table provides information about the event properties:

| <p>Property Name</p>        | <p>Description</p>                                                                                  | <p>Property Value/Example</p>           |
| :-------------------------- | :-------------------------------------------------------------------------------------------------- | :-------------------------------------- |
| <p>Partner Segment Name</p> | <p>Indicates the name of the cohort (segment) exported from Amplitude.</p>                          | <p>For example, Cart Drop off</p>       |
| <p>Action</p>               | <p>Indicates if the user has been added or removed from the segment in the CleverTap dashboard.</p> | <ul><li>Added</li><li>Removed</li></ul> |
| Partner Segment ID          | Indicates the Cohort ID in the Amplitude dashboard                                                  | For example, 1638361188                 |
| CT Source                   | Indicates the source of the event.                                                                  | Amplitude                               |
| Partner Name                | Indicates the name of the partner from where the segment was imported.                              | Amplitude                               |

> 📘 Campaign Exceptions for Partner Sync Event
> 
> The _Partner Sync_ event cannot be used as a trigger event to create the campaigns for the following channels as it is not an SDK event:
> 
> - In-App Messages
> - Web Popup
> - Web Exit Intent
> - App Inbox
> - Native Display

> 📘 Contribution Towards Billing
> 
> The _Partner Sync_ event contributes to data points for _MAU Billing Type_ and as an event for _Container Billing Type_.

# FAQs

### Q. Can I export the CleverTap engagement data to Amplitude for analysis?

A. Yes. For more information, refer to [Amplitude Export](https://docs.clevertap.com/docs/amplitude-export).