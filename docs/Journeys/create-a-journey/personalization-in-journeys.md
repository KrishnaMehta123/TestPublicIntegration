---
title: Personalization in Journeys
excerpt: Understand how to personalize your messages in journeys.
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

While creating a complex orchestration for your users, ending personalized messages is equally important to increase the actionability of those messages. The following steps guide you on achieving this within different engagement nodes available on Journeys:

- [Personalize Messages in Journeys](https://docs.clevertap.com/docs/personalization-in-journeys#personalize-messages-in-journeys)
- [Personalize Events across Nodes](https://docs.clevertap.com/docs/personalization-in-journeys#personalize-events-across-nodes)

# Personalize Messages in Journeys

You can personalize messages journeys after you finish [constructing a journey](https://docs.clevertap.com/docs/construct-a-journey). To personalize the messages in Journeys from the engagement nodes:

1. Click an engagement node and create a campaign. 
2. Select _What_  and then select the _Message Type_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02868b8-Journeys_campaign_personalization.png",
        "Select the message type for to create Journeys",
        780
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Select the Message Type"
    }
  ]
}
[/block]

3. Click _Go To Editor_ to edit and personalize the message. You can either use the inline @ personalization option or the more advanced options from _Personalization_ icon at the top of the page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/055e687-CNP_Personalization.png",
        "Create a personalized message",
        1988
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Create a Personalized Message"
    }
  ]
}
[/block]

For more information about message personalization, see [Message Personalization across campaigns](doc:personalize-message-all)

# Personalize Events across Nodes

You can personalize an _Event Triggered Journey_ to engage a user through the subsequent engagement nodes or messaging channels. 

For example, a user adds an item to the cart but does not purchase it. You can then create a journey to send personalized reminders for the abandoned cart item through different channels. To achieve this personalization, you can personalize multiple messages in the journey based on the event _Abandoned Cart_ in the following order:

1. _Push Message Reminder_: After an hour of abandoning the cart, send a reminder message that says, "Hey, the iPhone 14 in your cart is still waiting."
2. _Push Message Followup_: Send a follow-up message that says, "Still interested in iPhone 14? It’s still waiting in your cart; tap Buy to finish your purchase."
3. _Email Message_: An email that includes the Product Name, Image, Price, and Link to the product purchase.

The previous action node decides the event in the subsequent engagement node when multiple engagement nodes exist. The following table explains the node personalization sequence:

| Preceeding Node        | Subsequent Node | Is Event Personalization Available? |
| :--------------------- | :-------------- | :---------------------------------- |
| Action Segment Node    | Engagement Node | Yes                                 |
| Inaction Segment Node  | Engagement Node | Yes (For main event)                |
| Date Time Segment Node | Engagement Node | Yes                                 |

## Node Event Personalization Considerations

There are some factors to consider when personalizing events across engagement nodes:

- Event personalization is available for the Action, Inaction, and Date Time segment nodes.
- Currently, online channels such as Web Pop-up, In-App, and  App Inbox do not support Event Personalization across Nodes. 

## Valid Journeys for Node Personalization

The following scenarios indicate a valid user journey for node personalization:

### Personalize Engagement Nodes after Action Node

You can personalize multiple messages in the journey based on the user event, that is, the abandoned cart event, when the engagement node follows the action node.  For example, if a user adds an item to the cart but does not purchase it, you can set up a journey to send reminders for the abandoned cart item. You can send a push message followed by an email message to nudge the user. 

- Push Message Reminder: This is a reminder after an hour of abandoning the cart. A message that says, "Hey, the iPhone 14 in your cart is still waiting."
- Email Message: This is an email that includes the Product Name, Image, Price, and Link to the product purchase.

Following is a sample Journey flow:  
_Action Node  >  Engagement Node 1 >  Engagement node 2_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/737d23f-277a7fc-Action_engage1_engage2.png",
        "Sample journey flow showing engagement nodes after action node",
        2356
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Journey - Engagement Nodes after Action Node"
    }
  ]
}
[/block]

### Personalize Engagement Node with Delay

You can set up a maximum delay of less than 24 hours per node in a journey. The following journey shows a 15-hour delay for each node.  Send a push message after 15 hours and send another email message after 15 hours of delay.

Following is a sample Journey flow:  
_Action Node  > (delay of 15 hrs) > Engagement Node 1 > (delay of 15 hrs) > Engagement node 2_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e33188-614275c-Action_delay_case2.png",
        "Sample journey flow showing engagement node with delay",
        2384
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Journey - Engagement Node with Delay"
    }
  ]
}
[/block]

### Personalize Engagement Node with Delay and Controller Node

You can personalize an event across two engagement nodes even if there is a Controller Node, such as User Profile Update, or IntelliNODE, between these engagement nodes.

Consider a Journey where Engagement Node 1 before the Controller Node and Engagement Node 2 after the Controller Node (updating a user profile) can be personalized based on the event in the Entry Node.

Following is a sample Journey flow:  
_Action Node  > (delay of 15 hrs) > Engagement Node 1 > Controller node > (delay of 15 hrs) > Engagement node 2_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d3099e-6accfcc-Action_controller.png",
        "Sample journey flow showing engagement node with delay and controlled node",
        3510
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Journey Flow - Engagement Node with Delay and Controller Node"
    }
  ]
}
[/block]

### Personalize Events across Multiple Action Nodes

You can only personalize events from a preceding Action Node. Consider the following scenario: The entry segment is an Action Node _Segment 1_. All the subsequent engagement nodes get a trigger event from _Segment 1_. However, if you add another Action Node  _Segment 2 _  in the Journey, all the subsequent engagement nodes get a trigger event from  _Segment 2 _. 

Refer to the following Journey example:

_Segment 1 (Event 1) > Engagement Node 1(Event 1) > Engagement Node 2 (Event 1) > Segment 2 (Event 2) > Engagement Node 3 (Event 2) > Engagement Node 4 (Event 2)_

Now, all the engagement nodes after _Engagement Node 3_ will only get trigger events from _Segment 2_ for event personalization.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea42acf-fb01df9-two_action_nodes.png",
        "Sample journey flow showing event across multiple action nodes",
        5478
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Journey Flow - Events Across Multiple Action Nodes"
    }
  ]
}
[/block]