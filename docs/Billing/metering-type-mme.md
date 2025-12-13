---
title: Metering Type - MME
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

The Monthly Million Events (MME) metering is priced at monthly million events. The event data is stored for 12 months. 


# Measurement and Limits
The billable unit for this metering is events. You will get usage alerts on the dashboard and email reminders. 

* Unit of measurement: Events.
* Overage: Charged at 20% extra of the contracted price, that is 1.2X times. For example, if you are charged at 1$/100K events, then overage is charged at 1.2$/100K events.

The event limit is recharged each month. For example, if you have MME metering for one million events, then each month, you will get an additional million events for consumption. 

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

Customer history (previously DRP) or the lookback period allows for a minimum of three months for all metering types. 

Q. What if I have a seasonal spike in MAU?

For Enterprise plans, you can make an annual payment. You may then have the option to average the MAU over the year. It can help smooth over the spike in MAU.