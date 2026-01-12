---
title: Data Warehouse
excerpt: ''
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

A data warehouse is a centralized platform used to store, process, and analyze data from multiple sources across an organization. CleverTap integrates with modern data warehouses to enable bi-directional data movement, allowing you to import warehouse data for activation and export engagement data for analysis and reporting.

With data warehouse integrations, you can use your warehouse as the system of record while leveraging CleverTap to drive personalized and timely customer engagement.

# Supported Warehouses

<HTMLBlock>{`
<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1rem;
    padding: 0 1rem;
    max-width: 100%;
    margin: 0 auto;
  }

  .integration-card {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding: 1.5rem 1rem; /* add top & bottom padding */
  min-height: 64px; /* ensures consistent tile height */
  background: #fff;
  border-radius: 12px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

  .integration-card:hover {
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  }

  .icon {
    width: 24px;
    height: 24px;
    stroke: #2b2e33;
    flex-shrink: 0;
  }

  .name {
    font-size: 1rem;
    font-weight: 600;
    color: #2b2e33;
  }
</style>
<div class="grid">
  <a href="https://docs.clevertap.com/docs/snowflake-configuration" class="integration-card">
    <div class="name">Snowflake</div>
  </a>
  <a href="https://docs.clevertap.com/docs/databricks-configuration" class="integration-card">
    <div class="name">Databricks</div>
  </a>
<a href="https://docs.clevertap.com/docs/bigquery-configuration" class="integration-card">
    <div class="name">BigQuery</div>
  </a>
  <a href="https://docs.clevertap.com/docs/redshift-configuration" class="integration-card">
    <div class="name">Redshift</div>
  </a>
</div>
`}</HTMLBlock>

# Key Benefits

## Import Data into CleverTap

Importing data from a data warehouse into CleverTap allows you to use centrally stored data to power segmentation and engagement.

* **Unified Customer Profiles**
  Enrich CleverTap user profiles with attributes, transactional data, and analytical outputs stored in your data warehouse to maintain a consistent customer view across systems.

* **Advanced Segmentation Using Warehouse Data**
  Create audience segments in CleverTap using historical, aggregated, or model-driven data from the warehouse, enabling more precise targeting.

* **Activation of Business and Analytical Insights**
  Use insights such as customer tiers, propensity scores, or lifecycle states generated in the warehouse as inputs for campaigns and journeys in CleverTap.

* **Warehouse as the System of Record**
  Keep the data warehouse as the primary source of truth while using CleverTap for engagement execution, reducing data duplication and simplifying governance.

## Export Data from CleverTap

Exporting data from CleverTap to a data warehouse enables comprehensive analysis and broader access to engagement data.

* **Centralized Engagement and Campaign Data**
  Export user events, engagement signals, and campaign interaction data from CleverTap to combine them with internal datasets such as CRM, revenue, or support data.

* **Deeper Analysis and Reporting**
  Analyze CleverTap data using SQL or business intelligence tools to build custom reports, funnels, cohorts, and long-term trend analyses.

* **Consistent and Warehouse-Ready Data Structure**
  Export data in a standardized and predictable format to support downstream processing, transformations, and analytics workflows.

* **Cross-Team Data Accessibility**
  Make CleverTap engagement data available to analytics, data science, and reporting teams without requiring access to the CleverTap dashboard.

# Supported Capabilities

CleverTap data warehouse integrations support the following capabilities:

* Import user attributes, events, and analytical outputs into CleverTap
* Export engagement, campaign, and system events from CleverTap
* Support one-time and recurring data synchronization
* Maintain identity consistency across CleverTap and warehouse systems

<br />

<br />

<br />

CleverTap allows you to export data via partners:

* <Anchor label="BigQuery" target="_blank" href="doc:bigquery">BigQuery</Anchor>
* [Databricks](doc:databricks-configuration)
* [Snowflake](doc:snowflake-configuration)

<br />
