---
title: Setup
excerpt: Understand how to set up Email as a channel for your marketing campaigns.
deprecated: false
hidden: true
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

This section covers various email tasks, including the integrations, and inbox previews. No matter the type of customer emails, all businesses have the same goal to get to the correct recipient's inbox. By setting up your email correctly, you ensure successful email deliverability.

# Email Integrations

Before you can create email campaigns, you must integrate an email service provider with CleverTap.

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
        <li> This is a mandatory field. </li> <li> You get this key while setting up the provider dashboard. For more on finding the API key for CleverTap's default service provider, refer to the [Creating API Key ](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/api-keys#creating-an-api-key) section  </li>
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
4. Click _Send Test Email_ to check if the provider has been set up correctly and can send emails.

## Provider Operations

This section describes actions for the available email service providers.

<Image align="center" border={true} caption="Provider Operations" src="https://files.readme.io/36c908a-Email_Operations.png" />

### Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active _Campaigns_ or _Journeys_ for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats.

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
2. Click the ellipsis next to the provider.
3. Select _Archive_ from the list.

### Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting the email service provider will remove all existing data from our system and stop any active _Campaigns_ or _Journeys_. The deleted provider will not be available for use in the future, as well as the corresponding provider stats won't be retained.

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
5. Click **Send Test Email** to check that the provider is working correctly.
6. Click **Save**.

### Mark as Default

Set a service provider as default so that the same provider is used for delivering your emails.

1. Follow the steps to set a default email service provider:
2. From the CleverTap dashboard, navigate to _Settings > Channels > Email > Providers_ tab.
3. Click the ellipsis next to the provider.
4. Select _Mark as Default_ from the list.

# Inbox Previews

Before you can use inbox previews, you must enable them. Inbox previews with code analysis let you view an analysis of your HTML code. It also provides the capability to view previews across devices and inboxes before you send out a campaign.

<Callout icon="🚧" theme="warn">
  **Account Specifications**

  Email previews are available only if you have opted for the email add-on from CleverTap.
</Callout>

## Enable or Disable Inbox Previews

To enable or disable the inbox preview, perform the following steps:

1. From the dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _Email_.
2. Select the _Previews_ tab.
3. Select a client from the list.
4. Click on the ellipsis and click **Enable** or **Disable**.

<Callout icon="📘" theme="info">
  **Multi-select**

  You can also select multiple clients, then enable or disable previews by clicking **Enable in inbox previews** or **Disable in inbox previews**.
</Callout>

<Image align="center" border={true} caption="Enable or Disable Inbox Previews" src="https://files.readme.io/49e8f2d-Enable_an_inbox_preview.png" />

The _Previews_ tab lists the available email inboxes. For example, a mobile device that runs Gmail on Android 8 or a computer that runs Apple Mail 10 on an OS X 10.10 operating system.

<Callout icon="🚧" theme="warn">
  **Account Specifications**

  Email previews are available only if you have opted for the email add-on from CleverTap.  
  This feature is not available for trial accounts.
</Callout>

# Advanced Setup

## AppsFlyer OneLink

Deep linking gives your app users the most seamless experience possible by guiding them securely and contextually to in-app information.

CleverTap automatically wraps all links in the email body to track clicks. When a user clicks on any of the links in the email, this may lead to several redirects. Turning off click tracking for deep links is one option for marketers who wish to send users straight to the content.

The other option is to leverage the AppsFlyer OneLink with branded links. Doing so can provide your app users with the greatest experience possible as it directs them to a specific landing page, the app store, or in-app content. All this while, CleverTap tracks the click and assists in boosting conversion rates.

<br />

<Image align="center" border={true} caption="AppsFlyer OneLink Integration" src="https://files.readme.io/c7cedb7-CT_AF_Integration.png" />

### Set Up AppsFlyer OneLink(s)

The following are the steps to enable this feature:

#### 1. Set Up OneLink(s) in AppsFlyer

To use the AppsFlyer OneLink feature on the CleverTap dashboard, you must first set up a Branded OneLink on your AppsFlyer account. To set up branded OneLink in AppsFlyer, refer to these [steps](https://support.appsflyer.com/hc/en-us/articles/7696943216145-CleverTap-ESP-integration-with-AppsFlyer#step-3-configure-links-for-your-email-campaigns?utm_source=clevertap_dashboard).

#### 2. Set Up OneLink(s) in CleverTap Dashboard

To set up OneLink on the CleverTap dashboard:

a. Navigate to _Settings_ > _Channel_ > _Email_ > _Advanced Setup_ on the dashboard and click **AppsFlyer OneLink** dropdown.

<Image align="center" border={true} caption="Advance Setup" src="https://files.readme.io/64cb245-Click_the_Dropdown_to_Add_AppsFlyer_OneLink.png" />

b. Enter your AppsFlyer OneLink domain or sub-domain and click **Add**.

<Image align="center" border={true} caption="Add AppsFlyer OneLink" src="https://files.readme.io/d6aba01-Click_Add_to_Add_the_OneLink.png" />

<Callout icon="🚧" theme="warn">
  **Adding a Domain**

  You can add a maximum of 20 valid domains or sub-domains.
</Callout>

c. Click **Save** to save the domain.

Save AppsFlyer OneLink

The message _AppsFlyer domain deeplink successfully saved_ displays at the top.

<Image align="center" border={true} caption="AppsFlyer Domain Deeplink Success" src="https://files.readme.io/cb41781-AppsFlyer_OneLink_Saved_Successfully.png" />

### Disable Tracking via AppsFlyer OneLink

If you want to avoid click tracking via AppsFlyer OneLink, add the following tag for all the required links in your email:

`data-ct-track="false"`

AppsFlyer OneLink does not apply to links with this tag.

<Callout icon="🚧" theme="warn">
  **Note**

  Turn off click tracking from your email service provider's dashboard for one link redirection to function as intended. CleverTap will receive the click data directly from AppsFlyer.
</Callout>

<Callout icon="❗️" theme="error">
  **Invalid AppsFlyer Branded OneLink**

  AppsFlyer does not send the click data for invalid OneLink URLs configured in an Email campaign to CleverTap.
</Callout>

## Font Manager

This feature enables you to add and manage custom fonts and use them in your email campaigns. It simplifies font management across the _Drag & Drop_ and _Rich Media_ editors.

> 📘 Feature Availability
>
> The feature is available to customers on the Advanced and Cutting Edge plans.

### Add Custom Font

You can add custom fonts by navigating to  Settings _>_Channel_ > _Email_ > _Advanced Setup_ from the CleverTap dashboard. You can add **up to 100 custom fonts**.

The following are the steps to add a custom font:

1. From the _Advanced Setup_ page, click **Font Manager**.

   <Image align="center" border={true} caption="Font Manager" src="https://files.readme.io/73b41e4-image.png" />
2. Click **+ Custom Font**. The _Add Font_ popup opens.  

   <Image align="center" border={true} caption="Add Custom Font" src="https://files.readme.io/08ba774-Add_Font_Popup.png" width="65% " />
3. Enter the following details:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field Name
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        _Font Name_
      </td>

      <td>
        Uniquely identifies the font. This field has a limit of up to 50 characters.
      </td>
    </tr>

    <tr>
      <td>
        _Font Family_
      </td>

      <td>
        Defines the style applied to the font. This field has a limit of up to 50 characters. The custom font family must match the name of the font face in the CSS file.
      </td>
    </tr>

    <tr>
      <td>
        _Font URL_
      </td>

      <td>
        If the font is not on your local system, you can select this option to add the URL for the font you want to add. The URL must point to a CSS file.  
        If your custom font is a public font available on the web, you can directly add the URL for the font.  
        If you upload the font to your private server, ensure that CORS is enabled on the server that provides the custom font file.
      </td>
    </tr>

    <tr>
      <td>
        _Upload Font_
      </td>

      <td>
        If you already have a font downloaded on your local system, choose _Upload Font_, and click **Upload** to upload the CSS file for your custom font. The file size should be a maximum of 1 MB.

        The custom font file must have the following header: `Access-Control-Allow-Origin: \*`. When defining font URLs in the src attribute, utilizing the `https` protocol is essential. Refer to the [sample CSS code](doc:setup-custom-font#sample-css-code).
      </td>
    </tr>

    <tr>
      <td>
        * _Fallback Font_
      </td>

      <td>
        <li> Not all email clients support custom fonts. The following are some of the email clients that support custom fonts:
        <ul> <li> AOL Mail </li><li> Native Android Mail App(excluding Gmail)</li> <li> Apple Mail </li> <li> iOS Mail </li> <li> Outlook 2000 </li> </ul> </li> <li> Select from the dropdown list specific system fonts to seamlessly replace custom fonts in unsupported email clients. </li> <li> When defining multiple Fallback fonts, they are used in the order selected (from left to right). </li>**Note**: Ensure you test the fallback font before publishing the campaign.
      </td>
    </tr>
  </tbody>
</Table>

*The fields marked with asterisk sign are mandatory.

3. Click **Add** to add the custom font.

### Sample CSS code:

```css
@font-face {
  font-family: 'Charis SIL';
  src: url('https://files.readme.io/4a21a4b-CharisSIL-Regular.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'Charis SIL';
  src: url('https://files.readme.io/1aa9ad5-CharisSIL-Bold.woff2') format('woff2');
  font-weight: bold;
  font-style: normal;
}

@font-face {
  font-family: 'Charis SIL';
  src: url('https://files.readme.io/5c11c12-CharisSIL-Italic.woff2') format('woff2');
  font-weight: normal;
  font-style: italic;
}

@font-face {
  font-family: 'Charis SIL';
  src: url('https://files.readme.io/9da06d0-CharisSIL-BoldItalic.woff2') format('woff2');
  font-weight: bold;
  font-style: italic;
}
```

### Set Up Default Font

You can also set up the system and custom fonts as the default font for your email campaigns. Select the font from the _Default font_ dropdown to set up the default font for your email campaigns.

The default font cannot be deleted. If you still want to delete it, change the default font and then delete the required font.

  

### Delete Custom Font

You can delete one or multiple custom fonts to manage your custom font library. To delete a custom font

1. Select one or multiple custom fonts you want to delete.
2. Click the ![](https://files.readme.io/16fa1cc-Ellipses_icon.png) icon and select _Delete_. The _Delete font?_ popup opens, highlighting potential impacts on drafts and saved templates and prompting you to confirm your action.
3. Select _Delete_ to successfully delete the custom font(s). A confirmation message is displayed.  
   Upon deleting the custom font, it is unavailable for use in both the _Drag & Drop_ and Rich Media_ editors.

![](https://files.readme.io/82551f4-Delete_Custom_Font.gif)  Delete Custom Font

### Edit Custom Font

You can edit your custom font and update the font details.

1. Select the custom fonts you want to edit.
2. Click the ![](https://files.readme.io/3eec8d1-Ellipses_icon.png) icon and select _Edit_. The _Edit Font_ popup opens.
3. You can update the required fields related to the custom font and click _Save_ to save the changes.

![](https://files.readme.io/328e95b-Edit_Custom_Font.gif)  Edit Custom Fonts

The updated custom font is now available for both the _Drag & Drop_ and _Rich Media editors. When making changes to the custom font, an email alert is sent to the user updating the custom font and also to the account admin.

> 🚧 Delete or Edit Custom Font
>
> Editing or deleting custom fonts does not impact running, scheduled, and draft engagements. The modifications take effect for the campaigns created subsequent to your changes.
