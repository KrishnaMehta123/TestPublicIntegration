---
title: Loyalty Lion
excerpt: Loyalty Partner
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

[LoyaltyLion](https://loyaltylion.com) is a customer loyalty and engagement platform designed for e-commerce businesses. It helps brands to incentivize customer behavior and personalize user engagement through data-driven loyalty programs.

By integrating LoyaltyLion with CleverTap, you can:

* Send order and event data from CleverTap to LoyaltyLion using Webhooks
* Fetch user-specific reward data from LoyaltyLion into CleverTap using Linked Content and personalize campaigns

# Prerequisites for Integration

Ensure you have the following:

* LoyaltyLion API credentials (available in your LoyaltyLion dashboard).
* Access to your CleverTap dashboard with permissions to configure webhooks and campaigns.

# Integrate LoyaltyLion with CleverTap

To integrate LoyaltyLion with CleverTap, perform the following major steps:

1. [Create a Webhook in CleverTap](doc:loyalty-lion#create-a-webhook-in-clevertap)
2. [Configure Webhook Campaign in CleverTap](doc:loyalty-lion#configure-webhook-campaign-in-clevertap)
3. [Personalize Campaigns Using LoyaltyLion Rewards](doc:loyalty-lion#personalize-campaigns-using-loyaltylion-rewards)

## Create a Webhook in CleverTap

Create a webhook to push event and order data from CleverTap to LoyaltyLion. This webhook lets CleverTap transmit relevant customer activity data (for example, purchases, order totals, shipping) directly to LoyaltyLion in real time.To do so, perform the following steps:

1. Go to *Settings* > *Channels* > *Webhook* from the CleverTap dashboard.
2. Click **+ Create Webhook** and fill in the details:

| Field         | Value                                   |
| ------------- | --------------------------------------- |
| Name          | LoyaltyLion Orders Webhook              |
| Method        | `POST`                                  |
| Endpoint      | `https://api.loyaltylion.com/v2/orders` |
| Headers       | `Content-Type: application/json`        |
| Authorization | Bearer {'<Loyalty Lion API Key>'}       |

You will find the API key in your Loyalty Lion Dashboard in Settings

<Image alt="LoyaltyLion Dashboard" align="center" border={true} src="https://files.readme.io/3512408261b3c8b03e266b85a6b08cdbdec380882e591b7740d4ed1e1d85e998-image.png" />

3. Click **Save**.

<Image align="center" className="border" width="65% " border={true} src="https://files.readme.io/3f0944c4df4ae061158621c5a44ea6f8cfb8c954988546d104c5af0baccb21a5-image.png" />
## Configure Webhook Campaign in CleverTap

To push transactional data (like orders) to LoyaltyLion:

1. Go to *Campaigns* > *+ Campaign* > *Webhook*.
2. Select the Webhook configured in [Create a Webhook in CleverTap](doc:loyalty-lion#create-a-webhook-in-clevertap)
3. In the *What* section, under the *Webhook Content* section, select the *Content Format* as JSON and click the **Custom body** option.
4. Paste the following payload:

```json
{
  "merchant_id": "1212",
  "merchant_number": "12",
  "customer_id": {{ Profile.Identity | default: "0" }},
  "customer_email": "{{ Profile.Email | default: "test@gmail.com" }}",
  "total": "{{ Profile.Total | default: "0" }}",
  "total_shipping": "{{ Profile.Total_Shipping | default: "0" }}",
  "payment_status": "{{ Profile.Payment_Status | default: "Fail" }}",
  "date": "{{ Profile.order_date | default: "0" }}",
  "discount_codes": [
    {
      "code": "{{ Profile.code-used | default: "0" }}",
      "amount": "{{ Profile.amount | default: "0" }}"
    }
  ]
}
```

Type `{`, `{{`, or `@` to view available personalization options.

5. Click **Preview and Test** the campaign to check if the data appears correctly in the LoyaltyLion dashboard.

<Image alt="Verify the data on LoyaltyLion" align="center" width="65%" border={true} src="https://files.readme.io/4d155692e30ec741fa468077a5e940ab8cd970dfab9a9a2dd4001b9f143e3f19-image.png" />

6. If everything works as intended, click **Publish**.

For more information, refer to the [Loyalty Lion API documentation](https://developers.loyaltylion.com/api-reference/v2/resources/orders/create-order).

## Personalize Campaigns Using LoyaltyLion Rewards

Use [Linked Content](doc:linked-content) to fetch real-time rewards from LoyaltyLion and show them in campaigns. To display personalized creatives using dynamic URLs, follow these steps:

1. [Configure the Linked Content API in CleverTap.](doc:loyalty-lion#configure-linked-content-api-in-clevertap)
2. [Create a Personalized Campaign Using Linked Content.](doc:loyalty-lion#create-personalized-campaign-using-linked-content)

### Configure Linked Content API in CleverTap

To display the personalized rewards in CleverTap campaigns, you must configure Linked Content. To do so, follow these steps:
1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content**.
3. Provide a relevant name for the Linked Content, set the `HTTP` method to `GET`, and use the following endpoint as the destination URL:
   ```
   https://api.loyaltylion.com/v2/customers/{{cid}}/available_rewards
   ```

In this URL, `cid` represents the customer ID used to retrieve the user's available rewards. Ensure this parameter is marked as mandatory.

<Image alt="Configure Linked Content in CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/1a179c1e39a615f60b441392068825a51c5c44db43b7ad72aacf9f3d2db7d799-2025-05-09_19-41-03_1.gif" />

4. In the Headers, add this below key-value pair: 
   * Authorization: Bearer `{'<Loyalty Lion API Key>'}`
5. Test the Linked Content to ensure it returns the expected output.

<Image alt="Test the Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/8d9e5da0f498e31fdfcb33a0fb65241075404e7ea61b6f64f3dd3fde475b8be9-image.png" />

6. Click **Save** to finalize the Linked Content configuration.

Once your Linked Content is configured, you can use it in any messaging channel.

### Create Personalized Campaign Using Linked Content

With LoyaltyLion connected to CleverTap via Linked Content, you can now deliver personalized rewards through your campaigns. To do so, perform the following steps:

1. Go to *Campaigns*  from the CleverTap dashboard and click **+ Campaign**.

2. Select *Push Notification* from the *Messaging Channels* list.

3. Configure all the campaign settings and then go to the *What* section:

   1. Click **Personalization**. 
   2. Select the *Linked Content* configured under [Configure Linked Content API in CleverTap](doc:loyalty-lion#configure-linked-content-api-in-clevertap) and click **Apply**.

<Image alt="Personalization" align="center" width="65% " border={true} src="https://files.readme.io/e24f7ff1a37a0e936b6fd820948b17a598068c15a2fc8d88b4035de1f257bd94-image.png" />

4. Set the `cid` parameter to Custom and assign the value `{{'{{ Profile.c-id | default: "0" }}'}}`. This dynamically fetches the customer ID `cid` from the user profile when the campaign is delivered.
<Image alt="Create Personalized Message Using Linked Content" align="center" width="65%" border={true} src="https://files.readme.io/6e479e0d10c081b6a3edbbf5023899bf711640bce35f05cc68aeca3e0ffa7e7d-image.png" />

This configuration ensures that the correct variant is fetched based on the user's customer ID and displayed in the campaign.

5. Use the following Linked Content Liquid tag to extract the reward title from the LoyaltyLion Get Reward API's `JSON` response:

```liquid
{'{'}% for reward in response.content.data %{'}'}
  {'{'}{ reward.data.attributes.title }{'}'}
{'{'}% endfor %{'}'}
```

6. Configure the campaign's Title and Message using the retrieved reward title. For example:

<Image alt="Set the Title and Message" align="center" width="65%" border={true} src="https://files.readme.io/6e360137cfde9c61d7ca3990aa7bd229bf0a6061a305dd1b76f06dcd2b494cf7-image.png" />

7. Click **Preview & Test** to verify if the campaign pushes the default values you configured. 
8. Click **Publish** to launch the campaign. Verify if everything works as intended. Users will receive a push notification such as the one below.

<Image alt="Push Notifications" align="center" width="55%" border={true} src="https://files.readme.io/52e84680c8682ff563fd8c423d2e6c7413be99d860215c240a09b1b4e9e3ae59-image.png" />

By integrating LoyaltyLion with CleverTap, you can deliver real-time personalized visuals at scale across the following channels: [Push Notifications](doc:create-message-push), [Email](doc:create-message-email), [In-App Messages](doc:create-message-in-app), or [Web Popups](doc:create-message-web-popup#campaign-priority), LoyaltyLion empowers you to deliver highly relevant, personalized messaging at scale.