---
title: Pipedream
excerpt: Workflow Automation
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

[Pipedream](https://pipedream.com/) is a developer-friendly, low-code platform that allows you to build workflows triggered by events, schedules, or app interactions, enhancing operational efficiency and flexibility. 

Integrating CleverTap with Pipedream automates workflows and streamlines processes by connecting multiple data sources. Pipedream transforms incoming data into the required format and sends it to CleverTap. This enables powerful actions such as updating user profiles or capturing events directly on the CleverTap dashboard, helping you achieve more with less effort. For example, with this integration, you can:

- Capture sign-up data and trigger personalized welcome campaigns.
- Record purchase events and send thank you emails or product recommendations.
- Detect cart abandonment events and trigger re-engagement notifications or emails.

# Prerequisites for Integration

The following are the prerequisites:

- Ensure you have access to your Pipedream account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Pipedream. The CleverTap and Pipedream integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Pipedream](https://pipedream.com/support) for support and resolution.

# Integrate Pipedream with CleverTap

To integrate Pipedream with CleverTap, you must add CleverTap as an action in your Pipedream workflow to connect your source data with CleverTap's engagement tools. This enables seamless synchronization and ensures real-time, accurate data power the user engagement strategies. 

To configure CleverTap Actions on Pipedream:

1. Click **+** in your workflow to _Add Action_.
2. Search for CleverTap in the action library
3. Select from the following for _Pre-built Actions_ to send pre-defined user properties to CleverTap:
   - [Create or Update User Data](doc:pipedream#create-or-update-user-data),
   - [Upload User Events](doc:pipedream#upload-user-events), or
   - [Select _Custom Actions_ to send custom user properties to CleverTap](doc:pipedream#build-any-clevertap-api-request-custom-user-properties)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f8b540471f4694ed9730649868321fa833833e51d8a98e66ee916646066a8b3-set_action.gif",
        "",
        "Set Actions"
      ],
      "align": "center",
      "border": true,
      "caption": "Add CleverTap as an Action on Pipedream"
    }
  ]
}
[/block]


## Create or Update User Data

Select this action to link data from your source application to add or update user profiles in CleverTap. To do so, you must map key fields such as email, name, phone number, and unique identity to sync user data as follows:

1. Select the _Create or Update User_ action under the _Pre-built Actions_ section.
2. Click **Connect a CleverTap Account** and enter the required credential information as follows:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f748359cd0afd1db82d726670e794f8c829ec4a8e377d034a89578926045f72-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


3. (Optional) Test the connection and click **Save** to establish the connection.
4. Map the following fields:

| **Field**        | **Description**                                   |
| ---------------- | ------------------------------------------------- |
| **Email**        | Denotes email address of the user.                |
| **Name**         | Denotes name of the user.                         |
| **Phone Number** | Denotes phone number (for example, +15555555555). |
| **Identity**     | A unique identifier (for example, user_id).       |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84c85d8d7765edbbd68a1ff76e8c0b94e48a03313e8386be2fdc2215e31e35c8-image.png",
        null,
        "Configuring User Data"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Mapping Key Fields"
    }
  ]
}
[/block]


4. Test and deploy the workflow to verify that user data is reflected in CleverTap and activates automatically whenever the trigger runs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a55e5641a8e162935163dfe3b61325fe1a85dc4ed378f93e9c9e569afd646091-image.png",
        null,
        "Test and Deploy"
      ],
      "align": "center",
      "border": true,
      "caption": "Test and Deploy"
    }
  ]
}
[/block]


You can verify if the user profile was created or updated by navigating to the _Segments_ page on the CleverTap dashboard.

## Upload User Events

Select this action to send user activity data to CleverTap, using pre-defined event names, to track actions and interactions for advanced analytics and engagement. To do so, follow these steps:

1. Select the _Upload User Events_ action under the _Pre-built Actions_ section.
2. Connect a CleverTap Account, refer to _Step 2_ of [Create or Update User Data](doc:pipedream#create-or-update-user-data).
3. Configure the following event details:

| **Field**      | **Description**                                               |
| -------------- | ------------------------------------------------------------- |
| **Event Name** | Select a custom or inbuilt event name (for example, Charged). |
| **Identity**   | Map the user’s unique identifier from the source.             |
| **Event Data** | Add key-value pairs for event-specific data.                  |

Example Data:

```asp JSON
{
  "Product Name": "Casio Watch",
  "Category": "Mens Watch"
}
```

> 📘 Supported Event Types
> 
> Both custom events and in-built events are supported when configuring CleverTap actions in Pipedream. Custom events refer to events you define, while in-built events are predefined in CleverTap (for example, Charged).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7f98d8c7b4792ccecaf22dcc8d01b48589b86e4b21f2f88769ec48c8b87394ec-image.png",
        null,
        "Configuring Event Data"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Configuring Event Data"
    }
  ]
}
[/block]


3. Test and deploy the workflow to ensure the event data is uploaded to the CleverTap dashboard and is linked to the correct user profile.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a3fdbf8f373bb753bdcf4cd9a31bec591ef7a79e1239b27d437d6619a5f6c6b6-image.png",
        null,
        "Test and Deploy"
      ],
      "align": "center",
      "border": true,
      "caption": "Test and Deploy"
    }
  ]
}
[/block]


To verify if the data is uploaded correctly, go to the _User Profiles_ or _Event Analytics_ page from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f3214ca3d83df5a3c8e9f630f36d2cb340664af2a2aabaa430411f3018bad03b-image.png",
        null,
        "Event in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Event in CleverTap"
    }
  ]
}
[/block]


## Build any CleverTap API request (Custom User Properties)

Select this action to send custom user properties to CleverTap to track user actions for advanced analytics and engagement. To do so, follow these steps:

1. Select _Build any CleverTap API request_ under the _Custom Actions_ section.
2. Configure Headers to connect the CleverTap Account:

   1. _HTTP Method_: Set the method to POST to push the custom user properties to CleverTap.
   2. _Base URL_: Enter the API endpoint based on the region of your CleverTap account. To identify the API endpoint for the region of your account, refer to [Region](https://developer.clevertap.com/docs/common-api-components#region).

   <br />

   ```coffeescript JSON
   <https://<region>>.api.clevertap.com/1/upload
   ```

   iii. Add the following key-value pairs in the headers:

   | **Header Key**         | **Description**           |
   | ---------------------- | ------------------------- |
   | User-Agent             | `pipdream/1`              |
   | Content-Type           | `application/json`        |
   | X-CleverTap-Account-Id | Your CleverTap Account ID |
   | X-CleverTap-Passcode   | Your CleverTap Passcode   |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74d89a821a36c70100113acb2766142faf6d22b3234783d48ae6aba10c2d4056-image.png",
        null,
        "Configure Headers"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Headers"
    }
  ]
}
[/block]


3. Configure the Request Body.

   You can push user profiles with custom user properties. Use key-value pairs or raw JSON to map the data to the respective source fields. Click **Edit Raw JSON** to add JSON payload.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72d915c82c34566e01018400d206697f30925ea0b19848a12784740080cfcb55-image.png",
        null,
        "Configure the Request Body"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Request Body"
    }
  ]
}
[/block]


The following is the sample payload you can add to the request body. In this example, `CustomerID` represents a custom user property that can be uploaded to CleverTap:

```coffeescript JSON
{
  "d": [
    {
      "Email":   "{{steps.trigger.event.newRow[2]}} ",
      "type": "profile",
      "profileData": {
        "CustomerID" : "{{steps.trigger.event.newRow[4]}}"
      }
    }
  ]
}
//we can add custom properties and additional details about the user to this 
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84fb9099b93638e091abaf54cbb016066dcee30b19c801f3afb15663fb113ef4-image.png",
        null,
        "Edit Raw JSON"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Raw JSON"
    }
  ]
}
[/block]


4. Test and deploy the workflow to ensure the custom user properties and user profiles are uploaded to the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3fd718dae6ea2bf08e9cf59aeeb3e305f6e840c43b6ec7c2040a925d90629e40-image.png",
        null,
        "Test and deploy"
      ],
      "align": "center",
      "border": true,
      "caption": "Test and deploy"
    }
  ]
}
[/block]


To verify if the custom user properties and user profiles are uploaded correctly, go to the _User Profiles_ or _Event Analytics_ page from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e7986ffdd0f7f541132add52da10a3d51c4a409d21c9b10f39aee1f5e67e6c6-image.png",
        null,
        "Custom User Properties"
      ],
      "align": "center",
      "border": true,
      "caption": "Custom User Properties"
    }
  ]
}
[/block]


# FAQs

### What use cases does Pipedream and CleverTap integration solve?

You can automate workflows such as updating user profiles, tracking custom events, and enhancing user engagement through personalized campaigns.

### Can I track custom events in CleverTap using Pipedream?

You can send custom events to CleverTap with event names and details, such as product information or user actions.