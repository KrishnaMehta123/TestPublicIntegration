---
title: Metering Type - MAU Based
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

This document provides information about billing terminologies and calculations for MAU-based metering. The billing is based on the Billable MAU.  

# Billing Terminologies

## Monthly Active User (MAU)
An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user active on both devices with the same identity token is counted as one MAU.
An organization is charged based on the total number of MAUs across all projects, which means that if a user performs a qualifying event in multiple projects, they are counted once per project.

## Data Point
An event, event property, or profile property update is a data point, a usage measure associated with MAU. 

## Processed MAU
Processed MAU is calculated by dividing the total data points by the allowed data points per MAU (2,000 data points). In most cases, users perform fewer than 2,000 data points per month.

## Monthly Billable Users
The Monthly Billable Users is the highest of either of the following:
  * MAU 
  * Processed MAU
  * Contracted MAU tier

# Overages and Measurement
The billable unit for this metering is Monthly Billable Users (MBU). 

# Measurement and Limits
* Unit of measurement: Monthly Billable Users
* Overages: The overages are charged based on the mode of payment. 
  * Monthly payment: When the MBUs exceed the contracted MAU tier for any given month, the additional MAU is charged at 120% of the metering per MAU price.
 * Prepaid payment (3/6/12 months): MBUs are measured each month as the rolling average for the billing period. It means that you are not charged for the overage even if there is a spike in consumption during the contract period and the average consumption is lower. Additional MAU is charged at 120% of the metering per MAU price.  

# Account Lock and Suspension
If the usage limit reaches 110%, the dashboard access is restricted. The restriction means that even though data ingestion will continue, you will not be able to run campaigns, journeys, or queries. You can either upgrade to higher capacity (recommended) or pay for overages for the current month.  

The restriction is removed automatically after upgrading the plan.

# Alerts for Overages
All account admins receive alerts on their CleverTap dashboard and email notifications every time the account consumption exceeds 80%, 90%, 100%, 110%, and so on.

# Excluded Events
Some system events are excluded from the MAU and Data Point calculations.

## Events Excluded from Data Point Calculations
The following is the list of events that are excluded from the data point calculation:

  * UTM Visit
  * App Launched
  * Notification Clicked
  * App Installed
  * Notification Replied
  * App Upgraded
  * App Uninstalled
  * Notification Sent
  * Stayed
  * Notification Control
  * Notification Delivered
  * Reply Sent
  * Experiment Viewed
  * Channel Unsubscribed
  *  Session Concluded
  * WZRK Fetch
  * State Transitioned
  * Geocluster Entered
  * Geocluster Exited
  * AB Experiment Rendered
  * AB Experiment Rolled Out
  * AB Experiment Stopped
  * AB Experiment Disqualified
  * Identity Set
  * Identity Error
  * Identity Reset
  * Reachable By
  * Any Event

## Events Excluded from MAU Calculations
The following is the list of events that are excluded from the MAU calculation:
  * Push Impressions
  * Notification Viewed
  * App Uninstalled
  * Notification Sent
  * Stayed
  * Notification Control
  * Notification Delivered
  * Reply Sent
  * Experiment Viewed
  * Channel Unsubscribed
  * Session Concluded
  * WZRK Fetch
  * State Transitioned
  * Geocluster Entered
  * Geocluster Exited
  * AB Experiment Rendered
  * AB Experiment Rolled Out
  * AB Experiment Stopped
  * AB Experiment Disqualified
  * Identity Set
  * Identity Error
  * Identity Reset
  * Reachable By
  * Partner Sync
  * Any Event

# Update Billing Information and Card Details
If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Then, click **Billing **to update the required details.

[block:callout]
{
  "type": "info",
  "title": "Billing Currency",
  "body": "You cannot change the currency for billing."
}
[/block]