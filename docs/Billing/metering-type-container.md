---
title: Metering Type - Container
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

The Container metering allows for a fixed amount of event storage with unlimited ingestion. The minimum storage duration, also known as Data Retention Policy(DRP), spans three months.  Events can be stored as long as they do not exceed the container limit. 


# Measurement and Limits

You will get usage alerts on the dashboard and through email reminders.  The billable unit of measurement is events. 

* Unit of measurement: Events.

The storage space is available for use till the end of your service agreement with CleverTap and the selected billing cycle.

For example, let's say you opt for a storage plan of 10 million events. If you have consumed 4 million events, then your consumption available for the next billing cycle will be 6 million events. 

If the storage exceeds 10 million events, the account is allowed a grace period of 15 days after which the account is [locked or suspended](https://docs.clevertap.com/docs/metering-type-container#account-lock-and-suspension). You have two options:
* Optimize the storage 
* Buy more storage 

## Optimize Storage

The account administrators receive alerts and emails for optimizing data. You can optimize the storage by reducing the DRP limit. Specify the limit to store data per your business requirements. For more information, see [Set Data Retention Policy](https://docs.clevertap.com/docs/schema#set-data-retention-policy)

## Buy Storage
The account administrators receive alerts and emails for upgrading to higher capacity. Please contact our sales team or email [sales@clevertap.com](mailto:sales@clevertap.com)  to check for your upgrade options. 

# Account Lock and Suspension

A grace period of 15 days is allowed if your event usage reached 100% of the contracted limit. Within this grace period, if the usage limit reaches 110%  or the grace period ends (whichever is earlier), then the dashboard access is restricted. A restricted state means that even though data ingestion will continue, you will not be able to run campaigns, journeys, or queries. You can either [buy more storage](https://docs.clevertap.com/docs/metering-type-container#buy-storage) or [optimize](https://docs.clevertap.com/docs/metering-type-container#optimize-storage) data. 

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