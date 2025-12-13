---
title: Generic SMS
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

CleverTap supports any SMS provider via an HTTP integration, provided they support receiving messages via the HTTP protocol. In addition to this, CleverTap Generic SMS integration also supports [setting up callbacks](doc:generic-sms#configure-sms-callback) that help track detailed reports of every SMS being sent from the CleverTap dashboard like Clicked, Delivered, Replied, and Delivery-related errors.

# Integrate an SMS Provider

To integrate an SMS provider, perform the following steps:

1. In the CleverTap dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _SMS_.
2. Click **+ Add Provider**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/256e8bc0168c51fb77aac6018c4ff43f10eeed88022971a14da1a3b61dfefdde-image.png",
        null,
        "Add Provider"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Provider"
    }
  ]
}
[/block]


3. Under _Provider_, select _Other (Generic)_ and enter the following details:  

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Nickname",
    "0-1": "Uniquely identifies the provider",
    "1-0": "Callback URL",
    "1-1": "The delivery callback data for SMS campaigns are received on this URL. Customers must configure this URL in their SMS Provider Settings. For more information, refer to [SMS Callbacks](doc:generic-sms#sms-callbacks).",
    "2-0": "Request Type",
    "2-1": "Select the GET or POST option depending on which HTTP protocol your SMS provider supports, then enter the HTTP API endpoint of the provider. For a POST request under _Parameters_, select your request type in: <li> _Key-value pair_: Enter .your keys and values. </li>  <li>_JSON_: Enter your entire JSON payload structure. If the service provider supports batching, you can enable batching by specifying the key name and the number of records per batch.</li>",
    "3-0": "HTTP Endpoint",
    "3-1": "Enter the API endpoint of the provider.",
    "4-0": "Authentication",
    "4-1": "Under _Authentication_, select one of the following options: <li> No Authentication </li> <li> Basic Authentication: Enter the username and password. </li> <li> Auth 2.0: Enter client URL, client ID, secret key, and key-value pairs (optional). </li>",
    "5-0": "Headers",
    "5-1": "Select _Headers_ to pass along any HTTP headers which will be added to the HTTP request sent to the API endpoint."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


> 📘 OAuth 2.0 Authentication
> 
> In case of failure to authenticate the OAuth 2.0 credentials due to invalid or expired credentials, the CleverTap system will retry after every 120 seconds. All SMSs will fall under Dispatch Error until we successfully validate the credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6435fb-2_Under_Authentication.png",
        "2 Under Authentication.png",
        "Authentication Parameter for type Auth 2.0"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Authentication Parameter for type Auth 2.0"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23dd8e3-under_Parameters.png",
        "under_Parameters.png",
        "Parameters under POST Request Type"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Parameters under POST Request Type"
    }
  ]
}
[/block]


> 📘 Single Batch Limit
> 
> A single batch can have a maximum of 1,000 records.

# Set Up Your Message Payload

To determine the parameters your SMS provider supports, you can ask for a curl request from your SMS service provider or check the payload structure defined in the provider documentation. 

To set up your message payload, perform the following steps:

1. In the CleverTap dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _SMS_.
2. Click on the **+ Add Provider** button.
3. Under _Provider_, select _Other (Generic)_.
4. If the provider specifies all information, such as a phone number, a message body, or a template, should be passed under _Headers_, then under _Headers_, enter key and value pairs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/67d5387-Screen_Shot_2018-08-30_at_4.14.49_PM.png",
        "Screen Shot 2018-08-30 at 4.14.49 PM.png",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


4. If the provider specifies all information, such as a phone number, a message body, or a template, should be passed under _Body_, then under _Parameters_, select the supported encoding:
   - x-www-form-urlencoded: Within this format, all values are passed as key-value pairs, which are used when creating campaigns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd4a734-Screenshot_2021-05-12_at_4.26.41_PM.png",
        "Screenshot 2021-05-12 at 4.26.41 PM.png",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- JSON: Within this format, the exact payload is defined in a JSON structure. This is used to define the payload structure for all outgoing requests of this particular provider.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4039cdc-JSON_Payload_Structure_for_Outgoing_Requests.png",
        null,
        "JSON Payload Structure for Outgoing Requests"
      ],
      "align": "center",
      "border": true,
      "caption": "JSON Payload Structure for Outgoing Requests"
    }
  ]
}
[/block]


## System Dynamic Replacements

You can use the following five dynamic replacements within the key-value pairs in the headers or parameters tabs:

- $$To: A mandatory replacement value used to signify the key where the phone number is added to the payload.
- $$Body: An optional replacement value used to signify the key where the body of the message is added to the payload. Every configuration needs to have $$Body or $$TemplateID key as a mandatory replacement.
- $$TemplateID: An optional replacement value used to signify the key where the TemplateID of the message is added to the payload. Every configuration needs to have $$TemplateID or $$Body key as a mandatory replacement. This variable is optional and only applicable for campaigns targeted to **Indian mobile numbers**. Refer to the [Regulation Impact](https://docs.clevertap.com/docs/regulation-impact#section-future-campaigns) guide to learn more.
- $$TemplateVariables: An optional replacement value used to signify the key where the template variables of the message are added to the payload. 
- $$CampaignID: An optional replacement value used to signify the key where the CleverTap campaign ID is added to the payload.
- $$MessageID: A dynamic replacement parameter replaced by CleverTap with a specific value in the outgoing SMS payload to the provider's endpoint. The provider must send the same value in the [callback](doc:generic-sms#configure-sms-callback) request to CleverTap's callback URL in the meta key. This is mandatory in case of DLR (clicks, delivered, replied, and delivery-related errors) tracking.

## Custom Dynamic Replacements

In addition to system dynamic replacements, any configuration can have a custom dynamic replacement which is available on the campaign creation flow as a mandatory input. 

The following is an example of a configuration to better understand the setup:

```json
{
  "hid": "$$hid", //Global Key-Value pair
  "tid": "$$TemplateID",
  "cid": "$$CampaignID",
  "type": "template",
  "msgs": [
    {
      "seq": 1,
      "to": "$$To",
      "mid": "$$MessageID", //to be added for configuring callbacks
      "uid": "$$uid", //Message Body Key-Value pair
      "variables": "$$TemplateVariables",
      "enc": "utf8"
    }
  ]
}
```

The entire payload has two parts:

1. Message Body Key-Value Pairs: The keys are `seq`, `to`, `uid`, `variables`, and `enc`.
2. Global Key-Value Pairs: The keys are `hid`, `tid`, `cid`, and `type`.

In this configuration, a single msg record will be set up in the key `msgs` and all the message body key-value pairs are used with a user-level personalization. On the other hand, $$hid is a custom dynamic replacement that cannot be personalized on a user level, but the value can be set for each campaign.

Here is another example without batching:

```json
{
  "hid": "$$hid",//Message Body Key-Value pair
  "tid": "$$TemplateID",
  "cid": "$$CampaignID",
  "type": "template",
  "seq": 1,
  "to": "$$To",
  "mid": "$$MessageID", //to be added for configuring callbacks
  "uid": "$$uid",//Message Body Key-Value pair
  "variables": "$$TemplateVariables",
  "enc": "utf8"
}
```

In the example above, there is no bifurcation of the payload. Global and message key-value pairs are on the same level, and therefore, no batching is possible as each record will ping the provider individually. All dynamic replacements would be available for user-level personalization.

> 📘 Encoding
> 
> The messages sent out from CleverTap are encoded in the UTF-8 charset.

# SMS Callbacks

SMS callbacks help you track detailed reports of every SMS being sent from the CleverTap dashboard. All this information is received on the Callback URL present under the Provider _Setup_ tab on the CleverTap dashboard. For now, this feature is available only for Generic SMS Integration. If you already have a provider saved, you must set up a new one with the same configuration details along with additional information for SMS callbacks explained in the [Configure SMS Callback](doc:generic-sms#configure-sms-callback) section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64207ba-Callback_URL.png",
        "Callback URL.png",
        676
      ],
      "align": "center",
      "border": true,
      "caption": "Callback URL on CleverTap Dashboard"
    }
  ]
}
[/block]


## Configure SMS Callback

During the SMS provider setup process, you must specify the _mid_ key (you can have a custom name for this key) with  _$$MessageID_ as the value. _$$MessageID_ is the dynamic replacement parameter, replaced by CleverTap with the specific value in the outgoing SMS payload to the provider's endpoint. The provider must send the same value in the callback request to CleverTap's callback URL in the meta key mentioned under Send Callback Events section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d8f3d1-SMS_Callback_Configuration.png",
        null,
        "SMS Callback Working"
      ],
      "align": "center",
      "border": true,
      "caption": "SMS Callback Working"
    }
  ]
}
[/block]


## Sample Request

This section provides information about the sample request payload sent to SMS providers. 

### Sample Request with Batching

The following is a sample request payload structure with batching:

```json
{
	"tid": "$$TemplateID",
	"msgs": [{
		"seq": 1,
		"to": "$$To",
    "mid": "$$MessageID",
		"uid": "$$uid",
		"body": "$$Body",
		"enc": "utf8"
	}]
}
```

> 📘 Batch Size Limit
> 
> CleverTap supports a maximum batch size of 100 records.

### Sample Request without Batching

The following is a sample request payload structure without batching:

```json
{
	"tid": "$$TemplateID",
	"to": "$$To",
	"uid": "$$uid",
  "mid": "$$MessageID",
	"body": "$$Body",
	"enc": "utf8"
}
```

The following table provides information about the key-value pair present in the above sample requests: 

[block:parameters]
{
  "data": {
    "h-0": "Key Name",
    "h-1": "Description",
    "h-2": "Sample Value (Case Sensitive)",
    "0-0": "tid",
    "0-1": "Denotes Template ID.  \nAn optional replacement value used to signify the key where the TemplateID of the message is added to the payload.  \nEvery configuration must have $$TemplateID or $$Body key as a mandatory replacement.  \nThis variable is optional and only applicable for campaigns targeted to Indian mobile numbers.",
    "0-2": "Replacement - $$TemplateID  \n  \nFor example, 1107160016156755389",
    "1-0": "mid",
    "1-1": "Denotes Message ID.  \nMetadata that CleverTap sends to the provider and receives in the incoming payload if the callbacks are configured.  \nCleverTap dynamically replaces the mid with the required metadata, which is used to consume callback events and display them on the CleverTap dashboard.",
    "1-2": "Replacement - $$MessageID  \n  \nFor example, 9999999999.1200000000.1654002362.20220531.0.wzrk_default.-1.",
    "2-0": "to",
    "2-1": "A mandatory replacement value used to signify the key where the phone number is added to the payload.",
    "2-2": "$$To",
    "3-0": "body",
    "3-1": "A replacement value used to signify the key where the Body of the message is added to the payload",
    "3-2": "$$Body"
  },
  "cols": 3,
  "rows": 4,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## Send Callback Events

To send callback events to CleverTap, customers must send a POST request to CleverTap's callback URL. The following is the acceptable callback payload structure:

```json
[{
        "event": "failed", //in the case of errors in delivery
        "data": [{
                "ts": <10-digit Epoch Timstamp in seconds>,
                "meta": "<replaced by value received in $$MessageID in the outbound SMS payload>",
                "code": "<ErrorCode>",
                "description": "<error description>"
            },
            {
                "ts": <10-digit Epoch Timstamp in seconds>,
                "meta": "<replaced by value received in $$MessageID in the outbound SMS payload>",
                "code": "<ErrorCode>",
                "description": "<error description>"
            }
        ]
    },
 {
        "event": "replied", //in the case of response from the SMS recipient
        "data": [{
            "ts": <10-digit Epoch Timstamp in seconds>,
            "meta": "<replaced by value received in $$MessageID in the outbound SMS payload>",
            "toPhone": "<The number to which the user replied>",
      			"incomingText": "<Reciepient's response text>"
        }
    ]
    },
    {
        "event": "delivered", //in the case of successful delivery. 
        "data": [{
            "ts": <10-digit Epoch Timstamp in seconds>,
            "meta": "<replaced by value received in $$MessageID in the outbound SMS payload>",
            "description": "Delivered to handset"
        }]
    },
    {
        "event": "clicked", //when the user clicks on the links in the SMS.
        "data": [{
            "ts": <10-digit Epoch Timstamp in seconds>,
            "meta": "<replaced by value received in $$MessageID in the outbound SMS payload>",
            "url": "www.CleverTap.com", //This is the original URL
            "shortUrl": "<short URL from the provider shortened using URL Link shortener>" 
        }]
    }
]
```

The following table provides a brief description of the keys present in the callback payload:

| Key Name       | Description                                                                                                                                                                                     | Sample Values                                              |
| :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------- |
| event\*        | Denotes the event name.                                                                                                                                                                         | failed/replied/clicked                                     |
| ts\*           | Denotes the timestamp in Unix Epoch format.                                                                                                                                                     | 1654512921                                                 |
| meta\*         | Denotes information that CleverTap uses for attributing delivered, clicked, errors, etc., to respective campaigns, profiles, and sms providers. Must be passed as is to CleverTap callback URL. | 9999999999.1200000000.165263328.20220606.0.wzrk_default.1. |
| code\*         | Includes error code in case of an error in SMS delivery.                                                                                                                                        | 900, 901                                                   |
| description\*  | Description of callback event in case of failure or successful delivery.                                                                                                                        | For example: “sender blocked by DLT”                       |
| toPhone        | The number to which the user replied.                                                                                                                                                           | 5555                                                       |
| incomingText\* | User-originated message text. It is the reply string in case of a _replied_ event. This key is mandatory in case of a _replied_ event.                                                          | STOP, START                                                |
| url\*          | URL in case of the click event                                                                                                                                                                  | [www.CleverTap.com](http://www.CleverTap.com)              |
| shorturl       | Short URL in case the outbound URL has been shortened.                                                                                                                                          | <https://bit.ly/3OjG22B>                                   |

\*The asterisk mark against the key name indicates that keys are mandatory in the callback payload. 

> 📘 Note
> 
> If the payload includes additional key-value pairs apart from the ones that are defined in the acceptable sample payload for each event, CleverTap does not throw any errors, but simply disregards those.

## Error Codes

If there is an error in the SMS delivery, these error codes indicate the nature of an error encountered.  Each error code corresponds to a specific error description. The error descriptions are displayed within the Errors tab within the campaign stats section in case of any delivery-related failures. The following table provides information about the acceptable error codes:

[block:parameters]
{
  "data": {
    "h-0": "Error Code",
    "h-1": "Error Description",
    "h-2": "Details",
    "0-0": "901",
    "0-1": "DND failure",
    "0-2": "DND Failure refers to a scenario where a text message was not delivered to a recipient due to their phone number being registered on the national Do Not Disturb (DND) registry, which contains a list of phone numbers that have opted out of receiving promotional or marketing messages.",
    "1-0": "902",
    "1-1": "Failed spam detected",
    "1-2": "One of the most common reasons for SMS delivery failure is carrier-level spam filters. Carriers have added systems and algorithms that detect spam content and then block these messages. Unfortunately, these filters are hidden, subject to carrier preferences, vary from carrier to carrier, and can be changed without notice.",
    "2-0": "903",
    "2-1": "Failed rejected blacklist",
    "2-2": "The user has already sent a STOP/DND opt-out message and no longer wishes to receive messages from you. Other reasons could be illegal use of the number, nonpayment of bills, number belonging to VIPs, government order to stop SMS to the number, complaints from other mobile users about that number, or user complains to the operator/TRAI regarding unsolicited SMS being received. ",
    "3-0": "904",
    "3-1": "Failed system error",
    "3-2": "SMS failed while processing within your SMS Providers system.",
    "4-0": "905",
    "4-1": "Failed subscriber error",
    "4-2": "Problems with subscribers or recipients that are not related to their device, such as a lack of mobile balance or poor network to receive the SMS.",
    "5-0": "906",
    "5-1": "Blocked by DLT",
    "5-2": "Applicable only for SMS sent to Indian destination numbers via domestic lines. Sender ID (Header) is blocked or failed at the DLT platform by the operator due to mismatch, non-registration, template not linked with Sender (header), etc. ",
    "6-0": "907",
    "6-1": "Entity blocked by DLT",
    "6-2": "Applicable only for SMS sent to Indian destination numbers via domestic lines. Entity (DLT Entity ID) is blocked or failed at the DLT platform by the operator due to DLT Entity ID not being passed in API or configured on your SMS Providers Dashboard, values are mismatching, etc.",
    "7-0": "908",
    "7-1": "Template blocked by DLT",
    "7-2": "Applicable only for SMS sent to Indian destination numbers via domestic lines. Template (Template ID) is blocked or failed at DLT due to Template ID not set in API or configured on your SMS Providers Dashboard, content is not exactly matching, non-registration of the template, etc.",
    "8-0": "909",
    "8-1": "Failed DLT consent error",
    "8-2": "The SMS DLT consent registration is required for you to continue sending SMS to your customers. Applicable only for SMS sent to Indian destination numbers via domestic lines.",
    "9-0": "910",
    "9-1": "Invalid subscriber",
    "9-2": "Invalid/Inactive number. The number is either not a valid phone number, or it is no longer active.",
    "10-0": "912",
    "10-1": "Message Inbox Full",
    "10-2": "The user's inbox was full at the time of delivery.",
    "11-0": "913",
    "11-1": "NDNC Rejected",
    "11-2": "Number registered in NCPR database as DND.",
    "12-0": "914",
    "12-1": "Undelivered",
    "12-2": "Message delivery failed after multiple retries due to operator/end-user issues.",
    "13-0": "915",
    "13-1": "Dropped",
    "13-2": "Number banned by Indian Govt as it belongs to J&K (Jammu and Kashmir) series. Other reasons could be SMS dropping by the operator due to no usage of SIM i.e. no voice calls (incoming and outgoing), SMS, and data continuously for 60 days from the date of the first call.",
    "14-0": "916",
    "14-1": "Expired",
    "14-2": "The message was undelivered after multiple retries from the Operator because of the issues at the operator's end.",
    "15-0": "917",
    "15-1": "Force Expired",
    "15-2": "The message dropped due to one of the following reasons:  \n  \n<li> SMS provider’s rule</li> <li>Invalid numbers in the uploaded base, or </li> <li> The client has requested to drop.</li>",
    "16-0": "918",
    "16-1": "Duplicate Message Drop",
    "16-2": "The SMS provider dropped the duplicate message, as the same message content was attempted to be sent on the same mobile number within 30 minutes.",
    "17-0": "919",
    "17-1": "DLT Failure",
    "17-2": "Failed due to some issue at the DLT platform level.",
    "18-0": "920",
    "18-1": "URL not whitelisted",
    "18-2": "SMS rejected by operator as URL is not whitelisted."
  },
  "cols": 3,
  "rows": 19,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


> 🚧 Error Code 900
> 
> Any errors not specified in the above table must be sent with the status code 900 along with the corresponding error description in the incoming payload. The following is the sample payload for error code 900:
> 
> ```json
> [{
> 	"event": "failed",
> 	"data": [{
> 		"ts": 1435322805,
> 		"meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
> 		"code": "900",
> 		"description": "Not able to send message to this phone"
> 	}]
> }]
> ```

## Sample Payload

The following is the acceptable sample payload:

```json
[{
        "event": "failed", //in the case of errors in delivery 
        "data": [{
                "ts": 1654512921,
                "meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
                "code": "901",
                "description": "DND Failure"
            },
            {
                "ts": 1654512921,
                "meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
                "code": "902",
                "description": "Failed spam detected"
            }
        ]
    },
 {
        "event": "replied",
        "data": [{
            "ts": 1435322805,
            "meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
            "toPhone": "5555",
      			"incomingText": "STOP"
        }
    ]
    },
    {
        "event": "delivered", //in the case of successful delivery. 
        "data": [{
            "ts": 1435322805,
            "meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
            "description": "Delivered to handset"
        }]
    },
    {
        "event": "clicked", //when the user clicks on the links in the SMS.
        "data": [{
            "ts": 1435322805,
            "meta": "9999999999.1200000000.165263328.20220606.0.wzrk_default.1.",
            "url": "www.CleverTap.com", //This is the original URL
            "shortUrl": "https://bit.ly/3OjG22B" 
        }]
    }
]
```

## Incoming Payload Mapping to System Events

CleverTap maps the following incoming payloads with their respective system events. You can view these on the CleverTap dashboard.

[block:parameters]
{
  "data": {
    "h-0": "Event Name",
    "h-1": "Sample Payload Structure",
    "h-2": "Mapping to CleverTap System Events",
    "0-0": "Notification Delivered",
    "0-1": "\\[{  \n\t\"event\": \"delivered\",  \n\t\"data\": [{  \n\t\t\"ts\": 1435322805,  \n\t\t\"meta\": \"9999999999.1200000000.165263328.20220606.0.wzrk_default.1.\",  \n\t\t\"description\": \"Delivered to handset\"  \n\t}]  \n}]",
    "0-2": "Maps to Notification Delivered event. For more information, refer to [Events](https://docs.clevertap.com/docs/events#system-events).",
    "1-0": "Notification Clicked",
    "1-1": "\\[{  \n\t\"event\": \"clicked\",  \n\t\"data\": [{  \n\t\t\"ts\": 1435322805,  \n\t\t\"meta\": \"9999999999.1200000000.165263328.20220606.0.wzrk_default.1.\",  \n\t\t\"url\": \"www.CleverTap.com\",  \n                \"shorturl\": \"ct9.io/12345\"  \n\t}]  \n}]",
    "1-2": "<li> Value of the `url` key in the payload is populated in the `wzrk_c2a` event property of the Notification Clicked event. </li> <li> Value of the `shorturl` key in the payload is populated in the `wzrk_c2a_short_url` event property of the Notification Clicked event.</li> <li> For more information, refer to [Events](https://docs.clevertap.com/docs/events#system-events).</li>",
    "2-0": "Notification Replied",
    "2-1": "\\[{  \n\t\"event\": \"replied\",  \n\t\"data\": [{  \n\t\t\"ts\": 1435322805,  \n\t\t\"meta\": \"9999999999.1200000000.165263328.20220606.0.wzrk_default.1.\",  \n                \"toPhone\": \"5555”,  \n\t\t\"incomingText\": \"This is the user's response(512 chars only)\"  \n\t}]  \n}]",
    "2-2": "Value of `incomingText` in the payload is populated in the Notification Replied event. For more information, refer to [Events](https://docs.clevertap.com/docs/events#system-events)."
  },
  "cols": 3,
  "rows": 3,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


> 📘 Notification Replied
> 
> CleverTap trims the string within the `incomingText` parameter of the _Notification Replied_ event containing more than 512 characters.

## Response Codes

CleverTap sends the following status codes and descriptions as a response to the SMS provider upon receiving callbacks:

| Status Code | Description                                        | Explanation                                                                                                   |
| :---------- | :------------------------------------------------- | :------------------------------------------------------------------------------------------------------------ |
| 200         | -                                                  | Success.                                                                                                      |
| 400         | Bad request. Some mandatory parameter was missing. | Occurs when any of the mandatory keys are missing from the payload or n case of issues in the payload format. |
| 500         | Server error                                       | CleverTap internal server error. Contact CleverTap support if the issue persists.                             |
| 503         | Service Unavailable                                | CleverTap internal server error. Contact CleverTap support if the issue persists.                             |

> 📘 Retry Mechanism for Errors
> 
> In case of HTTP 5XX errors, we recommend retrying after 10 minutes with exponential backoff as CleverTap does not deduplicate requests.

### Sample Payload

The following is the payload structure sent by CleverTap to the providers upon receiving the payload:

```json
{
	"status": "<success, partial, fail>",
	"processed": "<count// should be sent as long int>",
	"unprocessed": [{
	"status": "fail",
	"code": "<error code>",
	"error": "<error description>",
	"record": "<record>"
	}]
}
```

The following is the sample success payload:

```json
{
    "status": "success",
    "processed": 1,
    "unprocessed": []
}
```

The following is the sample error payload:

```json
{
    "status": "fail",
    "processed": 0,
    "unprocessed": [
        {
            "status": "fail",
            "code": 400,
            "error": "Bad Request. Some mandatory parameter was missing",
            "record": {
                "event": "failed",
                "data": [
                    {
                        "ts": 1686138005,
                        "meta": "919632453300.1656678144.1686137940.20230607.0.wzrk_default.-1092441.",
                        "description": "NDNCRejected"
                    }
                ]
            }
        }
    ]
}
```

## Stats

CleverTap displays comprehensive stats such as Errors, Delivered, Clicked, and CTRs upon receiving callbacks from the SMS service provider. After setting up the provider on the CleverTap dashboard, you can view these statistics from the following pages on the CleverTap dashboard:

- _Stats_ tab of the Campaigns. For more information, refer to [SMS Setup](doc:sms-stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e014c49-SMS_Campaign_Stats_page.png",
        null,
        "SMS Campaign Stats"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "SMS Campaign Stats"
    }
  ]
}
[/block]


- Stats tab under Provider setup. For more information, refer to the [Provider Stats](doc:sms-provider-operations#view-provider-stats).