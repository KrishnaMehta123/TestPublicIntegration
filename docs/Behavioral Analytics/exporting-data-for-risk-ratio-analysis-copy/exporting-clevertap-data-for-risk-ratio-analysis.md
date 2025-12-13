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

The [Risk-Ratio template](https://docs.google.com/spreadsheets/d/1Hx5IB1Y0EFv30QZAO3fpEqA3E9SuMnqMESMTvU1wYLw/edit?usp=sharing) was pioneered by data expert [Crystal Widjaja](https://www.reforge.com/profiles/crystal-widjaja?utm_source=clevertap) at Reforge to help discover valuable insights that can improve your app engagement and increase conversions. It can help you understand the relationship between your user actions. For example, an e-commerce app may want to know the relationship between user behavior actions such as *Added to Cart*, and a goal such as *Charged*.

This document guides you through using behavioral data from CleverTap and visualizing the results using the risk-ratio template.

> 📘 Register for CleverTap Account
>
> If you are not already a CleverTap subscriber, you can explore [CleverTap Pricing Plans](https://clevertap.com/pricing/?utm_source=readme\&utm_medium=banner\&utm_campaign=risk-ratio-doc) or schedule a demo to learn more.

You can also refer to the video tutorial for exporting user profile data for risk ratio analysis using CleverTap.

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/SguGFSXOboAMJsMlg9PbFQ/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

# Create Behavioral Attributes

You can set up CleverTap Journeys to model the data exactly as expected in the Risk-ratio template.  A Past Behavior journey with a  *User Profile Update* controller node helps generate each of the attributes as listed in the following table:

| Journey   | CleverTap User Event | Risk-ratio Attribute | Description                                                                                         |
| :-------- | :------------------- | :------------------- | :-------------------------------------------------------------------------------------------------- |
| Journey 1 | Added to cart        | Y Behavior           | This attribute counts the number of *Added to cart* actions for a user.                             |
| Journey 2 | Charged              | Z Goal               | A successful conversion is represented as **1**, while a failed conversion is represented as **0**. |

> 📘 Note
>
> You can update any existing user property or create one using [CSV Upload](doc:csv-upload).

# Create Journey for Y Behavior

You can analyze the *Added to cart* event in CleverTap as Y behavior action in the Risk-ratio template. Create a journey to capture all the segments for the *Added to cart* event, where the count is zero, one, two, three, four, five, six, seven, and eight or more. The user property  *y\_behavior\_count* will track the count for each Added to Cart event instance. An   *Update user profile* controller node is used to increment the value from zero to eight for each *Added to cart* event. 

To create a journey for Y Behavior:

1. Navigate to Journeys from the CleverTap dashboard.
2. Set up the Journey using a *Past Behavior* user segment.
3. Add a Past Behavior node as the Entry Segment to qualify all users who have performed the *Added to cart* event.
4. Add a Past Behavior segment where users have added to the cart and the count is 0. 

   <Image alt="Add a Past Behavior Segment - Y attribute" align="center" width="75% " border={true} src="https://files.readme.io/61e446e46c1e7f46277b9e587d8822316e92ea4118657bf725bfc9e5026fb1da-Add_a_Past_Behavior_Segment_-_Y_attribute.png">
     Add a Past Behavior Segment - Y attribute
   </Image>

   1. Connect an Update user profile node. Set the   y\_behavior\_count  to 0.  

      <Image alt="Set count in Profile Update node - Y Behavior" align="center" border={true} src="https://files.readme.io/d10796d0605d8eb2519848300e4a6bfa3327c4a94c699913451481574df053fe-Set_count_in_Profile_Update_node_-_Y_Behavior.png">
        Set count in Profile Update node - Y Behavior
      </Image>
5. Add more segment nodes to the journey, incrementing the count for the *Added to cart* event by 1 each time.

   1. Connect an *Update user profile* node to each segment node. Increment the   y\_behavior\_count  by 1 subsequently.  The following image shows a sample Y Behavior journey:

   <Image alt="Sample Y Behavior Journey" align="center" border={true} src="https://files.readme.io/3831f5eff58df616ff11c9e7f7d8642aa0d34b4f4d6f9b4735a25f74627b1a29-image.png">
     Sample Y Behavior Journey
   </Image>

> 📘 Connect Segment and Profile Update Nodes
>
> Connect all Segment nodes via the *No* path and all the Profile update nodes via the *Yes* path.

# Create Journey for Z Goal

You can now create a similar journey for a Z goal in CleverTap. A *Charged* event indicates that the user has purchased the item. The value for the Z goal is boolean. If the user purchases the item, *Charged* is marked as *1*; if the user does not purchase, *Charged* is marked as *0*. 

The entry criteria for this Journey will be a Past Behavior segment. It includes users who have purchased an item at least once. 

<Image alt="Add a Past Behavior Segment - Z attribute" align="center" width="75% " border={true} src="https://files.readme.io/e9642ab67519799f77de364c8f273b6b2ec14eca60a73db5b8d0f00ff27df64b-Add_a_Past_Behavior_Segment_-_Z_attribute.png">
  Add a Past Behavior Segment - Z attribute
</Image>

This journey will have two updated user profile nodes: *Z Goal=1* and *Z Goal = 2*. The *Z Goal = 1* node records the count for all the instances where the user performed the *Charged* event. 

<Image alt="Set count in Profile Update node - Z Behavior" align="center" border={true} src="https://files.readme.io/52ba45a6e4bcf70ccf2b0476907ffeb85a90494e72970ab9974b64f22b39dc7f-Set_count_in_Profile_Update_node_-_Z_Behavior.png">
  Set count in Profile Update node - Z Goal
</Image>

The *Z Goal = 2* node records the count for all instances where the user did not perform the *Charged* event. The following image shows a sample Z Goal journey:

<Image alt="Sample Z Behavior Journey" align="center" border={true} src="https://files.readme.io/cf26b49053d57c5e15fbd2a29b6ddc3bf41e681b22d212a650d654f2de0c1673-Sample_Z_Behavior_Journey.png">
  Sample Z Goal Journey
</Image>

# Export Data

Export the *Y behavior* and *Z goal* count from the CleverTap dashboard. After the download, you can copy and paste the information from the downloaded CSV file to the Risk-ratio template.  

1. Go to *Segments* > *Find People*.
2. Under *Display common properties such as* section, search for *z\_goal\_count* and *y\_behavior\_count* properties. 
3. In the *Reachability* section, click the ![](https://files.readme.io/ce23ad296e6e1b62e130e20b29590b003a4609141f35e71fa7c0ae79a5236e00-Download_icon.png) icon. A window with the user attributes appears.

<Image alt="Export Attribute Data" align="center" border={true} src="https://files.readme.io/31b1fde5d766af9ea296ff65e292a93199e0b091fd7d5542245d577809f182da-Export_Attribute_Data.png">
  Export Attribute Data
</Image>

3. Select all the attributes.
4. Click **Proceed**. After the download is completed, you will receive an email with a download link for the selected properties. You can also go to *Settings* > *Downloads* and access this downloaded file on the CleverTap dashboard. 

# Analyze Risk Ratio

Once you have the CSV file, you can copy-paste the required data into the risk ratio template. To analyze the risk ratio, copy the  *CleverTap Id*, *Y Behavior*, and *Z Goal* columns to the respective[ Risk Ratio Template](https://docs.google.com/spreadsheets/d/1Hx5IB1Y0EFv30QZAO3fpEqA3E9SuMnqMESMTvU1wYLw/edit?usp=sharing) columns. 

The template will automatically populate with calculations for performing risk ratio analysis.

For further assistance, contact [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).
