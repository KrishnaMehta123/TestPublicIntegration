---
title: App Inbox
excerpt: Learn how to drive conversions with App Inbox messages.
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

*App Inbox* is a messaging channel that provides the ability to deliver rich, individually customized content to your users. Messages that are sent to *App Inbox* are saved on the user's device. 

<Image alt="App Inbox Notification" align="center" width="40% " border={true} src="https://files.readme.io/9906f6d-image.png">
  App Inbox Notification
</Image>

# App Inbox as a Channel

Push notification and in-app campaigns are great for grabbing the app user's attention, but they are short-lived. Once swiped off, they lose their ability to engage the customer. If the user is not online or is busy, you lose the opportunity to engage with them forever.

*App Inbox* provides the ability to send lasting content directly to your app from the CleverTap dashboard. Moreover, the inbox messages are targetable to individual segments such as other messaging channels. Your inbox can look different from the inbox of another user; the possibilities are endless.

## Inbox Delivery Timing and Campaign Behavior

App Inbox messages are session-based, meaning they are fetched when the app is launched or a new session begins. In live Push + App Inbox campaigns, the Push notification is delivered instantly, but the Inbox message appears only on the next app launch or session. This can lead to different delivery behaviors depending on the type of campaign and the trigger source.

Here is what to expect in various scenarios:

| Campaign Type    | Trigger Source | App Inbox Delivery                       |
| ---------------- | -------------- | ---------------------------------------- |
| App Inbox        | SDK            | Delivered in **next session/app launch** |
| App Inbox        | API            | Delivered in **next session/app launch** |
| Push + App Inbox | SDK            | Delivered in **next session/app launch** |
| Push + App Inbox | API            | Delivered in **next session/app launch** |

This behavior is by design and helps ensure Inbox messages are retrieved when the app is active.

> 🚧 Trigger App Inbox Notifications via Journeys Only
>
> To trigger an App Inbox notification via API, you must configure it through a Journey.\
> Campaigns do not support API-triggered App Inbox notifications.
>
> For assistance, contact your Customer Success Manager (CSM).

# Examples

## Simple Message

This type of Inbox message consists of only the Title and a Message in the App Inbox. It is an app inbox without the image.\
You can select this template from the WHAT section of the campaign. 

<Image title="Sample template for App-Inbox" alt={484} align="center" className="border" width="smart" border={true} src="https://files.readme.io/99159fa-app_inbox_simple_message_sample.png" />

### Usage Example

Get the app inbox message after you have placed the order stating that the order has been accepted. Example: “Your order has been accepted by the restaurant”

## Carousel Message with Content

Carousel messages in push notifications show multiple images under one notification. It can be personalized according to the campaign run. For every carousel image, we can put a new personalized message, according to the content. You can also add a link for each carousel message to navigate the users to that particular page. 

<Image title="2a Carousel message with Content.png" alt={1080} align="center" className="border" width="smart" border={true} src="https://files.readme.io/017189e-2a_Carousel_message_with_Content.png" />

<Image title="2b Carousel message with Content.png.png" alt={1080} align="center" className="border" width="smart" border={true} src="https://files.readme.io/a586da4-2b_Carousel_message_with_Content.png.png" />

### Usage Example

Along with the advertising images, you can add the related Headline in the message content along and use personalization in these messages

## Carousel Message Without Content

Carousel messages without content can be made in an attractive way that can grab the user's attention and also convey your motive for the campaign. You can add your promotional campaign creatives about your products as an image here without any text message. 

## Message with Icon

When you run a message with an icon app inbox campaign, unlike the “carousel with content” feature, here you cannot add multiple images. You can just add one single image in the given format along with any personalized or generic title and text that you would like to send to the users. 

<Image title="Message with Icon.png" alt={246} align="center" className="border" border={true} src="https://files.readme.io/5f9780b-Message_with_Icon.png" />
