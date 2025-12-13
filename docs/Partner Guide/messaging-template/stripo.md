---
title: Stripo
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

[Stripo](https://stripo.email/) is an email design platform that makes it easy to create responsive, professional email templates using the drag-and-drop editor and rich customization options. Integrating Stripo with CleverTap enables seamless export of email templates, combining Stripo’s intuitive, responsive email builder with CleverTap’s personalized campaign delivery. This integration simplifies email marketing by directly syncing Stripo templates into CleverTap, ensuring automated and targeted customer engagement.

With this integration, you can:

- Design responsive email templates in Stripo and import them with CleverTap for personalized customer engagement.
- Automate email delivery based on customer actions such as sign-ups, purchases, or abandoned carts.
- Re-engage users with targeted campaigns using dynamic templates designed in Stripo.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by Stripo. The CleverTap and Stripo integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Stripo](mailto:support@stripo.email.) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

- Ensure you have a Stripo account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Stripo with CleverTap

The integration process involves the following three steps:

1. [Export Email Template to CleverTap](doc:stripo#export-email-template-to-clevertap).
2. [Create a CleverTap Campaign Using Stripo Template](doc:stripo#create-a-clevertap-campaign-using-stripo-template).

## Export Email Template to CleverTap

After [setting up the template](https://stripo.email/blog/how-to-build-an-email-with-stripo-manual-a-to-z/) on the Stripo for Email, you can export the email templates to CleverTap:

1. Click **Export** in the top navigation bar and select _CleverTap_ from the export options.

2. Set up the CleverTap Connection:
   1. Provide a connection name (for example, CleverTap Export).
   2. Enter the following details:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

4. Click **Export ** to import the template in CleverTap.

> 📘 Exporting as AMP
> 
> CleverTap does not recommend enabling the "**Export as AMP**" toggle during export, as AMP templates currently cannot be exported to CleverTap. To ensure seamless integration, please export your email templates in standard HTML format.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/803ad8f02596af5793130c39dc710f0fb2ce8de14771d3c8f902ac1ac9b00b4c-wwwewewewe.gif",
        "",
        "Export Email Template to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Email Template to CleverTap"
    }
  ]
}
[/block]


## Create a CleverTap Campaign Using Stripo Template

To create an email campaign on CleverTap using the Stripo for Email template:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select Email from the list of messaging channels.
2. Click **Go to Editor** under the _When_ section and select _Saved Templates_.
3. Select the template you imported from Stripo.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70cbf0aee337c1d307e61bdd4dd28eae4a3d2c0841f061bfe60065a8ceb3502d-image.png",
        null,
        "Email Template - Saved Template in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap Saved Email Templates"
    }
  ]
}
[/block]


Once you create a campaign on the CleverTap dashboard, follow the remaining steps listed under the [Create Email Campaign](https://docs.clevertap.com/docs/create-message-email) section and publish the campaign.

# FAQs

**Can I edit the template in CleverTap after exporting it from Stripo?**

Yes, once the template is exported to CleverTap, you can use CleverTap's editor to make further modifications as needed.

**Who do I contact for integration issues?**

For technical assistance, reach out to [Stripo support](mailto:support@stripo.email.).

**What happens if I make changes to a Stripo template after exporting it to CleverTap?**

If you make changes to a Stripo template after exporting it, you must re-export the updated version to CleverTap to reflect those changes in your campaign.