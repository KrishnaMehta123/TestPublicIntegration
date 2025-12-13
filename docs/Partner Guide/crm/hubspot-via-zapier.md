---
title: HubSpot
excerpt: Customer Relationship Management
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

[HubSpot](https://www.hubspot.com/products/crm), a leading CRM platform, helps businesses manage customer relationships, automate workflows, and analyze performance to drive growth and improve customer engagement.

Using Zapier to integrate HubSpot with CleverTap, you can do the following:

- **Automate Lead Sync**: When a new contact is added in HubSpot, [create a user profile](doc:hubspot-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, and phone number to trigger personalized engagement campaigns.
- **Keep Profile Data Updated**: When contact details (such as email or phone number) change in HubSpot, [update the user profile](doc:hubspot-via-zapier#createupdate-user-profiles) in CleverTap to ensure accurate segmentation and targeting in engagement campaigns.
- **Track Contact Lifecycle Events**: When a contact performs a key action in HubSpot (for example, completes a deal or fills out a form), [upload an event](doc:hubspot-via-zapier#upload-event) in CleverTap with details such as event name, action type, and contact information. Use this event data to trigger relevant engagement campaigns or add contacts to tailored audiences for retargeting.

# Prerequisites for Integration

The following are the prerequisites for HubSpot:

- Ensure you have access to your HubSpot account.
- Ensure you have access to an active Zapier account to create the CleverTap app.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate HubSpot with CleverTap using Zapier

 The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:hubspot-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Information](doc:hubspot-via-zapier#createupdate-user-profiles). OR  
   [Upload Event](doc:hubspot-via-zapier#upload-event).

## Create a Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode). 

## Create/Update User Profiles

Consider an example where you want to automatically sync HubSpot contacts with CleverTap to trigger personalized engagement campaigns. This automation ensures that new HubSpot users are added to CleverTap while existing user profiles are updated when details change in HubSpot. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications. In this case, it will be HubSpot.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9b71c999e832d4a3344a2216c4e72dfaacf78feabca42da8617b0ec20d049f49-image.png",
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
   1. Select _HubSpot_ from the _App_ section. This starts the Zap when a trigger event takes place in HubSpot.
   2. Select _Trigger Event_ from the dropdown list and then select _New Contact_ for this use case.
   3. Select _Account_ and sign in using your HubSpot account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**. From the _Configure_ section, default properties will be already defined. You can add _Additional properties_ from the dropdown. For more information about the properties provided by HubSpot, refer to [Properties](https://developers.hubspot.com/docs/guides/api/crm/properties).
   5. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8c8e43d2ae7299e6e79b15e05341ad27d74528cd840c33403ca12f7e15724c72-hubspot_1.gif",
        "",
        "Set Up Trigger Event"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Select any one record, and click **Continue with selected record**.
5. Select the Action that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Create/Update User Profile_ from the _Action event_ dropdown. This implies that whenever a new lead is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:hubspot-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ebfce5b2976eb7c05e1f78da1a0ad1d2960d0240ecfa59f646c7d74b2571f21-hubbb1.1.gif",
        "",
        "Select Action for Zap"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map HubSpot data fields to CleverTap fields as follows:

| **CleverTap Field**    | ** Description**                                                                                      |
| ---------------------- | ----------------------------------------------------------------------------------------------------- |
| **Identity**           | HubSpot user ID field, email ID, or any unique identity field corresponding to the user.              |
| **Creation Date**      | Date of the user creation in HubSpot.                                                                 |
| **Profile Properties** | Include user properties in JSON format (for example, name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a303ee0133a36cc819514b7307040228eda352b74d549c075c8efd229f962659-hubb2.2.gif",
        "",
        "Configure the Action"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure the Action"
    }
  ]
}
[/block]


7. Click **Continue** and click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, a new user is created, or an existing user is updated on the CleverTap dashboard every time a trigger occurs. CleverTap uses the _Identity_ field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm the user profile has been created or updated. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22d496be8a5e1407f768b1da28e7e73561e1f39613a71b5229193767f597293e-image.png",
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

Consider an example where you want to track user interactions, such as new contact added, in HubSpot and sync it with CleverTap for better engagement. This automation ensures that user actions recorded in HubSpot are seamlessly uploaded to CleverTap, enabling more precise tracking and personalized engagement strategies. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select _HubSpot_ from the _App_ section. This starts the Zap when a trigger event takes place in HubSpot.
   2. Select _Trigger Event_ from the dropdown list and select _New Deal_ in this case.
   3. Select _Account_ and **Sign in** with your HubSpot account credentials. If your account does not appear in the dropdown, you can also connect a new account.
   4. Click **Continue**. Under the _Configure_ section, default properties are already defined. You can add _Additional properties_ from the dropdown. For more information about the properties provided by HubSpot, refer to [Properties](https://developers.hubspot.com/docs/guides/api/crm/properties).
   5. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82d397d156b832b034e6f6a3c436c345c57b0234cc826c5d9f2997dc6a5c3a01-h1b1.gif",
        "",
        "Set Up Trigger Event"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue with selected records**.
5. **Select the Action the zap must perform** after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the _Action event_ dropdown. This implies that whenever a new event is generated, an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. For more information about how to do this, refer to _step 5 (iii)_ under [Create or Update User Profiles](doc:hubspot-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/418e2742b66486bdd58872e444adab8e40d5423da64a6e16cb9275b1b2ead993-2025-01-31_18-56-59_1.gif",
        "",
        "Select Action for Zap"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map HubSpot data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Description**                                                                                                    |
| -------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **User ID**          | HubSpot user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                               |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the HubSpot data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                             |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/15fb9202fc85976eeec6196ee01ba320763402547310a93c3309eeb879ec9389-2025-01-31_18-58-36_1.gif",
        "",
        "Configure the Action"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure the Action"
    }
  ]
}
[/block]


7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs.  
CleverTap uses the _Identity_ field to identify if it is a new user or an existing user.

You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/97691b0eb7a10b805c2f2ee8f7bdc6afe85fc94f39d0a43e6e8d04500e553eb6-image.png",
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