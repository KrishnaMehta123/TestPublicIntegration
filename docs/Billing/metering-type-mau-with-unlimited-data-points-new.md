---
title: Metering Type - MAU with Unlimited Data Points (New)
excerpt: Understand how the MAU with Unlimited Data Points metering works in CleverTap.
deprecated: false
hidden: true
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

This document explains the billing terminologies, calculations, and measurement for the Monthly Active User (MAU)-based metering with Unlimited Data Points in CleverTap. If you have any questions or need further assistance. contact our support team. 

# Billing Terminologies

Familiarizing yourself with the following billing terminologies is crucial to manage and optimize your organization's usage and costs effectively:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Term
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Monthly Active User (MAU)
      </td>

      <td>
        A Monthly Active User (MAU) is an end-user who has recorded one or more events in a calendar month. This includes any unique user action across web, mobile, engagement channels, or through data imported from third-party services or offline uploads.\
        When tracking user activity on mobile apps and websites, a user active on both devices with the same identity token is counted as one MAU. Each organization is charged based on the total number of MAUs across all projects. Users who perform a qualifying event in multiple projects are counted once per project.
      </td>
    </tr>

    <tr>
      <td>
        Anonymous Users
      </td>

      <td>
        An anonymous user is a user who engages with a customer's app or website without logging in.
      </td>
    </tr>

    <tr>
      <td>
        Data Point
      </td>

      <td>
        An event, event property, or profile property update is a data point.
      </td>
    </tr>

    <tr>
      <td>
        Monthly Billable Users
      </td>

      <td>
        The Monthly Billable Users (MBU) is the highest of either of the following:  

         <li>**Actual MAU**: \{[All App, Web, and API users (including anonymous users of App and API)] + (1/3 * Web anonymous users)\}. </li>
         <li>**Contracted MAU tier**: The number of MAUs agreed upon in the contract.</li>
      </td>
    </tr>
  </tbody>
</Table>

## Handling Web Anonymous Users

A Web Anonymous User is a user who engages with the website without logging in. When calculating Monthly Active Users (MAUs) for the website, CleverTap considers one-third of the Web Anonymous Users. 

For example, 300 Web Anonymous Users are counted as one-third of 300 (i.e. 100 MAUs) and 300 Web Identified Users are counted as 300 MAUs.
> 📘 Lookback Period for Web Anonymous Users
>
> Web Anonymous Users have a default three-month Lookback Period, which means their activity is stored in CleverTap server for the past three months.

# Billable Events

The billable system and custom events are calculated as follows:

## System Events

The following is the list of system events included in the MAU calculations:

* App Launched
* Web Session Started
* UTM Visited

The *Partner Sync* system event and its properties are included in the Data Point calculation.

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

> 📘 Note
>
> The system event properties such as *CT App version*, *CT Latitude*, *CT Longitude*, and *CT Source* are not included when calculating data points.

For more information, refer to [Custom Events](doc:events#custom-events).

# Overages Calculation

Overages in CleverTap billing refer to the charges incurred when your usage exceeds the limits included in your subscription plan. The billable unit for calculation is Monthly Billable Users (MBUs). The overages are charged based on the chosen payment plan.

## Monthly Payment

Under the monthly payment plan, if the MBUs exceed the contracted MAU tier for any given month, the additional MAU is charged at 120% of the metering per MAU price. For example, if the metering per MAU price is $0.10 and you exceed 2,000 MAUs, the overage will be calculated as = \[($0.10 \\\* 2,000 \\\* 120%)] =  $240.

## Prepaid Payment (3/6/12 months):

Under this payment plan, the MBUs are measured each month as a rolling average throughout the billing period. This means that even if there is a usage spike during the contract period, you will not be charged for overage if the average consumption remains within the contracted limit. However, if you exceed the contracted MAU limit, you will be charged for the overage at 120% of the metering per MAU price. For example, if the metering per MAU price is $0.08 and you exceed 2,000 MAUs, you will be charged = \[($0.08 \\\* 2,000 \\\* 120%)] = $192.

> 📘 Alerts for Overages
>
> All account admins receive alerts on their CleverTap dashboard and email every time the account consumption reaches 80%, 90%, 100%, 110% of your subscription plan.

# Update Billing Information and Card Details

Organization members with billing permissions (only Admins) can update the billing and payment information by navigating to *Organization* > *Billling* > *Billing details* from the CleverTap dashboard.

> 📘 Changing Billing Currency
>
> The billing currency cannot be changed once set up.