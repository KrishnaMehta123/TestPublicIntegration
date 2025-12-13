---
title: Create Promo Campaigns
excerpt: >-
  Learn how to create and configure a Promo Campaign from scratch using the
  step-by-step campaign builder.
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

This document provides detailed instructions on creating and configuring a Promo Campaign using the Campaign Builder. It guides you through the key steps to set up your campaign, including defining your campaign goals, selecting the right target audience, choosing the campaign type, and customizing your settings.

# Create Promo Campaign

Go to _Promotions_ > _Promo Campaigns_ and click **Create Campaign**. The _New Promotion Campaign_ page opens. To create a Promo Campaign, perform the following five key steps:

1. [Define Qualification Criteria](doc:create-promo-campaigns#define-qualification-criteria)
2. [Select Target Segment](doc:create-promo-campaigns#select-target-segment)
3. [Set Up Reward](doc:create-promo-campaigns#set-up-reward)
4. [Set Up Delivery Preference](doc:create-promo-campaigns#set-up-delivery-preferences)
5. [Publish Campaign](doc:create-promo-campaigns#publish-campaign)

## Define Qualification Criteria

The _Start Here_ section is where you choose how users will qualify for the reward. The qualification criteria provide the following options:

- **Past behavior/Custom list**: Target users based on actions performed in the past or a custom list uploaded to the CleverTap dashboard. For example, you can target users who have not done a transaction in the last 6 months, and offer them a 20% discount coupon. 
- **Live behavior**: Trigger rewards in real-time when a user performs or does not perform an event. For example, you can trigger a reward when a user adds items to their cart but does not complete the checkout process within a set timeframe.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db8874c06fae7a9f98884e2d01a593742b44a052dc5bd6030f63527b1d42b607-image.png",
        null,
        "Define Qualification Criteria"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Qualification Criteria"
    }
  ]
}
[/block]


## Select Target Segment

The _Who_ section allows you to define who should receive the reward using the rule builder. The _Target Segment_ rule builder lets you select users from an existing saved segment or create a new segment using event and property-based rules as follows:

- **Find users from segment**: Select users from a saved segment or define a new one. 
- **Create rules based on events**: Build custom logic using event and property-based conditions
  - Users who **have done** specific events
  - Users who **have not done** certain events
  - Users who **have common user properties**, such as device type and location, are part of a particular segment, and so on. 
  - Users who **have common interests** or share common behavioral traits or usage patterns, such as frequent shoppers or high-engagement users.
- Option to enable **Constant event property**, which keeps event property values fixed during evaluation. It is useful when comparing multiple events with shared attributes. For example, you can lock the Product ID property across both events to find users who viewed and purchased the same product.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0f72135336ae3b88597f99adb1a424fad8b23e8c8d814927a28548d3ef4853c-image.png",
        null,
        "Select Target Segment"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Target Segment"
    }
  ]
}
[/block]


## Set Up Reward

The **What** section allows you to define the **reward type** for your Promo Campaign. Depending on your selection, the configuration options vary. CleverTap supports the following reward types:

- [Loyalty Points](doc:create-promo-campaigns#loyalty-points) 
- [Coupons](doc:create-promo-campaigns#coupons) 
- [Partner Vouchers](doc:create-promo-campaigns#partner-vouchers) 
- [Custom Rewards](doc:create-promo-campaigns#custom-rewards) 

## Set Up Delivery Preferences

The _When_ section defines when the campaign starts and ends, and the controls available vary based on whether you select a _Past Behavior Segment (PBS)_ or a _Live Behavior Segment_.

### For Past Behavior Segments or Custom List (PBS)

When you select Past Behavior or Custom List Segment, the _When_ section shows the following options:

| Option                 | Description                                                                                                                       | Example / Use Case                                                                  |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **Send Now**           | Launches the campaign immediately using the current timestamp and the **account timezone** (for example, GMT+05:30 Asia/Kolkata). | Run a flash-sale promotion as soon as it is configured.                             |
| **Schedule for Later** | Let's you choose a **future start date and time**. You can also adjust the timezone if required.                                  | Schedule a promo to start at 6:00 PM on a Friday evening to capture higher traffic. |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f64c9ea54de2ed6ec5e1f42297e4005d60be73e4dd7e6e07dd3364c20127b795-image.png",
        null,
        "Set Delivery Preferences"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Delivery Preferences in Past Behavior/Custom List Segments"
    }
  ]
}
[/block]


### For Live Behavior Segments

When you select Live Behavior Segment, the _When_ section shows the following options:

[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "h-2": "Example / Use Case",
    "0-0": "**Start Date and Time**",
    "0-1": "Choose when the campaign should start.  \n**Now**: Launches the campaign immediately after publishing.  \n**On a Date/Time**: Launches the campaign at a scheduled date and time.",
    "0-2": "Start the live campaign immediately to capture ongoing cart abandonment events, or schedule it to go live on the morning of a sale day.",
    "1-0": "**End Date and Time**",
    "1-1": "Choose when the campaign should stop.<ul><li>**Never**: Campaign keeps running until manually stopped.</li><li>**On a Date/Time**: Campaign automatically ends at a chosen date/time.</li>",
    "1-2": "End the campaign automatically at midnight on the final day of a seasonal sale."
  },
  "cols": 3,
  "rows": 2,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ac5f953cd43599b7d06b8532535fe1ae8871b5e900f4559687d0b0fa8bba8dfb-image.png",
        null,
        "Set Deliver Preference in Live Behavior Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Deliver Preference in Live Behavior Campaigns"
    }
  ]
}
[/block]


## Publish Campaign

Once you define all the above sections, click **Publish Campaign** to activate or schedule the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/208d31fed015df3703b4e35c6741ded52ecf1b99c62bfef9f5c085323a193ad1-image.png",
        null,
        "Publish Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]


# Reward Types

Each reward type includes different configuration settings, described in the sections below:

## Loyalty Points

Use Loyalty Points to incentivize users with loyalty points that can be accumulated and redeemed within your app or platform. This option requires that wallets be pre-created in your CleverTap account.

The following configuration options are available when Loyalty Points is selected:

[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "h-2": "Example / Use Case",
    "h-3": "Available In",
    "0-0": "**Loyalty wallet**",
    "0-1": "Select the wallet from the dropdown. Ensures that points are distributed to the correct wallet.",
    "0-2": "You can reward users based on context if you have multiple wallets (for example, Grocery vs. Food).",
    "0-3": "Past Behavior/Custom List + Live Behavior Segments",
    "1-0": "**Points earning scheme**",
    "1-1": "Define how points are calculated when users qualify. Options include:  \n**Flat**: A fixed number of points for each qualifying user.  \n**Percentage**: Points calculated as a percentage of an event property (for example, order amount).  \n**Proportional**: Points awarded per defined unit of an event property.  \n**Random**: Points assigned from a defined range; exposes Value Range + Distribution Bias controls.",
    "1-2": "**Flat**: Every eligible user earns 100 points regardless of order amount.  \n**Percentage**: If set to 10% of the amount, a ₹500 purchase earns 50 points.  \n**Proportional**: For every ₹100 spent, the user gets 10 points.  \n**Random**: Users earn between 10 and 50 points, with distribution bias favoring the average.",
    "1-3": "**Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior segments.  \n**Percentage** and **Proportional**: Available only in Live Behavior segments",
    "2-0": "**Points value**",
    "2-1": "The input control for Points value changes based on the selected Points Earning Scheme:  \n**Flat**: Enter a single fixed value of points/credits awarded to each qualifying user.  \n**Percentage**: Define a percentage of a selected event property (for example, order amount) from the qualifying event (typically a Charged event).  \n**Proportional**: Define “points per unit” of a selected event property (for example, for every X units of the property, award Y points).  \n**Random**: Set a min–max range of points/credits; the system randomly selects a value within this range for each qualifying user (also supports Distribution Bias).",
    "2-2": "**Flat**: Set to 100 means every qualifying user gets 100 credits.  \n**Percentage**: Set to 10% means a purchase of ₹500 (as per selected event property) gives 50 credits.  \n**Proportional**: Set to 10 credits for every Rs. 100 (per selected event property).  \n**Random**: Set to a range of 10–100 means each qualifying user gets a random value between 10 and 100.",
    "2-3": "**Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior Segment.  \n**Percentage** and **Proportional**: Available only in Live Behavior campaigns.",
    "3-0": "**Distribution bias** (For Random scheme only)",
    "3-1": "Control distribution pattern that allows you to select the following options:  \n**Favor Min**: Skews distribution toward the lower end of the range.  \n**Favor Avg**: Skews distribution toward the midpoint of the range.  \n**Favor Max**: Skews distribution toward the higher end of the range.",
    "3-2": "**Favor Min**: For a range of 10–100 points, most users receive lower values (for example, 10–30), while fewer receive higher values.  \n**Favor Avg**: For a range of 10–100 points, most users receive values around the midpoint (for example, ~55), with fewer at the extremes.  \n**Favor Max**: For a range of 10–100 points, most users receive higher values (for example, 70–100), while fewer receive lower values.",
    "3-3": "Past Behavior/Custom List + Live Behavior Segments",
    "4-0": "**Max points per reward**",
    "4-1": "Define the maximum number of points that can be awarded in a single transaction or instance. Applicable only when using **Percentage** or **Proportional** earning schemes in Live Behavior campaigns. Not available for **Flat** or **Random** schemes.",
    "4-2": "Cap points at 500 per purchase, even if the % calculation exceeds this value.",
    "4-3": "Live Behavior Segments",
    "5-0": "**Maximum recurrence per user**",
    "5-1": "Control how many times a single user can receive the reward. Multiple limits can be combined (for example, total + per day/week/month).",
    "5-2": "If the total limit is 5 and the per-day limit is 2, the user can receive the reward up to two times per day until they reach a total of 5 rewards.",
    "5-3": "Live Behavior Segments only",
    "6-0": "**Custom points validity**",
    "6-1": "Define the activation and expiry lifecycle of awarded points.",
    "6-2": "**Activation**: Immediate (points instantly usable) OR Custom delay (for example, activate after 7 days).  \n**Expiry**: Never, fixed date, or custom duration (for example, 30 days after activation).",
    "6-3": "Past Behavior/Custom List + Live Behavior Segments",
    "7-0": "**Budget**",
    "7-1": "Define the budget to control how rewards are distributed. Budget can be set at two levels:  \n**Per Campaign Budget**: Caps the total rewards that the campaign can distribute.  \n**Per User Budget**: Caps the maximum rewards a single user can receive during the campaign.  \nOnce the defined limit is reached (per user or for the entire campaign), no further rewards are issued.",
    "7-2": "If the Per Campaign Budget is 5,000 points, rewards stop once the campaign collectively distributes 5,000 points, even if more users qualify.  \nIf the Per User Budget is 500 points, each user can only receive up to 500 points during the campaign, even if they continue qualifying.",
    "7-3": "Live Behavior Segments only",
    "8-0": "**Custom metadata**",
    "8-1": "Add dynamic key–value pairs to pass additional data into the wallet points payload. Each row has two modes:  \n**System Key**: Select from predefined system keys.  \n**Custom Key**: Define your own key. <br>Duplicate keys are not allowed.",
    "8-2": "Add `{ \"orderId\": \"12345\", \"promoType\": \"festival\" }` as custom metadata to track order-related rewards.",
    "8-3": "Past Behavior/Custom List + Live Behavior Segments"
  },
  "cols": 4,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


> 📘 Points to Consider
> 
> - Custom Activation does not check user behavior. It delays redemption so businesses can increase net profit on orders.
> - Wallet must be pre-configured in your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d437eec9f1f394b546d51406d53ff000e37dfdcf458a6ec637b06d8f1ced0fb-image.png",
        null,
        "Set Up Loyalty Points in Rewards"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Loyalty Points in Rewards"
    }
  ]
}
[/block]


## Coupons

Use Coupons to provide users with discount codes or special offers. Coupons must be pre-created in CleverTap and active.

The following configuration options are available when Coupons is selected:

[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "h-2": "Example / Use Case",
    "h-3": "Available In",
    "0-0": "**Coupon Type**",
    "0-1": "Choose Single Code (shared) or Bulk Codes (unique).",
    "0-2": "**Single Code:** A fixed 20% off coupon shared with all users.  \n**Bulk Codes:** Each user gets a unique 10% off coupon.",
    "0-3": "Past Behavior/Custom List + Live Behavior Segments",
    "1-0": "**Coupon code**",
    "1-1": "Select from available coupons that match the type. Coupon must be active and not fully redeemed.",
    "1-2": "Dropdown lists valid Single or Bulk codes.",
    "1-3": "Past Behavior/Custom List + Live Behavior Segments",
    "2-0": "**Max coupons per user**",
    "2-1": "Defines how many times the coupon can be rewarded to the same user. This does not control redemption. If a user-level redemption limit is 2 and the same coupon is rewarded twice, user can redeem 4 times total.",
    "2-2": "Selecting _Limit = 1_ means each user can only be rewarded the coupon once.",
    "2-3": "Live Behavior Segments only",
    "3-0": "**Max coupons per campaign**",
    "3-1": "Defines the total number of coupon codes that the campaign can distribute.",
    "3-2": "Selecting _Limit = 1000_ means the campaign stops distributing coupons after 1000 coupons are issued.",
    "3-3": "Live Behavior Segments",
    "4-0": "**Coupon redemption activation**",
    "4-1": "Define when coupons can be redeemed, immediately or after a custom delay.",
    "4-2": "**Immediate:** Flash sale means redeem instantly.  \n**Custom:** Redeemable 48 hours after reward assignment.",
    "4-3": "Past Behavior/Custom List + Live Behavior Segments"
  },
  "cols": 4,
  "rows": 5,
  "align": [
    null,
    null,
    null,
    null
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/362ace8d3ea7a677c7c9a93f885bd75dbd8db80a5f74fc2fda32e1de4b2c66ca-image.png",
        null,
        "Set Up Coupons in Rewards"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Coupons in Rewards"
    }
  ]
}
[/block]


## Partner Vouchers

Use Partner Vouchers to distribute unique codes provided by third-party providers integrated with your account.

The following configuration options are available when Partner Vouchers is selected:

| Option                     | Description                                                                                                                                                                                                         | Example / Use Case                                                                                      | Available In                                       |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------ | :------------------------------------------------- |
| **Partner**                | Select from integrated and active voucher providers.                                                                                                                                                                | Pick Amazon Gift Cards provider.                                                                        | Past Behavior/Custom List + Live Behavior Segments |
| **List tag**               | Select the voucher batch (list tag) for distribution. Codes are auto-assigned uniquely to users.                                                                                                                    | Batch _Holiday2025_ with 10,000 gift codes.                                                             | Past Behavior/Custom List + Live Behavior Segments |
| **Max codes per user**     | Defines how many times the voucher can be rewarded to the same user. This does not control redemption. If a user-level redemption limit is 2 and the same voucher is rewarded twice, user can redeem 4 times total. | Selecting _Limit = 1_ means each user can only be rewarded the voucher once.                            | Live Behavior Segments only                        |
| **Max codes per campaign** | Defines the total number of voucher codes that the campaign can distribute.                                                                                                                                         | Selecting _Limit = 1000_ means the campaign stops distributing vouchers after 1000 vouchers are issued. | Live Behavior Segments                             |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ede864217cd7dc80e936bad3e1ea62efb4de25939eca23a041f1d8f2aa1126e-image.png",
        null,
        "Set Up Partner Vouchers in Rewards"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Partner Vouchers in Rewards"
    }
  ]
}
[/block]


> 📘 Note
> 
> - Only active, unexpired voucher lists are displayed.
> - No preview of voucher details is available.
> - System ensures each user receives a unique, unused code.

## Custom Rewards

Use Custom Rewards to integrate external reward systems. When a user qualifies, CleverTap triggers a webhook call to your configured endpoint, enabling you to issue rewards such as third-party gift cards, credits, or custom incentives.

The following configuration options are available when Custom Rewards is selected:

[block:parameters]
{
  "data": {
    "h-0": "Option",
    "h-1": "Description",
    "h-2": "Example / Use Case",
    "h-3": "Available In",
    "0-0": "**Webhook endpoint (mandatory)**",
    "0-1": "Select a pre-configured webhook endpoint from the dropdown. If none exist, click the link provided to add a new configuration.",
    "0-2": "Connect to an external gift card provider API endpoint.",
    "0-3": "Past Behavior/Custom List + Live Behavior Segment",
    "1-0": "**Custom reward type**",
    "1-1": "Select whether to issue Physical & digital rewards (tangible gifts) or Self-managed wallet credits (monetary/credit-based).",
    "1-2": "Physical & digital: Send a Bluetooth speaker as a gift.  \nSelf-managed: Credit ₹200 to a user’s wallet.",
    "1-3": "Past Behavior/Custom List + Live Behavior Segment",
    "2-0": "**Physical & digital rewards**",
    "2-1": "Choose a reward that must be pre-created in your account.",
    "2-2": "Select “Amazon Voucher” or “Smartwatch”.",
    "2-3": "Past Behavior/Custom List + Live Behavior Segment",
    "3-0": "**Max recurrence per user**",
    "3-1": "Allows you to control how many rewards can be granted per user on a daily, weekly, or monthly basis.",
    "3-2": "Max per user = 1 reward in a week",
    "3-3": "Past Behavior/Custom List + Live Behavior Segment",
    "4-0": "**Self-managed wallet credits**",
    "4-1": "Choose a wallet from the dropdown (must be pre-created).",
    "4-2": "Select a wallet to reward credits or money.",
    "4-3": "Past Behavior/Custom List + Live Behavior Segment",
    "5-0": "**Credits earning scheme** (only for Self-managed wallet credits)",
    "5-1": "Choose how to define wallet credits. Options include:  \n**Flat**: a fixed number of credits for each qualifying user.  \n**Percentage**: credits calculated as a percentage of an event property (for example, order amount).  \n**Proportional**: credits awarded per defined unit of an event property (for example, 10 credits per ₹100 spent).  \n**Random**: credits assigned from a defined range; exposes Value Range + Distribution Bias controls.",
    "5-2": "**Flat**: All qualifying users get 100 credits.  \n**Percentage**: 10% of ₹500 purchase, i.e., 50 credits.  \n**Proportional**: 10 credits for every ₹100 spent.  \n**Random**: Users get between 10–100 credits.",
    "5-3": "**Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior segments.  \n**Percentage** and **Proportional**: Only available in Live Behavior campaigns (not supported in PBS).",
    "6-0": "**Value**",
    "6-1": "The input control for the credits value changes based on the selected credits Earning Scheme:  \n**Flat**: Enter a single fixed value of credits awarded to each qualifying user.  \n**Percentage**: Define a percentage of a selected event property (for example, order amount) from the qualifying event (typically a Charged event).  \n**Proportional**: Define “credits per unit” of a selected event property (for example, for every X units of the property, award Y credits).  \n**Random**: Set a min–max range of credits; the system randomly selects a value within this range for each qualifying user (also supports Distribution Bias).",
    "6-2": "**Flat**: Set to 100 means every qualifying user gets 100 credits.  \n**Percentage**: Set to 10% means a purchase of ₹500 (as per selected event property) gives 50 credits.  \n**Proportional**: Set to 10 credits for every ₹100 (as per selected event property).  \n**Random**: Set to a range of 10–100 means each qualifying user gets a random value between 10 and 100.",
    "6-3": "**Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior Segment.  \n**Percentage** and **Proportional**: Available only in Live Behavior campaigns.",
    "7-0": "**Distribution bias** (For Random scheme only)",
    "7-1": "Control distribution pattern that allows you to select the following options:  \n**Favor Min**: skews distribution toward the lower end of the range.  \n**Favor Avg**: skews distribution toward the midpoint of the range.  \n**Favor Max**: skews distribution toward the higher end of the range.",
    "7-2": "**Favor Min**: For a range of 10–100 credits, most users receive lower values (for example, 10–30), while fewer receive higher values.  \n**Favor Avg**: For a range of 10–100 credits, most users receive values around the midpoint (for example, ~55), with fewer at the extremes.  \n**Favor Max**: For a range of 10–100 credits, most users receive higher values (for example, 70–100), while fewer receive lower values.",
    "7-3": "Past Behavior/Custom List + Live Behavior Segments",
    "8-0": "**Max credits per rewards** (only for Percentage and Proportional schemes)",
    "8-1": "Enter the maximum credits per reward.",
    "8-2": "Setting 100 means each user can get a maximum of 100 credits per reward.",
    "8-3": "Past Behavior/Custom List + Live Behavior Segment",
    "9-0": "**Max recurrence per user**",
    "9-1": "Allows you to control how many rewards can be granted per user on a daily, weekly, or monthly basis.",
    "9-2": "Max per user = 1 reward in a day",
    "9-3": "Past Behavior/Custom List + Live Behavior Segment",
    "10-0": "**Budget**",
    "10-1": "Defines how many rewards can be distributed.  \n**Physical & digital rewards**: Supports campaign-level and time-based limits.  \n**Self-managed wallet credits**: Supports per-campaign and per-user limits (varies by scheme). **Flat**: Supports Per Campaign budget only.  \n**Percentage**: Supports both Per Campaign and Per User budgets.  \n**Proportional**: Supports both Per Campaign and Per User budgets.  \n**Random**: Supports both Per Campaign and Per User budgets.</ul>",
    "10-2": "**Physical & digital rewards**:  \nCampaign limit = 5,000 vouchers; additionally, set 1,000 vouchers per month.  \n**Self-managed  wallet credits**:  \n**Flat Credits**: Campaign limit = 10,000 credits.  \n**Percentage Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.  \n**Proportional Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.  \n**Random Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.",
    "10-3": "Past Behavior/Custom List + Live Behavior Segment",
    "11-0": "**User identifiers key mapping**",
    "11-1": "Map CleverTap’s default user identity fields (User ID, Email address, Phone number) to your webhook payload keys. Each field supports the following modes: System key (CleverTap’s default field names) or Custom key (specify your own key names).",
    "11-2": "Map CleverTap’s identity field to your external system’s customerId or use default mapping for email and phone.",
    "11-3": "Past Behavior/Custom List + Live Behavior Segment",
    "12-0": "**Custom metadata**",
    "12-1": "Add dynamic key-value pairs to include contextual data in the reward payload. Duplicate keys are not allowed.",
    "12-2": "Add `{ \"orderType\": \"electronics\", \"promoType\": \"festival\" }` as custom metadata to track order-related rewards.",
    "12-3": "Past Behavior/Custom List + Live Behavior Segments",
    "13-0": "**Preview JSON Payload**",
    "13-1": "Displays a live JSON preview that includes reward metadata and configured key-value parameters.",
    "13-2": "For example, refer to [JSON Payload](doc:create-promo-campaigns#json-payload)",
    "13-3": "Past Behavior/Custom List + Live Behavior Segment"
  },
  "cols": 4,
  "rows": 14,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/539ebea5210050327666ff4ed929383317200eb806d0ab85a7d1fa1ccd95f621-image.png",
        null,
        "Set Up Reward in Custom Rewards"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Reward in Custom Rewards"
    }
  ]
}
[/block]


> 📘 **Points to Consider**
> 
> Before you begin:
> 
> - Ensure you configure the webhook endpoint before creating the campaign.
> - Verify that the endpoint can handle campaign volume, retries, and logging.
> 
> During setup:
> 
> - Physical & Digital Rewards and Self-managed Wallet Credits have separate configuration options; choose the appropriate type based on your use case.
> - The reward payload is fully customizable and scales automatically with campaign volume.
> - Custom Rewards give maximum flexibility but require your external system to handle issuance and redemption.

<JSONPayloadForCustomRewards />

# Best Practices

Maximize campaign effectiveness and avoid common pitfalls with the following best practices for setup, execution, and management:

- **Use Segments Wisely**: Tailor rewards with meaningful segmentation.
- **Test Before Scaling**: Start small to validate campaign performance.
- **Set Limits**: Always define per-user and per-campaign limits. 
- **Reward Inventory**: Ensure sufficient reward stock throughout the campaign.