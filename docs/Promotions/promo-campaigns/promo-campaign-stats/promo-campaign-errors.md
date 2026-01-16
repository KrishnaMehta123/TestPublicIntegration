---
title: Promo Campaign Errors
excerpt: >-
  Review reward distribution issues in Promo campaigns to understand error
  patterns and root causes.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

The **Errors** tab displays all failed reward distribution attempts for a Promo campaign. It helps you understand why a reward could not be issued, how often each error occurs, and whether limits, configurations, or system-level failures affected campaign performance.

These errors also help you:

* Diagnose reward delivery failures.
* Verify whether limits such as user-level, campaign-level, or redemption limits are being reached.
* Identify configuration issues with wallets, coupons, vouchers, or reward setups.
* Detect system-level failures such as assignment failures, _parsing errors_, or _inactive reward systems_.

By monitoring these errors, you can take targeted actions, such as updating reward configurations, increasing budgets, replacing exhausted code lists, or troubleshooting webhook integrations.

This tab is available for all campaign types and displays historical error logs for the selected date range.

<Image align="center" border={true} caption="Promo Campaign Errors" src="https://files.readme.io/b4306397c0fc8c480f018c5ab3b411f7bce911d99d7f38ee60870b4c142cdccb-image.png" />

# Total Errors

At the top of the **Errors** tab, the total number of failed reward distributions for the campaign is displayed. If no errors have occurred, the page displays an empty state, indicating that the campaign is running without any reward distribution issues.

Errors vary depending on the reward type selected in the campaign:

* [Loyalty Wallet Errors](doc:promo-campaign-errors#loyalty-wallet-errors)
* [Coupon Errors](doc:promo-campaign-errors#coupon-errors)
* [Partner Voucher Errors](doc:promo-campaign-errors#partner-voucher-errors)

## Loyalty Wallet Errors

The following errors may occur when distributing _Loyalty Points_ through a wallet.

| Error Type                                  | Description                                                                                     |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Invalid wallet configuration**            | Reward ID or wallet details are invalid.                                                        |
| **Inactive user wallet**                    | User’s wallet is inactive or does not exist.                                                    |
| **Invalid points calculated**               | Calculated points are less than 0 or not a numeric value.                                       |
| **User’s reward recurrence limit exceeded** | User has already been rewarded the maximum number of times allowed per user from this campaign. |
| **Campaign’s points budget exceeded**       | Campaign has reached the maximum points distribution budget.                                    |
| **User’s points budget exceeded**           | User has already been rewarded the maximum number of points allowed per user in this campaign.  |
| **Points credit failed**                    | Failed to credit points due to a system error.                                                  |

## Coupon Errors

The following errors may occur for _Single Code_ or _Bulk Code_ coupon rewards.

| Error Type                                  | Description                                                                     |
| ------------------------------------------- | ------------------------------------------------------------------------------- |
| **Invalid coupon configuration**            | Reward ID or coupon details are invalid.                                        |
| **Inactive coupon**                         | Coupon has expired or is inactive.                                              |
| **Campaign’s coupon limit exceeded**        | Campaign has reached the maximum number of coupons that can be rewarded.        |
| **User’s coupon limit exceeded**            | User has reached the maximum coupon rewards allowed per user for this campaign. |
| **Codes from bulk coupon series exhausted** | All possible codes from the bulk series have been distributed.                  |
| **Coupon redemption limit exceeded**        | Coupon has reached its maximum redemption limit.                                |
| **Coupon assignment failed**                | Failed to assign a coupon due to a system error.                                |

## Partner Voucher Errors

The following errors may occur when the reward type is a _Partner Voucher List_.

| Error Type                                 | Description                                                                      |
| ------------------------------------------ | -------------------------------------------------------------------------------- |
| Invalid voucher configuration              | Reward ID or voucher details are invalid.                                        |
| Inactive voucher list                      | Voucher list has expired or is inactive.                                         |
| **Campaign’s voucher code limit exceeded** | Campaign has reached the maximum number of vouchers that can be rewarded.        |
| _**User’s voucher code limit exceeded**_   | User has reached the maximum voucher rewards allowed per user for this campaign. |
| **Codes from voucher list exhausted**      | All codes from the uploaded voucher list have been distributed.                  |
| **Voucher code assignment failed**         | Failed to assign voucher code due to a system error.                             |