---
title: Pipedrive
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

[Pipedrive](https://www.pipedrive.com/) is a sales CRM and pipeline management tool that helps businesses track and manage leads efficiently. It enables sales teams to capture and store lead details, track deal progress, and automate workflows.

By integrating Pipedrive with CleverTap via Zapier, businesses can automatically transfer lead information, update user profiles in real-time, and trigger personalized engagement campaigns based on sales activities.

The following are some of the use cases that the CleverTap Pipedrive integration can address:

* **Automatically Sync New Leads**: When a new deal is added to Pipedrive, [create a user profile](doc:pipedrive-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, phone number, and deal information.
* **Update User Profiles with Deal Progress**: When a deal moves to a new stage in Pipedrive, [update the user profile](doc:pipedrive-via-zapier#createupdate-user-profiles) in CleverTap with the latest status and insights.
* **Trigger Personalized Campaigns**: When a deal reaches a specific stage, [upload an event](doc:pipedrive-via-zapier#upload-event) in CleverTap with event details like deal value, expected close date and pipeline stage to trigger automated engagement workflows.

# Prerequisites for Integration

The following are the prerequisites for Pipedrive:

* Ensure you have access to your Pipedrive account.
* Ensure you have an active Zapier account to create the CleverTap app.
* Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Pipedrive with CleverTap using Zapier

The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:pipedrive-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Information](doc:pipedrive-via-zapier#createupdate-user-profiles). OR\
   [Upload Event](doc:pipedrive-via-zapier#upload-event)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

Consider an example where you want to automatically sync new deals created in Pipedrive with CleverTap to trigger personalized engagement campaigns. This automation ensures that new deals in Pipedrive are added to CleverTap while existing deals are updated when details change. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.

<Image alt="Create a Zap on Zapier Dashboard" align="center" border={true} src="https://files.readme.io/9b71c999e832d4a3344a2216c4e72dfaacf78feabca42da8617b0ec20d049f49-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select *Pipedrive* from the *App* section. This starts the Zap when a trigger occurs on Pipedrive.
   2. Select *Trigger Event* from the dropdown list and then select *New Deal* for this use case.
   3. Select *Account* and sign in using your Pipedrive account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**.

<Image alt="Set up a Trigger" align="center" border={true} src="https://files.readme.io/025aad465c9d8525aefe051b3e00527a19be288fbc9c3783a580bcfa86d91ded-2025-02-05_21-11-27_1.gif">
  Set up a Trigger
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. After testing the trigger, you will see details of pulled records similar to the image below.

<Image alt="Selected Record" align="center" border={true} src="https://files.readme.io/4228c30c6ec1a9d3459aa459992cb5956cc5d602646ad2542187f960b00453ea-image.png">
  Selected Record
</Image>

5. Select any one record, and click **Continue with selected record**.
6. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the Action event dropdown. This implies that whenever a new deal is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select Account to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:pipedrive-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for zap" align="center" border={true} src="https://files.readme.io/fc717f4c26a1621b3e2a0f2f4c5c00f00f5241fb10d22c8425c3b03a31c3dac9-2025-02-05_21-28-45_1.gif">
  Select the Action for Zap
</Image>

7. **Configure the Action**. Map Pipedrive data fields to CleverTap fields as follows:

| **CleverTap Field**    | **Description**                                                                                       |
| ---------------------- | ----------------------------------------------------------------------------------------------------- |
| **Identity**           | Pipedrive user ID field, email ID, or any unique identity field corresponding to the user.            |
| **Creation Date**      | Date of the user creation in Pipedrive.                                                               |
| **Profile Properties** | Include user properties in JSON format (for example, name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" border={true} src="https://files.readme.io/b137ee8d99e66d05b6ecf7509309bbff429e8dd34daef21bed9e10937c91323e-image.png">
  Configure the Action
</Image>

8. Click **Continue** and click **Test Step** to test the zap after mapping the files.
9. Click **Publish**.

After publishing this zap, a new user is created, or an existing user is updated on the CleverTap dashboard every time a trigger occurs. CleverTap uses the *Identity* field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm the user profile has been created or updated.

<Image alt="Verify user in CleverTap" align="center" border={true} src="https://files.readme.io/22d496be8a5e1407f768b1da28e7e73561e1f39613a71b5229193767f597293e-image.png">
  Verify user in CleverTap
</Image>

## Upload Event

Consider an example where you want to track key deal activities in CleverTap. This automation ensures that sales actions taken in Pipedrive are recorded in CleverTap, enabling better tracking and personalized engagement strategies. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select *Pipedrive* as the App. This starts the Zap when a trigger event takes place in Pipedrive.
   2. Select *Trigger Event* from the dropdown list and select *Updated Deal Stage* in this case.
   3. Select *Account* and sign in using your Pipedrive account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**.

<Image alt="Set up a Trigger" align="center" border={true} src="https://files.readme.io/d9e074e4b07540b143f61dc71ec4da4e1bcc9e42451b2c6f58f63c42b0102c24-2025-02-05_21-44-34_1.gif">
  Set up a Trigger
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. After testing the trigger, you will see details of pulled records similar to the image under step 4 of [Create/Update User Profiles](doc:pipedrive-via-zapier#createupdate-user-profiles). Select any one record, and click **Continue with selected record**.
5. **Select the Action** the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the *Action event* dropdown. This implies that whenever a new event is generated, an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. For more information about how to do this, refer to *step 6 (iii)* under [Create or Update User Profiles](doc:pipedrive-via-zapier#createupdate-user-profiles).
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action" align="center" border={true} src="https://files.readme.io/fed63e6f70382484136efce39f42f47753018a2caf535a70778a13e91637a8e5-2025-02-05_21-52-39_1.gif">
  Select the Action
</Image>

6. **Configure the Action**. Map Pipedrive data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Pipedrive Field**                                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Pipedrive user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                                 |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the Pipedrive data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                               |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" border={true} src="https://files.readme.io/4cef3c097583c00da8e273e8a493dd9411e6937bc24897765bed10f1a5f57e9d-image.png">
  Configure the Action
</Image>

7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs.\
CleverTap uses the Identity field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

<Image alt="Verify Events in CleverTap" align="center" border={true} src="https://files.readme.io/3a99d9007e84cf54336a785f0e1482249157b58c9d03b37f8e5ea33cd1d4fb5c-image.png">
  Verify Events in CleverTap
</Image>

# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data transfer or failure to update user profiles and events correctly.
