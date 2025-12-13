---
title: 'Use Case 2: Recover Abandoned Cart Using Journeys'
excerpt: Learn how to recover abandoned carts using CleverTap Journeys.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Scenario

A potential user visits an online shoe app and adds a pair of sneakers to the cart. However, the consumer leaves the app without completing the transaction.

# Objective

Using CleverTap Journeys, send notifications to: 

- Encourage consumers to complete the transaction by re-engaging with them.
- Recover potential lost revenue.
- Provide a seamless and personalized shopping experience to the consumer.

# Create an Inaction Journey

Create an inaction journey that triggers when the user adds items to the cart but does not complete the purchase within two minutes. Using an inaction journey allows you to filter users for your Journey based on the actions they did not perform within a specified time. Use a combination of the user's preferred channels to send reminders at specific intervals. For example, Push, SMS, and Email messages. Customize these messages for a personalized touch. The goal is to encourage users to complete the transaction.

In this example, you create the following Journey flow:  
**_Inaction Segment > Yes > Push Notification > 2 Hours Delay > SMS > 2 Hours Delay > Email_**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3ee3f1-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


Let's understand how to create this sample Journey using the CleverTap dashboard.

On the **CleverTap Dashboard**, go to **Journeys** and click **+Journey**. On the canvas, perform the following steps: 

- [Set up the journey](https://docs.clevertap.com/docs/use-case-2-recover-abandoned-cart-using-journeys#set-up-the-journey)
- [Define goals](https://docs.clevertap.com/docs/use-case-2-recover-abandoned-cart-using-journeys#define-goals) 
- [Define entry segment](https://docs.clevertap.com/docs/use-case-2-recover-abandoned-cart-using-journeys#define-the-entry-segment)
- [Define the journey path](https://docs.clevertap.com/docs/use-case-2-recover-abandoned-cart-using-journeys#define-the-journey-path)
- [Personalize the journey ](https://docs.clevertap.com/docs/use-case-2-recover-abandoned-cart-using-journeys#personalize-the-messages)

Once you complete all the steps, publish your journey. 

## Set Up the Journey

As this is an Inaction Journey, the user's entry into the journey is determined based on the event trigger.

1. To set up your Journey, click the **Setup** widget and provide the following details as shown in the following image:

   - **Journey name**
   - **Journey entry criteria**
   - **Journey entry timelines**
   - **DND & Timezone**
   - **Journey control group**
   - **Journey timeout duration**

   [block:image]{"images":[{"image":["https://files.readme.io/8f50305-image.png",null,""],"align":"left","sizing":"80% ","border":true}]}[/block]

2. Click **Save & Close**. 

For more information, refer to the [Setting Up a Journey](https://docs.clevertap.com/docs/setup-journey) document. 

## Define Goals

To define goals for the Journey: 

1. Expand **GOALS**, drag and drop the **Action** segment in the **Goals** widget. 
2. Click the **Goals** widget and set the following details: 

   1. Enter the name of the goal in the **Goal name** field. For example, _Completed the Purchase_. 
   2. Under **Who** > **Target Segment**, set the **Charged** event as the exit criteria. Click **Continue**.

      [block:image]{"images":[{"image":["https://files.readme.io/8e561e9-image.png",null,""],"align":"left","sizing":"80% ","border":true}]}[/block]
3. Click **Save & Close**.

For more information, refer to the [Define Goals](https://docs.clevertap.com/docs/define-goals) document. 

## Define the Entry Segment

The Entry Segment identifies users who will qualify to enter the journey. For example, users who added items to the cart but didn't complete the transaction within 2 minutes qualify to enter the Journey.

1. Drag and drop the **Inaction** segment node to the **Entry Segment **block as the entry criteria. 
2. Click the **Action** segment node and enter the following details: 

   1. Enter the name of the segment in the **Segment name** field. For example, _Added to Cart but Did Not Do Charge_.
   2. Under **Who** > **Target Segment**, set the following events and click **Continue**:  

      1. **As soon as user does** = _Added to Cart_ event
      2. **And does not do** = _Charged_ event _within 2 minutes_

         [block:image]{"images":[{"image":["https://files.readme.io/a0bdb4d-image.png",null,""],"align":"left","sizing":"80% ","border":true}]}[/block]
3. Click **Save & Close**.

For more information, refer to the [Define Entry Segment](https://docs.clevertap.com/docs/define-entry-segment) document.

## Define the Journey Path

Drag and drop engagement nodes from the left pane, connect them using the journey links (e.g., **Yes** or **Sent** path), and set the delay hour using the **Sleep Time** icon. Create the journey path in the following sequence: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4319962-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


1. **Push Notification with Free Shipping**:

- Sent immediately if the user qualifies for the journey through the inaction segment.
- Offers free shipping to the consumer.

2. **SMS with Discount**:

- After 2 hours, if the user hasn't completed the purchase.
- Provides a limited-time offer of a 10% discount.

3. **Final Email Reminder**:

- Another 2-hour wait.
- Sends a final reminder through email.

## Personalize the Messages

Once you have outlined the journey path, compose the Push, SMS, and Email messages. 

For more information about composing your message, refer to the [Push](https://docs.clevertap.com/docs/push), [SMS](https://docs.clevertap.com/docs/sms), and [Email](https://docs.clevertap.com/docs/email) documents. 

In this example, let's understand how to personalize a Push message. 

1. Click the **Push** engagement node. 
2. Under **What**, select ** Message Type** and open the editor. 
3. Enter the message in the **Title** and **Message** field. You can use the **Scribe** ![](https://files.readme.io/bf3a4d6-2023-03-17_11-28-28.jpg) icon to generate personalized copies.
4. Further, you can use the inline **@** personalization option or the more advanced options from the **Personalization** icon at the top of the page.

In the following graphic, use **@Profile - Name** to includes the customer's name in the message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b5be7ddb8487f43c90f4efd078e85e48f875f50b39f68672388965959306cc3d-Personalize_in_Journeys.png",
        null,
        "Personalize in Journeys"
      ],
      "align": "center",
      "border": true,
      "caption": "Personalize in Journeys"
    }
  ]
}
[/block]


For more information on personalization, refer to the  [Personalization in Journeys](doc:personalization-in-journeys) document. 

5. Click **Done**. Similarly, you can compose SMS and Email messages.
6. Click **Publish** to make the journey live.

Once you have published the Journey, you can monitor the Journey using Journey stats. For more information on Journey statistics, refer to the [Journey Performance](https://docs.clevertap.com/docs/viewing-statistics) document.

# Conclusion

Thus, CleverTap Journeys offers an effective solution for addressing cart abandonment. It allows you to re-engage users and guide them toward completing their purchases. As a result, it increases conversions and revenue generation.