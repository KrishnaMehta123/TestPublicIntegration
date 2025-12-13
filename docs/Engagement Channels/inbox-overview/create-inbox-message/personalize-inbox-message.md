---
title: Personalize Message
excerpt: >-
  Understand how to personalize Inbox messages to engage better with your
  customers.
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

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](doc:user-profiles) and [Events](doc:events#event-properties).

# Inline Personalization

To invoke the personalization menu, type the @ or the {{}} symbol in the title or the text fields while creating a message.

You can also add dynamic replacements in the title and body. Notice a preview as displayed below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a2053c-Inline_Personalization.png",
        null,
        "Inline Personalization"
      ],
      "align": "center",
      "border": true,
      "caption": "Inline Personalization"
    }
  ]
}
[/block]


In addition to the title and body, you can personalize many other elements such as media URLs, deep links, or button text. An @ icon in a box indicates that this element can be personalized.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24a7d9f-image.png",
        null,
        "Personalize Media URL"
      ],
      "align": "center",
      "border": true,
      "caption": "Personalize Media URL"
    }
  ]
}
[/block]


# Identity Personalization

Identity personalization in CleverTap enables you to tailor user experiences and messaging based on individual user identities, such as email ID, identity, and phone number. For example, you are a streaming platform and you want to send a campaign offering a 50% discount on the first-month subscription. The campaign would target users who have registered with a mobile number but have not subscribed to premium content. In this case, you can use the identity personalization as follows:  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a29c3e-Identity_Personalization.png",
        null,
        "Identity Personalization Example"
      ],
      "align": "center",
      "border": true,
      "caption": "Identity Personalization Example"
    }
  ]
}
[/block]


> 📘 Key Points to Remember
> 
> In the cases where mulitple identiites are present, the most recent identity value is used and the notification is sent with those values.

When crafting any campaign message, you can leverage identity personalization by typing @ or the {{}} symbol in the title or text fields (refer to the following images).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c348477-Indentity_Personalization_usind_Personalization.png",
        "",
        "Identity Personalization Using @Personalization"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Identity Personalization Using @Personalization"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fb69862-Identity_Personalization_Using_Liquid_Tags.png",
        "",
        "Identity Personalization Using Liquid Tags"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Identity Personalization Using Liquid Tags"
    }
  ]
}
[/block]


> 📘 Key Points to Remember
> 
> In the cases where multiple identities are present, the most recent identity value is used and the notification is with that value.

# Liquid Tags

Liquid tags offer great flexibility when composing personalized messages. Liquid tags allow adding conditional logic using a scripting language, which can be leveraged to change the look and feel of your message.

Following is an example to send personalized coupon codes based on the type of membership:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae59bbe-image.png",
        null,
        "Sample Liquid Tag"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Sample Liquid Tag"
    }
  ]
}
[/block]


The following is a preview of the final message. Each notification is personalized to the receiver:

```Text Liquid Tags Output
Hello John!

Here is a special coupon for you: Gold4All
```

For more information, refer to [Liquid Tags](doc:liquid-tags).

# Linked Content

Linked content allows personalized notifications with rich and contextual data available outside of the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies, and you want to personalize offers to each user based on the weather and location. CleverTap can personalize based on location, and the weather information can come from an API that provides the current climate. If you want to add more information, you can opt for any source, such as third-party tools and in-house software, to include in your message. Following is an example of personalizing a message based on the weather conditions received from a weather API. For example, send a message to try a barbeque restaurant if the temperature is greater than 30 degrees, and try a hot pizza if the temperature is lower than 10 degrees.

```Text Linked Content
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

For more information, refer to [Linked Content](doc:linked-content-url-personalization).

# Campaign ID Personalization

When creating a message, type the @ or the {{}} symbol to invoke the personalization menu in the title, message, and Deep link/Open URL fields. Campaign ID Personalization allows you to customize and personalize your marketing campaigns based on specific campaign IDs. For example, you can send a follow-up email with personalized recommendations related to the products or services featured in the user's previous campaign interaction.

For more information, refer to [Campaign ID Personalization](doc:campaign-id-personalization).