---
title: Microsoft Azure
excerpt: Understand how to export data from CleverTap dashboard to Microsoft Azure.
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

[Microsoft Azure](https://azure.microsoft.com/en-in/), a Microsoft cloud computing platform, offers access to, management of, and development of applications and services through global data centers. The Microsoft Azure data export feature provides the capability to bulk export your CleverTap event data to Azure Blob Storage. You can use this for analysis in BI tools or storage in your data warehouse for analysis in the future.

> 📘 Feature Availability
> 
> This capability is a part of the _Enterprise_, _Advanced_, and _Cutting Edge_ plan. To activate this for your account, contact your Account Manager.

# Setup

The following are the two major steps involved in enabling this feature for your account:

1. [Create a Microsoft Azure Storage Account](doc:microsoft-azure#create-a-microsoft-azure-storage-account).
2. [Create a Blob Service Container](doc:microsoft-azure#create-a-blob-service-container).
3. [Generate a SAS Token](doc:microsoft-azure#generate-a-sas-token).
4. [Configure Microsoft Azure Blob Container details on the CleverTap Dashboard](doc:microsoft-azure#configure-microsoft-azure-blob-container-on-clevertap-dashboard).

> 📘 Data Export
> 
> Once you have set up both dashboards, you can configure export from the CleverTap dashboard. For more information, refer to the following: 
> 
> - [Data Exports](doc:data-exports) for Legacy Profile and Event Export flow
> - [Profile Exports](doc:profile-exports) for Enhanced Profile Export flow

## Create a Microsoft Azure Storage Account

To create a Microsoft Azure Storage Account:

1. Log in to your Microsoft Azure account and select _Storage Accounts_ from the left menu.  
2. Click **+ Create** to create a new storage account. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/214a3e7-Select_Storage_Account_from_the_left_menu.gif",
        null,
        "Select Storage Account from Left Manu"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Storage Account from Left Manu"
    }
  ]
}
[/block]


3. Enter the _Storage account name_, and do not modify the default settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9304d54-Enter_Storage_Account_Name.png",
        null,
        "Enter Storage Account Name"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Enter Storage Account Name"
    }
  ]
}
[/block]


4. Click **Review** and click **Create**. The following screen displays once the storage account is created:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/102207f-Storage_Account_created_successfully.png",
        null,
        "Storage Account Created Successfully"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Storage Account Created Successfully"
    }
  ]
}
[/block]


The storage account you created now appears under the _Storage accounts_ page.

## Create a Blob Service Container

To create a Blob Service Container:

1. Navigate to the _Blobs_ menu under the _Blob Service_ section of your storage account. 
2. Create **+ Container** to create a Blob Service Container within the storage account you created in the previous section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9763f96-Create_Blob_Service_Container.gif",
        null,
        "Create a Blob Storage Container"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Create a Blob Storage Container"
    }
  ]
}
[/block]


3. Enter the _Name_ of your Blob Service Container, and do not modify the other default settings.
4. Click **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e9032e-New_Container_popup.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "30% ",
      "border": true
    }
  ]
}
[/block]


## Generate a SAS Token

A Shared Access Signature (SAS) Token is a Uniform Resource Identifier (URI) that provides limited access to an Azure Storage container. It is used when you want to authorize access to storage account assets within a defined time frame while keeping your storage account key confidential. For more information about SAS, refer to [Delegate access by using a SAS Token](https://learn.microsoft.com/en-gb/rest/api/storageservices/delegate-access-with-shared-access-signature).

To generate a SAS Token:

1. Select the _Container_ and click the ![](https://files.readme.io/a593067-Ellipses_icon.png) icon.
2. Select _Generate SAS_ from the dropdown list. The _Generate SAS_ window opens on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e76239-Generate_SAS_Token.png",
        null,
        "Generate SAS Popup"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Generate SAS Popup"
    }
  ]
}
[/block]


3. Enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Signing method",
    "0-1": "Select **Account key** from the Signing method list. The Signing method provides secure delegated access to resources in your storage account. For more information, refer to [Types of shared access signatures](https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview#account-sas).",
    "1-0": "Signing key",
    "1-1": "Select any one key from the following options: <li> Key 1 </li> <li> Key 2 </li>.",
    "2-0": "Stored access policy",
    "2-1": "Select the _Stored access policy_ you want to define for your storage. When defining a policy, you need to define the following: start time, expiry time, and permissions for the signature. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container.  \n  \nWhen defined on a container, it grants permissions to the container itself or to the blobs that it contains. For more information, refer to [Define a stored access policy](https://learn.microsoft.com/en-us/rest/api/storageservices/define-stored-access-policy).",
    "3-0": "Permissions",
    "3-1": "This is a mandatory field. Select the permission for the request made with the service SAS. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container. If you have already assigned the required permissions to your stored access policy, the same permissions will be assigned to the request made with the service SAS. For more information, refer to [Account SAS Permissions by Operation](https://learn.microsoft.com/en-gb/rest/api/storageservices/create-account-sas#account-sas-permissions-by-operation).",
    "4-0": "Start and expiry date/time",
    "4-1": "Indicates the start and end date/time during which the blob SAS is valid. CleverTap recommends setting the expiration time to the maximum duration available. This is because you cannot export any data to the container if the expiration date has passed. For more information, refer to [Configure a SAS Expiration Policy](https://learn.microsoft.com/en-us/azure/storage/common/sas-expiration-policy?tabs=azure-portal#how-to-configure-a-sas-expiration-policy).",
    "5-0": "Allowed IP address",
    "5-1": "CleverTap recommends not adding any IP address range in this field. It indicates that Microsoft will accept export requests only from the IP address or range of IP addresses defined under this field. If you still want to add the IP address(es), you must whitelist the IP addresses listed under [CleverTap IP Ranges](https://developer.clevertap.com/docs/clevertap-ip-ranges).",
    "6-0": "Allowed protocols",
    "6-1": "Allowing requests over HTTPS only is recommended. This field indicates the protocols permitted for a request made with the service SAS."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


4. Click **Generate SAS token and URL**.

Copy the generated SAS token and URL, as you cannot access it later.

## Configure Microsoft Azure Blob Container on CleverTap Dashboard

To add your Microsoft Azure Blob Container to Clevertap:

1. Navigate to _Settings_ > _Partners_ and click **Integrate** against Mircosoft Azure. The _Integrate analytics partner - Microsoft Azure_ window displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/372d7a1-MSAzure.jpg",
        null,
        "Integrate analytics partner - Microsoft Azure"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Integrate analytics partner - Microsoft Azure"
    }
  ]
}
[/block]


2. Click **+ Microsoft Azure** to create a new bucket. The _Integrate Microsoft Azure Bucket_ window opens on the right side of the screen. 
3. Enter the _Bucket Nickname_. 
4. Select the _Azure Blob Storage Endpoint_.
   - Default: Enter the Blob Storage Account name. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb30e87-Default_Blob_Storage_Endpoint.png",
        null,
        "Default Blob Storage Account on Microsoft Azure Portal"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Default Blob Storage Account on Microsoft Azure Portal"
    }
  ]
}
[/block]


- Custom: Add a custom domain mapped to your Azure Blob Storage Endpoint. For more information about defining a custom endpoint, refer to [Map a Custom Domain](https://learn.microsoft.com/en-gb/azure/storage/blobs/storage-custom-domain-name?tabs=azure-portal#map-a-custom-domain).

2. Enter the container name that stores data on Azure and the SAS token we obtained in Step 4 of the Generate a SAS Token section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a27cb22-image.png",
        null,
        "Integrate Microsoft Azure Bucket"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Integrate Microsoft Azure Bucket"
    }
  ]
}
[/block]