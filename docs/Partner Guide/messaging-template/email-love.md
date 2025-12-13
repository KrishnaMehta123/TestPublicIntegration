---
title: Email Love
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

[Email Love](https://emaillove.com/) is a Figma plugin that allows you to design and export responsive, accessible HTML emails directly from Figma.

With this integration, you can:

* Convert Figma email designs into HTML.
* Embed your HTML directly into CleverTap campaigns.
* Enhance campaigns with personalization and automation using CleverTap’s tools.

This document explains integrating Email Love with CleverTap and using exported HTML in CleverTap campaigns.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* An active Email Love account.
* A CleverTap account with a valid Account ID and Passcode.

# Integrate Email Love with CleverTap

The integration process involves the following two major steps:

1. [Design Email in Email Love and Export HTML](doc:email-love#design-email-in-email-love-and-export-html).
2. [Configure Email Campaign](doc:email-love#configure-email-campaign) 

## Design Email in Email Love and Export HTML

Consider an example where a marketing team wants to send a visually rich onboarding email designed in Figma to newly registered users. 

Start by creating your email with the Email Love plugin in Figma, then export it as HTML into the CleverTap dashboard. To do so, perform the following steps:

1. Open your Figma file, go to the Plugins menu, search for Email Love, and launch the plugin.

<Image alt="Email love plugin" align="center" width="50% " border={true} src="https://files.readme.io/75c117e179239c12cbd3ee1a7f2743c0bb952df99fda42b648264a2984351594-image.png">
  Email Love plugin
</Image>

2. Create your email from scratch or use a pre-designed template.
3. Click **Export HTML file** to download the code, or click **Copy HTML code** to copy it directly.

<Image alt="Copy HTML Code" align="center" width="75% " border={true} src="https://files.readme.io/ed791445a9531f78392fefded251ddee6b15bb8305e40e8aba56f9613bea3590-image.png">
  Copy HTML Code
</Image>

Once exported, your HTML code can be embedded directly into a CleverTap email campaign for further personalization and delivery.

## Configure Email Campaign

Set up and personalize your email campaign in CleverTap using the exported HTML template from Email Love. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Email* from the list of messaging channels.
2. Under the *What* section, click **Go to Editor** and perform the following steps: 
   1. Select a *Blank Template*.
   2. Switch to **Source** mode in the email editor.
   3. Paste the copied HTML code from *step 3* of [Design Email in Email Love and Export HTML](doc:email-love#design-email-in-email-love-and-export-html) into the source editor.
3. (Optional) Edit the HTML as needed. You can also add [Liquid tags](doc:personalize-message-all#liquid-tags) for personalization.

<Image alt="Configure Email Campaign" align="center" width="75% " border={true} src="https://files.readme.io/d751750363fa06ae8c4de1a5b59e6595624312571cc65baa6cdb67d9c0a2680b-2025-07-28_14-50-14_1.gif">
  Configure Email Campaign
</Image>

4. Click **Preview & Test** to verify personalization and formatting.

> 📘 Preview Campaign
>
> The preview in CleverTap may render colors differently than what you designed in Figma. The final email renders correctly to recipients.

5. Once confirmed, click **Publish**.

Your personalized email, designed in Figma and exported from Email Love, is now ready to send. You can also save your HTML design as a template for future reuse within CleverTap campaigns. For more information about this, refer to [Content Manager Templates](doc:content-manager-templates).
