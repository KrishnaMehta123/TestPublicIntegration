---
title: 8X8
excerpt: Learn how to integrate 8x8 with CleverTap for WhatsApp communication.
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

[8x8](https://www.8x8.com/) offers a WhatsApp Business API solution that enables businesses to reach their users with high-quality, real-time messaging. By integrating 8x8 with CleverTap, businesses can:

* Send personalized WhatsApp campaigns using Meta-approved templates.
* Trigger journeys and transactional messages based on user behavior.
* Capture delivery and engagement metrics using CleverTap analytics.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by 8x8. The CleverTap and 8x8 integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [cpaas-support@8x8.com](mailto:cpaas-support@8x8.com) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

* The WhatsApp Campaigns feature is enabled on your CleverTap account.
* An 8x8 account with WhatsApp Business (WABA) access.
* A provisioned WhatsApp Business number from 8x8.

To activate a new WhatsApp number via 8x8, contact your account manager or write to [cpaas-support@8x8.com](mailto:cpaas-support@8x8.com).

# Integrate 8x8 with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:8x8-whatsapp#configure-clevertap-dashboard)
2. [Set Up CleverTap Callbacks in 8x8](doc:8x8-whatsapp#set-up-clevertap-callbacks-in-8x8)

## Configure CleverTap dashboard

To configure the CleverTap dashboard:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and select *Generic (Other)* from the *Provider* list.

<Image alt="Provider Setup" align="center" width="65% " border={true} src="https://files.readme.io/885f26f7e2110aab22dd2bda2eba90bc4c3e187863d865a407301bc495da3a4d-image.png">
  Provider Setup
</Image>

3. Enter the following details:

<Table align={["left","left"]}>
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
        Enter the nickname as 8x8  or `8x8_WA_India` for easy reference.
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
        Request Type
      </td>

      <td>
        Ensure the Request Type is *POST*.
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Paste the following URL:`https://chatapps.8x8.com/api/v1/subaccounts/{{subaccountid}}/partners/clevertap/wa`\
        Check that the URL is in HTTPS format, that is, your URL must begin with `https//`
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click **Header** >\
        Enter the Key name as a user and enter the user value received from 8x8.\
        Enter the second key name as the password and the value received from 8x8.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in 8x8](doc:8x8-whatsapp#set-up-clevertap-callbacks-in-8x8).
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message\
        Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in 8x8](doc:8x8-whatsapp#set-up-clevertap-callbacks-in-8x8).
      </td>
    </tr>
  </tbody>
</Table>

4. (Optional) Select *Mark this as default* to make this service provider the default provider to send a WhatsApp message via 8x8.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification (refer to the following image).

<Image title="Send Test Message on WhatsApp" alt="Send a text message" align="center" border={true} src="https://files.readme.io/c384922-sendtest.png">
  Send a Test Message on WhatsApp
</Image>

## Set Up CleverTap Callbacks in 8x8

To set up CleverTap callbacks in 8x8, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Interakt* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with Interakt**: Copy both URLs and send them to the 8x8 WhatsApp support team for configuration or email at [cpaas-support@8x8.com](mailto:cpaas-support@8x8.com).

<Image alt="Callback URLs" align="center" width="65% " border={true} src="https://files.readme.io/8422e19929f1eaab1b982d4d8a98785454eb8da322dcb9d4894562d55ce3dc5b-image.png">
  Callback URLs
</Image>

Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and 8x8.

> 📘 Note
>
> You have to get your templates approved on the 8x8 dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages.

## Adding Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, follow these steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Provider Nickname* in the CleverTap dashboard. 
2. Select the *Templates* option and click **+Template**.

<Image title="Create a New Template" alt="Create a New Template" align="center" border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg">
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

<Image alt="Define Template Content" align="center" border={true} src="https://files.readme.io/5bd5090-Generic_template_create.jpg">
  Define Template Content
</Image>

9. Click **Save Template**.

## Testing a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

## Create Campaign

For detailed instructions on creating a WhatsApp campaign using 8x8 as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using 8x8 as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp).
