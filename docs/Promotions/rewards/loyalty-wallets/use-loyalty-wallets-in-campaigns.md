---
title: Use Loyalty Wallets in Campaigns
excerpt: >-
  Learn how to engage users using the CT Points Credited event and drive repeat
  purchases or desired behaviors.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Engage with Wallet Points Rewarded Users

CleverTap allows you to target users who have received loyalty points by creating a campaign based on the _CT Points Credited_ event. This event helps you personalize communication and encourage users to redeem their points, driving higher conversions and user retention.

Let’s say you are an e-commerce brand that wants to remind users who earned points from a recent purchase or campaign but have not redeemed them yet. You can create a targeted campaign like this:

1. Go to _Campaigns_ from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the dropdown.
3. Click **Add an event** from the _Who_ section.
4. Select the **CT Points Credited** event and apply filters using the event properties.

   [block:image]{"images":[{"image":["https://files.readme.io/64dd0edc80500745812013eded24c2f99887d6b23476e38a3dfadecb22cf2efe-image.png",null,"Target Users with a Campaign/Journey"],"align":"center","border":true,"caption":"Target Users with a Campaign/Journey"}]}[/block]

# CT Points Credited

Whenever a user's wallet is credited with points, either via a campaign, API, or manually, CleverTap triggers the _CT Points Credited_ event. This allows you to create follow-up messaging such as reminders, promotional nudges, or personalized incentives.

The event includes the following System and Custom event properties, which help you to personalize campaigns or segment users:

## System Event Property

| Property      | Description                                              | Example Value |
| ------------- | -------------------------------------------------------- | ------------- |
| **CT Source** | Identifies the source via which the event was triggered. | `API`         |

## Custom Event Properties

| Property              | Description                                                             |
| --------------------- | ----------------------------------------------------------------------- |
| **walletId**          | The unique ID of the wallet credited.                                   |
| **transactionId**     | Unique identifier for the wallet transaction.                           |
| **points**            | Number of points credited.                                              |
| **source**            | Source of the credit (Campaign, API, Manual, Cashback Coupon).          |
| **campaignId**        | ID of the campaign through which the reward was issued (if applicable). |
| **pointsDescription** | Optional description about the transaction.                             |
| **eventTimestamp**    | Time when the points were credited.                                     |

These properties can be leveraged in Liquid Tags to personalize messages, enabling dynamic content in your engagement campaigns.