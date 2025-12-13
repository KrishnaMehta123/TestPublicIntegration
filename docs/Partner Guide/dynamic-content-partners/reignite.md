---
title: Reignite
excerpt: >-
  Power real-time image personalization in your campaigns using the CleverTap
  and Reignite integration.
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

[Reignite](https://www.reignitehq.com/) is a real-time email personalization platform that enables marketers to build and deliver sophisticated 1:1 visual experiences. With features like a visual Recipe Builder, AI-powered recommendations, and dynamic weather or location-based content, Reignite adapts creative content at the moment of engagement.

Using Reignite with CleverTap, you can embed personalized visuals into:

* Embed personalized visuals into Email campaigns and In-App messages.
* Tailor images in real time based on user profile data.
* Create dynamic greetings, offers, or promotions based on user context.

# Prerequisites for Integration

To integrate Reignite with CleverTap, ensure the following prerequisites are met:

* You have access to your Reignite account.
* You have an active CleverTap account.

# Integrate CleverTap with Reignite

The integration process involves the following two major steps:

1. [Create Personalized Content in Reignite](doc:reignite#create-personalized-content-in-reignite)
2. [Configure Reignite in CleverTap campaigns](doc:reignite#configure-reignite-in-clevertap-campaigns)

## Create Personalized Content in Reignite

To create personalized visuals in Reignite, start by following their step-by-step guide: [Create a Personalised Image in Reignite](https://reignite.freshdesk.com/support/solutions/articles/44001355067-create-a-personalised-image).

Once your image is ready, follow these steps to embed CleverTap personalization:

1. Click **Generate Tags** in the top-right to open the tag *Configuration* dialog.
2. In the *Configuration* section:

   * For `String 1`, enter:

     ```liquid
     {{ Profile.name | default: "-" }}
     ```

     This dynamically replaces the text with the recipient’s name.
   * For the **Email Field**, enter:

     ```liquid
     {{ Profile.Email | default: "-" }}
     ```

     This maps the campaign to the recipient's email address.

<Image alt="Configuration Tags" align="center" width="65% " border={true} src="https://files.readme.io/1b4d869942611e2daea1750027ca3ae15dc749bcbad913d074981e348227ffc5-image.png">
  Configuration Tags
</Image>

To learn more about CleverTap Liquid Tags, refer to [CleverTap Personalize Message](doc:personalize-message-all)

3. Copy the generated tag from the **Your Tag** field to use in your CleverTap campaign.

<Image alt="Copy the generated tag from Reignite to use in CleverTap." align="center" width="65% " border={true} src="https://files.readme.io/c9d2906fe6d90158dac5731111326a711720b632b9a0929c536d4145d5156c2b-image.png">
  Copy the generated tag from Reignite to use in CleverTap
</Image>

## Configure Reignite in CleverTap campaigns

The [personalized content configured in Reignite](doc:reignite#create-personalized-content-in-reignite) can be used in any CleverTap campaign that supports HTML or image URLs. While this guide includes an example for an [Email campaign](doc:reignite#configure-personalized-email-campaign-in-clevertap), you can also use Reignite content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-in-app), and other CleverTap messaging channels that support dynamic visuals.

### Configure Personalized Email Campaign in CleverTap

Set up and personalize your email campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to the *Campaigns*, click **+ Campaign**, and select *Email* from the list of messaging channels.
2. Configure the campaign as per your requirements and click **Go to Editor** under the *What* section.
3. Select a *Basic Template*, *Pre-used Template*, or a *Saved Template* from the available templates.
4. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
5. Paste the copied Reignite tag code copied in *step 3* of [Create Personalized Content in Reignite](doc:reignite#create-personalized-content-in-reignite) inside the `<body>` section in the CleverTap Email editor.

<Image alt="Insert the HTML Code Snippet" align="center" width="65% " border={true} src="https://files.readme.io/8e8820b3ac0bc0d56e6b0624e74a11c95d22bd5c5ea44622208328a7804bb8ad-image.png">
  Insert the HTML Code Snippet
</Image>

6. Send a test email to verify personalization and ensure the Reignite integration functions correctly.

<Image alt="Test Email" align="center" width="65% " border={true} src="https://files.readme.io/8062bb06097a2022a668cce88ecbe813274d0bf451094392804ee923d32bcdab-image.png">
  Test Email
</Image>

7. Publish the email campaign once verification is complete.

By integrating Reignite with CleverTap, you can automate visually engaging, hyper-personalized campaigns. Whether it's for celebrating birthdays or dynamically showcasing promotions, Reignite brings visual intelligence into your CleverTap-powered engagement strategy.
