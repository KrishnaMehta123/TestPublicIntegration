---
title: Create Campaigns using Recommendations
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

Once the recommendations have been published, you can use them in your engagement workflow by [creating personalized and contextual recommendations](https://docs.clevertap.com/docs/creating-a-recommendations) for your user base.

> 📘 Note
> 
> Recommendations are supported for all channels.

# Access Recommendations Within a Campaign

During the campaign creating in the _What_ section, access recommendations with the following steps:

1. Type the @ symbol to personalize your message. 
2. Click **Recommendations**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd5f606a034c27e36fe0ce8ae314119fd5af253667439185712100f327a9399c-image_5.png",
        "+Create Recommendation Content",
        667
      ],
      "align": "center",
      "border": true,
      "caption": "Create Recommendation Content"
    }
  ]
}
[/block]


# Create Recommendation Content

To create recommendation content, perform the following steps:

1. Select a recommendation from a list of recommendations that have already been published and the event that you want to trigger the recommendation.

> 📘 Event Selection
> 
> You can only select events you mapped to the catalog on which the chosen recommendation is running.

2. (Optional) Filter recommendations by event: 
   1. Click **+ Filter by event**.
   2. Select whether you want to include or exclude an event and categories.
   3. Add more events if required. 

> 📘 How the Filter by Event Works
> 
> The filter by event takes precedence over recommended items and selected events matching. It provides the capability to include and exclude all recommended items when an item in the product catalog column matches a defined event property.

3. (Optional) Filter recommendations by location:
   1. Click **+ Filter by location**.
   2. Select a product location catalog and a radius.
   3. Add more locations if required.

> 📘 How the Filter by Location Works
> 
> The filter by location takes precedence over the location of the recommended items which are fetched from the location catalog. Items in a defined range are looked up with the associated product location catalog and matched with the user's last known location to be included in the filter.

4. Decide the sequence of items to be served up to the user out of the list of items that can be recommended (for example, serve up the first item from the list of recommended items).
5. Click **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b772b6c-Enhanced_recommendations_with_both_catalogs.png",
        "Enhanced Recommendations with both Catalogs",
        1956
      ],
      "align": "center",
      "border": true,
      "caption": "Enhance the Recommendations with both Catalogs"
    }
  ]
}
[/block]


> 📘 Web Popup Campaign Preview
> 
> In case of Web Popup campaign preview, CleverTap does not support recommendations.

# Choose the Fields to Personalize your Message

Now that you have created a recommendation, use the following steps to finalize your content:

1. Choose the particular fields from the catalog that you want to use in your personalized message.
2. Enter your content in the title and message.

When the campaign is sent out, the fields will be replaced and the message will contain the personalized fields for each product. 

> 👍 Video Example
> 
> You can send out a recommended video to the user with the video name and thumbnail image based on the last videos a user has watched.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b47dbcdbab9b3f8afb1339d0ea79ad3c5130182ab1776def721cf1f48db0b160-image_7.png",
        "Select Catalog Field to Map",
        475
      ],
      "align": "center",
      "border": true,
      "caption": "Select Catalog Field to Map"
    }
  ]
}
[/block]


3. Send a test campaign to yourself to see the look and feel of the campaign. The test message will show the first item in the recommendation list.
4. Once you are done testing, publish the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81d8d588f36c2a9d2e7257f6a7c8851bc4efaae734e88bcc347ea226ee014777-image_8.png",
        "Preview the Campaign",
        328
      ],
      "align": "center",
      "sizing": "30% ",
      "border": true,
      "caption": "Preview the Campaign"
    }
  ]
}
[/block]


## Email Campaigns with Recommendations

You can create email campaigns with recommended content by invoking recommendations within the email messages. Beyond this part, all the steps are the same as the generic ones described in the sections above. 

You can create emails using:

- New email with rich media
- Templates

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0dbaef6b2bb18dcbcf3ff45976bfddcf15aa991f3a252fc9ea20250bc985d75e-image_9.png",
        "Create Email Campaigns with Recommendations",
        1597
      ],
      "align": "center",
      "border": true,
      "caption": "Create Email Campaigns with Recommendations"
    }
  ]
}
[/block]


## Recommendations using a New Email with Rich Media

You can create personalized recommendations using a new email with media with the steps below.

### Link with Recommendations

You can add recommendations within links with the following steps:

1. Click on the link icon to add a link to your email message.
2. Type the @ symbol to personalize the link using recommendations in the display text and the URL fields.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94cad613b7769f2701cb3e1b8ce627103da80c01ecb746731d35a96e894ecda0-new1.gif",
        "Create Link with Recommendations",
        1591
      ],
      "align": "center",
      "border": true,
      "caption": "Create Link with Recommendations"
    }
  ]
}
[/block]


### Image with Recommendations

You can also add recommendations within images with the following steps:

1. Click on the image icon to add an image to your email message.
2. Type the @ symbol to personalize the link using recommendations in the URL and the alternative text fields.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/330e9d1e51bfb0f9cef3e7de3ac78f2ed19157600a09cf835c4b2309cd577048-new23.gif",
        "Create Image with Recommendations",
        1591
      ],
      "align": "center",
      "border": true,
      "caption": "Create Image with Recommendations"
    }
  ]
}
[/block]


The remainder of the steps is the same as any other campaigns as explained in the sections above.

## Recommendations in Template Emails

You can create personalized recommendations using template emails with the steps below.

### Links, Images, Deeplinks, and Custom HTML with Recommendations

You can add recommendations within links, images, deeplinks, and custom HTML with the following steps:

1. Drag and drop the _Dynamic Content_ block into the content box in the center of the email body.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b60558056222abc47ad9337a561beacc4396b17f966843f731eb112a7cd8a706-newww0000.gif",
        "Dynamic Content button.png",
        1610
      ],
      "align": "center",
      "border": true,
      "caption": "Add Recommendations within Links, Images, Deep-links, and Custom HTML"
    }
  ]
}
[/block]


2. Click on the new content box to display the menu on the right.
3. Click on the **Add options** button to access the dynamic content options. 
4. When the window pop-up displays, select one of the following options:

- Image
- Deeplink
- Text
- Custom HTML

> 📘 Option Name Required
> 
> When you create a dynamic block, the option name is mandatory. Also, these dynamic blocks can be re-used if required.

#### Image with Recommendations

Type the @ symbol to personalize the image content using recommendations in the URL, alternative text, and target URL fields.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d86281691cd9570d8e42da21894995301473f270fad755318eb192a80a539be5-photo.png",
        "Personalize Image Content using Recommendations",
        643
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Personalize Image Content using Recommendations"
    }
  ]
}
[/block]


#### Deeplink with Recommendations

Type the @ symbol to personalize the deeplink content using recommendations in the display text and URL fields.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4278fd052690508381636ec08605359cb8d85935dab878ac78ab088319959b82-2025-02-11_17-03-37.png",
        "Personalize Deeplink Content using Recommendations",
        644
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Personalize Deeplink Content using Recommendations"
    }
  ]
}
[/block]


#### Text with Recommendations

Type the @ symbol to personalize the text content using recommendations in the text field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/796765ad2336362a5e78c9096d540c3e345bc2288a9d9691e7ea5103323c923a-2025-02-11_17-04-21.png",
        "Personalize Text Content using Recommendations",
        671
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Personalize Text Content using Recommendations"
    }
  ]
}
[/block]


#### Custom HTML with recommendations

Type the @ symbol to personalize the custom HTML content using recommendations in the custom HTML code box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ade4883507116312ba863b6797affc4924862ec90e4b01bdadc79417c3ebb108-2025-02-11_17-05-00.png",
        "Personalize Custom HTML Content using Recommendations",
        638
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Personalize Custom HTML Content using Recommendations"
    }
  ]
}
[/block]


### Existing Text Content Type in the Template Containing Deeplinks with Recommendations

You can access recommendations within the existing text content type with the following steps:

1. Drag and drop the _Text_ block into the content box in the center of the email body.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46a314eb544e6377897cb49c811240181e53bd0dac8a9d8446a5f6f28e3e089d-2025-02-07_20-06-11_1.gif",
        "Dynamic Content button.png",
        1610
      ],
      "align": "center",
      "border": true,
      "caption": "Create Personalized Deeplinks"
    }
  ]
}
[/block]


2. Click on the content box to display the menu.
3. Click **More** > **Personalized Deeplink**.
4. Type the @ symbol to personalize the deelink content using recommendations in the display text and URL fields.

Maximize your [Location-Based Marketing](https://clevertap.com/blog/location-based-marketing-guide/) with best practices and strategies to deliver targeted messages to users based on their physical location.