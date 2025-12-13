---
title: Voucherify
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

The[ Voucherify](https://www.voucherify.io) integration with CleverTap enables seamless data transfer between the platforms, allowing you to inform customers about promotions and deliver personalized coupons efficiently. By combining CleverTap campaigns with Voucherify, you can automate the distribution of unique coupons and gift cards based on customer actions or special occasions, ensuring timely and targeted engagement.  

With this integration, you can,

* **Bulk delivery**: Send codes to a specific customer segment in one go.
* **Segment updates**: Automatically deliver codes when a customer enters or exits a defined segment.
* **Event-based responses**: Send codes in reaction to an outstanding order or any custom event.

This integration enhances your ability to connect with customers and drive meaningful engagement through personalized promotions.

# Prerequisites

Before setting up the integration, ensure you have the following details readily available:

* **Campaign ID:** Retrieve it from the **Campaign** tile in the **Campaign List** from the Voucherify dashboard or by calling the [GET campaign endpoint](https://docs.voucherify.io/reference/get-campaign).
* **API URL**: Navigate to *Application Information section >  API endpoint > Project Settings*  to find your API URL on your Voucherify dashboard.
* **App ID and App Token**: Navigate to **Project Settings** on the Voucherify dashboard to obtain App ID and App Token after setting up the CleverTap integration.

> 📘 Troubleshooting
>
> For any queries or assistance required with integrating CleverTap and Voucherify, contact the [Voucherify Support](https://www.voucherify.io/contact-support) team.

# Setup Integration on the Voucherify Dashboard

To enable seamless communication between CleverTap and Voucherify, follow these steps to set up the integration on the Voucherify dashboard:

1. Navigate to **Project Settings** and scroll to **Integration Keys** in the General tab.
2. Click the **+** on the right.
3. Fill in the **Name** for your key. 
4. Choose your **Role** from the Role drop-down list.
5. Choose **CleverTap** from the Integration drop-down list.
6. Click the **Create Integration API Key** button. App ID and App Token will be generated after successful integration.

   <Image alt="Setup CleverTap Integration on Voucherify Dashboard" align="center" border={true} src="https://files.readme.io/0d91c3cedeb0c6f1a6908234a17008c11d3a30643e4a2f5eed310769b75dd523-Voucherify_9.png">
     Setup CleverTap Integration on Voucherify Dashboard
   </Image>

# Scenario 1: Distribute Voucherify unique coupons with CleverTap

Boost customer engagement by distributing Voucherify's unique coupon codes through CleverTap. This integration allows you to automate campaigns, track redemptions, and personalize offers to suit your audience with the following steps.

## Prepare a Voucherify Campaign to Engage Inactive Customers

To re-engage inactive customers, a unique coupon campaign can be configured in Voucherify. For example, a "Customer Reactivation" campaign can be created to offer a 20% discount on the entire cart, capped at a maximum discount value of $100.

**Key Configuration**:\
Enable the "Customers will be allowed to join the campaign only once" option to control code distribution:

* **When Enabled**: Each customer receives a single code from the campaign. If they request another, the system will provide the same code they were originally issued.
* **When Disabled**: A new coupon code is generated each time a request is made.

This setting allows you to decide whether customers can access multiple reactivation codes or just one, depending on your campaign strategy.

> 📘 Campaign ID
>
> Copy the Campaign ID at this stage to configure the Endpoint on the CleverTap Dashboard while setting up Linked Content for the campaign.

# Configure Linked Content on the CleverTap Dashboard

To publish a new code from the CleverTap campaign, configure Linked Content on the dashboard as follows: 

1. Navigate to *Settings > Setup > Linked Content* and select the **+ Linked Content**. A Linked Content form will appear. 

   * **API Name:** Enter a name for the Linked Content endpoint. For example, "**New Reactivation Voucher**" represents voucher code distribution from the Customer Reactivation campaign.  

   * **API URL:** Specify the URL of the Create Publications endpoint:\
     `**{{API_URL}}/v1/publications/create?campaign=[Voucherify campaign ID]&customer={{customersourceid}}**`.

   * **Headers tab**: 

     * Add the X-App-Id and X-App-Token headers you generated during [setting up integration on Voucherify](doc:voucherify#setup-integration-on-the-voucherify-dashboard).

     * Set Content-Type header to `**application/json**`.

   <Image alt="Linked Content Headers on CleverTap" align="center" border={true} src="https://files.readme.io/c6f6c72eb15175c0e0730881c1e3c0f6aa2649125a55411504c7cd5bbb427662-Voucherify_2.png">
     Linked Content Headers on CleverTap
   </Image>

* **Parameters Tab:**  A parameter named **customersourceid** will appear.  Enable the **Mark mandatory** checkbox to ensure the customer ID is provided, as it is required to assign a coupon to the customer. 

  <Image alt="Setup Linked Content on CleverTap - Voucherify" align="center" border={true} src="https://files.readme.io/f6d18ce12c759ebc670818efdc0fea675f7b1d8d17b128cd10ec35ea9723dbd3-Voucherify_1.png">
    Setup Linked Content on CleverTap - Voucherify
  </Image>

2. Click **Test Linked Content**. If the configuration is correct, Voucherify's response will be displayed. 

<Image alt="Testing for Response on CleverTap - Voucherify" align="center" border={true} src="https://files.readme.io/b53b764a4ad11839ab16375c75b4191526763492b3dd40b4b3f56cd9e3a39d47-Voucherify_3.png">
  Testing for Response on CleverTap - Voucherify
</Image>

3. Click on **Auto-Fill Objects with Response** to automatically populate objects present in the response. For this example, only the **voucher.code** field will be needed – it contains the published coupon code.

   <Image alt="Auto-Fill Objects with Response on CleverTap - Voucherify" align="center" border={true} src="https://files.readme.io/d209b291b7d39ff257c8bbd7d9b9e6cb3977b3936a5a69cc08eabc9186f9eb7d-Voucherify_4.png">
     Auto-Fill Objects with Response on CleverTap - Voucherify
   </Image>
4. Click **Save & Test Changes**.

Refer to [Linked Content ](doc:linked-content) for more details.

## Use Linked Content Endpoint and Create a Campaign on CleverTap

Create a new campaign in CleverTap. For this example, configure a one-time email outbound campaign targeting customers who last visited the e-commerce site 30 days ago. 

1. Navigate to **Campaigns** and select **Email** under **+ Campaign**.
2. Under the What section, Go to Editor and select **Personalization**.
3. Select the relevant API from the drop-down menu. For this example, select New Reactivation Voucher and click **Apply**.
4. Specify the field to be used as the request parameter for the endpoint and map the properties and values. 

   <Image alt="Personalization Setup in CleverTap Campaigns - Voucherify" align="center" border={true} src="https://files.readme.io/b086f217ec399430bf07fba77c269175c1c0d6ad144d1a59e61cded228ba3bf1-Voucherify_5.png">
     Personalization Setup in CleverTap Campaigns - Voucherify
   </Image>
5. Select **Apply**.
6. In the place where you want the coupon code to be displayed, choose Customize with Liquid tags and choose the code field from the Linked Content endpoint created during [configuring Linked Content](doc:voucherify#configure-linked-content-on-the-clevertap-dashboard). For this example, Add the `**{{Linked{"New Reactivation Voucher"].[code] | default: "contact us"}}**` which has been set during configuring [Linked Content](doc:voucherify#configure-linked-content-on-the-clevertap-dashboard). 

<Image alt="Linked Content in CleverTap Email - Voucherify" align="center" width="70% " border={true} src="https://files.readme.io/312af38868642e02f6f8debd84295d978f36f40a198d847cc0cf918230e2f6db-Voucherify_6.png">
  Linked Content in CleverTap Email - Voucherify
</Image>

7. Click **Preview & Test** to view how the message will appear for a specific customer.

> 📘 Delivery Preferences
>
> Email throttling can be configured within the campaign's delivery settings to regulate the message delivery rate. Ensure that the throttling rate is adjusted to remain within the minute limit defined in your Voucherify plan.

8. Upon publishing the campaign, messages will be delivered either at the scheduled time or immediately. Each message will be personalized for the recipient and will contain the voucher code allocated to them.

   <Image alt="Personalized Discount Code with CleverTap Email Campaign - Voucherify" align="center" width="70% " border={true} src="https://files.readme.io/edeb801976c5d71c9368907083b48d6abde52bb32052c7956adea81dbef06551-Voucherify_7.png">
     Personalized Discount Code with CleverTap Email Campaign - Voucherify
   </Image>

   <br />

   You can see each publication call made during the email send-out in the Audit Log in your Voucherify Dashboard with the URL `**/v1/publications/create**`.

   You can also view the generated codes in the selected campaign dashboard in the Vouchers tab. 

# Scenario 2: Referral code and loyalty card publication

The process of assigning a referral code or loyalty card is similar to the steps outlined above. Simply update the campaign name parameter to reference the specific referral or loyalty campaign you have created.

In this example, the customer's code is retrieved from the referral program with the ID `camp_f0bKCWIYyTfOept56g2UMLY7`.

Suppose the Customer is allowed to join the campaign only once (the option is enabled in the referral program configuration), a customer will receive their previously assigned referral code. If a referral code has not yet been assigned to the customer, a new code will be generated and included in the response.

1. Configure the Linked Content endpoint:

<Image alt="Linked Content - Voucherify" align="center" border={true} src="https://files.readme.io/4fc7770cb30b9158d5f982dffeb32f261177cb600217170d7a83b23fbb6f0002-Voucherify_10.png">
  Linked Content - Voucherify
</Image>

2. To retrieve the loyalty card, use the following code: `{{ Linked["Customer Referral Code"].code }}`.

The customer can share their referral code with a friend. When they use it during a purchase, the referrer will be awarded the gift you have set up in the Voucherify Dashboard.
