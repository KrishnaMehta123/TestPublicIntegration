---
title: Salesforce CRM
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

[Salesforce](https://www.salesforce.com/) is a leading CRM platform that helps businesses manage customer relationships, track sales activities, and automate workflows. By integrating Salesforce with CleverTap via Zapier, businesses can automatically sync customer data, track engagement, and trigger personalized campaigns based on sales interactions.

The following are some of the use cases that the CleverTap-Salesforce integration can address:

* **Automatically Sync Salesforce Contacts**: When a new contact is added to Salesforce, [create a user profile](doc:salesforce-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, phone number, and lead status.
* **Update User Profiles with Sales Activities**: When a lead progresses to a new stage in the sales pipeline (For example, from Prospect to Qualified Lead or Negotiation to Closed-Won) in Salesforce, [update the user profile](doc:salesforce-via-zapier#createupdate-user-profiles) in CleverTap with the latest insights.
* **Trigger Personalized Campaigns**: When a deal is closed in Salesforce, [upload an event](doc:salesforce-via-zapier#upload-event) in CleverTap with event details such as deal value, close date, and salesperson information to trigger automated engagement workflows.

# Prerequisites for Integration

The following are the prerequisites for Salesforce:

* Ensure you have admin access to your Salesforce account.
* Ensure you have an active Zapier account to create the CleverTap app.
* Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Salesforce with CleverTap using Zapier

The integration process involves the following two major steps:

1. [Create Passcode on CleverTap Dashboard](doc:salesforce-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Profiles](doc:salesforce-via-zapier#createupdate-user-profiles).\
   OR\
   [Upload Event](doc:salesforce-via-zapier#upload-event).

## Create Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

Consider an example where you want to automatically sync new Salesforce contacts with CleverTap to trigger personalized engagement campaigns. This automation ensures that new contacts in Salesforce are added to CleverTap while existing profiles are updated when details change. To do so, perform the following steps:

1. Log into the [Zapier Dashboard](https://zapier.com/app/home) and click **+ Create Zap**.

<Image alt="Create a Zap on Zapier Dashboard" align="center" width="75% " border={true} src="https://files.readme.io/f6a83adf175766819e979676ed2e40166e63233b96d64c3d1735ed2237ef43b7-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select *Salesforce* from the *App* dropdown. This starts the Zap when a trigger occurs on Salesforce.
   2. Select *Trigger Event* from the dropdown list and then select *New contacts* for this use case.
   3. Select *Account* and sign in using your Salesforce account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**.

<Image alt="Set up a Trigger" align="center" width="75% " border={true} src="https://files.readme.io/49910d8377cf69dde60e41917fcf0f4f8bc3094d822ee80b81a79b2ad564a051-2025-02-06_02-08-49_1.gif">
  Set up a Trigger
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Select relevant Salesforce objects to monitor and click **Continue**.
5. **Select the Action** that the zap must perform after the trigger occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the *Action event* dropdown. This implies that whenever a new contact is added in Salesforce, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:salesforce-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/3ab5447a6bfe7c10eea3c4c2b29b5e5380b2f868ffe471a50717c245346afaec-2025-02-06_02-20-52_1.gif">
  Select Action for Zap
</Image>

6. **Configure the Action**. Map Salesforce data fields to CleverTap fields as follows:

| **CleverTap Field**    | **Salesforce Field**                                                                             |
| ---------------------- | ------------------------------------------------------------------------------------------------ |
| **Identity**           | Salesforce user ID field, email ID, or any unique identity field corresponding to the user.      |
| **Creation Date**      | Date of the user creation in Salesforce.                                                         |
| **Profile Properties** | Include user properties in JSON format (such as name, email, role, and other custom properties). |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" width="75% " border={true} src="https://files.readme.io/6dd75773f6f0c046b67da9909e18de805a3769e683136af8329b65a03cfe6a2e-image.png">
  Configure the Action
</Image>

7. Click **Continue** and click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, a new user is created, or an existing user is updated on the CleverTap dashboard every time a trigger occurs. CleverTap uses the *Identity* field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm the user profile has been created or updated.

<Image alt="Verify user in CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/22d496be8a5e1407f768b1da28e7e73561e1f39613a71b5229193767f597293e-image.png">
  Verify user in CleverTap
</Image>

## Upload Event

Consider an example where you want to track key sales activities or the status of sales records in CleverTap, this automation helps by seamlessly syncing sales interactions from Salesforce to CleverTap. This enables real-time tracking, better visibility into customer touchpoints, and the ability to trigger personalized engagement strategies based on sales progress. To do so, perform the following steps:

1. Log into the [Zapier Dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select *Salesforce* as the *App*. This starts the Zap when a trigger event takes place in Salesforce.
   2. Select *Trigger Event* from the dropdown list and select *Updated Record* in this case.
   3. Select *Account* and sign in using your Salesforce account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**.

<Image alt="Set up a Trigger" align="center" width="75% " border={true} src="https://files.readme.io/2d6934cb8569b57a5d5be4ab64ee390a6418e94ac98a7d4067be6c3b65194117-2025-02-06_02-29-51_1.gif">
  Set up a Trigger
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the *Action event* dropdown. This implies that whenever a record is updated, an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. For more information about how to do this, refer to *step 5 (iii)* under [Create or Update User Profiles](doc:salesforce-via-zapier#createupdate-user-profiles).
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/4a721610d94c496a9da6bc85f50a26fb922907a5a0137ce1bf208bd0fecb121c-2025-02-06_02-37-47_1.gif">
  Select Action for Zap
</Image>

6. **Configure the Action**. Map Salesforce data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Salesforce Field**                                                                                                          |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Salesforce user ID field, email ID, or any unique identity field corresponding to the user.                                   |
| **Creation Date**    | Event creation date.                                                                                                          |
| **Event Name**       | You can select a predefined event or create a custom event. You can also map the event name using the Salesforce data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                                        |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" width="75% " border={true} src="https://files.readme.io/883a5b33191ab0d8ea765b4621f83e8339db36668ed11a1642462d9d18fecee7-image.png">
  Configure the Action
</Image>

7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs.\
CleverTap uses the *Identity* field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

<Image alt="Verify Events in CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/3a99d9007e84cf54336a785f0e1482249157b58c9d03b37f8e5ea33cd1d4fb5c-image.png">
  Verify Events in CleverTap
</Image>

# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data transfer or failure to update user profiles and events correctly.
