---
title: Metering Type - MTU
excerpt: Learn about the metering based on monthly transacting users (MTU).
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
This document provides information about billing terminologies and calculations for MAU-based metering. The MTU metering plan is available in tiers of 100K events. For example, 100K or 200K. 

#Monthly Active User (MAU)
An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user active on both devices with the same identity token will be counted as one MAU.
An organization is charged based on the total number of MAUs across all projects, which means that if a user performs a qualifying event in multiple projects, they are counted once per project.

#Measurement and Limits
The MAU metering is based on a Fair Usage Policy of 50 Events/MAU. You are charged based on Monthly Active Users(MAU) or Monthly Transacting Users (MTU). The MAU counts are derived based on the number of events generated in one month divided by 50. 

* Unit of measurement: Events.
* Overage: Charged at 20% extra of the contracted price, that is 1.2X times. For example, if you are charged at 1$/100K MAU, then overage is charged at 1.2$/100K MAU.  

# Account Lock and Suspension

If the usage limit reaches 110%, then the dashboard access is locked. The restriction means that even though data ingestion will continue, you will not be able to run campaigns, journeys, or queries. You can either upgrade to higher capacity (recommended) or pay for overages for the current month.

The restriction is removed automatically after upgrading the plan, even if the utilization is between 100 and 110%.

# Alerts for Overages
All account admins will receive alert emails when their account exceeds receive alerts on their CT dashboard and email inboxes every time the consumption exceeds 80%, 90%, 100%, 110%, and so on.

# Update Billing Information and Card Details

If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Click **Billing **to update the required details.

[block:callout]
{
  "type": "info",
  "title": "Billing Currency",
  "body": "You cannot change the currency for billing."
}
[/block]

# Customer History
Customer history (previously DRP) or the lookback period is available for three months by default for all accounts (user activity data).