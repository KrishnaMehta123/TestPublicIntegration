---
title: AiSensy
excerpt: Learn how to integrate AiSensy with CleverTap for WhatsApp communication.
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

[AiSensy](https://www.aisensy.com/) offers a native integration with CleverTap that enables businesses to send WhatsApp broadcasts directly from the CleverTap dashboard. This integration allows you to:

* Trigger campaigns using pre-approved WhatsApp templates.
* Automate user engagement based on behavioral events.
* Track delivery and response metrics using CleverTap analytics.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by AiSensy. The CleverTap and AiSensy integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [AiSensy](mailto:support@aisensy.com) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

* The WhatsApp Campaigns feature is enabled on your CleverTap account.
* An active AiSensy account with WhatsApp Business API (WABA) access.
* A provisioned WhatsApp number from AiSensy.

> 📘 Enable the CleverTap add-on
>
> Check that you have enabled the CleverTap add-on in the AiSensy dashboard before proceeding with the integration.

# Integrate AiSensy with CleverTap

This process involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:aisensy#create-a-passcode-on-the-clevertap-dashboard)
2. [Configure CleverTap Dashboard](#configure-clevertap-dashboard)
3. [Set Up Callbacks in AiSensy](#set-up-callbacks-in-aisensy)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to its REST API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Configure CleverTap Dashboard

To set up AiSensy as your WhatsApp provider from the CleverTap dashboard:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect*.

2. Click **+ Add Provider** and select *Generic (Other)* from the Provider list.

<Image alt="Provider Setup" align="center" width="60% " border={true} src="https://files.readme.io/e451b36150e189f94b3d4082226e5ef5b9a8517791b6774746a9137ad43370e9-image.png">
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
        Enter the nickname as AiSensy\_WA for easy reference.
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
        Paste the following URL:`https://backend.aisensy.com/clever-tap/t1/messages`\
        Check that the URL is in HTTPS format, that is, your URL must begin with https//
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in AiSensy](doc:aisensy#set-up-callbacks-in-aisensy).
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Refer to [Set Up CleverTap Callbacks in AiSensy](doc:aisensy#set-up-callbacks-in-aisensy).
      </td>
    </tr>
  </tbody>
</Table>

4. Add Headers from AiSensy. To do so, follow the steps to configure headers:
   1. Go to *AiSensy Dashboard* > *Integrations* > *CleverTap* > click **Regenerate Key**.
   2. Copy the Authorization Headers.
   3. Paste the headers into the Header section in CleverTap.

<Image alt="Configure Headers" align="center" width="65% " border={true} src="https://files.readme.io/0bdb0c80b88f1b3e9786dadf8dbc5219d4831ee6d9499066dc6aa6b73921b2bc-image.png">
  Configure Headers
</Image>

5. (Optional) Select *Mark this as default* to make the service provider the default provider for sending a WhatsApp message via AiSensy.
6. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
7. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
8. Test the integration and click **Save** to trigger a test message and automatically save your credentials.

## Set Up Callbacks in AiSensy

Callbacks ensure delivery reports and inbound user messages from WhatsApp are synced back to CleverTap, enabling accurate tracking and engagement workflows.

To set up CleverTap callbacks with AiSensy, follow the steps below:

1. In the AiSensy dashboard, go to *Integrations* > *CleverTap*.
2. Click **Regenerate Key** under *CleverTap Header Key*.
3. In the CleverTap dashboard, go to *Settings* > *Channels* > *WhatsApp*. The *Delivery Report Callback URL* and *Inbound Message Callback URL* are under the Provider Configuration page. Copy them.

<Image alt="Callback URLs" align="center" width="45% " border={true} src="https://files.readme.io/931f649e1d2a8e6a9c805ef928b38b661294cc92d1d2597d120df3702259a820-image.png">
  Callback URLs
</Image>

4. Paste both callback URLs in AiSensy and click **Submit**.

Once configured, check that message delivery reports and inbound messages sync correctly between CleverTap and AiSensy.

You can now broadcast WhatsApp messages directly from the CleverTap dashboard using AiSensy.

# Add WhatsApp Message Templates

WhatsApp message templates are reusable, pre-approved messages you can send to users at scale, such as alerts, reminders, or promotional campaigns. For detailed instructions on creating and testing WhatsApp message templates, refer to [WhatsApp Message Templates](doc:whatsapp-message-templates).

# Create Campaign

For detailed instructions on creating a WhatsApp campaign using AiSensy as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

# Creating a Journey

For detailed instructions on creating a WhatsApp journey using AiSensy as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).
