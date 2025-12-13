---
title: mParticle Import (Audience)
excerpt: Understand how to import audience (segment) from mParticle to CleverTap.
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

[mParticle](https://www.mparticle.com/), a customer data platform that helps make informed decisions for targeting users. This integration allows you to import audience (segment) from mParticle into CleverTap and provides different benefits described in the below section.

# Key Benefits

Here are some of the key benefits of this integration:

- **Enhanced Audience Management**: Leverage mParticle's product analytics to create a targeted audience (segments) in CleverTap for personalized messaging and engagement campaigns based on user behaviors and preferences captured in mParticle.
- **Comprehensive Event Tracking**: Capture and analyze user interactions within CleverTap, such as app installs, uninstallations, push notifications, and In-App messages, in mParticle for a holistic view of user engagement across both platforms.
- **Data-Driven Decision Making**: Make informed decisions and optimize your customer engagement strategies by leveraging the combined insights from CleverTap and mParticle's powerful analytics engines.
- **Personalized and Relevant Campaigns**: Deliver contextual and personalized messaging to your users based on their behaviors and preferences captured in mParticle, leading to higher engagement and conversion rates.
- **Streamlined Workflow**: Seamlessly push audience (segments) and system events between CleverTap and mParticle with a simple and intuitive setup, saving you time and effort in managing your marketing campaigns.

# Prerequisites to Integration

Before you begin the integration, ensure that you have the following:

- The required permission to create an audience (segments) in the mParticle account.
- The mParticle Audience (segments) mapped correctly to CleverTap Segments.

# Setup

This procedure involves the following three major steps:

1. [Find CleverTap Project Details](doc:mparticle-import-audience#find-clevertap-project-details)
2. [Configure CleverTap as an Audience Output in mParticle](doc:mparticle-import-audience#configure-clevertap-as-an-audience-output-in-mparticle)
3. [Import Audience from mParticle](doc:mparticle-import-audience#import-audience-from-mparticle)
4. [Map User Identities of mParticle Audience to CleverTap Segments](doc:map-user-identities-of-mparticle-audience-to-cleverTap-segments)

## Find CleverTap Project Details

Find the following project details to authorize the CleverTap integration on the mParticle dashboard:

- Project ID
- Passcode
- Project Token
- Region

> 📘 Passcode
> 
> When generating an account passcode, we recommend you set the expiry date for the passcode as _Forever_. To find the passcode for your mParticle Import project, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#account-level-passcode).

You can obtain the remaining project details by navigating to the _Settings_ > _Project_ page of the CleverTap dashboard (see figure below):

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

> 📘 Project Details
> 
> CleverTap suggests keeping the above details handy, as you will need them to configure the mParticle dashboard.

To identify the region for your account, refer to the following table:

| Region | CleverTap Dashboard URL                           |
| :----- | :------------------------------------------------ |
| eu1    | <https://eu1.dashboard.clevertap.com/login.html>  |
| in1    | <https://in1.dashboard.clevertap.com/login.html>  |
| aps3   | <https://aps3.dashbaord.clevertap.com/login.html> |
| mec1   | <https://mec1.dashboard.clevertap.com/login.html> |
| sg1    | <https://sg1.dashboard.clevertap.com/login.html>  |
| us1    | <https://us1.dashboard.clevertap.com/login.html>  |

## Configure CleverTap as an Audience Output in mParticle

To configure CleverTap on the mParticle dashboard:

1. Navigate to _Setup_ > _Output_ from the mParticle dashboard.
2. Select the _Audience_ tab, click **Add Audience Output**, and select _CleverTap_ from the dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c980230-Audience_Output_mParticle_Import.png",
        null,
        "Select CleverTap for Audience Output on mParticle Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Select CleverTap for Audience Output on mParticle Dashboard"
    }
  ]
}
[/block]

The _Audience Configuration_ popup opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ba04304-Audience_Configuration_Form_mParticle.png",
        null,
        "Add Audience Configuration Details"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Add Audience Configuration Details"
    }
  ]
}
[/block]

3. Enter the following details and click **Save** to save the details:

| Field              | Description                                                                                                        |
| :----------------- | :----------------------------------------------------------------------------------------------------------------- |
| Configuration Name | Enter the name to identify your configuration uniquely.                                                            |
| Account ID         | Enter the [Project ID](doc:mparticle-import-audience#find-clevertap-project-details) of your CleverTap account.    |
| Passcode           | Enter the [Passcode](doc:mparticle-import-audience#find-clevertap-project-details) of your CleverTap account.      |
| Account Token      | Enter the [Project Token](doc:mparticle-import-audience#find-clevertap-project-details) of your CleverTap account. |
| Region             | Enter the [Region](doc:mparticle-import-audience#find-clevertap-project-details) of your CleverTap account.        |

After configuring the output, it displays under the _CleverTap Default_ of the _Outputs_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d97571-CleverTap_mParticle_Audience_Output.png",
        null,
        "Add CleverTap Event on mParticle Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Add CleverTap Event on mParticle Dashboard"
    }
  ]
}
[/block]

## Import Audience from mParticle

To import Audience from mParticle to CleverTap output destination:

1. Navigate to _Audience_ from the mParticle dashboard and open the audience you want to connect to the output.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f43d25f-Connect_Audience_Output.png",
        null,
        "mParticle Audience Page"
      ],
      "align": "center",
      "border": true,
      "caption": "mParticle Audience Page"
    }
  ]
}
[/block]

2. From the _Connect_ tab, click **Connect Output**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4b101e9-Connect_Audience_mParticle.png",
        null,
        "Connect mParticle Audience"
      ],
      "align": "center",
      "border": true,
      "caption": "Connect mParticle Audience"
    }
  ]
}
[/block]

3. Select the configuration you want to set as an _Output_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1929b8a-Connect_Output_Configuration.png",
        null,
        "Connect Output Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Connect Output Destination"
    }
  ]
}
[/block]

4. Select the _User ID_ that you want to set up for mapping the mParticle audience on the CleverTap dashboard. For more information, refer to [User Identity Management](doc:mparticle-import-audience#user-identity-management).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4ee1e0-Connect_Output_Gif.gif",
        null,
        "Select Output and Add the Connection"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Output and Add the Connection"
    }
  ]
}
[/block]

> 📘 Verify User Identifications
> 
> To ensure that the user profiles imported from mParticle are correctly identified in CleverTap, we recommend importing a smaller audience (segment) before proceeding with larger audiences.

## Map User Identities of mParticle Audience to CleverTap Segments

CleverTap imports all users from mParticle except the **anonymous users**. During the import process, CleverTap compares the identifiers set by mParticle for its existing user profiles and maps the relevant user identifiers to CleverTap's user profiles. This ensures that user actions, attributes, and event data associated with a specific user in mParticle are accurately attributed to the corresponding user in CleverTap. To achieve this, a common identifier is used to map users when importing audience (segments) from mParticle to CleverTap.

CleverTap uses the following identities to map the imported audience (segments) from mParticle:

- **Partner ID:** A unique identifier assigned to every user profile whenever the data is exported from CleverTap to mParticle. This value is available on the mParticle dashboard as `CleverTap_User_ID` in the Partner ID field.
- **Customer ID:** A unique identifier generated by mParticle to individual users within the mParticle ecosystem.
- **mParticle ID:** A persistent, anonymized identifier assigned to each user in the mParticle system.
- **Email:** The email address associated with a user.
- **Phone Number:** The phone number associated with a user.

For more information about mParticle Identity Management, refer to [Identify Users](https://docs.mparticle.com/guides/idsync/identify-users/).

### User Identity Management

When importing audience (segments) from mParticle, the user identity is managed in the following manner:

- If the **Partner ID is present in an imported audience from mParticle**, it is mapped with the CleverTap ID value in CleverTap. In that case, the Email and Phone Number of the profile are merged with the same profile in CleverTap, and the profile becomes part of the CleverTap segment.
- If the **Partner ID is not present** in an imported audience from mParticle, the **Customer ID value from mParticle is used as an identifier** and mapped with the Identity value in CleverTap. In that case, the Email and Phone Number of the profile are merged with the same profile in CleverTap, and the profile becomes part of the CleverTap segment.
- If the **Customer ID is also not present** in an imported audience from mParticle, the **mParticle ID value is used as an identifier** and mapped with the Identity value in CleverTap. In that case, the Email and Phone Number of the profile are merged with the same profile in CleverTap, and the profile becomes part of the CleverTap segment.
- If **only mParticle ID is present** and the rest of the details are not present in the imported audience, then the **profile is considered anonymous** and does not become part of the CleverTap dashboard.

To understand this better, refer to the following diagram:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e644462-Identity_Management_mParticle.png",
        null,
        "User Identity Management between mParticle and CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "User Identity Management between mParticle and CleverTap"
    }
  ]
}
[/block]

# View mParticle Audience in CleverTap

The audience name defined in the mParticle dashboard appears as the segment under the _Segments_ list page of the CleverTap dashboard. The _Type_ column under the _Segments_ list page is displayed as _Partner - mParticle_ for the exported audience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc97e63-View_Imported_Audience_on_CleverTap.png",
        null,
        "View Synced Audience in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "View Synced Audience in CleverTap"
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
        "https://files.readme.io/7795346-View_Segment_Stats.png",
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

You can also validate if the user profile is ingested from mParticle by verifying if the _Partner Sync_ event is listed under the _User activity details_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dfe3a48-Partner_Sync_mParticle_Import.png",
        null,
        "View Partner Sync Event in CleverTap User Profile"
      ],
      "align": "center",
      "border": true,
      "caption": "View Partner Sync Event in CleverTap User Profile"
    }
  ]
}
[/block]

# Engage with mParticle Audience on CleverTap

You can also engage with the audience (segments) imported from mParticle by creating different campaigns and journeys. Creating campaigns for the Past Behavior Segment and Live Behavior Segment is the same except where we need to select the segment.

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
        "https://files.readme.io/e8daa93-View_mParticle_Audience_in_Past_Behavior_Campaigns.png",
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

In this case, the customer will create an audience (segment) in the mParticle dashboard and initiate a one-time export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create an In-App campaign for this audience of users. 

To create the campaign, the customer will navigate to In-App Campaign and select the segment under the **Who** segment section in the following way:

1. Select **App Launched** event under _As soon as the user does_ section.
2. Select _Filter on past behavior and user properties_ checkbox.
3. Select _With user properties_ > _Segments_ and select the segment name from the list.

## For Live Campaigns/Journeys

To select the segment:

1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.
4. Click **Who** and select _Partner Sync_ event from the list.
5. Click _Filter_ and then select _Event Property Action_ = Added.

> 📘 Partner Sync Event
> 
> The _Partner Sync_ event is raised every time CleverTap receives an audience sync request from mParticle.

6. Filter the target audience by selecting **Segments** under _With User Properties_.
7. Select the imported user segment from the available list of segments.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fe4c99-View_Audience_in_Live_Behavior_Campaign.png",
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

**Scenario: Customer wants to send a recurring Email campaign to the users who added an item to the cart but did not purchase the item.**  
In this case, the customer will create an audience (segment) in the mParticle dashboard and initiate a recurring export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create a recurring Email campaign for this audience of users. To create the campaign, the customer will navigate to Email Campaign and create the campaign in the following way:

1. Select _Start here_ > _Live Behavior_.
2. Select the **Partner Sync** event under the _As soon as the user does_ section.
3. Click _Filter_ and then select Event Property _Action_ = _Added_.
4. Select _Filter on past behavior and user properties_ checkbox.
5. Select _Segments_ under _With user properties_ and select the segment name from the list.

## Find mParticle Audience from CleverTap Dashboard

To find the mParticle audience:

1. Navigate to Segments > Find People from the CleverTap dashboard.
2. Select the **Partner Sync** event from the _Users who did_ section.
3. Select _Segments_ under _Display common properties, such as_, and select the segment name from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14cdf75-View_Audience_in_Find_People.png",
        null,
        "View the Imported Audience from Find People"
      ],
      "align": "center",
      "border": true,
      "caption": "View the Imported Audience from Find People"
    }
  ]
}
[/block]

# Partner Sync Event

The _Partner Sync_ event is raised for all the users who are part of different partner segments. The following table provides information about the event properties:

| <p>Property Name</p>        | <p>Description</p>                                                                                  | <p>Property Value/Example</p>           |
| :-------------------------- | :-------------------------------------------------------------------------------------------------- | :-------------------------------------- |
| <p>Partner Segment Name</p> | <p>Indicates the name of the audience (segment) exported from mParticle.</p>                        | <p>For example, Cart Drop off</p>       |
| <p>Action</p>               | <p>Indicates if the user has been added or removed from the segment in the CleverTap dashboard.</p> | <ul><li>Added</li><li>Removed</li></ul> |
| Partner Segment ID          | Indicates the Audience ID in the mParticle dashboard.                                               | For example, 47444                      |
| CT Source                   | Indicates the source of the event.                                                                  | mParticle                               |
| Partner Name                | Indicates the name of the partner from where the segment was imported.                              | mParticle                               |

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

### Q. Can I export the CleverTap engagement data to mParticle for analysis?

A. Yes. For more information, refer to [mParticle Export](doc:mparticle-export).