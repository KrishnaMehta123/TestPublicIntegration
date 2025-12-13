---
title: Personalize Message
excerpt: >-
  Understand how to personalize Web Inbox messages to engage better with your
  customers
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

You can personalize the web inbox message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](doc:user-profiles) and [Events](doc:events#event-properties).

# Inline Personalization

Type the _@_ symbol in the _Title_ or _Description_ fields to invoke the personalization menu when creating a message. The menu allows you to personalize the messages based on user and event properties.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72ec66e-web_inbox_personalization.png",
        "Personalize Web Inbox Messages",
        1532
      ],
      "align": "center",
      "border": true,
      "caption": "Personalize Messages"
    }
  ]
}
[/block]

In addition to the title and description, you can personalize image URLs, deep links, or button text. An _@_ icon against any field indicates that you can personalize that field.

# Liquid Tags

Liquid tags offer great flexibility when composing personalized messages. They allow adding logic using a scripting language, which you can leverage to change the look and feel of your message.

Click the  `{{ }}` icon in the editor to start liquid scripting.

 Following is an example to send personalized coupon codes based on the type of membership:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03628fb-Liquid_Tags.png",
        "Define Conditional Logic using Liquid Tags",
        1134
      ],
      "align": "center",
      "border": true,
      "caption": "Define Conditional Logic Using Liquid Tags."
    }
  ]
}
[/block]

Each notification is personalized to the receiver, as shown in the following example. 

```html Output - Liquid
Hi John!

Here's a special code for you - MUM50
```

For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).