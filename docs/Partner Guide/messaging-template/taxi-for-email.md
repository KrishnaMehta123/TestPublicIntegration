---
title: Taxi for Email
excerpt: Messaging Template Partner
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

[Taxi for Email](https://www.taximail.com/en/home), a collaborative platform, streamlines the design and coding of email campaigns, enabling teams to create consistent, high-quality emails without the need for extensive coding knowledge. CleverTap integrates with Taxi for Email to:

- **Design, code, and manage email templates using Taxi for Email**, which also enables collaborative editing, live previews, approval workflows, template management, and version control, ensuring compatibility across email clients.
- **Segment audiences, personalize content, and execute campaigns on the CleverTap dashboard**, effectively targeting the right users with tailored messages.

> 📘 Enable CleverTap Connector on Taxi For Email
> 
> To activate the CleverTap connector for Taxi For Email, contact the Taxi For Email support team or your account manager directly from the platform or send an email to [support@bird.com](mailto:support@bird.com) to submit a request.

# Prerequisites for Integration

The following are the prerequisites:

- [A Taxi for Email account](https://www.taximail.com/en/support/using-taximail/sign-up-with-email) with all the required setup and permissions to export email templates. 
- A CleverTap account.

# Steps for integration

The integration involves the following three main steps:

1. [Configure Taxi for Email Dashboard](doc:taxi-for-email#integrate-clevertap-on-taxi-for-email-dashboard).
2. [Set Up Personalization](doc:taxi-for-email#setting-personalization).
3. [Export Email Templates from Taxi For Email Dashboard to CleverTap](doc:taxi-for-email#export-email-templates-from-taxi-for-email-dashboard-to-clevertap).

## Configure Taxi for Email Dashboard

Add CleverTap credentials on the Taxi for Email dashboard:

1. Navigate to _Integrations_ > _ESP Connectors_ from the dashboard and click **Add New**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/630a9d6-Taxi_for_Email.png",
        "",
        "Add Integration"
      ],
      "align": "center",
      "border": true,
      "caption": "Add New Connector"
    }
  ]
}
[/block]


2. Select _CleverTap_ from the _Connector type_ dropdown. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c1c2e8a-taxi_add_new_connector.png",
        "",
        "Add Connector"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Connector Type"
    }
  ]
}
[/block]


3. Enter the following details:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d7c3386-Taxi.png",
        "",
        "Integrate CleverTap Connector"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate CleverTap Connector"
    }
  ]
}
[/block]


- **Account ID **: Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.
- **Passcode**: Locate Passcode under _Settings_ > _Project_ from the CleverTap dashboard. To know more, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
- **Region**: Locate Region for the API endpoint you want to select under _Settings_ > _Project_ from the CleverTap dashboard. To identify the region for your account, refer to the following table:

| Region | CleverTap Dashboard URL                           |
| :----- | :------------------------------------------------ |
| aps3   | <https://aps3.dashbaord.clevertap.com/login.html> |
| eu1    | <https://eu1.dashboard.clevertap.com/login.html>  |
| in1    | <https://in1.dashboard.clevertap.com/login.html>  |
| mec1   | <https://mec1.dashboard.clevertap.com/login.html> |
| sg1    | <https://sg1.dashboard.clevertap.com/login.html>  |
| us1    | <https://us1.dashboard.clevertap.com/login.html>  |

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


- **Default From Name and Email**: Adding a default _From Name_ and _Email_ address ensures recipients can recognize your emails easily. You can also change this information while exporting the email templates to CleverTap.
- **Default Reply To Name and Email**: Adding a default name and email address for replies ensures that your emails always have the correct details, saving time and preventing mistakes by automatically populating these fields.

> 📘 Note
> 
> Currently, we do not save _Reply to Name_ and _Email address_. CleverTaps sends the email as per the settings configured under the _Provider Setup_ page.

3. Click **Save Details & Continue**.

## Set Up Personalization

CleverTap supports personalization using [Liquid tags](https://docs.clevertap.com/docs/personalize-message-all#liquid-tags). To use Liquid tags for personalization in CleverTap, you must first set up personalization in Taxi for Email:

1. Navigate to _Dynamic Content_ > _Personalization_ from the Taxi for Email dashboard, and select _Add Field_.
2. Map the labels to the API default values saved in [step 1](doc:taxi-for-email#configure-taxi-for-email-dashboard). For example, the _Label_ can be mapped to a Default Value of _ABC_, which can be mapped to CleverTap's Liquid Tag, that is, `{{ Profile.name | default:"ABC" }}`
3. Select the project to which the personalization must be added, add the mapped Label in the template with the appropriate text, and click **Save Changes**. 

> 📘 Note
> 
> If a tag does not have the required personalization information, Taxi for Email sends a default value to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3896544-Taxi_14.png",
        "",
        "Adding Personalization"
      ],
      "align": "center",
      "border": true,
      "caption": "Adding Personalization"
    }
  ]
}
[/block]


3. Select **Export Mailing** and the personalization reflects under the email editor on the CleverTap dashboard.

# Export Email Templates to CleverTap

After setting up the template on the Taxi for Email, you can export the email templates to CleverTap:

1. Select the version of the Template to be exported to the CleverTap dashboard and click **Export Mailing**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be87c3e-Taxi_6.png",
        "",
        "Export Mailing"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Mailing"
    }
  ]
}
[/block]


2. Select the **API name** provided in [step 1](doc:taxi-for-email#configure-taxi-for-email-dashboard) under ESP Connectors. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/618b8d4-Taxi_15.png",
        "",
        "ESP Connector"
      ],
      "align": "center",
      "border": true,
      "caption": "ESP Connector"
    }
  ]
}
[/block]


After selecting the ESP connector, a new window opens for you to select the template type.

3. Select **Create a new template** to export a new template to CleverTap. To update an existing CleverTap template, select **Update an existing template** and select a template from the drop-down menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5c7da9-Taxi_10.png",
        "",
        "Create a new template"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Template"
    }
  ]
}
[/block]


> 🚧 Important
> 
> Ensure that the _Template Name_ is unique when exporting new templates to avoid errors.

4. Under Segmentation, select the version(s) that needs to be exported.
   - _Send one version_: Choose to export only a single version of the content.
   - _Create (or update) a template for each version_: Generate or modify templates for each selected version.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb47c8f-Taxi_9.png",
        "",
        "Export Version"
      ],
      "align": "center",
      "border": true,
      "caption": "Export or Create (or Update) a Particular Template Version"
    }
  ]
}
[/block]


5. Click **Start Export** to export the email template to the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/93e5ca8-Taxi_11.png",
        "",
        "Start Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Start Export"
    }
  ]
}
[/block]


# Create a Campaign on CleverTap Using Taxi for Email Template

To create an email campaign on CleverTap using the Taxi for Email template:

1. Navigate to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels. 
2. Click **Go to Editor** under the When section and select** Saved Templates**. 
3. Select the template you exported from the Taxi for Email dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75aacba-Taxi_12.png",
        "",
        "CleverTap Saved Email Templates"
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap Saved Email Templates"
    }
  ]
}
[/block]


Once you create a campaign on the CleverTap dashboard, follow the remaining steps listed under the [Create Email Campaign](doc:create-message-email) section and publish the campaign.