---
title: Comprehensive Guide to Engage With Users
excerpt: Learn how you can effectively target and engage with users.
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

This document is a comprehensive guide to effectively target and engage users. It provides an overview of the following key features in CleverTap and highlights specific scenarios where these features can be most effective:

- [Bulletins](doc:comprehensive-guide-to-engage-with-users#bulletins)
- [Create Campaign API](doc:comprehensive-guide-to-engage-with-users#create-campaign-api)
- [External Trigger ](doc:comprehensive-guide-to-engage-with-users#external-trigger-campaign)
- [Message via Identity API](doc:comprehensive-guide-to-engage-with-users#message-via-identity-api)

# Bulletins

Consider a music streaming app that wants to inform users about new album releases from their favorite artists. Instead of creating multiple campaigns, the app can use Bulletins to send personalized messages to users who are interested in specific artists. This approach allows the app to automate the process of keeping users updated, even if there are multiple new releases each week. With Bulletins, the app can deliver announcements, promotions, or surveys directly to users while they are using the app, making the process more efficient and engaging.

## Use Cases

The following are some of the ideal scenarios where Bulletins become handy to engage with your users:

- _New Season Releases_: Notify users about the release of a new season or episode based on their previously watched genres or previous show engagements.
- _Product Updates_: Inform users about new product features or updates, ensuring they know about enhancements and improvements.
- _Event Announcements_: Broadcast information about upcoming events or promotions, driving awareness and participation. 

## Implementation

The following are the four major steps to use the Bulletins feature in the CleverTap dashboard:

1. Determine the events or updates that require user notification.
2. [Set up business events in CleverTap that will trigger the automatic dispatch of Bulletins.](doc:bulletins#create-business-events)
3. [Configure Bulletin campaigns in CleverTap, specifying the message, audience, and channels](doc:bulletins#create-a-bulletin).
4. [Measure the impact of your Bulletins on user engagement and iterate based on data-driven insights](doc:bulletins#monitor-bulletin-performance).

## Key Differentiators

The following are the key differentiators of CleverTap's Bulletins feature:

- _Event-Driven Notifications_: Send messages triggered by specific business events.
- _Multi-Channel Reach_: Engage users across different channels, maximizing visibility.

# Create Campaign API

Consider an e-commerce business that wants to automate sending campaigns from its servers instead of creating them from the CleverTap dashboard. The business can use CleverTap's Create Campaign API to automate and scale the effort. This feature offers a programmatic approach to crafting and managing marketing campaigns. 

## Use Cases

The following are some of the ideal scenarios where Create Campaign API becomes handy to engage with your users:

- _Dynamic Campaign Creation_: Automate campaign generation based on user behavior or external data insights.
- _Workflow Integration_: Seamlessly incorporate CleverTap campaign functionalities into existing marketing workflows or CRM systems.
- _Scalable Marketing Efforts_: Manage and execute large-scale campaigns with ease, adapting to real-time marketing needs.

## Implementation

The following are the four major steps to use the Create Campaign API feature in the CleverTap dashboard:

1. Define the campaign parameters, including audience, content, and scheduling.
2. [Utilize the Create Campaign API to programmatically initiate campaigns within CleverTap](https://developer.clevertap.com/docs/create-campaign-api#create-campaign-api---target-user-events--properties).
3. [Monitor responses and errors from the API to ensure successful execution](https://developer.clevertap.com/docs/api-errors).
4. [Evaluate campaign effectiveness using CleverTap Analytics and refine strategies for optimal outcomes](https://developer.clevertap.com/docs/create-campaign-api#view-campaigns-created-through-apis).

## Key Differentiators

The following are the key differentiators of CleverTap's Create Campaign API feature:

- _Seamless Integration_: Integrate with existing systems for streamlined marketing processes.
- _Scalability_: Efficiently create and manage multiple campaigns, catering to diverse marketing goals.

# External Trigger Campaign

Consider a subscription platform that wants to send a confirmation mail to users when they upgrade their subscription plan. Previously, sending such critical non-promotional alerts required significant development efforts, making the process tedious. The business can use the External Triggers feature to manage and trigger notifications directly from the CleverTap dashboard. And, the content delivery is triggered from their servers and systems. The API request used to trigger the message can include supplementary data that can be dynamically inserted into the message.

External campaigns are tailored for non-promotional use cases, enabling the delivery of personalized messages based on specific user actions. This elevates the user experience through meaningful engagement.

## Use Cases

The following are some of the ideal scenarios where External Trigger Campaigns become handy to engage with your users:

- _Subscription Purchases or Upgrades_: Automatically send a confirmation email or push notification when a user upgrades their subscription plan, ensuring they are aware of the new benefits.
- _Fitness Milestones_: Celebrate user achievements by sending congratulatory messages or badges when they reach fitness goals, like walking 15,000 steps, encouraging continued app engagement.
- _Order Confirmations_: Send detailed order confirmation messages immediately after a purchase is made on your e-commerce platform, improving customer satisfaction and clarity.

## Implementation

The following are the four major steps to use the External Trigger feature in the CleverTap dashboard:

1. [Identify key user actions outside your app that warrant engagement](external-trigger#define-the-audience) (for example, subscription upgrades, fitness milestones).
2. [Set up External Trigger campaigns from the CleverTap dashboard, defining the message content with personalization keys](external-trigger#define-the-message).
3. Integrate your external systems with CleverTap to trigger external trigger API when specified actions occur.
4. Analyze and optimize the performance of your External Trigger campaigns based on user engagement and feedback.

## Key Differentiators

The following are the key differentiators of CleverTap's External Trigger feature:

- _Real-time Engagement_: Instantly respond to user actions.
- _Removes Engineering Dependency_: Managing content editing directly from the dashboard eliminates the need for engineering intervention.
- _Personalization_: Tailor messages based on the user's external activities and profile. Profile property personalization is available since the content is defined on the dashboard.

# Message via Identity API

Consider a scenario where the business wants to target users based on their unique identities across different platforms. They can do so using Message via Identity API to enable a cohesive messaging experience that transcends individual devices or channels. In a Message via Identity API campaign, both users and content must be passed in the API call

## Use Cases

The following are some of the ideal scenarios where the Message via Identity API feature becomes handy to engage with your users:

- Targeted Notifications Using External Segmentation Systems: Trigger notifications to target specific users identified and grouped by an external tool or service based on certain criteria.
- Notifications for Non-Promotional Use Cases: These notifications can be sent as general updates without requiring segmentation. They can be directed to specific individuals.

## Implementation

The following are the four major steps to use the Message via Identity API feature in the CleverTap dashboard:

1. Define the campaign parameters, including audience, content, and scheduling.
2. [Utilize the  Message via Identity API to programmatically initiate campaigns within CleverTap](https://developer.clevertap.com/docs/create-campaign-api#create-campaign-api---target-users-by-their-identities).
3. [Monitor responses and errors from the API to ensure successful execution](https://developer.clevertap.com/docs/api-errors).
4. [Evaluate campaign effectiveness using CleverTap Analytics and refine strategies for optimal outcomes](https://developer.clevertap.com/docs/create-campaign-api#view-campaigns-created-through-apis).

## Key Differentiator

The following is the key differentiator of CleverTap's Message via Identity API feature:

_Real-time Engagement_: Instantly respond to user actions.