---
title: Data Warehouse
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

The Data Warehouse section introduces the integrations that enable you to bring large volumes of data from your warehouse into CleverTap. It also provides an overview of the supported warehouse partners and the associated workflows for configuring imports, mapping fields, and scheduling automated data pipelines.

# Data Warehouse Sources

This section provides an overview of the data warehouse platforms that CleverTap supports for direct data ingestion.

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
  <a href="https://docs.clevertap.com/docs/snowflake" class="integration-card">
    <div class="name">Snowflake</div>
  </a>
  <a href="https://docs.clevertap.com/docs/databricks" class="integration-card">
    <div class="name">Databricks</div>
  </a>
<a href="https://docs.clevertap.com/docs/bigquery" class="integration-card">
    <div class="name">BigQuery</div>
  </a>
</div>
`}</HTMLBlock>

# Prerequisites

Before you begin, ensure you have the following:

* A data warehouse account integrated with CleverTap.
* Necessary permissions to create and manage imports.
* Access to the data warehouse database with correctly configured data.
* Identified data to be imported (**User Profile Data** or **Event Data**).

# Quick Start Guide for Data Warehouse Import

This section serves as a technical reference for users who have previously configured an Import and require a brief procedural overview before contacting support. It outlines the essential steps involved in setting up and executing a Data Warehouse Import.

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
  <a href="https://docs.clevertap.com/docs/create-import" class="integration-card">
    <div class="name">Set Up Import</div>
  </a>
  <a href="https://docs.clevertap.com/docs/map-data-for-import" class="integration-card">
    <div class="name">Map Data</div>
  </a>
<a href="https://docs.clevertap.com/docs/schedule-import" class="integration-card">
    <div class="name">Schedule Import</div>
  </a>
  <a href="https://docs.clevertap.com/docs/import-listing-and-stats" class="integration-card">
    <div class="name">Import Listing and Stats</div>
  </a>
</div>
`}</HTMLBlock>
