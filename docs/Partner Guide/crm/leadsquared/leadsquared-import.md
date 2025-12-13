---
title: LeadSquared Import
excerpt: Learn how to import lead data from LeadSquared to CleverTap.
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

[LeadSquared](https://www.leadsquared.com) lets you export lead data into CleverTap, enabling automated journey triggers and enriched user profiles.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by LeadSquared. The CleverTap and LeadSquared integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [LeadSquared](mailto:support@leadsquared.com) for support and resolution.

# Import Lead Data from LeadSquared to CleverTap

To automate pushing lead data from LeadSquared into CleverTap. To do so, follow these steps:

1. [Install the Push Data to CleverTap Connector](doc:leadsquared-import#install-the-push-data-to-clevertap-connector)
2. [Generate a Webhook URL in LeadSquared](doc:leadsquared-import#generate-a-webhook-url-in-leadsquared)
3. [Create Automation in LeadSquared](doc:leadsquared-import#create-automation-in-leadsquared)

## Install the Push Data to CleverTap Connector

Install the Push Data to CleverTap connector to send lead data from LeadSquared. To do so, follow these steps:

1. Go to *Apps* > *Apps Marketplace* in LeadSquared.
2. Search for *Push Data to CleverTap* and click **Install**.
3. Click **Configure** and set access:

   * By user roles or advanced user-level logic.

<Image alt="User-level settings" align="center" width="75% " border={true} src="https://files.readme.io/f1ae8f98942673fb33fafe0ed79d60e1e85a077b09d4e50a9ced633585e3dc7f-950fcaf0-349c-42d3-9b47-9121cf96aebb.gif">
  User-level settings
</Image>

4. Click **Save Details**.

## Generate a Webhook URL in LeadSquared

Generate a webhook URL in LeadSquared to send lead data to CleverTap during automated workflows. To do so, follow these steps:

1. Go to *Apps* > *Push Data to CleverTap*.

<Image alt="Push Data to CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/62628a60b3492df7c6b5f9c6331ad62b5303f53e1db531ececc0888905a75eda-d0840152-8197-4b77-b7fd-74a2d465cbe4.gif">
  Push Data to CleverTap
</Image>

2. Configure basic settings:

| Property                  | Description                                                                                                                                                                                                    |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CleverTap Account ID      | Locate the Project ID under *Settings* > *Project* from the CleverTap dashboard.                                                                                                                               |
| CleverTap Passcode        | Locate the Passcode under *Settings* > *Project* from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode). |
| Lead Source               | Origin of leads (for example, email campaign).                                                                                                                                                                 |
| Unique Search Criteria    | Key identifier for de-duplication.                                                                                                                                                                             |
| Default Country Code      | Default country prefix for phone numbers.                                                                                                                                                                      |
| User to Notify on Failure | Contact for sync issues.                                                                                                                                                                                       |
| Enable Notification       | Enable email alerts.                                                                                                                                                                                           |

3. Click **Save & Next**.
4. On the **Mapping** screen:

   * Review and update default mappings.
   * Set defaults where necessary.
   * Mark key fields and add custom ones if required.
5. Click **Save & Next**.
6. Copy the generated webhook URL.

> 📘 Note
>
> Sync behavior is set to "*Do Nothing*" by default. It is recommended not to change it.

7. Go to *More Actions* > *Enable Sync Job* to start data flow.

## Create Automation in LeadSquared

Set up automation workflows in LeadSquared to sync leads with CleverTap based on triggers. To do so, follow these steps:

1. Go to *Workflow* > *Automation*.
2. Create a new automation and set a trigger (for example, *New Lead*).
3. Add a *Webhook* action and enter the following details:

| Field             | Description                                                                                                                                                                  |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name              | For example, "CleverTap Lead Verification"                                                                                                                                   |
| URL               | Paste the URL copied in *Step 6* of [Generate a Webhook URL in LeadSquared](doc:leadsquared-import#generate-a-webhook-url-in-leadsquared). (remove `https://` if instructed) |
| Content Type      | `application/json`                                                                                                                                                           |
| Save Response     | Optional                                                                                                                                                                     |
| Notify on Failure | Select the user to notify                                                                                                                                                    |
| Retry Count       | Set the number of retry attempts                                                                                                                                             |

<Image alt="Create Automation in LeadSquared" align="center" width="75% " border={true} src="https://files.readme.io/cafa8c56cbfc303a4aa63f94bf804a38585e6ed913e79c5d5ebc52140f5a7160-e67f9d6f-9ed7-476e-837f-eb5555485ff9.gif">
  Create Automation in LeadSquared
</Image>

4. Click **Save** and **Publish**.

Once published, the automation will ensure that lead data is pushed from LeadSquared to CleverTap based on the configured trigger.
