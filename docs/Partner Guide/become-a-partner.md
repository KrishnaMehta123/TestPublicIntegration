---
title: Become a Technical Partner
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

CleverTap Marketplace gives our customers an option to integrate with different partners. This document helps you understand how to make the most of our adaptable, accommodating platform. Read on to learn how you can become a CleverTap Certified Technical Partner.

# Key Concepts

* **Users**\
   CleverTap creates the user profile for each user who launches the application, opens the website, or whose data is pushed directly to CleverTap from third-party systems. For more information, refer to [User Profiles](doc:user-profiles).

* **Events**\
   Events track user actions on your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item. For more information, refer to [Events](doc:events).

* **Segments**\
   A segment in CleverTap is a group of users who perform specific actions, users who did not perform certain actions, or whose user profile properties match a set of defined criteria. For example, a segment can be users who launched the app for the first time in the past 30 days. For more information, refer to [Segments](doc:segmentation).

* **Engagement Channels**\
   CleverTap offers different messaging channels to create engagement strategies to reach your users with a personalized message at the right time. This includes Push, In-app, App Inbox, Native Display, SMS, Email, Whatsapp, and Webhook. For more information, refer to [Messaging Channels](doc:push).

* **Region - Data Center**\
  CleverTap allows their customer to store data in different centers. For more information about configuring different regions for CleverTap, refer to [Configuration Steps to Enable CleverTap Region](https://developer.clevertap.com/docs/idc#enable-clevertap-region). 

# Generic Integration Guide

To set up the integration with CleverTap, refer to the following sections:

* [API](doc:become-a-partner#api)
* [Attribution](doc:become-a-partner#attribution)
* [Email](doc:become-a-partner#email)
* [SMS](doc:become-a-partner#sms)
* [WhatsApp](doc:become-a-partner#whatsapp)
* [Webhook](doc:become-a-partner#webhook)
* [Linked Content](doc:become-a-partner#linked-content)

## API

* **Authentication**\
  If you are a CleverTap customer trying to connect your partner dashboard to the CleverTap dashboard, you must use the `connect` API. This API enables partners to verify customer account credentials. For more information, refer to [Authorize Partners](https://developer.clevertap.com/docs/authentication#authorize-partners).

* **Importing User**\
   This API helps you upload user information to CleverTap. For more details, refer to [Upload User API](https://developer.clevertap.com/docs/upload-user-profiles-api).

* **Importing Events**\
   This API helps you upload user actions to CleverTap. For more details, refer to [Upload Events API](https://developer.clevertap.com/docs/upload-events-api). 

* **Getting User's Information**\
   This API will help you to get the User's information based on the required segments. For example, provide the list of all the users who have performed the App Launched event in the last 30 days. For more details, refer to [Get User Profile API](https://developer.clevertap.com/docs/get-user-profiles-api).

## Attribution

CleverTap partners with different attribution providers that help customers to know where their users are coming from and engage with them effectively. If your attribution provider is not listed under our partner list, our customers can still connect by following the steps listed under [Generic Attribution Partner](doc:generic-attribution-partner).

## Email

CleverTap supports Email service providers via an HTTP integration. The Email provider must support receiving emails via the HTTP protocol. For more information, refer to [Generic SMTP](doc:generic-smtp).

## SMS

CleverTap supports SMS providers via an HTTP integration. The SMS provider must support receiving messages via the HTTP protocol. For more information, refer to [Generic SMS](doc:generic-sms).

## WhatsApp

CleverTap has a WhatsApp API and standard callback formats public to global communities of WhatsApp service providers. BSPs and customers need not depend on CleverTap to build the native WhatsApp integration. Instead, BSPs or customers can use these APIs directly and build the integration independently. For more information, refer to [Generic WhatsApp](doc:generic-whatsapp).

## Webhook

CleverTap webhooks enable customers to pass user information basis-specific business workflows to any third-party endpoint. For more information, refer to [Webhooks](doc:webhooks-overview).

## Linked Content

Linked content allows customers to personalize their messages with rich and contextual data available outside of the CleverTap platform. For more information, refer to [Linked Content](doc:linked-content).

# Additional Information

To properly understand API usage and provide you with resources as part of our Technology Partner Program, you must first define your *Partner ID*. Pass *Partner ID*  along when calling CleverTap's APIs to send event data.

Your Partner ID must be a string representing your company's or solution's name. If CleverTap were a developer, our Partner ID would be "CleverTap."

For event data, you must include your `Partner ID` as the `$source` property value. The following is an example of passing a `Partner ID`:

```json
{
   "d": [
       {
           "identity": "john_124",
           "type": "event",
           "$source": "CleverTap",
           "evtName": "Product CleverTap 1",
           "evtData": {
               "Product name": "Casio Chronograph Watch"
              }
       }
   ]
}
```

# Steps to Become A Partner

To become a Technical Partner:

1. Perform the integration at your end and test the integration.
2. Write to us at [integrations@clevertap.com](mailto:integrations@clevertap.com) for the following:
   * Sharing the name of customers interested in the integration
   * Getting your Partner ID whitelisted on the CleverTap dashboard.
   * Defining the scope and its value proposition. We recommend you map integration features to the scope, so the mutual customers understand why you need each one. Describe your integration accurately and do not deliberately mislead or confuse customers – provide clear text, screenshots, and videos to clarify your integration's value.
   * Provide the contact details of the dedicated support and product team so that CleverTap can reach out to them in case of any issues.
3. Create integration documentation and share it with us in a .md format. Refer to the *[Partner Document Template](https://docs.google.com/document/d/1FNLq4Wxf9kTwT3A_My4IveonnCiG0y5LWMUX8RklFZg/edit?usp=sharing)*.\
   After the CleverTap team tests your integration, we list you as our Technical partner on our Marketplace.

# What's next

Once you are listed as a CleverTap Technical partner, this unlocks revenue-driving partnership opportunities.
