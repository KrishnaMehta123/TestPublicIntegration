---
title: Funnels
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

Funnels show users progress through defined paths in your app and pinpoint where they drop off between steps. Funnels are defined as a series of events that a user performs in a particular order.

Some common examples include a user onboarding flow where a user progresses from the initial launching of the app through activities such as registration, profile completion and orientation, or a purchase flow where a user progresses through a shopping cart experience through to a purchase event.

# Creating a Funnel

To create a funnel, perform the following steps:

1. Select the desired events in the desired order where you can create up to an eight-step funnel. 
2. Select event properties for each event to constrain the analysis for the users who performed that event/property combination.

<Image title="Define the Steps to Crete a Funnel" alt={1403} align="center" border={true} src="https://files.readme.io/833a1d8-1_Funnels_-_select_event_properties.png">
  Create a Funnel
</Image>

> 📘 Re-arrange Steps
>
> You can drag and drop to re-arrange the steps in a funnel.

## Setting Conversion Window

Funnels are calculated based on a specified conversion window (set to five days by default). The conversion window is the total elapsed time for the user to complete all the steps in the funnel (i.e. to convert). Shorter windows generally result in fewer users completing the funnel steps whereas larger windows result in more user converting.

> 📘 Time Interval for Conversion Window
>
> CleverTap recommends setting the *Conversion Window* to a duration shorter than the *Actual Date Range* to avoid data variance.

<Image title="Select Funnel Conversion Time" alt={888} align="center" border={true} src="https://files.readme.io/c1e68ec-Analytics_Funnels_Conversion_window.png">
  Set Conversion Window
</Image>

## Compare by Segments

You can choose to compare your conversion across different segments. For example, compare the funnel for *App Launched* > *Product Viewed* > *Charged* across the *All Users* segment and the *Frequent Buyers* segment. The differences in the conversion trends could reveal a difference in the behavior of your users in each segment and hence result in an insight that could be invaluable. 

To compare conversion across segments, perform the following steps:

1. Navigate to *Analytics* > *Funnels*.
2. Select the steps to analyze and view the conversion funnel.
3. Select the *Compare to another segment* box. Select a segment from the list or create an ad-hoc segment. For more information, refer to [Segments](doc:segments).
4. Click **View Funnel**.

<Image title="Select Compare to Another Segment options and Click View Funnel" alt={1165} align="center" width="100%" border={true} src="https://files.readme.io/7f9ed1b-2_Analytics_Funnels_Compare_Segments_Search.png">
  Compare by Segments
</Image>

The results are displayed.

<Image title="View Funnel Comparison by Percentage" alt={1155} align="center" width="100%" border={true} src="https://files.readme.io/eb0e3a1-Analytics_Funnels_Compare_Segments_Search_Results.png">
  View Comparison
</Image>

## Advanced Filtering

Advanced filters restrict your analysis to a specific segment of users. Create a segment based on any combination of past behaviors in combination with any set of user properties. 

> 📘 Advanced Filters
>
> Advanced filters is a general feature available for all analytics features and most campaigns. For more information, refer to [Segments](doc:segments).

# Reading Funnel Charts

Funnel charts let you quickly determine how many users progress through each of the funnel steps. 

The default view shows cumulative conversions per step for the selected time range and can be viewed as either an absolute count of users completing each step or as a percentage.

By definition, all users (100%) complete the first step in any funnel. In the example below, for the first step under *Product Viewed*, 157,858 users complete this step. Of these users, 103,094 go on to the *Added to Cart* step, then 30,704 users go on to complete the final *Charged* step in the funnel.

<Image title="View Funnels Charts by Percentage" alt={1999} align="center" border={true} src="https://files.readme.io/ff2abce-image8.png">
  Funnel Charts
</Image>

## Breakdown by Property

You can breakdown a funnel by profile properties for sessions, geographies, technographics, or by any event property associated with any event. By doing this, you can compare your conversion flows across product categories, geographies, devices, and more. 

To breakdown by property, perform the following steps:

1. Click **Analytics** > **Funnel**.
2. Add *Funnel* steps and click **View Funnel**.
3. Select the property and its value to breakdown the funnel.

<Image title="Select Options to Breakdowns Funnel by Property" alt={1208} align="center" width="100%" border={true} src="https://files.readme.io/3b40dbd-Analytics_Funnels_breakdown_by_profile_property.png">
  Funnel Breakdown by Property
</Image>

<Image title="View Funnel Breakdown by Property in Percentage" alt={1179} align="center" border={true} src="https://files.readme.io/56000b3-Analytics_Funnels_breakdown_by_event_property.png">
  View Funnel Breakdown
</Image>

## Hold Property Constant

You can define conversion based on event property which helps determine if the conversion was done for the intended item or not. 

You expect the user to view a shirt, add this shirt to cart, and then purchase it. Here, the product name is your event property and the property values are *Shirt*, *Dress*, *Trousers*, *Jackets*. If the user purchases anything else,  you do not consider it as conversion. 

Now the user views the shirt, adds the shirt to cart, but purchases a trouser. You still have a sale but this is not the intended analysis. If the user purchases trousers, then this must be considered as a drop-off. To do this, you can hold the event property (product name) constant and consider it a conversion only if the user purchases a shirt.

<Image title="Select Hold Property Constant Options and View Funnel" alt={1174} align="center" border={true} src="https://files.readme.io/b7b281f-3-Analytics_Funnels_hold_property.png">
  View Funnel with Hold Property Constant
</Image>

> 📘 Key Points to Remember
>
> The following are some of the points to remember:
>
> * Only the top 20 event property values are considered. 
> * This funnel type does not support creating a campaign or segment.
> * You can break down a funnel by an event property and hold that property constant. Holding the event property may lead to counting users multiple times if they perform the event with that property more than once. As funnels track unique users at the event level, you may observe significantly larger numbers when you switch to unique users at the event property level.

## Conversions over Time

For each funnel, CleverTap calculates and trends the time it takes for users to progress from one step to another and shows these trends in both a cumulative and absolute graph. 

Conversion time helps you understand how long it takes the majority of your users to progress between steps in your funnel. In turn, this can be used as a basis for sending engagement [campaigns](doc:intro-to-campaigns) timed to reach users who *do not* convert within the time the majority of your users convert. 

Depending on the nature of the app and conversion flow, users may progress through funnel steps measured in hours or minutes or measured in days, weeks, or even months.

For a funnel where users progress between steps rapidly, set the conversion time to an appropriate time (for example, 8 hours or less) to see the specific time when the majority of users convert. In the example below, the conversion time is set to 1 hour. From the graph, we see that 80% of users progress through the funnel within 14 minutes.

<Image title="Select Conversion Over Time Relative to Step 1" alt={1999} align="center" border={true} src="https://files.readme.io/c7cf6b2-image5.png">
  View Conversion Over Time
</Image>

The absolute trend graph shows you the spike in conversions within the first minute where 44% of users convert.

<Image title="View Trend Graph of Spike in Conversion" alt={1999} align="center" border={true} src="https://files.readme.io/296c6e0-image6.png">
  View Spike in Conversion
</Image>

## Daily Trend View

In the daily trend view, the completion of each step is calculated for each day in the selected time range and trended. The daily trend view lets you pinpoint spikes in conversions on a particular day as well as to see if conversions are trending up or down over time. Trends can be viewed as either an absolute count of users or a percentage.

Note that in the daily trend view on any particular day, the users converting for each step are independent of one another. For example, on September 4, 59,474 users completed the *Product Viewed* step and 47,794 users completed the *Added to Cart* step. 

Keep in mind that the users who complete *Added to Cart* on September 4 are not necessarily a subset of the users who completed the *Product Viewed* step on that day. Some of these users who completed *Added to Cart* on September 4 may have completed the *Product Viewed* step the prior day, week, and so on.

<Image title="Click Daily Trend and Select Count" alt={1999} align="center" border={true} src="https://files.readme.io/80237b3-image1.png">
  View Daily Trend
</Image>

# Funnel Computation Methods

This section covers two types of funnel computation methods including the default method and the strict ordering method.

## Default Method

By default, funnels will count all users who perform all the specified steps in order regardless of whether they loop back to an earlier step or move forward to a later step in the funnel. 

For example, if our funnel steps are defined as:  

* Funnel Steps: Step A → Step B → Step C → Step D 

In the scenarios below, we can analyze whether different users are counted as converting depending on the order in which each progress through the funnel steps.

* User 1: Step A → Step B → Step C → Step D
* User 2: Step A  → Step C → Step D
* User 3: Step A → Step C → Step B → Step D
* User 4:  Step A → Step B → Step A → Step C → Step D

User 1 is counted since she progresses through the funnel steps in order.\
User 2 is not counted since she did not perform Step B.\
User 3 is not counted since she completed the steps out of order.\
User 4 is counted since she completed the steps in order, even though she looped back and performed Step A twice.

## Strict Ordering Method

By checking *Enforce Strict Order,* users will only be counted if they complete the funnel steps in exactly the specified order without performing another one of the funnel steps out of order. 

Consider the same example as above where the funnel steps defined are:  

* Funnel Steps: Step A → Step B → Step C → Step D

If we analyze the users below:  

* User 1: Step A → Step B → Step C → Step D
* User 2: Step A  → Step C → Step D
* User 3: Step A → Step C → Step B → Step D
* User 4:  Step A → Step B → Step A → Step C → Step D

Here, only user 1 will be counted as converting as the strict order restricts any deviation from the specified steps in the funnel. The other users (i.e., 2, 3, and 4) are breaking the strict ordering, therefore, they do not qualify.

<Image title="Select Enforce Strict Order" alt={207} align="center" border={true} src="https://files.readme.io/18a3234-4_Enforce_strict_order.png">
  Strict Ordering Method
</Image>

# Table View

You can also view the funnel information in a table. 

<Image title="View the Funnel Information in Table" alt={1186} align="center" width="100%" border={true} src="https://files.readme.io/4cc5ae9-5-Analytics_Funnels_Table_view.png">
  Table View of Funnels
</Image>

Every categorization (split by user or event property) in the funnel is a row in the table. You can see the following information in each row:

* Overall % conversion from the first step to the last step. 
* Conversion % from one step to the next.
* Median time for conversion to the next step.

# Frequency Chart

The frequency chart displays the frequency of a user action from the current step to the next. For example, it can show the number of times a user viewed a shirt before purchasing it. 

To do so, perform the following steps:

1. Select the funnel step as follows:

   * *App Launched*
   * *Product Viewed*
   * *Charged*

   Once done, the funnel is displayed. 

<Image title="Click Frequency Tab to View Frequency Chart" alt={1201} align="center" border={true} src="https://files.readme.io/4b27769-Analytics_Funnels_Frequency.png">
  Frequency Chart
</Image>

2. Click the **Frequency** tab. 
3. Select the step for your analysis, *Product viewed* in our example. 

It shows you the frequency of users who viewed the product before purchasing it. We see in the example that  19.63 % of the users viewed the product two times before making a final purchase. So the insight might be that marketing effort needs to be towards reducing the number of product views or that maybe, the user needs more information in the first product view before making a purchase. 

> 📘 Frequency Chart Considerations
>
> Consider the following:
>
> * Frequency chart is available only from the second funnel step.
> * Creating a campaign or segment is not supported for this funnel type.

# Bookmarks

You can bookmark any funnel, cohort, or event query, and save it to quickly retrieve later. Bookmarks are specific to each logged-in user. No other dashboard users will see the bookmarks you save. 

Bookmarks are convenient for recalling a specific analysis that you want to see frequently. For example, you can bookmark your important conversion funnels and view them each day or week to see how they are changing over time.

# Actionable Funnels

After you build a funnel, you can use the actionable funnels feature to save a segment of users from the funnel or create a campaign targeting that segment. 

### Example

You can create a segment for users who did or did not complete an event at a specific stage of a funnel.

For example, we can create a new funnel that measures the progression of users who launch your app, add an item to their cart, and then purchase an item. 

First, we create a segment for the users who only launched your app, added an item to their cart, but then did not purchase an item. We can do this by clicking the gray area in the third bar which represents the users who dropped off and did not complete the charged event.

<Image title="View Actionable Funnels in Percentage" alt={1111} align="center" border={true} src="https://files.readme.io/6e87501-actionable-funnel-1.png">
  Actionable Funnels
</Image>

Alternatively, instead of targeting users who dropped off in the last stage of the funnel, we can create a segment or campaign targeting that segment for users who purchased an item.

<Image title="Click the Funnel to Take Actions" alt={1108} align="center" border={true} src="https://files.readme.io/3013112-actionable-funnels-3.png">
  Taking Action on Funnels
</Image>
