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
# Overview

Funnels show users' progress through defined paths in your app and pinpoint where they drop off between steps. Funnels are a series of events a user performs in a particular order.

A typical example is a user onboarding flow, where a user progresses from the app's initial launch through activities such as registration, profile completion, and orientation. Another example is a purchase flow, where a user progresses through a shopping cart experience to a purchase event.

<Callout icon="📘" theme="info">
  #### Public Beta

  This feature is released in Public Beta. For more information about this feature or any queries, contact your Success Manager or the [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).
</Callout>

# Creating a Funnel

To create a funnel, perform the following steps:

1. Go to _Analytics_ > _Funnels Beta_.
2. Select the events in the desired order to create up to an eight-step funnel.
3. Select event properties for each event to constrain the analysis for the users who performed that event/property combination.

<Image align="center" border={true} caption="Create a Funnel" src="https://files.readme.io/de1b286dcda584e174fc4d4edb9b177d47232785f91810731941c97bd91a0c13-image.png" width="50% " />

4. You can also duplicate a step or add multiple events for the step by clicking the ellipsis menu. For example, you can add Mobile Login and Website Login as two events with OR logic between them in Step 1 of the Funnel to ensure you capture your entire user base.

<Image align="center" alt="Select Multiple Events" border={true} caption="Select Multiple Events" src="https://files.readme.io/4bb245c3bd7e1c55d271354270052226658bf057accf2ee77e3a683657255db8-image.png" width="60% " />

## Setting Conversion Window

Funnels are calculated based on a specified conversion window (set to five days by default). The conversion window is the total elapsed time for the user to complete all the steps in the funnel (that is, to convert). Shorter duration windows generally result in fewer users completing the funnel steps, whereas longer windows result in more user conversions.

To set a conversion window:

1. Go to _Analytics_ > _Funnels_.
2. Select the required events.
3. Under the _MEASURED BY_ section, select the _Conversion window_.

<Image align="center" border={true} caption="Set Conversion Window" src="https://files.readme.io/25e96965fb19df284a72492c304d00646f1eba0f9f8b42479f2c6ff668ca1ac4-image.png" width="50% " />

<Callout icon="📘" theme="info">
  #### Time Interval for Conversion Window

  CleverTap recommends setting the _Conversion Window_ to a duration shorter than the _Actual Date Range_ to avoid data variance.
</Callout>

## Compare by Segments

You can compare funnel conversions across different user segments to analyze how behavior varies between user groups. For example, compare the funnel for _App Launched_ > _Product Viewed_ > _Charged_ across the _All Users_ and the _Engaged Users_ segments. The differences in the conversion trends could reveal differences in your users' behavior in each segment and result in invaluable insight.

To compare conversion across segments, perform the following steps:

1. Go to _Analytics_ > _Funnels_.
2. Select the steps to analyze and view the conversion funnel.
3. From the _SEGMENT_ section, select the required segments. Select a segment from the list or create an ad-hoc segment. For more information, refer to [Segments](doc:segments).
4. Click **View Analysis**.

<Image align="center" border={true} caption="Segment Comparison Results" src="https://files.readme.io/db9e91450c33e1a00480fb14730ef050bbc70a54ad3308f65eadc5f53e89e1c1-image.png" />

## Advanced Filtering

Advanced filters help restrict your analysis to a specific user segment. You can create a segment based on any combination of past behaviors and user properties.

> 📘 Advanced Filters
>
> Advanced filters is a general feature for all analytics and most campaigns. For more information, refer to [Segments](doc:segments).

# Reading Funnel Charts

Funnel charts enable you to quickly determine how many users progress through each step of the funnel.

The default view shows cumulative conversions per step for the selected time range. It can be viewed as an absolute count of users completing each step or a percentage.

<Image align="center" alt="Funnel Charts" border={true} caption="Funnel Charts" src="https://files.readme.io/004bcc51afc2a74579c288ffc3915fe73e0e85963c02da2f961c6939f8e346e0-image.png" />

## Split by Property

You can split a funnel by profile properties for sessions, geographies, and technographics, or by an event property associated with any event. This lets you compare your conversion flows across product categories, geographies, devices, and more.

To break down by property, perform the following steps:

1. Click **Analytics** > **Funnel**.
2. Add _Funnel_ steps and click **View Funnel**.
3. Select a user property or an event property to split the funnel.
4. Click **View Analysis** to view the funnel.

<Image align="center" alt="Split funnel by event property" border={true} caption="Split Funnel by Event Property" src="https://files.readme.io/765e14575db123f3fbf0d28e7c1d8174c0ad9e4c4ccdbbecccbbfcea3c41dfc9-image.png" />

<Image align="center" alt="Split Funnel by User Property" border={true} caption="Split Funnel by User Property" src="https://files.readme.io/43c847997049c7db2488cb2a08c2417a6fb9d37029765d8251a0f280e2022e1b-image.png" />

# Funnel Computation Methods

Funnels support two computation methods:

* [Flexible Order](doc:funnels-v2#flexible-order)
* [Strict Order](doc:funnels-v2#strict-order)

These methods determine how users are counted as they progress through funnel steps, especially when steps are repeated or performed out of sequence.

## Flexible Order

By default, funnels count users who complete all defined steps in the specified sequence. Users may repeat earlier steps, but they must still complete every funnel step to be counted as converted. If a user completes a later step before a required earlier step, the funnel does not count that user as converted.

For example, if a funnel's steps are defined as:

**Step A → Step B → Step C → Step D**

The following table explains how different users are counted based on their progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                                |
| ------ | ------------------------------------------ | ------------------ | --------------------------------------------------------------------- |
| User 1 | Step A → Step B → Step C → Step D          | Yes                | Completes all funnel steps in the correct order.                      |
| User 2 | Step A → Step C → Step D                   | No                 | Skips Step B, which is required in the funnel.                        |
| User 3 | Step A → Step C → Step B → Step D          | No                 | Performs funnel steps out of sequence.                                |
| User 4 | Step A → Step B → Step A → Step C → Step D | Yes                | Repeats Step A but still completes all steps in the correct sequence. |

## Strict Order

When _Strict Order_ is enabled, funnels count users only if they complete every step exactly in the defined sequence. Any repetition of a funnel step or deviation from the specified order disqualifies the user from being counted as converted.

For example, if a funnel's steps are defined as:

**Step A → Step B → Step C → Step D**

The following table explains how different users are counted based on how they progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                     |
| ------ | ------------------------------------------ | ------------------ | ---------------------------------------------------------- |
| User 1 | Step A → Step B → Step C → Step D          | Yes                | Completes all funnel steps exactly in the specified order. |
| User 2 | Step A → Step C → Step D                   | No                 | Skips Step B, breaking the required step sequence.         |
| User 3 | Step A → Step C → Step B → Step D          | No                 | Performs funnel steps out of order.                        |
| User 4 | Step A → Step B → Step A → Step C → Step D | No                 | Repeats Step A, which violates strict ordering rules.      |

## Why Use Strict Order?

Strict ordering is useful when you want to identify friction or unexpected behavior within a process.

For example, let's take a look at the following Login Flow of two users in an app:

* **User A:** App Launched → Login Attempted → Login Attempted → Login Attempted → Logged In
* **User B:** App Launched → Login Attempted → Logged In

With strict order enabled, User A would not be counted as a clean conversion, highlighting repeated login attempts and potential user friction. This makes strict order particularly valuable for diagnosing issues in critical flows such as authentication, onboarding, or payments.

# Table View

You can also view the funnel information in a table to easily compare and absorb information.

<Image align="center" alt="Table view in funnels" border={true} caption="Table View in Funnels" src="https://files.readme.io/1168404ff665e17b95e472aa0d4c35eb1537a2129529fb9b7b92f6aac07f3f91-image.png" />

Every funnel categorization (split by user or event property) is a row in the table. To get better insight, sort by the required column. You can refer to  the following information in each row:

* Overall % conversion from the first step to the last step.
* Conversion % from one step to the next.

In the current example, you can conclude after the sort that Arabic speakers have the highest conversion rate.

# Bookmark a Funnel Analysis

You can bookmark any Funnel analysis to quickly revisit it later. Bookmarks are user-specific; only the logged-in user can view their saved bookmarks on the CleverTap dashboard.

Bookmarks are especially useful for tracking frequently accessed conversion journeys. For example, if you regularly monitor funnel steps such as _App Launched_ > _Product Viewed_ >  _Charged_, bookmarking it lets you instantly return to the same setup without recreating the funnel each time.

To bookmark a Funnel, perform the following steps

1. Click **Bookmark** in the top-right corner of the dashboard after generating the Funnel analysis.
2. Enter a descriptive name to help you easily identify the analysis later.
3. Click **Save**.

You can add up to 50 bookmarks.

> 📘 **Note**
>
> Funnels are accessible only to the user who created them. You can access all your saved bookmarks from the bookmark list under the _Funnels_ section.
