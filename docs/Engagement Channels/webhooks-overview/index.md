---
title: Webhooks
excerpt: Monitor specific events.
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

CleverTap webhooks enable you to pass user information basis on specific business workflows to any third-party endpoint. 

For example, when a high-value transaction is abandoned on your e-commerce website, you can send details about the abandoned products and user details via a webhook campaign to your operations center.

There are six categories of webhooks that you can create. The table below describes each of those categories.

| Type                         | Description                                                                          | Example                                                 |
| :--------------------------- | :----------------------------------------------------------------------------------- | :------------------------------------------------------ |
| Single action                | User performed an action.                                                            | User launched the app.                                  |
| Actions                      | User performed multiple actions.                                                     | User launched the app and viewed a notification.        |
| Inaction within time         | User performed an action, but does not perform another action within a certain time. | User has not launched the app in three days.            |
| Inaction                     | Users performed an action, but did not perform another action.                       | User launched the app, but did not view a notification. |
| Date time property           | Period of time after a date time property on a user event.                           | User purchased an item and three days have passed.      |
| Actions with user properties | Performed an action or not, filtered by their demographic properties.                | User purchased an item and lives in Canada.             |

# FAQs

## Q. What are the timeouts and retry limits for Webhook?

A. The timeout for Webhook is 5 seconds with a retry limit of 2 times.

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).
