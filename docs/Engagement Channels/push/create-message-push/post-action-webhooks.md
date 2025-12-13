---
title: Post Action Webhooks
excerpt: Learn how to send campaign data with Post Action Webhooks.
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

A *post action* webhook is used to trigger a payload to your specified endpoint after sending a push notification.

# Use Case

You may want exact copies of all messages sent to each user and the message statuses as input to your recommendation engine. This can be solved by using a *post action* webhook.

You can enable the *post action* webhook during campaign creation under the *Setup* section.

<Image title="Enable Post Action Webhook" alt={820} align="center" border={true} src="https://files.readme.io/ae40a27-push_enable_webhook.png">
  Post Action Webhook
</Image>

After the configuration is enabled, the webhook endpoint is listed in the *Setup* section. Select the required webhook endpoint from the list.

<Image title="Select or Add a Webhook Endpoint" alt={820} align="center" border={true} src="https://files.readme.io/bcbcffe-push_webhook_select.png">
  Select the Webhook Endpoint
</Image>

Refer to the [Webhook Setup guide](doc:setup-webhooks) to learn more about Webhook configuration,

# Send Data

You can stream all the message-level data from a push campaign on your server by using a *post action* webhook. 

Following is the sample payload structure for push data: 

```json
{
  "targetId": 1628144342,
  "profiles": [
    {
      "identity": "6425",
      "all_identities": [
        "jane.doe@domain.com",
        "6425"
      ],
      "objectId": "-gdf3d1d914a65406a862bac176fb279f1",
      "payload": {
        "title": "Welcome to Acme!",
        "body": "Click here to register for the next event.",
        "kvs": {
          "wzrk_cid": "ChannelID",
          "wzrk_bi": "2",
          "wzrk_bc": "",
          "wzrk_ttl_s": 86400,
          "wzrk_ttl": 24,
          "wzrk_acct_id": "YOUR_ACCOUNT_ID"
        }
      }
    }
  ]
}
```

Following are the key types in the payload:

| Key            | Type              | Description                                                                                                                                 |
| :------------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| wzrk\_cid      | String            | Refers to Channel ID.                                                                                                                       |
| wzrk\_bi       | String            | Keys Badge icon in push notifications.                                                                                                      |
| wzrk\_bc       | String            | Key refers to badge count.                                                                                                                  |
| wzrk\_ttl\_s   | Integer           | Time to live in seconds.                                                                                                                    |
| wzrk\_ttl      | Integer           | Time to live of notification.                                                                                                               |
| wzrk\_acct\_id | String            | CleverTap account ID                                                                                                                        |
| wzrk\_pn       | N/A               | If present, this notification is sent from CleverTap.                                                                                       |
| wzrk\_id       | string            | Open rate tracking ID (can be empty or it may not be present).                                                                              |
| wzrk\_bp       | string            | If present, the value will be a URL of an image  displayed in the notification.                                                             |
| wzrk\_sound    | boolean or string | If present, it signifies that the default or custom Android notification sound must be played.                                              |
| nt             | string            | Notification Title. If absent or empty falls back to the app name.                                                                          |
| nm             | string            | Notification Body. If absent or empty, ignore this notification.                                                                            |
| wzrk\_dl       | string            | If present, this is a deep link that must be followed at the time of notification open.                                                     |
| wzrk\_d        | N/A               | If present, ignore this notification.                                                                                                       |
| ico            | string            | If present and not empty, it contains the URL of an image, that must be used as the small notification icon.                                |
| wzrk\_pivot    | string            | If present and not empty, it contains the URL of an image. It signifies the type of variant in A/B campaigns.                               |
| wzrk\_rnv      | string            | If present and not empty, it will raise Push Impressions event.                                                                             |
| wzrk\_nms      | string            | If present and not empty, it contains the summary text to be displayed along with the image.                                                |
| wzrk\_st       | string            | If present and not empty, it contains the subtitle text which is displayed next to the App name.                                            |
| wzrk\_clr      | string            | If present and not empty, it contains the *Hex* value of the color to be applied on the small icon (and app name for Android Pie and below) |

The post action webhook can collect data only after the successful delivery of push messages.
