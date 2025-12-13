---
title: Create and Manage Voucher Lists
excerpt: >-
  Learn how to efficiently manage your voucher lists, track their status, and
  ensure seamless distribution.
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

View and manage all your voucher lists in one place. The *Voucher Lists* page provides key details about each list, helping you track their status, usage, and associated campaigns. 

# Access Voucher List

To access the *Voucher Lists* page, perform these steps:

1. Go to *Promotions* from the CleverTap dashboard.
2. Click **Rewards** and select *Partner Vouchers* from the dropdown menu.

<Image alt="Voucher Lists" align="center" border={true} src="https://files.readme.io/b55c1ccbffd44f05f9ab7a67f24171c5aa6097fff121e15eba98d013160fed01-Voucher_Lists_Page.png">
  Voucher Lists
</Image>

The **Voucher Lists** page provides a comprehensive overview of all voucher lists with the following columns:

<Table>
  <thead>
    <tr>
      <th>
        **Column Name**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **List ID**
      </td>

      <td>
        A unique identifier for each voucher list. Click the ID to view detailed information about the list.
      </td>
    </tr>

    <tr>
      <td>
        **Partner**
      </td>

      <td>
        Displays the name of the voucher provider associated with the list.
      </td>
    </tr>

    <tr>
      <td>
        **List Tag**
      </td>

      <td>
        A unique identifier for the voucher list is used along with the Partner Name to generate a distinct List ID.
      </td>
    </tr>

    <tr>
      <td>
        **Updated On**
      </td>

      <td>
        The date and time of the most recent modification.
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        <p>Indicates the current state of the voucher list. The following are the statuses:</p><ul><li>Active</li><li>Expired</li><li>Paused</li><li>Archived</li></ul> For more information, refer to [Voucher List Status and Actions](doc:create-and-manage-voucher-lists#voucher-list-status-and-actions).
      </td>
    </tr>

    <tr>
      <td>
        **Linked Promo Campaigns**
      </td>

      <td>
        The number of campaigns using this voucher list.
      </td>
    </tr>

    <tr>
      <td>
        **Codes Uploaded**
      </td>

      <td>
        The total number of voucher codes uploaded.
      </td>
    </tr>

    <tr>
      <td>
        **Codes Distributed**
      </td>

      <td>
        The number of voucher codes issued to users.
      </td>
    </tr>
  </tbody>
</Table>

## Voucher List Status and Actions

 The status of a voucher list determines its availability and the actions you can take. Properly managing lists ensures seamless voucher distribution in promotional campaigns.

The table below outlines each voucher list status, its description, and the actions you can perform:  

| Status       | Description                                                                  | Available Actions                     |
| ------------ | ---------------------------------------------------------------------------- | ------------------------------------- |
| **Active**   | Voucher list is available for use in promotional campaigns.                  | Pause, Edit, Upload codes, Archive    |
| **Paused**   | Voucher list is temporarily inactive; campaigns cannot use codes.            | Activate, Edit, Upload codes, Archive |
| **Expired**  | Voucher list has passed its expiration date and cannot be used.              | Edit, Archive                         |
| **Archived** | The voucher list is permanently deactivated and retained for record-keeping. | No further actions allowed            |

## Voucher List Actions

To perform any action on the voucher list, click the ![](https://files.readme.io/bb833f57ad2428831fdc23f4a1bf488039206ddbf9bdd8083d13148e887e17cf-Ellipsis_Promo.png) icon next to the list. The available actions depend on the current status of the list.  

| Action           | Effect                                                                               |
| ---------------- | ------------------------------------------------------------------------------------ |
| **Pause**        | Temporarily deactivates an active voucher list, making it unavailable for campaigns. |
| **Upload codes** | Adds new voucher codes to the existing list, ensuring continued distribution.        |
| **Edit**         | Allows modifications to the list name, description, and expiry date.                 |
| **Activate**     | Reactivates a paused voucher list, making it available for use again.                |
| **Archive**      | Permanently disables a voucher list, preventing any further modifications or usage.  |

# Upload New Vouchers

Before uploading new voucher codes, you must create a voucher list in CleverTap. Once created, you can upload codes to distribute them through campaigns. To upload new voucher codes, follow these steps:

1. Go to *Promotions* from the CleverTap dashboard.
2. Click **Rewards** and select *Partner Vouchers* from the dropdown.
3. Click **New Voucher List** in the top-right corner.
4. Enter the following details:

| Field                | Description                                                                                                                                                                                                                                                                                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Partner**          | Enter the name of the voucher provider. For example, *Puma*. The partner name helps categorize and track voucher sources. If the Partner is not listed, click **Add Partner** to create a new entry. The system enforces case sensitivity and prevents duplicate partner names. For example, `clevertap` and `CLEVERTAP` are considered separate partners in Promo. |
| **List tag**         | Define a short, unique identifier for the codes. For example, *holi2025campaign*. The *List tag* uniquely identifies the uploaded voucher list within CleverTap. It must be unique for each Partner. The system automatically converts the value to lowercase. Special characters are permitted, but spaces are not.                                                |
| **List name**        | This is the name of the voucher list used for communication campaigns. For example, *Holi 2025 Sale*.  It does not describe individual voucher codes but serves as an identifier for the list.                                                                                                                                                                      |
| **List description** | This field defines the usage conditions of the voucher codes uploaded in a voucher list. For example, *Offer is applicable on orders above $100*.                                                                                                                                                                                                                   |
| **Files**            | Upload a CSV file with voucher codes. The maximum file size must not exceed 50MB. Add voucher codes in a single column without comma-separated values. If multiple columns are added, the system rejects the file.                                                                                                                                                  |
| **Expiry**           | Set up an expiration date for the voucher list. Once the date expires, CleverTap stops distributing vouchers from this list. However, you can extend the expiration date if needed.                                                                                                                                                                                 |

5. Click **Create**.

<Image alt="Create Voucher List" align="center" border={true} src="https://files.readme.io/35630e17dd4b532c7684410023af475c5cc7bedc9ef2324b2a4c569f3d80f922-Create_Voucher_List.png">
  Setup Voucher List
</Image>

# View Upload History

Once a voucher file is uploaded, the system processes and validates the codes and records the upload logs against each voucher list. The *Upload* tab logs details of uploaded voucher files, helping you track and manage the upload process. 

To view the upload history of a voucher file, click the **List ID** of the desired voucher list, then select the *Uploads* tab.

<Image alt="View Uploads" align="center" border={true} src="https://files.readme.io/b5be60febe7a6c8d3a4e898129653f3b4b8fdfb32e9f0104cee692872fe7fa7f-Uploads_History_Tab.gif">
  View Uploads
</Image>

Each entry has the following fields:

<Table>
  <thead>
    <tr>
      <th>
        Column Name
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Timestamp**
      </td>

      <td>
        The date and time when the voucher file was uploaded.
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        <p>Indicates the current state of the upload process. The possible statuses are:</p><ul><li>**Completed**: The upload was successful, and all valid voucher codes have been processed.</li><li>**In Progress**: The system is still processing the uploaded file.</li><li>**Failed**: The upload encountered errors, and no codes were processed.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        **Uploaded By**
      </td>

      <td>
        Displays the email ID of the user who uploaded the voucher file.
      </td>
    </tr>

    <tr>
      <td>
        **File Name**
      </td>

      <td>
        Displays the name of the uploaded file.
      </td>
    </tr>

    <tr>
      <td>
        **Codes (Uploaded/Total)**
      </td>

      <td>
        Displays the number of voucher codes successfully uploaded compared to the total codes in the file.
      </td>
    </tr>

    <tr>
      <td>
        **Errors**
      </td>

      <td>
        Displays issues found during upload, such as duplicate codes or an invalid file format. It also indicates the total number of errors found in the uploaded file.  

        Issues found during upload, such as duplicate codes or an invalid file format. The total number of errors is also displayed.
      </td>
    </tr>
  </tbody>
</Table>

You can download the uploaded voucher file from the *Uploads* page for reference or troubleshooting.

<Image alt="Download Uploaded Vouchers File" align="center" border={true} src="https://files.readme.io/705175fec85decd3d94309734cc68c0a717eaf9c758cc1fd7740efa60a77a34b-Download_Voucher_File.png">
  Download Uploaded Vouchers File
</Image>

## Upload Codes

If your voucher list is running low on codes, you can add more vouchers without creating a new list. This ensures seamless voucher distribution and prevents disruptions in your campaigns.

To upload additional voucher codes:

* Use the Upload Codes option to add new vouchers to an existing list at any time.
* The system automatically validates new codes to prevent duplicates within the same list.
* Once uploaded, the newly added codes immediately become available for distribution.

> 📘 Errors in Uploading Codes
>
> If an error occurs during upload, for example, duplicate codes or invalid format, download the *Error File* from the *Uploads* tab. This file contains error codes and corresponding error messages. Correct the errors and re-upload the corrected file using the *Upload codes* flow against the same voucher list.

# Best Practices

To ensure smooth voucher list management and avoid disruptions in campaigns, follow these best practices:

* **Upload Unique Voucher Codes**: Ensure that all voucher codes in a list are unique to prevent duplication errors and maintain accuracy.
* **Monitor Status Regularly**: Keep track of the voucher list status to ensure it remains active for ongoing campaigns.
* **Maintain Unique List Tag**: Use meaningful and distinct identifiers for better organization and easy reference.
* **Keep Codes Updated**: Regularly upload new voucher codes to prevent depletion and ensure continuous availability.
