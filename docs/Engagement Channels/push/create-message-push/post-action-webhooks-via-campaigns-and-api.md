---
title: Post Action Webhooks
excerpt: Learn how to send campaign data with Post Action Webhooks.
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

You may want exact copies of all messages sent to each user and their message statuses as input to your recommendation engine. A post-action webhook can solve this. It triggers a payload to your specified endpoint after sending a push notification.

# Set Up Post Action Webhooks

You can configure post-action webhooks for push campaigns created via the dashboard or API.

## Push Campaigns via Dashboard

You can enable the post action webhook during campaign creation under the Setup section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae40a27-push_enable_webhook.png",
        "Enable Post Action Webhook",
        820
      ],
      "align": "center",
      "border": true,
      "caption": "Post Action Webhook"
    }
  ]
}
[/block]


After the configuration is enabled, the webhook endpoint is listed in the _Setup_ section. Select the required webhook endpoint from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bcbcffe-push_webhook_select.png",
        "Select or Add a Webhook Endpoint",
        820
      ],
      "align": "center",
      "border": true,
      "caption": "Select the Webhook Endpoint"
    }
  ]
}
[/block]


For more information,  refer to [Webhook Setup](doc:setup-webhooks).

## Push Campaigns via API

For API Push, add the `pa_webhook_name` key in the payload with the name of the webhook connection. For more information, refer to [Create Campaign API - Target User Events & Properties](https://developer.clevertap.com/docs/create-campaign-api-post-action-webhook#create-campaign-api---target-user-events--properties). 

> 📘 Private Beta
> 
> Post-action webhooks in API Push campaigns is currently released in Private Beta. To enable this feature for your account, contact your Customer Success Manager.

# Send Data

Using a _ post action _ webhook, you can stream all the message-level data from a push campaign to your server. Following is the sample payload structure for push data: 

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

The following are the key types in the payload:

| Key          | Type              | Description                                                                                                                                 |
| :----------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| wzrk_cid     | String            | Refers to Channel ID.                                                                                                                       |
| wzrk_bi      | String            | Keys Badge icon in push notifications.                                                                                                      |
| wzrk_bc      | String            | Key refers to badge count.                                                                                                                  |
| wzrk_ttl_s   | Integer           | Time to live in seconds.                                                                                                                    |
| wzrk_ttl     | Integer           | Time to live of notification.                                                                                                               |
| wzrk_acct_id | String            | CleverTap account ID                                                                                                                        |
| wzrk_pn      | N/A               | If present, this notification is sent from CleverTap.                                                                                       |
| wzrk_id      | string            | Open rate tracking ID (can be empty or it may not be present).                                                                              |
| wzrk_bp      | string            | If present, the value will be a URL of an image  displayed in the notification.                                                             |
| wzrk_sound   | boolean or string | If present, it signifies that the default or custom Android notification sound must be played.                                              |
| nt           | string            | Notification Title. If absent or empty falls back to the app name.                                                                          |
| nm           | string            | Notification Body. If absent or empty, ignore this notification.                                                                            |
| wzrk_dl      | string            | If present, this is a deep link that must be followed at the time of notification open.                                                     |
| wzrk_d       | N/A               | If present, ignore this notification.                                                                                                       |
| ico          | string            | If present and not empty, it contains the URL of an image, that must be used as the small notification icon.                                |
| wzrk_pivot   | string            | If present and not empty, it contains the URL of an image. It signifies the type of variant in A/B campaigns.                               |
| wzrk_rnv     | string            | If present and not empty, it will raise Push Impressions event.                                                                             |
| wzrk_nms     | string            | If present and not empty, it contains the summary text to be displayed along with the image.                                                |
| wzrk_st      | string            | If present and not empty, it contains the subtitle text which is displayed next to the App name.                                            |
| wzrk_clr     | string            | If present and not empty, it contains the _Hex_ value of the color to be applied on the small icon (and app name for Android Pie and below) |

The post action webhook can collect data only after the successful delivery of push messages.