---
title: CSV Upload
excerpt: Understand how to import data to CleverTap dashboard using CSV upload feature.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
With the CSV upload feature, you can create new [user profiles](doc:user-profiles) in CleverTap in bulk by uploading a CSV file with a list of user profiles. You can also use this feature to add or update information for existing user profiles.

> 📘 CSV Upload Permissions
> 
> Anyone with the [required permissions](doc:role-based-access-control) to upload the CSV file can use this feature.

# CSV Upload Video Tutorial

The following is a video tutorial that highlights the recent CSV Upload enhancements:

[block:html]
{
  "html": "<div\n              style=\"\n                position: relative;\n                padding-bottom: 56.25%;\n                height: 0;\n                border-radius: 0;\n                box-shadow: 0 15px 40px rgba(63,58,79,.3);\n                overflow: hidden;\n                min-width:320px\"><iframe\n              src=\"https://clevertap.portal.trainn.co/share/lBa8u96eJfdEQ4k0qyr53w/embed?autoplay=false\"\n              frameborder=\"0\"\n              webkitallowfullscreen\n              mozallowfullscreen\n              allowfullscreen\n              allow=\"autoplay; fullscreen\"\n              style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe></div>"
}
[/block]


# Upload User Profiles using a CSV File

To upload user profiles to the CleverTap dashboard using a CSV file: 

1. [Upload user profiles](doc:csv-upload#upload-user-profiles).
2. [Map uploaded user profiles](doc:csv-upload#map-uploaded-user-profiles).

## Upload User Profiles

To upload user profiles:

1. Log in to your CleverTap account and click _Settings_ > _Engage_ > _CSV Uploads_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e03356-CSVUpload.jpg",
        null,
        "CSV Uploads Page"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "CSV Uploads Page"
    }
  ]
}
[/block]


2. Click **+ Upload**. The **Upload** page appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a074165-image.png",
        null,
        "Upload User Profiles"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Upload User Profiles"
    }
  ]
}
[/block]


3. Under **Upload user profiles**, drag and drop or browse the CSV file. For more information on the CSV file format, refer to [CSV File Format](doc:csv-upload#csv-file-format).  
   A preview of the uploaded user profiles appears on the right side.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8851b05-image.png",
        null,
        "CSV Uploads Page"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "View a Preview of the Uploaded User Profiles"
    }
  ]
}
[/block]


4. Enter a unique file name on the main screen for easy identification and click **Save & Upload**.  
   The _Data Export uploaded_ message appears.
5. (Optional) Click the **Preview** icon to view the uploaded user profiles.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/969865d-image.png",
        null,
        "Preview of the Uploaded User Profiles"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Preview of the Uploaded User Profiles"
    }
  ]
}
[/block]


Once you upload the CSV file, it is essential to map the uploaded user profiles with the appropriate data types and user properties.

## Map Uploaded User Profiles

 You must map the CSV column names with the corresponding date types and user properties in the CleverTap system.  

By default, CleverTap tries to map your file data. However, you can map your file data to the respective data type and user property.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6da3a93-image.png",
        null,
        "Map User Profiles"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Map User Profiles"
    }
  ]
}
[/block]


Click **Map** under the Upload user profiles page. It provides you with the following two methods to map the user profile with data type and user property: 

- [Manually Map the File](doc:csv-upload#manually-map-the-file) 
- [Upload the Mapped File](doc:csv-upload#upload-the-mapped-file) 

### Manually Map the File

To manually map the file: 

1. Select **Manually map file**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebdbdc9-image.png",
        null,
        "Manually Map User Profiles"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Manually Map User Profiles"
    }
  ]
}
[/block]


2. From the table below, select the appropriate data type and user properties for each column in the file:
   - **Data Types**: Select a data type from the dropdown list for the user profile values. For instance, _id_name_ has the value _John Doe_ and is of the _Alphanumeric_ data type.
     - **Alphanumeric**: A string value consisting of letters and numerals for data such as Phone Number,  customer_type, etc.
     - **Number**: An integer value for data such as an Amount, Wallet Balance, etc. 
     - **True or False**: A boolean value. For example, True indicates if an email ID exists for users.
     - **Date Formats**: A date value for data such as the Date of Birth of the user. For more information about date formats supported by CleverTap, refer to the [Date Format](doc:csv-upload#date-format) section. 
       > 📘 Guidelines for Mapping Data Types
       > 
       > - The data type for _identity_ and _objectID_ is always alphanumeric and cannot be changed.
       > - If the date format is _$D_1695801332_, then the data type must be alphanumeric.
   - **User Property**: Select the corresponding CleverTap user property from the drop-down list. For example, _id_email_ corresponds to _Email_ in CleverTap.
     > 📘 Guidelines for Mapping User Properties
     > 
     > While mapping, if you do not find the relevant user property under the dropdown, select the **Same as column name **option. CleverTap will create a new user property for that specific column data.

### Upload the Mapped File

To upload a pre-mapped JSON manifest file:

1. Select **Upload mapped file**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8d03f8-image.png",
        null,
        "Upload Pre-Mapped User Profiles"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Upload Pre-Mapped User Profiles"
    }
  ]
}
[/block]


2. Drag and drop or browse the pre-mapped JSON manifest file.  
   The following is a sample JSON manifest file:

```json
{
    "columns": {
        "identity": {
            "ctName": "identity",
            "dataType": "STRING"
        },
        "id_name": {
            "ctName": "Name",
            "dataType": "STRING"
        },
        "id_email": {
            "ctName": "Email",
            "dataType": "STRING"
        },
        "id_phone": {
            "ctName": "Phone",
            "dataType": "STRING"
        },
        "id_gender": {
            "ctName": "Gender",
            "dataType": "STRING"
        },
        "Employment Status": {
            "ctName": "employment_status",
            "dataType": "BOOLEAN"
        },
        "Education status": {
            "ctName": "education_status",
            "dataType": "STRING"
        },
        "Wallet Balance": {
            "ctName": "wallet_balance",
            "dataType": "INTEGER"
        },
        "DOB": {
            "ctName": "DOB",
            "dataType": "Date",
            "dateFormat": "UNIX"
        },
        "MSG-sms": {
            "ctName": "MSG-sms",
            "dataType": "BOOLEAN"
        },
        "Payment Date": {
            "ctName": "purchase_date",
            "dataType": "Date",
            "dateFormat": "dd/MM/yyyy HH:mm:ss"
        }
    }
}
```

3. Click **Preview** to view the mapped file. 
4. Click **Proces File**. 

> 📘 Guidelines for Uploading Mapped File
> 
> JSON is a valid format.

If you have not mapped the files, the status appears as _Start mapping_. Mapping is necessary to process the CSV upload. After the CSV file is processed, the status for that upload changes to _Completed_.  For more information about the statuses, refer to the [CSV Upload Details](doc:csv-upload#csv-upload-details) section. 

Once the file has been successfully processed, you will receive an email notification with the processed data file and a detailed error report if any problems occur.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2821017-image.png",
        null,
        "View the Status of the Newly Uploaded File"
      ],
      "align": "center",
      "border": true,
      "caption": "View the Status of the Newly-Uploaded File"
    }
  ]
}
[/block]


# Filter the Uploaded User Profiles

To filter the uploaded user profiles: 

1. Log in to your CleverTap account and click _Settings_ > _Engage_ > _CSV Uploads_.
2. Click the <img src="https://files.readme.io/a5b07fd-image.png" height="30px" width="30px" > icon.  
   The **Filter Profile Uploads** pane appears. 
3. Select the required options from the **Status** drop-down list: **Select All**, **Processing**, **Completed**, **Rejected**, or **Start mapping**. 
4. Click **Apply**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af9c277-StatusCSVUpload.gif",
        null,
        "Filter Uploaded User Profiles by Status"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Filter Uploaded User Profiles by Status"
    }
  ]
}
[/block]


5. You can also filter the uploads using the date range option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e4f9c51-2023-09-30_20-09-51_1.gif",
        null,
        "\n\n5."
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Filter Uploaded User Profiles by Date Range"
    }
  ]
}
[/block]


# Key Points to Remember

## CSV Upload Details

- If a new user profile is uploaded, a new user profile is created on the account.
- If an existing user profile is uploaded, the old user profile is updated with new values.
- If a new user profile property is added, a property is created on the user profile.
- You can upload multiple CSV files simultaneously, even when existing files are currently being processed.
- The phone number must be in the format [+][country code][phone number] and is treated as an Alphanumeric. For example, +919869311111, where +91 is the country code for the India.
- After the upload is complete, the following information for the upload is displayed: 
  - **Name**: Displays the CSV import name.
  - **Uploaded on**: Displays the date when the CSV file is uploaded. 
  - **Uploaded by**: Displays the email ID of the person who uploaded the file.
  - **Status**: Displays the status of CSV File upload. The following are the possible upload statuses: 
    - **Completed**: Indicates that the CSV file has been successfully uploaded.
    - **Processing**: Indicates that the CSV file is being processed. 
    - **Rejected**: Indicates that the CSV file was rejected due to multiple errors. Check your email to identify the error for rejection.
    - **Start mapping**: Indicates that the mapping has not been done. 
  - **Errors**: Displays the count of rows that were not uploaded due to an error.
  - **Processed**: Displays the count of records that were uploaded successfully. 

## CSV File Format

- The following is an example of a CSV file format:

  | identity                                    | id_name  | id_email                                    | id_phone       | id_gender | Employment Status | Education status | Wallet Balance | DOB        | MSG-sms | Payment Date      |
  | :------------------------------------------ | :------- | :------------------------------------------ | :------------- | :-------- | :---------------- | :--------------- | :------------- | :--------- | :------ | :---------------- |
  | 123456789                                   | John Doe |                                             | \+919900000000 | M         | TRUE              | Graduate         | 1              | 1487576752 | FALSE   | 09/10/23 10:15:02 |
  | 14155551235                                 | Jane     |                                             | \+919889000000 | M         | FALSE             | Graduate         | 12             | 1487576752 | FALSE   | 15/03/23 9:15:00  |
  | 14155551234                                 | Lincoln  |                                             | \+919778000000 | M         | 0                 | Graduate         | 34             | 1487576752 | FALSE   | 09/01/22 13:08:00 |
  | \_234853412                                 | Mary     | [mary@johndoe.com](mailto:mary@johndoe.com) | \+919667000000 | M         | 1                 | Graduate         | 255            | 1487576752 | FALSE   | 09/10/23 10:15:00 |
  | [bob@johndoe.com](mailto:bob@johndoe.com)   | Bob      | [bob@johndoe.com](mailto:bob@johndoe.com)   | \+919444000000 | M         | 0                 | Graduate         | 45             | 1487576752 | FALSE   | 08/01/21 10:15:00 |
  | [adam@johndoe.com](mailto:adam@johndoe.com) | Adam     | [adam@johndoe.com](mailto:adam@johndoe.com) | \+919556000000 | M         | 0                 | Graduate         | 24             | 1487576752 | FALSE   | 09/06/20 10:15:00 |
- The upload will not be allowed if the file is not a CSV file or does not comply with CSV standards.
- [identity](doc:user-profiles) is a mandatory column in the CSV file. However, if you want to make profile updates using the CleverTap ID, you can use the `objectId` in place of identity.

> 🚧 Note
> 
> - Ensure that the `identity` key is always in lower case.
> - You can upload CSV files up to **1 GB** in size.

The following is the sample format for the CSV file using the `objectId`:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c4102355774db6b01001fdc3188266cc0cc5a8d38d619b8bbeb171641c7f9b7-Sample_CSV_File.png",
        null,
        "Sample CSV File using `objectId`"
      ],
      "align": "center",
      "border": true,
      "caption": "Sample CSV File using `objectId`"
    }
  ]
}
[/block]


## Date Format

- CleverTap supports uploading date information in the following formats: 
  - dd/MM/yyyy HH:mm:ss
  - MM/dd/yyyy HH:mm:ss
  - yyyy/dd/MM HH:mm:ss
  - yyyy/MM/dd HH:mm:ss
  - dd MMM yyyy HH:mm:ss
  - dd/MM/yyyy 
  - MM/dd/yyyy 
  - yyyy/dd/MM 
  - yyyy/MM/dd 
  - dd MMM yyyy 
  - Unix (EPOCH): A timestamp or a count of seconds. For example, 1695799434. It measures time by the number of seconds that have elapsed since 00:00:00 UTC on 1 January 1970. All other formats will be treated as a String.

- Time defaults to 12:00:00 if hh:mm:ss is not added.

- 24-hour date format is supported.

> 📘 Note
> 
> We currently support uploading timestamps in 24-hour format and do not support AM/PM in timestamp. If the format is HH:mm:ss, use the 24-hour format (for example, 18:25:32). Do not use the 12-hour format (for example, 06:25:32 PM).

<br />

## Operations for Profile Properties

You can use the following operations on user profile properties:

- $add: You can add specific values for the [multi-value profile properties](https://developer.clevertap.com/docs/concepts-user-profiles#manually-updating-multi-value-user-profile-properties). For example, you can add a particular item from the list of items that belong to a particular user profile.

  [block:image]{"images":[{"image":["https://files.readme.io/e68c6fcc13bd5335aa899adf55472e0e5c087145db5d277d8db00b9f57c74d2f-Add_Value_for_User_Property.png","","Add a Value for User Property of Type Array"],"align":"center","sizing":"60% ","border":true,"caption":"Add a Value for User Property"}]}[/block]
- $remove: You can remove specific values from the multi-value user property. For example, you can remove a particular item from the list of items that belong to a particular user. 

  [block:image]{"images":[{"image":["https://files.readme.io/b9c9495b17dc8946d89ebab9a49aedc4942607b902e266e5d1dab9fbbe4ca8d2-Remove_Value_for_User_Property.png","","Remove Value for User Property"],"align":"center","sizing":"59% ","border":true,"caption":"Remove Value for User Property"}]}[/block]
- $set - You can replace the current value with a new value. For example, you can replace the current value of a particular single-value or multi-value user property.

  [block:image]{"images":[{"image":["https://files.readme.io/badb6f5287918a263b04d586844884ca23146f6dae4b0a2bd3608b7701f05db1-Set_Value_for_User_Property.png","","Set Value for User Property"],"align":"center","sizing":"60% ","border":true,"caption":"Set Value for User Property"}]}[/block]
- $delete - You can remove the property entirely. For example, you can completely remove the property `MyStuff` for user profile with identity `1904` and all the values in it.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1fa7a8d56aea992973b068192d92eea65fe4db9bc6f15ba574a668399bfedaab-Delete_a_User_Property.png",
        "",
        "Delete a User Property"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Delete a User Property"
    }
  ]
}
[/block]


# FAQ

### Q:   What Happens if an Invalid Identity Value Is Set?

A: If you input an incorrect or invalid identity, it results in the below error, and the system flags the records in the file as error.  

> ❗️ Error Message
> 
> Identity value cannot be undefined or set at least one of identity / fbId / gpId / objectId under 1024 chars to identify the user.

Make sure not to use the following values as the identity: 

- undefined
- null
- na
- n/a
- 0
- nil
- \-1
- infinity
- \-infinity
- inf
- \-inf
- nan
- \-nan
- empty
- xxxxxx
- none

### Q. How to upload user user data via CSV?

A. Uploading your historical user data via CSV is quick and simple; however, note the following key pointers before uploading your user data via CSV: 

- The identity field must be defined as _identity_ with a lowercase _i_ and not _Identity_.
- The _identity_ field is a mandatory column. 
- Check that your CSV complies with the CSV standards. Otherwise, the upload will be denied.
- You can download the sample CSV file for a quick check from the _Settings_ section under _CSV uploads_.

Below is a sample CSV:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61b074a-Identity_CSV_Uploads.png",
        "Identity_CSV_Uploads.png",
        1298
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


#