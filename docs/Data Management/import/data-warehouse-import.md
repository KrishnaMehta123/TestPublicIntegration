---
title: Data Warehouse Import
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

The Data Warehouse section introduces the native integrations that enable you to bring large volumes of data from your enterprise warehouse into CleverTap.

This document provides an overview of the supported warehouse partners and the associated workflows for configuring imports, mapping fields, and scheduling automated data pipelines.

# Data Warehouse Sources

This section provides an overview of the data warehouse platforms that CleverTap supports for direct data ingestion.

[block:html]
{
  "html": "<style>\n  .grid {\n    display: grid;\n    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));\n    gap: 1rem;\n    padding: 0 1rem;\n    max-width: 100%;\n    margin: 0 auto;\n  }\n\n  .integration-card {\n  display: flex;\n  align-items: center;\n  justify-content: flex-start;\n  padding: 1.5rem 1rem; /* add top & bottom padding */\n  min-height: 64px; /* ensures consistent tile height */\n  background: #fff;\n  border-radius: 12px;\n  border: 1px solid rgba(0, 0, 0, 0.08);\n  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);\n  transition: box-shadow 0.2s ease-in-out;\n  text-decoration: none;\n}\n\n  .integration-card:hover {\n    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);\n  }\n\n  .icon {\n    width: 24px;\n    height: 24px;\n    stroke: #2b2e33;\n    flex-shrink: 0;\n  }\n\n  .name {\n    font-size: 1rem;\n    font-weight: 600;\n    color: #2b2e33;\n  }\n</style>\n<div class=\"grid\">\n  <a href=\"https://docs.clevertap.com/docs/snowflake-configuration\" class=\"integration-card\">\n    <div class=\"name\">Snowflake</div>\n  </a>\n  <a href=\"https://docs.clevertap.com/docs/databricks-configuration\" class=\"integration-card\">\n    <div class=\"name\">Databricks</div>\n  </a>\n<a href=\"https://docs.clevertap.com/docs/bigquery-configuration\" class=\"integration-card\">\n    <div class=\"name\">BigQuery</div>\n  </a>\n  <a href=\"https://docs.clevertap.com/docs/redshift-configuration\" class=\"integration-card\">\n    <div class=\"name\">Redshift</div>\n  </a>\n</div>"
}
[/block]


# Prerequisites

Before you begin, ensure you have the following:

- A data warehouse account integrated with CleverTap.
- Necessary permissions to create and manage imports.
- Access to the data warehouse database with correctly configured data.
- Identified data to be imported (**User Profile Data** or **Event Data**).

# Quick Start Guide for Data Warehouse Import

This section serves as a technical reference for users who have previously configured an Import and require a brief procedural overview before contacting support. It outlines the essential steps involved in setting up and executing a Data Warehouse Import.

[block:html]
{
  "html": "<style>\n  .grid {\n    display: grid;\n    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));\n    gap: 1rem;\n    padding: 0 1rem;\n    max-width: 100%;\n    margin: 0 auto;\n  }\n\n  .integration-card {\n  display: flex;\n  align-items: center;\n  justify-content: flex-start;\n  padding: 1.5rem 1rem; /* add top & bottom padding */\n  min-height: 64px; /* ensures consistent tile height */\n  background: #fff;\n  border-radius: 12px;\n  border: 1px solid rgba(0, 0, 0, 0.08);\n  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);\n  transition: box-shadow 0.2s ease-in-out;\n  text-decoration: none;\n}\n\n  .integration-card:hover {\n    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);\n  }\n\n  .icon {\n    width: 24px;\n    height: 24px;\n    stroke: #2b2e33;\n    flex-shrink: 0;\n  }\n\n  .name {\n    font-size: 1rem;\n    font-weight: 600;\n    color: #2b2e33;\n  }\n</style>\n\n<div class=\"grid\">\n  <a href=\"https://docs.clevertap.com/docs/create-import\" class=\"integration-card\">\n    <div class=\"name\">Set Up Import</div>\n  </a>\n  <a href=\"https://docs.clevertap.com/docs/map-data-for-import\" class=\"integration-card\">\n    <div class=\"name\">Map Data</div>\n  </a>\n<a href=\"https://docs.clevertap.com/docs/schedule-import\" class=\"integration-card\">\n    <div class=\"name\">Schedule Import</div>\n  </a>\n  <a href=\"https://docs.clevertap.com/docs/import-listing-and-stats\" class=\"integration-card\">\n    <div class=\"name\">Import Listing and Stats</div>\n  </a>\n</div>"
}
[/block]