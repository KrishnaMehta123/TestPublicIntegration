---
title: Promo Campaign Stats
excerpt: >-
  Understand how Promo Campaign Stats provide clear, reward-specific insights
  into user engagement, reward distribution, and redemption trends through KPIs
  and time-based charts.
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

The **Rewards Distribution** tab under Promo Campaign Stats provides a comprehensive overview of Promo campaign performance, displaying real-time and historical analytics for user engagement, reward distribution, and redemption activity. The metrics and charts displayed depend on the _Reward type_ selected when creating the campaign.

Each reward type includes:

* Key Performance Indicators (KPIs) for campaign outcomes.
* Interactive charts visualizing trends over time.
* Date filters to customize your analysis by day, week, or month.

<Callout icon="📘" theme="info">
  #### Note

  The Campaigns with the Past Behavior Segments show total metrics only (no time-based charts), while Campaigns with the Live Behavior Segments include both total metrics and interactive, time-based performance graphs.
</Callout>

# Loyalty Points Campaign Stats

Loyalty Points campaigns display wallet-based reward performance and the total number of points distributed. These KPIs help you assess the frequency of rewards and the overall point volume during the campaign as follows:

* **Rewards Distributed**: Represents the total number of times a reward was distributed during the campaign. For example, if rewards were triggered multiple times for the same user, each instance is counted toward the total.
* **Points Distributed**: Indicates the total number of loyalty points issued to all qualifying users. For example, a total of 6,132 loyalty points were distributed.

<Image align="center" border={true} caption="KPIs for Promo Campaign with Loyalty Wallet Rewards" src="https://files.readme.io/7bbbd5a59eb1604a797ef115f65e89fe0db97a47a8ac64793961116be082cd31-image.png" />

## View Trends

The _Loyalty Wallets_ rewards KPIs also include two line charts that show how reward distribution changed throughout the campaign. These charts help you visually identify patterns such as high-engagement days, reward spikes, or periods of inactivity. For example, if users were rewarded on multiple days, the charts show recurring spikes corresponding to the distribution of rewards and points.

* **Rewards Distributed**: This line chart illustrates the frequency of rewards issued on each day, week, or month within the selected date range.

  * **X-axis**: Represents the Date or Month for the selected duration.
  * **Y-axis**: Represents the total number of rewards distributed during that period.
    You can aggregate chart data by Day, Week, or Month using the dropdown in the top-right corner of the chart. When you hover over any data point, the chart displays:
  * The exact number of rewards distributed for that period, and
  * The percentage change compared to the previous period (Day/Week/Month based on the selected aggregation).

<Image align="center" border={true} caption="Rewards Distributed Over Time in Loyalty Wallets" src="https://files.readme.io/0099b8772a477101867024a8c5f4247eafe3f64bd9932c39b712c6117d6732fb-image.png" />

* **Points Distributed**: This line chart illustrates the number of loyalty points issued on each date within the campaign range, as well as distribution trends, such as reward bursts on high-activity days or consistent distribution throughout the campaign.

<Image align="center" alt="Points Distributed Over Time in Loyalty Wallets" border={true} caption="Points Distributed Over Time in Loyalty Wallets" src="https://files.readme.io/6d2e0f2c8a263c3755b20a527328bdeb2bbb41749ae1dffbccf064c12da2e4a7-image.png" />

# Coupon Campaign Stats

Coupon campaigns help you track how coupons are issued and redeemed over time, providing visibility into user engagement and the financial impact of discounts or cashback rewards delivered.

The _Rewards Distribution_ tab adapts based on the Coupon Type (Single Code or Bulk Code) and the Coupon Benefit (Discount or Cashback). Only relevant KPIs and charts are displayed.

The KPIs in this section help you understand how frequently coupon rewards were issued, how coupons were distributed, and the total value redeemed by users.

* **Rewards Distributed**: Represents the total number of times a coupon reward was issued during the campaign. Each reward trigger is counted, including repeat rewards issued to the same user.

* **Coupons Distributed**: Indicates how coupon codes were distributed, based on the type of coupon used in the campaign.

  * **Single Code Coupon**: Shows the number of times the same coupon code was shared with users.
  * **Bulk Code Coupon**: Shows how many unique coupon codes from the bulk series were distributed. Each campaign trigger assigns a new code to the user.

* **Discount Redeemed**: Applicable only for discount coupons, this KPI shows the total value of discounts redeemed using coupons issued by the campaign.

<Image align="center" border={true} caption="KPIs for Promo Campaigns with Coupon Rewards" src="https://files.readme.io/f9d21685c45fb6d2761947cb6de699685f90106148397936392fa326f62bade7-image.png" />

* **Cashback Points Credited**: Applicable only to cashback coupons, this KPI shows the total number of cashback points credited to users’ wallets from coupon redemptions. For example, the campaign may show **5,000 cashback points credited** during the selected period.

<Image align="center" border={true} caption="Cashback Points Credited KPI for Cashback Coupon Types" src="https://files.readme.io/2fe7319573af245958699e24da8b6dc7b772d0c677f99c071bc27b3efa59182a-image.png" />

# Partner Voucher Campaign Stats

Partner Voucher campaigns track the distribution of unique voucher codes sourced from external providers. These analytics help you understand how many vouchers were issued and how distribution patterns changed over time.

The KPIs for Partner Voucher campaigns help you track the number of voucher codes assigned and overall engagement with voucher rewards.

* **Rewards Distributed**: Includes a line chart that displays voucher distribution patterns over time. This helps you analyze days with higher voucher issuance and spot trends or anomalies in campaign performance. For example, a spike on a specific date indicates higher voucher issuance compared to surrounding days.
* **Voucher Codes Distributed**: Indicates the total number of partner voucher codes assigned to users during the campaign.

<Image align="center" border={true} caption="KPIs for Promo Campaigns with Partner Voucher Rewards" src="https://files.readme.io/a53f44e93a25ebc9c4c278c31eb483bd8140a68c19a9c64ee3a8b0ba34db8f7c-image.png" />

## View Trends

This _Voucher Codes Distributed_ chart illustrates the distribution of voucher codes across each day, week, or month within the selected date range. It provides a clear view of distribution frequency and peak issuance dates.

<Image align="center" border={true} caption="Vouchers Distributed Over Time in Partner Vouchers" src="https://files.readme.io/9db18f74caff43027141697e3a2a0188d895c1b67b90e3128782d4c1a56f3f75-image.png" />

# Custom Rewards Campaign Stats

Custom Rewards campaigns rely on webhook calls to deliver rewards, such as wallet credits, digital items, or third-party payouts. The _Rewards Distributed_ tab displays the number of webhook-triggered rewards that succeeded, were sent, or failed.

The KPIs in this section help you evaluate webhook performance and identify any system-level issues that may impact reward delivery.

* **Webhook Credits Rewarded**: Represents the total credits successfully issued through webhook calls when _Self-Managed Wallet Credits_ are used as the reward type. This KPI does not apply to _Physical & Digital Rewards_.
* **Webhook Sent**: Indicates the total number of webhook requests triggered from CleverTap to the external endpoint.
* **Webhook Failed**: Shows the number of webhook requests that failed due to issues such as endpoint failures, timeouts, or invalid payloads.

<Image align="center" border={true} caption="KPIs for Promo Campaigns with Custom Rewards" src="https://files.readme.io/8715ca9cc75e88be4302d5ff0ae6d9575e601b9a2069b68111f17883c479af06-image.png" />
