---
title: Personalize Message
excerpt: >-
  Understand how to personalize WhatsApp messages to engage better with your
  audience.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: >-
    Refer to the page listed below to learn more about the following WhatsApp
    section:
---
# Overview

You can personalize the WhatsApp *Header* and message *Body* for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](doc:events).

# Message Personalization

To invoke the personalization menu, type the **@** symbol in the *Header* or the text fields while creating the WhatsApp notification message.

You can also add dynamic replacements in the WhatsApp title and body. Refer to the image below to check the available dynamic replacements for WhatsApp notifications.

<Image title="Whatsapp message personalization" alt={2426} align="center" border={true} src="https://files.readme.io/f7d98fb-Whatsapp_personalization.png">
  Personalize WhatsApp Messages
</Image>

# Liquid Tags

Liquid tags offer great flexibility while composing personalized messages. It primarily allows you to define conditional logic by using a scripting language. This conditional logic can help you dynamically change the look and feel of your message. 

The following use cases can explain using Liquid Tags:

### Sending personalized shipment alerts to users based on their membership

Consider you have an e-commerce template with specific placeholders in the body, as shown below. 

<Image title="Sample E-commerce Template for Shipment Delivery" alt={760} align="center" width="smart" border={true} src="https://files.readme.io/b8ffaab-liquid_personalization_2.png">
  Sample Template for Shipment Delivery
</Image>

You want to define different timelines for shipment delivery based on the customer membership. 

In this case, you can personalize the template message placeholders based on profile and event properties. You can also add conditional logic using liquid tags, as shown below. 

<Image title="Defining Conditional Logic based on customer type using Liquid Tags" alt={2154} align="center" border={true} src="https://files.readme.io/3ed6afa-use_case_1.png">
  Defining Conditional Logic using Liquid Tags
</Image>

In the above example, placeholder \{\{1}} is replaced with a custom profile Name property, and a conditional logic is defined for placeholder \{\{2}}. Per the conditional logic, users having *Prime* membership will receive the shipment in two working days, and standard users will receive the shipment in seven-eight working days.

### Sending Personalized Promo Codes to Users in Specific Cities

Consider you have a promotional e-commerce template with certain placeholders in the message body, as shown below.

<Image title="Sample E-commerce Template for Promotions" alt={1046} align="center" width="80%" border={true} src="https://files.readme.io/b0400b3-basic_ecommerce_template.png">
  Sample E-commerce Template for Promotions
</Image>

You want to send personalized promo codes for users based on their city. 

Similar to the previous use case, you can personalize the message template placeholders based on profile and event properties. You can define conditional logic, too, using liquid tags, as shown below:

<Image title="Defining Conditional Logic based on Geographies for Sending Promo codes" alt={2030} align="center" width="auto" border={true} src="https://files.readme.io/8ed3468-use_case_2.png">
  Conditional logic using liquid tags
</Image>

Defining a conditional logic will dynamically change the promo codes for different users. 

In the above example, placeholder \{\{1}} is replaced with a custom profile Name property, and a conditional logic is defined for placeholder \{\{2}}. As per the conditional logic:

* Customers from Mumbai receive - MUM50 as promo code.
* Customers from Delhi receive - DEL50 as promo code.
* By default, customers receive - IND50 as a promo code.

For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).

# Linked Content

Linked content allows personalizing your messages with media-rich and contextual data available outside the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies, and you want to personalize offers to each user based on the weather and location. The location can come from CleverTap personalization, and the weather information can come from an API that provides the current weather. If you want to add more information, you can opt for any source, such as third-party tools and in-house software, to include in your message.

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

For more information, refer to [Linked Content](doc:linked-content#write-linked-content).

# Catalog

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.  Select a catalog from the list. 

A *Catalog* provides the ability to personalize campaigns with dynamic information in messages from product prices to inventory levels. You can create a new product catalog by uploading a file that contains one row for each item in your product catalog. A *Catalog* can be uploaded directly on the CleverTap dashboard via a CSV file that is generated by your inventory management system. For more information on *Catalogs*, see [Catalogs](doc:catalog).

<Image title="Personalize Campaigns using Catalogs" alt={1560} align="center" border={true} src="https://files.readme.io/5077276-catalog_sample.png">
  Personalize Campaigns using Catalogs
</Image>

# Recommendations

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a [Catalog](doc:catalog), you can display personalized recommendations to your customers. Imagine sending a Web Push notification with shoe recommendations to a user who recently added shoes to their cart but didn't purchase. For more information on recommendations, refer to [Recommendations](doc:recommendations).
