---
title: QuickReply
excerpt: >-
  Learn how to integrate QuickReply with CleverTap to send personalized WhatsApp
  messages at scale.
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

[QuickReply](https://quickreply.ai/) is a conversational commerce platform that helps brands automate WhatsApp communication at scale. By integrating QuickReply with CleverTap, you can send personalized, automated WhatsApp messages triggered by user behavior, leveraging QuickReply’s API and infrastructure.

With this integration, you can do the following:

* Send automated WhatsApp messages based on user actions or campaigns.
* Personalize messages using CleverTap’s user profiles.
* Track message delivery and user engagement within CleverTap.

This setup combines QuickReply’s automation capabilities with CleverTap’s real-time engagement engine to drive relevant conversations and increase conversions.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by QuickReply. The CleverTap and QuickReply integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [QuickReply](mailto:help@quickreply.ai) for support and resolution.

# Prerequisites for Integration

To integrate QuickReply with CleverTap:

* You must have the WhatsApp add-on enabled on your CleverTap account in addition to the Essentials Plan.
* WhatsApp onboarding for the phone number must be completed via QuickReply.
* Check that you have the Project ID and Passcode from CleverTap and the Authorization Header from the QuickReply dashboard.

# Integrate QuickReply with CleverTap

This process involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:quickreply#create-a-passcode-on-the-clevertap-dashboard)
2. [Configure CleverTap dashboard](doc:quickreply#configure-clevertap-dashboard)
3. [Set Up CleverTap Callbacks with QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to its REST API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Configure CleverTap dashboard

To configure the CleverTap dashboard, perform the following steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.

2. Click **+ Add Provider** and select *Generic (Other)* from the dropdown.

<Image alt="Provider Setup" align="center" width="65% " border={true} src="https://files.readme.io/e5ea73360e548e7e9e865b5c4eee5d3de38df679e2e570c832c3c3d023bfa99e-image.png">
  Provider Setup
</Image>

3. Enter the following details:

<Table>
  <thead>
    <tr>
      <th>
        **Field**
      </th>

      <th>
        **Details**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter a name such as `QuickReply` for reference.
      </td>
    </tr>

    <tr>
      <td>
        Mobile Number
      </td>

      <td>
        Add your WhatsApp Integrated number with country code (for example, 918889500122)
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Ensure the Request Type is `POST`.
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Enter HTTP Endpoint as the following: `https://app.quickreply.ai/integrations/api/clevertap/WHATSAPP/send-message`.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Share the URL with the QuickReply account manager to configure it with the WhatsApp account. Refer to [Set Up CleverTap Callbacks in QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply).
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message\
        Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Share the URL with the QuickReply account manager to configure it with the WhatsApp account. Refer to [Set Up CleverTap Callbacks in QuickReply](doc:quickreply#set-up-clevertap-callbacks-in-quickreply) .
      </td>
    </tr>
  </tbody>
</Table>

4. Add Headers from QuickReply. To do so, follow the steps to configure headers:
   1. Go to *Settings* > *CleverTap Integration* in QuickReply Dashboard.
   2. Copy the *Authorization Headers*.
   3. Paste the headers into the *Header* section in CleverTap.

<Image alt="Configure Headers" align="center" width="65% " border={true} src="https://files.readme.io/b93b1972c649d1067acbbbdaa9b099db3261ac6f521a21de3fb1c5c1ded21576-image.png">
  Configure Headers
</Image>

5. (Optional) Select *Markthis as default* to make this service provider the default provider for sending a WhatsApp message via QuickReply.
6. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
7. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
8. Test the integration and click **Save** to trigger a test message and automatically save your credentials.

## Set Up CleverTap Callbacks in QuickReply

To set up CleverTap callbacks with QuickReply, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with QuickReply**: Copy both URLs and the WhatsApp phone number used in CleverTap, and send them to the QuickReply Account Manager or email [help@quickreply.ai](mailto:help@quickreply.ai).

<Image alt="Callback URLs" align="center" width="65% " border={true} src="https://files.readme.io/33695bf450091675cae04a63f9fcdc03d5b8a0fa04c6d77d7b8b718bbdb52b6b-image.png">
  Callback URLs
</Image>

Once configured, ensure that message delivery reports and inbound messages sync correctly between CleverTap and QuickReply.

> 📘 Message Templates
>
> You have to get your templates approved on the QuickReply dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the QuickReply integration, write to [help@quickreply.ai](mailto:help@quickreply.ai).

## Add Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, perform the following steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *QuickReply* on the CleverTap dashboard. 
2. Select *Templates* and click **+ Template**.

<Image title="Create a New Template" alt="Create a New Template" align="center" border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg">
  Create a New Template
</Image>

3. Enter the template name.

> 📘 Naming WhatsApp Templates
>
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
>
> For example, if you have multiple provider configurations, such as Phone\_1 and Phone\_2, you can use a particular template name once within Phone\_1 and then again on Phone\_2.

4. Select the language in which you want to display the message.
5. Select the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, or *Location*.
6. Create a [Limited Time Offer Template](doc:whatsapp-message-templates#limited-time-offer-templates), if required.
7. Enter the message content.
8. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).

<Image alt="Define Template Content" align="center" border={true} src="https://files.readme.io/5bd5090-Generic_template_create.jpg">
  Define Template Content
</Image>

9. Click **Save Template**.

## Test a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

# Create Campaign

For detailed instructions on creating a WhatsApp campaign using QuickReply as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

# Create a Journey

For detailed instructions on creating a WhatsApp journey using QuickReply as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).
