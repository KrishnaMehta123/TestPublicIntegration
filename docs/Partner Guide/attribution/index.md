---
title: Attribution Partners
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

For marketers, it is very important to understand where their customers are coming from and how they can engage with them effectively. This is when attribution plays a very important role. CleverTap partners with different attribution providers and tracks app installations, measure attribution with third-party sources, and view reports in the CleverTap Dashboard.

CleverTap supports integrations with the following third-party attribution providers:

* [Adjust](https://developer.clevertap.com/docs/adjust)
* [Airbridge](https://developer.clevertap.com/docs/airbridge)
* [AppsFlyer](https://developer.clevertap.com/docs/appsflyer) 
* [Branch](https://developer.clevertap.com/docs/branch)
* [Singular](https://developer.clevertap.com/docs/singular-apsalar)
* [AppTrove by Trackier](https://docs.clevertap.com/docs/apptrove)

# Types of Data

CleverTap receives the following event data from the specified attribution partner and then processes and saves it:

* **Inorganic Install Events** - These install events are attributed to some media source, for example, paid advertisements running on some third-party applications. It implies that the application is installed as a result of engaging with any advertisement.
* **Organic Install Events** - These install events are attributed to the website or app store or referrals. It implies that the application is installed either from the website, app store or via referrals and not by engaging with any kind of advertisements.
* **Custom Events** - These events can be any events (other than install events) that are provided by the attribution partner and tracked in the app. 

The following table lists the default CleverTap dashboard settings to track the events:

| Attribution Partner | Inorganic Install Events | Organic Install Events | Custom Events  |
| :------------------ | :----------------------- | :--------------------- | :------------- |
| CleverTap           | Not applicable           | Always selected        | Not applicable |
| Adjust              | Always selected          | Not selected           | Not selected   |
| Airbridge           | Always selected          | Not selected           | Not selected   |
| AppsFlyer           | Always selected          | Not selected           | Not selected   |
| Branch              | Always selected          | Not available          | Not selected   |
| Singular            | Always selected          | Not selected           | Not selected   |

Depending on the requirement, you can choose to track event data from the *Settings* > *Partners* page of the CleverTap dashboard. 

> 📘 Access Permissions
>
> To update the settings of this page, the user must have admin access or the required access rights.

For more information about enabling attribution settings for supported providers, refer to the following documents: 

* [Adjust](https://developer.clevertap.com/docs/adjust)
* [Airbridge](https://developer.clevertap.com/docs/airbridge)
* [Appsflyer](https://developer.clevertap.com/docs/appsflyer)
* [Branch](https://developer.clevertap.com/docs/branch)
* [Singular (formerly known as Apsalar)](https://developer.clevertap.com/docs/singular-apsalar)
