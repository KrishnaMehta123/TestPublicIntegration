---
title: FreshSales
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

[Freshsales](https://www.freshworks.com/crm/sales/) is a widely used Customer Relationship Management (CRM) platform that supports sales, marketing, and support teams by leveraging cloud technology to connect more efficiently with customers, partners, and prospects.

Integrating CleverTap with Freshsales helps you sync CRM data into CleverTap for personalized, event-driven engagement. With this integration, you can:

- Onboard new leads with product tour messages.
- Re-engage lost deals with targeted feature updates.
- Move leads down the funnel with timely nudges.
- Convert high-intent leads with automated follow-ups.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- A valid Freshsales account.
- A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Freshsales with CleverTap

To sync data from a Freshsales module (such as Contacts, Accounts, or Deals) to CleverTap, perform the following three major steps:

1. [Create Workflow in Freshsales](doc:freshsales#create-workflow-in-freshsales).
2. [Set Up Webhook with CleverTap APIs](doc:freshsales#set-up-webhook-with-clevertap-apis).
3. [Test and Activate Workflow](doc:freshsales#test-and-activate-workflow).

## Create Workflow in Freshsales

Consider a use case where a SaaS business wants to send automated product tour campaigns to new leads created in Freshsales. When a lead is created or updated in Freshsales, the information should be synced to CleverTap, triggering a welcome campaign.

To create a new Freshsales workflow, define which data should be synced as follows:

1. Log in to your Freshsales CRM account.
2. Go to _Admin Settings_ > _Term & Territories_ and select _Workflows_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d8bc7a7d630f9b5cf3f84edd7cbfa3b4e9c47a4fb547beba77a77979df93514-Screen_Recording_2025-06-23_at_3.39.17_PM_1.gif",
        "",
        "Create a new workflow in Admin Settings."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create a new workflow in Admin Settings"
    }
  ]
}
[/block]


3. Click **Create Workflow** and select the required Freshsales module (in this example, Contacts) to be synced with CleverTap.
   > 📘 Note
   > 
   > Freshsales supports one module per workflow. Create individual workflows for each additional module.
4. Select the **Contacts** module to track new or updated leads.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72f98253919987e987cf447a270d3490e9675928036aa007ce69c5f4ee88388e-image.png",
        null,
        "Select the Contacts module to sync leads."
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select Contacts Module to Sync Leads."
    }
  ]
}
[/block]


5. Under _When to trigger this workflow?_, define the trigger conditions when the workflow should run: 
   1. Define the _Trigger_ when Contact is created or updated.
   2. Define the intervals when the workflow should **Run**.
6. (Optional) Add a filter to sync only relevant records (for example, _Lead Status_ is New ). This ensures the sync only occurs for relevant leads.
7. Under _What actions should be executed?_, select _Trigger Webhook_. This action will send contact data to CleverTap when the trigger conditions are met.

In the next step, you will configure this webhook to call CleverTap’s API with the right authentication and payload.

## Set Up Webhook with CleverTap APIs

Use CleverTap’s API to configure the webhook to push data from Freshsales to CleverTap. In the Freshsales dashboard. To do so, perform the following steps:

1. In _Trigger Webhook_, select the _Advanced_ option.
2. Enter the CleverTap's API endpoint used for uploading data to CleverTap. For more information, refer to [Upload User Profiles API](https://developer.clevertap.com/docs/upload-user-profiles-api) or [Upload Events API](https://developer.clevertap.com/docs/upload-events-api).

```
https://<RegionValue>.api.clevertap.com/1/upload
```

3. Set method to `POST` and the encoding format to `JSON`.
4. In the _Custom Headers_ section, add the following:

| Key                      | Value                     |
| ------------------------ | ------------------------- |
| `X-CleverTap-Account-Id` | Your CleverTap Account ID |
| `X-CleverTap-Passcode`   | Your CleverTap Passcode   |
| `Content-Type`           | `application/json`        |

6. Using _ Insert Placeholder _, map Freshsales fields (such as first name, email, and phone number) to the payload.
7. After you map the fields, define the payload using the [Example payload](doc:freshsales#example-payload) or [Advanced Example Payload (User Preferences & Subscriptions)](doc:freshsales#advanced-example-payload).

After mapping and pasting the payload, you can test this webhook (optional but strongly recommended).

### Example Payload

Use this basic payload structure to upload a user profile from Freshsales to CleverTap. Using dynamic placeholders, it maps common fields such as name, email, and phone.

```json
{
  "d": [
    {
      "objectId": "{{email}}",
      "type": "profile",
      "profileData": {
        "Name": "{{first_name}}",
        "Email": "{{email}}",
        "Phone": "{{phone_number}}",
        "Lead Source": "{{lead_source}}"
      }
    }
  ]
}
```

### Advanced Example Payload

This extended payload includes user messaging preferences (DND flags), subscription categories, and a dynamic date of birth field. Use this format if you are managing advanced profile attributes in CleverTap.

```json
{
  "d": [
    {
      "objectId": "{{email}}",
      "type": "profile",
      "profileData": {
        "MSG-dndPhone": true,
        "MSG-dndEmail": true,
        "category-unsubscribe": {
          "email": ["Newsletters", "Promotions"]
        },
        "category-resubscribe": {
          "email": ["Football", "Movies"]
        },
        "DOB": "{{dob_timestamp}}"
      }
    }
  ]
}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db66ad7430d9f46a76eff295f083acae2994c43484b734a1689ba2f60ed48023-image.png",
        null,
        "Configure Webhook"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure Webhook"
    }
  ]
}
[/block]


## Test and Activate Workflow

Verify that the webhook is correctly set up and that CleverTap receives the data as expected.

1. In the Freshsales dashboard, click **Test this Webhook**.
2. In the CleverTap dashboard, verify that a new user profile has been created.
3. Once testing is complete, click **Save** in Freshsales to activate the workflow.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50d331e68921316ecf5fa49d275220cdd0dd912a1129f25a4c383a9e27698aa5-image.png",
        null,
        "Verify Data in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify Data in CleverTap"
    }
  ]
}
[/block]


Once activated, the configured Freshsales workflow sends lead and contact data to CleverTap whenever the trigger conditions are met. This data can be used to trigger campaigns, update user profiles, and power targeted engagement.