---
title: Content Manager Templates
excerpt: >-
  Learn how to use templates in CleverTap Content Manager for a consistent
  branding and messaging experience.
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

The _Templates_ section helps you organize and standardize your messaging templates. You can save and reuse templates from the _Templates_ section to have consistent messaging. 

> 📘 Custom Roles
> 
> All users with custom roles have read access to Templates by default. However, the administrator must  grant **write** access for any Template operations. For more information, refer to [Define Access for Custom Roles](doc:role-based-access-control#define-access-for-custom-roles).

Go to _Content Manager_ > _Templates > \_Email_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1cf70b0105d31dd336bf2be0630bc94b56ad3427443a98026ac07c0af312b1d3-image.png",
        null,
        "Content Manager Templates Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Templates Editor"
    }
  ]
}
[/block]


The _Templates Editor_ offers the following multiple options:

- _Select Views_: Switch between <img src= "https://files.readme.io/ac80074-list_view_icon.jpg" height="30px" width="30px"> list and card <img src= "https://files.readme.io/40d9260-tile_view_icon.jpg" height="30px" width="30px" > view for templates.
- _Search Templates_: Search a template by its name.
- _Sort Template_: Sort by template name, created date, and last modified date.
- _Bulk Delete_: Select multiple files and click the <img src= "https://files.readme.io/70a339a-delete_all_icon.jpg" height="30px" width="30px"> delete icon.

> 📘 Template Deletion
> 
> A template deleted from the template gallery does not affect the running campaign already using these templates.

# Create Templates

You can create a template that can be used across various campaigns.

> 📘 Supported Channels
> 
> Currently, only Email templates are supported. We will soon start supporting more channels for template management in the Content Manager.

1. Go to _Content Manager_ > _Templates_ > Email.
2. Click _Create Template_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc68aa6-Create_Templates.jpg",
        "",
        "Create Templates"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Templates"
    }
  ]
}
[/block]


3. After completing the steps to [create a template](https://docs.clevertap.com/docs/email-editor-templates#template-types), click **Save**. The _Save Template_ popup opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2da38d5136a7f4c8c13466c0d82395928892f0aaf59cef9b9e648493380a4f99-image.png",
        null,
        "save a template"
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Save a template"
    }
  ]
}
[/block]


4. Enter a name and select a label for the template. 

> 📘 Template names
> 
> Template names can include letters, numbers (0-9), underscores (\_), periods (.), hyphens (-), and spaces. Names must begin with a letter. Additionally, the template name must be unique.

5. Click **Save** to save your template.

You can add content to pre-built templates or customize and build your own. To create a new template with drag-and-drop elements, refer to [drag-and-drop templates](doc:email-editor-templates#drag-and-drop-template). You can also create a template from the HTML editor with a [Rich Media template](doc:email-editor-templates#rich-media-template). 

# Upload HTML Templates Using ZIP File

The Upload HTML Templates feature enables marketers to easily import email designs packaged as ZIP files directly into CleverTap. These ZIP files typically contain a single HTML file and associated image assets, enabling efficient template creation without manual image uploads. You can also upload templates from the _What_ section of the campaign setup. With this feature, you can:

- Faster template creation by uploading a pre-packaged HTML + assets ZIP file
- Automated asset management with image upload to CMS
- Reduces manual errors in HTML and image linkage

To upload an email HTML template using .zip files, perform the following steps:

1. Click **Create Template** from the Templates page. The Email editor opens.
2. Click **Upload File** or drag and drop to upload the required `.zip` file. You can download the sample zip file by clicking the _[Download sample file](https://d31lbcrrrnac8j.cloudfront.net/Sample-files/Sample-template.zip)_ link. The ZIP file must meet the following criteria:

   <br />

   | Requirement             | Details                                                                                                                                                                                             |
   | :---------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | File type               | Must be `.zip`                                                                                                                                                                                      |
   | HTML file               | Only one `.html` file allowed. It should be present inside the main folder and not in any subfolder. CSS must be inline and embedded within the .html file; separate stylesheets are not supported. |
   | Images                  | All image assets must be placed in a folder named **images**. Ensure all image references within the HTML file point to this folder correctly.                                                      |
   | Supported image formats | JPG, PNG, GIF                                                                                                                                                                                       |
   | File size               | Must be less than 5 MB                                                                                                                                                                              |

   [block:image]{"images":[{"image":["https://files.readme.io/1128408289c737b5629f81dd9f108e68c78b07a529083595073bf5d89cabe52a-Upload_HTML_Template.gif","","Upload HTML Template"],"align":"center","border":true,"caption":"Upload HTML Template"}]}[/block]

   <br />
3. CleverTap parses the ZIP file:

   - Images are uploaded to the **CMS File Manager**.
   - The template is saved under **Saved Templates** in the What section of campaign setup, as well as in the **Templates** section of Content Manager.

> 📘 Personalization for Uploaded Templates
> 
> If you upload an HTML file with characters like {{}} or @, CleverTap treats them as plain text. To use personalization, you can manually add them during email campaign setup after template upload. For detailed steps, refer to [Personalize Message](doc:personalize-message-upload-html-zip#:~:text=previous%20campaign%20interaction.-,When%20you,-upload%20an%20HTML).

## Upload Validations

Upload may fail due to the following validations performed by CleverTap:

| Errors                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                         |
| :----------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ZIP file exceeds maximum size of 5 MB.                                                                                               | The uploaded `.zip` file exceeds the maximum allowed size of 5 MB. Reduce the file size by optimizing images or HTML content and try again.                                                                                                                                                                                         |
| File type is unsupported. Upload ZIP file only.                                                                                      | Only `.zip` files are supported. Uploads using other file types are rejected.                                                                                                                                                                                                                                                       |
| ZIP file is corrupt. Check file contents and try uploading again.                                                                    | The file could not be unzipped or read. This may occur due to improper compression or file corruption. Create a `.zip` file again and upload it.                                                                                                                                                                                    |
| ZIP file name must start with a letter. Only letters, numbers, spaces, and following special characters are allowed: . - \_          | Ensure the ZIP file name starts with a letter. Only letters, numbers, spaces, and these special characters are allowed: `.`, `-`, `_`. Rename the file and upload again.                                                                                                                                                            |
| HTML file is missing from ZIP file. Add HTML file and upload again.                                                                  | The `.zip` does not contain a valid .html file. An HTML file is mandatory to define the email content and must be placed at the root level.                                                                                                                                                                                         |
| ZIP file must contain only one HTML file. Remove additional HTML files and upload again.                                             | More than one `.html` file was found. CleverTap supports only a single HTML file per upload. Remove additional files and retry.                                                                                                                                                                                                     |
| HTML file is invalid. Check file and try uploading again.                                                                            | The uploaded `.html` file is malformed or unreadable. Verify its structure and formatting before uploading again.                                                                                                                                                                                                                   |
| Some images referenced in HTML file are missing from image folder. Add all images to a separate folder in ZIP file and upload again. | One or more image URLs in the HTML are unavailable in the provided **images** folder. Ensure that all image assets are correctly referenced and try again.                                                                                                                                                                          |
| File not referenced in HTML. It won’t be saved in Content Manager.                                                                   | Images not referenced in the HTML file but present in the images folder are ignored during processing. They do not impact the upload and are not uploaded to the _Files_ section of Content Manager, but may unnecessarily increase the size of the ZIP archive. It is recommended that any unused assets be removed before upload. |
| Maximum 50 images allowed. Remove additional images and upload again.                                                                | The ZIP archive contains more than 50 image files. Remove the excess images and try uploading again. Each template supports up to 50 images.                                                                                                                                                                                        |

# Template Operations

You can click the ellipsis from the content card for additional actions to manage templates. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a6898b-CMS_Templates_Options.jpg",
        "",
        "Template Options"
      ],
      "align": "center",
      "border": true,
      "caption": "Template Options"
    }
  ]
}
[/block]


You can select from the following options:

- _Edit_: Select to make further changes to the template. 
- _Clone_: Select to create a copy of the template. You can then add further edits to the template.
- _Rename_:  Select to change the name of the template. 
- _Add label_: Select to add a label. Labeling templates helps organize and search them easily. 
- _Delete_: Select to delete the template. 

> 📘 Template Deletion
> 
> A template deleted from the template gallery will not affect a running campaign.

### Filter Templates

You can filter the templates to narrow down your search.

1. Navigate to _Content > Content Manager > Messaging Channel > Te\`ates_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4e68db-Filter_Templates.jpg",
        "",
        "Filter Templates in Content Manager"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Templates"
    }
  ]
}
[/block]


2. Click _Filters_. You can filter templates based on the following criteria:

- _Time Period_: Filter and search by the template's creation period.
- _Type_: Filter and search by the template type.
- _Labels_: Filter and search the template by the assigned label. 
- _Created by_: Filter and search by the person who created the template.