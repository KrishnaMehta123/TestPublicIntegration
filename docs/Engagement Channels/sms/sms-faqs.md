---
title: 'SMS: Troubleshooting & FAQs'
excerpt: >-
  Refer to our frequently asked questions and troubleshoot any issues with your
  SMS campaign.
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

This section covers FAQs related to the SMS messaging channel.

# FAQs

## How to unsubscribe a user from receiving SMS promotions?

A. The [Subscribe API](https://developer.clevertap.com/docs/subscribe-api) allows you to subscribe or unsubscribe to a phone number. This is important so that you do not accidentally send an SMS to a phone number unless they have explicitly opted for it. 

## What is a _Profile not reachable_ error?

A. The _Profile not reachable_ error occurs when the qualified device is not reachable via the selected communication channel.

In the case of SMS, this error occurs if the profile does not have a phone number or the user has unsubscribed from SMS communication.

## What is a _Duplicate Profile for the channel_ error?

A. This error indicates two different profiles have the same credentials, such as a phone number, a push token, and an email (based on the communication channel). The engagement is sent to the first profile, and this error is sent to the second profile.

## Why some emojis and characters do not appear in my SMS body?

A. To resolve this issue, ensure your service provider supports sending special characters or emojis in an SMS.

## What is the character limit for SMS?

A. The limit for a standard SMS is 140 to 160 characters, after which the remainder of the message is sent as a new SMS.

# Campaign

## SMS Error

An SMS error is a common campaign error that occurs while scheduling the SMS campaign. If the SMS service provider’s endpoint is unavailable, the SMS error appears. It applies to generic integrations and MSG91 (SMS provider).

The SMS error shows the following message: 

_Error java.net.SocketTimeoutException: Read timed out for message_. It is referred to as the _SocketTimeoutException_ error.

This SMS error occurs when CleverTap sends the SMS payload to the SMS provider’s endpoint, but there is no acknowledgment within 15 seconds. The SMS error appears under the _Technical Errors_ category. You can view the errors within the campaign reports under the _Error_ section. 

> 📘 Note
> 
> The issue generally means a socket timeout exception. Sometimes, it can also mean a connection request exception.

For other integrated vendors, we have the following equivalent errors: 

- Exotel server error
- Twilio server error
- Gupshup server error
- Netcore service error
- Nexmo SMS error

## What are the timeouts and retry limits for SMS?

A. The following are the timeout and retry limits for SMS:

| Channel     | Timeout (ConnectionRequest) | Retry Times |
| :---------- | :-------------------------- | :---------- |
| Generic SMS | 15 Seconds                  | 0           |
| BatchSMS    | 15 Seconds                  | 0           |
| Msg91       | 15 Seconds                  | 0           |
| GupShup     | 15 Seconds                  | 0           |
| Netcore     | 15 Seconds                  | 0           |
| Nexmo       | 15 Seconds                  | 0           |
| Exotel      | 15 Seconds                  | 0           |
| Twilio      | 15 Seconds                  | 0           |

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).