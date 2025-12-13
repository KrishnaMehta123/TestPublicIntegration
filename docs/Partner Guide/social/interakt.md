---
title: Interakt
excerpt: Learn how to integrate Interakt with CleverTap for WhatsApp communication.
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

[Interakt](https://www.interakt.ai/) is a WhatsApp Business platform that allows businesses to engage customers using automated notifications, product catalogs, and real-time messaging. Integrating Interakt enables businesses to send personalized WhatsApp campaigns powered by CleverTap's user segmentation and behavior analytics.

Use this integration to:

* Send personalized campaigns using Meta-approved templates.
* Automate user communication with template-triggered journeys.
* Track delivery and engagement using CleverTap’s reporting.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Interakt. The CleverTap and Interakt integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Interakt](mailto:hello@interakt.ai) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

* The WhatsApp Campaigns feature is enabled on your CleverTap account.
* A WhatsApp Business account on Interakt.
* An approved phone number is onboarded to WhatsApp Business via Interakt.
* The API credentials shared by the Interakt support team.

To activate a new WhatsApp Business number with Interakt, contact your Interakt Account Manager or write to [hello@interakt.ai](mailto:hello@interakt.ai).

# Integrate Interakt with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:interakt#configure-clevertap-dashboard)
2. [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt)

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
        Enter the nickname as Interakt  or `Interakt91XXXXXXXXXX` for easy reference.
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
        Paste the following URL:`https://api.interakt.ai/v1/platform_integrations/clevertap/message/`\
        Check that the URL is in HTTPS format, that is, your URL must begin with `https//`
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click **Header** >\
        Enter the Key name as a user and enter the user value received from Interakt.\
        Enter the second key name as password and enter the value received from Interakt.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt).
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message\
        Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in Interakt](doc:interakt#set-up-clevertap-callbacks-in-interakt).
      </td>
    </tr>
  </tbody>
</Table>

4. (Optional) Select *Mark this as default* to make this service provider the default provider when sending a WhatsApp message via Interakt.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification: 

<Image title="Send Test Message on WhatsApp" alt="Send a test message on whatsapp" align="center" border={true} src="https://files.readme.io/c384922-sendtest.png">
  Send a Test Message on WhatsApp
</Image>

## Set Up CleverTap Callbacks in Interakt

To set up CleverTap callbacks in Interakt, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Interakt* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with Interakt**: Copy the Delivery and Inbound report callback URLs and send them to the Interakt WhatsApp support team for configuration or email the URLs at [hello@interakt.ai](mailto:hello@interakt.ai).

<Image alt="Callback URLs" align="center" width="65% " border={true} src="https://files.readme.io/8422e19929f1eaab1b982d4d8a98785454eb8da322dcb9d4894562d55ce3dc5b-image.png">
  Callback URLs
</Image>

Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Interakt.

> 📘 Note
>
> You have to get your templates approved on the Interakt dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages.

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
> For example, if you have multiple provider configurations, such as Phone\_1 and Phone\_2, you can use the  particular template name once within Phone\_1 and Phone\_2.

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

For detailed instructions on creating a WhatsApp campaign using Interakt as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using Interakt as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).
