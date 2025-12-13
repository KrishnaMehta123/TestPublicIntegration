---
title: DataChannel
excerpt: Workflow Automation
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

[DataChannel](https://www.datachannel.co/) is a cloud-based ETL platform that allows businesses to integrate and load data from various sources, such as CleverTap, into data warehouses such as Amazon Redshift, Google BigQuery, or Snowflake.

With CleverTap and DataChannel integration, you can:

- **360-Degree Customer View**: Sync CleverTap [user profiles](https://developer.clevertap.com/docs/concepts-user-profiles) (demographics, preferences, activity) with a data warehouse to unify customer data across multiple sources for better personalization.
- **Behavioral Analytics & Funnel Optimization**: Export CleverTap [event data](https://developer.clevertap.com/docs/events) (app visits, purchases, drop-offs) to analyze user journeys, identify friction points, and optimize conversion funnels.
- **Cross-Channel Attribution & Campaign Performance**: Merge CleverTap events (email opens, push notifications, in-app actions) with CRM and ad platform data to measure marketing impact and refine targeting.

This powerful combination boosts customer engagement and drives impactful marketing and business results.

# Prerequisites for Integration

The following are the prerequisites:

- Ensure you have a DataChannel account.
- Ensure you have a destination data warehouse (for example, Amazon Redshift, Google BigQuery, Snowflake) set up and accessible in DataChannel account.
- Ensure you have a CleverTap account with a valid **Account ID**, **Passcode**, and **Region**.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by DataChannel. The CleverTap and DataChannel integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [DataChannel](https://www.datachannel.co/contact-us) for support and resolution.

# Integrate DataChannel with CleverTap

This process involves the following three major steps:

1. [Add CleverTap as a Source on DataChannel](doc:datachannel#add-clevertap-as-a-source-on-datachannel)
2. [Configure the Data Warehouse as a Destination on DataChannel](doc:datachannel#configure-the-data-warehouse-as-destination-on-datachannel)
3. [Create and Configure Data Pipelines](doc:datachannel#create-and-configure-data-pipelines)

## Add CleverTap as a Source on DataChannel

To add CleverTap as a source in DataChannel for exporting data from CleverTap to Datachannel:

1. Go to _Exporte Connections_ from your DataChannel dashboard and search for _CleverTap_.
2. Click ![Edit Icon](https://files.readme.io/074d4735641e94db6a3a89bc2572d8d54d34ddf42f2fb15d4acf6afd45673103-2025-02-20_13-52-51.png)  icon to create a new pipeline.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1aae59765891469cd4c260657ca8e8616271c70b17ea2a13b9f53fac98d590a4-image.png",
        null,
        "Add CleverTap as a Source on DataChannel"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Add CleverTap as a Source on DataChannel"
    }
  ]
}
[/block]


3. Enter the following details:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/063fc3d08049f1c072dcf87d0faf6381228639e2ac24713a98de1721b4281247-image.png",
        null,
        "Connect CleverTap as a source"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Connect CleverTap as a source"
    }
  ]
}
[/block]


4. Click **Save** to add CleverTap as a source once the connection is verified.

## Configure the Data Warehouse as Destination on DataChannel

After adding CleverTap as a source, configure the [data warehouse](https://docs.datachannel.co/getting-started/1.0.0/applications/cloud_application/clevertap/setup.html) to store the extracted data from CleverTap. To do so, follow these steps:

> ❗️ Data Warehouse selection
> 
> Data Warehouse once selected cannot be changed.

1. Navigate to the _Connect Your DataSource_ section in DataChannel.
2. Select your preferred Data Warehouse from the available options (for example, [Amazon Redshift](https://docs.datachannel.co/getting-started/1.0.0/destinations/redshift.html), [Google BigQuery](https://docs.datachannel.co/getting-started/1.0.0/destinations/bigquery.html), [Snowflake](https://docs.datachannel.co/getting-started/1.0.0/destinations/snowflake.html), [Azure Synapse](https://docs.datachannel.co/getting-started/1.0.0/destinations/azure-synapse.html), and [MySQL](https://docs.datachannel.co/getting-started/1.0.0/destinations/mysql.html)).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0c8f8b7d9147c7ff513b9ec5481c2eb74c9f28ff749a441d6e3dd4de4e2ad64-image.png",
        null,
        "Connect DataSource"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Connect DataSource"
    }
  ]
}
[/block]


3. Add your data warehouse as a destination by providing the required connection details and click **Continue**.

## Create and Configure Data Pipelines

Once CleverTap is connected and the data warehouse is set up, configure data pipelines to determine what data should be extracted from CleverTap and sent to the data warehouse.

Considering a use case to create and configure data pipelines:

**Tracking User Engagement Trends:** To illustrate the process, consider a business that wants to track daily user engagement trends from CleverTap and store them in [Google BigQuery](https://docs.datachannel.co/getting-started/1.0.0/destinations/bigquery.html) for analysis. To do so, follow these steps:

1. Define Data Sources: Select a data pipeline that suits your use case, and refer to [List of Available](https://docs.datachannel.co/getting-started/1.0.0/applications/cloud_application/clevertap/pipelines.html). In this use case, we will select **[Trend Analysis - Daily](https://docs.datachannel.co/getting-started/1.0.0/applications/cloud_application/clevertap/pipelines/trend-analysis-daily.html)** to track daily user engagement trends from CleverTap

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf6407952e653d3789c78c26b0fa1e57074660824aa8e4a8ae02ab859cc1fccf-Screen_Recording_2025-01-07_at_3.46.27_PM_1.gif",
        "",
        "Define Data Sources"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Define Data Sources"
    }
  ]
}
[/block]


2. Report Details Configuration: This pipeline can be used to request and retrieve the details of user events from CleverTap. Enter the following details:

| **Parameters** | **Description**                                                                                                                                                             |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Event Name     | The event type needed includes both standard and custom events.                                                                                                             |
| Number of Days | The number of days for which you wish to get the data in each run.                                                                                                          |
| Insert Mode    | UPSERT will insert only new records or records with changes; APPEND will insert all fetched data at the end; REPLACE will drop the existing table and recreate a fresh one. |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e1c709d9f4d022f864ec970f07b65a357642e0b27f43234166a776ccfe92465f-image.png",
        null,
        "Report Details Configuration"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Report Details Configuration"
    }
  ]
}
[/block]


3. [Schedule Data Sync](https://docs.datachannel.co/getting-started/1.0.0/set-up/scheduling.html): Choose a schedule for running the data pipeline:
   - [Manual Run](https://docs.datachannel.co/getting-started/1.0.0/set-up/scheduling.html#_manual_run): Manually trigger the pipeline whenever required.
   - [Scheduled Run](https://docs.datachannel.co/getting-started/1.0.0/set-up/scheduling.html#_scheduled_run): Select a predefined schedule from the dropdown options.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/91aff1bc2a0fd6ef0dc09200a5015ba49e871fda995caa4ab49d27eb8ca714ee-image.png",
        null,
        "Schedule Data Sync"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Schedule Data Sync"
    }
  ]
}
[/block]


4. [Entering Dataset Details](https://docs.datachannel.co/getting-started/1.0.0/set-up/naming_syncs.html):
   1. Provide a Name for the dataset.
   2. (Optionally) Add a Description for better identification.
   3. Check mark the _Run after save_ to save the integration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bd7cbae70657595fb0dd625366b8d83dcc578850617ff3f662e1b80ec129a6b-Screenshot_2025-01-07_at_4.28.32_PM.png",
        null,
        "Finalize Setup"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Finalize Setup"
    }
  ]
}
[/block]


5. Click **Submit** to finalize the setup and run the data export.
6. Select _Numbers of Runs_ to monitor the pipeline and check the status of your pipeline in the dashboard.  
   The statuses include:
   - Running
   - Successful
   - Error (if there are issues)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a047673546c5bc35b97183fedd7a64caf7291d78ed78e6696ac5927d2e07f92a-image.png",
        null,
        "Monitor the pipeline"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Monitor the Pipeline"
    }
  ]
}
[/block]


7. Select _Data Preview_ to preview the data once the pipeline has successfully run.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/58f48d341c6547bd17ad9d0b1429ce790815d4f07f37c45778564a186a751fd9-image.png",
        null,
        "Data Preview"
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Data Preview"
    }
  ]
}
[/block]


# FAQs

### What should I do if my data is not syncing properly?

If your data is not syncing, try the following steps:  

1. **Check Pipeline Status** – Ensure the data pipeline is active.  
2. **Verify Destination Setup** – Confirm that the data warehouse is correctly configured.  
3. **Review Logs** – Check logs in DataChannel for errors or failures.  
4. **Confirm API Access** – Make sure CleverTap API access is enabled.  
5. **Check Sync Schedule** – Ensure the pipeline is running at the scheduled time.  

If the issue persists, contact **[DataChannel Support](https://www.datachannel.co/contact-us)** for assistance.