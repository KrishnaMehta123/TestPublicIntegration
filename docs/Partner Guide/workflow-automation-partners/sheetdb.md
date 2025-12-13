---
title: SheetDB
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

[SheetDB](https://sheetdb.io/) turns a Google Spreadsheet into a RESTful JSON API. It enables you to use spreadsheets as dynamic data sources that can be read from or written to in real time.

With this integration, you can:

* Pull dynamic content (for example, titles, messages) into your CleverTap campaigns using Linked Content.
* Push user data from CleverTap into a Google Sheet via Webhook campaigns.

## Prerequisites for Integration

The following are the prerequisites for SheetDB:

* Ensure you have a valid SheetDB account.
* Ensure your spreadsheet has column headers such as `ID`, `Title`, `Message`, and `Button`.
* Ensure you have access to the CleverTap dashboard.

# Integration Overview

The integration process involves the following three major steps:

1. [Create an API in SheetDB](doc:sheetdb#create-an-api-in-sheetdb)
2. [Configure the Linked Content API](doc:sheetdb#configure-the-linked-content-api)
3. [Create a Personalized Campaign Using Linked Content](doc:sheetdb#create-a-personalized-campaign-using-linked-content)

> 📘 Import Your Spreadsheet into SheetDB
>
> To begin, connect a Google Sheet or upload a new one in the SheetDB dashboard. Your spreadsheet should include headers such as `ID`, `Title`, and `Message` for use in CleverTap campaigns.

## Create an API in SheetDB

1. Log in to your SheetDB dashboard and click **+ Create New API**.

2. Select your source:
   * *Existing spreadsheet*
   * *Create new spreadsheet*
   * *Create new spreadsheet JSON*

<Image alt="Select Source" align="center" width="75% " border={true} src="https://files.readme.io/0f042798072802b793ec8e2363660205ed93a7455b98e99c88b16ab24405dcd5-image.png">
  Select Source
</Image>

3. Paste the Google Sheet URL to generate the API for your spreadsheet.

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/03c444a48910b34cb5c65708ebd9f7a8bf13f478dfb43872ac48bc6c4fa550d8-Screen_Recording_2025-02-05_at_2.43.41_PM_1.gif" />

4. Once setup is complete, copy the generated **API URL** for your spreadsheet.

## Configure the Linked Content API

Set up Linked Content in CleverTap to connect your SheetDB API and retrieve dynamic campaign content using user profile parameters.

1. Go to *Settings* > *Setup* > *Linked Content* in the CleverTap dashboard. Click **+ Linked Content**.

<Image alt="Add Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/a06da6f0b7efc54f86dc7cf9f2af6c8dcfa0fe4b529b000e9c71bfa6615ff3f3-image.png">
  Add Linked Content
</Image>

2. In the **URL** field, paste the **API URL** copied in the previous step, and append the filter query using a profile parameter:

```
https://sheetdb.io/api/v1/<API KEY>/search?ID={{id}}&single_object=true
```

In this example, `ID` is used to identify the user from the spreadsheet based on their CleverTap `Identity`.

3. Click **Test Linked Content** and enter a sample ID to preview the response.

### Example Response

```json
{
  "ID": "1234",
  "Titile": "Hey",
  "Message": "How are you been?",
  "Button": "Buy Now!"
}
```

4. Click **Auto-Fill Objects with Response** to automatically map the fields from the API response to custom labels, as shown below.

<Image alt="Auto-Fill Objects with Response" align="center" width="75% " border={true} src="https://files.readme.io/c00a87fdc168e43428afcfd060fb01be047b7f3b09f02100c7f4ce10a6f8bdc6-image.png">
  Auto-Fill Objects with Response
</Image>

5. Click **Test and Save** to save this API.

<Image alt="Save Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/2ce451f75d46a57624713c63a1533e9bdee811edab759c5367f5b57a2ae66b44-image.png">
  Save Linked Content
</Image>

Once the SheetDB data is available through Linked Content, you can use it in any CleverTap campaign that supports personalization, such as [Push Notifications](doc:create-message-push) or [Email Campaigns](doc:create-message-email).

## Create a Personalized Campaign Using Linked Content

Use the Linked Content API inside a Push Notification campaign to personalize the message with SheetDB.

To do so, perform the following steps:

1. Go to *Campaigns* from the CleverTap dashboard and click **+ Campaign**.
2. Select *Push Notification* from the Messaging Channels list.
3. Configure all the campaign settings and then go to the *What* section:
   1. Click **Personalization**
   2. Select the *Linked Content* configured under [Configure the Linked Content API](doc:sheetdb#configure-the-linked-content-api) and click **Apply**.

<Image alt="Personalization" align="center" border={true} src="https://files.readme.io/a3374c8a1e5bc30a31aa7a3a306e8af5223cd4605cae1af3d3fc8d4c420c545f-2025-05-09_19-59-27_1.gif">
  Personalization
</Image>

4. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid tag](doc:personalize-message-all).

<Image alt="Create Personalized Message Using Linked Content" align="center" border={true} src="https://files.readme.io/6d72365caee91c86624e70cc6a2c9263e5fda1c9879c16cc566c6f0b07b8bc4c-image.png">
  Create Personalized Message Using Linked Content
</Image>

5. Click **Preview & Test** to see if the campaign pushes the default values you configured.
6. Click **Publish** to launch the campaign. Verify that everything works as intended. Users will receive a push notification like the one below.

<Image alt="Push Notifications" align="center" width="45% " border={true} src="https://files.readme.io/603907b0cec1fd9e727345df285791fea6588734f8449e407ece8501442ee94d-image.png">
  Push Notifications
</Image>

Similarly, you can apply this setup to other CleverTap campaigns using linked content, such as [Email](doc:create-message-email), [Web Push](doc:create-message-web-push).
