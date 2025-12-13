---
title: Using Attachments in Email
excerpt: >-
  Learn how to attach one or more files as part of the CleverTap email
  campaigns.
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

CleverTap allows you to attach files directly to your email campaigns and journeys. This helps marketers share downloadable content such as brochures, onboarding kits, and so on without redirecting users to external URLs. 

Here are some of the common cases:

* **Onboarding Kits**: Include welcome guides or product setup PDFs for new users.
* **Policy or Legal Documents**: Share terms and conditions, compliance forms, or updated policy documents.
* **Event Resources**: Send event passes, itineraries, and so on.
* **Customer Support**: Share product manuals, troubleshooting guides, or return forms.
* **Educational Resources**: Deliver course materials, certificates, or lesson plans to learners.

> 📘 Private Beta
>
> The Email Attachments feature is currently released in Private Beta. The feature is currently available for **SendGrid** and **Infobip** (with Advanced Email Add-on) providers. For early access, contact Customer Success Manager.

# Supported File Types and Limits

CleverTap supports uploading images and PDFs using flexible upload methods to help you include documents or media in your emails. Before uploading attachments, make sure your files meet the supported format and size limits outlined below:

<Table>
  <thead>
    <tr>
      <th>
        Attribute
      </th>

      <th>
        Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Supported file extensions
      </td>

      <td>
        The following are the supported file types for attachments: 

        `.pdf`

        , 

        `.doc`

        , 

        `.docx`

        , .

        `ics`

        , 

        `.jpg`

        , 

        `.png`

        , and 

        `.jpeg`
      </td>
    </tr>

    <tr>
      <td>
        Max number of files
      </td>

      <td>
        Up to 10 attachments per email
      </td>
    </tr>

    <tr>
      <td>
        Max file size
      </td>

      <td>
        <ul><li>2 MB per document (`.pdf`, `.doc`, `.docx`, .`ics`)</li><li>1 MB per image (`.jpg`, `.png`, and `.jpeg`)</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

# Add Attachments to Email

You can add attachments to your email directly from the **Content Manager**, **What** section of the campaign builder, or **Email engagement node** of the journey builder.  

From the campaign creation setup, select **Attachments** from the *What* section, select one of the following options, and click **Attach**:

* **File URL**: Paste a publicly accessible HTTPS URL pointing to the file. Also, provide a friendly display name for the file, such as *Monthly Report.pdf*.  After uploading, you can rename the file by hovering over the uploaded attachment and clicking the ![](https://files.readme.io/42a29cd4fe23c9ab89b9e3f19c62f7896517787823c9b86827530e2ee9266a0b-Rename_icon.png) icon. The display name provided here (for example, *Monthly Report.pdf*) is visible to the end user in their inbox. Attachments are **not stored in CMS automatically** when uploaded via this option.

  <Image alt="Attach Files via Files URL" align="center" border={true} src="https://files.readme.io/8f8cb6b88c9106711de6ffe8e1e6c8cc72665c6fa37542336a8126688306401d-Attach_Files_via_URL.gif">
    Attach Files via Files URL
  </Image>
* **Device Storage**: Click to open your file browser and select the file you want to upload. Attachments are **not stored in CMS automatically** when uploaded via this option.

  <Image alt="Attach Files via Device Storage" align="center" border={true} src="https://files.readme.io/fb71219a6004ddb399ce79bd6582106269af7a31314eecf4058e6b18294083ab-Attach_File_via_Device_Storage.gif">
    Attach Files via Device Storage
  </Image>
* **Content Manager**: Click **Browse** to attach previously uploaded assets to the email campaign.

  <Image alt="Attach Files via Content Manager" align="center" border={true} src="https://files.readme.io/960462938a0e3f3acd65abf846eaa10fd7ac803adc83c48ed9725f4a82d0ff20-Attach_FIles_via_Content_Manager.gif">
    Attach Files via Content Manager
  </Image>

  The attached files and their file names and types are displayed under the *Preview* section on the right. The files are validated for size, extension, and name during this time. You can **rename** a file uploaded by clicking the ![](https://files.readme.io/b79e2947976e8baefc1fba973c0a391d91528b5b933eb4e3a4eb7190ed62be37-Rename_icon.png) icon next to the file name and entering a display-friendly name. The display name provided here is visible to the end user in their inbox. You can remove any file by clicking the ![](https://files.readme.io/77cb7f4c433c6442788e32e4d6ec56906e305942d35b0c7c5e7f9f4a4c8949ad-70a339a-delete_all_icon.jpg) icon next to the uploaded file.\ <br />

  > 🚧 Maximum File Size Upload
  >
  > The overall email size must stay within your Email Service Provider’s limits as follows:
  >
  > * 30MB for SendGrid
  > * 24MB for Infobip

Once you have attached your files, add all the *Sender Details*. If you add CC/BCC recipients under *Sender Details*, they receive the same attachments as the primary recipient.

> 📘 Private Beta
>
> Adding CC/BCC recipients to email campaign is currently in Private Beta. For more information, refer to [CC/BCC](doc:create-message-email#ccbcc).

# Errors

CleverTap does not track attachment downloads or opens by the user. Failure to add attachments during campaign send results in the email not being delivered. In such cases, a **Notification Failed** event is triggered, and a **soft bounce** is recorded with the error type as *Attachment errors*. However, the user is **not unsubscribed** from future emails. The error appears under the *Errors* tab of the Campaign *Stats* page.

<Image alt="Email Attachment Errors" align="center" border={true} src="https://files.readme.io/6fb0e04c57b85a2861be36ee9cc5313fff2dbfc31d29c506d71a566ca296e227-Email_Attachment_Errors_Stats.png">
  Email Attachment Errors
</Image>
