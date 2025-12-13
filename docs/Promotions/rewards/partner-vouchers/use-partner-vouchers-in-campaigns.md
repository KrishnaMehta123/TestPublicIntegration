---
title: Use Partner Vouchers in Campaigns
excerpt: >-
  Learn how to engage users using the CT Partner Voucher Rewarded event and
  drive conversions.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Engage with Voucher Assigned Users

CleverTap allows you to target users who have received a voucher by creating a campaign based on the *CT Partner Voucher Rewarded* event. This event helps personalize communication and drive users toward completing a desired action, such as making a purchase or redeeming an offer.

For example, suppose you are a food delivery app that wants to increase redemption rates on the app. Let's say you want to remind users who received a discount voucher but have not redeemed it yet. You can set up a campaign as follows:

1. Go to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the *Messaging Channels* dropdown.
3. Click **Add an event** from the *Who* section.
4. Select the *CT Partner Voucher Rewarded* event and the required *Event Property*.

<Image alt="Target Users with a Campaign/Journey" align="center" border={true} src="https://files.readme.io/fcb5f165b05a8e274d0810b66f096cdcebeb48b95b8da4a48fe07d0bfa1d6dcd-CT_Partner_Voucher_Rewarded.png">
  Target Users with a Campaign/Journey
</Image>

For more information about creating a campaign, refer to the *Create Message* document of the respective messaging channel.

# CT Partner Voucher Rewarded

After a voucher is assigned to a user, CleverTap triggers the *CT Partner Voucher Rewarded* event. This event enables you to engage users by creating targeted campaigns based on voucher-related actions.

The event includes the following System and Custom event properties, which help you track and personalize user engagement strategies:

## System Event Property

| Property    | Description                                                      | Example Value  |
| ----------- | ---------------------------------------------------------------- | -------------- |
| `CT Source` | Identifies the source system or module that triggered the event. | `Promo Module` |

## Custom Event Properties

| Property          | Description                                                                                                                                                |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `campaignId`      | The unique identifier of the campaign through which the voucher was distributed. For example, CMP123456.                                                   |
| `eventTimestamp`  | The exact time when the voucher was assigned to the user. For example, 1708351200.                                                                         |
| `listDescription` | A brief description of the voucher list, typically outlining its purpose or restrictions. For example, *Winter Sale 2024 - ₹500 off on orders above ₹2000* |
| `listExpiry`      | The expiration date of the voucher list, after which no more vouchers from this list can be assigned. For example, `2024-03-31T23:59:59Z`                  |
| `listTag`         | A short, unique identifier for the voucher list, used to categorize vouchers within CleverTap. For example, `winter_sale_500`.                             |
| `partner`         | The name of the voucher provider. For example, `Puma`                                                                                                      |
| `source`          | The origin of the voucher assignment. For example, Campaign or API.                                                                                        |
| `voucherCode`     | The unique code assigned to the user for redemption. For example, `PM500FF`                                                                                |
| `voucherListId`   | The unique identifier of the voucher list to which the assigned voucher belongs. For example, `1837`                                                       |

These properties can be leveraged in Liquid Tags to personalize messages, enabling dynamic content in your engagement campaigns.
