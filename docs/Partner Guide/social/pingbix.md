---
title: Pingbix
excerpt: Learn how to integrate Pingbix with CleverTap for WhatsApp communication.
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

[Pingbix](https://pingbix.com/) is a WhatsApp Business Service Provider (BSP) that helps businesses automate and scale customer communication through WhatsApp. It supports features such as campaign management, real-time delivery tracking, and secure message routing via WhatsApp’s Cloud API.

When integrated with CleverTap, Pingbix enables you to do the following:

* Track message delivery via Pingbix’s callback system.
* Combine WhatsApp messaging with CleverTap’s segmentation and personalization.
* Use pre-approved templates for transactional and promotional campaigns.
* Send WhatsApp messages directly from the CleverTap dashboard.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Pingbix. The CleverTap and Pingbix integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Pingbix](https://pingbix.com/contact) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

* WhatsApp Campaigns feature is enabled on your CleverTap account.
* Active Pingbix WABA (WhatsApp Business Account) credentials.
* Pingbix API key and message delivery callback URLs.

# Integrate Pingbix with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:pingbix#configure-clevertap-dashboard)
2. [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix)

## Configure CleverTap Dashboard

To configure the CleverTap dashboard for Pingbix:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and select *Generic (Other)* from the *Provider* list.

<Image alt="Provider Setup" align="center" width="65% " border={true} src="https://files.readme.io/885f26f7e2110aab22dd2bda2eba90bc4c3e187863d865a407301bc495da3a4d-image.png">
  Provider Setup
</Image>

3. Enter the following details:

<Table>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Details
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter the nickname as Pingbix or the `<10-digit phone number>` for easy reference.
      </td>
    </tr>

    <tr>
      <td>
        Mobile Number
      </td>

      <td>
        Add your WhatsApp Integrated number with country code (for example, +918889500122)
      </td>
    </tr>

    <tr>
      <td>
        HTTP End Point
      </td>

      <td>
        Paste the URL received from the Pingbix team.\
        Check that the URL is in HTTPS format, that is, your URL must begin with **https\://**.
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Ensure the Request Type is *POST*.
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click **Header**\
        Enter the first key name as a user and enter the user value received from Pingbix.\
        Enter the second key name as the password, and enter the value received from Pingbix.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically on the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix).
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message\
        Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Pingbix](doc:pingbix#set-up-clevertap-callbacks-in-pingbix).
      </td>
    </tr>
  </tbody>
</Table>

4. (Optional) Select *Mark this as default* to make Pingbix as the default provider when sending a WhatsApp messages.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to a WhatsApp message from users not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* to any value between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification to verify if the configuration is successful.

<Image alt="Send a test message on whatsapp" align="center" border={true} src="https://files.readme.io/8218fbb75f9546083d2e6bdcfdd5ad32895514885569383c9ec157e337176e2d-image.png">
  Send a Test Message on WhatsApp
</Image>

## Set Up CleverTap Callbacks in Pingbix

To set up CleverTap callbacks in Pingbix, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Pingbix* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with Pingbix team**: Copy the Delivery and Inbound report callback URLs and send them to the Pingbix WhatsApp support team for configuration.

<Image alt="Callback URLs" align="center" width="75% " border={true} src="https://files.readme.io/17b2d251719811d51b3ba0ae7173be50be62ca9e7e716c2c445c2c6ed21362fb-image.png">
  Callback URLs
</Image>

Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Pingbix.

> 📘 Note:
>
> Your templates must be approved on the Pingbix dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the Pingbix integration, write to [Pingbix Support](https://pingbix.com/contact).

## Adding Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, follow these steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Provider Nickname* in the CleverTap dashboard.
2. Select the *Templates* option and click **+Template**.

<Image title="Create a New Template" alt="Create a New Template" align="center" width="70% " border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg">
  Create a New Template
</Image>

3. Enter the template name.
   > 📘 Naming WhatsApp Templates
   >
   > Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
   >
   > For example, if you have multiple provider configurations, such as Phone\_1 and Phone\_2, you can use the particular template name once within Phone\_1 and Phone\_2.
4. You can also choose the language in which you will display the message.
5. Select the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, or *Location*.
6. Create a [Limited Time Offer Template](doc:whatsapp-message-templates#limited-time-offer-templates), if required. 
7. Enter the message content.
8. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).

<Image alt="Define Template Content" align="center" width="70% " border={true} src="https://files.readme.io/5bd5090-Generic_template_create.jpg">
  Define Template Content
</Image>

9. Click **Save Template**.

## Testing a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

## Create Campaign

For detailed instructions on creating a WhatsApp campaign using Pingbix as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using Pingbix as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp).
