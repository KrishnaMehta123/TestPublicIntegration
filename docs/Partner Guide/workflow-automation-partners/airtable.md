---
title: Airtable
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

[Airtable](https://airtable.com) is an intuitive platform for building and sharing relational databases online. With the CleverTap and Airtable integration, you can automatically send user data and event details from CleverTap to Airtable using webhook campaigns.

This integration allows you to:

* Store CleverTap user data centrally in Airtable.
* Automate data transfer via Webhook campaigns.
* Enrich external databases for further analysis or processing.

# Prerequisites for Integration

To integrate Airtable with CleverTap, ensure the following prerequisites are met:

* Access to your Airtable dashboard and ability to create API tokens
* Access to your CleverTap dashboard with permissions to configure webhooks and campaigns
* Airtable Base and Table IDs available for the integration

# Integrate Airtable with CleverTap

The integration process involves the following three major steps:

1. [Generate Airtable API Token](doc:airtable#generate-airtable-api-token)
2. [Set Up Webhook in CleverTap](doc:airtable#set-up-webhook-in-clevertap)
3. [Create a Webhook Campaign in CleverTap](doc:airtable#create-a-webhook-campaign-in-clevertap)

## Generate Airtable API Token

Generate a secure access token from your Airtable account, which will be used to authorize CleverTap API calls. To do so, follow these steps:

1. Log in to your [Airtable account](https://airtable.com/account).
2. Click on your *Profile* > *Builder Hub* or visit `https://airtable.com/create/token`.
3. Click **Create token**.
4. Assign a token name and enable the following scope:

   * `data.records:write`: Create, edit, or delete records using API.
5. Define *Access* based on your Airtable workspace requirements.
6. Click **Create token** and copy the token. Airtable will not display it again.

<Image alt="Generate Airtable API Token" align="center" width="65% " border={true} src="https://files.readme.io/74cda9fe9289d6e014578195e5696598dd52c698d31302c497ba62d0eb120336-image.png">
  Generate Airtable API Token
</Image>

> 🚧 Note
>
> This token must be included in the authorization header for every CleverTap webhook call.

To understand more about Airtable's supported authentication methods, refer to the [Airtable Authentication](https://airtable.com/developers/web/api/authentication).

## Set Up Webhook in CleverTap

To begin the integration, you will first create a webhook in CleverTap. This webhook sends recipient and campaign-specific data to Airtable whenever the campaign is triggered. It ensures real-time delivery of user profile data to your Airtable base based on campaign actions.

To do so, follow these steps:

1. Go to *Settings* > *Channels* > *Webhook*.
2. Click **+ Add Webhook** and enter the following:

| Field        | Value                                                  |
| ------------ | ------------------------------------------------------ |
| Name         | Airtable                                               |
| HTTP Method  | `POST`                                                 |
| Endpoint URL | `https://api.airtable.com/v0/{baseId}/{tableIdOrName}` |

> 📘 Retrieve your `baseId` and `tableIdOrName` from the Airtable URL.
>
> * Base ID starts with `app`
> * Table ID starts with `tbl`
> * View IDs starts with `viw`

3. Add the following key-value pair under *Headers*:

| Key           | Value                         |
| ------------- | ----------------------------- |
| Authorization | `Bearer <Airtable API Token>` |
| Content-Type  | `application/json`            |

<Image alt="Create Webhook" align="center" width="55% " border={true} src="https://files.readme.io/daad6532a73c1782054774b9d0a4b9927179df74923104ea0e65e54d527122ff-image.png">
  Create Webhook
</Image>

4. Click **Save** to create the webhook.

After saving the webhook, CleverTap will be ready to send user profile data directly to Airtable.

## Create a Webhook Campaign in CleverTap

Design and launch a webhook campaign in CleverTap to dynamically push selected user data to Airtable.

To do so, follow these steps:

1. Go to *Campaigns* > *+ Campaign* > *Webhook*.
2. Select the Webhook configured in [Set Up Webhook in CleverTap](doc:airtable#set-up-webhook-in-clevertap).
3. In the *What* section, under the *Webhook Content* section, select the *Content Format* as JSON and click the **Custom body** option.
4. Paste the following JSON payload:

```json
{
   "records": [
     {
       "fields": {
         "Name": "{{ Profile.name | default: "-" }}",
         "Email": "{{ Profile.Email | default: "test@clevertap.com" }}"
       }
     }
   ]
}
```

> ⚠️ Important
>
> Ensure that the field names used in your payload (for example, Name, Email) exactly match the column names in your Airtable table. If the fields don't match, data will not be recorded.
>
> You can customize the payload to align with your table structure. Learn more about [Airtable request fields](https://airtable.com/developers/web/api/create-records#request-fields).

Use the personalization toolbar (`{`, `{{`, or `@`) to insert dynamic user profile values.

5. Click **Preview and Test** to validate the integration.

<Image alt="Preview and Test" align="center" width="65% " border={true} src="https://files.readme.io/3e0e836c4f773875008b1ffda49c92e687036a7b12c9be47cef246a09149c558-image.png">
  Preview and Test
</Image>

6. Open your Airtable base and verify that a new row has been created with the test data (for example, Name, Email).

<Image alt="Test entry successfully reflected in Airtable" align="center" width="65% " border={true} src="https://files.readme.io/dc42baa587a027785b71a6f956a9c926ee44bb0d66f9924b82c581ed4fea5a43-image.png">
  Test entry successfully reflected in Airtable
</Image>

7. Once confirmed, click **Publish** in CleverTap.

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/9199ed42c3d23f43d88e2e6fd042f2fa0fee0bb13221abf58885c34521060636-image.png" />

Integrating Airtable with CleverTap allows you to streamline your data operations and centralize analytics across platforms.
