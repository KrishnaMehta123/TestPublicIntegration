---
title: Segmentation Rules
excerpt: >-
  Understand how you can create rules to segment your users based on different
  properties in CleverTap.
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

In CleverTap, user property and behavior are significant when creating user segments. You can target your audience for campaigns based on their user properties and behavior. You can do so by creating segmentation rules from the *Create Segments* page.

## User Property

User property refers to a user's demographic attributes, such as age, gender, location, device type, subscription status, etc. You can define these properties from the CleverTap dashboard, which is later collected during signup or interaction with your application. The following are the specific factors used to create segments based on user property:

* **User property**: Segment users based on custom user property values such as email, phone number, customer type, etc. For example, you can create a segment of users whose *customertype* is *Gold*.

<Image alt="Users Property Rule" align="center" border={true} src="https://files.readme.io/26e646e-User_Property_Rule.png">
  Segment by User Property Rule
</Image>

* **User bucket**: Segment users based on a system user property called [User Bucket](doc:user-bucket). For example, you can create a segment of users with bucket numbers 7, 100, and 999.

<Image alt="Segment by User Bucket Rule" align="center" border={true} src="https://files.readme.io/b86aea6-User_Bucket.png">
  Segment by User Bucket Rule
</Image>

* **Demographic**: Segment users based on demographic user property values such as gender, age, etc. For example, you can segment your users based on their gender.

<Image alt="Demographics Rule" align="center" border={true} src="https://files.readme.io/dc14c9a-Demographics_Rule.png">
  Segment by Demographics Rule
</Image>

* **Geography**: Segment users based on their location. For example, you can create a segment of users living in Los Angeles, California, the United States, and so on.

<Image alt="Geography Rule" align="center" border={true} src="https://files.readme.io/fe644d9-Geography_Rules.png">
  Segment by Geography Rule
</Image>

* **Geography Radius**: Segment users that are located at a certain distance from the particular location. For example, you can create a segment of users within a particular retail store's radius.

<Image alt="Geography Radius Rule" align="center" border={true} src="https://files.readme.io/64478f1-Gegraphy_Radius_Rule.png">
  Segment by Geography Radius Rule
</Image>

* **Technographics**: Segments users based on the technical specifications of their devices. For example, you can create a segment of users who use your App on a mobile device with an Android OS.

<Image alt="Technographics Rule" align="center" border={true} src="https://files.readme.io/c83a72f-Technographics_Rule.png">
  Segment by Technographics Rule
</Image>

* **Reachability**: Segment users based on their reachability via different messaging channels such as push notifications, SMS, or email. For example, you can create a segment of unsubscribed users to receive emails.

<Image alt="Reachability Rule" align="center" border={true} src="https://files.readme.io/b8b831a-Reachability_Rule.png">
  Segment by Reachability Rule
</Image>

* **App Fields**: Segment users based on the version or type of your App. For example, you can create a segment of users with a Samsung device using the app version 5.3.0.

<Image alt="App Fields Rule" align="center" border={true} src="https://files.readme.io/a012675-App_Fields_Rule.png">
  Segment by App Fields Rule
</Image>

* **Segments**: Segment users based on their membership in a particular segment. For example, you can create a segment of users who have purchased in the past 30 days and save it as *Charged Users*. You can then include and exclude this segment based on your target audience while creating a new segment rather than creating a complex query each time.

<Image alt="Segments Rule" align="center" border={true} src="https://files.readme.io/0904d67-Segments_Rules.png">
  Segment by Segments Rule
</Image>

> 📘 Include and Exclude
>
> The following are some of the points that you consider when you include and exclude segments:
>
> * The include and exclude segments are currently unavailable for bulletins and A/B Testing.
> * You can only include or exclude  [PBS](https://docs.clevertap.com/docs/segments#section-past-behavior-segments) and [Custom List](https://docs.clevertap.com/docs/custom-list-segments) segments.

## User Behavior

User behavior refers to a user's actions within your App or Website, such as completing a purchase, adding items to a cart, clicking on a specific link or button, abandoning a session, or leaving a review. CleverTap tracks these behaviors through event tracking. The following are the factors used to create segments based on user behavior:

* **Event (Did)**: Segment users based on the events they have done. For example, you can create a segment of users who have performed the *App Installed* event in the last 30 days.

<Image alt="Segment by Did Rule" align="center" border={true} src="https://files.readme.io/18dda8d-Did.png">
  Segment by Did Rule
</Image>

* **Event (Have not done)**: Segment users based on the events they have not done. For example, you can create a segment of users who have not performed the *App launched* event in the last 30 days.

<Image alt="Segment by Have Not Done Rule" align="center" border={true} src="https://files.readme.io/7d2fa6e-Have_Not_Done.png">
  Segment by Have Not Done Rule
</Image>

* **Combination of (Did any of)**: Segment users based on any of the events they have done in a specified period of time. For example, you can create a segment of users who have performed any of the events, such as Product Viewed, Added to Cart, or Charged in the last 30 days.

<Image alt="Segment by Did Any Of Rule" align="center" border={true} src="https://files.readme.io/fbef063-Did_Any_Of.png">
  Segment by Did Any Of Rule
</Image>

## User Interests

User Interests refer to the psychography of users, which enables you to segment your users based on event properties, including their relative frequencies, date, and time. It tells you how often the users do something and when they do it (by date and time). 

There are three types of rules provided by CleverTap:

* **Event Property**: Interest by Event Property allows you to segment users based on specific actions they frequently perform. For example, you can segment users users who frequently read articles on technology out of all the articles they read. This helps in targeting users who have a specific interest in tech-related content.
* **Time of the day**: Interest by Time of the Day allows you to segment users based on when they usually perform actions during the day. For example, you can segment users who typically shop online between 8 PM and 10 PM. This allows you to send targeted promotions or reminders during their preferred shopping hours.
* **Day of the week**: Interest by Day of the Week allows you to segment users based on which day of the week they usually perform actions. For example, you can segment users who usually order food delivery on Fridays. This enables you to send special weekend offers or discounts to encourage repeat orders.

> 📘 Predominantly vs. At Least
>
> The *Predominantly* option means the event property you select will only include users, where that event property is the most frequently occurring event property for the user. The *At Least* option lets you specify the specific percentage you need.

# AND/OR Rules

The *AND/OR* rules are an important segmentation feature in CleverTap. Combining different conditions using these operators allows you to create highly personalized campaigns that resonate with your users. When using these rules, it is important to understand the syntax and usage, ensuring you target the right segment for your campaign. The following sections provide information about the syntax and usage of *AND/OR* rules when creating segments in CleverTap.

## Using AND Operator

The *AND* operator combines multiple conditions that must be met simultaneously to qualify for the segment.

For example, if you want to target users who are both male and have purchased at least one product in the last 30 days. In this case, the *AND* rule would be as follows:

<Image alt="Segmenting with AND Operator" align="center" border={true} src="https://files.readme.io/ae30ff4-Segment_with_AND_Operator.png">
  Segmenting with AND Operator
</Image>

In this case, the audience will only include users who match both the specified conditions.

## Using OR Operator

The *OR* operator combines multiple conditions where at least one must be true to qualify for the segment.

For example, if you want to target users who have either made a purchase in the last 30 days or have added items to their cart but have not completed the purchase. In this case, the *OR* rule would look like this:

<Image alt="Segmenting with OR Operator" align="center" border={true} src="https://files.readme.io/9c0b2ec-OR_Operator.png">
  Segmenting with OR Operator
</Image>

In this case, the segment will include users who match either of the specified conditions.

## Combining AND/OR Operators

Both *AND* and *OR* operators can be combined to create more complex segmentation rules. For example, if you want to target male users who have made a purchase in the last 30 days OR female users who have not completed the purchase in the last 30 days. 

The following image shows how you can create the above segment query using the combination of  AND/OR operators:

<Image alt="Combining AND/OR Operators" align="center" border={true} src="https://files.readme.io/519ac77-Combining_ANDOR_Rules.png">
  Combining AND/OR Operators
</Image>

# Additional Filters

These filters allow customers to segment users based on count, average, or total sum of an event property value.

## Count

It allows customers to filter users by event count. The following query finds all users who performed a *Charged* event greater than five times in the past 30 days:

<Image alt="Filter by Count" align="center" border={true} src="https://files.readme.io/72dc3a3-Count_Filter.png">
  Filter by Count
</Image>

## Total Sum of Property

It allows customers to filter users by the sum of a chosen event property. The following query finds all users who performed a *Charged* event such that the *Revenue* event property is greater than $10:

<Image alt="Filter by Total Sum of Property" align="center" border={true} src="https://files.readme.io/8b92312-image_13.png">
  Filter by Total Sum of Property
</Image>

## Average Sum of Property Filter

It allows you to filter users by the average of a chosen event property. For example, you can filter all the users who performed a *Charged* event with an *Average sum of property* being *greater or equal* to $10. Let us assume that user A performed five *Charged* events each for $8, $9, $10, $11, and $12. Here, the average of property from user A is ($8+9+10+11+12)/5 events = 50/5 = $10 per event, which is equal to $10. As a result, user A will qualify for this segment.

Let us assume that the value for two charged events is missing. The *Charged* event values received are $5, $7, and $13. In this case, the value of the missing events will be considered as 0. As a result, the average of property is now ($5+7+13+0+0)/5 events = 25/5 = $5 per event. As a result, the user will not qualify for this segment.

If you want to exclude all the events that do not have event properties, you can select the property that *exists* as a condition in the *Filter by* section. 

The following query finds all users who performed a *Charged* event such that the *Average sum of property* per event is *greater or equal* to $10:

<Image title="2020-11-24_17-52-22_Average of property.png" alt={1192} align="center" border={true} src="https://files.readme.io/cbadd22-Filter_by_Average_Sum_of_Property.png">
  Filter by Average Sum of Property
</Image>
