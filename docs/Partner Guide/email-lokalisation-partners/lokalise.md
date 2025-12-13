---
title: Lokalise
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

[Lokalise ](https://lokalise.com/) is a platform that streamlines the translation and localization of digital content for multilingual support. Integrate CleverTap with Lokalise to automate the translation of email templates. By exporting templates from CleverTap to Lokalise for translation and then importing them back, you can deliver personalized campaigns in your users' preferred languages, enhancing engagement and streamlining your localization process.

# Prerequisites for Integration

Ensure that you have the following:

- Lokalise account 
- CleverTap account

# Integrate CleverTap with Lokalise

To set up the CleverTap integration with your Lokalise account:

1. Set Up Project with CleverTap App on Lokalise Dashboard
2. Get Email Templates from CleverTap and push back translated templates to CleverTap
3. Find Translated Email templates in CleverTap

# Set Up Project with CleverTap App on Lokalise Dashboard

1. Navigate to _Project > New Project_ and select **Marketing and support**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de416561d68967244d3eb788d598daab4fc9534fdb8a31803b601c8a512fd330-Lokalise_2.png",
        "",
        "Marketing and support"
      ],
      "align": "center",
      "border": true,
      "caption": "Marketing and support"
    }
  ]
}
[/block]


2. Add information in the following fields:

- **Project Name**: Add a name for the project.
- **Base language**: Select the language in which the emails have been created from the drop-down menu.
- **Target languages**: Select the languages in which the created emails need to be translated from the drop-down menu.
- **Select content integration**: Select **CleverTap** from the drop-down menu.

3. Click on **Create Project**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8de124f468b3d3d0f3129ed39283dd1df5cc0b23c3c31449c68c5a3e770f7d9b-CleverTap_23.png",
        "",
        "Create Project - Lokalise"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Create Project - Lokalise"
    }
  ]
}
[/block]


4. Enter the following details:

- **Account ID **: Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.
- **Passcode**: Locate Passcode under _Settings_ > _Project_ from the CleverTap dashboard. To know more, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
- **Region**: Locate Region for the API endpoint you want to select under _Settings_ > _Project_ from the CleverTap dashboard. To identify the region for your account, refer to the following table:

| Region              | CleverTap Dashboard URL                           |
| :------------------ | :------------------------------------------------ |
| Indonesia           | <https://aps3.dashbaord.clevertap.com/login.html> |
| Europe (default)    | <https://eu1.dashboard.clevertap.com/login.html>  |
| India               | <https://in1.dashboard.clevertap.com/login.html>  |
| Middle East (UAE)   | <https://mec1.dashboard.clevertap.com/login.html> |
| Singapore           | <https://sg1.dashboard.clevertap.com/login.html>  |
| United States (U.S) | <https://us1.dashboard.clevertap.com/login.html>  |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6907e7-Taxi_Project_ID.png",
        "Project ID and Region",
        "Locate Project ID and Region on CleverTap Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Locate Project ID and Region on CleverTap Dashboard"
    }
  ]
}
[/block]


5. Click on **Authorize**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7c297451b073f564bf149757d7ec490501daa6688ac9d66a193e4276eb0a520-Lokalise_15.png",
        "",
        "Account ID, Passcode and Region"
      ],
      "align": "center",
      "border": true,
      "caption": "Account ID, Passcode and Region"
    }
  ]
}
[/block]


# Get Email Templates from CleverTap and push back translated templates to CleverTap

1. Navigate to _Content Management_  and all the templates under _Content Manager > Templates > Email_ from the CleverTap dashboard will be imported to Lokalise. Click on **Refresh** if any changes are made to the templates on the CleverTap Dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4daec4fabac58dc7ba8f9c63d1fca76f61e6db69c9648f54e2f42ec858cede81-Lokalise_19.png",
        "",
        "Import from CleverTap and Refresh"
      ],
      "align": "center",
      "border": true,
      "caption": "Import from CleverTap and Refresh"
    }
  ]
}
[/block]


6. Select the template that needs to be translated, and click on **Import from CleverTap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf80cf3b3b84f0957224dcc3ce7f18964d35ebb070e1dc3a3c09194c72c2bac0-Lokalise_20.png",
        "",
        "Import from CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Import from CleverTap"
    }
  ]
}
[/block]


7. The template will then appear in the Imported tab. Click on **View Content** from the confirmation message or navigate to the **Editor** tab to view translated content.

> 🚧 Personalization
> 
> CleverTap allows email personalization using **{}** formats. When importing emails from CleverTap into Lokalise, these personalized values are included. Make sure not to translate them while exporting content back to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ba322d02fd63f883915ed67366aa25932ebdb6d7ff3dfff4d7dd22eb627e97d7-Lokalise_22.png",
        "",
        "Lokalise Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Lokalise Editor"
    }
  ]
}
[/block]


8. After reviewing the translated content, navigate back to _Content Manager > Imported_, select the template and click on **Export to CleverTap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/394bfb85a2db7b03a5a2b2d5444af6c1bfee7495ed153216e835f7d07b023ff0-Lokalise_21.png",
        "",
        "Export to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Export to CleverTap"
    }
  ]
}
[/block]


# Find Translated Email templates in CleverTap

1. For users with a Content Manager subscription in CleverTap, the exported translated templates from Lokalise will be found under _Content Manager > Templates > Email_. Each language will have its own separate template.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad56bfcc4cb4563dc7133e94c9f3d1b37db975c55f4cf831d0686101f772a851-Lokalise_24.png",
        "",
        "Translated Email Template - CMS"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Email Template - CMS"
    }
  ]
}
[/block]


2. For users without a Content Manager subscription, the exported translated templates will appear under _Campaigns > + Campaigns > Emails > What Section > Saved Templates_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd727e756fd86db027e700d858b1d7c1df16cb5d7fb8d5cf35cb1c3bcd47b800-Lokalise_26.png",
        "",
        "Translated Email Template - Saved Template in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Email Template - Saved Template in Campaign"
    }
  ]
}
[/block]


# FAQs

**Why are only base templates fetched from CleverTap to Lokalise?**  

Currently, only base templates are integrated, which limits the availability of translated templates.

**Why are translated templates not matching the "drag-and-drop" base email templates?**  

Translating JSON to match the "drag-and-drop" template format presents challenges, leading CleverTap to store translated templates in HTML format instead.

**Why do translated templates include the locale present in the base template?**  

- The locale for the base template is not currently set, making it difficult to differentiate between the base locale and the translated locale.
- To streamline this, translated templates are created as "Base Template name\_{Locale}." These are considered child templates.
- When base templates are fetched and translated templates are pushed back, CleverTap updates child templates with the specified locale. For instance, a base template named "Welcome to the App" with the locale "en" will result in three templates upon translating to "fr" and "es": "Welcome to the App_en," "Welcome to the App_fr," and "Welcome to the App_es."

**How can translated templates be used for sending email campaigns from CleverTap?**  

When creating an email campaign, the ["By User Property"](https://docs.clevertap.com/docs/create-message-email#by-user-property) option can be utilized to set the property to match the locale of the translated campaign.

**What happens if a translated email template currently in use is updated?**  

- When an email template from CleverTap CMS or saved templates is used in a campaign, separate instances are created for each send. This ensures personalization and localization are tailored to each email.
- Edits made to an existing template do not impact campaigns created with earlier versions of that template.
- Changes to the main email template in the CMS or saved templates do not retroactively apply to previously created or sent campaigns.
- New campaigns will utilize the updated template, while campaigns in draft or scheduled status require manual updates with the new version.