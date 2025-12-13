---
title: Storylane
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

[Storylane](https://www.storylane.io) enables B2B marketing and sales engineering teams to create engaging product demos and interactive walkthroughs.

With the CleverTap and Storylane integration, you can:

* Share personalized product demo links with leads via CleverTap campaigns.
* Drive engagement with embedded product tours tailored to each user.

# Prerequisites for Integration

To integrate Storylane with CleverTap, ensure the following prerequisites are met:

* You have access to a Storylane account with permissions to create demos.
* You have access to the CleverTap dashboard with permissions to create email campaigns.

# Integrate Storylane with CleverTap

The integration process involves the following two major steps:

1. [Create Demo Links in Storylane](doc:storylane#create-demo-links-in-storylane)
2. [Configure Storylane in CleverTap Campaigns](doc:storylane#configure-storylane-in-clevertap-campaigns)

## Create Demo Links in Storylane

To begin, you must generate a Storylane demo link to be used in CleverTap campaigns:

1. Log in to your [Storylane account](https://app.storylane.io/login).
2. Create the product demo you want to share.
3. After publishing the demo, copy the shareable link.

<Image alt="Create Demo Links in Storylane" align="center" width="65% " border={true} src="https://files.readme.io/291bfdbecff34d073620ee854e2ee1096c572984d47558467905e7b4f356987a-image.png">
  Create Demo Links in Storylane
</Image>

## Configure Storylane in CleverTap Campaigns

The [personalized demo link](doc:storylane#create-demo-links-in-storylane) created in Storylane can be used across any CleverTap campaign that supports URLs or HTML, such as [email campaigns](doc:create-message-email), [push notifications](doc:create-message-push), or [In-App campaigns](doc:create-message-in-app). While this guide walks through an email example, you can embed demo links similarly in other campaign types using dynamic profile attributes.

### Configure a Personalized Email Campaign in CleverTap

Set up and personalize your email campaigns in CleverTap to effectively engage users with dynamic Storylane demos. To do so, follow these steps:

1. Go to the *Campaigns*, click **+ Campaign**, and select *Email* from the list of messaging channels.
2. Configure the campaign as per your requirements and click **Go to Editor** under the *What* section.
3. Select a *Basic Template*, *Pre-used Template*, or a *Saved Template* from the available templates.
4. Draft your email content based on your campaign requirements.
5. Paste the Storylane demo link copied in *Step 3* of [Create Demo Links in Storylane](doc:storylane#create-demo-links-in-storylane) into the email body.

<Image alt="Draft Email With Demo Link" align="center" width="65% " border={true} src="https://files.readme.io/17f51b24817f039b8ad3ba43f2993568ae1d69621b85506f8a2d0e89c028a0ca-image.png">
  Draft Email With Demo Link
</Image>

6. Replace the placeholder `{{email}}` in the demo link with a dynamic [CleverTap Liquid tag](doc:personalize-message-all#liquid-tags) using the personalization toolbar. For example, use `{{ Profile.Email | default: "test@clevertapcom" }}` to dynamically insert the user's email address.
7. Send a test email to verify personalization and ensure the Storylane integration functions correctly.

<Image alt="Test Email" align="center" width="65% " border={true} src="https://files.readme.io/831a9caa9deef7a865916e59396fd07f3532999552fe32e39ee3f1350af037cc-image.png">
  Test Email
</Image>

8. Publish the email campaign once verification is complete.

By integrating Storylane with CleverTap, you enable dynamic, user-specific demo experiences that can boost product understanding and conversion rates.
