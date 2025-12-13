---
title: Setup (COPY)
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

1. From the dashboard, navigate to *Settings* > *Engage* > *Channels* > *Email*.
2. Click **+ Provider** to add a provider. 

<Image title="Click +Provider" alt={1162} align="center" border={true} src="https://files.readme.io/9206de0-Plus_provider.png">
  Add Provider
</Image>

3. Add the email provider's information.
4. Click **Save**.
5. Click *Send Test Email* to check if the provider has been set up correctly and can send emails.

## Provider Operations

This section describes actions for the available email service providers.

<Image title="Email Provider Operations" alt={736} align="center" border={true} src="https://files.readme.io/36c908a-Email_Operations.png">
  Provider Operations
</Image>

### Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active *Campaigns* or *Journeys* for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Archive* from the list. 

### Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting the email service provider will remove all existing data from our system and stop any active *Campaigns* or *Journeys*.  The deleted provider will not be available for use in the future, as well as the corresponding provider stats won't be retained.

Follow the steps to delete an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Delete* from the list.

### Edit Settings

Edit the email settings to change *Provider credentials*.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Edit settings* from the list. The *Provider credentials* window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider is working correctly. 
6. Click **Save**.

### Mark as Default

Set a service provider as default so that the same provider is used for delivering your emails. 

1. Follow the steps to set a default email service provider:
2. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
3. Click the ellipsis next to the provider. 
4. Select *Mark as Default* from the list.

# Inbox Previews

Before you can use inbox previews, you must enable them. Inbox previews with code analysis let you view an analysis of your HTML code. It also provides the capability to view previews across devices and inboxes before you send out a campaign. 

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

<Image title="Enable or Disable Inbox Preview" alt={1172} align="center" border={true} src="https://files.readme.io/49e8f2d-Enable_an_inbox_preview.png">
  Enable or Disable Inbox Previews
</Image>

The *Previews* tab lists the available email inboxes. For example, a mobile device that runs Gmail on Android 8 or a computer that runs Apple Mail 10 on an OS X 10.10 operating system. 

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.\
> This feature is not available for trial accounts.

# Advanced Setup

## AppsFlyer OneLink

Deep linking gives your app users the most seamless experience possible by guiding them securely and contextually to in-app information.

CleverTap automatically wraps all links in the email body to track clicks. When a user clicks on any of the links in the email, this may lead to several redirects. Turning off click tracking for deep links is one option for marketers who wish to send users straight to the content.

The other option is to leverage the AppsFlyer OneLink with branded links. Doing so can provide your app users with the greatest experience possible as it directs them to a specific landing page, the app store, or in-app content. All this while, CleverTap tracks the click and assists in boosting conversion rates.

<Image title="CleverTap + AppsFlyer Integration New Scenario" alt={3840} align="center" width="smart" border={true} src="https://files.readme.io/c7cedb7-CT_AF_Integration.png">
  AppsFlyer OneLink Integration
</Image>

### Set Up AppsFlyer OneLink(s)

The following are the steps to enable this feature:

#### 1. Set Up OneLink(s) in AppsFlyer

To use the AppsFlyer OneLink feature on the CleverTap dashboard, you must first set up a Branded OneLink on your AppsFlyer account. To set up branded OneLink in AppsFlyer, refer to these [steps](https://support.appsflyer.com/hc/en-us/articles/7696943216145-CleverTap-ESP-integration-with-AppsFlyer#step-3-configure-links-for-your-email-campaigns?utm_source=clevertap_dashboard).

#### 2. Set Up OneLink(s) in CleverTap Dashboard

To set up OneLink on the CleverTap dashboard:

a. Navigate to *Settings* > *Channel* > *Email* > *Advanced Setup* on the dashboard and click **AppsFlyer OneLink** dropdown.

<Image title="Click the Dropdown to Add AppsFlyer OneLink" alt="Advance Setup" align="center" border={true} src="https://files.readme.io/64cb245-Click_the_Dropdown_to_Add_AppsFlyer_OneLink.png">
  Advance Setup
</Image>

  b. Enter your AppsFlyer OneLink domain or sub-domain and click **Add**.

<Image title="Click Add to Add the OneLink" alt="Add AppsFlyer OneLink" align="center" border={true} src="https://files.readme.io/d6aba01-Click_Add_to_Add_the_OneLink.png">
  Add AppsFlyer OneLink
</Image>

> 🚧 Adding a Domain
>
> You can add a maximum of 20 valid domains or sub-domains.

  c. Click **Save** to save the domain.

<Image title="Click Save to Save the Added OneLink" alt="Save AppsFlyer OneLink" align="center" border={true} src="https://files.readme.io/ced9b07-Click_Save_to_Save_the_Added_OneLink.png">
  Save AppsFlyer OneLink
</Image>

  The message *AppsFlyer domain deeplink successfully saved* displays at the top.

<Image title="AppsFlyer OneLink Saved Successfully" alt="AppsFlyer Domain Deeplink Success" align="center" border={true} src="https://files.readme.io/cb41781-AppsFlyer_OneLink_Saved_Successfully.png">
  AppsFlyer Domain Deeplink Success
</Image>

### Disable Tracking via AppsFlyer OneLink

If you want to avoid click tracking via AppsFlyer OneLink, add the following tag for all the required links in your email:

```html
<a data-track="off" href="donotoverrride"> Your link </a>
```

AppsFlyer OneLink does not apply to links with this tag.

> 🚧 Note
>
> Turn off click tracking from your email service provider's dashboard for one link redirection to function as intended. CleverTap will receive the click data directly from AppsFlyer.

> ❗️ Invalid AppsFlyer Branded OneLink
>
> AppsFlyer does not send the click data for invalid OneLink URLs configured in an Email campaign to CleverTap.

## Font Manager

 This feature enables you to add and manage custom fonts and use them in your email campaigns. It simplifies font management across the *Drag & Drop* and *Rich Media* editors.

> 📘 Feature Availability
>
> The feature is available to customers on the Advanced and Cutting Edge plans.

### Add Custom Font

You can add custom fonts by navigating to  Settings *>\_Channel* > *Email* > *Advanced Setup* from the CleverTap dashboard. You can add **up to 100 custom fonts**. 

The following are the steps to add a custom font:

1. From the *Advanced Setup* page, click **Font Manager**.

<Image alt="Font Manager" align="center" border={true} src="https://files.readme.io/73b41e4-image.png">
  Font Manager
</Image>

2. Click **+ Custom Font**. The *Add Font* popup opens.

<Image alt="Add Custom Font" align="center" width="50% " border={true} src="https://files.readme.io/08ba774-Add_Font_Popup.png">
  Add Custom Font
</Image>

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
         *Font Name*
      </td>

      <td>
        Uniquely identifies the font. This field has a limit of up to 50 characters.
      </td>
    </tr>

    <tr>
      <td>
         *Font Family*
      </td>

      <td>
        Defines the style applied to the font. This field has a limit of up to 50 characters. The custom font family must match the name of the font face in the CSS file.
      </td>
    </tr>

    <tr>
      <td>
        *Font URL*
      </td>

      <td>
        If the font is not on your local system, you can select this option to add the URL for the font you want to add. The URL must point to a CSS file.\
        If your custom font is a public font available on the web, you can directly add the URL for the font.\
        If you upload the font to your private server, ensure that CORS is enabled on the server that provides the custom font file.
      </td>
    </tr>

    <tr>
      <td>
        *Upload Font*
      </td>

      <td>
        If you already have a font downloaded on your local system, choose *Upload Font*, and click **Upload** to upload the CSS file for your custom font. The file size should be a maximum of 1 MB.  

        The custom font file must have the following header: `Access-Control-Allow-Origin: \*`. When defining font URLs in the src attribute, utilizing the `https` protocol is essential. Refer to the [sample CSS code](doc:setup-custom-font#sample-css-code).
      </td>
    </tr>

    <tr>
      <td>
        * *Fallback Font*
      </td>

      <td>
        <li> Not all email clients support custom fonts. The following are some of the email clients that support custom fonts:
        <ul> <li> AOL Mail </li><li> Native Android Mail App(excluding Gmail)</li> <li> Apple Mail </li> <li> iOS Mail </li> <li> Outlook 2000 </li> </ul> </li> <li> Select from the dropdown list specific system fonts to seamlessly replace custom fonts in unsupported email clients. </li> <li> When defining multiple Fallback fonts, they are used in the order selected (from left to right). </li>**Note**: Ensure you test the fallback font before publishing the campaign.
      </td>
    </tr>
  </tbody>
</Table>

\*The fields marked with asterisk sign are mandatory.

3. Click **Add** to add the custom font.

### Sample CSS code:

```css
@font-face {
  font-family: 'Dancing Script';
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url(https://fonts.gstatic.com/s/dancingscript/v25/If2RXTr6YS-zF4S-kcSWSVi_szLgiuEHiC4W.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
```

### Set Up Default Font

You can also set up the system and custom fonts as the default font for your email campaigns. Select the font from the *Default font* dropdown to set up the default font for your email campaigns. 

The default font cannot be deleted. If you still want to delete it, change the default font and then delete the required font.

<Image alt="Set Up Custom Font as Default Font" align="center" border={true} src="https://files.readme.io/0152270-Set_Up_Custom_Font_as_Default_font_.png">
  Set Up a Default Font
</Image>

### Delete Custom Font

You can delete one or multiple custom fonts to manage your custom font library. To delete a custom font

1. Select one or multiple custom fonts you want to delete. 
2. Click the ![](https://files.readme.io/16fa1cc-Ellipses_icon.png) icon and select *Delete*. The *Delete font?* popup opens, highlighting potential impacts on drafts and saved templates and prompting you to confirm your action.
3. Select *Delete* to successfully delete the custom font(s). A confirmation message is displayed.\
   Upon deleting the custom font, it is unavailable for use in both the *Drag & Drop* and Rich Media\_ editors.

<Image alt="Delete Custom Font" align="center" border={true} src="https://files.readme.io/82551f4-Delete_Custom_Font.gif">
  Delete Custom Font
</Image>

### Edit Custom Font

You can edit your custom font and update the font details.

1. Select the custom fonts you want to edit.
2. Click the ![](https://files.readme.io/3eec8d1-Ellipses_icon.png) icon and select *Edit*. The *Edit Font* popup opens.
3. You can update the required fields related to the custom font and click *Save* to save the changes. 

<Image alt="Edit Custom Fonts" align="center" border={true} src="https://files.readme.io/328e95b-Edit_Custom_Font.gif">
  Edit Custom Fonts
</Image>

The updated custom font is now available for both the *Drag & Drop* and \_Rich Media editors. When making changes to the custom font, an email alert is sent to the user updating the custom font and also to the account admin.

> 🚧 Delete or Edit Custom Font
>
> Editing or deleting custom fonts does not impact running, scheduled, and draft engagements. The modifications take effect for the campaigns created subsequent to your changes.
