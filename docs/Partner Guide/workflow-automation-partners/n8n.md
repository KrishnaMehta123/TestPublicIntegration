---
title: n8n
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

[n8n](https://n8n.io) is a powerful no-code or low-code workflow automation tool that enables you to connect a wide range of applications through visual workflows. With the CleverTap and n8n integration, you can trigger workflows based on any app supported by n8n and send user or event data directly to CleverTap, without writing any custom code or handling the API manually.

With this integration, you can:

- Automatically send form submissions from tools such as Typeform or Google Forms to CleverTap for real-time user segmentation.
- Trigger CleverTap events when a deal is marked as won in CRM tools such as HubSpot.
- Ingest webhook data (for example, payment confirmations, support tickets) into CleverTap for timely, personalized engagement.

This document explains how to send _Form_ responses or data from other apps into CleverTap using n8n’s HTTP Request node.

# Prerequisites for Integration

Ensure you have the following before starting the integration:

- A CleverTap account with a valid **Account ID**and **Passcode**.
- An active [n8n account](https://n8n.io)

# Integrate n8n with CleverTap

To integrate n8n with CleverTap, perform the following three major steps:

1. [Create Trigger Node in n8n](doc:n8n#create-trigger-node-in-n8n).
2. [Set Up HTTP Request Node for CleverTap](doc:n8n#set-up-http-request-node-for-clevertap).
3. [Test and Activate Workflow](doc:n8n#test-and-activate-workflow).

## Create Trigger Node in n8n

Use this integration to automatically capture user details from form submissions, such as feedback, registration, or sign-up forms, and send them to CleverTap as user profiles for real-time personalization, segmentation, or campaign targeting. Create a workflow using a _Form Submission_ trigger in n8n to collect user data.

To do so, perform the following steps on the n8n dashboard:

1. Log in to your n8n account and create a _New Project_.
2. Click **Add First Step** and select a trigger node. For this example, select _Form Submission_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4a3f1c257e6080b29f7705a37a5448bbbb902fe04578ffc2abdb60a44c4eb45d-Screen_Recording_2025-07-02_at_3.40.01_PM_2.gif",
        "",
        "Set up a Form Submission trigger node in n8n to collect user input."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Up Form Submission Trigger Node in n8n to Collect User Input."
    }
  ]
}
[/block]


3. Design and configure your _Form_ as per your use case.
4. Test the _Form submission_ and check that the data is captured correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c813be0d569ea5d8cefbcb9a0b17d713bd9d88844fc1eea4c2f6a9ce7c780d3-Screen_Recording_2025-07-02_at_3.42.06_PM_1.gif",
        "",
        "Submit the form to test and capture user data."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Submit Form to Test and Capture User Data."
    }
  ]
}
[/block]


5. Save the trigger node once verified.

## Set Up HTTP Request Node for CleverTap

Capture _Form_ data and send it to CleverTap using an HTTP Request node. This step defines where and how you send the data. To do so, perform the following steps on the n8n dashboard:

1. Add a new node by clicking the **+** symbol.
2. Search and select the _HTTP Request_ node.
3. Set the _HTTP Method_ to `POST`.
4. Use the following CleverTap endpoint to upload user profile data: 
   ```
   <https://<Region Value>.api.clevertap.com/1/upload>
   ```
   Replace `<Region Value>` with your CleverTap region. To identify the region of your account, refer to [CleverTap Regions](https://developer.clevertap.com/docs/idc#api)
5. In the _Headers_ section, add the following key-value pairs:

   | Key                      | Value              |
   | ------------------------ | ------------------ |
   | `X-CleverTap-Account-Id` | Your Account ID    |
   | `X-CleverTap-Passcode`   | Your Passcode      |
   | `Content-Type`           | `application/json` |

To find your CleverTap Account ID and Passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/59d02f00f9bdcea5c7269da16f534a511feaaf608baa7e84ab00240391f1550f-Screen_Recording_2025-07-02_at_3.48.27_PM_1.gif",
        "",
        "Configure the HTTP Request node with CleverTap's endpoint and headers."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure HTTP Request Node with CleverTap Endpoint and Headers."
    }
  ]
}
[/block]


### Map Form Fields to CleverTap API Keys

In the HTTP Request node, you must map the _Form_ fields collected in n8n to the required CleverTap API keys to ensure the data is sent correctly. Depending on your use case, refer to [Upload/Update User Profile](https://developer.clevertap.com/docs/upload-user-profiles-api) or [Upload Events](https://developer.clevertap.com/docs/upload-events-api).

To map form fields, perform the following steps on the n8n dashboard:

1. Set the  _Body Parameters_ to _Raw JSON_.
2. Use dynamic variables from the _Form_ trigger node to populate the payload.  
   **Example Payload for Uploading User Profile**

```json
{
  "d": [
    {
      "objectId": "={{$json['email']}}",
      "type": "profile",
      "profileData": {
        "Name": "={{$json['name']}}",
        "Email": "={{$json['email']}}",
        "Phone": "={{$json['phone']}}"
      }
    }
  ]
}
```

3. Once mapped, click **Execute Node** to test if data is sent successfully.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d662e6cf73e9ef937f1c2212f3053ed7b82a1d400e787ed3becff5fb2fa0e22c-Screen_Recording_2025-07-02_at_3.53.00_PM_1.gif",
        "",
        "Map form fields to CleverTap’s user profile payload using dynamic variables."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Map Form Fields to CleverTap’s User Profile Payload Using Dynamic Variables"
    }
  ]
}
[/block]


## Test and Activate Workflow

Run the workflow and validate the results in CleverTap. After testing, activate the workflow to make it live. To do so, perform the following steps:

1. Go to your CleverTap dashboard and check if a user with the provided email has been created or updated. Open **User Profiles** in the CleverTap dashboard to confirm successful record creation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7a356561a78ea30b6dc659bab64a68dbae9c0399fc3b64a2e3a8e5f1ff9da5e-image.png",
        null,
        "Verify the user profile in the CleverTap dashboard after submission."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify User Profile on CleverTap Dashboard After Submission"
    }
  ]
}
[/block]


2. If successful, enable the **Activate** workflow in n8n.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/56584dd7f1c6100530f29c3cb1a4434c89f34de70e506dde3a634812b2618933-image.png",
        null,
        "Activate the workflow in n8n to start syncing data with CleverTap."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Activate Workflow in n8n to Sync Data with CleverTap"
    }
  ]
}
[/block]


Every time the _Form_ is submitted, the corresponding user data is synced with CleverTap. You can review **Recent API Calls** to troubleshoot or monitor the integration.

This integration allows you to automate user onboarding or event tracking using any app supported by n8n, without writing or maintaining any code.