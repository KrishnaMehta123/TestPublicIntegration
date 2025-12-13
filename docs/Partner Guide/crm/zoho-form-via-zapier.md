---
title: Zoho Form
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

[Zoho Forms](https://www.zoho.com/) is an online form builder that enables businesses to collect structured data for lead generation, feedback, event registrations, and more.

Using Zapier to integrate Zoho Form with CleverTap, you can do the following:

- **Keep CRM Data Synchronized**: When a new lead submits a Zoho Form, [create a user profile](doc:zoho-form-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, phone number, and so on.
- **Remove Converted Users from Re-Engagement Campaigns**: When a user converts through a Zoho Form (for example, completes a feedback), [update the user profile](doc:zoho-form-via-zapier#createupdate-user-profiles) in CleverTap (example, mark the profile as Converted).
- **Track Lead Source**: When a new lead submits a Zoho Form, [upload an event](doc:zoho-form-via-zapier#upload-event) in CleverTap with details such as event name, lead source, campaign name, and lead contact information. You can then use the event data to add the lead to a Zoho Form for tailored retargeting ads.

# Prerequisites for Integration

The following are the prerequisites for Zoho:

- Ensure you have access to your Zoho account.
- Ensure you have access to an active Zapier account to create the CleverTap app.
- Ensure you have access to the CleverTap dashboard.

# Integrate Zoho with CleverTap

The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:zoho-form-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Information](doc:zoho-form-via-zapier#createupdate-user-profiles). OR  
   [Upload Event](doc:zoho-form-via-zapier#upload-event)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

Consider an example where you want to automatically sync leads from Zoho with CleverTap to trigger personalized engagement campaigns. This automation ensures that new leads from Zoho are added to CleverTap while existing leads are updated when details change. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Zoho.

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
   1. Select _Zoho Forms_ from the _App_ section. This starts the Zap when a trigger event occurs on Zoho Forms.
   2. Select _Trigger Event_ from the dropdown list and then select _New Form Entry_ for this use case.
   3. Select _Account_ and sign in using your Zoho Forms account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**. From the _Configure_ section, fill in the mandatory detail.
   5. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90d9d7ef7ab31873c44d939a041d78fa85a67855deffd9ac760e17ac8b448f32-2025-05-12_00-20-14_1.gif",
        "",
        "Set Up Trigger Event"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue**.
5. **Select the Action the zap must perform after the trigger event occurs.** To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ event dropdown.
   2. Select _Create/Update User Profile_ from the _Action event_ dropdown. This implies that whenever a new lead is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. 
   4. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained in the [Create a Passcode on CleverTap Dashboard](doc:zoho-form-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   5. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d0dfca0f6afd34b71d8af0a427d86d5dfb30c315691437c1d9e96da346f34c5-2025-05-12_00-27-30_1.gif",
        "",
        "Select Action for Zap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map Zoho Form data fields to CleverTap fields as follows:

| **CleverTap Field**    | **Zoho Form**                                                                                    |
| ---------------------- | ------------------------------------------------------------------------------------------------ |
| **Identity**           | Zoho Form user ID field, email ID, or any unique identity field corresponding to the user.       |
| **Creation Date**      | Date of the user’s creation in Zoho Form.                                                        |
| **Profile Properties** | Include user properties in JSON format (such as name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a78bcc46eb7dccb38faf8afc6f56cea9c0c0eaf810b0ad58a80490c17e1cc246-image.png",
        null,
        "Configure the Action"
      ],
      "align": "center",
      "sizing": "75% ",
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
        "https://files.readme.io/2fa5b9906d44c1d52a372e152207bac731edb98bea70bb57d10ea5430e88d474-image.png",
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

Consider an example where you want to upload an event to CleverTap with details such as event name, lead source, campaign name, and lead contact information. Every time a new lead submits a Zoho form. This automation ensures that user actions or events tracked in Zoho form are automatically recorded in CleverTap, enabling better tracking and personalized engagement strategies. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select _Zoho Forms_ from the _App_ section. This starts the Zap when a trigger event occurs on Zoho Forms.
   2. Select _Trigger Event_ from the dropdown list and then select _New Form Entry_ for this use case.
   3. Select _Account_ and sign in using your Zoho Forms account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**. From the _Configure_ section, fill in the mandatory detail.
   5. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90d9d7ef7ab31873c44d939a041d78fa85a67855deffd9ac760e17ac8b448f32-2025-05-12_00-20-14_1.gif",
        "",
        "Set Up Trigger Event"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue**.
5. Select the Action that the zap must perform after the trigger event occurs.  To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ event dropdown.
   2. Select _Upload Event_ from the Action _event_ dropdown. This implies that whenever a new event is generated, a new user profile is created, and an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. For more information about how to do this, refer to _step 5 (iii)_ under [Create or Update User Profiles](doc:zoho-form-via-zapier#createupdate-user-profiles).
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b789ebf6ebef1290e1cff3bea5b31bf06bb69129168c6e99d9450c8013fd3fe-2025-05-12_00-46-58_1.gif",
        "",
        "Select Action for Zap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map Zoho Form data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Zoho Form**                                                                                                        |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Zoho Form user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                                 |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the Zoho Form data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                               |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3322ece5499cfa79224e4f23f9639ce386e8f860d64131d31f43301bc8be4e22-image.png",
        null,
        "Configure the Action"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure the Action"
    }
  ]
}
[/block]


7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs. CleverTap uses the _Identity_ field to identify if it is a new user or an existing user.

You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9945540bf21ecc30ebe4930ed8545d4d62da118d2bdeafef19b9c986a802e3ab-image.png",
        null,
        "Verify Events in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify Events in CleverTap"
    }
  ]
}
[/block]


# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data being transferred or failure to update user profiles and events correctly.