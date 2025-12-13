---
title: Automated Audit Log Exports for SIEM
excerpt: >-
  Learn how to configure CleverTap Audit Log exports to your cloud storage and
  integrate them with your SIEM tools for centralized security monitoring and
  compliance.
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

A Security Information and Event Management (SIEM) system enables organizations to collect, analyze, and correlate security data from multiple sources in real-time. It allows centralized visibility into potential threats, supports faster incident response, and simplifies compliance reporting.

CleverTap Audit Logs capture every security-relevant action in your account, including user access, configuration changes, and data exports. With the SIEM Integration for Audit Logs, you can automatically export these records to your preferred storage and analytics systems (AWS S3, Google Cloud Storage, or Microsoft Azure Blob Storage).

Once Audit Logs are exported on a set schedule, they can be integrated with SIEM tools such as Splunk, IBM QRadar, or Azure Sentinel on your end for unified monitoring, threat detection, and compliance reporting.

Audit Log exports are delivered once every 4 hours (based on your account’s time zone).

> 📘 **Add-on Feature**
>
> This feature is available as a paid add-on. To enable Automated Audit Log Exports for SIEM, contact your sales representative.

## Advantages

The SIEM integration for Audit Logs offers several key advantages that enhance security visibility, compliance, and operational efficiency.

* **Continuous Security Monitoring**: Feed logs directly to SIEM tools for anomaly detection and incident investigation. 
* **Regulatory Compliance**: Retain detailed records to meet audit and governance requirements.
* **Custom Retention Policies**: Maintain logs in your own bucket for the duration your organization requires.
* **Centralized Insights**: Correlate user activity with infrastructure and application events.

## Prerequisites

Before setting up the export, check the following:

* You have Admin access to your CleverTap account.
* You have an existing cloud storage bucket in AWS S3, Google Cloud Storage, or Azure Blob Storage.
* You can generate and provide access credentials (for example, AWS Access Key ID, Secret Access Key, GCP Service Account JSON, or Azure Connection String).
* The destination bucket allows write permissions from CleverTap’s export service.

> 📘 **Secure Log Delivery for Compliance Tracking**
>
> Customers in BFSI or regulated sectors often require SIEM integrations for continuous compliance tracking. CleverTap’s export mechanism ensures secure and traceable delivery of log files to your environment.

# Set Up SIEM Export


To configure automatic Audit Log exports, perform the following steps:

1. Log in to your CleverTap dashboard.
2. Go to *Settings > Partners*.
3. Select *Export Center*.
4. Click **Create Export**.
5. Choose *Audit Logs* as the export type.
6. Select your destination platform:

   * AWS S3
   * Google Cloud Storage
   * Microsoft Azure Blob Storage
7. Select an available bucket from the drop-down or add a new bucket using *Add*.
8. Click **Save** to activate the export.

Exports will automatically begin within 24 hours.

The following image shows the SIEM export for the Audit Logs:

<Image alt="SIEM Export for Audit Logs" align="center" border={true} src="https://files.readme.io/04275d38d7769d1d0b70296b58d4564cc5fa1f73497ebf21189c193c6518d0d6-2025-11-19_17-27-50_1.gif" />  SIEM Export for Audit Logs











> 📘 **Support**
>
> If you encounter issues with export delivery or access permissions, contact your Customer Success Manager or submit a support ticket through the CleverTap Support Portal.

## Data Delivery and Format

CleverTap delivers Audit Logs with the following schedule and file structure.

* **Delivery Frequency**: Once every 4 hours (starting from midnight as per account time zone).
* **Delivery Mode**: Incremental batch files delivered securely to your configured bucket.
* **File Format**: JSON (UTF-8 encoded).
* **File Naming Convention**: audit/&lt;account-encoded&gt;/audit*<account-encoded>*<timestamp>.zip

Each exported file includes the same fields visible in the Audit Logs dashboard:

| Field       | Description                                          |
| ----------- | ---------------------------------------------------- |
| Date        | Timestamp of the action.                             |
| Email       | Email address of the user who performed the action.  |
| Action      | The type of activity (Login, Export, Campaign Save). |
| Action ID   | Unique identifier of the resource impacted.          |
| Description | Summary of the activity.                             |
| IP Address  | Originating IP address of the request.               |

## Security and Permissions

The following security measures ensure your Audit Log exports remain protected throughout the export process:

* All exports are HTTPS-encrypted during transit.
* Credentials (access keys or tokens) are stored securely and used only for writing to your bucket.
* Bucket permissions can be revoked at any time without affecting dashboard-level access.
> 👍 **Security Tip**
>
> Always rotate access credentials periodically and restrict write access to a dedicated folder or prefix within your bucket.

## Verify Export Delivery

Once configured, perform the following:

1. Wait for the next scheduled export window (midnight).
2. Check your destination bucket for a new file with the prefix `audit`.
3. Validate file content and timestamps.

If you cannot view the files after 4 hours, verify the following:

* Bucket permissions (write access).
* Region configuration.
* Access credentials.

# FAQs

The following are some frequently asked questions to help you set up and manage your SIEM integration effectively:

### How often are logs exported?

Audit Logs are exported once every 4 hours starting from midnight (as per the account time zone).

### Can I export to multiple destinations?

Currently, you can configure only one destination per project.

### How to stop a running export?

You can stop a running export by reaching out to your Customer Support SPOC or it automatically stops if your paid add-on has expired.

### Can I manually trigger exports?

No. Exports run automatically every 4 hours.