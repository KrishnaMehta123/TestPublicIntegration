---
title: Twilio
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

Twilio is a leading communication platform that empowers businesses to connect with their users through various channels, including SMS. This document highlights the integration of CleverTap and Twilio, empowering businesses to elevate their SMS communication using Twilio's infrastructure. 

# Prerequisites for Integration

Before you begin with integration, ensure you have:

- A Twilio account with SMS permissions
- A CleverTap account with SMS setup enabled

# Twilio Setup

This process involves the following three significant steps:

1. [Find Twilio Details](doc:twilio#find-twilio-details)
2. [Add Twilio Details on CleverTap Dashboard](doc:twilio#add-twilio-details-on-clevertap-dashboard)
3. [Send a Test SMS](doc:twilio#send-a-test-sms)

## Find Twilio Details

CleverTap recommends keeping the Twilio account handy before configuring it on the CleverTap dashboard. To locate these details, navigate to the _Console_ page from the Twilio dashboard:

- Account SID
- Auth Token
- My Twilio phone number

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4ef390-Twilio_Account_Details.png",
        "",
        "Twilio Account Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Account Details"
    }
  ]
}
[/block]


## Add Twilio Details on CleverTap Dashboard

To add Twilio details on the CleverTap dashboard:

1. From the CleverTap Dashboard, navigate to  _Settings_ > _Channels_ > _SMS_.
2. Click **+Add Provider**. The _Add SMS provider_ page opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd87beb-SMS_Add_Provider.png",
        "",
        "Add SMS Provider"
      ],
      "align": "center",
      "border": true,
      "caption": "Add SMS Provider"
    }
  ]
}
[/block]


3. Under _Setup_, enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "_Nickname_",
    "0-1": "Uniquely identifies the provider.",
    "1-0": "_Account SID_",
    "1-1": "Enter your account identifier from the Twilio dashboard. This is a unique key to distinguish a specific Twilio parent account or subaccount.  For more information, refer to [Twilio Account SID](https://support.twilio.com/hc/en-us/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).",
    "2-0": "_Auth token_",
    "2-1": "Enter the Auth Token (Password) obtained from the Twilio dashboard. For more information, refer to [Auth Token](https://support.twilio.com/hc/en-us/articles/223136027-Auth-Tokens-and-How-to-Change-Them).",
    "3-0": "_Callback URL_",
    "3-1": "Enter the URL where delivery or error callbacks must be posted after sending the SMS. By default, CleverTap's callback URL will be pre-populated. If you wish to send the callbacks to a custom URL instead, you can also set it here. For more information on setting a custom callback URL, refer to [Custom callback URL](doc:twilio#custom-callback-url).  \n  \n**Note**: This feature is currently in Public Beta.",
    "4-0": "_Restore_",
    "4-1": "Click _Restore_ to reinstate CleverTap's callback URL. This will remove any custom callback URLs.",
    "5-0": "_From Number_",
    "5-1": "Enter phone numbers obtained under the Twilio console → _Manage-numbers_ → _Active number_ section.",
    "6-0": "_Service SID (Copilot)_",
    "6-1": "Enter Service SID details obtained from the Twilio dashboard. The Copilot Service SID, a Twilio identifier, streamlines message management. It automates number selection and formatting, enhancing engagement by optimizing message delivery based on location and carrier requirements.",
    "7-0": "_Template ID_",
    "7-1": "It is a unique template ID for each SMS template that you want to use. Selecting this option will make it mandatory to input the template ID when saving the provider.",
    "8-0": "_Mark as default_",
    "8-1": "Select _Mark this as default_ to make this SMS provider the default provider to send the SMS."
  },
  "cols": 2,
  "rows": 9,
  "align": [
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd8bd05845c1a4e832ccc1ae84a5149131c03e448940d4bf5bfffbf6b7d771e5-image_44.png",
        "",
        "Add SMS provider as Twilio"
      ],
      "align": "center",
      "border": true,
      "caption": "Add SMS provider as Twilio"
    }
  ]
}
[/block]


4. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful, send a test SMS as follows:

1. Click the _Send Test SMS_ hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   - _Country Code _ and _ Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   - _Message_: This is a test message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02ee2f3-Send_a_Test_SMS_.png",
        "",
        "Send a Test SMS"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Send a Test SMS"
    }
  ]
}
[/block]


> 🚧 Twilio Trial Account
> 
> With a Twilio trial account, you can only send SMS campaigns only to numbers registered on the Twilio dashboard.

> 📘 Encoding
> 
> The messages sent out from CleverTap are encoded in the UTF-8 charset.

# Twilio Callbacks

> 📘 Public Beta
> 
> Currently, this feature is in Public Beta.

The Twilio callback functionality enhances the tracking of SMS interactions originating from the CleverTap dashboard. Twilio's webhooks allow your Twilio phone number to receive incoming text messages. Within CleverTap's setup, the Callback URL is seamlessly generated and prefilled in the provider configuration under _Settings_ > _Channels_ > _SMS_ > _+Provider_. Users can replace this URL with their own, which must be configured on our end to receive callbacks. 

The callback mechanism between Twilio and CleverTap is designed to facilitate communication regarding SMS status updates. The Clevertap callback URL tracks for Delivered (SMS delivered to the user), Failed (SMS delivery error), and Replied (user response to SMS) events from Twilio.

## Delivery Callback URL

CleverTap manages delivery callbacks automatically when sending messages through Twilio. No manual setup is required—CleverTap will automatically receive delivery and status updates.

1. Navigate to _Settings > Channels > SMS_ in the CleverTap Dashboard and select **Twilio** from the provider list.  
2. The Inbound Message Callback URL field is preconfigured and non-editable, ensuring that CleverTap receives delivery and status updates automatically.  

If needed, you can configure delivery callbacks manually in your Twilio account by setting up a webhook, but this is not required for CleverTap to receive status updates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf4f66d762379716b70e22d4bfe3f328c7c67bd74c6dbb34cce0de74848aa13b-image_45.png",
        "",
        "Delivery Callback URL - Twilio"
      ],
      "align": "center",
      "border": true,
      "caption": "Delivery Callback URL - Twilio"
    }
  ]
}
[/block]


## Incoming Message Callback URL

To configure the Incoming Message Callback URL for Twilio SMS in CleverTap, follow these steps on the CleverTap Dashboard:

1. Navigate to _Settings > Channels > SMS > _ select Twilio provider from the provider list on the CleverTap Dashboard. 

2. The Callback URL field will display a pre-filled, non-editable URL generated by CleverTap. This URL is essential for receiving incoming messages. Copy this URL.

On the the Twilio dahsboard:

1. Navigate to _Messaging > Services_ and select the messaging service you intend to use. 

   [block:image]{"images":[{"image":["https://files.readme.io/9c73e69b6b110bcf1fa75303cdbb8290b64c995fa94fdfbaf6c11d6d695b949b-image_40.png","","Messaging Services - Twilio"],"align":"center","border":true,"caption":"Messaging Services - Twilio"}]}[/block]

2. To set up incoming message callback URL, go to the **Integration** tab and under _Incoming Messages_, select _Send a webhook_ > _Request URL _ field enter the Callback URL provided by CleverTap into this field. 

   [block:image]{"images":[{"image":["https://files.readme.io/e942ad9917d2035a0458ff4a6db55ce9ae44b3e75023624d292e758c1bafb5de-image_45.png","","Incoming Messages - Twilio"],"align":"center","border":true,"caption":"Incoming Messages - Twilio"}]}[/block]

3. Ensure the **HTTP Method** is set to **POST**.

4. Click **Save** to apply the changes.

By completing these configurations, Twilio will forward incoming SMS messages and delivery statuses to CleverTap, enabling seamless message tracking and response handling within the CleverTap platform.

## Error Codes

If there is an error in the SMS delivery, these error codes indicate the nature of an error encountered. Each error code corresponds to a specific error description. The error descriptions are displayed within the _Errors_ tab in the campaign stats section in case of delivery-related failures. The following table provides information about the acceptable error codes:

| Error Codes | Error Description                   | Details                                                                                                                                                                                                                                               |
| :---------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 30001       | Queue overflow                      | Indicates that the rate limit was exceeded for sending messages, causing the queue to overflow. To resolve this issue, please wait a while before sending your message again.                                                                         |
| 30002       | Account suspended                   | Indicates that the account was temporarily suspended between sending the message and its delivery. Kindly get in touch with Twilio for further assistance.                                                                                            |
| 30003       | Unreachable destination handset     | Indicates that the recipient's mobile device is either turned off or presently not reachable.                                                                                                                                                         |
| 30004       | Message blocked                     | Indicates that the recipient's number you are attempting to contact is blocked from receiving this message, possibly due to being blacklisted.                                                                                                        |
| 30005       | Unknown destination handset         | Indicates that the attempt to reach the specified number encounters an unfamiliar recipient, which may suggest an invalid or non-existent contact.                                                                                                    |
| 30006       | Landline or unreachable carrier     | Indicates that the destination number is unable to receive this message. This can arise when contacting a landline or encountering an unreachable carrier, particularly with shortcodes.                                                              |
| 30007       | Carrier violation                   | Indicates that the carrier has detected the message content as objectionable, prompting the activation of content or spam filtering to safeguard their subscribers. For a deeper understanding of carrier filtering, consult supplementary resources. |
| 30008       | Unknown error                       | This error does not conform to any predefined categories mentioned above.                                                                                                                                                                             |
| 30009       | Missing segment                     | Indicates that one or more segments associated with your multipart inbound message were not received.                                                                                                                                                 |
| 30010       | Message price exceeds the max price | Indicates that the cost of the message surpasses the maximum price parameter set.                                                                                                                                                                     |
| 21614       | Invalid Mobile Number               | Indicates that the user's number is not valid.                                                                                                                                                                                                        |
| 21610       | Unsubscribed recipient              | Indicates that the individual you are attempting to message has chosen not to receive messages from your Twilio phone number, Channels sender, or Messaging Service.                                                                                  |

### Sample Payload

The following is a sample error payload:

```
curl --location 'https://sk1.cb.wzrkt.com/sms/twilio?account=YOUR_ACCOUNT_ID&meta=000000000.1200000000.1691686363.20230810.0.wzrk_default.-4930006' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'ErrorCode=30005' \
--data-urlencode 'SmsSid=SMXXXXXXXXXXXXXXXXXXXXXXX' \
--data-urlencode 'SmsStatus=failed' \
--data-urlencode 'MessageStatus=failed' \
--data-urlencode 'To=000000000000' \
--data-urlencode 'MessagingServiceSid=MGXXXXXXXXXXXX' \
--data-urlencode 'MessageSid=SMXXXXXXXXXXXXXXX' \
--data-urlencode 'AccountSid=AAAAAAA000000' \
--data-urlencode 'From=0000000000' \
--data-urlencode 'ApiVersion=2010-04-0'
```

# Stats

CleverTap displays comprehensive stats such as Errors, Delivered, Clicked, and CTRs upon receiving callbacks from Twilio. After setting up the provider on the CleverTap dashboard, you can view these statistics from the following pages on the CleverTap dashboard:

- _Stats_ tab of the Campaigns. For more information, refer to [SMS Stats](doc:sms-stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/907e612-Twilio_Campaign_Stats.png",
        "",
        "Twilio Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Campaign Stats"
    }
  ]
}
[/block]


> 📘 Note
> 
> The stats for _Clicked_ event is available only if you use CleverTap's [Click Tracking](<>) feature.

- _Stats_ tab under _Provider_ setup. For more information, refer to the [Provider Stats](https://docs.clevertap.com/docs/sms-provider-operations#view-provider-stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37199a0-SMS_Provider_Stats.png",
        "",
        "Twilio Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Provider Stats"
    }
  ]
}
[/block]


You can also analyze the _Notification Delivered_ and _Notification Replied_ events by navigating to the _Analytics_ > _Events_ page, as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb5134e-image.png",
        null,
        "Analyze Notification Delivered"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Analyze Notification Delivered"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50e5a6f-2023-09-13_17-36-47_1.gif",
        null,
        "Analyze Incoming Text"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Analyze Notification Replied"
    }
  ]
}
[/block]