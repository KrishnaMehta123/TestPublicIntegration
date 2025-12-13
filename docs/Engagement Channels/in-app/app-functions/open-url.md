---
title: Open URL
excerpt: Open an external web page or deep-linked screen in the app.
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

Use the Open URL app function to send users to a specific URL. This function supports deeplinks and allows customization with Handlebars for dynamic values, such as user attributes or events. For more information, refer to  [Personalize message content](doc:personalize-message-all).

> 📘 Tip
> 
> Check that the URL is mobile-optimized and uses HTTPS for security.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/052eba4ebfa743926990f29f5b551bd5ca359a4df67b9bb1d3dabac4ae7d8ef3-image.png",
        null,
        "Personalize with @ Personalization and Liquid Tags"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Personalize with Liquid Tags and @ Personalization"
    }
  ]
}
[/block]


# Deeplinks

A deeplink is a direct link to a specific location inside your app.

For Example, you have an e-commerce app, and want to send your users a push notification when there is a deal on a popular item. You might have a deeplink schema such as this, where _productID_ can be replaced with an actual ID to send a user directly to a specific product page

# Dynamic links

You can make your links, even deeplinks, dynamic based on a User Attribute or Parameter values.  
Using CleverTap's [Liquid Tags](doc:liquid-tags) and [@ Personalization](doc:personalize-message-all) functionality, you can populate the productID dynamically. However, you must send the product ID as a parameter value of the event that triggers the push notification. For example, you might want to send the user to a product they have previously viewed. 

You now have a message that always leads a user to the product they were recently viewing, resulting in a highly personalized experience.

# Considerations

The following are the system considerations:

- URL opens immediately on tap.
- Campaign-level analytics track only the In-App click or view, not the destination behavior.