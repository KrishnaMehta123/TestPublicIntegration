---
title: Funnels Beta
excerpt: >-
  Learn how to use the new and improved visualization using Funnels to gain
  deeper insights into your data and make more informed decisions.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<br />

# Overview

Funnels are a series of actions that a user performs in a particular order. They show users' progress through defined paths in your app and identify where they drop off between steps.

A typical example is a user onboarding sequence, where a user progresses from the app's initial launch through activities such as registration, profile completion, and orientation. Another example is a purchase sequence, where a user progresses through a shopping cart experience to complete a purchase.

<Callout icon="📘" theme="info">
  #### Public Beta

  This feature is released in Public Beta. For more information about this feature or any queries, contact your Customer Success Manager or the [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).
</Callout>

# Creating a Funnel

To analyze how users progress through a defined sequence of events, you can create a funnel using the Funnels feature in CleverTap.

To create a funnel, go to _Analytics > Funnels Beta_ and perform the following steps:

* [Select Events](doc:funnels-v2#select-events)
* [Select Segments](doc:funnels-v2#select-segments)
* [Split by Property](doc:funnels-v2#split-by-property)
* [Select Measured by Options](doc:funnels-v2#select-measured-by-options)

## Select Events

Select the events in the desired order to create a funnel with up to eight steps. You can also select event properties for each event to limit the analysis to the users who performed the selected event with the associated properties.

<Image align="center" border={true} caption="Select Funnel Events" src="https://files.readme.io/698381e8f564ec79290e3f589d750385dd98ee602cf9aa6c8a883c7778728895-image.png" />

You can add multiple events (up to four) within a single funnel step using an OR condition. This is useful when the same user action can be represented by different events but should be treated as a single step in the funnel.

For example, if users can log in through either a mobile app or a website, you can group the Mobile Login and Website Login events into a single funnel step using OR logic. This ensures that users are counted as having completed the step regardless of the platform they used, providing a more accurate view of user progression.

<Image align="center" border={true} caption="Add Multiple Events with an OR Condition" src="https://files.readme.io/43b1604c14a3fd8b3cee34c3b5563dec6f22a49b165b065382c7db87e94de83c-image.png" />

## Select Segments

You can compare funnel conversions across different user segments to analyze how behavior varies between user groups. For example, compare the funnel for _App Launched > Product Viewed > Charged_ across the _All Users_ and the _Engaged Users_ segments. The differences in conversion trends could reveal variations in your users' behavior across each segment and result in invaluable insights.

You can compare funnel conversions across different user segments to analyze how behavior varies between user groups. For example, you can compare the funnel _App Launched > Product Viewed > Charged_ across the _All Users_ and _Engaged Users_ segments to understand how engagement level impacts conversion.

In the example below, the _Engaged Users_ segment shows a higher conversion rate at each funnel step compared to _All Users_. This indicates that users who are already engaged with the app are more likely to progress through the funnel and complete a purchase. Insights like these can help you prioritize high-value segments, refine your targeting strategies, and identify where less-engaged users tend to drop off.

<Image align="center" border={true} caption="Segment Comparison Results" src="https://files.readme.io/a5b1682c49204dbb5775efbf02ea21cfb6f6df96ed3fabef0c83939233ced1ee-image.png" />

## Split by Property

You can split a funnel by event properties or user profile properties, such as sessions, geographies, technographics, or any custom attributes. This allows you to compare how different attributes influence user progression and conversion across the same funnel.

Splitting funnels helps you answer questions like:

* Which products convert better?
* Which languages, regions, or devices show higher drop-offs?
* Where should optimization efforts be focused?

### Split by Event Property

In the following example, the funnel is split by the _product_ event property. Each row represents a different product, allowing you to compare how users progress through the funnel for each product variant.

Here, the analysis shows that some products have higher overall conversion rates than others. This indicates which products are more effective in driving users toward conversion and which may require improvements in discovery, pricing, or user experience.

<Image align="center" border={true} caption="Split Funnel by Event Property" src="https://files.readme.io/db0c4c73ebfd5874869ae362b54bde3ea5cb834b4e87dae943fc51f8756b3bcd-image.png" />

### Split by User Property

In the following example, the funnel is split by the _Language_ user property. Each row represents a language group, enabling you to compare conversion behavior across different user demographics.

Here, the analysis shows that users with different language preferences convert at different rates. These insights can help identify which language segments are performing well and which may benefit from localized content, messaging, or onboarding improvements.

<Image align="center" border={true} caption="Split Funnel by User Property" src="https://files.readme.io/959e4ab3fcef7f905082f8930ddbd5746f506e1e76fe3f02c2cc59492a105cab-image.png" />

## Select Measured By Options

The _MEASURED BY_ section controls how funnel conversions are calculated, grouped, and evaluated. These settings directly impact how users are counted and how funnel results are displayed.

From the _MEASURED BY_ section, you can query:

* [Measurement Mode](doc:funnels-v2#measurement-mode)
* [Conversion Window](doc:funnels-v2#conversion-window)
* [Step Order](doc:funnels-v2#step-order)

## Measurement Mode

The measurement mode determines whether funnel performance is displayed as a single aggregated value or as a trend over time.

You can choose one of the following measurement modes:

* [Total Conversion](doc:funnels-v2#total-conversion)
* [Trends](doc:funnels-v2#trends)

### Total Conversion

Selecting **Total Conversion** allows you to view the aggregate conversion count or conversion rate for the selected time range. Results are shown as a single value and are not broken down by time.

For example, selecting total conversion for the funnel _App Installed > App Launched > Added to Cart_ over the last 30 days shows the overall percentage and number of users who completed the entire funnel during that period. This provides a quick snapshot of how effectively users convert from the first step to the final step, without focusing on daily or weekly fluctuations.

<Image align="center" border={true} caption="Measured By Total Conversion" src="https://files.readme.io/bb8d24cbf8632ce064c529da93367986bb336bc6c72260c1b96edbc0716de140-image.png" />

Use the Total Conversion option when you want to:

* Get a high-level summary of funnel performance
* Compare overall conversion rates across segments
* Report a single conversion metric for a given period

### Trends

Selecting **Trends** allows you to analyze how funnel conversions change over time. When **Trends** is selected, you must also choose a time granularity, that is, Day, Week, or Month, to view the trend.

For example, analyzing daily conversion trends for the funnel _App Installed > App Launched > Added to Cart_ over the last 30 days can help you identify when conversions increase or decline. These patterns may correlate with product releases, marketing campaigns, or external factors, enabling you to understand what influences user progression through the funnel and take timely action.

<Image align="center" border={true} caption="Measured By Trends" src="https://files.readme.io/a224fc96cc40590298e10b64aa81633b76c57cf53f9d9429411b26fcd43d1cce-image.png" />

Use the Trends option when you want to:

* Track conversion performance over time
* Identify spikes, drops, or seasonality in funnel conversions
* Compare trends across segments or properties

## Conversion Window

Funnels are calculated using a conversion window, which defines the maximum time you allow for users to complete all steps in the funnel. The conversion window is set to 5 days by default, but you can adjust it based on the type of analysis you want to perform.

A shorter conversion window applies stricter criteria and includes only users who complete the funnel within a shorter timeframe. A longer conversion window allows users more time to complete all steps, which results in more users qualifying for the analysis, not necessarily more conversions.

Choose the conversion window based on how long your typical user journey takes. For example, fast actions, such as onboarding, may require shorter windows, while high-consideration flows, like purchases, may need longer ones.

<Image align="center" border={true} caption="Set Conversion Window" src="https://files.readme.io/97a73f12ec359477da234ef50ad379553f6bf28f38c59a1e6f165e2c9908aa9b-image.png" />

<Callout icon="📘" theme="info">
  #### Time Interval for Conversion Window

  CleverTap recommends setting the Conversion Window to a duration shorter than the selected date range of the analysis. This helps ensure consistent and reliable funnel results by avoiding partial or overlapping conversions.
</Callout>

## Step Order

The _Step Order_ setting determines whether users must follow the predefined sequence of funnel steps to be counted as converted. This order determines how users are counted as they progress through funnel steps, primarily when steps are repeated or performed out of sequence.

<Image align="center" border={true} caption="Funnel Step Order" src="https://files.readme.io/0a03b55656f6066ebb8ff9e59b3fe3344e6526a45ad37a317c64bff3fef5fcd2-image.png" />

You can select one of the following options:

* [Flexible Order](doc:funnels-v2#flexible-order)
* [Strict Order](doc:funnels-v2#strict-order)

### Flexible Order

By default, funnels count users who complete all defined steps in the specified sequence. Users may repeat earlier steps, but they must still complete every funnel step to be counted as converted. If a user skips a required step and then completes it later, the funnel does not count that user as converted.

For example, a funnel's steps are defined in the following sequence:

**Step A > Step B > Step C > Step D**

The following table explains how different users are counted based on their progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                                |
| ------ | ------------------------------------------ | ------------------ | --------------------------------------------------------------------- |
| User 1 | Step A > Step B > Step C > Step D          | Yes                | Completes all funnel steps in the correct order.                      |
| User 2 | Step A > Step C > Step D                   | No                 | Skips Step B, which is required in the funnel.                        |
| User 3 | Step A > Step C > Step B > Step D          | No                 | Performs funnel steps out of sequence.                                |
| User 4 | Step A > Step B > Step A > Step C > Step D | Yes                | Repeats Step A but still completes all steps in the correct sequence. |

#### Why Use Flexible Order?

Flexible ordering is useful when you want to measure overall funnel completion without ignoring users for repeated or exploratory behavior.

In many user journeys, users may repeat steps, navigate back and forth between screens, or perform actions multiple times before progressing. Flexible Order ensures that these natural behaviors do not prevent users from being counted as converted, as long as they eventually complete all required steps in the correct sequence.

For example, consider the following conversion sequence of two users in an app:

**User A**: App Launched > Viewed Product > Viewed Product > Added to Cart > Viewed Product > Purchased

**User B**: App Launched > Viewed Product > Added to Cart > Purchased

With Flexible Order enabled, both users are counted as converted because they complete all funnel steps in the defined order, even though User A repeats some steps.

### Strict Order

When _Strict Order_ is selected, funnels count users only if they complete every step exactly in the defined sequence. Any repetition of a funnel step or deviation from the specified order disqualifies the user from being counted as converted.

For example, a funnel's steps are defined as follows:

**Step A > Step B > Step C > Step D**

The following table explains how different users are counted based on how they progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                     |
| ------ | ------------------------------------------ | ------------------ | ---------------------------------------------------------- |
| User 1 | Step A > Step B > Step C > Step D          | Yes                | Completes all funnel steps exactly in the specified order. |
| User 2 | Step A > Step C > Step D                   | No                 | Skips Step B, breaking the required step sequence.         |
| User 3 | Step A > Step C > Step B > Step D          | No                 | Performs funnel steps out of order.                        |
| User 4 | Step A > Step B > Step A > Step C > Step D | No                 | Repeats Step A, which violates strict ordering rules.      |

#### Why Use Strict Order?

Strict ordering is useful when you want to identify friction or unexpected behavior within a process.

For example, consider the following Login sequence of two users in an app:

* **User A:** App Launched > Login Attempted > Login Attempted > Login Attempted > Logged In
* **User B:** App Launched > Login Attempted > Logged In

With strict order enabled, User A is not counted as a clean conversion, highlighting repeated login attempts and potential user friction. This makes strict order particularly valuable for diagnosing issues in critical sequences such as authentication, onboarding, or payments.

# Reading Funnel Analysis

CleverTap offers multiple views to help you effectively interpret funnel performance. Based on whether you want a visual overview or a detailed comparison, you can analyze funnel data using [Chart View](doc:funnels-v2#chart-view) or [Table View.](doc:funnels-v2#chart-view) Each view highlights different aspects of user progression and conversion behavior.

## Chart View

Chart View offers a visual representation of how users progress through each step of the funnel, allowing for easy identification of drop-offs and overall conversion trends at a glance.

The default chart shows cumulative conversions per step for the selected time range. You can view the data either as an absolute count of users completing each step or as a percentage.

<Image align="center" border={true} caption="Chart View of Funnel Analysis" src="https://files.readme.io/cfa94110676c19e93c60cc3dc28393b2198e29518d30250053c2e069e8be9010-image.png" />

## Table View

Table View presents the same funnel data in a structured, tabular format, making it easier to compare conversions across segments or property-based splits.

Each row in the table represents a funnel categorization, such as a user or event property used to split the funnel. You can sort the table by any column to quickly identify patterns or outliers.

The table includes the following metrics for each row:

* Overall conversion percentage from the first step to the last step
* Conversion number and percentage between consecutive steps

In the example shown below, sorting the table reveals that English speakers have the highest overall conversion rate.

<Image align="center" border={true} caption="Table View of Funnel Analysis" src="https://files.readme.io/9aeb7ed709958f6ef3ce3ffa1cb23d594a84466a827bd6ae1586f7752da823d5-image.png" />

# Bookmark a Funnel Analysis

You can bookmark any Funnel analysis to quickly revisit it later. Bookmarks are user-specific; only the logged-in user can view their saved bookmarks on the CleverTap dashboard.

Bookmarks are especially useful for tracking frequently accessed conversion journeys. For example, if you regularly monitor funnel steps such as _App Launched_ > _Product Viewed_ > _Charged_, bookmarking it allows you to instantly return to the same setup without recreating the funnel each time.

To bookmark a Funnel:

1. Click **Bookmark** in the top-right corner of the dashboard after generating the Funnel analysis.
2. Enter a descriptive name to help you easily identify the analysis later.
3. Click **Bookmark**.

<Image align="center" border={true} caption="Bookmark a Funnel Analysis" src="https://files.readme.io/0a95c2524453a5d5e5b88f4d133534cefadfa02b54ced32746f4b63b34aa6eb7-2026-01-02_15-18-05_1.gif" />

<Callout icon="📘" theme="info">
  #### Note

  You can add up to 50 bookmarks. Funnels are accessible only to the user who created them. You can access all your saved bookmarks from the bookmark list under the _Funnels_ section.
</Callout>

# FAQ

Find answers to the following common questions about using ̉Funnels:

### How Are Users Counted?

Each user is counted once per funnel evaluation period.

### What Happens If a User Completes the Funnel Multiple Times?

If a user completes the funnel multiple times within the selected date range, only the first valid conversion within the conversion window is counted. Subsequent completions by the same user are ignored for that analysis.

### What If a User Does Not Complete All Funnel Steps?

Users who do not complete all defined funnel steps within the specified conversion window are not considered to have been converted. They are included only in the steps they completed, which helps identify drop-off points in the funnel.

### How Does the Conversion Window Affect Funnel Results?

The conversion window defines the maximum time allowed for a user to complete all funnel steps. If a user exceeds this time, the funnel does not count them as converted, even if they eventually complete all steps. A shorter window results in stricter conversion criteria, while a longer window allows more users to qualify.

### Can I Change Funnel Settings After Viewing Results?

Yes. You can modify funnel settings such as events, segments, measurement mode, conversion window, or step order at any time. However, changing these settings triggers a new funnel calculation, and previously generated results are not retained.

### Are Funnel Results Calculated in Real Time?

Funnel results are near real-time, but may experience a short processing delay due to varying data volumes and query complexities. Recently ingested events may take a few minutes to appear in funnel analysis.

### Can I Compare Funnels Across Different Date Ranges?

Yes. You can change the date range and re-run the same funnel configuration to compare performance across different periods. For trend-based analysis, using the Trends measurement mode is recommended.
