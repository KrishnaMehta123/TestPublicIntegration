---
title: Sheetlabs
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

[Sheetlabs](https://sheetlabs.com/) is a platform that turns Google Sheets or Excel files into easy-to-use, RESTful APIs. When integrated with CleverTap, it enables you to use a spreadsheet as a lightweight customer data source or content manager for campaigns.

With this integration, you can:

* Pull dynamic content (for example, messages, titles) into your CleverTap campaigns using Linked Content.
* Push user data from CleverTap into a Sheetlabs spreadsheet using Webhooks.

# Prerequisites for Integration

The following are the prerequisites for integrating Sheetlabs with CleverTap:

* Ensure you have a valid Sheetlabs account.
* Ensure you have a spreadsheet in either **Google Sheets** or in **CSV/Excel format**
* Ensure you have access to the CleverTap dashboard.

# Integrate Sheetlabs with CleverTap

The integration process involves the following three major steps:

1. [Create an API in Sheetlabs](doc:sheetlabs#create-an-api-in-sheetlabs)
2. [Configure Linked Content API](doc:sheetlabs#configure-linked-content-api).
3. [Create Personalized Campaign Using Linked Content](doc:sheetlabs#create-personalized-campaign-using-linked-content).

> 📘 Import Your Spreadsheet into Sheetlabs
>
> To use Sheetlabs as a content source, import your spreadsheet into Sheetlabs by uploading a CSV/Excel file or connecting your Google account to import a Google Sheet. You can optionally enable auto-sync to keep the data updated automatically.

## Create an API in Sheetlabs

To programmatically access your imported table data from Sheetlabs, you must create an API. This allows you to fetch data dynamically and use it across external tools or platforms. To do so, perform the following steps:

1. From API section of your Sheetlabs dashboard, click **+ New API**.
2. Select the *Data table* you just imported.

<Image alt="Create an API in Sheetlabs" align="center" width="75% " border={true} src="https://files.readme.io/d71c8b3ff2263793e5ca9956fe0aff6d9e2fa9c01a05ece26fb8bb8d2bdf5a1d-image.png">
  Create an API in Sheetlabs
</Image>

3. Name your API and optionally add a description.
4. Select *GET* as the method to fetch data.
5. Copy the **Base URL** for the API.

<Image alt="Copy Base URL" align="center" width="75% " border={true} src="https://files.readme.io/4b9255b6eaac7989faca0e89c1aa00cb861be9fa6ec5465e87091d2d8eef7e72-image.png">
  Copy Base URL
</Image>

## Configure Linked Content API

Set up Linked Content in CleverTap to connect your Sheetlabs API and retrieve dynamic campaign content using user profile parameters. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* in the CleverTap dashboard. 
2. Click **+ Linked Content**.

<Image alt="Add Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/a06da6f0b7efc54f86dc7cf9f2af6c8dcfa0fe4b529b000e9c71bfa6615ff3f3-image.png">
  Add Linked Content
</Image>

3. In the *URL* field, paste the **Base URL** copied in *Step 5* of [Create an API in Sheetlabs](doc:sheetlabs#create-an-api-in-sheetlabs), and append the parameter `ID={{id}}` to personalize the request.

#### Example:

```html
<BASE_URL_FROM_SHEETLABS>?ID={{id}}
```

In this example, `ID` is used to identify the user, and the corresponding `Title` and `Message` fields from the sheet will be used in the campaign. `ID` acts as the lookup parameter for fetching personalized content.

4. Click **Test Linked Content** to verify if the data is being correctly retrieved based on the `ID` provided from the linked Google Sheet.

#### Example API response:

```json
[
  {
    "ID": 1234,
    "Title": "Hey",
    "Message": "How have you been?",
    "Button": "Buy Now!"
  }
]
```

> 🚧 Auto-mapping
>
> Auto-mapping of objects and labels is not supported for this type of array-based response from the Sheetlabs API. You need to manually iterate through the JSON response using [Liquid tags](doc:personalize-message-all) to access specific values.

5. Click **Test and Save** to save this API.

<Image alt="Save Linked Content" align="center" width="45% " border={true} src="https://files.readme.io/2ce451f75d46a57624713c63a1533e9bdee811edab759c5367f5b57a2ae66b44-image.png">
  Save Linked Content
</Image>

Once the Sheetlabs data is available through Linked Content, you can use it in any CleverTap campaign that supports personalization, such as [Push Notifications](doc:create-message-push) or [Email Campaigns](doc:create-message-email).

## Create Personalized Campaign Using Linked Content

Use the Linked Content API inside a Push Notification campaign to personalize the message with Sheetlabs.

To do so, perform the following steps:

1. Go to *Campaigns*  from the CleverTap dashboard and click **+ Campaign**.

2. Select *Push Notification* from the *Messaging Channels* list.

3. Configure all the campaign settings and then go to the *What* section:
   1. Click **Personalization**. 
   2. Select the *Linked Content* configured under [Configure Linked Content API](doc:sheetlabs#configure-linked-content-api) and click **Apply**.

<Image alt="Personalization" align="center" border={true} src="https://files.readme.io/a3374c8a1e5bc30a31aa7a3a306e8af5223cd4605cae1af3d3fc8d4c420c545f-2025-05-09_19-59-27_1.gif">
  Personalization
</Image>

4. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid tag](doc:personalize-message-all).

<Image alt="Create Personalized Message Using Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/0e57df8c5ec77404ebfa2a5b5faecc58e9f458eb839a86c673b71ce81058613e-image.png">
  Create Personalized Message Using Linked Content
</Image>

5. Click **Preview and Test** to see if the campaign pushes the default values you configured. 
6. Click **Publish** to launch the campaign. Verify that everything works as intended. Users will receive a push notification like the one below.

<Image alt="Push Notifications" align="center" width="35% " border={true} src="https://files.readme.io/5ed6bac92131b5b8ad3e32d420439690fb3f096c0b0cddc995afb4494b09bafb-image.png">
  Push Notifications
</Image>

Similarly, you can apply this setup to other CleverTap campaigns using linked content, such as [Email](doc:create-message-email), [WhatsApp](doc:create-message-whatsapp), or [Web Push](doc:create-message-web-push).
