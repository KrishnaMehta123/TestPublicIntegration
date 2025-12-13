---
title: OneXtel
excerpt: Learn how to integrate OneXtel with CleverTap for WhatsApp communication.
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

CleverTap users can now leverage [OneXtel](https://docs.onextel.com/) WhatsApp capabilities to communicate with customers. Communications include:

* Sending real-time, personalized offers to drive customer engagement and purchases.
* Gathering feedback on the services.
* Keeping customers updated about important information, such as promotions, service updates, or event alerts.

# Prerequisites for Integration

The following are the prerequisites for OneXtel:

* An active OneXtel WhatsApp account must be set up on [365cx.io.](https://365cx.io)
* WhatsApp add-on enabled on the CleverTap account in addition to the basic or essential price plan.
* WhatsApp onboarding for the phone number used with CleverTap must be completed.

> 🚧 Support for Integration:
>
> For creating a new account, resolving account-related queries, or addressing any integration issues, reach out to [OneXtel Support](mailto:support@onextel.com).

# Integrate OneXtel with CleverTap

This process involves the following two steps:

1. [Find OneXtel Details.](doc:onextel-whatsapp#find-onextel-details)
2. [Configure CleverTap Dashboard.](doc:onextel-whatsapp#configure-clevertap-dashboard)
3. [Set Up CleverTap Callbacks in OneXtel](doc:onextel-whatsapp#set-up-clevertap-callbacks-in-onextel)

## Find OneXtel Details

We recommend having the HTTP endpoint URL (which includes the Channel ID) readily available before configuring the CleverTap dashboard. Follow these steps to access the HTTP endpoint URL:

1. Navigate to *Channels* in the OneXtel dashboard.
2. Click the **Integration** option on the right. To Create new Integration.

<Image alt="Integration" align="center" border={true} src="https://files.readme.io/43fa274c04c453b81824d4f5a2235d10b4fd44a5bb9a9b8ad9104b2d5ca3917b-image.png">
  Integration
</Image>

3. Enter the following details: 

| Step                 | Description                                                  |
| -------------------- | ------------------------------------------------------------ |
| **Integration Name** | Enter a name for the integration.                            |
| **Platform**         | Select **CleverTap** as the platform.                        |
| **Channel Type**     | Select **WhatsApp** as the channel type.                     |
| **Choose Channel**   | Select the channel you want to integrate with **CleverTap**. |

<Image alt="Create Channel Integration" align="center" border={true} src="https://files.readme.io/732508eb3fda5f99a9925933b90ecc6d7bfb7410ac80fbc3b08cb1a6a9f331c5-image.png">
  Create Channel Integration
</Image>

4. Click **Submit**. You will be able to get the HTTP endpoint to paste into the CleverTap account.

<Image alt="HTTP endpoint" align="center" border={true} src="https://files.readme.io/e967b40677b977c523c9bb7e49bf4e6d720824d7bfc52d332f5d1eb7694fa4b7-image.png">
  HTTP endpoint
</Image>

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings > Channels > WhatsApp > WhatsApp Connect* from the CleverTap dashboard.
2. Click *+ Add Provider* and select Generic (Other) from the dropdown.

<Image alt="Provider Setup" align="center" width="50% " border={true} src="https://files.readme.io/5d276daba70a9156fe64ed69678d024e089edd77bd0bd7b4a7b102a5489ba456-image.png">
  Provider Setup
</Image>

3. Enter the following details:

| Field                                                      | Details                                                                                                                                  |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Provider                                                   | Generic (Other)                                                                                                                          |
| Nickname                                                   | Enter the nickname as OneXtel                                                                                                            |
| Mobile Number                                              | Enter the same WABA number along with the country code as mentioned on [365cx.io](https://365cx.io) (OneXtel) while creating the channel |
| Request Type                                               | Ensure the Request Type is *POST*                                                                                                        |
| [HTTP Endpoint](doc:onextel-whatsapp#find-onextel-details) | Enter the HTTP endpoint from OneXtel.                                                                                                    |

4. To make this service provider the default provider to send a WhatsApp message, select the *Mark this as default checkbox*.
5. To automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard, select the *Set auto-reply for users not tracked on CleverTap checkbox*.
6. (Optional) You can set the *Maximum Concurrent API requests* anywhere between 30 to 1000 requests. Consider your requirement and the provider's limitations to define this value.
7. Click **Save**.

## Set Up CleverTap Callbacks in OneXtel

To set up the CleverTap callbacks:

1. Copy the *Delivery Report Callback URL*  from the CleverTap dashboard. You can find the Callback URLs under the Provider *Setup* page under *Settings* > *Channels* > *WhatsApp* > OneXtel

<Image alt="Configure callback" align="center" border={true} src="https://files.readme.io/9721cd77f5e4365b8068059d7ca837208a637fb655b14042264981fa87820517-image.png">
  Configure callback
</Image>

2. Go to OneXtel dashboard, go to *Channels* > *Integrations* and paste the same Delivery Report Callback URL.

# FAQs

#### How do I set up Throttling for better campaign performance?

To set up campaign-level throttling, go to *Settings > Setup > Campaign Limits*, add the *WhatsApp* channel, set the throttle limit to *1,00,000* (recommended), and save the changes.
