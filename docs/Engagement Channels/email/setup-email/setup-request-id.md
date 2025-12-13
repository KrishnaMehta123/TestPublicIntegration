---
title: Setup
excerpt: Understand how to set up Email as a channel for your marketing campaigns.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

This section covers various email tasks, including the integrations and inbox previews. No matter the type of customer emails, all businesses have the same goal of getting to the correct recipient's inbox. By setting up your email correctly, you ensure successful email deliverability.

# Email Integrations

Before creating email campaigns, you must integrate an email service provider with CleverTap. 

CleverTap supports integrations with popular email service providers. Select your email service provider from the following list:

* [Mandrill](doc:mandrill) 
* [Amazon Simple Email Service](doc:amazon-simple-email-service) 
* [Postmark](doc:postmark) 
* [SendGrid](doc:sendgrid) 
* [Gmail/Google Apps](doc:gmail-google-apps) 

For all other service providers, use [Generic SMTP](doc:generic-smtp).

# Set Up Provider

Once you have integrated an email service provider with CleverTap, you can set up your email service provider.

To add a provider, perform the following steps:

1. From the dashboard, navigate to *Settings* > *Engage* > *Channels* > *Email*.
2. Click **+ Provider** to add a provider. 

<Image title="Click +Provider" alt={1162} align="center" border={true} src="https://files.readme.io/9206de0-Plus_provider.png" /> Add Provider











3. Add the following provider details:
<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Column
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Provider
      </td>

      <td>
        Select your *Email Provider* from the dropdown list. Select *SMPT* if the provider is not listed
      </td>
    </tr>

    <tr>
      <td>
        Nickname
      </td>

      <td>
        This is a mandatory field. Enter the nickname for the Email Provider to uniquely identify it.
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        <ul><li> This is a mandatory field. </li> <li> Callback URL is used to get the bounce, rejection, and subscription information from the Email Partner to CleverTap. </li> <li> It is a read-only field that is pre-populated with CleverTap's callback URL. </li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Host
      </td>

      <td>
        <ul><li> This is a mandatory field. </li> <li> This is the address of the email server. In this case, it is the domain name (for example, [http://smtp.sendgrid.com](http://smtp.sendgrid.com)) that directs to the server responsible for sending emails.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Port
      </td>

      <td>
        <ul><li> This is a mandatory field. </li> <li> This is the specific gate on the email server through which communication occurs. For example, 587. </li></ul>
      </td>
    </tr>

    <tr>
      <td>
        API Key
      </td>

      <td>
        <ul><li> This is a mandatory field. </li> <li> You get this key while setting up the provider dashboard. For more on finding the API key for CleverTap's default service provider, refer to the [Creating API Key ](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/api-keys#creating-an-api-key) section  </li></ul>
      </td>
    </tr>

    <tr>
      <td>
        From Address
      </td>

      <td>
        <ul><li> This is a mandatory field. </li> <li> Enter the email address you want to use for sending your email campaigns.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Reply Address
      </td>

      <td>
        Enter the email address to which you want your users to reply to the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Email Preference Center
      </td>

      <td>
        <ul><li> Select _System_ from the dropdown to use a pre-built preference center with a sample preview. </li>  <li>Select _Custom URL_ to add your hosted unsubscription page URL. </li> <li> Select _None_ if you want to manage the email preferences directly on your own. </li> </ul>For more information, [Manage Email Preferences](doc:manage-email-preferences#configure-email-preference-center).
      </td>
    </tr>

    <tr>
      <td>
        Add request ID
      </td>

      <td>
        Selecting this option adds a unique, 36-character system-generated identifier (`request_id`) to every email sent using this provider configuration. For example, `fbeaf62c-f5db-40c5-bc5b-58edc50b91b4`.  

        * \*Note\*\*: This feature is currently in Private Beta and is supported for SendGrid and the Infobip Email Add-on email service providers. For more information, refer to [Add Request ID](doc:setup-request-id#add-request-id).
      </td>
    </tr>
  </tbody>
</Table>
3. Click **Save**.
4. (Optional) Click **Send Test Email** to check if the provider has been set up correctly and can send emails.

# Add Request ID

In PBS recurring and live campaigns, the same user may receive multiple emails in a single day, sometimes just seconds apart. As these messages are part of the same campaign, it can be difficult to differentiate when tracking delivery or engagement for each individual message. 

To solve this, you can enable the *Add request ID* option while setting up the email provider. This unique system-generated identifier (`systemRequestId)`) is assigned to every email sent using that provider configuration.

<Image alt="Add Request ID" align="center" width="35%" border={true} src="https://files.readme.io/8c40201c0deaf001517889d8fca6fb6044b4ecd24a19baa30b98aaa5fdf3f9e5-Add_Request_ID.png" />  Add Request ID

The `systemRequestId` helps you track each email using the `systemRequestId` to uniquely identify its progress across the following key events: Notification Sent, Notification Failed, Notification Delivered, Notification Viewed, and Notification Clicked. It is available as an event property for these events, helping you easily distinguish multiple messages sent as part of the same campaign and debug delivery issues more effectively.

While particularly useful for PBS recurring and live campaigns, this feature enhances message-level visibility for all campaign types.

Once enabled, CleverTap generates a unique, random request ID for every message sent using the selected provider. This setting applies to all campaigns that use that provider configuration. Messages sent before enabling this option remain unaffected.

You can disable this option anytime by editing the provider configuration. Disabling it stops new messages from including the request ID; however, messages sent prior to the change retain their existing identifiers.

# Provider Operations

This section describes actions for the available email service providers.

<Image title="Email Provider Operations" alt={736} align="center" border={true} src="https://files.readme.io/36c908a-Email_Operations.png" />  Provider Operations

## Archive Service Providers
You can archive any current email service providers from the email settings. Archiving the email service provider stops any active *Campaigns* or *Journeys* for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Archive* from the list. 

## Delete Service Providers

You can delete any current email service providers from the email settings. Deleting the email service provider will remove all existing data from our system and stop any active *Campaigns* or *Journeys*.  The deleted provider will not be available for use in the future, and the corresponding provider stats won't be retained.

Follow the steps to delete an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Delete* from the list.

## Edit Settings

Edit the email settings to change *Provider credentials*.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Edit settings* from the list. The *Provider credentials* window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider works correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as the default so that the same provider is used to deliver your emails. 

1. Follow the steps to set a default email service provider:
2. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
3. Click the ellipsis next to the provider. 
4. Select *Mark as Default* from the list.

# Inbox Previews

Before you can use inbox previews, you must enable them. Inbox previews with code analysis let you view an analysis of your HTML code. It also allows viewing previews across devices and inboxes before you send out a campaign. 

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.

## Enable or Disable Inbox Previews

To enable or disable the inbox preview, perform the following steps:


1. From the dashboard, navigate to *Settings* > *Engage* > *Channels* > *Email*.
2. Select the *Previews* tab.
3. Select a client from the list.
4. Click on the ellipsis and click **Enable** or **Disable**.

> 📘 Multi-select
>
> You can also select multiple clients, then enable or disable previews by clicking **Enable in inbox previews** or **Disable in inbox previews**.

<Image title="Enable or Disable Inbox Preview" alt={1172} align="center" border={true} src="https://files.readme.io/49e8f2d-Enable_an_inbox_preview.png" />  Enable or Disable Inbox Previews

The *Previews* tab lists the available email inboxes. For example, a mobile device that runs Gmail on Android 8 or a computer that runs Apple Mail 10 on an OS X 10.10 operating system. 

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.\
> This feature is not available for trial accounts.

# Advanced Setup

The *Advance Setup* for email campaigns in CleverTap allows users to configure more complex and fine-tuned settings for their email campaigns. This feature typically includes options such as:

* *[AppsFlyer OneLink](doc:appsflyer-onelink)*: Enables you to set up deep links using Appsflyer, guiding recipients directly to specific in-app content when they click on an email link.
* *[Font Manager](doc:font-manager)*: Allows font customization within the email template, giving more control over the look and feel of the email design to align with brand guidelines.
* *[Email Preference Center](doc:manage-email-preferences)*: Enables you to manage user email preferences, allowing them to choose which types of emails they want to receive, improving the relevance of communications.
* *[One-Click Unsubscribe](doc:one-click-unsubscribe)*: Offers recipients a quick and easy way to unsubscribe from future emails with a single click, ensuring compliance with regulations and enhancing the user experience.