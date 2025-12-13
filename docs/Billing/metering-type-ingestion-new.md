---
title: Metering Type - Ingestion (New)
excerpt: Understand how the Ingestion metering works in CleverTap.
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

The Ingestion metering plan in CleverTap is designed based on the number of data points ingested per month. A Data Point is an event, event property, or profile property update. This document explains the billing calculations and measurement for the Ingetion metering plan. If you have any questions or need further assistance. contact our support team.

# Billable Events

The billable system and custom events are calculated as follows:

## System Events

The following system events and their properties are included in the Data Point calculation:

* Partner Sync
* App Launched
* Web Session Started
* UTM Visited

CleverTap has many more system events, which are not billable and hence excluded in the Data Point calculation. To know about those events, refer to [System Events](https://docs.clevertap.com/docs/events#system-events). 

## Custom Events

All the custom events count towards MAU calculations. However, the following two scenarios arise at the time of Data Points calculation for custom events:

### Scenario 1: All the custom events and their custom properties are included in the Data Point calculation

For example, the custom event *Add to Cart* is triggered when a user adds a product to their shopping cart. You capture the product's name, quantity, and price as properties associated with this event.

In this case, data points are calculated as follows:

**Data Point attributed to the event captured** = 1 data point

**Data Point attributed to the event properties captured** = 3 data points (product name, quantity, and price).

**Total data points for this event** = 1 (event tracking) + 3 (event properties) = 4 data points.

### Scenario 2: System events properties captured along with custom events are not billable and hence not included in the Data Point calculation

In CleverTap, every custom event captures some system event properties to provide additional context or information related to that specific system event.

For example, suppose a custom event called *AppUpdateCompleted* is raised when a user updates the app to a new version. This custom event captures custom event properties such as *UpdateStatus*, *DeviceInformation*, and system event properties such as *CT App version*, *CT Latitude*, *CT Longitude*, and *CT Source*.

In this case, data points are calculated as follows:

**Data Point attributed to the event captured** = 1 data point

**Data Point attributed to the custom event properties captured** = 2 data points (*UpdateStatus* and *DeviceInformation*) 

**Total data points for this event** = 1 (event tracking) + 2 (custom event properties) + 0 (system event properties) = 3 data points.

> 📘 Exclusion of Certain System Event Properties from Billing Calculation
>
> CleverTap calculates data points for both system and custom events. While custom events and their properties are included in data point calculations, the system event properties *CT App Version*, *CT Latitude*, *CT Longitude*, and *CT Source* are included only in system event data point calculations and excluded from custom event data point calculations.

For more information, refer to [Custom Events](https://docs.clevertap.com/docs/events#custom-events).

> 🚧 Data Point Calculation for Messaging Channels
>
> For any messaging channel, CleverTap does not include the following events in the Data Point calculation:
>
> * Notification Sent
> * Notification Delivered
> * Notification Viewed
> * Notification Clicked
> * Push Impressions
>
> This implies that businesses do not incur charges for the number of messages sent, viewed, or clicked when using CleverTap's messaging features. However, certain channels may have distinct billing policies and must be considered separately.

# Overages

Overages in CleverTap billing refer to the charges incurred when your usage exceeds the limits included in your subscription plan. The billable unit for calculation is Data Points per Month. The overages are charged based on the chosen payment plan.

## Monthly Payment

Under the monthly payment plan, if the data points exceed the contracted data points for any given month, the additional data points are charged at 120% of the data points rate. For example, if the data point rate is 1$/100K DPs and your contracted tier limit is 1 million DPs, but your actual usage exceeds by 0.5 million DPs, the overage will be calculated as follows:

**Contracted Tier Limit:** 1 million DPs

**Actual Usage:** 1.5 million DPs

**Charge Rate:** $1 per 100K DPs

**Calculation:** (1 million / 100K) x $1 + (0.5 million / 100K) x $1.2 = $16

## Prepaid Payment (3/6/12 months)

Datapoints are measured monthly as a rolling average for the billing period. This means that if there is a spike in consumption during the contract period but the average consumption is lower, you are not charged for the overage. All additional data points are charged at 120% of the data point rate for the contract tier. For example, if the data point rate is 1$/100K DPs and your contracted tier limit is 1 million DPs per month (for 3 months), but your actual usage exceeds by 1 million DPs, the overage will be calculated as follows:

**Contracted Tier Limit:** 3 million DPs for 3 months

**Usage:**

* **1st Month:** 1 million DPs
* **2nd Month:** 1.4 million DPs
* **3rd Month:** 1.6 million DPs

**Actual Usage:** 4 million DPs

**Charge Rate:** $1 per 100K DPs

**Calculation:** (3 million / 100K) x $1 + (1 million / 100K) x $1.2 = $42

> 📘 Alerts for Overages
>
> All account admins receive alerts on their CleverTap dashboard and email every time the account consumption reaches 80%, 90%, 100%, 110% of your subscription plan.

# Update Billing Information and Card Details

Organization members with billing permissions (only Admins) can update the billing and payment information by navigating to *Organization* > *Billling* > *Billing details* from the CleverTap dashboard.

> 📘 Changing the Billing Currency
>
> The billing currency cannot be changed once set up.
