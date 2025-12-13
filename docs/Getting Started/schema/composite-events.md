---
title: Composite Events
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

Composite events provide you the ability to combine multiple events. A composite event can be used as a single event on the dashboard which can be analyzed in reports.  

> 👍 Composite Events Examples
> 
> Some examples include:
> 
> - The _Video played_ and _Song played_ events can be combined into a single event called _Content consumed_.
> - You may group _Item purchased_ and _Subscription created_ into a new composite event called _Money spent_.

# Create a Composite Event

To create a composite event, perform the following steps:

1. Navigate to _Settings_ > _Schema_ > _Composite Events_. The _Composite Events_ page displays. 
2. Click the **Add composite event** button. 
3. Name your event and select the events that you want to group together. In our example, we name the event as _Travel Bookings_. 
4. Select the events and filter by properties, if required. In our example, we filter the _Hotel Booked_ event by the event property _Rating_ which is 3 stars and flight booked event by the event property _Class_ (_Economy_).  

> 📘 Additional Events
> 
> You can add any additional events (if required) or save the new composite event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06128bd-Events_Composite_Create.png",
        "Set Up Composite Event Options and Click Save",
        619
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Set Up Composite Event"
    }
  ]
}
[/block]


> 📘 Considerations
> 
> Consider the following:
> 
> - You can combine existing events into a new composite event. 
> - This event does not add to the event storage limit. 
> - This event adds to the global event limit.
> - You can have a maximum of 20 underlying events in a composite event.

# Delete a Composite Event

To delete a composite event, perform the following steps:

1. Click the ellipsis.
2. Click the **Delete** icon to delete the composite event. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ee75996-1_Delete_composite_event.png",
        "Click the Ellipsis Icon and Delete a Composite Event",
        1401
      ],
      "align": "center",
      "border": true,
      "caption": "Delete a Composite Event"
    }
  ]
}
[/block]


# Create a Composite Event Property

Now that you have created a composite event, you can create a composite property using the properties of the underlying events. You can create a composite event property by grouping together two or more underlying event properties. After they are grouped together, they behave as a single event property. 

For example, we create an event property called _Booking_ revenue that groups the underlying properties such as _Flight_ booked amount (from flight booked event) and _Hotel_ booked amount (from the hotel booked event). When you analyze the _Booking_ revenue property, it will function as a single event property. 

You can add composite event properties from the _Composite Events_ page. 

To add a composite event property, perform the following steps:

1. Click the **Add property** link for the required composite event from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21d4852-2_Add_property.png",
        "Click +Composite Event",
        1401
      ],
      "align": "center",
      "border": true,
      "caption": "Composite Event Property"
    }
  ]
}
[/block]


2. Click the **Property** button and select _Add composite property_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ec7b45-Events_Composite_Add_Property_compsite_and_single.png",
        "Click the Property Button and Select Add Composite Property",
        1178
      ],
      "align": "center",
      "border": true,
      "caption": "Add Property"
    }
  ]
}
[/block]


3. Select the properties to be added from the underlying events.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5837078-Events_Composite_Add_composite_properties.png",
        "Map Event Property to the Composite Property and Click Save",
        593
      ],
      "align": "center",
      "border": true,
      "caption": "Map Event Property to Composite Property"
    }
  ]
}
[/block]


4. Click **Save**. 

You can now start using this composite property instead of two separate underlying properties. For example, you can view a trend of the _Booking Revenue_ property in the [Trends](doc:trends#view-a-trend) report. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cfea8e2-Events_Composite_Trend.png",
        "Click Properties Tab and Click View Trend",
        1172
      ],
      "align": "center",
      "border": true,
      "caption": "View Trend"
    }
  ]
}
[/block]


# Add an Individual Event Property

You can choose to add any of the properties that belong to any of the underlying events as an individual property to the composite event. 

The composite event behaves as a single event and this individual property behaves as its underlying property. Therefore, you can stop referencing the underlying event just to analyze a specific property. 

For example, if you want to analyze an event called _Flight Class_ from the flight booked event, you can add this event to the main composite event _Travel Bookings_, then use it as if it is an underlying property of this event. You do not need to use the Flight Booked event because the new composite property offers you a better view of your events. 

You can add event properties from the _Composite Events_ page. 

To add a composite event property, perform the following steps:

1. Click the **Add property** link for the required composite event from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73bae29-Events_Composite_Create.png",
        "Set Composite Event Property Options and Click Save",
        613
      ],
      "align": "center",
      "border": true,
      "caption": "Add Composite Event Property"
    }
  ]
}
[/block]


2. Click the **Property** button on the top and select _Add property_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4607f7d-Events_Composite_Add_Property_Single.png",
        "Click the Property Button and Select Add Property.",
        1180
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Add Property"
    }
  ]
}
[/block]


3. Select the property to be added from the underlying event.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eba39db-Events_Composite_Add_single_property.png",
        "Select the Property to be added from the Underlying Event",
        517
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Add Property to Event"
    }
  ]
}
[/block]


4. Click **Save**. 

You have now grouped the underlying properties together. 

> 🚧 Composite Events Limitations
> 
> - Composite events cannot be split by their event properties in Pivots, Trends, and Funnels.
> - Composite events are not available for Intent Based Segments, Trigger Events in Campaigns (Live Behavior Segment), Flows, mapped events in Catalogs, Recommendations, and Bulletins. 
> - Composite events cannot be exported using AWS S3 and GCP export feature.