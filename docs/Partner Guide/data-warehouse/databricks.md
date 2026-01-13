---
title: Databricks
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

[Databricks](https://docs.databricks.com/) is a cloud-based Lakehouse platform that unifies data engineering, data science, and analytics on a single foundation built on Delta Lake. It enables organizations to store, process, and analyze large volumes of data with governed access through Unity Catalog and high-performance SQL Warehouses.

> 📘 Private Beta
>
> Databricks is a private beta release. Contact your Customer Success Manager for access.

Integrating Databricks with CleverTap allows businesses to:

* Sync customer data from Databricks to CleverTap for personalized campaigns.
* Share features, model outputs, or segmentation from Databricks with CleverTap to enhance campaign targeting.
* Provide marketing teams with the latest customer insights without managing separate pipelines.

# Key Benefits

The following are the key benefits of integrating Databricks with CleverTap:

* **Unity Catalog governance**\
  Scope imports to the right catalog and schema with fine-grained permissions and built-in lineage.

* **Delta Lake reliability**\
  Import from ACID tables with schema evolution and time travel so you get consistent, auditable data.

* **Incremental sync with Change Data Feed**\
  Use Delta Change Data Feed or updated timestamps to pull only new and changed rows, reducing cost and run time.

* **Elastic SQL Warehouses**\
  Run imports on scalable SQL Warehouses with auto-stop for cost control and predictable performance.

* **Model and feature activation**\
  Bring ML scores and feature tables managed in Databricks into CleverTap for targeting and personalization.

* **Performance at scale**\
  Benefit from Photon execution, partition pruning, and caching for faster queries on large datasets.

* **Flexible sourcing**\
  Import from tables, views, or custom SQL so you can reuse your existing dbt models and notebooks.

* **End-to-end visibility**\
  Use Unity Catalog lineage to trace which upstream tables and jobs feed each CleverTap attribute or event.

# Resources

The following guides walk you through configuring the integration and importing data from Databricks:

* Databricks Configuration
* Databricks Import
