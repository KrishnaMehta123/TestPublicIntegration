---
title: BigQuery Configuration
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

1. In the Google Cloud Console, navigate to *IAM & Admin > Service Accounts*.
2. Click **Create Service Account**.
3. Enter a **Service account name** (for example, `clevertap-bq-sa`).
4. Click **Create and continue**, then **Done**.

### Assign BigQuery Permissions

Assign the required roles to the service account:

1. Go to *IAM & Admin > IAM*. Go to the *Service account*.
2. Locate the service account and click **Manage Permissions**.
3. Click on **Manager Access**.
4. Add the following roles:

   * **BigQuery Job User**
   * **BigQuery Data Editor**
5. Click **Save**.

### Create Service Account JSON Key

Generate a JSON key that CleverTap will use for authentication:

1. In *IAM & Admin > Service Accounts*, select the service account.
2. Open the **Keys** tab.
3. Click **Add key > Create new key**.
4. Select **JSON** and click **Create**.
5. Download and securely store the JSON file.

### Create Dataset

Create a dataset for CleverTap to store and query data:

1. Go to *BigQuery* in the Google Cloud Console.
2. Select your project and click **Create dataset**.
3. Enter:

   * **Dataset ID** (for example, `clevertap_dataset`)
   * **Location** (choose the required region)
4. Click **Create dataset**.

Or use SQL:

## Use Existing BigQuery Resources

If your project already has datasets and service accounts configured, follow the steps below to retrieve required values.

### Find Your Project ID

1. Open Project Picker next to the Google Cloud logo.
2. Copy the **Project ID** of the target project.

### Find Existing Dataset ID

1. Go to *BigQuery*.
2. Expand your project to view datasets.
3. Select the dataset you intend to use with CleverTap.

Or use SQL:

### Find a Service Account

1. Navigate to *IAM & Admin > Service Accounts*.
2. Select an existing service account with sufficient permissions, or create a new one.

### Download or Create a Service Account JSON Key

1. Select the service account.
2. Go to the **Keys** tab.
3. Create a new JSON key if needed.

# Set Up CleverTap Dashboard for Integration

After preparing your BigQuery project, dataset, and service account, connect BigQuery to CleverTap using the collected values.

![](https://files.readme.io/90a4cea28203917d02cabc0c6ea3483bd5344657ba5d867f4446f0b1b1d5d9ac-image_74.png) Integrate BigQuery with CleverTap

1. Go to *Settings > Partners > BigQuery* and select **Add Database**.
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

4. After saving the connection, navigate to *[Create Import](doc:data-warehouse-import)* in the *Import Connections* dashboard.

# FAQs

### How can I delete a connection that has running imports?

Go to *Import Connections*, select the connection, click **Delete**, review the running imports, and confirm deletion. This stops all active imports associated with the connection.

### How can I filter import connections?

Use the filters on *Import Connections* to refine the list:

* **Connected On**: Filter by creation date.
* **Connected By**: Filter by the user who created the connection.

### How can I whitelist IPs for CleverTap integration?

Whitelist the required IP ranges to allow CleverTap to access your Google Cloud project. Refer to **CleverTap IP Ranges** for the latest list.
