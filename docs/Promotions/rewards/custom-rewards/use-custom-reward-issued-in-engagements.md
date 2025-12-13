---
title: Use Custom Reward Issued in Engagements
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

CleverTap allows you to engage users who have received a Custom Reward by targeting them through the CT Custom Reward Issued event.

This system event helps you personalize communication and drive users to complete key actions, such as redeeming an offer, using a reward, or making a follow-up purchase.

# Use Custom Reward Issued in Engagements

If you are a food delivery app that wants to increase redemption rates on the app. Let's say you want to remind users who received a custom reward but have not redeemed it yet. You can set up a campaign as follows:

1. Go to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the *Messaging Channels* dropdown.
3. Click **Add an event** from the *Who* section.
4. Select the *CT Custom Reward Issued* event and the required *Event Property*.

<Image alt="Target CT Custom Reward Issued Users with a Campaign/Journey" align="center" border={true} src="https://files.readme.io/f81f7887d173e10a42a487baf665044f7d8559a9fe6cce5ca287b21a2b2a776a-image.png">
  Target CT Custom Reward Issued Users with a Campaign/Journey
</Image>

For more information about creating a campaign, refer to the *Create Message* document of the respective messaging channel.

# CT Custom Reward Issued

After a custom reward is issued to a user, CleverTap logs the *CT Custom Reward Issued* event. This event enables you to engage users by creating targeted campaigns based on custom reward-related actions.

This event includes both System and Custom Properties that allow you to: 

* Filter users for targeted engagement.
* Personalize message content using Liquid Tags.
