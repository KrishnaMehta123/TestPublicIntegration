---
title: Create Custom Rewards
excerpt: ''
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

Before using Custom Rewards in Promo campaigns, you must first create the reward configurations that will be triggered via webhooks.

You can create the following two types of Custom Rewards:

* [Create Physical & Digital Reward](doc:create-custom-rewards#create-physical--digital-rewards)
* [Create Self-managed Wallet Credits](doc:create-custom-rewards#create-self-managed-wallet-credits)

# Create Physical & Digital Rewards

Physical & Digital Rewards manage external digital or physical rewards such as vouchers, gift cards, or merchandise. 

To create a Physical & Digital Reward, perform the following steps:

1. Go to *Promo > Rewards > Webhook Rewards > Physical & Digital Reward*.
2. Click **Add reward configuration**.
3. In the creation modal, fill in the following details:

   * **Client Reward ID**: A unique identifier from your system. This value is case-sensitive and must not duplicate an existing reward.
   * **Client Reward Name**: The name of the reward.
   * **Client Reward Description**: Optional details about the reward.
   * **Reward Expiry**: Choose **Never Ends** or a specific date. 
4. Click **Save**.

<Image alt="Add Reward Configuration" align="center" border={true} src="https://files.readme.io/d32d7bd039853122a6a742e2c70ff4cf20301a5f27e951e0f7e8a6d3ae0627a5-Add_Reward_Configuration.gif">
  Add Reward Configuration
</Image>

# Create Self-managed Wallet Credits

Self-managed Wallet Credits represent real money or point-based rewards managed in an external wallet. 

To create a Webhook Wallet, perform the following steps:

1. Go to *Promo > Rewards* > *Webhook Rewards* > *Self-managed Wallet Credits*.
2. Click **Add Wallet Configuration**.
3. In the creation modal, fill in the following details:

   * **Wallet ID**: A unique external wallet ID from your system. This value is case-sensitive and must not duplicate an existing reward.
   * **Wallet Name**: The display name of the wallet.
4. Click **Save**.

<Image alt="Add Wallet Configuration" align="center" border={true} src="https://files.readme.io/5ff7e753bd385ab5224f5eb26bbc4a710c6838e7b13ddf1f26397af072e92395-Add_Wallet_Configuration.gif">
  Add Wallet Configuration
</Image>

<JSONPayloadForCustomRewards />
