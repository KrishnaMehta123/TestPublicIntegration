---
title: Collapse Key
excerpt: >-
  Understand how to use the collapse notification key to update push
  notifications on Android and iOS devices.
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

A collapse notification key, or collapse key, is used to update push notifications on both Android and iOS devices.

This feature is used to update a notification that is rendered and available in the notification tray. While setting up the campaigns, check that the same key is used in similar campaigns. For example, a Score Update notification if the key used is _score-update_. All following campaigns that would be used to update earlier notifications must have the same key.

> 📘 New Notification
> 
> A new notification will be rendered if the earlier notification was dismissed and not present on the device notification tray.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73ae9f0-Collapse_Key.png",
        "Collapse Key.png",
        989
      ],
      "align": "center",
      "border": true,
      "caption": "Collapse Key"
    }
  ]
}
[/block]


# Use Case

Following is the order in which a notification can be replaced:

Push Notification 1 (_general notification_) > Notification 2 (_promo code or coupon_) > Notification 3 (_higher validity offer_).

Coupon code to avail free snacks with orders above $20 at 5:00 PM > Promotional code valid for one hour can be sent at 7:00 PM > Replace it with a thank you notification for ordering and status tracking notification.