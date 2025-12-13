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

The _Custom Rewards_ section in the **Rewards** option allows you to manage and monitor both _Physical & Digital Rewards_ and _Self-Managed Wallets_. 

# Physical & Digital Rewards Tab

The **Physical & Digital Rewards** tab helps you create and manage external digital or physical rewards such as gift cards, vouchers, or merchandise (for example, iPhones, cameras).

Clicking on this tab displays a list of all configured Physical & Digital Rewards. Each reward entry includes the following information:

- CT Reward ID
- Client Reward ID
- Reward Name
- Reward Description
- Promo Campaigns Linked
- Created By / Created Date
- Status (Active, Paused, Archived, Expired, Ended)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78c2ddd0b3484272d9266a4974b10693d5122ce66d029cd7d2311f5db2e0f297-image.png",
        null,
        "Physical & Digital Rewards Tab"
      ],
      "align": "center",
      "border": true,
      "caption": "Physical & Digital Rewards Tab"
    }
  ]
}
[/block]


## Manage Physical & Digital Rewards

You can perform the following operations directly from the list view:

| Action        | Availability                                  | Description                                                                                |
| :------------ | :-------------------------------------------- | :----------------------------------------------------------------------------------------- |
| **Activate**  | When status = _Paused_                        | Resumes the reward for distribution in campaigns.                                          |
| **Pause**     | When status = _Active_                        | Temporarily halts the reward from being distributed.                                       |
| **End**       | When status = _Active_ or _Paused_            | Stops the reward and marks it as ended.                                                    |
| **Archive**   | When status = _Paused_, _Ended_, or _Expired_ | Moves the reward to the archived state; it cannot be reused in active campaigns.           |
| **View JSON** | When status = _Active_ or _Paused_            | View reward details, including ctRewardID, rewardName, description, and creation metadata. |

# Self-Managed Wallets Tab

The **Self-Managed Wallets** tab enables you to configure and manage wallet-based reward configurations. These wallets represent external reward systems, such as cashback or loyalty wallet credits hosted on your end.

Clicking on this tab displays wallet configurations in a card view format. Each card contains the following:

- Webhook Wallet ID
- CT Reward ID
- Wallet Name
- Created By
- Created On

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc52af03376cf3d06058c5de3128d572d46e703e0bfea7686d5c3c224d7a3859-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


## Manage Self-Managed Wallets

You can perform the following operations to manage wallets directly from the tab:

| Action        | Description                                | Description                                                                      |
| :------------ | :----------------------------------------- | :------------------------------------------------------------------------------- |
| **Activate**  | When status = _Paused_                     | Resumes the wallet for credits distribution.                                     |
| **Pause**     | When status = _Active_                     | Temporarily halts the wallet from credit distribution.                           |
| **End**       | When status = _Active_ or _Paused_         | Stops the wallet and marks it as ended.                                          |
| **Archive**   | Deactivate the wallet if no longer needed. | Moves the wallet to the archived state; it cannot be reused in active campaigns. |
| **View JSON** | When status = _Active_ or _Paused_         | View wallet details, including ctRewardID, walletID, and walletName.             |

> 📘 Notes
> 
> To ensure smooth management and consistent behavior across all reward types, keep the following points in mind:
> 
> - Rewards and wallets can be linked to multiple Promo campaigns.
> - Each reward and wallet credit is assigned a unique CleverTap Reward ID upon creation.
> - Rewards cannot be paused, ended, or archived while actively mapped to an ongoing campaign.
> - Inline validation ensures field accuracy and prevents duplication of reward or wallet IDs.