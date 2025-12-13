---
title: Group Unsubscribe
excerpt: Allow users to opt-out of a specific group of messages.
deprecated: false
hidden: false
metadata:
  title: ''
  description: >-
    DOCS NOTE: COMPARE/REVIEW WITH THE EXISTING PAGE:
    https://docs.clevertap.com/docs/handling-unsubscribes
  robots: index
next:
  description: ''
---
## Overview

CleverTap offers Group Unsubscribe, which allows customers to opt out of certain groups of messages. With Group Unsubscribe, the customer unsubscribes only from a particular group of messages but continues receiving the messages of interest. CleverTap tracks group unsubscribe if you are using a CleverTap-hosted Unsubscribe page or [CleverTap's unsubscription methods](doc:handling-unsubscribes) in your Custom Unsubscribe page.

## Subscription Groups

You can group every marketing campaign or outgoing communication message into different subscription group categories. Customers may like to receive messages about a particular category but might opt out of a separate category of messages.

## Create Subscription Groups

Perform the following steps to create a Subscription Group from a particular campaign.

1. From the CleverTap dashboard, select *Settings* > *Engage* > *Setup* *Subscription Groups*.
2. Enter the group's name, provide a brief description, and select the *Email* channel.

<Image title="Create Email Subscription Group" alt={1027} align="center" width="smart" border={true} src="https://files.readme.io/2c812d9-Email_subscription_group_setup.png">
  Create Subscription Group
</Image>

3. Click **Save**.

> 📘 Active Subscription Groups
>
> Customers can set up 50 active groups. They can also archive groups to create new ones.

## Use Subscription Groups in Segments

1. From the CleverTap dashboard, select  *Segments*  > *Find People*.

2. From *Display common properties such as* section, click **+Properties.**

3. Click **+Properties** and select *Subscription Groups* from the dropdown menu.

<Image title="Use Subscription Groups in Segments" alt={929} align="center" border={true} src="https://files.readme.io/fca954f-Email_subscription_group_list.png">
  Use Subscription Groups in Segments
</Image>

4. Select the *Exclude/Include* parameter and accept the All default or select one or multiple options.

<Image title="Include/Exclude Email Subscription Groups" alt={926} align="center" width="smart" border={true} src="https://files.readme.io/4412785-Email_subscription_group_include_exclude.png">
  Include/Exclude Subscription Groups
</Image>

## Use Subscription Groups in Campaigns

Subscription groups allow users to select the content they want to receive, reducing unsubscription rates and fostering strong brand-user relationships. This approach enhances user satisfaction and builds a more personalized connection with your audience.

You can select the subscription group you want to include in your campaign from the *Select Subscription Groups* list. This allows you to target users who have subscribed to all the groups you selected for the campaign. To do so:

1. From the CleverTap dashboard, select *Campaign* and create an email campaign. Refer to [Create Email Campaign](https://docs.clevertap.com/docs/create-message-email).
2. From the *Who* > *Control group and targeting cap* > *Send campaign only to users subscribed to all groups selected below*. 
3. Select the groups you want to include in your campaign from the *Select subscription groups* list.

<Image align="center" className="border" border={true} src="https://files.readme.io/e0653d9-image.png" />

4. Click **Done** and click **Continue**.
5. Complete creating the email campaign.

## Use Subscription Groups in Email Landing Page

Refer to [handling unsubscribes](https://docs.clevertap.com/docs/handling-unsubscribes) to add the Subscription Group configuration to your email landing page.

## Track Unsubscribes

Whenever a user unsubscribes, CleverTap raises a system event called *Channel Unsubscribed* which updates the user's property with the status of subscription for the group.

<Image title="Track Unsubscribes" alt={1012} align="center" width="50% " border={true} src="https://files.readme.io/b1c9872-Unsubscribe_last_step.png">
  Track Subscription Groups
</Image>
