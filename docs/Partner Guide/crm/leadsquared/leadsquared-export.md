---
title: LeadSquared Export
excerpt: Learn how to export lead data from CleverTap to LeadSquared.
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

[LeadSquared](https://www.leadsquared.com) allows you to receive lead data from CleverTap, enabling automated lead capture and CRM updates in real time.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by LeadSquared. The CleverTap and LeadSquared integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [LeadSquared](mailto:support@leadsquared.com) for support and resolution.

# Export Lead Data from CleverTap to LeadSquared

To push lead data from CleverTap to LeadSquared using webhooks. To do so, follow these steps:

1. [Install the CleverTap Connector in LeadSquared](doc:leadsquared-export#install-the-clevertap-connector-in-leadsquared)
2. [Generate a Webhook URL in LeadSquared](doc:leadsquared-export#generate-a-webhook-url-in-leadsquared)
3. [Configure Webhook in CleverTap](doc:leadsquared-export#configure-webhook-in-clevertap)
4. [Create Webhook Campaign](doc:leadsquared-export#create-webhook-campaign)

## Install the CleverTap Connector in LeadSquared

Install the CleverTap connector to start capturing leads from CleverTap into LeadSquared. To do so, follow these steps:

1. Go to *Apps* > *Apps Marketplace* in LeadSquared.
2. Search for *CleverTap* and click **Install**.
3. After installation, click **Configure**.

<Image alt="Install the CleverTap Connector in LeadSquared" align="center" width="75% " border={true} src="https://files.readme.io/33343dd088913851a3134410a5324cded17641062df21da260f920755f288ea4-clevertap-install-20250108-104125.gif">
  Install the CleverTap Connector in LeadSquared
</Image>

4. Grant connector access by role or user-level settings:
   * *Based on Role*: Choose roles from the *Specify Roles* dropdown.
   * *Advanced (User Level)*: Select a user boolean field that controls access.

<Image alt="User-level settings" align="center" width="75% " border={true} src="https://files.readme.io/d7b4ab2fb5138724c7d27cb304404de3c9d88de4b294fdbcb0be461894a70c57-24a530cd-0416-482b-8302-20e0579ec61c.gif">
  User-level settings
</Image>

5. Click **Save Details** to apply settings.

> 📘 Note
>
> All Admin users have access to the connector by default.

## Generate a Webhook URL in LeadSquared

Generate a webhook URL in LeadSquared to push lead data into CleverTap. To do so, follow these steps: in LeadSquared that can be used to automate the data push into CleverTap.

1. Go to *Apps* > *CleverTap*.
2. Enter the following details:

| Property                                  | Description                                             |
| ----------------------------------------- | ------------------------------------------------------- |
| Lead Source                               | Define the lead source (for example, CleverTap).        |
| Default Country Code                      | Adds country code if missing in leads.                  |
| Select Time Zone                          | Aligns with your CleverTap account time zone.           |
| Lead Capture Search By Criteria           | Primary lead identifier (for example, email or mobile). |
| Lead Capture Secondary Search By Criteria | Fallback identifier if the primary fails.               |
| Select User to Notify on Failure          | Select the user who receives sync failure alerts.       |
| Enable Notification                       | Toggle to send failure alerts via email.                |

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/d385c2f0ad10c867d563e76efccbd4c67cad433cb958ff394266ff65d289a963-image.png" />

3. Configure *Entity Options* to define sync behavior:

   * *Capture (Create and Update existing)*
   * *Create only new record*
   * *Update only existing record*

<Image alt="Configure Entity Options" align="center" width="75% " border={true} src="https://files.readme.io/f2598854231f75bad51cb0cba8cf3b8b2ac61b61195306fc2346aa0f5419672a-image.png">
  Configure Entity Options
</Image>

4. On the *Mapping* screen:
   * Review auto-mapped CleverTap to LeadSquared fields.
   * To set default values, click the **edit** icon, enter value, and save.
   * Disable any fields not needed.
   * Use the search key icon to mark a unique identifier.
   * Add custom fields if required and map them accordingly.

<Image alt="Mapping" align="center" width="75% " border={true} src="https://files.readme.io/86da639eb053e49f656ae4b39eb8c3537041f2da30b8a4160b7ee79dca26547d-clevertap-lead-mapping-20250108-112803.gif">
  Mapping
</Image>

5. Click **Save & Next** to generate the webhook URL.
6. Copy the webhook URL for use in CleverTap.
7. Go to *More Actions* > *Enable Sync Job* to activate data flow.

<Image alt="Copy Webhook URL" align="center" width="75% " border={true} src="https://files.readme.io/bc6f02cbccd70fd6dd4ad81fb92cda36ba03a48ca3c54c632bcd3c4578981ecf-e9ea505e-234f-4074-ace8-ec8d1da41648.gif">
  Copy Webhook URL
</Image>

> 📘 Note
>
> To view job history, Go to *More Actions* > *View Logs*.

## Configure Webhook in CleverTap

To enable real-time lead capture, create and configure the CleverTap webhook using the URL generated in LeadSquared. To do so, follow these steps:

1. Go to *Settings* > *Channels* > *Webhook* in the CleverTap dashboard.
2. Click **+ Add Webhook**.
3. Enter the following configuration:

| Field          | Value                                                                                                                                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Name           | Enter a unique nickname for your webhook (for example, LeadSquared)                                                                        |
| HTTP Method    | `POST`                                                                                                                                     |
| Endpoint URL   | Paste the URL copied in *step 6* of [Generate a Webhook URL in LeadSquared](doc:leadsquared-export#generate-a-webhook-url-in-leadsquared). |
| Authentication | Select `No Authentication`.                                                                                                                |
| Headers        | Add a Key/Value pair to the events that trigger this webhook.                                                                              |

<Image alt="Configure Webhook in CleverTap" align="center" width="45% " border={true} src="https://files.readme.io/d778ff148e399a594bd0660309ca2510d5b7597019cec978391ba4a78a255042-image.png">
  Configure Webhook in CleverTap
</Image>

4. Click **Save** to validate the configuration.

Once saved and tested successfully, the webhook can export lead data from CleverTap to LeadSquared.

## Create Webhook Campaign

After configuring your webhook in CleverTap, you must create a campaign that triggers the webhook and sends data to LeadSquared. To do so, follow these steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Webhook* from the list of messaging channels.
2. Under the *What* section, select the Webhook created in the [Configure Webhook in CleverTap](doc:leadsquared-export#configure-webhook-in-clevertap) section.
   * Select **JSON** as the content format.
   * Select **Custom Body**.

<Image alt="Webhook Content" align="center" width="75% " border={true} src="https://files.readme.io/ecb2568f744869aad55de0a83e8464e50ff5a3440212253f0e2b01b582af2bdd-image.png">
  Webhook Content
</Image>

3. In the **Webhook Content**, paste the following sample payload:

```json
{
  "RelatedProspectId": "{{ Profile.Identity | default: 'NULL' }}",
  "ActivityEvent": 201,
  "ActivityNote": "Lead has read the email at {{ Profile.data | default: '0' }} tracked via CleverTap",
  "ActivityDateTime": "{{ Profile.purchase_date | default: '0' }}",
  "Fields": [
    {
      "SchemaName": "Platform",
      "Value": "Email"
    },
    {
      "SchemaName": "mx_Custom_2",
      "Value": "{{ Profile.QualtricID | default: 'N/A' }}"
    },
    {
      "SchemaName": "mx_Custom_3",
      "Value": "custom_value"
    }
  ]
}
```

You can dynamically personalize values using [Liquid tags](doc:personalize-message-all#liquid-tags) (`{{ }}`). For example, `{{ Profile.Identity }}` picks the LeadSquared prospect ID of the user, and `{{ Profile.purchase_date }}` dynamically fills in the user’s last purchase date.

4. Click **Preview and Test** to validate the payload and campaign behavior.
5. If everything works as expected, click **Publish**.

Once launched, CleverTap will trigger the webhook to LeadSquared when the specified event and audience conditions are met, ensuring real-time data sync.
