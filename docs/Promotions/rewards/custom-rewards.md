---
title: Custom Rewards
excerpt: >-
  Learn how Custom Rewards simplify reward management for enabling seamless
  promotions and user rewards.
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

Custom Rewards help you extend CleverTap’s reward ecosystem to integrate with your own partner systems. They allow you to create, manage, and distribute a catalog of external rewards, such as gift cards, digital subscriptions, physical items (for example, iPhones, cameras), or wallet-based credits, through CleverTap Promo campaigns.

With Custom Rewards, you can maintain a centralized reward catalog that your system or your reward partner can fulfill. CleverTap manages the orchestration, triggering, and secure delivery of these rewards via **webhook notifications** whenever a user qualifies for a campaign.

By using Custom Rewards, you can:

* Configure and manage external rewards centrally.
* Automate reward distribution through Promo campaigns.
* Ensure accuracy, scalability, and governance in reward fulfillment.

# Custom Reward Types

Custom Rewards support two types of reward delivery: 

* **Physical & Digital Reward**: Digital or physical rewards such as vouchers, gift cards, or an iPhone.
* **Self-managed Wallet Credits**: Real money or point-based rewards managed in an external wallet. An external wallet is a real-money or points-based system hosted on your infrastructure. It is responsible for storing, crediting, and redeeming wallet balances when a user earns rewards. CleverTap only triggers the reward delivery via webhook; your wallet service performs the actual crediting.

For more information about how to configure Custom Rewards in a campaign, refer to Create Custom Rewards.

# Examples by Business Verticals

Custom Rewards are flexible and apply across industries. Examples include:

* **Quick Commerce**: Customers spending over $100 can instantly receive a movie ticket or streaming voucher, turning high-value purchases into rewarding experiences.
* **FinTech**: A fixed deposit above ₹10,000 can trigger instant cashback to a user’s wallet, adding real-time value to financial milestones.
* **E-Commerce**: Shoppers completing three purchases in a week can be gifted a third-party voucher, encouraging repeat buying and loyalty.
* **Telecom**: Prepaid users recharging a monthly plan can unlock one-month OTT access, enhancing satisfaction with added entertainment benefits.
* **EdTech**: Learners finishing a course on time can earn a digital certificate and discount voucher, motivating continued engagement.
* **Mobility**: Frequent riders completing ten rides in a month can get wallet credits, rewarding consistent usage.

# Prerequisites

Before you begin, ensure you have the following:

* A webhook endpoint that your system must expose to receive reward data. To know how to do that, refer to [Set Up Webhooks](doc:setup-webhooks#set-up-webhooks).
* Access to CleverTap Promo with the Promo add-on enabled.
* Webhook keys are already configured for mapping CleverTap system keys to your internal reward system.
