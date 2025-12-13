---
title: Metering Type - Ingestion
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
This metering is available only for accounts that require more than 15 million MAU. This type of metering is based on data points ingested per month (not storage.) 

# Billing Terminologies

## Data Point
An event, event property, or profile property update is a data point.
[block:callout]
{
  "type": "info",
  "title": "Excluded Event",
  "body": "The Notification Sent event is excluded from data points calculation."
}
[/block]



#Measurement and Limits

The billable unit for this metering is data points (DP). It is an event, event property, or profile property update. 

  * Unit of measurement: data points/month
  * Overages: The overages are charged based on the mode of payment. 
    * Monthly payment: Charged at 120% of datapoint rate for contracted tier. For example, if you are charged at 1$/100K DPs, then overage is charged at 1.2$/100K DPs.
    * Prepaid payment (3/6/12 months): Datapoints are measured each month as a rolling average for that billing period. It means that if there is a spike in consumption during the contract period, but if the average consumption is lower, then you are not charged for the overage. All additional data points are charged at 120% of the data point rate for the contract tier.


# Additional Charges
A one-time *Data Import* fee of $0.50 cents per million data points (in 1 million datapoint increments) is charged. This fee is charged in the upcoming invoice.

# Account Lock and Suspension

If the usage limit reaches 110%, then the dashboard access is restricted. The restriction means that even though data ingestion will continue, you will not be able to run campaigns, journeys, or queries. You can either upgrade to higher capacity (recommended) or pay for overages for the current month.
The restriction is removed automatically after upgrading the plan, even if the utilization is between 100 and 110%.

# Alerts for Overages
All account admins will receive alert emails when their account exceeds receive alerts on their CT dashboard and email inboxes every time the consumption exceeds 80%, 90%, 100%, 110%, and so on.

# Update Billing Information and Card Details

If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Then, click **Billing **to update the required details.
[block:callout]
{
  "type": "info",
  "title": "Billing Currency",
  "body": "You cannot change the currency for billing."
}
[/block]

# Customer History 
Customer history (previously DRP) or the lookback period is available for three years by default for all accounts (user activity data). The customer history period can be reduced for larger customers but only up to 3 months.