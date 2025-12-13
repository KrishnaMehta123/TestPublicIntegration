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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a8d7c22-SMS_temp_new.png",
        "Enter Template ID for Future Campaigns",
        1702
      ],
      "align": "center",
      "border": true,
      "caption": "Template ID"
    }
  ]
}
[/block]


This field is optional because it is only required for sending SMS messages to phone numbers in India. Check that you provide a matching template ID every time you create an SMS campaign for customers in India. 

For generic service providers, you can edit the settings to additionally set up a key-value pair as shown below:

- Key: This indicates the name of the key for a template ID your service provider is expecting you to send. In the example shown below 'content_id' is the name of the key expected by the service provider.
- Value: Specify $$TemplateId. You can enter the value of the template ID at the time of the campaign creation. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d89ec0d-Screenshot_2021-01-29_at_3.21.42_PM.png",
        "Enter Key Value Pair in Header",
        733
      ],
      "align": "center",
      "border": true,
      "caption": "Header"
    }
  ]
}
[/block]


For example, if the key name for a template ID is expected as content_id.

The Template ID that you have to use in the campaign, has to be entered in the _WHAT_ section of the campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/577d331-temp_id.png",
        "Enter Template ID in What Section",
        1720
      ],
      "align": "center",
      "border": true,
      "caption": "Create Message"
    }
  ]
}
[/block]


The value that you will enter here is the one that is being accepted by your service provider for passing the Template ID. The Template ID parameter that you put in the endpoint URL.  
Check with the service provider which key they accept for Template ID and accordingly add that key and then the Template ID value in the message section.

## Current Campaigns

Current campaigns are the campaigns that were started before February 1, 2021. 

### Campaigns

To receive all your running campaigns, perform the following steps:

1. From the dashboard, navigate to _Campaigns_.
2. Select the channel as _SMS_ from the filter.
3. Select the status as _Running_, then click **Apply**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8fbcbae634f9a33a521d0fc1b2740863ed7ac3c7f74602fa731343b4ec75526f-1.png",
        "Filter Running Campaigns and Click Apply",
        "Filter Running Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Running Campaigns"
    }
  ]
}
[/block]


4. Click on the **Subscribe to Reports** link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68598cdd1e7cad4cc902ba720f74f58159ad56f38a86bb84dcb3f081df41b60a-2.png",
        "Click Subscribe to Reports",
        "Subscribe to Reports"
      ],
      "align": "center",
      "border": true,
      "caption": "Subscribe to Reports"
    }
  ]
}
[/block]


5. Once the _Campaign Summary Emails_ window displays, enter a report name.
6. Select _Campaign overview_.
7. Click **Send Report**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35dad38-4_Fill_out_report.png",
        "Set Up Email Subscription and Click Send Report",
        "Set Up for Email Subscription"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up for Email Subscription"
    }
  ]
}
[/block]


You will then receive a report via email with all the running SMS campaigns and their relevant campaign IDs.  

### Journeys

To receive all your running journeys, perform the following steps:

1. From the dashboard, navigate to _Journeys_.
2. Select the status as _Running_ from the filter, then click **Apply**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/58cda56-filter_journeys.png",
        "Select Running to Filter Journeys",
        460
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Filter Running Journeys"
    }
  ]
}
[/block]


3. Select the desired campaign and click the **Email report** link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea0a4d0-email_reports_1.png",
        "Select Journeys to Receive Email Reports",
        2736
      ],
      "align": "center",
      "border": true,
      "caption": "Select Journeys"
    }
  ]
}
[/block]


4. Once the _Email report_ window displays, enter a report name.
5. Select _Nodewise_ for the report type.
6. Click **Email report**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a02134-er.png",
        "Select Nodewise and Click Email Report",
        588
      ],
      "align": "center",
      "border": true,
      "caption": "Nodewise Email Report"
    }
  ]
}
[/block]


You will then receive a report via email that you can filter by campaign channel as SMS to get a list of all SMS campaigns with their campaign IDs.

### Match IDs

After you have a list of all campaign IDs from the campaign and journey steps above, perform the following steps:

1. Match these IDs to the template IDs from the SMS service provider's dashboard.
2. Send this data to the CleverTap platform in the JSON format/JSON payload and hit our endpoint. 

#### Base URLs

Use the appropriate URL depending on your location:

- For customers on an EU stack: <https://api.clevertap.com/1/update/templateIds.json> 
- For customers on an IN stack: <https://in1.api.clevertap.com/1/update/templateIds.json>

#### HTTP POST Method

The X-CleverTap-Account-Id and X-CleverTap-Passcode are used to authenticate the request. Please refer to the [authentication guide](https://developer.clevertap.com/docs/authentication) to view how to get their values.

The following headers are all required:

| Header                 | Description                                             | Type   | Example Value                        |
| :--------------------- | :------------------------------------------------------ | :----- | :----------------------------------- |
| X-CleverTap-Account-Id | Your CleverTap account ID.                              | String | "X-CleverTap-Account-Id: ACCOUNT_ID" |
| X-CleverTap-Passcode   | Your CleverTap account passcode.                        | String | "X-CleverTap-Passcode: PASSCODE"     |
| Content-Type           | Request content-type is always set to application/JSON. | String | "Content-Type: application/json"     |

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