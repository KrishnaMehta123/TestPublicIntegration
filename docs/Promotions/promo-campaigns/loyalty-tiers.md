---
title: Loyalty Tiers
excerpt: >-
  Learn how to set up loyalty tiers that automatically group users by activity,
  reward them at each level, and regularly re-evaluate eligibility using
  configurable expiry and downgrade rules.
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

Loyalty Tiers allow you to group users into different levels (tiers) based on their activity and reward them accordingly. As users engage more with your app by spending more, performing key actions, or earning points, they can progress to higher tiers and unlock enhanced benefits.

Common examples of tiers include airline loyalty tiers (Silver, Gold, Platinum), E-commerce membership levels (Bronze, Silver, Gold), and so on. Loyalty Tiers work seamlessly with Rewards such as [Loyalty Wallets](doc:loyalty-wallets), [Coupons](doc:coupons), [Partner Vouchers](doc:partner-vouchers), and [Custom Rewards](doc:custom-rewards) within CleverTap Promotions.

With Loyalty Tiers, you can:

* Automatically assign users to tiers based on their actions in the app
* Define clear upgrade and downgrade rules
* Reward users differently at each tier
* Control how long tiers remain valid
* Periodically re-evaluate user eligibility

<Callout icon="📘" theme="info">
  #### Note

  A Loyalty Tier system must include:

  * At least one tier upgrade parameter
  * At least one earned tier (beyond the default tier)
</Callout>

# Create Loyalty Tiers

To create Loyalty Tiers, go to _Promotions > Loyalty Tiers > Create Loyalty Tiers_ and select from the following options that best match the level of your loyalty tiers:

* [Program Details](doc:loyalty-tiers#program-details)
* [Tier Definition](doc:loyalty-tiers#tier-definition)
* [Tier Rewards](doc:loyalty-tiers#tier-rewards)
* [Qualification and Expiry](doc:loyalty-tiers#qualification-and-expiry)
* [Downgrade Policy](doc:loyalty-tiers#downgrade-policy)

## Program Details

This section includes the entry rules and upgrade signals for your loyalty tiers, defining who qualifies for each tier and which activities are tracked.

* **Tier System Name**: Enter a name to identify this tier system internally. For example,
  `Airmiles Plus`, `BlueChip Membership`
* **Existing Users Tier**: Choose how existing users should be handled when the tier system is created. Existing users can be placed in either the default tier or specific tiers based on available data. This ensures historical users are not excluded.
* **Default Tier Assignment**: Defines how users enter the tier system. Select an event that adds users to the default tier. For example, selecting the `Signup` event results in every user who signs up entering the tier system in the default tier. You can optionally apply filters to narrow eligibility.

<Image align="center" border={true} caption="Program Details" src="https://files.readme.io/29b8af172a7e49e79949468c402a295d7e72e831cf96cc0580698f787040d13f-image.png" />

* **Tier Upgrade Criteria**: Define which user activities are tracked to determine eligibility for higher tiers. These criteria act as the signals of loyalty or engagement that users must meet to progress through your tier hierarchy. You must add at least one upgrade criterion to create a tier system. Once defined, these criteria are reused when setting qualification rules for individual tiers in the Tier Definition section. Tier Upgrade Criteria do not decide _which tier_ a user belongs to by themselves. Instead, they define what data is available to build tier qualification rules.

<Image align="center" border={true} caption="Supported Criterion Types" src="https://files.readme.io/541c4699f2d96ab43f7b5c6f1f92bf6e38f7131a659ba88c33ad9f13a780285d-image.png" />

### Supported Criterion Types

You can track user activity using one or more of the following criterion types.

#### Count of an Event

Use this criterion to track how many times a specific event occurs for a user. This is best suited for measuring frequency-based engagement, such as how often users perform an action.

For example, if you select the `Order Placed` event, you can later define tier rules, such as:

* Users with 5 or more orders qualify for Silver
* Users with 15 or more orders qualify for Gold

#### Sum of an Event Property

Use this criterion to track the total value of a numeric property across multiple occurrences of an event. This is ideal for measuring value-based engagement, such as how much a user spends over time.

For example, if you select the `Order Placed` event and the `order_value` event property, you can later define tier rules such as:

* Users who have spent $1,000 or more qualify for Silver
* Users who have spent $4,000 or more qualify for Gold

#### Points Collected

Use this criterion to track a user's total loyalty points earned in a selected loyalty wallet. This is best suited for loyalty-driven tier progression, where users advance by actively earning points.

For example, if you select a `Rewards Wallet`, you can later define tier rules such as:

* Users who have earned **500 points** qualify for Silver
* Users who have earned **2,000 points** qualify for Gold

<Callout icon="📘" theme="info">
  #### Use Multiple Criteria Together

  You can define multiple upgrade criteria to capture different types of loyalty signals. These criteria can then be combined using OR logic when defining tier qualification rules.

  For example, a user qualifies for Silver if they meet any one of the following:

  * Placed 5 or more orders
  * Spent $1,000 or more
  * Earned 500 loyalty points

  This approach allows both high-frequency and high-value users to progress through tiers.
</Callout>

## Tier Definition

This section defines the tier hierarchy and the conditions users must meet to move up the ladder from the default tier to higher earned tiers.

### Tier 1 (Default Tier)

Tier 1 is the starting point for every user. Use this tier to offer entry-level benefits to new or low-engagement users while they work toward higher tiers.

* **Who starts here**: All users begin in the base tier by default.
* **Expiry behavior**: Default tiers are permanent and do not expire.
* **Where the entry rule comes from**: Entry criteria are defined in **Program Details** and cannot be edited in this section.

<Image align="center" border={true} caption="Default Tier" src="https://files.readme.io/bf475af9ba5184d746dac9febf471a5a7846b06a742ffe6d86103205657e0bc9-image.png" />

### Earned Tiers (Tier 2 and above)

Earned tiers represent higher tiers that users qualify for through activity. These tiers are typically where your users' benefits begin (for example, Silver, Gold, Diamond).

For each earned tier, configure the following:

* **Tier Name**: Enter the name of the tier. For example, `Silver`, `Gold`, and `Diamond`.
* **Tier Expiry**: Choose whether the tier:

  * **Does not expire**, or
  * **Expires** based on the evaluation rules you set later in _Qualification and Expiry_.
* **Tier Criteria**: Define what a user must do to qualify for this tier. You select from the upgrade criteria you already created in **Program Details**, and combine them using **OR** logic (meaning any one condition can qualify the user).

<Image align="center" border={true} caption="Example of a Tier 2" src="https://files.readme.io/a36e6e2225ee28d42c547880648ea5bda49654c300bb740281a0d298930d77e6-image.png" />

The following is an example of an earned tier:

A user qualifies for **Silver** if they meet any one of the following:

* Flights booked between 5 and 10 **OR**
* Total spend between ₹5,000 and ₹10,000 **OR**
* Points collected ≥ 500

If a user satisfies any of the defined conditions, they qualify for the tier.

## Tier Rewards

This section defines what users receive at each tier. Rewards are applied while users are in a tier, allowing you to differentiate benefits across the tier hierarchy.

### Default Tier Rewards

These are rewards given to users in the default (base) tier. Use these to provide basic benefits that help onboard or retain early-stage users. For example, reward the default users with basic wallet points or welcome coupons.

### Earned Tier Rewards

These rewards apply to users who qualify for higher tiers (such as Silver, Gold, or Diamond). Earned-tier rewards are usually more valuable and are designed to motivate continued engagement. Each tier can have its own reward configuration, allowing higher tiers to receive better or more exclusive benefits.

Supported reward types include:

* Wallet points
* Coupons
* Partner vouchers
* Custom rewards

### Adding a Reward

When you add a reward to a tier, you configure:

* **Reward type**: Select what you want to grant (wallet points, coupon, voucher, or custom reward).
* **Reward value**: Define the value or selection for the chosen reward type.
* **Expiry behavior**: Set how long the reward remains valid.

For **wallet points**, you can additionally configure:

* **Points type**: Choose whether points are awarded as fixed or random.
* **Points expiry**: Decide when points expire (never, when the tier expires, or on a custom date).

<Image align="center" border={true} src="https://files.readme.io/5b3866f894cb5e095255a25d0d0f755b8d2625d574e31ed3fb30951e8b9e7348-image.png" className="border" />

## Qualification and Expiry

This section controls two key parts of tier behavior:

1. How often users are evaluated, and
2. How long the tier benefits remain valid before a re-evaluation happens.

### Tier Expiry

Tier expiry determines when tier benefits expire and when users are re-evaluated for eligibility.

You can choose one of the following approaches:

* **Every Calendar Year**: All users are evaluated at the end of each calendar year. This evaluation is calendar-based, so a user’s tier entry date does not matter.
* **Custom Duration**: Users are evaluated after a fixed duration (for example, 12 months). The duration is calculated from when the user enters the tier.

### Qualification Period

The qualification period defines which user activity is considered during an evaluation. This determines what data is used to decide whether a user qualifies to stay in a tier, move up, or be downgraded. For example, evaluate user spend over the last 6 months, regardless of the user's tier entry date.

You can choose one of the following:

* **Within Tier Validity**: Only activity after the user entered the tier is considered.
* **Rolling Window**: Only activity within the selected time window is considered, and that window moves forward as time progresses.

<Image align="center" border={true} caption="Qualification and Expiry" src="https://files.readme.io/a222cc68ec165dcf5e9eee7fd0f5c5fda46498ccbe1a292b4617b596bc3f7ea2-image.png" />

## Downgrade Policy

This section defines what happens when users no longer qualify for their current tier. This happens either because their tier expires and they fail evaluation, or because they do not meet the qualification rules.

### Downgrade Options

Choose one of the following downgrade approaches:

* **Highest tier they qualify for**: Users are reassigned to the highest tier they still meet criteria for. If they do not qualify for any tier, they move to the default tier.
* **Next lower tier**: Users move down one tier at a time (for example, Gold > Silver > Bronze).
* **Default tier**: Users are moved directly to the default tier.

<Image align="center" border={true} caption="Downgrade Options" src="https://files.readme.io/a67004c477ee74edc9460a901e7e355936dd70b4af54880c15112e201b99a47e-image.png" />

# FAQs

Find answers to the frequently asked questions that you may have regarding Loyalty Tiers:

### Q. What’s the difference between the default tier and earned tiers?

The default tier is where all users start. It is permanent and does not expire. Earned tiers (Tier 2 and above) are for higher-tier users who qualify based on activity and can expire or be downgraded per your rules.

### Q. What is tier upgrade criteria and how is it different from Tier criteria?

* **Tier upgrade criteria** are the _signals you track_ (for example, order count, total spend, points collected).
* **Tier criteria** are the _thresholds_ you set for each tier using those signals (for example, “Order count ≥ 5”).

### Q. Can a tier system work without a loyalty wallet?

Yes. You can create a tier system using event counts or event property sums, even if you don’t use a loyalty wallet. However, if you want to grant wallet points as rewards, you must have a loyalty wallet created.

### Q. What are some best practices for tier design?

Keep tiers simple (3–5 tiers), choose criteria that users can realistically achieve, and make rewards meaningfully better as tiers increase. Use rolling windows if you want tiers to reflect recent loyalty.

### Do I need to add more than just the default tier?

Yes. A tier system must include at least one earned tier (Tier 2 or above) in addition to the default tier. Earned tiers allow users to progress based on their activity and unlock higher-level benefits.

### Do tiers have to follow a specific order?

Yes. Tiers follow a hierarchical order from lowest to highest. Users always progress upward through the hierarchy as their activity increases and cannot skip the defined tier structure.