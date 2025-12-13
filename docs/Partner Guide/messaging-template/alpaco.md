---
title: Alpaco
excerpt: Email Templates
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

[Alpaco](https://alpaco.email/) is a powerful email design platform that helps marketing teams create responsive, on-brand email templates. Integrating Alpaco with CleverTap allows you to design email templates in Alpaco and seamlessly export them to CleverTap for automated targeted customer engagement.

With this integration, you can:

* Design responsive [email templates](https://documentation.alpaco.email/template/base) in Alpaco and import them into CleverTap for personalized customer interactions.
* Automate email delivery based on customer actions such as sign-ups, purchases, or abandoned carts.
* Re-engage users with targeted campaigns using dynamic templates created in Alpaco.

> 🚧 Support For Integration
>
> This integration is managed and continuously improved by Alpaco. The CleverTap and Alpaco integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Alpaco](mailto:hello@alpaco.email) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

* Ensure you have an Alpaco account.
* Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Alpaco with CleverTap

The integration process involves the following three steps:

1. [Configure Alpaco Dashboard](doc:alpaco#configure-alpaco-dashboard).
2. [Export Email Template to CleverTap](doc:alpaco#export-email-template-to-clevertap).
3. [Create a CleverTap Campaign Using Alpaco Template](doc:alpaco#create-a-clevertap-campaign-using-alpaco-template).

## Configure Alpaco Dashboard

Add CleverTap credentials on the Alpaco dashboard:

> 📘 Note
>
> Currently, only **[Alpaco Support](mailto:hello@alpaco.email)** can create new ESP connection.

### Request CleverTap Integration to Alpaco

To integrate CleverTap with Alpaco, send a request to the [Alpaco Support team](mailto:hello@alpaco.email) with the following CleverTap credentials:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under *Settings* > *Project* from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under *Settings* > *Project* from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate *Region* for the API endpoint you want to select under *Settings* > *Project*. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

Once the Alpaco team adds the integration with your CleverTap credentials, proceed with the following steps to configure the connection in the Alpaco dashboard.

1. Go to *the Integration* card in the lower right corner and click the edit icon ![Edit Icon](https://files.readme.io/7b1f6d0b5bdb305c353eda57953fc8a0f214786b757d83a7ed5bd015e5715680-2025-02-18_00-34-22.png) next to the ESP connection that has been set up for you.

<Image alt="ESP connection on Alpaco dashboard" align="center" width="65% " border={true} src="https://files.readme.io/cd0cb25ed1158fb2276d2f8516340163b1d9a7744e64b6ff719decb64540f209-image.png">
  ESP Connection on Alpaco Dashboard
</Image>

2. Select *CleverTap* from the *ESP Integration* dropdown.
3. Enter the same CleverTap **Account ID**, **Passcode**, and **Region** details that were sent in the request to Alpaco Support (these must match the credentials you provided).

<Image alt="Connect CleverTap to Alpaco" align="center" width="65% " border={true} src="https://files.readme.io/27a28127cacd5d98bd9481d340ad49ad96db16754b784ba18e318da647bfe78f-image.png">
  Connect CleverTap to Alpaco
</Image>

4. Click **Save** to connect CleverTap as an ESP connection.

### Set Up Personalization

CleverTap supports personalization using [Liquid tags](https://docs.clevertap.com/docs/personalize-message-all#liquid-tags). To use Liquid tags for personalization in CleverTap, you must first set up personalization in Alpaco. To do so, refer to [Alpaco Merge Tags](https://documentation.alpaco.email/account-settings/merge-tags).

<Image alt="Personalization using Liquid tags in Alpaco" align="center" width="65% " border={true} src="https://files.readme.io/545b0f726d1e24ee4a5dad7c72520f72dc25100b4d4178c9ff88b1ba9181360e-image.png">
  Personalization using Liquid tags in Alpaco
</Image>

## Export Email Template to CleverTap

After [setting up the template](https://documentation.alpaco.email/template/base) on Alpaco, you can export the email templates to CleverTap:

1. Click **Export** in the top navigation bar and select *CleverTap* from the export options.

<Image alt="Export Email Template to CleverTap" align="center" width="65% " border={true} src="https://files.readme.io/55fea5bce91f3a6ba84344732783e4ca328c9cbff229206b9d7b3ff4be9c1090-image.png">
  Export Email Template to CleverTap
</Image>

2. Select ESP connection as CleverTap.
3. Click **Export** to import the template in CleverTap.

## Create a CleverTap Campaign Using Alpaco Template

To create an email campaign on CleverTap using the Alpaco for Email template, follow these steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Email* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section and select *Saved Templates*.

> 📘 Update Email Templates in CleverTap
>
> If you make any changes to email templates in Alpaco, they will not automatically reflect in the *Saved Templates* on the CleverTap dashboard. To update the template in CleverTap, you must re-export it from Alpaco into CleverTap.

3. Select the template you imported from Alpaco.

<Image alt="Email Template - Saved Template in Campaign" align="center" width="65% " border={true} src="https://files.readme.io/70cbf0aee337c1d307e61bdd4dd28eae4a3d2c0841f061bfe60065a8ceb3502d-image.png">
  CleverTap Saved Email Templates
</Image>

Once you [create an email campaign](https://docs.clevertap.com/docs/create-message-email) on the CleverTap dashboard, publish the campaign.

# FAQs

### Can I edit an email template in CleverTap after exporting it from Alpaco?

Yes, you can edit the template in CleverTap, but we do not recommend it. CleverTap does not sync changes back to Alpaco. To keep both versions updated, edit the template in Alpaco and re-export it to CleverTap.

### Will editing a template in CleverTap affect the original in Alpaco?

No, changes made in CleverTap do not affect the original template in Alpaco.

### If I make changes to the template in Alpaco after exporting it to CleverTap, will it automatically update in CleverTap?

No, changes made to a template in Alpaco after exporting it to CleverTap will not automatically reflect in CleverTap. You must re-export the updated template from Alpaco to update it in CleverTap.
