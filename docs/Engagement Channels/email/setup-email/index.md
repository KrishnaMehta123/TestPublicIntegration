---
title: Setup
excerpt: Understand how to set up Email as a channel for your marketing campaigns.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
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

# Setup Provider

Once you have integrated an email service provider with CleverTap, you can set up your email service provider.

To add a provider, perform the following steps:

1. From the dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _Email_.
2. Click **+ Provider** to add a provider.  

   <Image align="center" border={true} caption="Add Provider" src="https://files.readme.io/9206de0-Plus_provider.png" />
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
        Select your

        _Email Provider_

        from the dropdown list. Select

        _SMPT_

        if the provider is not listed
      </td>
    </tr>

    <tr>
      <td>
        Nickname
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> Enter the nickname for the Email Provider to uniquely identify it. </li>
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> Callback URL is used to get the bounce, rejection, and subscription information from the Email Partner to CleverTap. </li> <li> It is a read-only field that is pre-populated with CleverTap's callback URL. </li>
      </td>
    </tr>

    <tr>
      <td>
        Host
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> This is the address of the email server. In this case, it is the domain name (e.g., [http://smtp.sendgrid.com](http://smtp.sendgrid.com)) that directs to the server responsible for sending emails. </li>
      </td>
    </tr>

    <tr>
      <td>
        Port
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> This is the specific gate on the email server through which communication occurs. For example, 587. </li>
      </td>
    </tr>

    <tr>
      <td>
        API Key
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> You get this key while setting up the provider dashboard. For more on finding the API key for CleverTap's default service provider, refer to the [Creating API Key ](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/api-keys#creating-an-api-key) section </li>
      </td>
    </tr>

    <tr>
      <td>
        Default From Address
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> Enter the default email address you want to use for sending your email campaigns.</li> <li> The email address will be pre-populated under the *From Email Address* field as a default value when creating an Email campaign. If you want to personalize the *From Address*  field for your email campaign, refer to  [sender details](doc:create-message-sender-details#sender-details) </li>
      </td>
    </tr>

    <tr>
      <td>
        Default Reply Address
      </td>

      <td>
        <li> This is a mandatory field. </li> <li> Enter the default email address to which you want your users to reply to the campaign. </li> <li> The email address will be used to pre-populate the  *Reply-to Email Address* field as a default value when creating an Email campaign. If you want to personalize the *Reply-to Email Address* field, refer to [sender details](doc:create-message-sender-details#sender-details) .</li>
      </td>
    </tr>

    <tr>
      <td>
        Email Preference Center
      </td>

      <td>
        <li> Select *System* from the dropdown to use a pre-built preference center with a sample preview. </li>  <li>Select *Custom URL* to add your hosted unsubscription page URL. </li> <li> Select *None* if you want to manage the email preferences directly on your own. </li>  For more information, [Manage Email Preferences](doc:manage-email-preferences#configure-email-preference-center).
      </td>
    </tr>
  </tbody>
</Table>

3. Click **Save**.
4. (Optional) Click **Send Test Email** to check if the provider has been set up correctly and can send emails.

## Provider Operations

This section describes actions for the available email service providers.

![](https://files.readme.io/36c908a-Email_Operations.png "Email Provider Operations") Provider Operations

### Archive Service Providers

You can archive any current email service providers from the email settings. Archiving the email service provider stops any active _Campaigns_ or _Journeys_ for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats.

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
2. Click the ellipsis next to the provider.
3. Select _Archive_ from the list.

### Delete Service Providers

You can delete any current email service providers from the email settings. Deleting the email service provider will remove all existing data from our system and stop any active _Campaigns_ or _Journeys_. The deleted provider will not be available for use in the future, and the corresponding provider stats won't be retained.

Follow the steps to delete an email service provider:

1. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
2. Click the ellipsis next to the provider.
3. Select _Delete_ from the list.

### Edit Settings

Edit the email settings to change _Provider credentials_.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
2. Click the ellipsis next to the provider.
3. Select _Edit settings_ from the list. The _Provider credentials_ window displays.
4. Change the required information.
5. Click **Send Test Email** to check that the provider works correctly.
6. Click **Save**.

### Mark as Default

Set a service provider as the default so that the same provider is used to deliver your emails.

1. Follow the steps to set a default email service provider:
2. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
3. Click the ellipsis next to the provider.
4. Select _Mark as Default_ from the list.

# Inbox Previews

Before you can use inbox previews, you must enable them. Inbox previews with code analysis let you view an analysis of your HTML code. It also allows viewing previews across devices and inboxes before you send out a campaign.

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.

## Enable or Disable Inbox Previews

To enable or disable the inbox preview, perform the following steps:

1. From the dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _Email_.
2. Select the _Previews_ tab.
3. Select a client from the list.
4. Click on the ellipsis and click **Enable** or **Disable**.

> 📘 Multi-select
>
> You can also select multiple clients, then enable or disable previews by clicking **Enable in inbox previews** or **Disable in inbox previews**.

![](https://files.readme.io/49e8f2d-Enable_an_inbox_preview.png "Enable or Disable Inbox Preview")  Enable or Disable Inbox Previews

The _Previews_ tab lists the available email inboxes. For example, a mobile device that runs Gmail on Android 8 or a computer that runs Apple Mail 10 on an OS X 10.10 operating system.

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.  
> This feature is not available for trial accounts.

# Advanced Setup

The _Advance Setup_ for email campaigns in CleverTap allows users to configure more complex and fine-tuned settings for their email campaigns. This feature typically includes options such as:

* _[AppsFlyer OneLink](doc:appsflyer-onelink)_: Enables you to set up deep links using Appsflyer, guiding recipients directly to specific in-app content when they click on an email link.
* _[Font Manager](doc:font-manager)_: Allows font customization within the email template, giving more control over the look and feel of the email design to align with brand guidelines.
* _[Email Preference Center](doc:manage-email-preferences)_: Enables you to manage user email preferences, allowing them to choose which types of emails they want to receive, improving the relevance of communications.
* _[One-Click Unsubscribe](doc:one-click-unsubscribe)_: Offers recipients a quick and easy way to unsubscribe from future emails with a single click, ensuring compliance with regulations and enhancing the user experience.
