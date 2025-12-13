---
title: Setup
excerpt: Learn how to set up Amazon Eventbridge to send event data to Amazon service
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Integrate EventBridge with CleverTap

This process involves the following three steps:

1. [Find Amazon EventBridge Event Source Details](doc:setup-amazon-eventbridge#find-amazon-eventbridge-event-source-details).
2. [Configure CleverTap Event Source](doc:setup-amazon-eventbridge#configure-clevertap-event-source).
3. [Associate Event Source with Designated Event Bus in AWS Console](doc:setup-amazon-eventbridge#associate-event-source-with-designated-event-bus-in-aws-console).

## Find Amazon EventBridge Event Source Details

To find the event source details:

1. Navigate to Amazon EventBridge Partners from the Amazon EventBridge dashboard.
2. Click **Set up** under the CleverTap partner listing. The _Set up event source_ page opens.
3. Click **Copy** to copy your AWS account number to your clipboard and save it. You will require these details for configuring the CleverTap dashboard.

## Configure CleverTap Event Source

To configure CleverTap Event Source:

1. Log in to your CleverTap account and navigate to the _Settings_ > _Partners_ page. Select _Amazon Eventbridge_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d68579c40857f395a42742c0aaa22f480b47ea6ff49126bf706c4ef73117f836-Amplitude_Partner_Page.png",
        "",
        "Partners Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Partners Page"
    }
  ]
}
[/block]


2. Enter the following Amazon service details and click **Integrate**:

| <p>Field</p>            | <p>Description</p>                                                                                                                                                                                                                                                                                                     |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Partner Nickname</p> | <p>Enter the <em>Nickname</em> for your integration.</p>                                                                                                                                                                                                                                                               |
| <p>AWS Account ID</p>   | <ul><li>Enter the AWS account number obtained in <em>Step 3</em> of <a href="doc:setup-amazon-eventbridge#find-amazon-eventbridge-event-source-details">Find Amazon EventBridge Event Source Details</a>.</li><li>This user property is used as an identifier when sending event data to Amazon EventBridge.</li></ul> |
| Region                  | The AWS account region. The events are sent to the selected region.                                                                                                                                                                                                                                                    |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/56c40042768e84671c59b240a57f7bc1da2f35682f8635063dbd0e314d62502f-image.png",
        null,
        "Configure Amazon Service Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Amazon Service Details"
    }
  ]
}
[/block]


## Associate Event Source with Designated Event Bus in AWS Console

To establish an event connection to Amazon EventBridge, your CleverTap event source must be associated with the event bus in Amazon EventBridge. You can now see the CleverTap event source, created in _Step 3_ of [Configure CleverTap Event Source](doc:setup-amazon-eventbridge#configure-clevertap-event-source),  
under the _Partner_ events sources on the Amazon EventBridge dashboard. To associate the event source with the designated event bus in the AWS console:

1. Select the event source name and associate it with an event bus. 
2. After establishing the connection, set your rules and targets for Amazon EventBridge to redirect events to an AWS service. For more information, refer to the [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/index.html).