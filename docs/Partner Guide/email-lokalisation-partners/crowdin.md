---
title: Crowdin
excerpt: Email Translation Partner
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

[Crowdin](https://crowdin.com/) is a platform that streamlines the translation and localization of digital content for multilingual support. Integrating CleverTap with Crowdin helps automate the translation of email templates. You can export templates from CleverTap to Crowdin for translation and then import them back. In this way, you can deliver personalized campaigns in your users' preferred languages, enhancing engagement and simplifying your localization process.

> 📘 Integration Availability
> 
> Currently, this feature is released in Public Beta. For more information about this integration or if you face any issue, contact [Crowdin Support](mailto:support@crowdin.com). This integration is exclusive to traditional email campaigns on CleverTap and currently, does not support AMP emails.

# Prerequisites

Ensure that you have the following:

- Crowdin account 
- CleverTap account

# Integrate CleverTap with Crowdin

To set up the CleverTap integration with your Crowdin account:

1. [Configure CleverTap on Crowdin Dashboard](doc:crowdin#configure-clevertap-on-crowdin-dashboard)
2. [Export, Translate, and Upload Email Templates to CleverTap](doc:crowdin#export-translate-and-upload-template-to-clevertap)

## Configure CleverTap on Crowdin Dashboard

Follow the steps to integrate CleverTap with Crowdin:

1. Select the **Integrations** tab and click **Add Integration**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4ce2003d2f4d30077ce8bd158c919bb4bf8ab64ac5ef1c5ec6eab45f6a16893-crowdin_14.png",
        "",
        "Install CleverTap 1"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Integration on Crowdin"
    }
  ]
}
[/block]


2. Search for CleverTap and click !![](<>)  icon to install it. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1fcb1de464bf433afbdfb7bd1f512c44d1782f545cc341074fdf1fd18abd5a09-Crowdin_13.png",
        "",
        "Install CleverTap 2"
      ],
      "align": "center",
      "border": true,
      "caption": "Install CleverTap "
    }
  ]
}
[/block]


3. Select the users that will be allowed to access the project
   - **All Project Members**: Select** All Project Members ** to grant access to all users who are part of the project.
   - **Custom Access**: Select **Custom Access** and click **Select Users** to specify which users or roles can access the project
4. Select the projects for which the users will have access and click **Install**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dde1b0731275794809d44d8a88a686ff0484e317ac589179e62aad3a8130a22e-crwodin_14.png",
        "",
        "Install CleverTap"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Install CleverTap"
    }
  ]
}
[/block]


Once installed, you will be redirected to the **Integrations** tab. 

3. Add the following details: 

- **Region**: Navigate to _Settings > Project _ from the CleverTap dashboard to select the appropriate API endpoint for your region. To identify your account’s region, refer to the table below:

| Region              | CleverTap Dashboard URL                           |
| :------------------ | :------------------------------------------------ |
| Indonesia           | <https://aps3.dashbaord.clevertap.com/login.html> |
| Europe (default)    | <https://eu1.dashboard.clevertap.com/login.html>  |
| India               | <https://in1.dashboard.clevertap.com/login.html>  |
| Middle East (UAE)   | <https://mec1.dashboard.clevertap.com/login.html> |
| Singapore           | <https://sg1.dashboard.clevertap.com/login.html>  |
| United States (U.S) | <https://us1.dashboard.clevertap.com/login.html>  |

- **Account ID **: Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard. 
- **Passcode**: Locate Passcode under _Settings_ > _Project_ from the CleverTap dashboard. To know more, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e47a55df28b7406305274ab6614439a90e0be53554811675a25da32b86e6ac0-crowdin_9.png",
        "",
        "Integrate CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate CleverTap"
    }
  ]
}
[/block]


# Export, Translate, and Upload Template to CleverTap

Follow these steps to export, translate, and upload your templates to CleverTap:

1. Click **Sync to Crowdin**  from the _Integrations_ tab to export the templates from CleverTap to Crowdin. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/081c5f3c20a75e2ddb31a4ce74dea56ca6b8174c66487e28a15697059d2f79ca-crowdin_2.png",
        "",
        "Sync Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Template"
    }
  ]
}
[/block]


Once the templates are synced, they appear on the left side. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70358d21e9b8007f9df4b2aa0b41e2024bf0f1e80dd586245ca5763289b3c00a-crowdin_24.png",
        "",
        "Synced Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Synced Template"
    }
  ]
}
[/block]


2. Select the _Dashboard_ tab, select the target language, and click **Go to Editor** and [translate the selected template](https://support.crowdin.com/ordering-professional-translations). 
3. Select the_ Integrations_ tab once the template is translated, select the template from the left side, and click  **Sync files to CleverTap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cced595be9d754c5623127ad9f57a91ad24979aad5465210cea5e43c1037382f-crowdin_8.png",
        "",
        "Sync Translated Template to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Translated Template to CleverTap"
    }
  ]
}
[/block]


For users with a Content Manager subscription to CleverTap, the exported translated templates from Crowdin will be found under _Content Manager > Templates > Email_. Each language will have its own separate template.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6ce9e6831bfb8a390500e7865add71c3828482e929d91bbbb191ba6d2af7148-crowdin_23.png",
        "",
        "Translated Templated - CMS"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Templated - CMS"
    }
  ]
}
[/block]


For users without a Content Manager subscription, the exported translated templates will appear under _Campaigns > + Campaigns > Emails > What Section > Saved Templates_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a077cb11ef98433bc9fda0a5d8bc0c88ddf8f0eb271d7202977854584f31fae2-crowdin_10.png",
        "",
        "Translated Template - Saved Template in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Template - Saved Template in Campaign"
    }
  ]
}
[/block]


# FAQs

Here are some frequently asked questions to help you with the integration process:

### Why are only base templates fetched from CleverTap to Crowdin?

Currently, only base templates are integrated, which limits the availability of translated templates.

### Why are translated templates not matching the Email with drag-and-drop base email templates?

Translating JSON to match the drag-and-drop template format presents challenges, leading CleverTap to store translated templates in HTML format instead.

### Why do translated templates include the locale present in the base template?

- The locale for the base template is not currently set, making it difficult to differentiate between the base locale and the translated locale.
- To streamline this, translated templates are created as "Base Template name\_{Locale}." These are considered child templates.
- When base templates are fetched and translated templates are pushed back, CleverTap updates child templates with the specified locale. For instance, a base template named _Welcome to the App_ with the locale _en_ will result in three templates upon translating to _fr_ and _es_: _Welcome to the App_en_, _Welcome to the App_fr_, and _Welcome to the App_es_.

### How can translated templates be used for sending email campaigns from CleverTap?

When creating an email campaign, the [By User Property](https://docs.clevertap.com/docs/create-message-email#by-user-property) option can be utilized to set the property to match the locale of the translated campaign.

### What happens if a translated email template currently in use is updated?

- When an email template from CleverTap CMS or saved templates is used in a campaign, separate instances are created for each send. This ensures personalization and localization are tailored to each email.
- Edits made to an existing template do not impact campaigns created with earlier versions of that template.
- Changes to the main email template in the CMS or saved templates do not retroactively apply to previously created or sent campaigns.
- New campaigns will utilize the updated template, while campaigns in draft or scheduled status require manual updates with the new version.