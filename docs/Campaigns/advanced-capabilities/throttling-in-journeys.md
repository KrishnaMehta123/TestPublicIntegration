---
title: Messaging Frequency Caps
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

Frequency caps help you control the number of messages your users receive. It is common to run multiple messaging campaigns simultaneously or in close proximity to one another. The same user may qualify for more than one of these campaigns and be subject to receiving several messages in short succession. 

Alternatively, for a recurring or triggered campaign, the same user may re-qualify for this campaign and receive the same message more than once. Frequency caps provide the capability to ensure your users do not receive too many messages. 

CleverTap has two types of frequency caps, including:

* *Global Frequency Caps* control the maximum messages a user can get across campaigns for a particular channel of communication.
* *Message-level Frequency Caps* define how often messages can be sent to a particular user for a particular campaign.

When a frequency cap applies to a user, CleverTap does not deliver the associated message. The dropped messages are accounted for in the campaign report error table.

# Global Frequency Caps

Global frequency caps operate on a per-channel basis and let you specify the message cadence, dwell time between messages, and throttle limits (delivery rates).

## Message Limits

You can define the maximum number of messages a user can receive from a specific communication channel across campaigns.

<Image align="center" className="border" border={true} src="https://files.readme.io/84c565d-Global_Message_Limits.png" />

> 👍 Cadence Example
>
> You can define a cadence of three push notifications in seven days. This ensures that users only receive three push messages in seven days.

## Dwell Time

For a communication channel, you can set a minimum time interval between consecutive messages sent to the same user across different campaigns. For example, you can set intervals between messages with a range of:

* Minimum gap: Five minutes
* Maximum gap: Seven days

<Image align="center" className="border" border={true} src="https://files.readme.io/59118b4-Dwell_time.png" />

<br />

## Throttle

Throttle is a feature that enables you to manage the rate at which notifications are sent to end users. It helps prevent overload on your platform/operations by distributing the incoming traffic over a longer period of time rather than redirecting too many users to your mobile application/website at once with too many notifications simultaneously. This feature can significantly reduce the peak traffic on your platform, enabling you to serve more customers without impacting the platform's performance.

Finding the optimal throttling rate is crucial in ensuring the effectiveness of your engagements. A high throttling rate can overload your platform, while a low rate can result in engagements running for longer than expected, affecting the relevance of your messages to end users. Therefore, it is important to strike a balance by setting a reasonable throttling rate that suits your engagement reach and frequency to ensure that your messaging stays relevant without overloading your platform.

> 📘 Throttle Limit Recommendations
>
> Check that you always set throttle limit to more than 100 when setting the Ad Hoc limit. 
>
> Always check that your throttle limit is set high enough to prevent messages from running for multiple days, because the messages will stop delivering after the third day. This ensures that the relevance for messsages is maintained. 
>
> The *restricted reach* of your messages is displayed in a banner below the *Global throttle limits*. Make sure that the restricted reach is higher than your expected reach to ensure that all users receive the messages.

### Types of Throttle

There are two types of throttle:

* *Global Limit*: Select this option to apply global throttle settings to control the overall rate of message delivery. This setting ensures a consistent throttling rate across all campaigns or engagement nodes in journeys.
* *Ad hoc Limit*: Select this option if you want to override the global throttle limits for specific campaigns or engagement nodes in journeys. This option allows for more granular control over message delivery rates based on individual requirements.

#### Global Limit

 The Global Limit is a default throttle setting that applies to all campaigns. This limit is set globally and can be configured from the *Settings* section. To change the throttle limit:

1. Go to *Settings > Setup > Campaign Limits*.
2. Click **Add channel** and select the channel from the list to add a throttle limit for the channel. 

<Image alt="Set Global Throttle" align="center" border={true} src="https://files.readme.io/d620174-Defined_Limit_Settings.png">
  Set Up Global Throttle Limits
</Image>

This is now the defined limit for all your campaigns. You can check this limit from the Campaigns by navigating to *Delivery preferences* under the  *When* section >.

<Image align="center" className="border" border={true} src="https://files.readme.io/89acccf-Defined_Limit_Campaign.png" />

#### Ad hoc Limit

 The Ad Hoc Limit enables you to use a custom throttle limit for a specific campaign, which is different from the Global Throttle settings. This is useful when you want to apply a different throttle limit for a particular campaign without changing the global settings.

1. Go to the *When* section > *Delivery preferences*. The Delivery preferences section displays the *Global Limit* and the *Ad Hoc Limit*. 
2. Select *Ad Hoc* Limit to change throttle the message from the current campaign.
3. Enter the value and Click **Done**.

<Image alt="Set Adhoc Limit" align="center" border={true} src="https://files.readme.io/f1ab9bb-Adhoc_Limit.png">
  Set Adhoc Limit
</Image>

The Ad Hoc limit applies only to the current campaign or an engagement node in journeys. 

### Throttling in Journeys

> 📘 Private Beta
>
> Currently, throttling in Journeys is released in Private Beta. If you want to access this feature, contact your Customer Success Manager (CSM).

For Journeys, throttle limits for the engagement nodes are the same as the Campaign throttle limits for Push notifications, SMS, Email, Webhooks, and WhatsApp. If global or ad hoc limits have not been set up already, you can define them under the *When* section during Journey creation. This option is not available for Campaigns.

<Image alt="Set Up Throttle Limits from Journeys" align="center" border={true} src="https://files.readme.io/b0793d6-Set_Up_Throttle_Limits_from_Journeys.gif">
  Set Up Throttle Limits from Journeys
</Image>

Depending on the time settings within a Journey, throttling may be allowed or disallowed:

* **Timezone**: The *Account Timezone* setting provides a centralized way to manage and schedule campaigns, ensuring consistency in timing and reporting across the entire user base. User Timezone settings are designed to send messages at the timezone the user was last active. Applying throttling in this context could cause delays in message delivery, disrupting optimal engagement times and reducing the overall effectiveness of the communication. To avoid this, throttling is allowed only when the messages are scheduled based on the Account Timezone. If you still schedule messages based on the User Timezone, a popup notifies you that throttling will be disabled for campaign limits.\
  Throttling is permitted when you schedule messages based on the User Timezone only if you select the *Exclude the node from user timezone* option. 

<Image alt="Throttling Permitted When Scheduling Campaigns Based on Account Timezone" align="center" border={true} src="https://files.readme.io/acbe90c-Available_in_Account_Timezone.gif">
  Throttling Permitted When Scheduling Campaigns Based on Account Timezone
</Image>

* **Best Time Campaigns**: The Best Time setting is designed to optimize message delivery by sending messages at times when users are most likely to engage based on their individual behavior and activity patterns. Throttling is not permitted in this context because it could cause delays in message delivery, disrupting the optimized timing and reducing the overall effectiveness of the campaign. Additionally, throttling would undermine the personalized nature of Best Time messaging by introducing inconsistencies in delivery, potentially diminishing the user experience. To ensure messages are delivered at the ideal moment, CleverTap disables throttling for campaigns that use Best Time, helping to maximize engagement success.

<Image align="center" className="border" border={true} src="https://files.readme.io/132f464-Throttling_Not_Permitted_for_Best_Time_Campaigns_.gif" />

* **Segment Action Node with Zero Sleep Time**: When a segment action node with zero sleep time is added before an engagement node, CleverTap automatically removes throttling for the following engagement node. Zero sleep time indicates that users should proceed immediately from the segment action to the next step without delay. In this scenario, throttling, which controls message delivery rates by spreading them out over time, conflicts with the intent of instant progression. By disabling throttling, CleverTap ensures that messages are delivered in real time, preserving their relevance and impact.\
  Additionally, when this configuration is applied, the system prompts for user confirmation, ensuring you are aware that the following engagement node will no longer be subject to throttling limits.

<Image alt="Segment Action Node with Zero Sleep Time" align="center" border={true} src="https://files.readme.io/694d0f1-Segment_Action_with_Zero_Sleep_Time.gif">
  Segment Action Node with Zero Sleep Time
</Image>

However, if you set a sleep time of more than 24 hours, throttle limits remain in effect for the engagement node that follows the segment action node.

<Image alt="Segment Action Node with Sleep Time Greater Than One Day" align="center" border={true} src="https://files.readme.io/0e1157d-Segment_Action_Node_with_Sleep_Time_Greater_than_One_Day.gif">
  Segment Action Node with Sleep Time Greater Than One Day
</Image>

# Message-level Frequency Caps

Message-level caps let you control the number of times a particular ongoing campaign is delivered to the same user. 

> 🚧 Message Level and Global Frequency Caps
>
> Message-level and global frequency caps work together when applied simultaneously. A user may be subject to either or both frequency cap limits.

> 📘 Note
>
> Session limits are not a part of Campaign limits. They are considered separately.

These caps are important for recurring campaigns or triggered campaigns where the same user may re-qualify multiple times to receive a message.

## Control Options

The control options include:

* Send every time the user qualifies (default): This sends a message every time the user qualifies (can choose to respect global caps).
* Send with a minimum gap of: This sets a minimum gap between subsequent messages. The minimum gap allowed is five minutes, and the maximum gap allowed is 30 days.
