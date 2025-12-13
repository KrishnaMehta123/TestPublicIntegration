---
title: Personalize Message
excerpt: >-
  Understand how to personalize Email messages to engage better with your
  audience.
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

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](https://docs.clevertap.com/docs/events#event-properties).

> 📘 Live Campaigns with Delay > 24 hours
> 
> You can apply event personalization to Live Action and Date time campaigns with a delay greater than 24 hours. For example, airlines can now personalize flight check-in reminders by sending them reminders 24-48 hours before departure. Additionally, they can engage users with personalized messaging related to flight experience, hotel bookings, or cab services based on destination from booking details, even beyond the 24-hour window. However, you cannot apply event personalization for Live Inaction campaigns with a delay greater than 24 hours.
> 
> This is a private beta feature.

# Inline Personalization

To invoke the personalization menu, type the _@_ or the \_{{}} \_symbol in the title or the text fields while creating a message.

You can also add dynamic replacements in the title and body. Notice a preview as displayed below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/62c4796-Email_inline_personalization.png",
        "Email Inline Personalization",
        1313
      ],
      "align": "center",
      "border": true,
      "caption": "Inline Personalization"
    }
  ]
}
[/block]


In addition to title, body, you can also personalize many other things such as media URLs, deep links, or button text. An _@ _ icon in a box indicates that it can be personalized. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae0ec11-Personalization_.png",
        "Personalize Media, Links or Button Text",
        748
      ],
      "align": "center",
      "border": true,
      "caption": "Personalize Media, Links or Button Text"
    }
  ]
}
[/block]


# Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

Liquid tags offer great flexibility while composing personalized messages. Liquid tags allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example to send personalized coupon codes based on the type of membership:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed642bf-campaigns_liquid_tags_common_example.png",
        "Campaigns Liquid Tags Common Example",
        1357
      ],
      "align": "center",
      "border": true,
      "caption": "Liquid Tags"
    }
  ]
}
[/block]


Each notification is personalized to the receiver. 

```html Output - Liquid
Hello John!

Here is a special coupon for you: Gold4All
```

For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).

# Linked Content

Linked content provides the ability to personalize emails with rich and contextual data available outside of the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies, and you want to personalize offers to each user based on the weather and location. The location can come from CleverTap personalization, and the weather information can come from an API that provides the current weather. If you want to add more information, you can opt for any source such as third-party tools and in-house software to include in your message.

```liquid
Hi {{ Profile.name | default:"there!" }},

{% if Linked.cityBasedWeather.temp > 30 %}
It is a bright sunny day in {{ Profile.location | default:"your city" }}. How about a barbeque today?

Use the coupon code (BARBQ).
These are the top 5 restaurants near you:
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}


{% elsif Linked.cityBasedWeather.temp < 10 %}
It is indeed cold today in {{ Profile.location | default:"your city" }}!! 
Time for some hot pizza!
                                         
Use the coupon code (PIZZA). These are the top 5 restaurants near you:
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
                                          
{% else %}
                                          
It has  been a while in {{ Profile.location | default:"your city" }}. 
Order something exotic!
                                          
Use the coupon code (EXOTIC).These are the top 5 restaurants near you:           {% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
                                          
{% endif %}
```

For more information, refer to [Linked Content](https://docs.clevertap.com/docs/linked-content#write-linked-content).

# Recommendations

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. For example, you can have a sliding carousel displayed to your customers based on their personal likes!  For more information on recommendations, see [Recommendations](doc:recommendations).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6264702-Recommendation_Sample.png",
        "Display Personalized Recommendations",
        1752
      ],
      "align": "center",
      "border": true,
      "caption": "Create Recommendations"
    }
  ]
}
[/block]


# Catalog

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.  Select a catalog from the list. 

A _Catalog_ provides the ability to personalize campaigns with dynamic information in messages from product prices to inventory levels. You can create a new product catalog by uploading a file that contains one row for each item in your product catalog. A _Catalog_ can be uploaded directly on the CleverTap dashboard via a CSV file that is generated by your inventory management system. For more information on _Catalogs_, see [Catalogs](doc:catalog).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5077276-catalog_sample.png",
        "Personalize Campaigns with Catalogs",
        1560
      ],
      "align": "center",
      "border": true,
      "caption": "Catalog Preview"
    }
  ]
}
[/block]


# Constant event property

Constant Event Property allows you to engage the user on multiple actions and inactions. For example, person A added to cart a white coat and person B added to cart a pair of blue jeans, but they both did not purchase the items. 

You can either create a campaign for each product that was added to the cart or you can use a _constant event property_ to personalize the campaign to each user that did not purchase the item. 

For example, you can map the _prod_name_ property of the _charged_ event to the _product_name_ property of the _added to cart_ event. You can then hold this property constant across both events. Based on this property, you can now personalize the message received by each user. 

 For more information on using a constant event property, see [Constant Event Property](doc:constant-property).