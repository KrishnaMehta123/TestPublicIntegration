---
title: Create a Recommendation
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
## Overview

You can create a recommendation by choosing a catalog and defining the required configurations based on which our recommendation engine will churn out results. These recommendations are served up to users automatically when you create a campaign using a recommendation.

# Create a Recommendation

To create a new recommendation, perform the following steps: 

1. From the dashboard, navigate to *Settings* > *Engage* > *Recommendations*.
2. Click **+ Recommendation**.

<Image title="Create a New Recommendation" alt={1401} border={true} src="https://files.readme.io/a317ff3-1_Plus_Recommendation.png">
  Create a New Recommendation
</Image>

# Select a Catalog

Select a catalog from which to generate recommendations. You can access the catalogs to which you have mapped the events.

<Image title="Select a Catalog to Generate Recommendations" alt={875} border={true} src="https://files.readme.io/ee58c7e-2_Select_a_Catalog.png">
  Select a Catalog to Generate Recommendations
</Image>

> 📘 Unmapped Catalog
>
> Unmapped catalogs will not be available for generating recommendations.

# Select an Event

This is the event in which CleverTap will consider similar items. Follow the steps below:

1. Select an event from which to generate recommendations. You can access the events that have been mapped to the chosen catalog. 
2. Select the relevant timeframe for which you want to generate the recommendations (e.g., create recommendations for items that have been viewed together in the last 10 days).

<Image title="Select an Event to Generate Recommendations" alt={878} border={true} src="https://files.readme.io/d6ba848-3_Select_an_Event.png">
  Select an Event to Generate Recommendations
</Image>

## Some Examples

Below are some examples:

### e-Commerce App

An e-Commerce app may want to trigger a recommendation as soon as a user adds Nike shoes to cart. 

* In this scenario, you can recommend other shoes to the user. 
* This can be either based on the shoes that the user may have viewed together or searched together in the last 30 days.
* In this case, the event to select would be *Viewed* together or *Searched* together.

### Video Streaming App

A video streaming app may want to trigger a recommendation once a user completes watching a trailer of a fantasy TV series. 

* In this scenario, you can recommend other shows that have been watched together with fantasy TV shows in the last 10 days. 
* In this case, the event to select would be *Watched* together.

# Filter Recommendations

To filter recommendations, you can include or exclude certain items.

> 👍 Fashion eCommerce Example to Include Items
>
> A fashion eCommerce could set up their filter to only recommend shoes.

To filter the items that are served up to only include certain items, perform the following steps:

1. Select the checkbox for *Filter recommendations to specific catalog items*.
2. Select *Include*.
3. Click **+ Catalog Field**.
4. Select the appropriate category fields.
5. Add more catalog fields as required.
6. Click **Create**.

<Image title="Filter Recommendations to Include Specific Catalog Items" alt={884} src="https://files.readme.io/ac08cc8-4a_Filter_recommendations_-_include.png">
  Filter Recommendations - Include
</Image>

> 👍 Fashion eCommerce Example to Exclude Items
>
> A fashion eCommerce could set up their filter to exclude any items rated as a C user rating from their recommendations.

To filter the items that are served up to only exclude certain items, perform the following steps:

1. Select the checkbox for *Filter recommendations to specific catalog items*.
2. Select *Exclude*.
3. Click **+ Catalog Field**.
4. Select the appropriate category fields.
5. Add more catalog fields as required.
6. Click **Create**.

<Image title="Filter Recommendations to Exclude Specific Catalog Items" alt={876} src="https://files.readme.io/3fc8c73-4b_Filter_recommendations_-_exclude.png">
  Filter Recommendations - Exclude
</Image>

> 📘 Processing Time
>
> It takes up to 24 hours for the CleverTap data science engine to publish the recommendations from the time the recommendation is generated.
