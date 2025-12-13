---
title: API Segments
excerpt: >-
  Learn how to manage user segments in CleverTap with APIs for seamless audience
  targeting and engagement.
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

API Segments enable CleverTap customers to create and manage user segments directly through public APIs. You can leverage these segments for targeted campaigns and analytics. API Segments address the challenges of scalability, efficiency, and real-time updates, making them ideal for customers looking to integrate their internal segmentation systems with CleverTap.

You can manage these API Segments with the following two APIs:

* [Create Segment API](https://developer.clevertap.com/docs/create-segment-api)
* [Update Segment API](https://developer.clevertap.com/docs/update-segment-api)

> 📘 Private Beta
>
> This feature is currently released in Private Beta for select CleverTap customers. For early access to this feature, contact your Customer Success Manager.

# How Does it Work?

API Segments provide a seamless way to create and manage user segments programmatically instead of relying solely on the CleverTap dashboard. By leveraging CleverTap's APIs, businesses can segment users and ensure their segmentation strategy aligns with real-time engagement needs.

## Segment Creation

The Create Segment API allows you to create new user segments within CleverTap. To create a segment, you must send segment details, including the segment name and an optional Customer Segment ID (a unique identifier the customer uses to manage segments on their end). The Customer Segment ID allows you to update the segment using your own ID without mapping it to the CleverTap Segment ID. Upon successful creation, CleverTap generates a unique Segment ID to identify the segment within the system.  

In CleverTap, all segments created via API are categorized as *API Segments*, ensuring they are distinct from manually created segments.

### View API Segments

After creating a segment with APIs, you can view it from the *Segment* list page.

<Image alt="View API Segment on Segment List Page" align="center" border={true} src="https://files.readme.io/91122a3844319d1f684530de3bd95a162922679b995c65f4bbbc3b153314130e-API_Segments.png">
  View API Segment on Segment List Page
</Image>

## Segment Update

Once a segment is created, you can modify its membership in a segment using the Update Segment API. This API enables adding or removing users from an existing segment by providing the relevant user identities. CleverTap processes these updates by mapping the provided user identities to internal CleverTap IDs and updating user profiles accordingly. When using this API, a new user profile will be created automatically if a user does not exist in the CleverTap system.

## Engagement Readiness

You can use segments created via API across all the messaging channels. Whether for scheduled or instant engagement, CleverTap ensures that segment updates are reflected immediately, enabling precise targeting and timely messaging. CleverTap ensures that API Segments are available for engagement across the following campaign types:

* **Offline Campaigns**: Segments created via the API are categorized under **API Segments** and can be leveraged for offline engagement, such as Email or SMS. In offline campaigns, you can use these API segments only with the include/exclude rule, similar to Partner Segments.
* **Online Campaigns**: When a user is added or removed from the segment created via API, CleverTap triggers a system event called *Segment Membership Change*. This event allows customers to use API segments in real-time engagement workflows, ensuring timely communication through online channels. This event includes the following properties:
  * **Action**: Indicates whether a user was added or removed. For example, ADD or REMOVE.
  * **Segment Name**: The name of the updated segment. For example, Gold Users.
  * **Segment ID**: The unique identifier assigned to the segment. For example, 1739791829.
  * **Customer\_Segment\_ID**: A reference identifier the customer provides for external tracking. For example, SEG12345.

### Engage with API Segments

You can engage with users of API Segments by creating different campaigns and journeys. The process of creating campaigns for the Past Behavior Segment and Live Behavior Segment is the same, except for the step where you select the segment.

To select an API Segment in a campaign:

1. Go to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the *Messaging Channels* dropdown.
3. Click the **Who** dropdown. The *Target Segment* section opens.
4. Click **Add Rule** and then select *Segments* from the segmentation rules pop-up.
5. Select the *API Segments* from the available list of segments.

<Image alt="Targetting an API Segment in a Campaign/Journey" align="center" border={true} src="https://files.readme.io/86a555ff4213f6001ea7c63848955ceab609d9ac9588ddddb6191dd74ea146c2-Targeting_API_Segment.png">
  Targetting an API Segment in a Campaign/Journey
</Image>

To learn how to create a campaign, refer to [Create Message](doc:create-message-push#create-a-new-push-campaign).

## Real-Time Updates

CleverTap processes API requests instantly, ensuring that segment details are always up to date. This includes:

* **Membership Updates**: User additions or removals reflect immediately.
* **Reachability Numbers**: A segment's estimated number of reachable users updates dynamically.

These instant updates enable customers to run data-driven marketing campaigns efficiently and maximize user engagement.

# FAQs

Find answers to the following common questions about using API Segments:

### Is there a limit on API Segments?

The total number of segments per account is limited to 2,500.

### Can I delete a segment created via API?

Yes, but attempts to update a deleted segment will result in an error.

### What is the batch size of the APIs?

Each API request can handle up to 100 segments and 100 user profiles.

### Are API Segments available to all customers?

API Segments are available for customers using the **CleverTap Advanced** and **Cutting Edge** plans.

### Are system events triggered for API Segments billable?

Yes, system events triggered for API Segments are billable and are counted under data points consumption.

### How are API Segment-related events billed?

These events contribute to your overall data point consumption, which impacts your billing based on the plan to which you are subscribed.
