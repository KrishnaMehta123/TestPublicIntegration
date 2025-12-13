---
title: System Maintenance
excerpt: >-
  Learn about the CleverTap system maintenance schedule, its impact on
  operations, and key recommendations for adequate preparation to minimize
  disruptions.
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

CleverTap will undergo scheduled system maintenance to enhance platform stability and performance. The CleverTap dashboard and certain functionalities will be temporarily unavailable during this time. 

This document details the expected impact and recommendations to help you prepare for this maintenance window.

# Impact on Operations

During the maintenance window, some features of the CleverTap dashboard will be unavailable, while others will remain accessible. Here is an overview of the affected projects and the service availability during this period.

## Service Availability

Here is a breakdown of what is accessible on the CleverTap dashboard during the maintenance period:

| Accessible During Maintenance | Not Accessible During Maintenance                           |
| :---------------------------- | :---------------------------------------------------------- |
| Logging into the dashboard    | Dashboard queries                                           |
| Raising support tickets       | Analytics and campaign statistics                           |
|                               | PBS and Live Action campaigns                               |
|                               | Data ingestion via API, SDK, and other endpoints (SFTP, S3) |

# Key Recommendations

To ensure a smooth transition and minimize disruption during the maintenance, follow these recommendations:

* **Prepare Campaigns in Advance**: Schedule all PBS and Live Action campaigns to run before or after the maintenance period.
* **Pre-download Required Reports**: Extract any critical analytics or campaign performance data beforehand.
* **Submit Data Early**: Complete data ingestion tasks through APIs, SDKs, or other endpoints before the maintenance begins.
* **Notify Your Team**: Share this information with all relevant stakeholders to avoid confusion during the maintenance window.

# Post Maintenance

Once the maintenance concludes, all services will resume as usual. CleverTap can address any delayed campaigns or queries immediately afterward. If you encounter any issues, contact [CleverTap Support](doc:support-ticket) for assistance.

# FAQs

### Q. Why is this maintenance necessary?

A. This maintenance is part of our ongoing efforts to improve platform stability and enhance overall performance.

### Q. Will my campaigns run during the maintenance time?

A. PBS and Live Action campaigns will not function during the maintenance period. Any campaigns scheduled to be sent during the maintenance time will be automatically queued and sent after the maintenance period concludes. We recommend you plan your campaigns accordingly.

### Q. What happens if I need to ingest data during the maintenance?

A. Data ingestion via API, SDK, and other endpoints will be temporarily unavailable during maintenance. However, no data will be lost. All incoming data will be securely stored in a processing queue and automatically ingested once the system is back online. We recommend completing ingestion tasks before the maintenance begins to avoid delays.

### Q. Can I still raise support tickets?

A. Yes, raising support tickets will remain available through alternate channels.

### Q. Who can I contact for further assistance?

A. If you experience any issues post-maintenance, reach out to [CleverTap Support](doc:support-ticket) for help.
