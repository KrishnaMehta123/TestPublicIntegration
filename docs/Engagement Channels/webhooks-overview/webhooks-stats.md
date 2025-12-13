---
title: Webhooks Stats
excerpt: View stats for your webhooks.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View Statistics

You can view the statistics of your webhook from the _Campaign_ list page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3bd12d5-image_1.png",
        "",
        "Analyse Webhook Statistics"
      ],
      "align": "center",
      "border": true,
      "caption": "Analyse Webhook Statistics"
    }
  ]
}
[/block]


- **Webhooks streamed**  - Represents the total webhooks streamed to an endpoint.
- **Message Trend** - Represents performance trend for total webhooks streamed over a specific period of time (for example, daily, weekly, monthly) in a campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/768ebf47071fc82ac232d41b3c6daae1093a870878d8be7d59448d658f283144-Webhooks_Errors.png",
        "",
        "Webhook Streamed Errors"
      ],
      "align": "center",
      "border": true,
      "caption": "Webhook Streamed Errors"
    }
  ]
}
[/block]


- **Errors**: It represents the count and reason for the webhooks that were not exported due to errors.

The following table lists the errors that may occur while delivering the webhook campaign:

[block:parameters]
{
  "data": {
    "h-0": "Error",
    "h-1": "Description",
    "0-0": "Webhook dispatch error",
    "0-1": "This error means that the webhook payload failed to deliver or dispatch to the specified target URL. This error occurs when CleverTap attempts to send the data to the webhook endpoint, but the delivery process encounters an issue, preventing successful transmission. The cause could be various reasons, such as:  \n  \n<ul><li> Server unavailability </li><li> Incorrect URL </li><li> Network connectivity issues </li><li> Problems with the receiving server </li></ul>",
    "1-0": "Invalid Webhook URL",
    "1-1": "The provided URL for the webhook is not valid or properly formatted. When configuring a webhook in CleverTap, you must provide a correct and complete URL specifying the endpoint where the data should be delivered. If the URL is missing essential components, contains errors, or is not in the expected format, CleverTap cannot deliver the webhook payload."
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "left",
    "left"
  ]
}
[/block]