---
title: Route Mobile
excerpt: WhatsApp Provider
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

[Route Mobile](https://routemobile.com/) is a global cloud communications platform that enables businesses to send messages via SMS, WhatsApp, RCS, and more. By integrating Route Mobile with CleverTap’s WhatsApp Business solution, you can send personalized, automated WhatsApp messages at scale using your Route Mobile-approved WhatsApp sender.

With this integration, you can:

* Trigger WhatsApp messages based on user actions or segments.
* Personalize content using CleverTap's enriched user profiles. 
* Track delivery, read status, and user engagement directly in CleverTap.

This setup combines Route Mobile’s reliable messaging infrastructure with CleverTap’s powerful engagement engine, enabling you to drive conversion-oriented conversations. 

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Route Mobile. The CleverTap and Route Mobile integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Route Mobile](mailto:support@routemobile.com) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites for Route Mobile.

* You must have the WhatsApp add-on enabled on the CleverTap account in addition to the Essentials Plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
* Ensure that you have the API URL and account credentials from Route Mobile. 

> 📘 Activating a New Phone Number via Route Mobile
>
> If you want to activate a new phone number with WhatsApp Business API via Route Mobile, contact your Account Manager from Route Mobile.

# Integrate Route Mobile with CleverTap

This process involves the following three steps:

1. [Find Route Mobile WhatsApp account credentials](doc:route-mobile#find-route-mobile-whatsapp-account-credentials)
2. [Configure CleverTap dashboard](doc:route-mobile#configure-clevertap-dashboard)
3. [Set Up CleverTap Callbacks with Route Mobile](doc:route-mobile#set-up-clevertap-callbacks-with-route-mobile)

## Find Route Mobile WhatsApp Account Credentials

CleverTap recommends that you keep the following information handy before starting with the configuration on the CleverTap dashboard:

* HTTP Endpoint
* Username and password

Contact the Route Mobile WhatsApp Support Team or raise a request at [Route Mobile](mailto:support@routemobile.com). The response will include the username, password, and WhatsApp number for your WhatsApp account.


## Configure CleverTap dashboard

To configure the CleverTap dashboard, perform the following steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and select *Generic (Other)* from the dropdown.

<Image alt="Provider Setup" align="center" width="65%" border={true} src="https://files.readme.io/885f26f7e2110aab22dd2bda2eba90bc4c3e187863d865a407301bc495da3a4d-image.png" />  Provider Setup

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
        Enter the nickname as Route Mobile &lt;10-digit phone number&gt; for easy\
        reference.
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
        Ensure the Request Type is *POST*.
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Paste the URL received from the Route Mobile team.\
        Ensure that the URL is in HTTPS format, i.e., your URL must begin with **https\://**.
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click **Header** and enter the following key-value-pairs: <li>Key: API-KEY</li><li>Value: &lt;Authentication Token&gt;</li> Contact to [support@routemobile.com](mailto:support@routemobile.com) for API key.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Report Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Share the URL with Route Mobile’s account manager to configure it with the WhatsApp account.
      </td>
    </tr>

    <tr>
      <td>
        Inbound Message\
        Callback URL
      </td>

      <td>
        This URL is generated automatically in the CleverTap dashboard. Share the URL with Route Mobile’s account manager to configure it with the WhatsApp account.
      </td>
    </tr>
  </tbody>
</Table>
4. (Optional) Select *Mark this as default to make this service provider the default provider* to send a WhatsApp message via Route Mobile.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification (refer to the following image).

<Image title="Send Test Message on WhatsApp" alt={1488} align="center" border={true} src="https://files.readme.io/c384922-sendtest.png" />  Send Test Message on WhatsApp











## Set Up CleverTap Callbacks with Route Mobile

To set up CleverTap callbacks with Route Mobile, perform the following steps:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with Route Mobile**: Copy both URLs and the WhatsApp phone number used in CleverTap, send them to the Route Mobile WhatsApp support team for configuration.

<Image alt="Callback URLs" align="center" width="75%" border={true} src="https://files.readme.io/cc474e967352120cb3db115ee543e49e98dda60cbe05e91aa5cffc2978a6ccb2-image.png" />  Callback URLs











Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Route Mobile.

> 📘 Message Templates
>
> You have to get your templates approved on the Route Mobile dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the Route Mobile integration, write to [support@routemobile.com](mailto:support@routemobile.com).

## Add Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, perform the following steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Provider Nickname* on the CleverTap dashboard. 
2. Select *Templates* and click **+ Template**.

<Image title="Create a New Template" alt="Create a New Template" align="center" border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg" />  Create a New Template
3. Enter the template name.

> 📘 Naming WhatsApp Templates
>
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
>
> For example, if you have multiple provider configurations, such as Phone\_1 and Phone\_2, you can use the a particular template name once within Phone\_1 and Phone\_2.

4. Select the language in which you want to display the message.
5. Select the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, or *Location*.
6. Create a [Limited Time Offer Template](doc:whatsapp-message-templates#limited-time-offer-templates), if required.
7. Enter the message content.
8. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).

<Image alt="Define Template Content" align="center" border={true} src="https://files.readme.io/5bd5090-Generic_template_create.jpg" /> Define Template Content

9. Click **Save Template**.

## Test a Message Template

For detailed instructions on testing a WhatsApp message template, refer to [Testing a Message Template](doc:whatsapp-message-templates#testing-a-message-template).

# Create Campaign

For detailed instructions on creating a WhatsApp campaign using Route Mobile as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

# Create a Journey

For detailed instructions on creating a WhatsApp journey using Route Mobile as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).