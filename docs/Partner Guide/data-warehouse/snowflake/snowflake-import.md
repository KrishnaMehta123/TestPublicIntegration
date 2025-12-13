---
title: Snowflake Import
excerpt: >-
  Learn how to seamlessly import your data from Snowflake into CleverTap to
  streamline workflows and boost user engagement through efficient data
  integration.
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

The Snowflake Import feature enables seamless import and synchronization of data from your Snowflake database into CleverTap. This integration ensures you maintain up-to-date customer insights for segmentation, analytics, and engagement.  

With Snowflake Import, you can:  

- Automate **User Profile Data** and **Event Data** imports.  
- Perform a **Dry Run** to validate your configuration before importing.  
- Schedule imports with custom intervals or run them manually as needed.  
- Ensure data accuracy through identity mapping and timestamp-based sync. 

> 📘 Private Beta
> 
> CleverTap's integration with Snowflake is currently in Private Beta. Contact your Customer Success Manager for access.

# Prerequisites

Before you begin, ensure you have the following:  

- A Snowflake account integrated with CleverTap.  
- Necessary permissions to create and manage imports.  
- Access to the Snowflake database with properly configured data.  
- Identified data to be imported (**User Profile Data** or **Event Data**).  

# Quick Start Guide for Snowflake Import

This section is intended for users who have previously set up **Snowflake Import** and need a quick refresher on technical steps for Snowflake Import before contacting support. The following are the key steps for Snowflake Import:

1. [Set Up Snowflake Import](doc:snowflake-import#set-up-snowflake-import)
2. [Map Data and Identity](doc:snowflake-import#map-data-and-identity)
3. [(Optional) Perform a Dry Run](doc:snowflake-import#optional-perform-a-dry-run)
4. [Schedule Import](doc:snowflake-import#schedule-import)

## Set Up Snowflake Import

To start an import, navigate to **Settings > Partners > Import Center > Create Import**, then select **Snowflake**.  

Ensure that:  

- Your **Snowflake database is integrated** with CleverTap.  
- You configure the **import nickname, database selection, and query type (SQL or Tab)**.  
- Use **Preview Results** to validate the query before saving the configuration.  

For detailed steps, refer to [Create Import](doc:create-snowflake-import).  

## Map Data and Identity

CleverTap requires mapping Snowflake data to either **User Profile Data** or **Event Data**.  

- **Identity Mapping:** Choose from the following options:  
  - **Identity**: Uses email, phone number, or other unique identifiers to match users.  
  - **CleverTap ID**: Uses CleverTap’s system-generated ID to track users.  
- **Updated On Mapping:** Ensures only new or updated rows are imported.  
- **User & Event Property Mapping:** Assign Snowflake fields to CleverTap attributes.  

For more information, refer to [Map Data for Snowflake Import](doc:map-data-for-snowflake-import).  

## (Optional) Perform a Dry Run

A **dry run** allows you to test the import setup without affecting live data.  

- Checks for **data mapping errors, missing fields, or syntax issues**.  
- Displays validation results, including profile updates and new profile creation.  

For error handling and troubleshooting, refer to [Perform Dry Run](doc:map-data-for-snowflake-import#perform-dry-run-recommended).  

## Schedule Import

To automate data imports, configure a **schedule** based on business needs:  

- **Repeat Intervals**: Automate imports at fixed intervals (hourly, daily, and so on).  
- **Custom Schedule**: Set up imports on specific days of the week or month.  
- **Manually Trigger**: Run imports immediately or at a specific date/time.  

For setup instructions, refer to [Schedule Import](doc:schedule-snowflake-import).  

# Monitor Import Status and Stats

Track and troubleshoot import progress via the **Import Listing** page.  

- View **status, frequency, and health** of imports.  
- Use filters to track imports by **date, creator, or status**.  
- Analyze **import stats**, including **total records, success rate, and errors**.  

For more information, refer to [Import Listing and Stats](doc:snowflake-import-listing-and-stats).