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

* **Design, code, and manage email templates using Taxi for Email**, which also enables collaborative editing, live previews, approval workflows, template management, and version control, ensuring compatibility across email clients.
* **Segment audiences, personalize content, and execute campaigns on the CleverTap dashboard**, effectively targeting the right users with tailored messages.

> 📘 Enable CleverTap Connector on Taxi For Email
>
> To activate the CleverTap connector for Taxi For Email, contact the Taxi For Email support team or your account manager directly from the platform or send an email to [support@bird.com](mailto:support@bird.com) to submit a request.

# Prerequisites for Integration

The following are the prerequisites:

* [A Taxi for Email account](https://www.taximail.com/en/support/using-taximail/sign-up-with-email) with all the required setup and permissions to export email templates. 
* A CleverTap account.

# Steps for integration

The integration involves the following three main steps:

1. [Configure Taxi for Email Dashboard](doc:taxi-for-email#integrate-clevertap-on-taxi-for-email-dashboard).
2. [Set Up Personalization](doc:taxi-for-email#setting-personalization).
3. [Export Email Templates from Taxi For Email Dashboard to CleverTap](doc:taxi-for-email#export-email-templates-from-taxi-for-email-dashboard-to-clevertap).

## Configure Taxi for Email Dashboard

Add CleverTap credentials on the Taxi for Email dashboard:

1. Navigate to *Integrations* > *ESP Connectors* from the dashboard and click **Add New**.

<Image alt="Add Integration" align="center" border={true} src="https://files.readme.io/630a9d6-Taxi_for_Email.png">
  Add New Connector
</Image>

2. Select *CleverTap* from the *Connector type* dropdown. 

<Image alt="Add Connector" align="center" border={true} src="https://files.readme.io/c1c2e8a-taxi_add_new_connector.png">
  Select Connector Type
</Image>

3. Enter the following details:

<Image alt="Integrate CleverTap Connector" align="center" border={true} src="https://files.readme.io/d7c3386-Taxi.png">
  Integrate CleverTap Connector
</Image>

* **Account ID** : Locate the Project ID under *Settings* > *Project* from the CleverTap dashboard.
* **Passcode**: Locate Passcode under *Settings* > *Project* from the CleverTap dashboard. To know more, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
* **Region**: Locate Region for the API endpoint you want to select under *Settings* > *Project* from the CleverTap dashboard. To identify the region for your account, refer to the following table:

| Region | CleverTap Dashboard URL                                                                            |
| :----- | :------------------------------------------------------------------------------------------------- |
| aps3   | [https://aps3.dashbaord.clevertap.com/login.html](https://aps3.dashbaord.clevertap.com/login.html) |
| eu1    | [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html)   |
| in1    | [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html)   |
| mec1   | [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html) |
| sg1    | [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html)   |
| us1    | [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html)   |

<Image title="Project ID and Region" alt="Locate Project ID and Region on CleverTap Dashboard" align="center" border={true} src="https://files.readme.io/d6907e7-Taxi_Project_ID.png">
  Locate Project ID and Region on CleverTap Dashboard
</Image>

* **Default From Name and Email**: Adding a default *From Name* and *Email* address ensures recipients can recognize your emails easily. You can also change this information while exporting the email templates to CleverTap.
* **Default Reply To Name and Email**: Adding a default name and email address for replies ensures that your emails always have the correct details, saving time and preventing mistakes by automatically populating these fields.

> 📘 Note
>
> Currently, we do not save *Reply to Name* and *Email address*. CleverTaps sends the email as per the settings configured under the *Provider Setup* page.

3. Click **Save Details & Continue**.

## Set Up Personalization

CleverTap supports personalization using [Liquid tags](https://docs.clevertap.com/docs/personalize-message-all#liquid-tags). To use Liquid tags for personalization in CleverTap, you must first set up personalization in Taxi for Email:

1. Navigate to *Dynamic Content* > *Personalization* from the Taxi for Email dashboard, and select *Add Field*.
2. Map the labels to the API default values saved in [step 1](doc:taxi-for-email#configure-taxi-for-email-dashboard). For example, the *Label* can be mapped to a Default Value of *ABC*, which can be mapped to CleverTap's Liquid Tag, that is, `{{ Profile.name | default:"ABC" }}`
3. Select the project to which the personalization must be added, add the mapped Label in the template with the appropriate text, and click **Save Changes**. 

> 📘 Note
>
> If a tag does not have the required personalization information, Taxi for Email sends a default value to CleverTap.

<Image alt="Adding Personalization" align="center" border={true} src="https://files.readme.io/3896544-Taxi_14.png">
  Adding Personalization
</Image>

3. Select **Export Mailing** and the personalization reflects under the email editor on the CleverTap dashboard.

# Export Email Templates to CleverTap

After setting up the template on the Taxi for Email, you can export the email templates to CleverTap:

1. Select the version of the Template to be exported to the CleverTap dashboard and click **Export Mailing**. 

<Image alt="Export Mailing" align="center" border={true} src="https://files.readme.io/be87c3e-Taxi_6.png">
  Export Mailing
</Image>

2. Select the **API name** provided in [step 1](doc:taxi-for-email#configure-taxi-for-email-dashboard) under ESP Connectors. 

<Image alt="ESP Connector" align="center" border={true} src="https://files.readme.io/618b8d4-Taxi_15.png">
  ESP Connector
</Image>

After selecting the ESP connector, a new window opens for you to select the template type.

3. Select **Create a new template** to export a new template to CleverTap. To update an existing CleverTap template, select **Update an existing template** and select a template from the drop-down menu.

<Image alt="Create a new template" align="center" border={true} src="https://files.readme.io/e5c7da9-Taxi_10.png">
  Create a New Template
</Image>

> 🚧 Important
>
> Ensure that the *Template Name* is unique when exporting new templates to avoid errors.

4. Under Segmentation, select the version(s) that needs to be exported.
   * *Send one version*: Choose to export only a single version of the content.
   * *Create (or update) a template for each version*: Generate or modify templates for each selected version.

<Image alt="Export Version" align="center" border={true} src="https://files.readme.io/bb47c8f-Taxi_9.png">
  Export or Create (or Update) a Particular Template Version
</Image>

5. Click **Start Export** to export the email template to the CleverTap dashboard.

<Image alt="Start Export" align="center" border={true} src="https://files.readme.io/93e5ca8-Taxi_11.png">
  Start Export
</Image>

# Create a Campaign on CleverTap Using Taxi for Email Template

To create an email campaign on CleverTap using the Taxi for Email template:

1. Navigate to the *Campaigns* page, click **+ Campaign**, and select *Email* from the list of messaging channels. 
2. Click **Go to Editor** under the When section and select **Saved Templates**. 
3. Select the template you exported from the Taxi for Email dashboard. 

<Image alt="CleverTap Saved Email Templates" align="center" border={true} src="https://files.readme.io/75aacba-Taxi_12.png">
  CleverTap Saved Email Templates
</Image>

Once you create a campaign on the CleverTap dashboard, follow the remaining steps listed under the [Create Email Campaign](doc:create-message-email) section and publish the campaign.
