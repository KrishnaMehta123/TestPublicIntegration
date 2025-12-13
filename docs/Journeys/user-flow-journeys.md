---
title: User Flow in Journeys
excerpt: Understand how to nudge users to perform the desired action.
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

Your users perform one action in a Journey and then move on to the next action. However, there may be instances when they do not move forward in the Journey if not handled correctly.  
We will walk through various combinations to ensure all users' participation in journeys.

## Users Waiting at Segment Node

In scenarios where the next node in a Journey is a Segment Node, the Users will wait till they qualify for the node or exit via Journey Timeouts or Goals.  
For instance, you have shown the Users a Welcome message In-app and are now waiting for them to qualify for the next Segment Node, _Redeem Offer_. In this case, you’d want to set a time limit based on which the users should move down a different path if they don’t qualify for the Segment. This will allow you to nudge the Users to Redeem their offer in this example, and then they can join the main journey again.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/662237f-Journeys_Segment_Waiting_Users_Blink.png",
        "Users waiting at Segment node to qualify for the Journey",
        456
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Users Waiting at Segment Node"
    }
  ]
}
[/block]


### Set the Qualifying Window

Click the **hexagon**![hexagon](https://files.readme.io/a7efd36-Hexagon.png) on the _Segment_ node to set the qualifying window for the users. 

> 🚧 
> 
> The qualifying window must be set up in combination with the drawing of the Node Timeout connector. The users will not move if the _Node Timeout_ is not connected to another node.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aeabc0d-Qualifying_Window.gif",
        "Set the qualifying window for the Journey",
        1440
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Set Qualifying Window"
    }
  ]
}
[/block]


### Connect to Another Node

Connect the _Node Timeout_ connector to another node. After the qualifying window is complete, the user automatically moves to the next node through this timeout connector.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/27822b5-Node_Timeout.gif",
        "Connect the node timeout connector to another node",
        838
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Node Timeout Connector"
    }
  ]
}
[/block]


> 📘 Note
> 
> The yellow indicator on your segment node is a reminder that you may need to plan for _Waiting_ _users_ on this node in the Journey.

## Users Waiting at Engage Node

There may be another instance where the users have received a message but they may still wait for action. If the users do not click the message, then they are waiting for the next action.  It means that when you created the Journey, the node following the Engage node is connected with a _Viewed_ or _Clicked_ connector. When you draw a _Viewed_ or _Clicked_ connector, a _Phantom_ node with a node timeout will appear automatically. You can set the qualifying window from this _Phantom_ node to move the users further.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f676ab4-User_Waiting_at_Engage_Node.gif",
        "Phantom node with a node timeout",
        1438
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Users Waiting at Engage Node"
    }
  ]
}
[/block]