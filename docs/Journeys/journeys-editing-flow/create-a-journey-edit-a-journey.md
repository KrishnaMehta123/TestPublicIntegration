---
title: Create a Journey
excerpt: ''
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

On the CleverTap dashboard, click **Journeys** under the _MESSAGES_ section on the left pane. Journey creation includes the following high-level steps: 

[block:parameters]
{
  "data": {
    "h-0": "Steps",
    "h-1": "Description",
    "0-0": "[**Setting Up a Journey**](doc:setup-journey)",
    "0-1": "Specify the following details and criteria to set up a Journey:  \n  \n- Journey name\n- Type of user behavior to qualify user entry into a Journey\n- Date and time when the users can qualify for the Journey\n- Do not disturb and timezone preference\n- Control group\n- Journey timeout ",
    "1-0": "[**Define Goals**](doc:define-goals)",
    "1-1": "Define the goal of the Journey. A goal is the desired action you want a subset of users to achieve on your app as they progress through a Journey. For example, perform a purchase, subscribe,  launch, or register on the app, and so on.",
    "2-0": "[**Define Entry Segment**](doc:define-entry-segment)",
    "2-1": "Define your target users for the Journey based on their past behavior or live action. For example, target users who have just installed an app to increase user registrations.",
    "3-0": "[**Define Journey Path **](doc:construct-a-journey)",
    "3-1": "Define various Journey paths based on the specified goal and entry criteria. It orchestrates the path users can follow based on their actions on each engagement node.",
    "4-0": "[**Personalize the Journey Content**](doc:personalization-in-journeys)",
    "4-1": "Use CleverTap's personalization capabilities, such as [Recommendations](https://staging.docs.user.clevertap.net/docs/recommendations), [Linked Content](https://staging.docs.user.clevertap.net/docs/linked-content), and [Liquid Tags](https://staging.docs.user.clevertap.net/docs/liquid-tags), to customize the Journey for specific users. You can send dynamic and real-time recommendations to users based on user behavior.",
    "5-0": "[**Publish a Journey**](doc:publish-a-journey-edit-a-journey)",
    "5-1": "Save and publish the Journey. ",
    "6-0": "[**Monitor the Journey**](doc:journey-performance-edit-a-journey)",
    "6-1": "Monitor its performance using Journey stats."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


Once you have created and published a journey, you can edit it to make changes to the current journey or create a new version without affecting the current live version. This allows you to iterate and improve your engagement flow over time. For more information, refer to [Edit a Journey](doc:edit-a-journey). 

# Prerequisites for Creating a Journey

First, you must understand the use case you are trying to solve using a Journey. Based on this, you will plan your Journey creation. 

Consider a scenario where a segment of users regularly visits your app and frequently views specific products. However, they are indecisive about buying the product. They are most likely still evaluating the product or looking for more exciting offers. To solve this sample use case, you must have the following prerequisites: 

- **Determine your use case**: Create a Journey that delivers real-time offers to entice on-the-fence shoppers to buy the product.
- **Define the goal**: On-the-fence shoppers make a purchase.
- **Identify your target segment**: Analyze and track all users viewing a product frequently. For example, fetch users whose event property is _Product Viewed_ and the view count is more than five times. 
- **Identify the offer/promotion**: Determine the specific discount, benefit, or promotion you want to give shoppers. For example, it could be a percentage discount, a gift, an extended trial period, or exclusive access to certain features.
- **Identify the engagement channels**: Determine the various engagement channels through which users will engage with the app. For example, Push, In-App, Email, and so on. 
- **Identify the duration of your Journey**: Decide on the duration of the offer. Ensure the time frame is reasonable enough to entice the user to buy the product.
- **Visualize the Journey path**: Visualize the logical flow of users' journey paths depending on their actions. For example, the users move along different paths based on their actions: 
  - **Path A**: Users who viewed the product more than five times.
  - **Path B**: Users who viewed the product more than ten times. 

Now that you have outlined your Journey requirement, you can start creating the Journey. 

Before building a Journey on the CleverTap Dashboard, ensure you understand the [Journey Components](doc:journey-components).