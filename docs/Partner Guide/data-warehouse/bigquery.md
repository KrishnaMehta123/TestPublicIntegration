---
title: BigQuery
excerpt: ''
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

Configuring Google BigQuery with CleverTap enables seamless data import, ensuring synchronization and access to relevant information for analysis, personalized engagement, and data-driven growth.

> 📘 Note
>
> BigQuery is a private beta release. Contact your Customer Success Manager for access.

# Quick Start Guide for Existing Users

<details>
  <summary>Expand for quick setup if your BigQuery environment is already configured.</summary>

  <hr />

  This section is intended for users who already have a configured BigQuery project, dataset, and service account with the required permissions.

  ## Prerequisites

  Before you begin, ensure you already have the following details:

  * **Project ID**
  * **Dataset ID**
  * **Google Service Account JSON Key** (file or JSON text)

  Once you have these values, you can now proceed to add them in CleverTap (see *Set Up CleverTap Dashboard for Integration*).
</details>

# Prerequisites for Integration

If you are setting up BigQuery for the first time, ensure you have the following before proceeding with the CleverTap configuration:

* **CleverTap Access** to configure BigQuery integrations.
* **Google Cloud Project with BigQuery enabled**.
* **Required Dataset Details**:

  * Project ID
  * Dataset ID
* **Service Account and Permissions** used by CleverTap:

  * Recommended: a dedicated service account
  * Required roles:

    * **BigQuery Job User**
    * **BigQuery Data Editor**

# Set Up BigQuery for Integration

You can set up BigQuery using one of the following options:

* For new users who need to provision resources from scratch:
  * [Create a Service Account](#create-service-account),
  * [Assign BigQuery Permissions](#assign-bigquery-permissions),
  * [Create a Dataset](#create-dataset),
  * [Create a Service Account JSON Key](#create-service-account-json-key)

* For users who already have resources configured in Google Cloud: [Use Existing BigQuery Resources](#use-existing-bigquery-resources)

## Create New BigQuery Setup

If you do not already have a dataset, service account, or JSON key configured in Google Cloud, you must create them before connecting to CleverTap.

To create each resource, perform the following steps:

1. [Create a Service Account](#create-service-account)
2. [Assign BigQuery Permissions](#assign-bigquery-permissions)
3. [Create a Dataset](#create-dataset)
4. [Create a Service Account JSON Key](#create-service-account-json-key)

### Create Service Account

To allow CleverTap to access your BigQuery environment, first create a dedicated service account:

1. In the Google Cloud Console, click on ![](https://files.readme.io/cfd2c44400c28fea69ef0071381f439904b5e3678672e6b8a60a7f94422edd3f-Big_query_1.png)  navigate to _IAM & Admin > Service Accounts_.
2. Click **Create Service Account**.

   <Image align="center" border={true} caption="Create Service Account" src="https://files.readme.io/ebdda5aa27f331774b22fc80c051edcfc30150b4971c511f27b1c69d13decc38-big_query_2.png" />
3. Enter a **Service account name** (for example, `clevertap-bq-sa`).
4. Click **Create and continue**, then **Done**.

   <Image align="center" border={true} caption="Service Account Name" src="https://files.readme.io/f8accc2410e1ca0aed7e62389cffd088719090482f032fa10bd06fa87650ff4e-big_query_3.png" />

### Assign BigQuery Permissions

Assign the required roles to the service account:

1. In the Google Cloud Console, click on ![](https://files.readme.io/cfd2c44400c28fea69ef0071381f439904b5e3678672e6b8a60a7f94422edd3f-Big_query_1.png)  navigate to _IAM & Admin > Service Accounts_.
2. Locate the service account and click **Manage Permissions**.

   <Image align="center" border={true} caption="Manage Permissions" src="https://files.readme.io/c8cfdb534f2fc6a74ec903b6a6a91d7e4425f00bade1498b8c074bbba69baa97-Big_Query_4.png" />
3. Click on **Manage Access**.

   <Image align="center" border={true} caption="Manage Access" src="https://files.readme.io/1fc3eb1a644816830b4647391aaefa7d195c168fff00608cb6efef4ed7616fc4-Big_Query_5.png" />
4. Add the following roles:

   * **BigQuery Job User**
   * **BigQuery Data Editor**

     <Image align="center" border={true} caption="Add Roles" src="https://files.readme.io/2fb32a730950cf71532b5a3d7b8feb42df8c4c5d753b69ca8cb8e3b3b3642a82-big_query_6.png" />
5. Click **Save**.

### Create Service Account JSON Key

Generate a JSON key that CleverTap will use for authentication:

1. In the Google Cloud Console, click on ![](https://files.readme.io/cfd2c44400c28fea69ef0071381f439904b5e3678672e6b8a60a7f94422edd3f-Big_query_1.png)  navigate to _IAM & Admin > Service Accounts_.
2. Open the **Keys** tab.
3. Click **Add key > Create new key**.

   <Image align="center" border={true} caption="Create new key" src="https://files.readme.io/493ab42bf9ecd411c3441c09c35d3f30ab2484ff50331c97639a072ea116f334-Big_query_8.png" />
4. Select **JSON** and click **Create**.

   <Image align="center" border={true} width="75% " src="https://files.readme.io/cda52a9b26d122363c1a73efc4f23abed6480d2cd9832fd76908b4a03d8113dc-Big_Query_9.png" className="border" />
5. Download and securely store the JSON file.

### Create Dataset

Create a dataset for CleverTap to store and query data:

1. Go to _BigQuery_ in the Google Cloud Console.
2. Select your project and click **Create dataset**.
3. Enter:

   * **Dataset ID** (for example, `clevertap_dataset`)
   * **Location** (choose the required region)
4. Click **Create dataset**.

Or use SQL:

```sql
CREATE SCHEMA IF NOT EXISTS `[ProjectID].[DatasetID]`;
```

## Use Existing BigQuery Resources

If your project already has datasets and service accounts configured, follow the steps below to retrieve required values.

### Find Your Project ID

1. Open Project Picker next to the Google Cloud logo.
2. Copy the **Project ID** of the target project.

### Find Existing Dataset ID

1. Go to _BigQuery_.
2. Expand your project to view datasets.
3. Select the dataset you intend to use with CleverTap.

Or use SQL:

```sql
SELECT schema_name FROM `projectID`.INFORMATION_SCHEMA.SCHEMATA;
```

### Find a Service Account

1. Navigate to _IAM & Admin > Service Accounts_.
2. Select an existing service account with sufficient permissions, or create a new one.

### Download or Create a Service Account JSON Key

1. Select the service account.
2. Go to the **Keys** tab.
3. Create a new JSON key if needed.

# Set Up CleverTap Dashboard for Integration

After preparing your BigQuery project, dataset, and service account, connect BigQuery to CleverTap using the collected values.

![](https://files.readme.io/90a4cea28203917d02cabc0c6ea3483bd5344657ba5d867f4446f0b1b1d5d9ac-image_74.png) Integrate BigQuery with CleverTap

1. Go to _Settings > Partners > BigQuery_ and select **Add Database**.
2. Enter the following details:

| Field                          | Description                                                                                                                                                                                                                                |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Connection name**            | A unique name for this BigQuery connection.                                                                                                                                                                                                |
| **Project ID**                 | The Google Cloud project ID.                                                                                                                                                                                                               |
| **Dataset ID**                 | The dataset where CleverTap will read and write data.                                                                                                                                                                                      |
| **Google Service Account Key** | In the Upload JSON file tab, upload the JSON key generated during [Create Service Account JSON Key](doc:bigquery-configuration#create-service-account-json-key). Alternatively, use the Custom key tab to paste the JSON content directly. |

3. Click **Test Connection** or **Save**:

   * **Test Connection:** Verifies project access, dataset validity, and service account permissions.
   * **Save:** Stores the connection for use with imports.

4. After saving the connection, navigate to _[Create Import](doc:data-warehouse-import)_ in the _Import Connections_ dashboard.

# FAQs

### How can I delete a connection that has running imports?

Go to _Import Connections_, select the connection, click **Delete**, review the running imports, and confirm deletion. This stops all active imports associated with the connection.

### How can I filter import connections?

Use the filters on _Import Connections_ to refine the list:

* **Connected On**: Filter by creation date.
* **Connected By**: Filter by the user who created the connection.

### How can I whitelist IPs for CleverTap integration?

Whitelist the required IP ranges to allow CleverTap to access your Google Cloud project. Refer to **CleverTap IP Ranges** for the latest list.