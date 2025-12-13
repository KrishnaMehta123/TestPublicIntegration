---
title: 'WhatsApp: Troubleshooting & FAQs'
excerpt: This page covers the FAQs for WhatsApp channel
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Is there a specific aspect ratio for media files in the WhatsApp campaign?

A. No. You can use any aspect ratio to send media files on WhatsApp. The media files are resized dynamically.

## What are the timeouts and retry limits for WhatsApp?

A. The following are the timeout and retry limits for WhatsApp:

| Channel   | Timeout (ConnectionRequest) | Retry Times    |
| :-------- | :-------------------------- | :------------- |
| CleverTap | Not applicable              | 4              |
| Generic   | Not applicable              | Not applicable |
| Gupshup   | Not applicable              | Not applicable |
| Nexmo     | Not applicable              | Not applicable |

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).

## Why do I encounter a 404 error when I open shortened links?

A. The shortened URLs from the WhatsApp campaign expire seven days after the campaign was sent. If the user opens these links after the expiration date, they are redirected to a 404 page.