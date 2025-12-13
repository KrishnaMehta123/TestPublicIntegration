---
title: Generic Attribution Partner
excerpt: Understand how to leverage CleverTap APIs to push these events to CleverTap
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

CleverTap partners with various attribution providers that help customers to know where their users are coming from and how they should engage with them. CleverTap allows attribution partners to push the following events:

- Organic attribution events 
- Inorganic install attribution events, and 
- Custom events

# Acceptance Criteria

Any attribution partner can integrate with our open APIs, but they must perform the following steps to be visible on the CleverTap dashboard:

1. Perform the server-side integration at their end.
2. After integrating, reach out to us at [integrations@clevertap.com](mailto:integrations@clevertap.com) for the following:
   - Share the name of customers interested in the integration
   - Get yourself whitelisted on the CleverTap dashboard. 
   - Share details about the type of data to be sent to CleverTap: Organic install, Inorganic install, or Custom events. 
3. [Create a document](https://docs.google.com/document/d/1FNLq4Wxf9kTwT3A_My4IveonnCiG0y5LWMUX8RklFZg/edit?usp=sharing) and share it with CleverTap team in a .md format. Also, provide your company logo in the SVG format with a transparent background. The size of the logo must be _40 x 40 px_.

After CleverTap tests the integration, the partner is then listed on our _Settings_ > _Partners_ page.

# Prerequisites for Integration

The following are the prerequisites for integrating with CleverTap:

- Partner dashboard must accept the following authentication parameters: Project Id, Project Token, Project Passcode, and CleverTap Region.
- Client SDK must capture CleverTap identifiers.
- Ability to call different CleverTap endpoints based on the CleverTap credential configuration.
- Ability to differentiate between Organic and Inorganic install attribution events.

# Integrate with CleverTap

## Workflow

This figure explains the exact process of how the information flows from the application to the CleverTap dashboard:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/441024d-Workflow.png",
        "Workflow.png",
        1217
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Get CleverTap ID

CleverTap uses the Device Identifier key-value parameter to attribute the partner attribution data to the right user. After integrating the CleverTap SDK, the value for the Device Identifier becomes available. If the `device_idetifier` is empty, CleverTap does not process the data.

### For Android

Add the following code to your Android app code:

- **For SDK version 4.2.0 and above**

```java
cleverTapInstance.getCleverTapID(new OnInitCleverTapIDListener() {
   @Override
   public void onInitCleverTapID(final String cleverTapID) {
       // Callback on main thread
       ;
   }   
});
```



- **For SDK version 4.1.1 and below**

```java
String attributionID = cleverTapInstance.getCleverTapAttributionIdentifier();
```



### For iOS

Add the following code to your iOS app code:

```java
[CleverTap autoIntegrate];
[[PartnerSDK sharedTracker] setCustomerUserID:[[CleverTap sharedInstance] profileGetCleverTapAttributionIdentifier]];
```



### For React-Native

Add the following code to your React Native app code:

```java
CleverTap.profileGetCleverTapAttributionIdentifier((err, res) => { 
const userId = res;
});
```



## API Endpoint Format for Capturing Inorganic, Organic, and Custom Events

To push data from your server to CleverTap, use the following API endpoint format:

**API Endpoint Format** 

```text
https://{REGION.}{ENDPOINT}/attribution?partner_name={PARTNERNAME}&event_type={TYPEOFDATA}&timestamp={EPOCH VALUE}&utm_source={UTMSOURCE}&utm_medium={UTMMEDIUM}&utm_campaign={UTMCAMPAIGN}&device_identifier={CLEVERTAPID}&account_id={PROJECTID}&account_token={PROJECTTOKEN}&account_passcode={PASSCODE}&platform={Android/iOS}
```



The following table provides information about the API endpoint parameters:

| <p>Parameter</p>                                       | <p>Description</p>                                                                                                                                                                                                      | <p>Mandatory</p>                                                                      |
| :----------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------ |
| <p>Campaign Source (utm_source)</p>                    | <p>Used to identify the source of your traffic. This could be a website name, search engine, newsletter name, or social network.</p><p>For example, utm_source=google.</p>                                              | <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul> |
| <p>Campaign Medium (utm_medium)</p>                    | <p>Used to identify the medium used to share and access your link. This could be email, social, cost per click (cpc), or any other such method.</p><p>For example, utm_medium=cpc.</p>                                  | <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul> |
| <p>Campaign Name (utm_campaign)</p>                    | <p>Used to identify a campaign or promotion tied to your link. This could be a product name, type of sale, contest name, etc.</p><p>For example, utm_campaign=summer-sale.</p>                                          | <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul> |
| <p>Device Identifier</p>                               | <p>Helps to identify the device to which you must map the attribution data,</p>                                                                                                                                         | <p>Yes</p>                                                                            |
| <p>Event Type</p>                                      | <p>Indicates the type of data received:</p><ul><li>Organic Install</li><li>Inorganic Install</li><li>Custom Event</li></ul>                                                                                             | <p>Yes</p>                                                                            |
| <p>Partner Name</p>                                    | <ul><li>Indicates the name of the attribution partner.</li><li>Partner Name. must be whitelisted. If the Partner Name is not whitelisted, CleverTap drops the request and sends out the error to the partner.</li></ul> | <p>Yes</p>                                                                            |
| <p>Account Id, Account Token, and Account Passcode</p> | <p>Helps validate customer account before capturing the data</p>                                                                                                                                                        | <p>Yes</p>                                                                            |
| <p>Platform</p>                                        | <p>Indicates the application platform. For example, Android, iOS, React Native, etc.</p>                                                                                                                                | <p>Yes</p>                                                                            |
| <p>Timestamp</p>                                       | <ul><li>Indicates the time when event occurred.</li><li>Must be in EPOCH format. </li><li>If you do not send the timestamp, CleverTap considers the processing time as the timestamp for that event.</li></ul>          | No                                                                                    |

> 📘 For CleverTap to accept the attribution data, it is mandatory to provide at least one of the following parameters: Campaign Source (utm_source), Campaign Medium (utm_medium), or Campaign Name (utm_campaign).

> 📘 Additional API Endpoint Parameter
> 
> Apart from the parameters listed in the above table, CleverTap processes the additional parameters without any validation.

- **API Endpoint for Organic Install**  
  The following is the sample API endpoint for the organic install event:

```text
https://api.clevertap.com/attribution?partner_name=airbridge&event_type=organic_install&utm_source=utm_google&utm_medium=gd&utm_campaign=adir&device_identifier=__android11235&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```



- **API Endpoint for Inorganic Install**  
  The following is the sample API endpoint for the inorganic install event:

```text
https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=inorganic_install&utm_source=utm_google&utm_medium=gd&utm_campaign=adir&device_identifier=__android11235&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```



- **API Endpoint for Custom Event**  
  The following is the sample API endpoint for the custom event:

```text
https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=Add_to_cart&timestamp=1656317838&device_identifier=__g1234abc&items=shoes&price=12.00&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```



### Region Mapping for API Endpoints

This section provides a region-wise mapping of API endpoints.

[block:parameters]
{
  "data": {
    "h-0": "Region (Data Center)",
    "h-1": "API Endpoint",
    "h-2": "URL",
    "0-0": "EU (Europe)  \nThis is the default data center.",
    "0-1": "`https://api.clevertap.com/`",
    "0-2": "`https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "1-0": "IN (India)",
    "1-1": "`https://in1.api.clevertap.com/`",
    "1-2": "`https://in1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "2-0": "US (U.S.A)",
    "2-1": "`https://us1.api.clevertap.com/`",
    "2-2": "`https://us1.api.clevertap.com/attribution?partner_name=airbirdge&timestamp=1656317838&event_type=custom&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "3-0": "SG (Singapore)",
    "3-1": "`https://sg1.api.clevertap.com/`",
    "3-2": "`https://sg1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "4-0": "SK (South Korea)",
    "4-1": "`https://sk1.api.clevertap.com/`",
    "4-2": "`https://sk1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "5-0": "Indonesia",
    "5-1": "`https://aps3.api.clevertap.com`",
    "5-2": "`https://aps3.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`",
    "6-0": "Middle East (UAE)",
    "6-1": "`https://mec1.api.clevertap.com`",
    "6-2": "`https://mec1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`"
  },
  "cols": 3,
  "rows": 7,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

# Callback Error Codes

The following table lists down the callback error codes:

| <p>Error Code</p> | <p>Description</p>                                                                                                                                                            |
| :---------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>200</p>        | <p>Ok - Success</p><p>Indicates that the data was successfully sent to CleverTap.</p>                                                                                         |
| <p>401</p>        | <p>Authorization error</p>                                                                                                                                                    |
| <p>400</p>        | <p>Bad request. </p><ul><li>Case 1: {Mandatory Field} is missing</li><li>Case 2: Partner name not whitelisted. Connect with the product team to get it whitelisted.</li></ul> |
| 5XX               | Service Unavailable. Please retry later.                                                                                                                                      |

**Sample Response**

```json
{
  "status": "fail", 
  "error": "Invalid Account Info", 
  "code": 401
}
```



```json
{
    "status": "fail",
    "error": "utm_source is missing",
    "code": 400
}
```



# FAQs

#### Q. What attribution data is accepted by CleverTap?

Ans: CleverTap accepts the following three types of data from our attribution partners:

- Inorganic Install Events
- Organic Install Events
- Custom Events

For more information about these events, refer to [Types of Data](doc:attribution#types-of-data). CleverTap accepts Inorganic install events from Attribution partners by default. Organic Install and Custom events must be enabled from the CleverTap dashboard by navigating to _Settings_ > _Partners_ page.

#### Q. Where can I find the CleverTap project details?

Ans: CleverTap Project ID, Token, Passcode, and Region is available under _Settings_ > _Project_ on the CleverTap dashboard

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44d3714-Project_page.png",
        "Project page.png",
        5724
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



#### Q. Is there any validation API for validating credentials?

Ans: No. Currently, CleverTap does not have an API for validating credentials. So, we recommend trimming the spaces before saving the credentials on the partner dashboard.

#### Q. Any recommendation for integrating with CleverTap?

Ans: Yes, we recommend that for Project ID, Token & Passcode, it should be a text input field accepting alphanumeric characters. For Region, we recommend a dropdown for input with the options EU, US, IN, SG & SK, defaulting to EU.

#### Q. Is batching supported for API?

Ans: No.

#### Q. What are the different errors that we can encounter when performing generic partner attribution integration?

Ans: The following are the different errors that we can experience when performing this integration:

- **Inorganic Installs**: Retry with an exponential back-off in case of 500X errors. 
- **Organic Install**: Retry with an exponential back-off in case of 500X errors. 
- **Custom**: Retry with an exponential back-off in case of 500X errors. 
- **Compulsory parameter missing or Empty**: It throws HTTP 400 and does not retry.
- **Authorization error**: It throws HTTP 403 and does not retry. 

> 📘 Error 500X for More than 10 Minutes
> 
> Write to [integrations@clevertap.com](mailto:integrations@clevertap.com) if you observe a 500X error for more than 10 minutes or 99.5% SLA ([CleverTap System Status](https://status.clevertap.com/)).

#### Q. When does the response timeout?

Ans: 60 seconds.

#### Q. How can I confirm that CleverTap is recording attribution events?

Ans: For organic and inorganic events, CleverTap captures the data under the _UTM Visited_ event. You can filter data by _UTM Visited_ by navigating to _Analytics_ > _Events_ from the dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed80aef-Events_page.png",
        "Events page.png",
        3448
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



For Custom events, CleverTap captures the data by adding a prefix to the event name. For example, if the partner name is _attribution partner_ and the custom event is _Checkout_, we save it as _AP_Checkout_.