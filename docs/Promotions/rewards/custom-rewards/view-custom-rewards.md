---
title: View Custom Rewards
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

The *Custom Rewards* section in the **Rewards** option allows you to manage and monitor both *Physical & Digital Rewards* and *Self-Managed Wallets*. 

# Physical & Digital Rewards Tab

The **Physical & Digital Rewards** tab helps you create and manage external digital or physical rewards such as gift cards, vouchers, or merchandise (for example, iPhones, cameras).

Clicking on this tab displays a list of all configured Physical & Digital Rewards. Each reward entry includes the following information:

* CT Reward ID
* Client Reward ID
* Reward Name
* Reward Description
* Promo Campaigns Linked
* Created By / Created Date
* Status (Active, Paused, Archived, Expired, Ended)

<Image alt="Physical & Digital Rewards Tab" align="center" border={true} src="https://files.readme.io/78c2ddd0b3484272d9266a4974b10693d5122ce66d029cd7d2311f5db2e0f297-image.png">
  Physical & Digital Rewards Tab
</Image>

## Manage Physical & Digital Rewards

You can perform the following operations directly from the list view:

| Action        | Availability                                  | Description                                                                                |
| :------------ | :-------------------------------------------- | :----------------------------------------------------------------------------------------- |
| **Activate**  | When status = *Paused*                        | Resumes the reward for distribution in campaigns.                                          |
| **Pause**     | When status = *Active*                        | Temporarily halts the reward from being distributed.                                       |
| **End**       | When status = *Active* or *Paused*            | Stops the reward and marks it as ended.                                                    |
| **Archive**   | When status = *Paused*, *Ended*, or *Expired* | Moves the reward to the archived state; it cannot be reused in active campaigns.           |
| **View JSON** | When status = *Active* or *Paused*            | View reward details, including ctRewardID, rewardName, description, and creation metadata. |

# Self-Managed Wallets Tab

The **Self-Managed Wallets** tab enables you to configure and manage wallet-based reward configurations. These wallets represent external reward systems, such as cashback or loyalty wallet credits hosted on your end.

Clicking on this tab displays wallet configurations in a card view format. Each card contains the following:

* Webhook Wallet ID
* CT Reward ID
* Wallet Name
* Created By
* Created On

<Image align="center" className="border" border={true} src="https://files.readme.io/bc52af03376cf3d06058c5de3128d572d46e703e0bfea7686d5c3c224d7a3859-image.png" />

## Manage Self-Managed Wallets

You can perform the following operations to manage wallets directly from the tab:

| Action        | Description                                | Description                                                                      |
| :------------ | :----------------------------------------- | :------------------------------------------------------------------------------- |
| **Activate**  | When status = *Paused*                     | Resumes the wallet for credits distribution.                                     |
| **Pause**     | When status = *Active*                     | Temporarily halts the wallet from credit distribution.                           |
| **End**       | When status = *Active* or *Paused*         | Stops the wallet and marks it as ended.                                          |
| **Archive**   | Deactivate the wallet if no longer needed. | Moves the wallet to the archived state; it cannot be reused in active campaigns. |
| **View JSON** | When status = *Active* or *Paused*         | View wallet details, including ctRewardID, walletID, and walletName.             |

> 📘 Notes
>
> To ensure smooth management and consistent behavior across all reward types, keep the following points in mind:
>
> * Rewards and wallets can be linked to multiple Promo campaigns.
> * Each reward and wallet credit is assigned a unique CleverTap Reward ID upon creation.
> * Rewards cannot be paused, ended, or archived while actively mapped to an ongoing campaign.
> * Inline validation ensures field accuracy and prevents duplication of reward or wallet IDs.
