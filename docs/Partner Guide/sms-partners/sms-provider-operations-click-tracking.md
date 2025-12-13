---
title: SMS Provider Operations
excerpt: Understand how to edit, archive, and delete providers.
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

This section describes actions for the available SMS service providers.

<Image title="SMS_setup_provider_archive_edit.png" alt={1183} align="center" className="border" border={true} src="https://files.readme.io/936ca90-SMS_setup_provider_archive_edit.png" />

# Operations

The operations for SMS providers are as follows:

## Edit Settings

Edit the SMS settings to change *Provider credentials*.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to *Settings* > *Channels* > *SMS* > Providers\_ tab. 
2. Click the ellipsis next to the provider. 
3. Select *Edit settings* from the list. The *Provider credentials* window displays.
4. Change the required information. 
5. Click **Send Test SMS** to check that the provider is working correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as default so that the same provider appears pre-selected from the dropdown by default in the campaign creation workflow for delivering your SMS

1. Follow the steps to set a default SMS service provider:
2. From the CleverTap dashboard, navigate to *Settings > Channels > SMS > Providers* tab. 
3. Click the ellipsis next to the provider. 
4. Select *Mark as Default* from the list.

## Archive Service Providers

You can archive any current SMS service providers from the SMS settings. Archiving the SMS service provider stops any active *Campaigns* or *Journeys* for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

Follow the steps to archive an SMS service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > SMS > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Archive* from the list.

> 📘 Restoring an Archived Provider
>
> After you archive a service provider, you can not restore it. However, the stats are available for the user to view.

## Delete Service Providers

You can delete any current SMS service providers from the SMS settings. Deleting the SMS service provider will remove all existing data from our system and stop any active *Campaigns* or *Journeys*. The deleted provider will not be available for use in the future.

Follow the steps to delete an SMS service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > SMS > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Delete* from the list.

## View Provider Stats

You can view the detailed actionable stats such as SMS delivered, clicked, and replied from the CleverTap dashboard. To view the provider stats:

1. Navigate to *Settings* > *Channels* > *SMS* from the dashboard.
2. Click the SMS provider name from the *Providers* tab.
3. Navigate to the *Stats* tab. The following *Stats* page opens where you can view the overall stats with different metrics:

<Image align="center" className="border" border={true} src="https://files.readme.io/ba2a6c6-small-Provider_Stats.png" />

* **Total Sent**: Displays the total number of SMS sent from CleverTap.
* **Total Delivered**: Displays the total number of messages sent to the end user. 
* **Total Clicks**: Displays the total number of clicks registered on the shortened link sent via CleverTap in an SMS. 
* **Total Errors**: Displays the total number of system errors encountered when delivering an SMS campaign.
* **Delivery Rate**: Displays the percentage of total SMS sent.

The *Provider Stats* also provides:

* **Delivery Stats** such as:

<Image align="center" className="border" border={true} src="https://files.readme.io/d3f50ea-small-Delivery_Stats.png" />

* *Daily Avg Sent*: Calculated as the total sent SMS divided by the number of days. 

* *Daily Avg Delivery*: Calculated as total delivered SMS divided by the number of days.

* *Clicked*: Displays the number of clicks registered on SMSes when sent using CleverTap link shortening.

* *Errors*: Displays the number of errors for the selected duration.

* **Sends and Errors**: Displays the line graph for the following: *Total Sent*, *Total Errors*, and *Total Clicks*. You can toggle each of these stats to view only the specific stats or view all these stats at once. You can also filter the data for a specific period (for example, daily, weekly, or monthly).

<Image align="center" className="border" border={true} src="https://files.readme.io/3d47f24-small-Sends_and_Errors.png" />

* **Performance**: Displays the campaign performance based on Click Through Rate (CTR) for a specific period (for example, daily, weekly, or monthly).

<Image align="center" className="border" border={true} src="https://files.readme.io/377439e-small-Performance_Stats.png" />

* **Delivery Rate**:  Displays the percentage of total SMS sent for a specific period (for example, daily, weekly, monthly).

<Image align="center" className="border" border={true} src="https://files.readme.io/2928613-small-Delivery_Rate_Stats.png" />

> 📘 SMS Clicks
>
> Total SMS Clicks count is available in SMS only if the URL specified in the message body is shortened using [CleverTap Link Shortening](doc:create-message-sms-click-tracking#click-tracking) feature.
