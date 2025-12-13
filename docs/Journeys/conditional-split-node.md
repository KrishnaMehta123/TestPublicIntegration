---
title: Conditional Split Node
excerpt: >-
  Learn how to use the Conditional Split node to create personalized user
  journeys based on user details or actions.
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

The Conditional Split node in CleverTap Journeys empowers marketers to route users dynamically based on real-time behavior and profile attributes. The node evaluates the most recent user data at the exact moment a user reaches the node. Based on conditions configured using event properties or user profile attributes, CleverTap instantly determines which path the user should follow. This enables real-time segmentation within a journey, eliminating the need for static, pre-defined segments and unlocking adaptive, data-driven engagement flows.

For example, a music streaming app wants to split users based on the `plan_type` user property as soon as the user signs up. The Conditional Split node acts as a decision point within a journey. When a user completes sign-up and reaches this node, CleverTap evaluates the defined conditions using the most recent user data and instantly routes the user to the matching path.

Here, the triggering event is `Sign Up Completed`:

* `plan_type` = Premium → Sends a thank-you email with loyalty rewards.
* `plan_type` = Free → Sends an upgrade prompt.
* `Others` → Sends a generic thank-you message.

<Image alt="Split Based on User Property `plan_type`" align="center" width="40% " border={true} src="https://files.readme.io/64367ad6e2f692ab51d8f218186c5703760e04ff2fa7c609457c92eaaeba3e20-CS_Introduction.png">
  Split Based on Conditions
</Image>

# Key Features

The following are the key features of the Conditional Split node:

* **Real-Time Evaluation**: Distribution happens in real time when the previous node is a live trigger or delay node. This ensures users are routed instantly based on their latest property or behavior data. For example, a journey starts when a user launches the app. The Conditional Split node immediately checks the user’s most current `Subscription status`:

  <Image alt="Real-time Evaluation of Subscription Status " align="center" width="35% " border={true} src="https://files.readme.io/ec27578ca595efb4a1974d85ff6840b8507f3f64c297197bfc7df641066b3517-CS_Evaluation_of_Subscription_Status.png">
    Real-time Evaluation of Subscription Status 
  </Image>

  This ensures that if a user upgraded their subscription before launching the app, the journey reflects that in real time. 
* **Dynamic Targeting Based on User Property**: Users are routed based on real-time user profile attributes. For example, you are running a regional promotion. You can use the Conditional Split node to check the user property `location`. This helps you personalize messages geographically without needing separate journeys or static segments.

  <Image alt="Dynamic Targeting Based on User Location" align="center" width="40% " border={true} src="https://files.readme.io/f5bfc0669909ecdf48075c9ad901546dc4d2f2082bea2b88737a22d4e716388e-User_Property_CS.png">
    Dynamic Targeting Based on User Location
  </Image>
* **Contextual Event Property-Based Routing**: Trigger routing decisions based on live user actions, such as purchases, searches, or job applications, using event properties directly from the triggering event. This allows real-time branching of users into relevant paths the moment they perform an action, enabling instant, context-aware engagement. For example, a job portal app wants to tailor onboarding based on the type of job the user is looking for when they sign up. Now, with Conditional Split, the journey triggered by the Sign Up Completed event (Action node) can immediately route users based on the `preferred_job_type` event property submitted during signup:

  <Image alt="Event Property-Based Targeting" align="center" width="40% " border={true} src="https://files.readme.io/156a9199d5cd32d6419fdd53e3e911e68831b0fc2effeeb79d7cc8aa80f65c96-CS_Real-time_evaluation_of_Event_Porperties.webp">
    Event Property-Based Targeting
  </Image>
* **Combined Logic with Flexible AND/OR Operators**: Combine user and event properties, making split logic highly granular. For example, you are running a luxury promotion and want to tailor offers based on both `Loyalty Tier` tier and `Product Interest`.

  <Image alt="Combined Logic with Flexible AND/OR Operators" align="center" width="40% " border={true} src="https://files.readme.io/f20ee96cf21653357948cef275bd8cc3e5fb37115f7bfabd9b63fd9305741607-CS_Luxury_Promotion.png">
    Combined Logic with Flexible AND/OR Operators
  </Image>
* **Sequential Splitting**: Supports chaining up to three Conditional Split nodes within a journey. This allows you to evaluate multiple criteria step by step, creating layered, decision-based flows that adapt as more context becomes available. Each split adds more nuance based on what you know about the user, leading to hyper-relevant engagement without overwhelming a single decision point. For example, you are running a journey to promote tailored travel packages to users based on their travel intent and destination interest.
  * Split 1: Check Travel Intent
    * If Intent = Leisure, go to Split 2
    * If Intent = Business, send corporate travel offers
    * Others → Send a survey to understand user preferences
  * Split 2: Travel Destination Interest
    * If Interest = Beach, show tropical getaway packages
    * If Interest = Mountains, highlight hiking and cabin stays
    * Others → Recommend trending travel spots
* **Fallback Path**: Always includes an *Others* path to handle users who do not qualify for any of the paths. For example, if a Conditional Split is configured with conditions for `plan_type` = Premium and `plan_type` = Free, any user with a different or missing `plan_type` value is routed to the *Others* path and can be sent a generic message or a prompt to complete their profile.

# Resources

<HTMLBlock>{`
<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1rem;
    padding: 0 1rem;
    max-width: 100%;
    margin: 0 auto;
  }

  .integration-card {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding: 1.5rem 1rem; /* add top & bottom padding */
  min-height: 64px; /* ensures consistent tile height */
  background: #fff;
  border-radius: 12px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

  .integration-card:hover {
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  }

  .icon {
    width: 24px;
    height: 24px;
    stroke: #2b2e33;
    flex-shrink: 0;
  }

  .name {
    font-size: 1rem;
    font-weight: 600;
    color: #2b2e33;
  }
</style>

<div class="grid">
  <a href="https://docs.clevertap.com/docs/conditional-split-by-user-property" class="integration-card">
    <div class="name">Conditional Split by User Property</div>
  </a>
<a href="https://docs.clevertap.com/docs/conditional-split-by-event-property" class="integration-card">
    <div class="name">Conditional Split by Event Property</div>
  </a>
<a href="https://docs.clevertap.com/docs/conditional-split-with-advanced-conditions" class="integration-card">
    <div class="name">Conditional Split with Advanced Conditions</div>
  </a>
<a href="https://docs.clevertap.com/docs/create-conditional-split-journey" class="integration-card">
    <div class="name">Create Conditional Split Journey</div>
  </a>
<a href="https://docs.clevertap.com/docs/conditional-split-stats" class="integration-card">
  <div class="name">Conditional Split Stats</div>
</a>
</div>
`}</HTMLBlock>
