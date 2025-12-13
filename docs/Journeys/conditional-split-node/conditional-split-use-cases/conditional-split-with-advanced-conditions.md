---
title: Conditional Split with Advanced Conditions
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
# Overview

The Advanced Split configuration enhances the flexibility of the Conditional Split node by allowing marketers to define complex split conditions using AND/OR logic across user properties and event properties of different data types. This enables highly targeted personalization within Journeys based on combinations of real-time and historical user data.

Advanced Conditions also support real-time triggers (from Action nodes) and scheduled PBS-based triggers, offering flexibility across journey types. This mode is useful when journey logic depends on both static user profile details and contextual event data, such as recent purchases, last browsed items, or user engagement history.

Use the Advanced configuration when your targeting criteria involve multiple conditions per path. For example:

* Target users who are on a Premium plan AND located in Mumbai
* Target users who purchased an Electronics product OR used a coupon code

You can create conditions based on the following data types: String, Boolean, Number, or DateTime properties. For example:

* `plan_type` = Premium (String)
* `order_value` > 500 (Number)
* `is_first_time_buyer` = true (Boolean)
* `event_time` \< 7 days ago (DateTime)

# Target Evaluation Type: Action Node

When an Action node triggers a journey, the Conditional Split can evaluate event properties from the triggering event in real time alongside user properties.

For example, a fitness app wants to personalize post-workout follow-ups based on:

* **User property**: `customer_type`  
* **Event property**: `workout_duration`

**Setup**

* Trigger: The journey starts when a user logs a workout session (Action node).
* Conditional Split (Advanced): Evaluates both the `Customer Type` (user property) and `workout_type` (event property) from the same workout event. 

<Image alt="Advanced Split Setup for Trigger Type Action Node" align="center" width="60% " border={true} src="https://files.readme.io/423bcb1442a8f53aa60aa9bddf9dc6152aeb7b21f27bdccaf0ccd3a43e1d3351-Advaced_-_Trigger_Type_Action_Node.png">
  Advanced Split Setup for Trigger Type Action Node
</Image>

**Conditions and Paths**

* Condition 1: `Customer Type` = Premium AND `workout_type` = Cardio\
  → Sends a curated HIIT playlist via email, followed by a push reminder for cooldown tracking.
* Condition 2: `Customer Type` = Free AND `workout_type` > Cardio\
  → Sends an upgrade prompt email highlighting premium recovery videos, followed by a push the next day.
* Condition 3: `Customer Type` = Premium AND `workout_type` = Weight Training\
  → Sends a quick post-strength stretch routine via email, followed by a push notification with muscle recovery tips.
* Fallback Path: Others\
  → Sends a motivational push to encourage consistent logging and engagement.

<Image alt="Advanced Split Journey for Trigger Type Action Node " align="center" border={true} src="https://files.readme.io/689ecaa8722dfe36667e727576eb5ac6f5f57a8e68f516c7646fb1a902b39def-Advaced_Use_Case_-_Action_Node_Journey.png">
  Advanced Split Journey for Trigger Type Action Node 
</Image>

This approach ensures that every user receives a contextual message tailored to their fitness behavior and membership level in real time without requiring multiple nested segments.

# Trigger Type: Past Behavior Segment

When the Past Behavior Segment (PBS) triggers a journey, the Conditional Split node in Advanced mode can evaluate multiple user properties using Advanced Split logic. While a basic split may rely on a single attribute, Advanced configuration allows combining several user-level criteria using AND/OR operators, supporting precise targeting.

For example, a FinTech app wants to re-engage dormant users by tailoring communication based on their subscription tier and investment profile.

**Setup**

* Trigger: PBS segment `DormantUsers` (users inactive for 30 days)
* Split Logic: The Advanced Conditional Split node evaluates:
  * `plan_type` (user property)
  * `investment_profile` (user property)

<Image alt="Conditional Split with Advanced Use Case Setup" align="center" width="65% " border={true} src="https://files.readme.io/8ca53545895d5eafbc5d02deda8957dd91149a5cca95b618cebdd277508bec6b-Advanced_Conditional_SPlit_Setup.png">
  Conditional Split with Advanced Use Case Setup
</Image>

**Conditions and Paths**

* Condition 1: `plan_type` = Premium AND `investment_profile` = Aggressive\
  → Sends an SMS with high-return investment ideas and a personalized win-back offer.
* Condition 2: `plan_type` = Free AND `investment_profile` = Conservative\
  → Sends an email with savings tips and curated low-risk product recommendations.
* Fallback Path: No match\
  → Sends a push notification with a limited-time discount or referral bonus.

<Image alt="Conditional Split with Advanced Use Case Journey" align="center" border={true} src="https://files.readme.io/567841e0c658293c4c29b40be77a988fadad0f068b56ba485115fd11f2687d9c-Advanced_CS_Journey.png">
  Conditional Split with Advanced Use Case Journey
</Image>

The Conditional Split node uses the most updated user profile data at the time of qualification. Users are evaluated once and moved through their respective paths after satisfying the intermediate conditions, if any (such as a delay node).
