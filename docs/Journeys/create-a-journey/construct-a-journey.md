---
title: Define Journey Path
excerpt: >-
  Understand how to use the journey canvas and link various journey nodes to
  construct a journey.
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

You can connect the Segment, Engagement, and Controller blocks from the Journey canvas to define how your users must move through the Journey. 

# Create a Journey

The first step is to define your target users. Drag the *Segment* block from the palette to the canvas. 

<Image title="Drag and drop a Segment node to create a Journey" alt={1218} align="center" border={true} src="https://files.readme.io/c27e919-Segment_Node_for_Journey.gif">
  Segment Node for Journey
</Image>

Click the Segment node to define the qualifying criteria for your users. Define your qualifying criteria and click **Continue**.\
View the details and **Save & Close**.

<Image title="Select target segment for Journeys" alt={775} align="center" width="80%" border={true} src="https://files.readme.io/46d331f-Journeys_define_entry_node.png">
  Select Target Segment
</Image>

 Next, decide the type of engagement to send to the qualified users. 

<Image title="Select the engagement type" alt={1216} align="center" border={true} src="https://files.readme.io/957551d1fdc481fe40112a88c5f9911d0e94084c18f30c442fe15578b2c7f0f9-2025-04-14_11-59-41_1.gif">
  Select Engagement Type
</Image>

<Image title="Select the message type" alt={784} align="center" width="80%" border={true} src="https://files.readme.io/5e9f457-Journeys_define_engagment_node.png">
  Select the Message Type
</Image>

Add more nodes to plan for scenarios where the user does or does not respond. For example, you want to send an additional nudge if the user does not buy a product or a thank you note if the user does purchase the product. You can decide the level of details for your Journey. 

> 🚧 Note
>
> You can apply campaign limits in a Journey. However, global throttling is not supported in Journeys.

# Connections

Drag and drop blocks from the palette to the canvas to create connections. 

## Connect Segment & Engage Blocks

Once you have defined a segment of users, you can choose to communicate with the segment by dragging and dropping a channel of communication from the palette on the right-hand side. This communication could go to users who match the segment criteria specified by you, or to the rest of the users i.e. the users who don’t match your segment criteria.

> 📘 Tip on Duplicating Segments
>
> To duplicate a specific segment, use the copy/paste function by hovering over a segment, then perform the following:
>
> * MacOS: Alt + mouse click 
> * Windows: Ctrl + mouse click

<Image title="Connect segment and engage blocks" alt={1051} align="center" border={true} src="https://files.readme.io/7a32f70-Journeys_Connect_Segment_Engage_Blocks.png">
  Connect Segment and Engage Blocks
</Image>

## Connect Engage & Segment Blocks

After a user receives a message, you can add a segment after that to ensure that only users who meet the criteria specified by you are taken further in the Journey. 

Example: After users receive a push notification, wait for 1 day, check if users have transacted, for the people that have transacted, send them down path A, and for those who haven’t send them down path B.

<Image title="Connect engage and segment blocks" alt={973} align="center" border={true} src="https://files.readme.io/37b12e3-Journey_Connect_Engage_Segment_Blocks.png">
  Connect Engage and Segment Blocks
</Image>

## Connect Engage & Engage Blocks

After a user receives a message, you can follow it up immediately, or with a delay with another message on a channel of communication of your choosing. 

Example: After a user receives a push notification, you can wait for 3 days, and send another push notification.

<Image title="Connect engage with engage blocks" alt={905} align="center" border={true} src="https://files.readme.io/ee6bb98-Journeys_Connect_Engage_Engage_Blocks.png">
  Connect Engage with Engage Blocks
</Image>

## Connect Segment & Segment Blocks

After a user has been segmented, you can follow it up with another segment to further refine your Journey. 

Example: If someone has not transacted in the last 30 days, send users who qualify for this segment down path A, and if one of these users adds an item to their cart, and doesn’t buy within 15 mins, send them down a specific path.

<Image title="Connect segment and segment blocks" alt={999} align="center" border={true} src="https://files.readme.io/430bb85-Journeys_Connect_Segment_Segment_Blocks.png">
  Connect Segment and Segment Blocks
</Image>

# User Flow in Journeys

Your users perform one action in a Journey and then move on to the next action. However, there may be instances when they do not move forward in the Journey if not handled correctly.\
We will walk through various combinations to ensure all users' participation in journeys.

## Users Waiting at Segment Node

In scenarios where the next node in a Journey is a Segment Node, the Users will wait till they qualify for the node or exit via Journey Timeouts or Goals.\
For instance, you have shown the Users a Welcome message In-app and are now waiting for them to qualify for the next Segment Node, *Redeem Offer*. In this case, you’d want to set a time limit based on which the users should move down a different path if they don’t qualify for the Segment. This will allow you to nudge the Users to Redeem their offer in this example, and then they can join the main journey again.

<Image title="Users waiting at Segment node to qualify for the Journey" alt={456} align="center" width="90% " border={true} src="https://files.readme.io/662237f-Journeys_Segment_Waiting_Users_Blink.png">
  Users Waiting at Segment Node
</Image>

### Set the Qualifying Window

Click the **hexagon**![hexagon](https://files.readme.io/a7efd36-Hexagon.png) on the *Segment* node to set the qualifying window for the users. 

> 🚧
>
> The qualifying window must be set up in combination with the drawing of the Node Timeout connector. The users will not move if the *Node Timeout* is not connected to another node.

<Image title="Set the qualifying window for the Journey" alt={1440} align="center" width="90% " border={true} src="https://files.readme.io/024e4106e7a4ea2388bfa272c03ba0a3270ab4418c7b26ad62bf02d3405e2508-2025-04-14_12-31-53_1.gif">
  Set Qualifying Window
</Image>

### Connect to Another Node

Connect the *Node Timeout* connector to another node. After the qualifying window is complete, the user automatically moves to the next node through this timeout connector.

<Image title="Connect the node timeout connector to another node" alt={838} align="center" width="90% " border={true} src="https://files.readme.io/4490344015aba7ca7e5fc16c09ffce98106d8ce1de9b4f729013b005b4dc3ebc-2025-04-14_13-12-13_1.gif">
  Node Timeout Connector
</Image>

> 📘 Note
>
> The yellow indicator on your segment node is a reminder that you may need to plan for *Waiting* *users* on this node in the Journey.

## Users Waiting at Engage Node

There may be another instance where the users have received a message but they may still wait for action. If the users do not click the message, then they are waiting for the next action.  It means that when you created the Journey, the node following the Engage node is connected with a *Viewed* or *Clicked* connector. When you draw a *Viewed* or *Clicked* connector, a *Phantom* node with a node timeout will appear automatically. You can set the qualifying window from this *Phantom* node to move the users further.

<Image title="Phantom node with a node timeout" alt={1438} align="center" width="90% " border={true} src="https://files.readme.io/90fce4581e8604206c8268c6d0d986c741feeaf908e4f5daa78f11739ebc3b8c-2025-04-14_13-17-01_1.gif">
  Users Waiting at Engage Node
</Image>

# Using User Profile Update Node

The **User profile update** node is a controller node that allows you to update user properties in a Journey. It updates the user profile details based on the events triggered in the preceding segment or engagement node. Consider an action segment node followed by a user profile update node. For example, when a user subscribes to an OTT channel, the *Channel Subscribed* event is triggered. The user profile update node tracks this event and updates the latest property values, such as subscription plan name, price, validity, billing interval, etc. 

<Image alt="User Profile Update Node" align="center" width="70% " border={true} src="https://files.readme.io/9e4d725-image.png">
  User Profile Update Node
</Image>

You can add conditional logic to your live behaviour Journeys using Liquid Tags, which can reference events from the previous segment. This enables you to retrieve event properties and use them to update user profile details.

## User Profile Update Node Video Tutorial

Discover the video tutorial for the User Profile Update node in Journeys.

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
              src="https://clevertap.portal.trainn.co/share/pDjLPfTJ8C5UCccIH80BQQ/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

<br />

To define the user profile update node: 

1. Drag and drop the **User profile update** node and connect it to the desired segment node. 

2. Click the **User profile update** node. The **Controller - User profile update** window appears.

3. Enter the controller name.

4. Under **Setup**, click **+ User Property** and define the user property values. The following UI elements appear. For more information, refer to the [Define User Property](https://docs.clevertap.com/docs/construct-a-journey#define-user-property-values) section.

<Image align="center" className="border" width="70% " border={true} src="https://files.readme.io/a305ceb-image.png" />

5. Click **Continue** and **Save & Close**.

## Define User Property Values

This section describes how to define user property values. 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        UI Elements
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **User Property**
      </td>

      <td>
        From the drop-down list, you may choose the following two categories of user properties to update:  

        <li>**System Properties**: System user properties are predefined attributes often essential for user identification, segmentation, and tracking. You can set boolean values or custom values. For example, _MSG-whatsapp_ set to _True_ indicates that the user has subscribed to WhatsApp notifications. </li><li>**Custom Properties**: Custom user properties allow you to capture additional data about a user that is not captured by system properties. For example, subscription plan, language preference, location, interests, and so on.</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        **Operator**
      </td>

      <td>
        From the drop-down list, you may choose one of the following operators to set values to the user properties:  

        <li>**Set to**: Sets a new value to the current user property value. By default, combines comma-separated values into a single value.</li><li>**Increase by**: Adds a specified value to an existing value.</li><li>**Decrease by**: Subtracts a specified value from an existing value.</li><li>**Add to array**: Appends the new value to the existing array.</li><li>**Remove from array**: Removes the values from the array.</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        **Text Box**
      </td>

      <td>
        Depending on the type of user property and operator you choose, you can enter the values in the following formats:  

        <li>Set a boolean value. For example, _True_ or _False_. It is not case-sensitive.</li><li>Set an array of comma-separated values. For example, the Location is set to London, Amsterdam, New York.</li><li>Set liquid tag conditions. The maximum character limit for the Liquid Tag condition is 512. For more information, refer to [Updating User Profile Details using Liquid Tags](https://docs.clevertap.com/docs/construct-a-journey#updating-user-properties-using-liquid-tags).</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        **Apply as a single value**
      </td>

      <td>
        This is enabled for **Add to array** and **Remove from array** operators:  

        <li>When you check the box, it combines the comma-separated values into one single value. For example, "London, UK" is considered a single value.</li><li>When you uncheck the box, it separates the values using commas. For example, "London", "UK" are considered separate values.</li>  
          
        <br />
      </td>
    </tr>
  </tbody>
</Table>

## Updating User Properties using Liquid Tags

This section explains how to update user properties using the user profile update node and liquid tags.

### Use Case 1: Update User's Preferred Movie According to User Ratings

This use case lets you update a user's preferred or favorite movie based on the ratings the user provided for a movie. You can reference the *Movie Rated* event property in the conditional logic to update the *Favorite Movie* user property. The following is a sample conditional logic: 

<Image align="center" className="border" border={true} src="https://files.readme.io/8152361-image.png" />

### Use Case 2: Total Customer Revenue Based on Yearly Flights Booked per User

In this use case, you can keep track of a customer's total revenue for the year by adding up all their flight booking amount. For example, if a user booked flights worth $1000 by September 14th and then booked another flight for $500 on September 15th, an event is triggered with this new booking information. You can reference the *Booking Amount* event property in the liquid logic and add it to the *Total Revenue* user property, resulting in a total revenue of $1500 for the year.

<Image align="center" className="border" border={true} src="https://files.readme.io/f5b5f3d-image.png" />

### Use Case 3: Score a Customer Using Triggered Segment Journey

This use case lets you identify certain user behaviors, assign the users a score based on their activity, and segment them later for targeted marketing campaigns. For instance, when users update their profile, such as adding a picture or status on social media, their engagement score goes up by 1. The following is a sample logical condition: 

<Image align="center" className="border" border={true} src="https://files.readme.io/e1d4705-image.png" />

### Use Case 4: Calculate the Total Purchase Value for a User when a Charged Event is Recorded

This use case tracks a user's total purchase value by adding up the amounts of their purchases recorded through a *Charged* event and updates it when a product is returned. For instance, if a customer buys groceries costing $50, $100, $30, and $75, the total value of their groceries purchased is $255. The following is a sample logical condition: 

<Image align="center" className="border" border={true} src="https://files.readme.io/bddb6a5-image.png" />

> 📘 Points to Remember
>
> * Only event properties can be used in liquid tags for user profile update node. 
> * You can update a specific user property only once. 
> * Irrespective of whether the update fails or succeeds, user moves ahead via the **Updated** path.
> * If the user property for the user does not exist in the profile, then the property is created for that user profile.
