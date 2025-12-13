---
title: Font Manager
excerpt: ''
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

 This feature enables you to add and manage custom fonts and use them in your email campaigns. It simplifies font management across the *Drag & Drop* and *Rich Media* editors.

> 📘 Feature Availability
>
> The feature is available to customers on the Advanced and Cutting Edge plans.

# Add Custom Font

You can add custom fonts by navigating to  Settings *>\_Channel* > *Email* > *Advanced Setup* from the CleverTap dashboard. You can add **up to 100 custom fonts**. 

The following are the steps to add a custom font:

1. From the *Advanced Setup* page, click **Font Manager**.

<Image alt="Font Manager" align="center" border={true} src="https://files.readme.io/73b41e4-image.png">
  Font Manager
</Image>

2. Click **+ Custom Font**. The *Add Font* popup opens.

<Image alt="Add Custom Font" align="center" width="70% " border={true} src="https://files.readme.io/6a899bb9a9afd1e8ba4902d0f326a6cd7c42b80c7734ce5e9c3553f53c7f3852-font_manager_new.png">
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

        The custom font file must have the following header: `Access-Control-Allow-Origin: \*`. When defining font URLs in the src attribute, utilizing the `https` protocol is essential. Refer to the [sample CSS code](doc:setup-custom-font#sample-css-code) .
      </td>
    </tr>

    <tr>
      <td>
        *Upload Font*
      </td>

      <td>
        If you already have a font file available on your local system, choose *Upload Font*, and click **Upload** to upload the CSS file for your custom font. The file size should be a maximum of 1 MB.
      </td>
    </tr>

    <tr>
      <td>
        * *Fallback to*
      </td>

      <td>
        <li> Not all email clients support custom fonts. The following are some of the email clients that support custom fonts:
        <ul> <li> AOL Mail </li><li> Native Android Mail App(excluding Gmail)</li> <li> Apple Mail </li> <li> iOS Mail </li> <li> Outlook 2000 </li> </ul> </li> <li> Select from the dropdown list specific system fonts to seamlessly replace custom fonts in unsupported email clients. </li> <li> When defining multiple Fallback fonts, they are used in the order selected (from left to right). </li>**Note**: Ensure you test the fallback font before publishing the campaign.
      </td>
    </tr>
  </tbody>
</Table>

\*The fields marked with asterisk sign are mandatory.

4. Click **Add** to add the custom font.

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

# Set Up Default Font

You can also set up the system and custom fonts as the default font for your email campaigns. Select the font from the *Default font* dropdown to set up the default font for your email campaigns. 

The default font cannot be deleted. If you still want to delete it, change the default font and then delete the required font.

<Image alt="Set Up Custom Font as Default Font" align="center" border={true} src="https://files.readme.io/0152270-Set_Up_Custom_Font_as_Default_font_.png">
  Set Up a Default Font
</Image>

# Delete Custom Font

You can delete one or multiple custom fonts to manage your custom font library. To delete a custom font

1. Select one or multiple custom fonts you want to delete. 
2. Click the ![](https://files.readme.io/16fa1cc-Ellipses_icon.png) icon and select *Delete*. The *Delete font?* popup opens, highlighting potential impacts on drafts and saved templates and prompting you to confirm your action.
3. Select *Delete* to successfully delete the custom font(s). A confirmation message is displayed.\
   Upon deleting the custom font, it is unavailable for use in both the *Drag & Drop* and Rich Media\_ editors.

<Image alt="Delete Custom Font" align="center" border={true} src="https://files.readme.io/82551f4-Delete_Custom_Font.gif">
  Delete Custom Font
</Image>

# Edit Custom Font

You can edit your custom font and update the font details.

1. Select the custom fonts you want to edit.
2. Click the ![](https://files.readme.io/3eec8d1-Ellipses_icon.png) icon and select *Edit*. The *Edit Font* popup opens.
3. You can update the required fields related to the custom font and click *Save* to save the changes. 

<Image alt="Edit Custom Fonts" align="center" width="70% " border={true} src="https://files.readme.io/5149c05cf018c6e7388d9719940a928b7cd61e46617f6461ba0b54a9e9f2d489-2024-11-29_17-02-40_1.gif">
  Edit Custom Fonts
</Image>

The updated custom font is now available for both the *Drag & Drop* and *Rich Media editors*. When making changes to the custom font, an email alert is sent to the user updating the custom font and also to the account admin.

> 🚧 Delete or Edit Custom Font
>
> Editing or deleting custom fonts does not impact running, scheduled, and draft engagements. The modifications take effect for the campaigns created subsequent to your changes.
