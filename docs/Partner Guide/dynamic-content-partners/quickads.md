---
title: Quickads
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

[QuickAds](https://www.quickads.ai/) is an AI-powered ad generator that simplifies the creation of high-quality ads for your marketing campaigns. Integrating it with CleverTap allows you to:

- Instantly create custom visuals for targeted email or push campaigns.
- Streamline ad creation directly within your campaign workflow.
- Ensure consistent branding across all communication channels.

This integration enables marketing teams to launch visually compelling campaigns faster, without sacrificing quality.

# Prerequisites for Integration

The following are the prerequisites for integrating QuickAds with CleverTap:

- Ensure you have an active QuickAds account.
- Ensure you have a CleverTap account.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by QuickAds. The CleverTap and QuickAds integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [QuickAds](https://www.quickads.ai/contact-us) for support and resolution.

# Integrate QuickAds with CleverTap

The integration process involves the following two major steps:

1. [Generate Ads on QuickAds](doc:quickads#generate-ads-on-quickads)
2. [Configure CleverTap Email Campaign](doc:quickads#configure-clevertap-email-campaign)

## Generate Ads on QuickAds

QuickAds provides a streamlined process for creating high-quality ads tailored to your brand. To generate your ads, perform the following steps:

1. Go to the QuickAds dashboard and start a new ad project.
2. Define your brand identity:

   - Set your brand colors
   - Describe your campaign objective
3. Select a template that fits your campaign style.
4. Customize the ad:

   - Edit the text, colors, and images to match your brand voice
5. Download the final ad image to your device.

For detailed instructions, refer to [QuickAds Tutorials](https://www.quickads.ai/tutorials).

## Configure CleverTap Email Campaign

Once you download your QuickAds ad, you can incorporate it into CleverTap campaigns via the following two methods:

- [Upload via Content Manager](doc:quickads#method-1-upload-via-content-manager)
- [Upload Directly in an Email Campaign](doc:quickads#method-2-upload-directly-in-an-email-campaign)

### Method 1: Upload via Content Manager

Upload your QuickAds image for reuse across multiple campaigns using the Content Manager as follows:

1. From the CleverTap dashboard, go to **Content Manager**.
2. Click **Upload File** to add your QuickAds image.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/751fb6fe7c02fa53d06594aa2a43f59b2c08ed4f07a04c60409050261f9a5976-2025-05-11_10-16-55_1.gif",
        "",
        "Upload via Content Manager"
      ],
      "align": "center",
      "border": true,
      "caption": "Upload via Content Manager"
    }
  ]
}
[/block]


The uploaded asset can now be reused across multiple campaigns. For more information, refer to the CleverTap [Content Manager](https://staging.docs.user.clevertap.net/docs/content-manager-files) feature.

### Method 2: Upload Directly in an Email Campaign

You can upload your QuickAds creative directly while building an email campaign in CleverTap as follows:

1. Create a new email campaign on the CleverTap dashboard.
2. Go to the _What_ section in the setup.
3. Select an **Email Template**.
4. Locate the image placeholder to be replaced, click **Change Image**, and upload your QuickAds creative.
5. Click **Insert** to replace the sample image.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e7810bb004a01319a704fa482e7fd096ce27c42b9eac012c94381353fd7b1ef-Screen_Recording_2025-01-20_at_12.40.06_PM_1.gif",
        "",
        "Upload QuickAds Directly in an Email Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Upload QuickAds Directly in an Email Campaign"
    }
  ]
}
[/block]


Your QuickAds-generated visuals can be reused in different CleverTap campaign formats, including: [Push Notifications](doc:create-message-push), [In-App messages](doc:create-message-in-app), or [Web Popups](doc:create-message-web-popup).

Using the same creative across channels helps maintain brand consistency and improve campaign performance.