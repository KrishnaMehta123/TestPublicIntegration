---
title: Nexla
excerpt: Data Warehousing and Analytics Platform
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[Nexla](https://www.nexla.com) is a unified data operations platform that enables teams to connect, transform, and monitor ready-to-use data across any system. Designed for analytics and AI workflows, Nexla simplifies complex data integrations using no-code and low-code tools.

With the CleverTap and Nexla integration, you can:

* Export campaign interaction events from CleverTap to data warehouses using _Data Warehouse Exports_ or _Webhook campaigns_.
* Transform and forward enriched data from Nexla to CleverTap using _Amazon S3_, _SFTP Imports_, or _Nexla’s REST API_.

This integration enables real-time, high-quality data flow between CleverTap and your enterprise data stack, powering personalized engagement and advanced analytics.

# Prerequisites for Integration

Ensure the following before starting the integration:

* An active Nexla account.
* Automated _Data Warehouse Exports_ or _Webhook campaigns_ configured in CleverTap.
* Access to your _BigQuery_ , or _Amazon S3_ account.

# Integrating Nexla with CleverTap

To integrate Nexla with CleverTap, perform the following five major steps:

1. [Export Data from CleverTap](doc:nexla#export-data-from-clevertap-to-your-data-warehouse)
2. [Add Data Source in Nexla](doc:nexla#add-data-source-in-nexla)
3. (Optional) [Send Webhook Data from CleverTap to Nexla](doc:nexla#optional-send-webhook-data-from-clevertap-to-nexla)
4. [Transform Data in Nexla](doc:nexla#transform-data-in-nexla)
5. [Import Data Back into CleverTap](doc:nexla#import-data-back-into-clevertap)

## Export Data from CleverTap to Your Data Warehouse

Use Data Warehouse Exports in CleverTap to send campaign interaction data to supported destinations such as:

* [BigQuery](https://docs.clevertap.com/docs/bigquery)
* [Amazon S3](https://docs.clevertap.com/docs/data-export-to-aws-s3)

<Image align="center" alt="Create Export" border={true} caption="Create Export" src="https://files.readme.io/d2bd87a881b08611cf192e3ce42e5875793ac33c1830a6eabfe5fdbd6f7cac3b-image.png" width="75% " />

Once configured, Nexla can pull this data directly from the connected source.

## Add Data Source in Nexla

To configure your data source, perform the following steps:

1. Log in to the Nexla dashboard.
2. Add the appropriate warehouse (such as BigQuery or Amazon S3). For more information, refer to [Add a Data Source in Nexla](https://docs.nexla.com/user-guides/data-sources/add-data-source).
3. Authenticate using your access credentials.

Once connected, Nexla begins ingesting the exported CleverTap data.

## (Optional) Send Webhook Data from CleverTap to Nexla

You can optionally use Webhook campaigns in CleverTap to push event data to Nexla in real time. You can do so by creating a connector webhook campaign with Nexla’s webhook URL as the endpoint.

Use this approach if you want immediate data delivery without waiting for exports.

To configure Webhooks, refer to [Send Webhooks from CleverTap](doc:create-message-webhook) and [Nexla Webhook Reference](https://docs.nexla.com/user-guides/connectors/webhook).

## Transform Data in Nexla

To apply custom logic or formatting before sending data to CleverTap, perform the following steps:

1. Locate the dataset in Nexla and click **Transform**.
2. Use the _Transform Builder_ to:

   * Rename fields
   * Apply conditions or filters
   * Add computed fields or enrichments
3. Click **Save** to transform the dataset.

For more information, refer to [Using the Transform Builder](https://docs.nexla.com/dev-guides/modifying-data/transforms/transforms).

## Import Data Back into CleverTap

You can send data from Nexla into CleverTap using one of the following options:

* [Nexla REST API Destination](doc:nexla#nexla-rest-api-destination)
* [Using SFTP Imports](doc:nexla#using-sftp-imports)

### Nexla REST API Destination

* Configure [Nexla](https://docs.nexla.com/user-guides/connectors/rest-api/rest-api-generic#3-data-destination) to use [CleverTap’s Upload Users or Events API](https://developer.clevertap.com/docs/api-overview).
* Format the JSON payload to match the API requirements.
* Ensure the following headers are set:

```http
X-CleverTap-Account-Id: <Your Account ID>
X-CleverTap-Passcode: <Your Passcode>
Content-Type: application/json
```

<Image align="center" alt="Edit Credentials" border={true} caption="Edit Credentials" src="https://files.readme.io/8e3197252c1565d94e0d79b56d15ba19467068d788e52ac40a4245dc9990cd94-image.png" width="55% " />

<Callout icon="⚠️" theme="warn">
  #### Note

  Select _Skip Credential Validation_  to set up header values manually using your CleverTap credentials.
</Callout>

### Using SFTP Imports

Export the transformed dataset from Nexla to a supported destination (for example, SFTP). Configure CleverTap to import the data using the native import capability. For more information, refer to [SFTP Import](https://developer.clevertap.com/docs/imports-via-sftp).

<Image align="center" alt="SFTP Imports" border={true} caption="SFTP Imports" src="https://files.readme.io/63788bc898378ab2ed85fc3bbdd67d7e5ad990db37e0d1db7ea80dad09df3db7-image.png" width="55% " />

# Verify Integration

Once your data flow is set up:

* Nexla monitors source and destination schema changes.
* Errors are flagged and visible in the Nexla dashboard.
* Any edits to the flow (such as sources, transformations, and destinations) are reflected automatically.

This enables a fully automated, scalable, and error-resilient integration between Nexla and CleverTap.
