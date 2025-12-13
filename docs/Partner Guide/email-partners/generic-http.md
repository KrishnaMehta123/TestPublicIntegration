---
title: Generic HTTP
excerpt: >-
  Learn how to integrate any third-party Email Service Provider with CleverTap
  using the Generic HTTP method.
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

The Generic HTTP feature enables flexible integration with any third-party Email Service Provider (ESP) using the HTTP protocol. It supports sending email campaigns using custom payloads, headers, and dynamic fields. It also enables callback tracking for delivery success, failures, and user interactions such as clicks or unsubscribes.

# Set Up Email Provider in CleverTap

To configure any third-party ESP using the Generic HTTP provider in your CleverTap account, perform the following steps:

1. Go to _Settings_ > _Channels_ > _Email_.
2. Click **+ Provider** and select _Generic HTTP_ from the _Provider_ dropdown.
3. Enter the following provider details:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b717e7c15eec34e63788f1928b5956c2a447899d506fc88c4b34f5f9e335708b-Provider_Setup.png",
        "",
        "Provider Setup"
      ],
      "align": "center",
      "border": true,
      "caption": "Provider Setup"
    }
  ]
}
[/block]


| Field                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nickname                 | A unique name for identifying the configuration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Callback URL             | The Callback URL is used to receive bounce, delivery, and subscription information from the ESP to CleverTap. This is a read-only field that is auto-populated with CleverTap's callback URL. Ensure that you add this URL to your ESP dashboard settings to send callback data to CleverTap.                                                                                                                                                                                                                                                        |
| Request Type             | Choose between `GET` or `POST`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| HTTP Endpoint            | API endpoint of the ESP. Must start with `http://` or `https://`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Authentication           | Choose _None_ or _Basic_. Provide credentials if using Basic authentication.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Headers                  | Add static or dynamic headers. For more information, refer to [Headers](doc:generic-http#headers).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parameters               | Applicable for the POST method. Define the request payload in JSON format; supports both single and batch message delivery. For more information, refer to [Body Parameters](doc:generic-http#body-parameters).                                                                                                                                                                                                                                                                                                                                      |
| Batch parameter          | <li>Applicable for the POST method.</li> <li>Enable to send up to 1000 emails in one API call. Before enabling this option, confirm the batch size supported by your ESP.</li><p> For more information, refer to [Body Parameters](doc:generic-http#body-parameters).</p>                                                                                                                                                                                                                                                                            |
| Default From Address     | <li> This is a mandatory field only if the feature is enabled for your account.</li> <li> Enter the default email address you want to use for sending your email campaigns.</li> <li> The email address will be pre-populated under the _From Email Address_ field as a default value when creating an Email campaign.</li> <br>**Note**: Adding _Default From Address_ to your email campaigns is currently in Private Beta. For more information, refer to [Sender Details](doc:create-message-sender-details#sender-details).                     |
| Default Reply to Address | <li> This field is available only if the feature is enabled for your account.</li><li>Enter the default email address to which you want your users to reply to the campaign. </li> <li> The email address will be used to pre-populate the  _Reply-to Email Address_ field as a default value when creating an Email campaign.</li><br> **Note**: Adding _Default Reply-to Email Address_ for your email campaigns is currently in Private Beta. For more information,  refer to [Sender Details](doc:create-message-sender-details#sender-details). |
| Email Preference Center  | <li> Select _System_ from the dropdown to use a pre-built preference center with a sample preview. </li>  <li>Select _Custom URL_ to add your hosted unsubscription page URL. </li> <li> Select _None_ if you want to manage the email preferences directly on your own. </li>  For more information, refer to [Manage Email Preferences](doc:manage-email-preferences#configure-email-preference-center).                                                                                                                                           |

4. Click **Save** and click **Send Test Email** to verify the setup.

# Set Up Message Payload

You can configure headers and define the JSON payload structure for sending emails through your Generic HTTP provider, which supports dynamic values and batching.

## Headers

Specify headers to pass authentication details (such as API keys or credentials) and campaign-level metadata. Authentication headers are typically static, for example, a username/password or token, and should be added as fixed key-value pairs. If your provider requires additional metadata (such as campaign identifiers) to be sent as headers, use dynamic placeholders to populate those at runtime.

You can either specify one of the following types of headers:

- **Static Headers**: In this case, you must specify fixed values. For example, `Authorization: Bearer <API_KEY>` or `Content-Type: application/json`.
- **Dynamic Headers**: Dynamic headers allow you to personalize your HTTP request payload with campaign-level and user-level values at send time. These placeholders are defined using the $$ prefix and are replaced with actual values during message delivery. For instance, you can include placeholders such as `$$UserName` or `$$CampaignID` in the request headers. These are dynamically populated with actual values defined during campaign setup. To learn about Dynamic Replacement Parameters, refer to [System Dynamic Replacements](doc:generic-http#system-dynamic-replacements) and [Custom Dynamic Replacements](doc:generic-http#custom-dynamic-replacements).

  [block:image]{"images":[{"image":["https://files.readme.io/d0ef4f8b54b35652aa473d75739ca3adf93f92a2a9943e8e58d0c64cf4ae0279-POST_Method_-_Headers_Setup.png","","Dynamic Headers - POST Method"],"align":"center","sizing":"50% ","border":true,"caption":"Dynamic Headers - POST Method"}]}[/block]

  In the following example, `"UserName": "$$UserName"` is a dynamic placeholder used in the payload. The part that follows the $$ (in this case, UserName) must match the key you define in the _Request Headers_ section during campaign setup.

  CleverTap uses this mapping to replace the placeholder with the corresponding value at the time of sending the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0b9bbfaadecbaf2e1acdf8540659e87aa6723c40f9905c1b4c289016e99d8f6-POST_Parameters_screenshot.png",
        null,
        "Define Parameters - Generic HTTP via POST Method"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure Parameters For POST Method"
    }
  ]
}
[/block]


When using the GET method, parameters are passed via the _Request Query Parameters_ section. This section allows you to define dynamic values that CleverTap sends into the query string of your HTTP endpoint.

> 🚧 Note
> 
> Do not use dynamic placeholders such as `$$HTML` or any large body content in the query string of the request. Including such content can significantly increase the URL length and may lead to request failures.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f3c8d0c524630d0d2bf5239af9aba583eb2e1e168427b24aef2926499b819239-image.png",
        null,
        "Provider Setup for Generic HTTP - GET Method "
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Provider Setup for Generic HTTP - GET Method "
    }
  ]
}
[/block]


In the following example, you define a value for PromoCode during campaign creation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/121117e7a212b1cdb34cdc27b8161ffad25b55b77fe96f07d01eefd4fd7b2dc0-image.png",
        null,
        "Define Request Query Parameters - For GET Method"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Request Query Parameters - For GET Method"
    }
  ]
}
[/block]


## Body Parameters

For a POST request type, these parameters are included in the request body to define recipient details and message content. You can also configure batch processing to send multiple messages in a single request.

### Sample Request Without Batching

```json
{
  "peid": "1202159255273620968",
  "tmid": "1202159255273620968",
  "cid": "$$CampaignID",
  "fromName": "$$FromName",
  "fromAddress": "$$FromAddress",
  "to": "$$To",
  "cc": "$$cc",
  "bcc": "$$bcc",
  "mid": "$$MessageID",
  "uid": "$$userid",
  "variables": "$$TemplateVariables",
  "typeB": "$$HTML",
  "plaintext": "$$Plaintext",
  "amp": "$$AMPHTML",
  "replyTo": "$$ReplyToAddress",
  "tid": "$$Subject"
}
```

### Sample Request With Batching

If your provider supports batching, structure your payload as shown below. In the following example, the `msgs` array holds multiple personalized email messages. Ensure all dynamic parameters that require user-level or campaign-level personalization (such as $$CampaignID) are included within each object inside `msgs`.

```json
{
  "peid": "1202159255273620968",       // Static Global key-value pair
  "tmid": "1202159255273620968",       // Static Global key-value pair
  "msgs": [
    {
      "seq": 1,													// Static parameter
      "cid": "$$CampaignID",           
      "type": "$$FromName",
      "typeA": "$$FromAddress",
      "to": "$$To",
      "cc": "$$cc",
      "bcc": "$$bcc",
      "mid": "$$MessageID",
      "uid": "$$userid",		// Dynamic custom parameter, value for userID key should be provided during campaign setup
      "typeB": "$$HTML",
      "plaintext": "$$Plaintext",
      "amp": "$$AMPHTML",
      "replyTo": "$$ReplyToAddress",
      "tid": "$$Subject"
    },
    {
      "seq": 2,
      "cid": "$$CampaignID",
      "type": "$$FromName",
      "typeA": "$$FromAddress",
      "to": "$$To",
      "cc": "$$cc",
      "bcc": "$$bcc",
      "mid": "$$MessageID",
      "uid": "$$userid",
      "typeB": "$$HTML",
      "plaintext": "$$Plaintext",
      "amp": "$$AMPHTML",
      "replyTo": "$$ReplyToAddress",
      "tid": "$$Subject"
    }
  ]
}
```

> 📘 Batch Size Limit
> 
> CleverTap supports a maximum batch size of 1000 records in a single request.

## System Dynamic Replacements

You can use the following dynamic replacements within your payload. At send time, CleverTap replaces each placeholder with the corresponding value.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "h-2": "Mandatory",
    "0-0": "`$$To`",
    "0-1": "A dynamic replacement parameter replaced by CleverTap with the recipient’s email address.",
    "0-2": "Mandatory",
    "1-0": "`$$Subject`",
    "1-1": "A dynamic replacement parameter replaced by CleverTap with the subject line of the email.",
    "1-2": "Mandatory",
    "2-0": "`$$FromName`",
    "2-1": "A dynamic replacement parameter replaced by CleverTap with the sender’s display name.",
    "2-2": "Mandatory",
    "3-0": "`$$FromAddress`",
    "3-1": "A dynamic replacement parameter replaced by CleverTap with the sender’s email address.",
    "3-2": "Mandatory",
    "4-0": "`$$HTML`",
    "4-1": "A dynamic replacement parameter replaced by CleverTap with the HTML content of the email.",
    "4-2": "Mandatory",
    "5-0": "`$$MessageID`",
    "5-1": "A dynamic replacement parameter replaced by CleverTap with a unique identifier in the outgoing Email payload to the provider endpoint. The provider must send the same value in the callback request to CleverTap's [callback](doc:generic-http#set-up-callbacks)  URL in the `meta` key. This is mandatory for DLR (delivered and delivery-related errors such as bounces, unsubscribe, spam, and so on) tracking.",
    "5-2": "Mandatory for delivery tracking",
    "6-0": "`$$cc`",
    "6-1": "A dynamic replacement parameter replaced by CleverTap with the CC recipient email addresses.  \n  \n**Note**: Adding CC recipients to email campaign is currently in Private Beta. CleverTap recommends using the `$$cc` field only if your account has CC support enabled for email campaigns. If the feature is not enabled or CC recipients are not configured during campaign setup, CleverTap still includes the key in the payload with a blank value. For more information, refer to [CC/BCC](doc:create-message-email#ccbcc).",
    "6-2": "Optional",
    "7-0": "`$$bcc`",
    "7-1": "A dynamic replacement parameter replaced by CleverTap with the BCC recipient email addresses.  \n  \n**Note**: Adding BCC recipients to email campaign is currently in Private Beta. CleverTap recommends using the `$$cc` field only if your account has CC support enabled for email campaigns. If the feature is not enabled or CC recipients are not configured during campaign setup, CleverTap still includes the key in the payload with a blank value. For more information, refer to [CC/BCC](doc:create-message-email#ccbcc).",
    "7-2": "Optional",
    "8-0": "`$$ReplyToAddress`",
    "8-1": "A dynamic replacement parameter replaced by CleverTap with the reply-to email address.",
    "8-2": "Optional",
    "9-0": "`$$Plaintext`",
    "9-1": "A dynamic replacement parameter replaced by CleverTap with the plain-text version of the email.",
    "9-2": "Optional",
    "10-0": "`$$AMPHTML`",
    "10-1": "A dynamic replacement parameter replaced by CleverTap with the AMP version of the email.  \n  \n**Note**: AMP for Email is available only with Email Booster Max/Advanced Email add-on. Contact your Customer Success Manager to upgrade your plan.",
    "10-2": "Optional",
    "11-0": "`$$CampaignID`",
    "11-1": "A dynamic replacement parameter replaced by CleverTap with the CleverTap campaign ID.",
    "11-2": "Optional"
  },
  "cols": 3,
  "rows": 12,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


## Custom Dynamic Replacements

Custom dynamic replacements allow you to pass additional metadata, such as user preferences or campaign-level attributes, into your payload. These placeholders are defined during campaign setup and are replaced by CleverTap at send time.

```json
{
  "cid": "432",                            // Global Key-Value pair
  "msgs": [                               // Start of batched message array
    {
      "from": "$$FromName",             // System Dynamic Parameter: sender display name
      "senderaddr": "$$FromAddress",   // System Dynamic Parameter: sender email address
      "to": "$$To",                   // System Dynamic Parameter: recipient email address
      "mid": "$$MessageID",          // System Dynamic Parameter: unique message ID (used in callbacks)
      "name": "$$name",            // Custom Dynamic Parameter: recipient’s name (user-level personalization)
      "uid": "$$userID",    // Custom Dynamic Parameter: user’s ID (user-level personalization)
      "content": "$$HTML",      // System Dynamic Parameter: HTML email body
      "heading": "$$Subject"   // System Dynamic Parameter: email subject
    }
  ]
}
```

In a batching scenario, the JSON payload consists of the following two parts

- **Global Key-Value Pairs**: Apply uniformly across the entire batch, do not support personalization. In the above example, `cid : 432` is a global key-value pair.
- **Message-level Key-Value Pairs**: Specific to individual messages within the batch, supports personalization. In the above example, all the parameters within the `msgs` array are message body key-value pairs.

  [block:image]{"images":[{"image":["https://files.readme.io/346263802bed10052b6054f8f53a2efc4dcd731df06783e0f6e49044bc8c9cc2-image.png",null,"Campaign Creation in case of Batching"],"align":"center","border":true,"caption":"Campaign Creation in case of Batching"}]}[/block]

  When the campaign is sent, CleverTap resolves all placeholders and sends the payload to your email service provider (refer to the following sample JSON payload): 

```json
{
  "cid": "43a",
  "discountPercentage": "$$DiscountPercentage",
  "msgs": [
    {
      "from": "Acme Deals",
      "senderaddr": "deals@acmestore.com",
      "to": "sara@example.com",
      "mid": "sara@example.com|1568798080|1730799638|20241105|0|wzrk_default|-17005910|",
      "name": "Sara",
      "uid": "user_9021",
      "content": "<html><body>Hello Sara, enjoy your exclusive 20% discount today!</body></html>",
      "heading": "Your 20% Discount Awaits!"
    }
  ]
}
```

# Set Up Callbacks

CleverTap enables real-time tracking of delivery status and user interactions, such as bounces, unsubscribes, spam reports, and clicks, through HTTP callbacks sent to CleverTap's Callback URL displayed during provider setup.

During provider setup, you must include a key in your outgoing payload (for example, `mid`) with `$$MessageID` as its value. CleverTap replaces this dynamic placeholder with a unique identifier for each message sent. This identifier must be returned in the callback payload to allow CleverTap to attribute the callback to the appropriate campaign and user profile.

## Sample Callback Request

The following is an example payload structure of a callback request that can be sent to the CleverTap callback URL:  

```json
{
  "version": "v2",
  "events": {
    "success": [
      {
        "type": "delivered",	//Indicates the message was delivered to the intended recipient 
        "email": "user@example.com",	//recipient email address
        "meta": "user4@example.com|1568798080|1730799638|20241105|0|wzrk_default|-17005910|"
      }
    ],
    "failed": [ 
      {
        "type": "unsubscribed", // Indicates the user has unsubscribed		
        "email": "user1@example.com",		// The email address of the affected user
        "meta": "user1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005907|",
        "description": "User Unsubscribed"
      },
      {
        "type": "hard_bounce",
        "email": "user3@example.com",
        "meta": "user3@example.com|1568798080|1730799638|20241105|0|wzrk_default|-17005910|",
        "description": "Hard bounce detected"
      },
      {
        "type": "soft_bounce",
        "email": "user5@example.com",
        "meta": "usert5@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005905|",
        "description": "Recipient Inbox Full"
      },
      {
        "type": "spam",
        "email": "user4@example.com",
        "meta": "user4@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005904|",
        "description": "Marked as spam"
      }
    ]
  }
}
```

Ensure your callback payload includes the following keys:

| keys          | Description                                                                                                                                                                                                                                                                                                         | Required |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| `version`     | Indicates the version of the callback payload schema. Must be set to `v2`.                                                                                                                                                                                                                                          | Yes      |
| `type`        | Type of event for tracing user engagement (for example, `delivered`, `clicked`, `hard_bounce`, `unsubscribed`).                                                                                                                                                                                                     | Yes      |
| `email`       | Recipient email address.                                                                                                                                                                                                                                                                                            | Yes      |
| `meta`        | Required for delivery tracking (DLR). CleverTap sends a unique identifier in place of `$$MessageID` for every outgoing message. The ESP must return this exact identifier in the `meta` field of the callback payload. This ensures CleverTap correctly attributes the event to the corresponding user and campaign | Yes      |
| `description` | An optional description about the event.                                                                                                                                                                                                                                                                            | No       |

## Incoming Payload Mapping to System Events

CleverTap maps the incoming payloads with their respective system events. You can view these on the CleverTap dashboard.

[block:parameters]
{
  "data": {
    "h-0": "Callback Type",
    "h-1": "Maps to CleverTap System Event",
    "h-2": "Sample Payload Structure",
    "0-0": "`delivered`",
    "0-1": "Maps to the Notification Delivered system event. The event property _CT Source_ specifies the email provider used to send the campaign, for example, `Generic email` indicates that the campaign was sent using a generic email provider configuration.",
    "0-2": "{  \n  \"type\": \"delivered\",  \n  \"email\": \"[user@example.com](mailto:user@example.com)\",\t\t\t\t\t\"timestamp\": 1425744000,  \n \"meta\": \"...\"  \n      }",
    "1-0": "`hard_bounce`",
    "1-1": "Maps to the Notification Failed system event and also raises a Channel Unsubscribed event. The user is unsubscribed from future email campaigns. The `description` key in the callback payload is mapped to:<li>The _Error_ event property in the Notification Failed event.</li><li>The _Type_ event property in the Channel Unsubscribed event.</li>",
    "1-2": "{  \n  \"type\": \"hard_bounce\",  \n  \"email\": \"[user@example.com](mailto:user@example.com) \",  \n  \"meta\": \"...\",  \n  \"description\": \"Invalid recipient address\"  \n}",
    "2-0": "`soft_bounce`",
    "2-1": "Maps to the Notification Failed system event. The `description` key is mapped to the _error_ event property. In this case, the user is not unsubscribed from future email campaigns. ",
    "2-2": "{  \n\"type\": \"soft_bounce\",  \n\"email\": \"[user@example.com](mailto:user@example.com) \",  \n\"meta\": \"..\"  \n\"description\": \"Soft bounce detected\"  \n}",
    "3-0": "`unsubscribed`",
    "3-1": "Maps to the Channel Unsubscribed system event. The `description` key is mapped to the _Type_ event property. Also, the user is unsubscribed from future email campaigns.",
    "3-2": "{  \n  \"type\": \"unsubscribed\",  \n  \"email\": \"[user@example.com](mailto:user@example.com)\",  \n  \"meta\": \"...\",  \n  \"description\": \"User unsubscribed\"  \n}",
    "4-0": "`spam`",
    "4-1": "Mpas to the Channel Unsubscribed system event. The `description` key is mapped to the _Type_ event property. Also, the user is unsubscribed from future email campaigns.",
    "4-2": "{  \n\"type\": \"spam\",  \n\"email\": \"[user@example.com](mailto:user@example.com) \",  \n\"meta\": \"..\",  \n\"description\"Spam detected\"\"  \n}",
    "5-0": "`clicked`",
    "5-1": "Maps to the Notification Clicked system event. You must use this only if you are not using CleverTap's default click tracking (to avoid duplicate click numbers).",
    "5-2": "{  \n  \"type\": \"clicked\",  \n  \"email\": \"[user@example.com](mailto:user@example.com)\",  \n  \"meta\": \"...\",  \n  \"description\": \"Link clicked\"  \n}"
  },
  "cols": 3,
  "rows": 6,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


## Response Codes

CleverTap sends the following status codes and descriptions as a response to the ESP upon receiving callbacks:

| Status Code | Error Message                                      | Description                                                                                                          |
| ----------- | :------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| 200         |                                                    | Callback received and processed.                                                                                     |
| 400         | Bad request. Some mandatory parameter was missing. | Occurs when any of the mandatory keys are missing from the payload or when there are issues with the payload format. |
| 5xx         | Server error                                       | CleverTap internal server error. Contact CleverTap support if the issue persists.                                    |

The following is the sample response sent by CleverTap to the provider upon processing the callback payload successfully:

```json
{
  "TOTAL_EVENTS": 4,
  "PROCESSED_EVENTS": 4,
  "UNPROCESSED_EVENTS": []
}
```

> 📘 Retry Mechanism for Errors
> 
> In case of HTTP 5XX errors, we recommend retrying after 10 minutes with exponential backoff as CleverTap does not deduplicate requests.