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

* Organic attribution events 
* Inorganic install attribution events, and 
* Custom events

# Acceptance Criteria

Any attribution partner can integrate with our open APIs, but they must perform the following steps to be visible on the CleverTap dashboard:

1. Perform the server-side integration at their end.
2. After integrating, reach out to us at [integrations@clevertap.com](mailto:integrations@clevertap.com) for the following:
   * Share the name of customers interested in the integration
   * Get yourself whitelisted on the CleverTap dashboard. 
   * Share details about the type of data to be sent to CleverTap: Organic install, Inorganic install, or Custom events. 
3. [Create a document](https://docs.google.com/document/d/1FNLq4Wxf9kTwT3A_My4IveonnCiG0y5LWMUX8RklFZg/edit?usp=sharing) and share it with CleverTap team in a .md format. Also, provide your company logo in the SVG format with a transparent background. The size of the logo must be *40 x 40 px*.

After CleverTap tests the integration, the partner is then listed on our *Settings* > *Partners* page.

# Prerequisites for Integration

The following are the prerequisites for integrating with CleverTap:

* Partner dashboard must accept the following authentication parameters: Project Id, Project Token, Project Passcode, and CleverTap Region.
* Client SDK must capture CleverTap identifiers.
* Ability to call different CleverTap endpoints based on the CleverTap credential configuration.
* Ability to differentiate between Organic and Inorganic install attribution events.

# Integrate with CleverTap

## Workflow

This figure explains the exact process of how the information flows from the application to the CleverTap dashboard:

<Image title="Workflow.png" alt={1217} align="center" className="border" border={true} src="https://files.readme.io/441024d-Workflow.png" />

## Get CleverTap ID

CleverTap uses the Device Identifier key-value parameter to attribute the partner attribution data to the right user. After integrating the CleverTap SDK, the value for the Device Identifier becomes available. If the `device_idetifier` is empty, CleverTap does not process the data.

### For Android

Add the following code to your Android app code:

* **For SDK version 4.2.0 and above**

```java
cleverTapInstance.getCleverTapID(new OnInitCleverTapIDListener() {
   @Override
   public void onInitCleverTapID(final String cleverTapID) {
       // Callback on main thread
       ;
   }   
});
```

* **For SDK version 4.1.1 and below**

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

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Parameter</p>
      </th>

      <th>
        <p>Description</p>
      </th>

      <th>
        <p>Mandatory</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Campaign Source (utm\_source)</p>
      </td>

      <td>
        <p>Used to identify the source of your traffic. This could be a website name, search engine, newsletter name, or social network.</p><p>For example, utm\_source=google.</p>
      </td>

      <td>
        <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Campaign Medium (utm\_medium)</p>
      </td>

      <td>
        <p>Used to identify the medium used to share and access your link. This could be email, social, cost per click (cpc), or any other such method.</p><p>For example, utm\_medium=cpc.</p>
      </td>

      <td>
        <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Campaign Name (utm\_campaign)</p>
      </td>

      <td>
        <p>Used to identify a campaign or promotion tied to your link. This could be a product name, type of sale, contest name, etc.</p><p>For example, utm\_campaign=summer-sale.</p>
      </td>

      <td>
        <ul><li>For Organic and Inorganic Install: Yes</li><li>For Custom Event: No</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Device Identifier</p>
      </td>

      <td>
        <p>Helps to identify the device to which you must map the attribution data,</p>
      </td>

      <td>
        <p>Yes</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Event Type</p>
      </td>

      <td>
        <p>Indicates the type of data received:</p><ul><li>Organic Install</li><li>Inorganic Install</li><li>Custom Event</li></ul>
      </td>

      <td>
        <p>Yes</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Partner Name</p>
      </td>

      <td>
        <ul><li>Indicates the name of the attribution partner.</li><li>Partner Name. must be whitelisted. If the Partner Name is not whitelisted, CleverTap drops the request and sends out the error to the partner.</li></ul>
      </td>

      <td>
        <p>Yes</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Account Id, Account Token, and Account Passcode</p>
      </td>

      <td>
        <p>Helps validate customer account before capturing the data</p>
      </td>

      <td>
        <p>Yes</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Platform</p>
      </td>

      <td>
        <p>Indicates the application platform. For example, Android, iOS, React Native, etc.</p>
      </td>

      <td>
        <p>Yes</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Timestamp</p>
      </td>

      <td>
        <ul><li>Indicates the time when event occurred.</li><li>Must be in EPOCH format. </li><li>If you do not send the timestamp, CleverTap considers the processing time as the timestamp for that event.</li></ul>
      </td>

      <td>
        No
      </td>
    </tr>
  </tbody>
</Table>

> 📘 For CleverTap to accept the attribution data, it is mandatory to provide at least one of the following parameters: Campaign Source (utm\_source), Campaign Medium (utm\_medium), or Campaign Name (utm\_campaign).

> 📘 Additional API Endpoint Parameter
>
> Apart from the parameters listed in the above table, CleverTap processes the additional parameters without any validation.

* **API Endpoint for Organic Install**\
  The following is the sample API endpoint for the organic install event:

```text
https://api.clevertap.com/attribution?partner_name=airbridge&event_type=organic_install&utm_source=utm_google&utm_medium=gd&utm_campaign=adir&device_identifier=__android11235&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```

* **API Endpoint for Inorganic Install**\
  The following is the sample API endpoint for the inorganic install event:

```text
https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=inorganic_install&utm_source=utm_google&utm_medium=gd&utm_campaign=adir&device_identifier=__android11235&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```

* **API Endpoint for Custom Event**\
  The following is the sample API endpoint for the custom event:

```text
https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=Add_to_cart&timestamp=1656317838&device_identifier=__g1234abc&items=shoes&price=12.00&account_id=W6W-797-865Z&account_token=aca-060&account_passcode=1f81b71b91d84885a898911ab8722f34&platform=android&timestamp=1660717763
```

### Region Mapping for API Endpoints

This section provides a region-wise mapping of API endpoints.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Region (Data Center)
      </th>

      <th>
        API Endpoint
      </th>

      <th>
        URL
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        EU (Europe)
        This is the default data center.
      </td>

      <td>
        `https://api.clevertap.com/`
      </td>

      <td>
        `https://api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        IN (India)
      </td>

      <td>
        `https://in1.api.clevertap.com/`
      </td>

      <td>
        `https://in1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        US (U.S.A)
      </td>

      <td>
        `https://us1.api.clevertap.com/`
      </td>

      <td>
        `https://us1.api.clevertap.com/attribution?partner_name=airbirdge&timestamp=1656317838&event_type=custom&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        SG (Singapore)
      </td>

      <td>
        `https://sg1.api.clevertap.com/`
      </td>

      <td>
        `https://sg1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&device_identifier={CLEVERTAPID}&timestamp=1656317838&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        SK (South Korea)
      </td>

      <td>
        `https://sk1.api.clevertap.com/`
      </td>

      <td>
        `https://sk1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        Indonesia
      </td>

      <td>
        `https://aps3.api.clevertap.com`
      </td>

      <td>
        `https://aps3.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>

    <tr>
      <td>
        Middle East (UAE)
      </td>

      <td>
        `https://mec1.api.clevertap.com`
      </td>

      <td>
        `https://mec1.api.clevertap.com/attribution?partner_name=airbirdge&event_type=custom&timestamp=1656317838&device_identifier={CLEVERTAPID}&platform=android&android_id=&city=Mumbai&match_type=gp_referrer`
      </td>
    </tr>
  </tbody>
</Table>

# Callback Error Codes

The following table lists down the callback error codes:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Error Code</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>200</p>
      </td>

      <td>
        <p>Ok - Success</p><p>Indicates that the data was successfully sent to CleverTap.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>401</p>
      </td>

      <td>
        <p>Authorization error</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>400</p>
      </td>

      <td>
        <p>Bad request. </p><ul><li>Case 1: \{Mandatory Field} is missing</li><li>Case 2: Partner name not whitelisted. Connect with the product team to get it whitelisted.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        5XX
      </td>

      <td>
        Service Unavailable. Please retry later.
      </td>
    </tr>
  </tbody>
</Table>

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

* Inorganic Install Events
* Organic Install Events
* Custom Events

For more information about these events, refer to [Types of Data](doc:attribution#types-of-data). CleverTap accepts Inorganic install events from Attribution partners by default. Organic Install and Custom events must be enabled from the CleverTap dashboard by navigating to *Settings* > *Partners* page.

#### Q. Where can I find the CleverTap project details?

Ans: CleverTap Project ID, Token, Passcode, and Region is available under *Settings* > *Project* on the CleverTap dashboard

<Image title="Project page.png" alt={5724} align="center" className="border" border={true} src="https://files.readme.io/44d3714-Project_page.png" />

#### Q. Is there any validation API for validating credentials?

Ans: No. Currently, CleverTap does not have an API for validating credentials. So, we recommend trimming the spaces before saving the credentials on the partner dashboard.

#### Q. Any recommendation for integrating with CleverTap?

Ans: Yes, we recommend that for Project ID, Token & Passcode, it should be a text input field accepting alphanumeric characters. For Region, we recommend a dropdown for input with the options EU, US, IN, SG & SK, defaulting to EU.

#### Q. Is batching supported for API?

Ans: No.

#### Q. What are the different errors that we can encounter when performing generic partner attribution integration?

Ans: The following are the different errors that we can experience when performing this integration:

* **Inorganic Installs**: Retry with an exponential back-off in case of 500X errors. 
* **Organic Install**: Retry with an exponential back-off in case of 500X errors. 
* **Custom**: Retry with an exponential back-off in case of 500X errors. 
* **Compulsory parameter missing or Empty**: It throws HTTP 400 and does not retry.
* **Authorization error**: It throws HTTP 403 and does not retry. 

> 📘 Error 500X for More than 10 Minutes
>
> Write to [integrations@clevertap.com](mailto:integrations@clevertap.com) if you observe a 500X error for more than 10 minutes or 99.5% SLA ([CleverTap System Status](https://status.clevertap.com/)).

#### Q. When does the response timeout?

Ans: 60 seconds.

#### Q. How can I confirm that CleverTap is recording attribution events?

Ans: For organic and inorganic events, CleverTap captures the data under the *UTM Visited* event. You can filter data by *UTM Visited* by navigating to *Analytics* > *Events* from the dashboard. 

<Image title="Events page.png" alt={3448} align="center" className="border" border={true} src="https://files.readme.io/ed80aef-Events_page.png" />

For Custom events, CleverTap captures the data by adding a prefix to the event name. For example, if the partner name is *attribution partner* and the custom event is *Checkout*, we save it as *AP\_Checkout*.
