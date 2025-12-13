---
title: Exporting Data for Risk-Ratio Analysis
excerpt: Learn how to export data from CleverTap to perform a Risk-Ratio Analysis.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

The [Risk-Ratio template](https://docs.google.com/spreadsheets/d/1Hx5IB1Y0EFv30QZAO3fpEqA3E9SuMnqMESMTvU1wYLw/edit?usp=sharing) was pioneered by data expert [Crystal Widjaja](https://www.reforge.com/profiles/crystal-widjaja?utm_source=clevertap) at Reforge to help discover valuable insights that can improve your app engagement and increase conversions. It can help you understand the relationship between your user actions. For example, an e-commerce app may want to know the relationship between user behavior actions such as _Added to Cart_, and a goal such as _Charged_.

This document guides you through using behavioral data from CleverTap and visualizing the results using the risk-ratio template.

> 📘 Register for CleverTap Account
> 
> If you are not already a CleverTap subscriber, you can explore [CleverTap Pricing Plans](https://clevertap.com/pricing/?utm_source=readme&utm_medium=banner&utm_campaign=risk-ratio-doc) or schedule a demo to learn more.

You can also refer to the video tutorial for exporting user profile data for risk ratio analysis using CleverTap.

[block:html]
{
  "html": "<div\n              style=\"\n                position: relative;\n                padding-bottom: 56.25%;\n                height: 0;\n                border-radius: 0;\n                box-shadow: 0 15px 40px rgba(63,58,79,.3);\n                overflow: hidden;\n                min-width:320px\"><iframe\n              src=\"https://clevertap.portal.trainn.co/share/SguGFSXOboAMJsMlg9PbFQ/embed?autoplay=false\"\n              frameborder=\"0\"\n              webkitallowfullscreen\n              mozallowfullscreen\n              allowfullscreen\n              allow=\"autoplay; fullscreen\"\n              style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe></div>"
}
[/block]


# Create Behavioral Attributes

You can set up CleverTap Journeys to model the data exactly as expected in the Risk-ratio template.  A Past Behavior journey with a  _User Profile Update_ controller node helps generate each of the attributes as listed in the following table:

| Journey   | CleverTap User Event | Risk-ratio Attribute | Description                                                                                         |
| :-------- | :------------------- | :------------------- | :-------------------------------------------------------------------------------------------------- |
| Journey 1 | Added to cart        | Y Behavior           | This attribute counts the number of _Added to cart_ actions for a user.                             |
| Journey 2 | Charged              | Z Goal               | A successful conversion is represented as **1**, while a failed conversion is represented as **0**. |

> 📘 Note
> 
> You can update any existing user property or create one using [CSV Upload](doc:csv-upload).

# Create Journey for Y Behavior

You can analyze the _Added to cart_ event in CleverTap as Y behavior action in the Risk-ratio template. Create a journey to capture all the segments for the _Added to cart_ event, where the count is zero, one, two, three, four, five, six, seven, and eight or more. The user property  _y_behavior_count_ will track the count for each Added to Cart event instance. An   _Update user profile_ controller node is used to increment the value from zero to eight for each _Added to cart_ event. 

To create a journey for Y Behavior:

1. Navigate to Journeys from the CleverTap dashboard.
2. Set up the Journey using a _Past Behavior_ user segment.
3. Add a Past Behavior node as the Entry Segment to qualify all users who have performed the _Added to cart_ event.
4. Add a Past Behavior segment where users have added to the cart and the count is 0. 

   [block:image]{"images":[{"image":["https://files.readme.io/61e446e46c1e7f46277b9e587d8822316e92ea4118657bf725bfc9e5026fb1da-Add_a_Past_Behavior_Segment_-_Y_attribute.png","","Add a Past Behavior Segment - Y attribute"],"align":"center","sizing":"75% ","border":true,"caption":"Add a Past Behavior Segment - Y attribute"}]}[/block]

   1. Connect an Update user profile node. Set the   y_behavior_count  to 0.  

      [block:image]{"images":[{"image":["https://files.readme.io/d10796d0605d8eb2519848300e4a6bfa3327c4a94c699913451481574df053fe-Set_count_in_Profile_Update_node_-_Y_Behavior.png","","Set count in Profile Update node - Y Behavior"],"align":"center","border":true,"caption":"Set count in Profile Update node - Y Behavior"}]}[/block]
5. Add more segment nodes to the journey, incrementing the count for the _Added to cart_ event by 1 each time.

   1. Connect an _Update user profile_ node to each segment node. Increment the   y_behavior_count  by 1 subsequently.  The following image shows a sample Y Behavior journey:

   [block:image]{"images":[{"image":["https://files.readme.io/3831f5eff58df616ff11c9e7f7d8642aa0d34b4f4d6f9b4735a25f74627b1a29-image.png",null,"Sample Y Behavior Journey"],"align":"center","border":true,"caption":"Sample Y Behavior Journey"}]}[/block]

> 📘 Connect Segment and Profile Update Nodes
> 
> Connect all Segment nodes via the _No_ path and all the Profile update nodes via the _Yes_ path.

# Create Journey for Z Goal

You can now create a similar journey for a Z goal in CleverTap. A _Charged_ event indicates that the user has purchased the item. The value for the Z goal is boolean. If the user purchases the item, _Charged_ is marked as _1_; if the user does not purchase, _Charged_ is marked as _0_. 

The entry criteria for this Journey will be a Past Behavior segment. It includes users who have purchased an item at least once. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9642ab67519799f77de364c8f273b6b2ec14eca60a73db5b8d0f00ff27df64b-Add_a_Past_Behavior_Segment_-_Z_attribute.png",
        null,
        "Add a Past Behavior Segment - Z attribute"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Add a Past Behavior Segment - Z attribute"
    }
  ]
}
[/block]


This journey will have two updated user profile nodes: _Z Goal=1_ and _Z Goal = 2_. The _Z Goal = 1_ node records the count for all the instances where the user performed the _Charged_ event. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/52ba45a6e4bcf70ccf2b0476907ffeb85a90494e72970ab9974b64f22b39dc7f-Set_count_in_Profile_Update_node_-_Z_Behavior.png",
        null,
        "Set count in Profile Update node - Z Behavior"
      ],
      "align": "center",
      "border": true,
      "caption": "Set count in Profile Update node - Z Goal"
    }
  ]
}
[/block]


The _Z Goal = 2_ node records the count for all instances where the user did not perform the _Charged_ event. The following image shows a sample Z Goal journey:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cf26b49053d57c5e15fbd2a29b6ddc3bf41e681b22d212a650d654f2de0c1673-Sample_Z_Behavior_Journey.png",
        null,
        "Sample Z Behavior Journey"
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Z Goal Journey"
    }
  ]
}
[/block]


# Export Data

Export the _Y behavior_ and _Z goal_ count from the CleverTap dashboard. After the download, you can copy and paste the information from the downloaded CSV file to the Risk-ratio template.  

1. Go to _Segments_ > _Find People_.
2. Under _Display common properties such as_ section, search for _z_goal_count_ and _y_behavior_count_ properties. 
3. In the _Reachability_ section, click the ![](https://files.readme.io/ce23ad296e6e1b62e130e20b29590b003a4609141f35e71fa7c0ae79a5236e00-Download_icon.png) icon. A window with the user attributes appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/31b1fde5d766af9ea296ff65e292a93199e0b091fd7d5542245d577809f182da-Export_Attribute_Data.png",
        null,
        "Export Attribute Data"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Attribute Data"
    }
  ]
}
[/block]


3. Select all the attributes.
4. Click **Proceed**. After the download is completed, you will receive an email with a download link for the selected properties. You can also go to _Settings_ > _Downloads_ and access this downloaded file on the CleverTap dashboard. 

# Analyze Risk Ratio

Once you have the CSV file, you can copy-paste the required data into the risk ratio template. To analyze the risk ratio, copy the  _CleverTap Id_, _Y Behavior_, and _Z Goal_ columns to the respective[ Risk Ratio Template](https://docs.google.com/spreadsheets/d/1Hx5IB1Y0EFv30QZAO3fpEqA3E9SuMnqMESMTvU1wYLw/edit?usp=sharing) columns. 

The template will automatically populate with calculations for performing risk ratio analysis.

For further assistance, contact [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).