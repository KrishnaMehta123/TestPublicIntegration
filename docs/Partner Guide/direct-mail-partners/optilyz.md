---
title: Optilyz
excerpt: Direct Mail
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

[Optilyz](https://www.optilyz.com) is a direct Email automation platform that helps you create personalized, sustainable, and efficient direct email campaigns, including letters, postcards, and self-mailers.

Integrating CleverTap with Optilyz allows you to run hyper-targeted direct mail campaigns as part of your customer journeys. This integration bridges digital and physical channels, enhancing campaign ROI and customer experience. 

With this integration, you can:

* Send personalized postcards or letters based on In-App or online user behavior.
* Automate A/B testing of print creatives using campaign variations.
* Include direct mail in omnichannel customer journeys for better conversion and engagement.

# Prerequisites for Integration

Ensure the following before starting the integration:

* Ensure you have access to your CleverTap account.
* Ensure you have access to your Optilyz account.
* Ensure that you have your Optilyz API key. Your Optilyz customer success manager will provide you with your Optilyz API key.
* Ensure that you have your Optilyz Automation ID. The ID can be found in a box on the page header. Navigate to the automation (you want to send data into) on your Optilyz dashboard. The automation must be activated for your account first.

<Image alt="Automation ID" align="center" width="65% " border={true} src="https://files.readme.io/fe4f1a826389ac743c03895201bbeda1d08f1db094b728bc6792ab6ebdc74d5c-image.png">
  Automation ID
</Image>

# Integrate CleverTap with Optilyz

To integrate Optilyz with CleverTap, perform the following two major steps:

1. [Set Up Webhook in CleverTap](doc:optilyz#set-up-webhook-in-clevertap)
2. [Create Webhook Campaign in CleverTap](doc:optilyz#create-webhook-campaign-in-clevertap)

These steps allow you to automate the delivery of personalized direct mail, such as letters and postcards, triggered by user activity tracked in CleverTap.

> ⚠️ Enable Webhooks
>
> If Webhooks are not enabled for your account, contact [CleverTap Support](mailto:support@clevertap.com).

## Set Up Webhook in CleverTap

Configure the webhook in your CleverTap dashboard to initiate direct mail triggers using the Optilyz endpoint. To do so, perform the following steps:

1. Go to *Settings* > *Channels* > *Webhooks* from the CleverTap dashboard.
2. Click **+ Add Webhook** and provide a meaningful name for the webhook.
3. Set the *HTTP Method* to `POST` and enter the following *Endpoint URL*. For more information, refer to [Optilyz API](https://www.optilyz.com/doc/api/).

```json
https://www.optilyz.com/api/v2/automations/<OPTILYZ_AUTOMATION_ID>/recipient
```

4. Add the following key-value pair under *Headers*:

| Key           | Value              |
| ------------- | ------------------ |
| Authorization | `Bearer ApiKey`    |
| Content-Type  | `application/json` |

5. Select *Basic Authentication* for Authentication and enter the following:
   * Username: Your Optilyz *Private API Key*
   * Password: Use a hyphen (`-`)

<Image alt="Create Webhook" align="center" width="55% " border={true} src="https://files.readme.io/c9824d65ed8b74c5a8f112e584a85021592581ff2be239a7339755817cd9b4c0-image.png">
  Create Webhook
</Image>

6. Click **Save** to create the webhook.

After saving the webhook, CleverTap will be ready to send user profile data directly to Optilyz.

## Create Webhook Campaign in CleverTap

Launch a Webhook campaign to deliver personalized direct mail from CleverTap to Optilyz users. To do so, perform the following steps:

1. Go to *Campaigns* on the CleverTap dashboard, click **+ Campaign** and select *Webhook* from the list of messaging channels.
2. Configure the following campaign settings: target audience, schedule, and other basic settings.
3. Perform the following steps under the *What* section:

   1. Select the webhook created in [Set Up Webhook in CleverTap](doc:optilyz#set-up-webhook-in-clevertap).
   2. Set Content Format to `JSON`.
   3. Select *Custom Body*.

<Image alt="Webhook Content" align="center" width="50% " border={true} src="https://files.readme.io/8b0fc07b06e7eb830724731b27111799d57f1fa3fd1ce267189bdaf18888e668-image.png">
  Webhook Content
</Image>

4. Enter the payload under the *Custom Body* section using [Liquid Tags](doc:personalize-message-all#liquid-tags):

```json
{
   "address": {
       "title": "{{ Profile.title | default: "-" }}",
       "firstName": "{{ Profile.first_name | default: "-" }}",
       "lastName": "{{ Profile.last_name | default: "-" }}",
       "street": "{{ Profile.street | default: "-" }}",
       "houseNumber": "{{ Profile.address | default: "-" }}",
       "zipCode": "{{ Profile.zipcode | default: "-" }}",
       "city": "{{ Profile.city | default: "-" }}",
       "country": "{{ Profile.country | default: "-" }}"
   },
   "variation": 1
}
// Note: The `variation` field is optional and controls which design variation will be used in Optilyz. If omitted, a variation will be selected randomly.
```

Click the variable selector (`@`, `{`, or `{{`) in the editor to personalize the campaign. You can dynamically reference user profile properties using [Liquid Tags](doc:personalize-message-all#liquid-tags).

> 📘 Personalization
>
> You can use any available personalization attributes and structure your request body according to the [Optilyz API documentation](https://www.optilyz.com/doc/api/).

5. Click **Preview & Test** to validate the webhook request.

<Image alt="Preview and Test" align="center" width="65% " border={true} src="https://files.readme.io/8b742e0eedd4aef31484a49717a237f5136489e06971a38baa3a216533ad8ea8-image.png">
  Preview and Test Campaign
</Image>

6. Click **Publish** to launch the campaign. Verify in the Optilyz dashboard if everything works as intended.

<Image alt="Verify in the Optilyz dashboard" align="center" width="65% " border={true} src="https://files.readme.io/24692cbe1e05095d58fea2d47b1e39392831bdfb0dd07683ddbe680851963380-image.png">
  Optilyz dashboard
</Image>

Once published, your campaign will trigger real-world mailers based on live user behavior.
