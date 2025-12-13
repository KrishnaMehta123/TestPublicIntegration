---
title: Wove
excerpt: Dynamic Content
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

[Wove](https://wove.com/) enables brands to reach new customers by embedding partner content into email campaigns. With Wove, you can display content from your network partners and allow them to feature your brand in their campaigns, helping you grow your audience through trusted, brand-aligned placements.

With the CleverTap and Wove integration, you can:

* Embed dynamic content blocks in your email templates to show personalized offers, for instance, a user sees fitness gear recommendations based on past purchases.
* Display partner brand content in your campaigns, such as a wellness brand featuring skincare offers from a partner.
* Expand your reach by letting Wove partners promote your content, such as a fashion brand’s promo shown in a lifestyle partner’s email.

This integration enables dynamic, mutually beneficial collaboration between complementary brands using CleverTap’s campaign delivery infrastructure.

# Prerequisites for Integration

Ensure you have the following before starting the integration:

* A verified Wove dashboard account
* An active CleverTap account with email campaign access

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Wove. The CleverTap and Wove integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Wove](mailto:founders@wove.com) for support and resolution.

# Integrating Wove with CleverTap

To integrate Wove with CleverTap, perform the following two major steps:

1. [Create Element on Wove Dashboard](doc:wove#create-element-on-the-wove-dashboard).
2. [Configure CleverTap Email Campaign](doc:wove#configure-clevertap-email-campaign).

## Create Element on the Wove Dashboard

Use this setup when you want to insert a Wove-powered dynamic content block, such as partner brand offers or promotional banners, within your CleverTap email template.

To create and configure a content placement in Wove, perform the following steps:

1. Log in to your Wove dashboard.
2. Create and customize a *tag* for each of your email templates. This tag defines the content block where Wove partner messaging will appear.

<Image alt="Create Tags" align="center" width="40% " border={true} src="https://files.readme.io/ef1eb2030b8a94e8dea48c618531fa0b111921bdd92e46709b2ed83742604639-ChatGPT_Image_Aug_18_2025_11_56_37_AM.png">
  Create Tags
</Image>

3. After setting up the tag, click **Copy to ESP**, then use the **Copy** icon to get the HTML snippet.\
   Paste this snippet into your CleverTap email template, where the partner content should be rendered.

<Image alt="Copy to ESP" align="center" width="45% " border={true} src="https://files.readme.io/68336fe238202698b47ec908c2397218fd25eb369a44587626a20d30f898221d-image.png">
  Copy to ESP
</Image>

This HTML snippet links your CleverTap template to the Wove content block at open time.

## Configure CleverTap Email Campaign

To integrate Wove into your CleverTap email campaign, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select Email from the list of messaging channels.
2. Click **Go to Editor** under the *What* section and select a Basic Template or Saved Template.
3. Depending on your editor preference, use one of the following methods:

   * If using the **Drag-and-Drop Editor**:

     1. Drag an **HTML block** onto your email template.
     2. Click the block to activate it.
     3. In the **Content** panel on the right, paste the HTML Snippet copied in *step 3* of [Create Element on the Wove Dashboard](doc:wove#create-element-on-the-wove-dashboard) inside the block.

        <Image alt="Drag-and-Drop Editor" align="center" width="65% " border={true} src="https://files.readme.io/26e8cc12fc75ff9003bf9f1b143d22bad115dfc80ead5d1c72b1f164fb5c19ef-Screenshot_2025-02-12_at_3.49.49_PM.png">
          Drag-and-Drop Editor
        </Image>
   * If using the **HTML Editor**:
     1. Click **Source** to open the HTML view.
     2. Paste the HTML Snippet copied in *step 3* of [Create Element on the Wove Dashboard](doc:wove#create-element-on-the-wove-dashboard) inside the `<body>` tag.

   <Image alt="HTML Editor" align="center" width="65% " border={true} src="https://files.readme.io/37a44902c1da9d41edf277607e58e15b99d05720175ba4148a2da3a455c9b9e0-Screen_Recording_2025-02-12_at_3.50.35_PM_1.gif">
     HTML Editor
   </Image>
4. Click **Preview and Test** to ensure the campaign displays Wove content as expected.
5. Once verified, click **Publish**

By combining CleverTap’s personalization capabilities with Wove’s partner network, you can create cross-brand campaigns that drive higher engagement, broaden your audience, and deliver measurable business impact.
