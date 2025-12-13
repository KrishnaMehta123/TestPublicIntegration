---
title: Test Push Notifications
excerpt: Understand how to test Push notifications before you send them.
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

This section covers how to send test notifications in operations in two ways and test push notifications with multiple logins.

# Send Test Notifications in Operations

The test notification can be sent during the campaign creation. 

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test push notification to any CleverTap user profile you have marked as a *Test profile*.\
Click the **Preview & Test** button from the message editor to test a message.

<Image title="Send Test Push to Profiles" alt={836} border={true} src="https://files.readme.io/a9f309e-push_test_notification.png">
  Notification Preview and Test
</Image>

In the second approach, you can initiate *Send Push* for the required device to send test push notifications to the user on a specific user profile page. 

<Image title="Delivered Test Push Details" alt={1999} border={true} src="https://files.readme.io/4bd5d33-2.png">
  Push Notifications to Specific Users
</Image>

# Send Test Notifications with Multiple Logins

If there are multiple logins during a test push notification, the push token moves to the latest profile. 

Suppose a user has multiple devices associated with a profile and qualifies for a campaign. In that case, all the devices attached to the user profile will receive the push notification.
