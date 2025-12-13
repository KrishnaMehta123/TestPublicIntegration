---
title: Comprehensive Guide to System Events
excerpt: >-
  Gain in-depth insights into CleverTap system events and their associated
  properties to enhance your analytics strategy.
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

This document provides a comprehensive overview of the system events tracked by CleverTap and their associated event properties. Understanding these events and properties will help you effectively analyze user interactions and optimize engagement strategies.

> 📘 IMPORTANT
> 
> The document currently includes details on three system events. We are continuously working to expand this document and will be adding more system events over time. Please check back regularly for updates.

# Notification Delivered

The Notification Delivered event is raised when an Email, WhatsApp, or SMS provider confirms that the campaign has reached the end user. If delivery data is not received, check with your provider to ensure proper integration and callback configurations.

| Property Name | Description                                                                              |
| :------------ | :--------------------------------------------------------------------------------------- |
| CT Source     | Indicates the source from where the event originated, for example, SendGrid.             |
| Campaign id   | Indicates the ID of the campaign or Node ID of a Journey sent to the user.               |
| Campaign type | Indicates the messaging channel. Possible values are Email, SMS, or WhatsApp.            |
| wzrk_id       | Indicates the Campaign ID.                                                               |
| wzrk_pivot    | Indicates the campaign variant, in the case of the A/B Test, which was sent to the user. |

# Notification Failed

The Notification Failed event is raised when the campaign fails to reach the provider. 

| Property Name | Description                                                                                                                                             |
| :------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Campaign ID   | Identifies the specific campaign associated with the error.                                                                                             |
| Campaign Type | Denotes the type of campaign (for example, WhatsApp, SMS, Email, and so on).                                                                            |
| Error         | Denotes the error message for the error observed in the campaign. For more details, refer to [Errors](doc:comprehensive-guide-to-system-events#errors). |
| Label         | Denotes the specific label associated with the campaign.                                                                                                |
| Variant       | Identifies the campaign variant for which the error is observed in the case of A/B, split delivery, or multi-variant campaigns.                         |

## Errors

This section provides insights into the reasons for notification delivery failures across different messaging channels. Understanding these errors helps diagnose issues and improve message deliverability.

These errors can be categorized as follows:

### Cross-Channel Errors

These errors can occur across multiple messaging channels.

| Error                          | Description                                                                                                                                                                               |
| :----------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Profile not reachable          | Occurs when an attempt is made to send a message to a user profile, but CleverTap determines that the profile cannot be contacted through the selected communication channel.             |
| Duplicate profile for channel  | Occurs when multiple user profiles have the same unique identifier, leading to ambiguity in message delivery.                                                                             |
| No recommendation found        | Occurs when no recommendations are available for the profile.                                                                                                                             |
| No Liquid Replacement found    | Occurs when a liquid tag in a message fails to resolve due to incorrect syntax.                                                                                                           |
| Abort liquid logic encountered | Occurs when a message is intentionally not sent due to an ABORT command within the Liquid template. This allows you to prevent message dispatch based on specific criteria conditionally. |
| Liquid render timeout          | Occurs when Liquid template processing exceeds the allowed time limit, preventing the message from being rendered successfully.                                                           |
| User DND                       | Occurs when a message (such as Email, SMS, Push Notification, or WhatsApp) fails to be sent because the recipient profile is marked as Do Not Disturb (DND).                              |
| Group Unsubscribed             | Occurs when a user opts out of receiving messages from a specific subscription group.                                                                                                     |
| User not reachable             | Occurs when a message fails to deliver because the user cannot be contacted via the selected communication channel.                                                                       |
| User not qualified             | Occurs when a user does not meet the required criteria for a campaign, journey, or segment-based message, preventing them from receiving the communication.                               |
| Content API Invalid URL        | Occurs when a request to fetch dynamic content via the Content API fails due to an incorrect, malformed, or unreachable URL.                                                              |
| Content API Invalid            | Occurs when the system is unable to fetch or process data from an external Content API.                                                                                                   |
| Content API Invalid Auth       | Occurs when a request to an external Content API fails due to authentication issues.                                                                                                      |
| ContentAPIFailed 3XX           | Occurs when a request to an external Content API receives an unexpected 3XX (Redirection) HTTP response.                                                                                  |
| ContentAPIFailed 4XX           | Occurs when a request to an external Content API fails due to a client-side error (4XX HTTP status code).                                                                                 |
| ContentAPIFailed 5XX           | Occurs when a request to an external Content API fails due to a server-side error (5XX HTTP status code).                                                                                 |
| ContentAPI Response Exception  | Occurs when the external Content API returns an unexpected response format or an invalid response, preventing CleverTap from processing the retrieved content.                            |

### Email Campaigns Errors

This section covers errors that occur when sending email campaigns, including dispatch failures, delivery issues, and provider-specific errors.

| Error                         | Description                                                                                                                                                                                                                                               |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Email Dispatch Error          | Occurs when an attempt to send an email to a user fails before it can be successfully dispatched.                                                                                                                                                         |
| SendGrid email dispatch error | Occurs when an email sent via CleverTap using SendGrid as the Email Service Provider (ESP) fails to be dispatched. This implies that the email was not successfully handed off to SendGrid for delivery, preventing it from reaching the recipient inbox. |
| Email hard bounced            | Occurs when an email fails to deliver permanently due to an invalid, non-existent, or blocked email address. Future emails to this address are suppressed to maintain sender reputation.                                                                  |
| Email soft bounced            | Occurs when an email temporarily fails due to issues such as a full inbox, server downtime, or message size limits. The ESP may retry sending before marking it as undeliverable.                                                                         |
| Email Dropped                 | Occurs when the ESP does not send the email because the recipient is on a suppression list due to previous bounces, spam complaints, or unsubscribes.                                                                                                     |

# Webhook Delivered

Webhook Delivered event tracks the successful delivery of webhook campaigns sent from CleverTap.

| Property Name | Description                                                                                                                 |
| :------------ | :-------------------------------------------------------------------------------------------------------------------------- |
| CT Source     | Indicates the source from which the webhook was triggered. For example, the event may originate from a Mobile, SDK, or API. |
| Campaign Id   | Unique identifier of the campaign associated with the webhook.                                                              |