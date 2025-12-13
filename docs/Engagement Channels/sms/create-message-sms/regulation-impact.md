---
title: Regulation Impact
excerpt: >-
  Learn about the impact of regulations by the Telecom Regulatory Authority of
  India (TRAI). This impact is limited only to Indian users.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

The Telecom Regulatory Authority of India (TRAI) requires distributed ledger technology (DLT) registration for all the service providers for bulk SMS services in India. Starting February 1, 2021, it is mandatory to send messages to customers via a pre-approved template. For more information regarding DLT registration, refer to [SMS Regulations](doc:sms-regulations). 

# What This Means to Our Clients

This requires the following changes from your side when you create an SMS campaign on the CleverTap dashboard. 

> ❗️ Template IDs
>
> A template ID is required for the SMS campaigns targeted to Indian mobile numbers and having MSG-91 as the service provider. A template ID may or may not be required for other service providers. We recommend checking with your service provider.

## Future Campaigns

Future campaigns are the campaigns that have started after February 1, 2021.

When you create campaigns after the mandated date, you must use a pre-approved template. In the campaign setup where you choose a service provider, we now provide an extra field to provide a template ID. 

<Image title="Enter Template ID for Future Campaigns" alt={1702} align="center" border={true} src="https://files.readme.io/a8d7c22-SMS_temp_new.png">
  Template ID
</Image>

This field is optional because it is only required for sending SMS messages to phone numbers in India. Check that you provide a matching template ID every time you create an SMS campaign for customers in India. 

For generic service providers, you can edit the settings to additionally set up a key-value pair as shown below:

* Key: This indicates the name of the key for a template ID your service provider is expecting you to send. In the example shown below 'content\_id' is the name of the key expected by the service provider.
* Value: Specify $$TemplateId. You can enter the value of the template ID at the time of the campaign creation. 

<Image title="Enter Key Value Pair in Header" alt={733} align="center" border={true} src="https://files.readme.io/d89ec0d-Screenshot_2021-01-29_at_3.21.42_PM.png">
  Header
</Image>

For example, if the key name for a template ID is expected as content\_id.

The Template ID that you have to use in the campaign, has to be entered in the *WHAT* section of the campaign. 

<Image title="Enter Template ID in What Section" alt={1720} align="center" border={true} src="https://files.readme.io/577d331-temp_id.png">
  Create Message
</Image>

The value that you will enter here is the one that is being accepted by your service provider for passing the Template ID. The Template ID parameter that you put in the endpoint URL.\
Check with the service provider which key they accept for Template ID and accordingly add that key and then the Template ID value in the message section.

## Current Campaigns

Current campaigns are the campaigns that were started before February 1, 2021. 

### Campaigns

To receive all your running campaigns, perform the following steps:

1. From the dashboard, navigate to *Campaigns*.
2. Select the channel as *SMS* from the filter.
3. Select the status as *Running*, then click **Apply**. 

<Image title="Filter Running Campaigns and Click Apply" alt="Filter Running Campaigns" align="center" border={true} src="https://files.readme.io/8fbcbae634f9a33a521d0fc1b2740863ed7ac3c7f74602fa731343b4ec75526f-1.png">
  Filter Running Campaigns
</Image>

4. Click on the **Subscribe to Reports** link.

<Image title="Click Subscribe to Reports" alt="Subscribe to Reports" align="center" border={true} src="https://files.readme.io/68598cdd1e7cad4cc902ba720f74f58159ad56f38a86bb84dcb3f081df41b60a-2.png">
  Subscribe to Reports
</Image>

5. Once the *Campaign Summary Emails* window displays, enter a report name.
6. Select *Campaign overview*.
7. Click **Send Report**.

<Image title="Set Up Email Subscription and Click Send Report" alt="Set Up for Email Subscription" align="center" border={true} src="https://files.readme.io/35dad38-4_Fill_out_report.png">
  Set Up for Email Subscription
</Image>

You will then receive a report via email with all the running SMS campaigns and their relevant campaign IDs.  

### Journeys

To receive all your running journeys, perform the following steps:

1. From the dashboard, navigate to *Journeys*.
2. Select the status as *Running* from the filter, then click **Apply**. 

<Image title="Select Running to Filter Journeys" alt={460} align="center" width="smart" border={true} src="https://files.readme.io/58cda56-filter_journeys.png">
  Filter Running Journeys
</Image>

3. Select the desired campaign and click the **Email report** link.

<Image title="Select Journeys to Receive Email Reports" alt={2736} align="center" border={true} src="https://files.readme.io/ea0a4d0-email_reports_1.png">
  Select Journeys
</Image>

4. Once the *Email report* window displays, enter a report name.
5. Select *Nodewise* for the report type.
6. Click **Email report**.

<Image title="Select Nodewise and Click Email Report" alt={588} align="center" border={true} src="https://files.readme.io/2a02134-er.png">
  Nodewise Email Report
</Image>

You will then receive a report via email that you can filter by campaign channel as SMS to get a list of all SMS campaigns with their campaign IDs.

### Match IDs

After you have a list of all campaign IDs from the campaign and journey steps above, perform the following steps:

1. Match these IDs to the template IDs from the SMS service provider's dashboard.
2. Send this data to the CleverTap platform in the JSON format/JSON payload and hit our endpoint. 

#### Base URLs

Use the appropriate URL depending on your location:

* For customers on an EU stack: [https://api.clevertap.com/1/update/templateIds.json](https://api.clevertap.com/1/update/templateIds.json) 
* For customers on an IN stack: [https://in1.api.clevertap.com/1/update/templateIds.json](https://in1.api.clevertap.com/1/update/templateIds.json)

#### HTTP POST Method

The X-CleverTap-Account-Id and X-CleverTap-Passcode are used to authenticate the request. Please refer to the [authentication guide](https://developer.clevertap.com/docs/authentication) to view how to get their values.

The following headers are all required:

| Header                 | Description                                             | Type   | Example Value                         |
| :--------------------- | :------------------------------------------------------ | :----- | :------------------------------------ |
| X-CleverTap-Account-Id | Your CleverTap account ID.                              | String | "X-CleverTap-Account-Id: ACCOUNT\_ID" |
| X-CleverTap-Passcode   | Your CleverTap account passcode.                        | String | "X-CleverTap-Passcode: PASSCODE"      |
| Content-Type           | Request content-type is always set to application/JSON. | String | "Content-Type: application/json"      |

The following is a sample JSON:

```json
[
{
"campaign_id" : 1563478922,  // campaign ID
"template_id" : "455633413", // template ID
},
{
"campaign_id" : 1563478922,  
"template _id" : "455633413"
}
]
```

Your CleverTap campaigns will now have the correct template IDs tagged to them.
