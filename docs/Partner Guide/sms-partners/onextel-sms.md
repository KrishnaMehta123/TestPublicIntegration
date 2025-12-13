---
title: OneXtel
excerpt: Learn how to integrate OneXtel into CleverTap as an SMS service provider.
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

Integrate [OneXtel](https://www.onextel.com/), a CPaaS provider specializing in SMS solutions, into your CleverTap account for streamlined messaging capabilities. This guide outlines the steps to configure OneXtel as an SMS service provider and enable delivery notifications.

# Prerequisites for Integration

To integrate OneXtel with CleverTap, ensure the following:

* You should have an active OneXtel Aura account with associated API keys.
* Ensure that the Entity ID and Sender IDs are added to the OneXtel account.
* Obtain the API keys for the account based on the use case Service Implicit, Service Explicit, and Promo and get the API keys whitelisted from the backend for CleverTap.
* Ensure you have a CleverTap account with SMS setup enabled.

> 📘 Note:
>
> Disable DND scrubbing while creating the API key to ensure complete submission from the connector to the OneXtel platform.

> 🚧 Support for Integration:
>
> For creating a new account, resolving account-related queries, or addressing any integration issues, reach out to [OneXtel Support](mailto:support@onextel.com).

# Integrate OneXtel with CleverTap

This process involves the following four steps:

1. [Configure OneXtel Dashboard](doc:onextel-sms#configure-onextel-dashboard)
2. [Find OneXtel Details](doc:onextel-sms#find-onextel-details)
3. [Configure CleverTap Dashboard](doc:onextel-sms#configure-clevertap-dashboard)
4. [Delivery Notifications on CleverTap Dashboard](doc:onextel-sms#delivery-notifications-on-clevertap-dashboard)

## Configure OneXtel Dashboard

Per the [DLT](https://docs.onextel.com/docs-category/sms-dlt/) mandate, you must upload the following details to the Settings page of your OneXtel Account to send an SMS:

* [Entity ID](https://docs.onextel.com/docs/aura-dlt/entity-id/): The unique ID provided to every business.
* [Sender ID](https://docs.onextel.com/docs/aura-dlt/sender-id/): The six-digit ID from which the SMS is sent.
* [Template ID:](https://docs.onextel.com/docs/aura-dlt/template/) The unique ID for each transactional or promotional SMS you want to use.

## Find OneXtel Details

We recommend that you keep the following information handy before starting with the configuration on the CleverTap dashboard:

* **[API Credentials](https://docs.onextel.com/docs-category/api/)**: Navigate to the *API* on the left navigation on the OneXtel dashboard.

<Image alt="Find OneXtel API Credentials" align="center" border={true} src="https://files.readme.io/bf87f446bd906e0ac12ac168a65f6a3dfcc19a0132af95cd9e052f17b2d9121f-image.png">
  Find OneXtel API Credentials
</Image>

* **[Sender ID](https://docs.onextel.com/docs/aura-dlt/sender-id/)**: Navigate to *DLT* > *Sender ID* on the left navigation on the OneXtel dashboard.

<Image alt="Find OneXtel Sender ID" align="center" border={true} src="https://files.readme.io/7f4cb49f706e91e8f4f4aa1430561318c0826bfb6143ce62e5c41da9bb9d7cc5-image.png">
  Find OneXtel Sender ID
</Image>

* **[Entity ID](https://docs.onextel.com/docs/aura-dlt/entity-id/)**: Navigate to *DLT* > *Entity ID* on the left navigation on the OneXtel dashboard.

<Image alt="Find OneXtel Entity ID" align="center" border={true} src="https://files.readme.io/467433b386674023e54c43812d4c2ccb8e89c9649c9daa11fa04332b33244117-image.png">
  Find OneXtel Entity ID
</Image>

* **[DLT Template ID](https://docs.onextel.com/docs/aura-dlt/template/)**: Navigate to *DLT* > *Template* on the left navigation on the OneXtel dashboard.

> 📘 Recommended:
>
> Add your DLT approved templates in Aura account using the bulk upload option.

<Image alt="Find OneXtel Template ID" align="center" border={true} src="https://files.readme.io/0e3a3afaec09ec0a75012c3e22b33444478e25df887c57f371841c0ce7ca5a65-image.png">
  Find OneXtel Template ID
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Engage* > *Channels* > *SMS* from the CleverTap dashboard.
2. Click *+ Add Provider*. The *Add SMS* provider screen displays.
3. Under Provider, select **Other (Generic)** and enter the following details:

| Field         | Description                                                                    |
| :------------ | :----------------------------------------------------------------------------- |
| Nickname      | Enter the nickname as (Sender ID - Mention your sender ID)                     |
| Callback URL  | No changes (Default)                                                           |
| Request Type  | *POST*                                                                         |
| HTTP Endpoint | [https://ctgwapi.onex-aura.com/postsms](https://ctgwapi.onex-aura.com/postsms) |

4. Under the *Authentication* section, select *No Authentication*.

<Image alt="Add SMS Provider Credentials in CleverTap Dashboard" align="center" border={true} src="https://files.readme.io/b7e68a2a1d929855343dd3e5d574e24c3e5199a90bdd6490dfa4aa4ec3f29e9b-image.png">
  Add SMS Provider Credentials in CleverTap Dashboard
</Image>

5. Enter the following details under the Headers section.

| Key       | Value       |
| :-------- | :---------- |
| `onexkey` | SMS API key |

> 📘 Note :
>
> Once the Key and Value details are filled, kindly share the API key with the [Onextel Support Team](mailto:support@onextel.com) so that the given API key can be whitelisted for the CT configuration from Onextel backend.

<Image alt="Headers" align="center" width="60% " border={true} src="https://files.readme.io/e3d7935a68c235022cadc7983d1c5b73da8d4ebe91dd6c3d2746d0a2d5c4b34f-image.png">
  Headers
</Image>

6. Under *Parameters*, select your request type as **JSON** for a *POST* request. Enter your entire JSON payload structure. You can enable batching by specifying the key name and the number of records per batch.
7. Delete the curly braces, paste the below payload, and replace the **Sender\_ID** and **Entity\_ID** :

```coffeescript JSON
{
  "listsms": [
    {
      "from": "Sender_ID",
      "to": "$$To",
      "body": "$$Body",
      "entityid": "Entity_ID",
      "templateid": "$$TemplateID",
      "clientsmsid": "$$MessageID"
    }
  ]
}
```

Refer to the table below for the detailed mapping of each field in the SMS request body:

| Field                                                                                               | Description                             | Example Value |
| --------------------------------------------------------------------------------------------------- | --------------------------------------- | ------------- |
| [Sender ID](https://staging.docs.user.clevertap.net/docs/onextel-sms#configure-onextel-dashboard)   | DLT-approved Header ID/Sender ID        | SENDER\_ID    |
| To                                                                                                  | Recipient’s mobile number               | $$To          |
| Body                                                                                                | Message content                         | $$Body        |
| [Entity ID](https://staging.docs.user.clevertap.net/docs/onextel-sms#configure-onextel-dashboard)   | The organization’s registered Entity ID | EntityID      |
| [Template ID](https://staging.docs.user.clevertap.net/docs/onextel-sms#configure-onextel-dashboard) | Template ID of the message content      | $$TemplateID  |
| Message ID                                                                                          | Unique ID for tracking the SMS message  | $$MessageID   |

<Image alt="Provider Configuration" align="center" border={true} src="https://files.readme.io/1856c034e1e6f8f6f2a75207ec9aa91d3b9a18485c0246b41355c75010ef37c9-image.png">
  Provider Configuration
</Image>

8. After pasting the payload, select the Batch checkbox and fill in the details as mentioned below.

| Parameter name | Value |
| :------------- | :---- |
| listsms        | 1000  |

> 📘 Single Batch Limit
>
> A single batch can have a maximum of 1,000 records.

9. Click on **Save**. A pop-up box will appear, prompting you to **Send Test SMS**.

## Delivery Notifications on CleverTap Dashboard

1. On the CleverTap Dashboard, go to *Settings* > *Channels* > *SMS*, and select the configured SMS setup.  
2. Copy the **Callback URL** and email it to `support@onextel.com` with TUC details, SMS API key, and integration request.  

For more details, refer to the [Notification Delivery Options Documentation](https://docs.clevertap.com/docs/notification-delivery-options).

> 📘 Encoding
>
> The messages sent out from CleverTap are encoded in the UTF-8 charset.

# FAQs

#### **How do I set up Throttling for better campaign performance?**

After completing the configuration, set up campaign-level throttling by following these steps:

1. Click on *Setup* from the left menu.
2. Select *Campaign Limits* from the dropdown.
3. Add the SMS channel and set the throttle limit to *1,00,000* (recommended).
4. Save the changes.

#### **What steps should I follow to send a test SMS?**

To ensure the SMS integration is successful:  

1. Click the *Send Test SMS* link before creating SMS campaigns or journeys.  
2. Provide the following details:  
   * Country Code and Mobile Number: Enter the recipient's country code and phone number.  
   * Message: This is a test message powered by OneXtel.  

Once the test SMS is sent, confirm its receipt to validate the integration.
