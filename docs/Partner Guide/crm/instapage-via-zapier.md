---
title: Instapage
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

[Instapage ](https://instapage.com/), a landing page platform, helps businesses create and optimize high-converting pages without coding. Marketers can capture leads through New Form Submissions, where visitors enter and submit their details (for example, Name, Email, Phone). 

Integrating Instapage with CleverTap via Zapier helps transfer leads, updates user profiles in real time, and triggers personalized engagement campaigns on CleverTap based on user actions.

The following are some of the use cases that the CleverTap Instapage integration can address:

- **Automatically Sync New Leads**: When a user submits a form on Instapage, [creation of a user profile is triggered](doc:instapage-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, phone number, and so on.
- **Update User Profiles with Form Submissions**: When an existing user fills out a new form, [updation of the profile is triggered](doc:instapage-via-zapier#createupdate-user-profiles) in CleverTap with the latest details, such as preferences or interests.
- **Trigger Personalized Campaigns**: When a user submits a lead form, [an event is uploaded](doc:instapage-via-zapier#upload-event) in CleverTap with event details such as submission time, form type, and campaign source to trigger automated engagement workflows.

# Prerequisites for Integration

The following are the prerequisites for Instapage:

- Ensure you have access to your Instapage Account with a valid workspace token.
- Ensure you have access to an active Zapier account to create the CleverTap app.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Instapage with CleverTap using Zapier

 The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:instapage-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Information](doc:instapage-via-zapier#createupdate-user-profiles). OR  
   [Upload Event](doc:instapage-via-zapier#upload-event).

## Create a Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

Consider an example where you want to automatically sync new forms submitted from Instapage with CleverTap to trigger personalized engagement campaigns. This automation ensures that new forms submitted from Instapage are added to CleverTap while existing forms are updated when details change. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Instapage.

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
   1. Select _Instapage_ from the _App_ section. This starts the Zap when a trigger event occurs on Instapage.
   2. Select _Trigger Event_ from the dropdown list and then select _Form Submission_ for this use case.
   3. Select _Account_ and sign in using your Instapage [workspace token](https://help.instapage.com/hc/en-us/articles/11953465179159-Workspace-settings-and-account-settings). You can also connect a new account if your account does not appear in the dropdown. refer to [Integrating with Zapier](https://help.instapage.com/hc/en-us/articles/360001720908-Integrating-with-Zapier).
   4. Click **Continue** after your workspace token has been accepted. All the pages within this particular workspace will be imported. 
   5. Select the page that you want to connect to and click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2d788816cb3c71f454307f8cd3955ac227e0341993190afa1b598bb31d38d5f8-2025-02-03_10-25-08_1.gif",
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
   After testing the trigger, you will see details of pulled records similar to the image below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2b99401f69593a359ac1110a6c6132c140c061aea1316e7f1215c969851f7566-image.png",
        null,
        "Pulled Records"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Details of Pulled Records"
    }
  ]
}
[/block]


5. Click **Continue with selected record**.
6. _Select the Action_ that zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ event dropdown.
   2. Select _Create/Update User Profile_ from the _Action event_ dropdown. This implies that whenever a new form is submitted, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. 
   4. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained in the [Create a Passcode on CleverTap Dashboard](doc:instapage-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   5. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1a233c252eb2bcb8a9952932a4c94bcd2c56bd83be36c80dfc1dfe7d1e10392-2025-02-03_10-28-31_1.gif",
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


6. **Configure the Action**. Map Instapage data fields to CleverTap fields as follows:

| **CleverTap Field**    | **Instapage Field**                                                                              |
| ---------------------- | ------------------------------------------------------------------------------------------------ |
| **Identity**           | Instapage user ID field, email ID, or any unique identity field corresponding to the user.       |
| **Creation Date**      | Date of the user’s creation in Instapage.                                                        |
| **Profile Properties** | Include user properties in JSON format (such as name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1be3cfe84968a98c1dbd121081cd4be5e12c18892130be9c8646894169f5566-image.png",
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

Consider an example where a user submits a form on an Instapage landing page to download a resource, such as the "Marketing Trends 2025" eBook. This automation ensures that the form submission is recorded as an event in CleverTap, allowing businesses to track content engagement. By leveraging this data, businesses can segment users based on interests, trigger targeted email/SMS campaigns, and re-engage them with personalized offers or webinars, improving conversions and retention

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select _Instapage_ from the _App_ section. This starts the Zap when a trigger event occurs in Instapage.
   2. Select _Trigger Event_ from the dropdown list and select _Form Submission_ in this case.
   3. Select _Account_ and sign in using your Instapage [workspace token](https://help.instapage.com/hc/en-us/articles/11953465179159-Workspace-settings-and-account-settings). You can also connect a new account if your account does not appear in the dropdown. refer to [Integrating with Zapier](https://help.instapage.com/hc/en-us/articles/360001720908-Integrating-with-Zapier).
   4. Click **Continue** once your workspace token has been accepted, and all the pages within this particular workspace will be imported. 
   5. Select the page that you want to connect to and click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ca1b44f10b3a82190de50fdc829cfd13bd75b47b4e2e269f82d9ca0bb54416ca-2025-02-03_10-25-08_1.gif",
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
4. Click **Continue**. After testing the trigger, you will see details of pulled records similar to the image under _step 4_ of [Create/Update User Profiles](doc:instapage-via-zapier#createupdate-user-profiles). 
5. Select any one record, and click **Continue with selected record**.
6. **Select the Action** that the zap must perform after the trigger event occurs.  To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ event dropdown.
   2. Select _Upload Event_ from the Action _event_ dropdown. This implies that whenever a new event is generated, a new user profile is created, and an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. For more information about how to do this, refer to _step 5 (iii)_ under [Create or Update User Profiles](doc:instapage-via-zapier#createupdate-user-profiles).
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea4a8b64eba629e8b65a9e30c07117ea9a4b19ecf120e40044b2d8f48a43dbe7-image.png",
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


6. **Configure the Action**. Map Instapage data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Instapage Field**                                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Instapage user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                                 |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the Instapage data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                               |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75d925cad97915288b31dd58bcf061e64113db667f8054c4d9742507d6de5a5c-image.png",
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


7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs. CleverTap uses the _Identity_ field to identify whether the user is new or existing. You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a259011eccc4f51a518798447618f843a3045fcacb8c5028b0314434397c9058-image.png",
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


# FAQs

### What happens if you do not map the required fields?

Not mapping required fields may result in incomplete data being transferred or failure to update user profiles and events correctly.