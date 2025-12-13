---
title: Email Provider Operations
excerpt: Understanding Email Provider Stats and Key Metrics
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

This section describes actions for the available email service providers.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1cfc01dc329a46ceff3f4e3e4946e06045baa444afb2632bcf3494ae2e28a1ae-providers.png",
        "",
        "Email Service Providers"
      ],
      "align": "center",
      "border": true,
      "caption": "Email Service Providers"
    }
  ]
}
[/block]


# Operations

You can perform the following operations on any email service provider:

## Edit Settings

Edit the email settings to change _Provider credentials_.

To edit the provider settings:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/ecfbe56-Ellipses_icon.png) icon next to the provider. 
3. Select _Edit settings_ from the list. The _Provider credentials_ window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider is working correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as the default so that the same provider is used to deliver your emails. To set up a default email service provider:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/9c12d50-Ellipses_icon.png) icon next to the provider.
3. Select _Mark as Default_ from the list.

## Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active _Campaigns_ or _Journeys_ for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

To archive an email service provider:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/690a04c-Ellipses_icon.png) icon next to the provider. 
3. Select _Archive_ from the list. 

## Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting a provider will remove all existing data from our system and stop any active _Campaigns_ or _Journeys_. The deleted provider will not be available for use in the future.

To delete an email service provider

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/0f986d4-Ellipses_icon.png) icon next to the provider. 
3. Select _Delete_ from the list. 

# View Provider Stats

You can view the detailed actionable stats such as Email Sent, Delivered, Delivery Rate, Open, and Open Rate from the CleverTap dashboard. To view the provider stats:

1. Navigate to _Settings_ > _Channels_ > _Email_ from the dashboard.
2. Click the Email provider name from the _Providers_ tab.
3. Navigate to the _Stats_ tab. The following _Stats_ page opens where you can view the overall stats with different metrics:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cb5d783abd1ae37121e3322ef1696a9fa12499117323c391d0a7a78fd525e32f-image_33.png",
        "",
        "Provider Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Provider Stats"
    }
  ]
}
[/block]


- **Sent**: Displays the total number of emails sent from CleverTap. This count excludes the count for CC Sent and BCC Sent. 
- **Delivered**: Raised when the email campaign is delivered to the end user. The percentage is calculated as `[(Delivered / Sent)*100]`. 

> 📘 Private Beta
> 
> Delivered is currently released in Private Beta for Infobip (in the case of Advanced Email add-on) and SendGrid email providers. Contact your Customer Success Manager for access.

- **Viewed**: Raised when the user opens the email campaign.
- **Clicked**: Raised when the user clicks on the email campaign.
- **Open Rate**: Displays the open percentage for your message. It is calculated as `[(Viewed /Delivered)* 100]`. In case the Delivered count is zero, the open rate will be calculated as `[(Viewed /Sent)* 100]`.
- **Delivery Rate**: Displays the percentage of emails successfully delivered to the recipient. It is calculated as `[(Delivered/Sent)*100.]` 
- The _Provider Stats_ also displays the following stats for the selected time period:  

| **Metric**           | **Description**                                                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Daily Avg Sent**   | The average number of emails sent per day, calculated by `(Total Emails Sent / Number of Days the Campaign is Active)`          |
| **Daily Avg Viewed** | The average number of emails viewed per day. It is calculated as: `(Total views / Number of Days)` in the selected time period. |
| **Total Clicked**    | Displays the total number of clicks registered, including multiple clicks by the same recipient.                                |
| **Unsubscribed**     | Displays the total number of users who unsubscribed from the email campaign.                                                    |
| **Spam Reports**     | Displays the total number of emails marked as spam by recipients.                                                               |
| **Total Delivered**  | Displays the total number of emails successfully delivered to recipients’ inboxes.                                              |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bec34f21c98de67318daed4b7a508e5f4b1bd6059f46a6a4420855d98421f350-Screenshot_2025-01-06_at_15.41.53.png",
        "",
        "Email Delivery Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Email Delivery Stats"
    }
  ]
}
[/block]


- **Performance Stats**: Displays the campaign performance based on Click Through Rate (CTR) and Average Open Rate for a specific period.  
  - Average CTR: Total number of link clicks and an average percentage of email views where at least one link was clicked during the selected time period, calculated as `[(Total Clicked/Total Viewed) * 100]`. 
  - Average Open Rate:  Total number of delivered emails opened and the percentage of delivered emails that were opened during the selected time period, calculated as `[(Total Viewed/Total Delivered) * 100]`. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1cc4516c56c9f815d28950303fffec78e86d16e1a99cf9504033459d645a2808-Screenshot_2025-01-06_at_15.42.04.png",
        "",
        "Performance Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Performance Stats"
    }
  ]
}
[/block]


- **Deliverability Stats**: Visualizes campaign deliverability trends, comparing key metrics—such as Delivered, Opened, and Spam Reports—over a defined period. These metrics provide insights into user engagement, content effectiveness, and potential issues affecting deliverability.
  - Delivered Vs. Opened:  
    A high open rate indicates strong engagement, while a low open rate may point to issues such as poor subject lines, timing, or sender reputation.  
  - Delivered Vs. Spam Reports:  
    An increase in spam reports indicates problems with content, frequency, or targeting and can harm deliverability.  
  - Opened Vs. Spam Reports:  
    Few spam reports with many opens show effective content. Rising spam reports, even with opens, may indicate misleading or irrelevant content. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de87328747db1934cbfb8272a6de735e28debe1d39bde961284f5f16ca9cf736-Screenshot_2025-01-06_at_15.42.16.png",
        "",
        "Deliverability Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Deliverability Stats"
    }
  ]
}
[/block]