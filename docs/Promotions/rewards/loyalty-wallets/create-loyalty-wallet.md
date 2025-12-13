---
title: Create Loyalty Wallet
excerpt: Learn how to create a Loyalty Wallet to reward users with virtual points.
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

The loyalty wallet keeps track of all the reward points that can be used for discounts, offers, and in-app purchases. This document provides an overview of wallet creation and explains each configurable field with examples to help you set up your wallet accurately.

# Create a Wallet

To create a wallet:

1. Go to _Promotions_ from the CleverTap dashboard.
2. Click **Rewards** and select **Loyalty Wallets** from the list.
3. Click the **Create Loyalty Wallet** button and configure the following wallet settings:
   1. **Loyalty wallet name**: Enter a unique name of the loyalty wallet. Once created, the wallet name cannot be changed. For example, _Festival Rewards_.
   2. **Loyalty points name**: Choose the applicable currency or points system of the loyalty points associated with the wallet. For example, _Supercoins_.
   3. **Points Expiry:** Define expiration rules if applicable. The points expiry rule can only be set once and cannot be changed later.
      1. **Never**: Points will never expire.
      2. **After**: Points expire after a specific duration. You can specify the number of days after which points must expire.
   4. **Rounding Rules**: Determine how point values are rounded when calculated. You can calculate the point values up to three decimal places. The options include 0, 1, 2, or 3 and have the following rounding types:
      1. **Round up**: Rounds the points up to the nearest specified decimal. For example, if the calculation result is 12.34 and rounding is set to 1 decimal place with Round Up, the points credited will be 12.4.
      2. **Round down**: Rounds the points down to the nearest specified decimal. For example, if the calculation result is 12.78 and rounding is set to 1 decimal place with Round Down, the points credited will be 12.7.
4. Click **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/969df6fcfe723fc072a7dbcb31c891336a60ae81a59db07e02d4c7d52029ffca-Create_Loyalty_Wallet.png",
        null,
        "Set Up a Wallet"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up a Wallet"
    }
  ]
}
[/block]