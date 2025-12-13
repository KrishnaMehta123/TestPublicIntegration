---
title: Yotpo
excerpt: Loyalty Partner
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

[Yotpo](https://www.yotpo.com) is a leading platform that powers customer reviews, loyalty programs, and User-Generated Content (UGC) for e-commerce businesses. CleverTap’s Linked Content feature allows you to fetch real-time data from Yotpo, such as loyalty points, product ratings, or 5-star reviews, and use it to personalize campaigns across channels.

With this integration, you can:

* Personalize campaigns using dynamic data such as reward point balances or product ratings.
* Fetch real-time customer data from Yotpo using their APIs.
* Enhance engagement by directly incorporating social proof (for example,  loyalty points, star ratings, or top reviews) into messages.

# Prerequisites for Integration

The following are the prerequisites for Yotpo:

* Ensure you have a valid Yotpo Loyalty API Key.
* Ensure you have access to the CleverTap dashboard.
* Ensure user profiles in CleverTap should include a valid `email`.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Yotpo. The CleverTap and Yotpo integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Yotpo](https://support.yotpo.com/docs/contacting-yotpo-support) for support and resolution.

# Integrate Yotpo with CleverTap

The integration process involves the following two major steps:

1. [Configure Linked Content API](doc:yotpo#configure-linked-content-api)
2. [Create a Personalized Campaign Using Linked Content](doc:yotpo#create-a-personalized-campaign-using-linked-content)

Let us understand the process with the help of an example. Here, the use case is to show Customer Loyalty Points and personalize messages with each customer’s current reward point balance.

## Configure Linked Content API

To display each user's loyalty point balance, you must set up a Linked Content API that connects to Yotpo. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* in the CleverTap dashboard and click **+ Linked Content**.

<Image alt="Add Linked Content" align="center" width="85% " border={true} src="https://files.readme.io/a06da6f0b7efc54f86dc7cf9f2af6c8dcfa0fe4b529b000e9c71bfa6615ff3f3-image.png">
  Add Linked Content
</Image>

2. Paste the following in the **URL** field. This endpoint fetches loyalty details using the user’s email from CleverTap.

```html
https://loyalty.yotpo.com/api/v2/customers?customer_email={{email}}
```

3. Click **Test** and click **AutoFill Objects with response** to map the returned fields such as `points_balance`.

<Image alt="AutoFill Objects with response" align="center" width="75% " border={true} src="https://files.readme.io/6989c76f720f6ce907ed933fffaebd3479a3a6ebbed6948162b488de299a415a-image.png">
  AutoFill Objects with Response
</Image>

4. Click **Test and Save** to save this API.

> 🚧 Important
>
> Ensure the email field is present and correctly populated in the user's CleverTap profile. This field is required for fetching loyalty details from Yotpo and enabling dynamic personalization. For more information, refer to [Fetch Customer Details](https://loyaltyapi.yotpo.com/reference/fetch-customer-details) in Yotpo.

Once the loyalty data is available, you can use it in any CleverTap campaign that supports Linked Content, such as [Push Notifications](doc:create-message-push) or [Email campaigns](doc:create-message-email).

## Create a Personalized Campaign Using Linked Content

For this example, the Linked Content API is used inside a Push Notification campaign to personalize the message with loyalty data.

To do so, perform the following steps:

1. Go to *Campaigns*  from the CleverTap dashboard and click **+ Campaign**.

2. Select *Push Notification* from the *Messaging Channels* list.

3. Configure all the campaign settings and then go to the *What* section:
   1. Compose your message and click **Personalization**. 
   2. Select the *Linked Content* configured under [Configure Linked Content API](doc:yotpo#configure-linked-content-api) and click **Apply**.

<Image alt="Personalization" align="center" border={true} src="https://files.readme.io/a3374c8a1e5bc30a31aa7a3a306e8af5223cd4605cae1af3d3fc8d4c420c545f-2025-05-09_19-59-27_1.gif">
  Personalization
</Image>

4. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid tag](doc:personalize-message-all).

<Image alt="Create Personalized Message Using Linked Content" align="center" border={true} src="https://files.readme.io/654f2c92e549bbae6d27ced23d353aea68dc2e9964400737c16c9c49c139660c-image.png">
  Create Personalized Message Using Linked Content
</Image>

5. Click **Preview & Test** to ensure that the campaign pushes the default values you configured. 
6. Click **Publish** to launch the campaign. Users will receive a push notification such as the one below.

<Image alt="Push Notifications" align="center" width="35% " border={true} src="https://files.readme.io/ca72494929343ce3df7d8c3c3bd483c7926eb26118724a80c0f4a83b47b8695d-image.png">
  Push Notifications
</Image>

Using different API endpoints during Linked Content setup, you can follow the same process to show additional Yotpo data in your campaigns, including **[review ratings](https://apidocs.yotpo.com/reference/get-bottom-line-total-reviews-and-average-score)**, **[product images](https://apidocs.yotpo.com/reference/product-images)**, or **[5-star testimonials](https://apidocs.yotpo.com/reference/retrieve-reviews-for-a-product)**.
