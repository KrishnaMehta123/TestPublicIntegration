---
title: Slack (via Zapier)
excerpt: Messenger Partner
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

[Slack](https://slack.com/) is a messaging platform that enables teams to communicate and collaborate in real time. By integrating Slack with CleverTap via Zapier, businesses can automate workflows, track user interactions, update user profiles, and trigger personalized campaigns based on Slack activities.

The following are some of the use cases that the CleverTap Slack integration can address:

- **Track Key Engagement Activities**: Capture Slack interactions such as message posts, reactions, or mentions and log them as events in CleverTap.
- **Automate Internal Notifications**: Send automated notifications to a Slack channel when key events are raised in CleverTap.
- **Update or Create User Profiles**: Automatically [update user profiles](doc:slack-via-zapier#createupdate-user-profiles) in CleverTap based on Slack interactions, ensuring accurate and real-time data synchronization.

# Prerequisites for Integration

The following are the prerequisites for Slack integration:

- Ensure you have access to your Slack workspace with admin permissions.
- Ensure you have an active Zapier account to create the CleverTap integration.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Slack with CleverTap using Zapier

The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Profiles](doc:slack-via-zapier#createupdate-user-profiles).OR  
   [Upload Event](doc:slack-via-zapier#upload-event).

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate API requests. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

To ensure real-time updates and maintain accurate user data in CleverTap, you can automatically update or create user profiles based on Slack interactions. Perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d40f28468176d9ecfb6604f0bfe71dd6508f502d2d288acc7396da4c9f2b212-image.png",
        null,
        "Create a Zap on Zapier Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Zap on Zapier Dashboard"
    }
  ]
}
[/block]


2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select _Slack_ from the _App_ section. This starts the Zap when a trigger occurs on Slack.
   2. Select _Trigger Event_ from the dropdown list and then select _New Message Posted_ or _New Reaction Added_ for this use case.
   3. Select _Account_ and sign in using your Slack account credentials. Authorize Zapier to access your Slack workspace. You can also connect a new account if your account does not appear in the dropdown
   4. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa6d7f84db141947e09669e3ed4e2627073e1189f557658efd16e85f1078573a-rework_sla_1.gif",
        "",
        "Set up a Trigger"
      ],
      "align": "center",
      "border": true,
      "caption": "Set up a Trigger"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. After testing the trigger, you will see details of pulled records similar to the image below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5b273e7b7a2043b6c365372c022069da325e3a523ccfbe877841f0e3028ec89-image.png",
        null,
        "Selected Record"
      ],
      "align": "center",
      "border": true,
      "caption": "Selected Record"
    }
  ]
}
[/block]


5. Select any one record, and click **Continue with selected record**.
6. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the App dropdown.
   2. Select _Create/Update User Profile_ from the _Action event_ dropdown. This will create or update user details such as email, role, and activity based on Slack interactions.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:slack-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a3efb6339fc4acab6933a7203d732258e4ad77518bda86e639335e644d1584e4-2025-02-05_23-30-09_1.gif",
        "",
        "Select the Action"
      ],
      "align": "center",
      "border": true,
      "caption": "Select the Action"
    }
  ]
}
[/block]


7. **Configure the Action**. Map Slack data fields to CleverTap fields as follows:

| **CleverTap Profile Field** | **Slack Field**                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------ |
| **Identity**                | Slack user ID field, email ID, or any unique identity field corresponding to the user.           |
| **Creation Date**           | Date of the user’s creation in Slack.                                                            |
| **Profile Properties**      | Include user properties in JSON format (such as name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8642dd6ee1bd3f81cee31aebbc2873981a81ec75b3688a87b729a343d44de8b0-image.png",
        null,
        "Configure the Action"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure the Action"
    }
  ]
}
[/block]


8. Click **Continue** and click **Test Step** to test the zap after mapping the files.
9. Click **Publish**.

After publishing this, Zap will automatically create or update user profiles in CleverTap whenever relevant Slack interactions occur. This ensures user data remains up-to-date and helps in deliver personalized engagement. You can verify this by checking your CleverTap dashboard to confirm the user profile has been created or updated.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ce1ae4eb36ce0cdf6fcbcd767bb14a3ccd498e085e0422f0fc0d9acc899b6d5a-image.png",
        null,
        "Verify user in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Verify user in CleverTap"
    }
  ]
}
[/block]


## Upload Event

Consider an example where you want to track user engagement activities in Slack and log them as events in CleverTap. This allows you to analyze interactions and personalize engagement strategies. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select _Slack_ from the _App_ section. This starts the Zap when a trigger occurs on Slack.
   2. Select _Trigger Event_ from the dropdown list and then select _New Message Posted_ or _New Reaction Added_ for this use case.
   3. Select _Account_ and sign in using your Slack account credentials. Authorize Zapier to access your Slack workspace. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa6d7f84db141947e09669e3ed4e2627073e1189f557658efd16e85f1078573a-rework_sla_1.gif",
        "",
        "Set up a Trigger"
      ],
      "align": "center",
      "border": true,
      "caption": "Set up a Trigger"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. After testing the trigger, you will see details of pulled records similar to the image under step 4 of [Create/Update User Profiles](doc:slack-via-zapier#createupdate-user-profiles). Select any one record, and click **Continue with selected record**.
5. **Select the Action** the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the App dropdown.
   2. Select _Upload Event_  from the _Action event_ dropdown. This will log interactions (messages, reactions) as events for analytics and automation.
   3. Select _Account_ to connect the CleverTap account. For more information about how to do this, refer to step 6 (iii) under [Create/Update User Profiles](doc:slack-via-zapier#createupdate-user-profiles).
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/47b61eac0acbcdf21d2d5de2c569c136ed358b6f9d4f2e354bcb48d6ec1c3f5c-image.png",
        null,
        "Select Action for Zap"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map Slack data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Slack Field**                                                                                                  |
| -------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Slack user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                             |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the Slack data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                           |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d138d08ece87cad5edbe25444ea319b9a6c32b901a1063fca2c8b01d8d419d35-image.png",
        null,
        "Configure the Action"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure the Action"
    }
  ]
}
[/block]


7. Click **Continue**Click **Test Step** to test the zap after mapping the files.
8. Click **Publish** to activate the Zap.

After publishing this, Zap will log Slack events as CleverTap events, providing actionable insights into user engagement. This data can be leveraged for analytics and triggering automated campaigns. You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b025e3e336babe3ab6761036891af08b6ec988cce876885d2fcd87ed507a7526-image.png",
        null,
        "Verify Events in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Verify Events in CleverTap"
    }
  ]
}
[/block]


## FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data transfer or failure to trigger events and campaigns correctly.