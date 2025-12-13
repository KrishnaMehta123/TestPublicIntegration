---
title: Catalog Send-Time Personalization
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

Catalog send-time personalization provides the ability to personalize messages with external data pulled from an uploaded catalog at the time a campaign is sent. Automatically include dynamic information available in the catalog directly in a message such as product price, product category, available inventory levels, and more. 

> 👍 E-commerce App Example
> 
> A user adds a laptop to the cart, then exits. By providing additional details in the engagement message such as the image, size, latest price, and specifications of the laptop, the user can be nudged to purchase the item. Using catalog send-time personalization helps keep users engaged in a meaningful way.

After you have uploaded the catalog, you can start using it in a campaign. For more information, refer to [Catalog](https://docs.clevertap.com/docs/catalog).

# Event Property

Follow the steps below to personalize a catalog by event property:

1. Create a [campaign](doc:intro-to-campaigns).

2. Click the **Personalization** link to select a catalog. Once the personalization setup window displays, you can map the required catalog columns to event properties and user properties. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a68d9c-Catalog_Send_Time_Personalization.png",
        "Create Push Notification",
        2878
      ],
      "align": "center",
      "border": true,
      "caption": "Create Push Notification"
    }
  ]
}
[/block]


3. Click the **Catalog** tab and select the required catalog from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1266641-Catalog_Personalization.png",
        "Select the Catalog",
        1898
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select the Catalog"
    }
  ]
}
[/block]


4. Select the event. You can personalize your message based on the property values of this event. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be98af1-Select_Catalog_Send-Time_Values.png",
        "Select Catalog Send-Time Values",
        1894
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select the Catalog Send-Time Values"
    }
  ]
}
[/block]


> 📘 Recent Occurrence
> 
> The most recent occurrence of the event is used to select the relevant item from the catalog. If the campaign is a triggered campaign, then the event that triggered the campaign is considered.

5. Select the event property to map to the catalog column. This mapping is important to identify the catalog column that matches the event property. For example, we map _Product Name_, such as a laptop (from the _Viewed_ event) to the _Name_ column in the catalog. 

Repeat this step to map more properties. 

> 📘 Map Multiple Properties
> 
> - If required, map multiple properties. Every addition to the mapping is treated as an _and_ condition. For example, map the name, the color, and the brand to personalize the message for the user.  
> - Catalog mapping is not supported for the items stored in the `Charged.Items` array.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fad7eeb-Map_Catalog_Columns.png",
        "Map Event to the Catalog Columns",
        1896
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Map Event to the Catalog Columns"
    }
  ]
}
[/block]


6. Click **Save** to set up the personalization. 

7. Use [liquid tags](doc:liquid-tags) to create a personalized message for your target audience. 

In this example, the syntaxes for using different catalog columns are shown below:

```liquid Liquid Tag
{{ Catalog.["Sample Catalog"].Name | default: "Laptop" }}
{{ Catalog.["Sample Catalog"].Amount | default: "0" }}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3069384-catalog_personalization_liquid_message.png",
        "Create Message using Liquid Tags",
        1173
      ],
      "align": "center",
      "border": true,
      "caption": "Create Message using Liquid Tags"
    }
  ]
}
[/block]


You can now use the latest amount for the last added to cart item, such as the laptop. 

# User Property

Follow the steps below to personalize a catalog by user property:

1. Create a [campaign](doc:intro-to-campaigns).
2. Click the **Personalization** link to select a catalog. After the personalization setup window displays, you can map the required catalog columns to event properties and user properties. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e5be68-Catalog_Send_Time_Personalization.png",
        "Create a Push Notification",
        2878
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Push Notification"
    }
  ]
}
[/block]


3. Click the **Catalog** tab and select the required catalog from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18b28fa-Catalog_Personalization.png",
        "Select a Catalog",
        1898
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select a Catalog"
    }
  ]
}
[/block]


4. Select the user property to map to the catalog column. For example, you can recommend the top restaurant in New York with rich details about the restaurant from the catalog to a user with the user property _City_ set as New York. 

> 📘 Note
> 
> If required, map multiple properties. Every addition to the mapping is treated as an _and_ condition. For example, map the city, the top-rated restaurants, and the Chinese restaurants to personalize the message for the user.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f75e23-Map_Catalog_Columns_Event_Property.png",
        "Map Catalog Columns to Event Property",
        1900
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Map Catalog Columns to Event Property"
    }
  ]
}
[/block]


5. Click **Apply** to set up the personalization. 
6. Use [liquid tags](doc:liquid-tags) to create a personalized message for your target audience. 

In this example, the syntax for using a catalog column is shown below:

```liquid Liquid Tag
{{ Catalog.Sample_Catalog.["City Restaurants"] | default:"New York Top Restaurant" }}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc955ed-catalog_personalization_liquid_message_User_property.png",
        "Create Message using Liquid Tag",
        1081
      ],
      "align": "center",
      "border": true,
      "caption": "Create Message using Liquid Tag"
    }
  ]
}
[/block]


> 📘 Map Multiple Properties
> 
> Create personalization by combining catalog send-time personalization with [constant event property](https://docs.clevertap.com/docs/constant-property#section-advanced-constant-property-with-catalog-personalization).

# Video Tutorial

For further information, you can watch the following video on catalog send-time personalization:

[block:embed]
{
  "html": "<iframe class=\"embedly-embed\" src=\"//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2FTVltd1_rpG4%3Ffeature%3Doembed&display_name=YouTube&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DTVltd1_rpG4&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2FTVltd1_rpG4%2Fhqdefault.jpg&key=7788cb384c9f4d5dbbdbeffd9fe4b92f&type=text%2Fhtml&schema=youtube\" width=\"854\" height=\"480\" scrolling=\"no\" title=\"YouTube embed\" frameborder=\"0\" allow=\"autoplay; fullscreen; encrypted-media; picture-in-picture;\" allowfullscreen=\"true\"></iframe>",
  "url": "https://www.youtube.com/watch?v=TVltd1_rpG4",
  "title": "Product Demo: Send-Time Personalization",
  "favicon": "https://www.google.com/favicon.ico",
  "image": "https://i.ytimg.com/vi/TVltd1_rpG4/hqdefault.jpg",
  "provider": "youtube.com",
  "href": "https://www.youtube.com/watch?v=TVltd1_rpG4",
  "typeOfEmbed": "default"
}
[/block]