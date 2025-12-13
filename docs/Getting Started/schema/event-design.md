---
title: Event Design
excerpt: Understand event design, guidelines and its best practices.
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

A good event design can unlock actionable insights and maximize the value of your analytics data. CleverTap offers a comprehensive event design framework to help businesses track and analyze user interactions effectively. This document describes the guidelines and the best practices of event design within CleverTap. By following the guidelines and best practices outlined in this guide, businesses can optimize their event-tracking strategy and drive meaningful user engagement and retention.

# Guidelines for Event Design

The following is a comprehensive set of guidelines to help you navigate the complexities of event tracking:

## How Many Events to Track?

Determining the number of events to track depends on the complexity of your app or website's functionality. While some apps or websites may require only a few key events, others with richer functionalities may need a more extensive event-tracking approach. It is essential to strike a balance and avoid tracking every minor user action, focusing instead on actions crucial for completing processes within your app or website.

* **Basic Apps**: Apps with fundamental features typically require only a few key events. For example, these apps require approximately 20 key events to track essential user interactions, such as Sign-ups, Purchases, and App Launches.
* **Feature-rich Apps**: Applications offering a wide range of features and functionalities may require tracking approximately 200 events to capture diverse user actions comprehensively. For example, in addition to tracking Sign-ups and Purchases, these apps may need to monitor advanced interactions such as feature usage, content consumption, and social sharing.

> 📘 Note
>
> Please note that these number serves as a rough guideline and may vary depending on individual app requirements.

## Which Events to Track?

Identifying the events to track depends on the critical actions users perform within your app. A helpful rule of thumb is to check if all steps of a process can be represented in a funnel structure. You can optimize your event-tracking strategy by focusing on actions that drive engagement and contribute to your app's success. You can consider the following examples of essential events to track:

* **Sign-up Process Completion**: Tracking when users complete the sign-up process provides valuable insights into user acquisition and conversion rates.
* **In-App Purchases**: Monitoring purchases within your app allows you to analyze user spending behavior and optimize revenue generation strategies.
* **Onboarding Progress**: Tracking users' progress through the onboarding process helps identify potential bottlenecks and areas for improvement.

# Best Practices for Event Design

From naming conventions to user action properties, explore key strategies to enhance your event-tracking strategy and drive actionable insights. Unlock the full potential of your app analytics with the best practices for effective event design listed below.

## Nomenclature for Events

Clear and descriptive event names ensure consistency and clarity in your event-tracking strategy. Name events by adopting a Noun-Verb pair format (for example, App Launched, Product Viewed) to ensure consistency. This approach enhances data comprehension and facilitates collaboration within your team.

Let's illustrate this concept with a few more examples:

| Poor Event Name         | Improved Event Name   |
| :---------------------- | :-------------------- |
| Initiated\_Buy\_Screen1 | Product Added to Cart |
| Clicked\_Button123      | Button Clicked        |
| Opened\_Screen\_ABC     | Screen ABC Opened     |
| Selected\_Item\_XYZ     | Item XYZ Selected     |
| Completed\_Form\_1      | Form 1 Completed      |

## Finding Essential Events to Track

Identifying key user actions involves understanding the most frequent and important actions users perform within your app. You can identify key user actions by answering two fundamental questions:

* What are the most frequent actions users perform in my app?
* What are the most important actions I want users to perform in my app?

These questions guide the selection of meaningful and actionable user-centric metrics, steering away from traditional event-centric tracking methods. For example:

* **Frequent User Actions**: *Search*, *Visit Sale Pages*, *Add to Cart*
* **Important User Actions**: *Register*, *View Products*, *Purchase*

## Tracking User Action Properties

Enhance the granularity of event tracking by incorporating user action properties. Start with tracking fundamental actions and gradually introduce complexity by including action properties to enrich your data analysis.

For example, with the *Added to Cart* event, you can track properties such as *Product Name*, *Product Category*, and *Cart Amount*. By including properties like *Product Name* and *Category*, you can gain deeper insights into user behavior and preferences, enabling more targeted marketing campaigns and personalized user experiences.

## Managing Consistency Across Platforms

Maintain consistency in tracked user actions across web and mobile platforms to ensure accurate data analysis and reporting. For example, tracking *Product Viewed* consistently across web and mobile platforms enables seamless multi-platform marketing reporting and unbiased platform-wise analysis.

# Resources and Support

For additional resources and support on event design within CleverTap, explore the following:

* Explore further insights and tips on event design in our blog post: [A Marketer's Guide to Event Design](https://clevertap.com/blog/a-marketers-guide-to-event-design/).
* For assistance or inquiries regarding event design and implementation, contact our support team at [support@clevertap.com](mailto:support@clevertap.com).
