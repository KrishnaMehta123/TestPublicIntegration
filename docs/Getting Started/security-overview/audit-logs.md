---
title: Audit Logs
excerpt: >-
  Learn how Audit Logs in CleverTap record and track user actions, configuration
  changes, and system activities to help you monitor security and maintain
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

Audit Logs in CleverTap record a detailed trail of all security-relevant actions in your account. These logs show who performed an action, what changes occurred, and when the activity happened.

You can use Audit Logs to monitor access, investigate incidents, and comply with security and regulatory requirements. You can view these logs directly on the dashboard or export them as a CSV file for offline review.

# Accessing Audit Logs

You can access and review Audit Logs from the CleverTap dashboard. To view the logs, do the following:

1. Log in to your CleverTap account.
2. Navigate to **Settings > Audit Logs**.
3. Apply the date range to filter and view the logs for a specific period.
4. Use **Download All Logs** to export logs in CSV format.

<Image align="center" alt="Audit Logs in CleverTap" border={true} caption="Audit Logs at CleverTap" src="https://files.readme.io/b7b52012580073a2eda9b79f2782a4b035a9e8e03f53454e6a5d55c9ef4a7974-image.png" />

The Audit Logs dashboard displays a structured table of activities. The logs show which user performed an action, what resource the action affected, and where the action originated.

## Log Fields

Each log entry includes the following fields:

| Field           | Description                                                            |
| --------------- | ---------------------------------------------------------------------- |
| **Date**        | Timestamp of the action, shown in your account's time zone.            |
| **Email**       | The email address of the user who performed the action.                |
| **Action**      | The type of action performed, such as Login, Campaign, or Export.      |
| **Action ID**   | The unique identifier of the impacted resource, such as a Campaign ID. |
| **Description** | A descriptive message about the action, such as _Saved Campaign_.      |
| **IP Address**  | The IP address where the action originated.                            |

The following are examples of recorded activity:

* A user logging in from a specific IP address.
* A campaign created, saved, or stopped with its campaign ID.
* A data export initiated by a user.

## Events Captured

Audit Logs record activities across multiple categories to provide complete visibility into account actions. The following are the Audit logs recorded in CleverTap:

* [Authentication Logs](doc:audit-logs#authentication-logs)
* [Role and Permission Changes](doc:audit-logs#role-and-permission-changes)
* [Privileged and Sensitive Activities](doc:audit-logs#privileged-and-sensitive-activities)
* [System and Integration Events](doc:audit-logs#system-and-integration-events)

### Authentication Logs

These logs capture user login and access activity.

* User login (success)
* User logout
* Session expired
* Password reset
* User account locked

> 📘 Note
>
> Auth0 maintains Authentication failures, MFA attempts, and unusual login patterns, which are not included in CleverTap Audit Logs.

### Role and Permission Changes

These logs capture changes that affect user roles and access.

* User invited to a project
* User removed from a project
* Roles created or deleted
* Role assignments or removals
* Role permissions details
* Administrative privilege escalations

### Privileged and Sensitive Activities

These logs capture high-impact actions that affect configurations, security, or data.

* Data export or download initiated
* Project configuration changed
* API key or token created or revoked
* Audit Log accessed

### System and Integration Events

These logs capture system-driven activities and integration-level changes.

* Campaign created, updated, or deleted
* Journey created, updated, or deleted
* Segment created, updated, or deleted
* Integration connected or disconnected
* API access logs

## Exporting Audit Logs in CSV

You can export Audit Logs from the dashboard to preserve records or perform offline analysis. To export audit logs in CSV, perform the steps below:

1. Click **Download All Logs** to export the complete set of logs in CSV format.
2. Exported CSV files include the same fields as the dashboard view.
3. Export logs periodically if you require long-term retention or external analysis.

## Export Audit Logs into S3/GCP/Azure

CleverTap allows you to automatically export Audit Logs to AWS S3, Google Cloud Storage, or Microsoft Azure Blob Storage, with logs delivered once every 24 hours at midnight (account time zone), enabling long-term retention, compliance, and integration with SIEM tools.

> 📘 Note
>
> To enable the Audit Logs into S3/GCP/Azure, reach out to your Customer Support Manager.

# FAQs

### Do Audit Logs include failed login attempts?

No. Auth0 manages authentication failures. Contact CleverTap Support for these records.

### Can I stream Audit Logs to my SIEM system?

Yes. You can configure automated exports to AWS S3, Google Cloud, or Microsoft Azure and connect them to your SIEM tools for monitoring.

### Who can access Audit Logs?

Only account admins can view, download, and configure exports for Audit Logs.
