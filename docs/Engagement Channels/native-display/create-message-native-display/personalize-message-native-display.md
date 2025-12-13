---
title: Personalize Message
excerpt: >-
  Understand how to personalize Native Display messages to engage better with
  your audience.
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

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](https://docs.clevertap.com/docs/events#event-properties).

# Inline Personalization

To invoke the personalization menu, type the *@* or the \_\{\{}} \_symbol in the title or the text fields while creating a message.

You can also add dynamic replacements in the title and body. Notice a preview as displayed below.

<Image title="Native Display Personalization.png" alt={1520} align="center" border={true} src="https://files.readme.io/720126f-Native_Display_Personalization.png">
  Inline Personalization
</Image>

In addition to the title, body, you can also personalize many other things, such as media URLs, deep links, or button text. An *@* icon in a box indicates that it can be personalized. 

# Recommendations

Click the ![](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. For example, you can display a sliding carousel to your customers based on their likes!  For more information on recommendations, see [Recommendations](doc:recommendations).

<Image title="Recommendation_Sample.png" alt={1752} align="center" border={true} src="https://files.readme.io/6264702-Recommendation_Sample.png">
  Catalog Based Recommendation
</Image>

# Linked Content

Linked content provides the ability to personalize messages with rich and contextual data available outside of the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies and want to personalize offers to each user based on the weather and their location. The location can come from CleverTap personalization, and the weather information can come from an API that provides the current weather. If you want to add more information, you can opt for any source, such as third-party tools or in-house software, to include in your message.

For more information, refer to [Linked Content](doc:linked-content).
