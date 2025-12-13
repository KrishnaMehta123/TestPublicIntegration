---
title: Sinch
excerpt: Learn how to integrate Sinch with CleverTap for WhatsApp communication.
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

[Sinch India](https://sinch.com/in/) offers a powerful WhatsApp messaging solution that helps businesses engage customers with personalized and automated communication. By integrating Sinch India with CleverTap, you can:  

* Send just-in-time offers to customers to drive purchases.  
* Gather feedback on services to improve customer satisfaction.  
* Keep customers informed with real-time updates and notifications.

Powered by Sinch India, This Integration is scalable and reliable for your conversations.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Sinch India. The CleverTap and Sinch India integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Sinch India](mailto:support.cm@sinch.com) for support and resolution.

# Prerequisites for Integration

Check that you have the following:

* The WhatsApp add-on enabled on the CleverTap account in addition to the Basic or Essentials Plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed.
* You must have Sinch India WhatsApp Business API.

# Integrate Sinch India with CleverTap

This process involves the following three steps:

1. [Find Sinch India WhatsApp account credentials](doc:sinch#find-sinch-india-whatsapp-account-credentials)
2. [Configure CleverTap dashboard](doc:sinch#configure-clevertap-dashboard)
3. [Set up CleverTap callbacks in Sinch India platform](doc:sinch#set-up-clevertap-callbacks-in-sinch-india-platform)

## Find Sinch India WhatsApp account credentials

We recommend that you keep the following information handy before starting with the configuration on the CleverTap dashboard:

* HTTP Endpoint
* Username and password

Reach out to the Sinch India WhatsApp support team. Raise a request at **Sinch mobile email** and expect a response with - WhatsApp account details such as Username, Password, WhatsApp number.

## Configure CleverTap dashboard

To configure the CleverTap dashboard:

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
        Enter the nickname as Sinch India or Sinch \<10 digit phone number> for easy reference.
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
        HTTP End Point
      </td>

      <td>
        Paste the URL received from the Sinch India team.\
        Check that the URL is in HTTPS format, that is, your URL must begin with **https\://**.
      </td>
    </tr>

    <tr>
      <td>
        Headers
      </td>

      <td>
        Click **Header** >\
        Enter the Key name as a user and enter the user value received from Sinch India.\
        Enter the second key name as the password and enter the value received from Sinch India.
      </td>
    </tr>
  </tbody>
</Table>

4. (Optional) Select *Mark this as default* to make this service provider the default provider when sending a WhatsApp message via Sinch India.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.
7. Send a Test WhatsApp notification: 

<Image title="Send Test Message on WhatsApp" alt="Send a test message on whatsapp" align="center" border={true} src="https://files.readme.io/c384922-sendtest.png">
  Send a Test Message on WhatsApp
</Image>

## Set Up CleverTap Callbacks in Sinch India platform

To set up CleverTap callbacks in Sinch India platform, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Sinch* from the CleverTap dashboard. You will find the *Delivery Report Callback URL* and *Inbound Message Callback URL* under the *Provider Configuration* page.
2. **Share Callback URLs with Sinch India**: Copy the Delivery and Inbound report callback URLs and send them to the Sinch India WhatsApp support team for configuration.

<Image alt="Callback URLs" align="center" width="65% " border={true} src="https://files.readme.io/17b2d251719811d51b3ba0ae7173be50be62ca9e7e716c2c445c2c6ed21362fb-image.png">
  Callback URLs
</Image>

Once configured, these webhooks ensure that message delivery reports and inbound messages sync correctly between CleverTap and Sinch India.

> 📘 Note:
>
> You have to get your templates approved on the Sinch dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the Sinch India integration, write to [support.cm@sinch.com](mailto:support.cm@sinch.com).

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

For detailed instructions on creating a WhatsApp campaign using Sinch India as the provider, refer to [Create a WhatsApp Campaign](doc:create-message-whatsapp).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using Sinch India as the provider, refer to [Create a WhatsApp Journey](doc:engagement-nodes-whatsapp).
