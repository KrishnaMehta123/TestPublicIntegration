---
title: Email Editor
excerpt: >-
  Learn about the HTML and AMP email templates offered by CleverTap out of the
  box.
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

The Email Editor tool is a feature available when building an email message in CleverTap. It lets you add content to pre-built templates or customize and build your templates. After creating an email template, you can use it in the current campaign or save it for future campaigns.

From the _What_ section in the Email builder, click **Go to Editor**.

The Email Editor tool displays.

<Image align="center" alt={1424} border={true} caption="Email Editor" title="Email Editor Templates" src="https://files.readme.io/db93bcba07e17c25cad0eedcbdd8074382d45005fc89bd4178da2dabedbf6acc-Email_Editor.png" />

# Template Types

You can choose from the following template options:

* **Basic Templates**: You can choose from pre-built or empty templates available from this tab.
* **AMP Templates**: You can choose from pre-built Templates, Email with custom HTML & AMP, and  
  Email with drag and drop from this tab.

You can also save customized templates and view them under **Saved Templates**.

# Basic Templates

Basic Templates provide a library of pre-built email templates that help you quickly create campaigns for common use cases without starting from scratch.

**Template Types**

Basic Templates include the following template types:

* **Email with rich media**: Rich Media templates include [out-of-the-box templates](doc:ootb-email-templates) for use cases, such as product announcements, feature highlights, or promotional campaigns, and also allow you to [build templates from scratch](doc:email-templates#rich-media-template). These templates are designed for advanced template customization using HTML and are optimized for visually rich emails, featuring layouts that accommodate images, text, and call-to-action elements. You can customize the layout and content to suit your campaign requirements. You can also add personalization by using the **@** and **\{\{}}** icons. For more information about personalization, refer to [Personalize Message](doc:personalize-message-email).
* **Email with drag-and-drop**: These include out-of-the-box drag-and-drop templates for use cases such as Welcome emails, promotional, or offer-based emails. Drag-and-drop templates are ideal for no-code email creation. You can start with an existing template or [create one from scratch](doc:email-templates#drag-and-drop-template), and visually customize it by adding, removing, or rearranging elements such as text, images, buttons, and dividers.

You can filter Basic Templates to narrow down and view templates based on the following: _Industry_ (for example, Food Delivery), _Goal_ (for example, Referral), or _Type_ (for example, HTML). This makes it easier to browse the template library and quickly find the most relevant template for your campaign.

<Image align="center" border={true} caption="Filter Basic Templates" src="https://files.readme.io/ea332ac1a3e33ffe2ce1b84ee1616f4740953b618037d7e16b03c65c471a24ce-Filter_Basic_Templates.gif" />

## Rich Media Template

Create rich messages using rich text and images. There are two ways in which you can create a message.

### Using Built-in Editor

To create a message using a built-in editor:

1. Select _Email with rich media_.
2. Create a template using the Built-in Editor:  
   i. Add the text.  
   ii. Click the icon to insert images.  
   iii. Click the icon to insert links.

<Image align="center" alt={1410} border={true} src="https://files.readme.io/2a757b2-Rich_Media_Template.png" title="Create a Template using Build-in Editor" className="border" />

### Using Source Mode

To create a message using a source mode:

1. Select _Email with rich media_.
2. Click **Source** mode and add your HTML content.

<Callout icon="🚧" theme="warn">
  #### Grammarly Extension

  If the Grammarly extension is enabled on your device when creating the Email campaign using Rich Media Editor, it may add unwanted _\<p>_ tags to the code in Source mode. To maintain clean code, we recommend disabling Grammarly and refreshing the page before adding content. If content has already been added, disable Grammarly, refresh, and re-add the content.

  <Image align="center" alt="View Source Mode" border={true} src="https://files.readme.io/22f1e95-image_8.png" className="border" />
</Callout>

<Image align="center" alt={1413} border={true} src="https://files.readme.io/bf4ca46-Source.png" title="Add HTML Content using Source View" className="border" />

3. Click the **@** and **\{\{}}** icon to add personalization. For more information on personalization, refer to  [Personalize Message](doc:personalize-message-email).
4. (Optional) Enter the template _Name_ and save your customized template for future use under Saved Templates.

<Image align="center" alt={1408} border={true} src="https://files.readme.io/d45ee9dafe0689e81fe2e3468597aa4632fae70ed298a508c494fe5040a16285-Saved_Templates.png" title="View Saved Templates" className="border" />

## Drag and Drop Template

Learn how to use an _Email with drag and drop_ template. There are many edits you can make to this template. In this step, we will look at three of them: how to change an image, add a new block, and delete an element.

### Change an Image

1. Click inside the box of the image you want to change.

<Image align="center" alt={1053} border={true} src="https://files.readme.io/f0237ec-Email_Campaign_Templates_select.png" title="Create Content in Email Campaign's Body" className="border" />

2. Click the image.

<Image align="center" alt={1225} border={true} src="https://files.readme.io/44d57b7-Email_Campaign_Templates_change_image1.png" title="Change and Existing Image Content" className="border" />

3. Click the **Change Image** button. The _File manager_ displays.
4. Select an image from the gallery or upload a custom image.

<Image align="center" alt={1225} border={true} src="https://files.readme.io/3cd76ca-Email_Campaign_Templates_change_image_select.png" title="Upload an Image from the Gallery" className="border" />

5. Click Insert. Your new image will appear in the selected box.

<Image align="center" alt={1305} border={true} src="https://files.readme.io/e1e933f-Email_Campaign_Templates_image_inserted.png" title="Insert the Uploaded Image" className="border" />

### Add a New Text Block

1. Under the Content tab, find Text.

<Image align="center" alt={1324} border={true} src="https://files.readme.io/ceae7fa-Email_Campaign_add_new_text.gif" title="Add a Text Box to Email Content" className="border" />

2. Drag the Text icon to the desired location.

Now you have a new text block.

Similarly, you can also drag other elements, such as Images, Buttons, or Videos, into your template. You can also add personalization by using the **@** and **\{\{}}** icons. For more information about personalization, refer to  [Personalize Message](doc:personalize-message-email).

### Delete an Element

1. Click the box of the element you want to delete.

<Image align="center" alt={1324} border={true} src="https://files.readme.io/7610436-Email_Editor_delete_element.gif" title="Delete an Element from Email Content" className="border" />

2. Click the trashcan icon.

3. Click **Delete**.

The element you deleted will no longer appear.

## Rows

You can drag and drop, delete, rename, or re-organize your saved rows, right inside the editor.

1. Select the _Email with a drag and drop_ template.
2. Click the ROWS tab.
3. Select the **Empty**, **Default**, or **Saved Rows** from the list. You can also update the **Display Condition** for the rows.
4. Drag and drop the row to the editor.

### Save Rows

To save a row:

1. Double-click the row.
2. Click the ![](https://files.readme.io/54b1fcd-Email_save_icon.png) icon to save the row for future use.

<Image align="center" alt={1164} border={true} src="https://files.readme.io/67215bf-email_editor_rows_edit_clone_delete.gif" title="Save, Delete and Duplicate the Rows" className="border" />

### Delete Rows

1. You can delete saved rows from the editor.
2. Click the ROWS tab in the editor.
3. Select the saved row and click the ellipsis.
4. Click **Delete**.

<Image align="center" alt={1306} border={true} src="https://files.readme.io/eeae8e5-email_editor_rows_delete.png" title="Delete a Saved Row" className="border" />

## Display Condition

Display conditions determine when and under what circumstances certain content is rendered to the recipients.

1. Click the row to which you want to add the display condition.
2. Click **Add Condition** under the **DYNAMIC CONTENT** section. The **Add display conditions** pop-up window appears. The following columns appear.

| Column Name                                   | Description                                                                                                                                                                            |
| :-------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name                                          | Add your condition name.                                                                                                                                                               |
| Description                                   | Add your description for the condition.                                                                                                                                                |
| Add display condition before the selected row | Add a criteria that is checked before the selected row from the email is rendered. This feature ensures that specific rows are displayed only to recipients who meet certain criteria. |
| Add display condition after the selected row  | Add a criteria that is checked after the selected row from the email is rendered. This feature controls the visibility of the content that follows the selected row.                   |

<Image align="center" alt="Email Editor Display Condition" border={true} src="https://files.readme.io/bb8dfbc-Email_Editor_-_Liquid_Tags.gif" className="border" />

3. Click **Add** to add the display condition and its details. Click **Cancel** to discard the changes.

## Mobile View

You can switch between the mobile and desktop views of your message to view and edit content. You can check how the content will display on a mobile phone without going to Previews or sending a test message. Any changes made to the mobile view will be reflected on the desktop view as well. It is a What You See is What You Get (WYSIWYG) editor.

<Image align="center" alt={1096} border={true} src="https://files.readme.io/bb4fe41-email_editor_mobile_view.gif" title="View Email Content in Mobile" className="border" />

# Saved Templates

The _Saved Templates_ tab in the email editor enables you to quickly reuse or access the existing templates and maintain consistency in branding across campaigns. Within this tab, you can preview the template before using it. The Saved templates are managed from the _Content Manager_ > _Templates_ > _Email_ page. Updates made in Content Manager are reflected in this tab.

<Image align="center" alt="Template Listing" border={true} src="https://files.readme.io/2173ec56565d05ad28197988acbed63640da62b81931948675145d7386c6482b-Template_Listing.png" className="border" />

# Template Operations

You can perform basic template operations directly from the _Saved Templates_ tab in the email editor during campaign creation. These include:

* **Select View**: Switch between <img src="https://files.readme.io/ac80074-list_view_icon.jpg" height="30px" width="30px" /> list and card <img src="https://files.readme.io/40d9260-tile_view_icon.jpg" height="30px" width="30px" /> view for templates.

  <Image align="center" alt="Select View" border={true} src="https://files.readme.io/6920d54391f6a75a315233af587b849aa4dc7db3b556735ded607e6509f9c43d-Select_View.gif" className="border" />
* **Filter Templates**: Filter templates based on the following criteria: Time Period, Created By, Labels, Editor Type, and Amp Type.

  <Image align="center" alt="Filter Templates" border={true} src="https://files.readme.io/a77d3d62a1afa3bd6a68f8bb0723e3a008a4c400d5d0eec4563d447850f238d3-Filter_Templates.gif" className="border" />
* **Sort Templates**: Sort by template name, created date, and last modified date.

  <Image align="center" alt="Sort Templates" border={true} src="https://files.readme.io/513563298d4655ecfff9d8bae8ae45aecb7c04e9f5efb5736cd7c6e8454703fb-Sort_Templates.gif" className="border" />
* **Delete Templates**: Deleted templates are permanently removed and cannot be recovered. Select multiple files and click the <img src="https://files.readme.io/70a339a-delete_all_icon.jpg" height="30px" width="30px" /> delete icon. Alternatively, enable _Selection Mode_ to delete templates in bulk.

  <Image align="center" alt="Delete Template" border={true} src="https://files.readme.io/f479b42f813d39f3cfd7d885ede9d816ee5d822a5c22d2fc5fc427290d4df8e1-Delete_A_Template.png" className="border" />
* Search Templates: Search a template by its name.

You can perform the following template operations by navigating to the _Content Manager_ > _Templates_ > _Email_ page: Edit, Clone, Rename, and Add labels. For more information, refer to [Content Manager Templates](doc:content-manager-templates).

# Device Preview

## Dark Mode

You can preview how your email displays in dark mode on both desktops and mobile phones.

<Callout icon="📘" theme="info">
  #### Note

  Dark Mode is only available in the _Email with drag and drop_ editor.
</Callout>

Follow the steps to preview your template in Dark Mode:

1. Select the _Email with drag and drop_ editor.

<Image align="center" alt={2866} border={true} caption="Select Drag-and-Drop Editor" title="Select the Email with Drag and Drop" src="https://files.readme.io/5d708b8aaad79c2e2ec52b6cb1ea65c5084b486166e8b8b7fa74a0697029454d-Email_Editor.png" />

2. Draft your message.

<Image align="center" alt={2880} border={true} caption="Draft Email Campaign" title="Create the Email Content" src="https://files.readme.io/2e30dbe-Create_message.png" />

3. Click the **Preview and Test** button. The _Preview and test_ window displays. You can preview how the email will look in dark mode by turning the _Dark Mode_ toggle ON.

<Image align="center" alt={1440} border={true} caption="Toggle ON Dark Mode" title="Preview Content in Dark Mode" src="https://files.readme.io/c6ed33f-Dark_Mode_Preview.gif" />

<Callout icon="📘" theme="info">
  #### Dark Mode Preview

  Dark Mode support varies across email clients and devices. Test the mails on an email client with dark mode enabled for best results. The Dark Mode preview generates a generic dark mode color scheme when enabled.

  Refer to the links below for dark mode email design tips:

  * [5 Tips for Dark Mode Email Design](https://emaildesign.beefree.io/5-tips-for-dark-mode-email-design/)
  * [The Ultimate Guide to Dark Mode for Email Marketers](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers/)
</Callout>

## Inbox Previews with Code Analysis

Inbox Previews with Code Analysis offers you an analysis of your HTML code. It also provides you previews across devices and inboxes before you send out a campaign. The Email Add-On offers you 100 inbox previews a month.

Before we begin, check that you have enabled Inbox Previews. For enabling the Inbox Previews, see [Enable Email Previews](doc:enabling-previews). Follow the steps to create an email campaign.

1. Select the template.
2. Create your message.
3. Click the **Preview and Test** button.  The _Previews and test_ window displays.
4. Click the **Inbox Previews** tab.
5. Click the **Generate Report** button. The display may take some time if you have selected multiple inboxes. We will render the results and send you a notification email to know when the preview is ready.

<Image align="center" alt={1648} border={true} caption="Spam Report" title="Generate Report of a Campaign" src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />

6. Click **Inbox Previews** tab to view the preview report. The tests will display email previews across all the selected inboxes. It displays the errors, if any, for each inbox. For selecting inboxes, see [Enabling Previews](doc:enabling-previews).

<Image align="center" alt={1646} border={true} caption="Inbox Preview" title="View the Preview Report" src="https://files.readme.io/439b55a-Screenshot_2021-07-12_at_7.08.00_PM.png" />

7. The _Code Analysis_ tab displays the error type and details. You can sort these errors by severity or property.

<Image align="center" alt={1644} border={true} src="https://files.readme.io/d94922b-Screenshot_2021-07-12_at_7.08.29_PM.png" title="View the Code Analysis" className="border" />

<Callout icon="📘" theme="info">
  #### Templates for Inbox Preview

  Code Analysis with Inbox Preview is available for the [Custom HTML template](doc:email-templates#custom-html-template) and [Rich Media Template](doc:email-templates#rich-media-template).
</Callout>

8. Click the _Fix issues_ in the editor link to fix the issues. You are redirected to the email editor.  
   Rerun the preview tests to check that the previews are in order.

## Spam Report

A spam report allows you to test your email for deliverability by creating a spam report. The Email Add-On offers you 100 spam reports a month.

Follow the steps to create an email campaign.

1. Select the template.
2. Create your message.
3. Click the **Preview and Test** button. The _Previews and test_ window displays.
4. Click the **Spam Report** tab.
5. Click the **Generate Report** button.

<Image align="center" alt={1648} border={true} caption="Generate Spam Report" title="Generate Spam Report" src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />
