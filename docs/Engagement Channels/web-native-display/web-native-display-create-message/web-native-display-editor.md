---
title: Web Native Display Editor
excerpt: >-
  Learn how to leverage Web Native Display Editor for creating personalized
  experiences.
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

The Web Native Display editor offers several templates to personalize your customer's website experiences. For example, you can personalize the banner or banner carousels on your customer's websites based on their past events. These templates are mobile responsive, which means marketers can deliver personalized campaigns across devices (mobiles, tablets, desktops, etc.).

Additionally, CleverTap offers Advanced Personalization tools such as the Visual Editor, which allows you to customize the website's look and feel in real-time through a user-friendly interface and minimal development effort. For more information, refer to [Advanced Personalization](doc:advanced-personalization).

From the What section in the Web Native Display campaign builder, select the message type and click **Go to Editor.** The Web Native Display Editor displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b71dad4-visual_editor.jpg",
        "",
        "Web Native Display Editor."
      ],
      "align": "center",
      "border": true,
      "caption": "Web Native Display Editor"
    }
  ]
}
[/block]


# Basic Templates

The Web Native Display editor offers six basic templates:

- [Custom key values](doc:web-native-display-editor#custom-key-value)
- [Banner](doc:web-native-display-editor#banner)
- [Banner Carousel](doc:web-native-display-editor#banner-carousel)
- [Banner with Text](doc:web-native-display-editor#banner-with-text)
- [Banner Carousel with Text](doc:web-native-display-editor#banner-carousel-with-text)

### Custom Key Value

Marketers can use the custom Key-Value template to deliver an engaging and personalized user experience.  
The custom key value can have any value. 

> 🚧 Note
> 
> The first key of your object will always be **topic**. The marketer can provide the relevant value of this key while configuring the campaign. The developer must use this value to access the right payload for that campaign.

For example, if you want to change the carousel images for your users based on their language and favorite products, you can set the custom key-value pairs for this change.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd5c152-web_native_display_key_value.png",
        "Configure Custom Key-Value Pairs",
        1596
      ],
      "align": "center",
      "border": true,
      "caption": "Define Custom Key-Value Pairs "
    }
  ]
}
[/block]


Refer to the [sample key-value pair web native display campaign](https://developer.clevertap.com/docs/web-native-display#sample-key-value-web-native-display-campaign). It explains the steps you need to perform after creating a campaign in detail.

### Banner

The banner template allows you to create visually appealing banners for your website. You can directly upload the banner image or add a URL to the banner. You also have the flexibility to upload a dedicated image for mobile users to deliver an optimal experience for mobile audiences. 

You must enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.  
You can also provide a URL to redirect users to a specific web page when they click a banner.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/79e565b-banner_1.png",
        "Configuring a Banner Template",
        2558
      ],
      "align": "center",
      "border": true,
      "caption": "Banner Template"
    }
  ]
}
[/block]


### Banner with Text

Similar to the Banner template, the Banner with Text template allows you to create visually appealing banners with personalized messages for contextual communications. Marketers can add Titles and Descriptions to their banners and personalize them to deliver individualized experiences. For example, marketers can target their audience by personalizing names in the banner title for enhanced engagement.

You must enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.  
You can also provide a URL to redirect users to a specific web page when they click the banner.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe8f080-banner_text.png",
        "Setting up a Banner with Text Template",
        2868
      ],
      "align": "center",
      "border": true,
      "caption": "Banner With Text"
    }
  ]
}
[/block]


Under the _Style_ tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. You can also define the font style, size,  and color of the title and description.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/12ecfc1-banner_font_2.png",
        "Style your Banner",
        2544
      ],
      "align": "center",
      "border": true,
      "caption": "Banner with Text Editor"
    }
  ]
}
[/block]


### Banner Carousel

Banner Carousels allow you to display up to seven rotating banners that help you deliver engaging content faster. They primarily let you display broader and more engaging content within a restricted area on your website.

Using the Banner Carousel template, you can create promotional and engaging banner slides that can auto-rotate. You can use this template for various purposes, such as displaying the latest product releases on e-commerce sites, banners of web series on OTT platforms, and displaying festive offers on your application's home page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec98127-banner_carousel_gif_1.gif",
        "Banner with Carousel",
        1272
      ],
      "align": "center",
      "border": true,
      "caption": "Banner with Carousel"
    }
  ]
}
[/block]


Enter the Div ID for the relevant container on your website where you wish to render the banner carousel. Optionally, you can define the Div height to adjust the appearance of the banner carousel.

You can also provide a URL to redirect users to a specific web page when they click a specific banner slide. Additionally, you can use a different image for mobile users to optimize the viewing experience for your mobile audience.

You need to define the _Slider Time_ (in seconds) so that the banner slides auto-rotate after the defined time. You also have the option to enable the _Carousel dots_ and _Navigation arrows_ to scroll banner slides manually.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37db7f7-Screenshot_2022-12-11_at_4.35.07_PM.png",
        "Set the Slider Time for Auto Scroll",
        1454
      ],
      "align": "center",
      "border": true,
      "caption": "Define Scroll Time"
    }
  ]
}
[/block]


### Banner Carousel with Text

This template is similar to the _Banner Carousel_ template with an additional option of adding a Title and Description on top of each banner in the carousel. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3fa56dc-banner_carousel.gif",
        "Set up Banner Carousel with Text Template",
        1264
      ],
      "align": "center",
      "border": true,
      "caption": "Banner Carousel with Text"
    }
  ]
}
[/block]


Under the _Style_ tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. You can also define the font style, size,  and color of the title and description.