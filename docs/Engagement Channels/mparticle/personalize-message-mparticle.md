---
title: Personalize Message
excerpt: Understand how to personalize your mParticle campaign
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

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](https://docs.clevertap.com/docs/events#event-properties).

# @ Personalization

To personalize your campaign, click **+Key-Value Pair** and click **@** symbol in the *Values* field when creating a message.

You can also add dynamic replacements in the *Values* field. The preview of the selected key-value pairs is displayed on the right side of the page (see figure below).

<Image title="Personalize mParticle Campaign" alt={2880} align="center" border={true} src="https://files.readme.io/3a9606f-Personalize_campaign.png">
  mParticle Campaign Personalization
</Image>

# Recommendations

Click the ![Personlization](https://files.readme.io/d946c02-personalization_icon.png) icon in the editor to open personalization options. 

You can send recommendation data to mParticle. For more information on recommendations, see [Recommendations](doc:recommendations).

# Constant event property

Constant Event Property allows you to engage the user on multiple actions and inactions. For example, person A added a white coat to the cart, and person B added a pair of blue jeans to the cart, but they both did not purchase the items. 

You can either create a campaign for each product added to the cart or use a *constant event property* to personalize the campaign to each user that did not purchase the item. 

For example, you can map the *prod\_name* property of the *charged* event to the *product\_name* property of the *added to cart* event. You can then hold this property constant across both events. Based on this property, you can now personalize the message received by each user.  For more information on using a constant event property, see [Constant Event Property](doc:constant-property).
