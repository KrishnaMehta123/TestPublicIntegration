---
title: Reminders
excerpt: >-
  Learn how you can send automated reminders before or after a specific date to
  boost engagement, and ensure timely communication, enhancing the overall
  customer experience.
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

Reminders allow users to send personalized messages or notifications to take specific actions before or after a certain date. The primary aim is to enhance user engagement and productivity by proactively prompting users to complete tasks, meet deadlines, or adhere to schedules. By leveraging personalized notifications and flexible scheduling options, Reminders empower users to stay on top of their tasks and commitments, ultimately leading to improved time management.

# Reminders Video Tutorial

Check out the video tutorial for setting up Reminders in CleverTap.

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/pp7DS512FT1gIh3ZSvL2MQ/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

# Key Features

The following are the key features of Reminder Campaigns:

* **Personalization**: Reminders can be personalized to suit individual preferences and requirements, ensuring relevance and effectiveness.
* **Flexibility**: You can set Reminders for various tasks, events, or deadlines, accommodating diverse scheduling needs.
* **Scheduling**: You can schedule Reminders to trigger at specific times or dates or at a fixed time of their choice in a day or at the best time for the customer, allowing for precise timing of notifications.
* **Recurrence**: You can schedule recurring reminders, automating the process of reminding your customers about tasks or events. The message content can vary for each date, or messages can also be grouped together for a specified date range.
* **Disqualification Upon Cancellation**: You can ensure that cancellation automatically removes your customers from future notifications. For example, if a customer cancels a flight booking for any reason, they will be disqualified from receiving any further reminders associated with that booking.

# Use Cases

The following are some of the use cases for the Reminders feature:

### FinTech

You can send a reminder before or after the due date for different utility bill payments, such as electricity, credit card, postpaid bills, broadband, gas, and so on. The reminder can include personalization parameters, such as Bill Amount, Bill ID, Bill Due Date, and so on. 

In the case of pre-due date reminders, you can prompt your customers to make the payment before the due date to avoid penalties. For post-due date reminder notifications, inform your customers about the penalty incurred due to late payment and encourage them to settle the outstanding amount promptly.

### Subscription

In this case, the Reminders feature helps manage subscription renewals efficiently. You can send a reminder before the customer's subscription to OTT or FoodTech services expires.  In the case of pre-expiry reminders, you can prompt your customers to renew their subscriptions to avoid service interruption. For post-expiry reminders, you can send reminders with offers to incentivize renewal. You can send your customers special offers or discounts to encourage them to renew their subscriptions.

### EdTech

In this case, the Reminders feature ensures the timely completion of an online course for which students have enrolled. The student receives a reminder before the course end date. This encourages the student to review their progress and complete any remaining coursework to meet the deadline.

### Transactional

In this case, the Reminders feature helps customers stay informed and organized regarding upcoming bookings. For pre-event reminders, you can send a reminder before the scheduled booking date for a movie, event, or flight to remind your customers about upcoming events. The reminder provides essential details such as the date, time, and location of the booking, ensuring the customer is prepared for the event. Additionally, for post-event reminders, you can send notifications soliciting feedback on their flight experience or requesting movie reviews.

### E-Commerce

In this case, the Reminders feature helps drive voucher redemption by nudging users to use their allocated coupons before they expire. You can send reminders after a voucher is issued, such as during a festive sale, personalized campaign, or loyalty reward. The reminder can include personalization parameters such as Voucher Code, Discount Value, Expiry Date, and Eligible Products.\
For pre-expiry reminders, you can create urgency by highlighting the upcoming expiry date and encouraging redemption. Post-expiry reminders can inform users that the voucher has expired and optionally share alternate offers to retain engagement.

# Set Up Reminder

Consider the example where you want to remind your customers about their upcoming Credit Card bill due date. To ensure timely payment, you can define the trigger event under the *Setup* section.

> 📘 Prerequisite for Tracking Reminder Interactions
>
> Reminder-related events such as *Set Reminder*, *Reminder Cleared*, *Reminder Canceled*, and *Reminder Snoozed*, are tracked only after the Reminder setup is created and made live on the CleverTap dashboard. Events triggered before the setup goes live are not tracked.

To set up a Reminder, perform the following steps:

1. Go to *Reminders* page from the CleverTap dashboard and click **Create Reminder**. The *Setup* page opens.

<Image alt="Navigating to Reminders Page" align="center" border={true} src="https://files.readme.io/6be41bb-Create_a_Reminder.gif">
  Navigating to Reminders Page
</Image>

2. Enter the following details:

<Image alt="Set Up a Reminder" align="center" width="75% " border={true} src="https://files.readme.io/07f757a392e2fb894c04d2666991fe749b2be65f16ec6faa5092b0d53c959ede-Set_Up_Reminder.png">
  Set Up a Reminder
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Reminder Name
      </td>

      <td>
        Enter the name to uniquely identify your reminder.
      </td>
    </tr>

    <tr>
      <td>
        Duration
      </td>

      <td>
        Indicates the amount of time the reminder data is stored for each customer once the due date passes.
      </td>
    </tr>

    <tr>
      <td>
        Set Reminder
      </td>

      <td>
        Define the event to qualify your customers for the reminder campaigns. For example, you want to set up a reminder to pay the electricity bill. In this case, `Bill Reminder` can be the event that can qualify the customers for the Reminders campaign. <li> **Reminder ID**: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *Bill ID*, uniquely identifying the bill for which you are setting up a reminder.</li> <li> **Due Date**: Refers to the deadline or scheduled time by which a particular action or task needs to be completed or addressed. This due date serves as a reference point for triggering reminders to customers, ensuring that they are prompted to take necessary actions before the specified deadline. For this example, the due date for paying the Credit Card bill. </li> <li> **Event Properties for Personalization**: Refers to the customizable attributes or details associated with specific events or actions that can be used to personalize reminder messages sent to your customers. These event properties allow for tailoring reminders to individual users based on their specific interactions, preferences, or characteristics. You can add up to 10 properties for personalization. For example, Bill Amount, Payment Status, Category, and so on.</li>
      </td>
    </tr>

    <tr>
      <td>
        Clear Reminder/Cancel Reminder
      </td>

      <td>
        Refers to the action taken by a user or an administrator to deactivate or stop a scheduled reminder from being sent to a particular recipient.\
        Select the event that will be raised when the customer stops the scheduled reminder.\
        Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *Bill ID*, uniquely identifying the bill for which you are setting up a reminder.
      </td>
    </tr>

    <tr>
      <td>
        Snooze Reminder
      </td>

      <td>
        If a customer receives a reminder about a task they need to complete but are currently occupied, they can choose to snooze the reminder for a certain duration (for example, 1 day). During this snooze period, the reminder will not be sent. <li> Select the event that will be raised when the user stops the scheduled reminder. </li> <li> **Reminder ID**: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *Bill ID*, uniquely identifying the bill for which you are setting up the reminder. </li> <li> **Reminder Until**: Select the date until which you want to snooze the reminder.</li>
      </td>
    </tr>
  </tbody>
</Table>

After saving the reminder, you can update it to include additional event properties, allowing for greater flexibility in personalizing reminder messages.

# Create Campaign using Reminders

Consider the same example where you want to remind your customers about their upcoming Credit Card bill due date. You can create a targeted campaign using reminders to automate and personalize notifications. By setting up the right triggers, scheduling messages, and selecting the appropriate channels, you can ensure timely and effective communication, improving customer engagement and reducing missed payments.

After setting up the reminder, you can create a campaign using reminders:

1. From the *Setup* page, click **Create Campaign**. The *Select the channels for your Reminder campaigns* popup opens.

<Image alt="Select Channels for Reminder Campaign" align="center" border={true} src="https://files.readme.io/d34811692d7c954797d4f7bc316594cfad9c1a5c84acae4bace03a3faa07d2cc-Select_Channels_for_Reminder_Campaigns.png">
  Select Channels for Reminder Campaign
</Image>

2. Select the channel for your Reminder campaign. For this example, we are selecting Push Notification. The *New Push Notification Reminder* popup opens.

<Image alt="New Push Notification Reminder" align="center" width="90% " border={true} src="https://files.readme.io/c44c59a-New_Push_Notification_Reminder.png">
  New Push Notification Reminder
</Image>

2. Define the *Start here* section for the campaign.
3. Define the *Who* section. Here, you must define the duration for which engagements need to be sent. You can also filter your target audience.

<Image alt="Define Target Segment for Reminder Segment" align="center" width="75% " border={true} src="https://files.readme.io/2955c85-image.png">
  Define Target Segment for Reminder Campaign
</Image>

4. [Define the content for your Reminder campaigns](doc:reminders#define-message-for-reminder-campaigns).
5. [Define the *Date and time* to send the reminder campaign and also define the *Delivery preferences*](doc:reminders#define-schedule-and-delivery-preferences).

## Define Message for Reminder Campaigns

Consider the same example where you want to remind your customers about their upcoming Credit Card bill due date. When defining the target audience, we chose to send reminders two days before the due date, one reminder on the due date, and one reminder one day after the due date. Here, you can create different message variants for each day, that is, a different reminder message copy for -2 day, -1 day, due date, and +1 day. This customization allows for targeted messaging that aligns with the evolving context or objectives of each day.

<Image alt="Create Reminder Message for Each Day " align="center" width="65% " border={true} src="https://files.readme.io/679b331-Create_Reminder_Notification_for_Each_Day.png">
  Create Reminder Message for Each Day 
</Image>

You also have the option to define a common message for multiple days. In our example, you may want to send the same reminder copy before the due date (in this case, -2 days to -1 day), a different copy for the reminder to be sent on the due date, and a different reminder message copy to be sent one day after the due date (+1 day).

<Image alt="Define Common Reminder Copy For Date Range" align="center" width="75% " border={true} src="https://files.readme.io/1cfe543-Create_Common_Reminder_Copy_for_Date_Range.gif">
  Define Common Reminder Copy For Date Range
</Image>

You also have the option to copy a particular message and reuse it with minor or no changes, as shown in the following image:

<Image alt="Copy Message from a Particular Variant" align="center" border={true} src="https://files.readme.io/48a4863-Copy_Message_from_a_Particular_Variant.png">
  Copy Message from a Particular Variant
</Image>

## Define Schedule and Delivery Preferences

You can set up the *When* section to schedule the reminder campaign based on the following available options:

### Data and Time

You can deliver the Reminder campaigns at the following times:

* *Per the due date time*: Selecting this option allows you to deliver the reminder campaign on and around the due date, ensuring timely delivery of notifications.
* *Best time for every user*: Selecting this option allows you to send the reminder campaign to every customer based on their most active time throughout the day. For more information, refer to [Best Time Campaigns](doc:best-time).
* *A fixed time*: Selecting this option allows you to send the reminder campaign to the customers at a fixed time during the day.

<Image alt="Select Delivery Option for Reminder Campaigns " align="center" width="75% " border={true} src="https://files.readme.io/88a07fb-Date_and_Time_for_Reminder_Campaigns.png">
  Select Delivery Option for Reminder Campaigns 
</Image>

### Delivery Preferences

You can apply global campaign limits to determine how many notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the *Don’t apply global campaign limits to this campaign* option.

You can also select the *Advanced* checkbox to specify Do Not Disturb (DND) hours during which notifications from this campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image alt="Set Up Delivery Preferences for Reminder Campaign" align="center" width="65% " border={true} src="https://files.readme.io/d5c96d8-image.png">
  Set Up Delivery Preferences for Reminder Campaign
</Image>

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

#### Time To Live

Time to Live is the persistence of a notification sent to an end user. Push services such as FCM, APNS, XPS, Baidu, and HMS manage Time to Live. They regulate the time the system monitors user device status to deliver a push notification. Whenever the user is online during the set TTL period, the notification is delivered. Any user not coming online will not receive the push notification, and no notifications are attempted after the TTL period is over.

#### Do Not Disturb (DND)

Select this option to avoid sending messages during certain times of the day. By default, DND limits are based on the user's time zone. 

#### Cut-off

The campaign cut-off time ensures no notifications are sent after the specified time. Clevertap does not send notifications to the push services after the cut-off. This is useful if the campaign is time-sensitive and a later time makes the notification irrelevant.\
Select *Cut-off*  and specify the time to stop sending the notification when the target audience is large. This will cause a significant delay in processing the user queue, ensuring that no notification is sent after the set time.

# Reminder Stats

Each reminder is evaluated based on various factors, including the number of messages sent, engagement rates, and user actions. Reminder Stats can be broadly categorized into the following sections:

* [User Engagement and Insights](doc:reminders#user-engagement-and-insights)
* [Individual Campaign Performance](doc:reminders#individual-campaign-performance)

> 📘 Campaign Reports
>
> To generate reports for Reminders campaigns, contact your Customer Success Manager or the Support Team.

## User Engagement and Insights

This section offers an in-depth analysis of customer interactions with reminder campaigns, enabling you to measure engagement, identify trends, and optimize future campaigns for better performance. 

<Image alt="User Engagement Stats for Reminder" align="center" border={true} src="https://files.readme.io/160626711a09a381e46e976c60ffdb9a837182ed0d1629deee7d498d6f8919cb-Reminder_Setup_Stats_-_Final.png">
  User Engagement Stats for Reminder
</Image>

The key metrics analyzed include the following:

* **Actions Trend**
  * *Set*: Total number of reminders sent to users. This indicates the campaign reach.
  * *Clear*: Number of customers who manually dismissed or marked the reminder as completed. A high number suggests reminders are acknowledged but may also indicate your customers prefer fewer notifications.
  * *Cancel*: Number of customers who opted out of receiving further reminders. A high cancellation rate may indicate irrelevance or excessive notifications.
  * *Snooze*: Number of customers who postponed the reminder for a later time. This shows how many customers engage but prefer flexibility.
* **Performance By Channels**
  * *Channel Type*: The messaging channel used to deliver the reminder, such as push notifications, email, SMS, or InApp messages. The effectiveness of each channel varies based on user preferences and engagement patterns.
  * *Number of Campaigns*: The total campaigns executed through each channel. This helps analyze the distribution of reminders across different channels.
  * *Sent*: The total number of reminders sent through a particular channel. A higher number indicates a broader reach.
  * *Impressions*: The number of times a reminder was displayed to customers (applicable to certain channels such as InApp messages). 
  * *Clicked*: The number of customers who engaged with the reminder by clicking on it. A high click count suggests strong user interest and engagement.

## Individual Campaign Performance

You can view the performance of each campaign by clicking it from the *Performance By Channels* section. This section offers a detailed breakdown of each reminder campaign's performance, enabling you to measure engagement and refine future campaigns for improved results. For more information, refer to the Campaign Stats document for the respective messaging channel.

<Image alt="Individual Campaign Performance" align="center" width="75% " border={true} src="https://files.readme.io/f1625f525c065cdb361e60ff2cef4bf2a6dfd5c10874ac80859e54ccb23b1bc2-Reminder_Campaign_Stats.png">
  Individual Reminder Campaign Performance
</Image>

# FAQs

This section covers FAQs related to the Reminders.

### What value do CleverTap Reminders offer for my business?

CleverTap Reminders help reduce churn, boost conversions, and increase customer engagement by sending timely, automated nudges. This ensures users do not miss important actions, minimizes unnecessary notifications, and improves operational efficiency through smart automation.

### Which channels are supported for sending Reminders?

You can deliver Reminder campaigns via Push Notifications, SMS, Email, WhatsApp, and Webhooks.

### How do I create a Reminder campaign?

Set up predefined triggers to notify customers about key actions such as bill payments, subscription renewals, or special offers. Use **Set Reminder** and **Clear Reminder** events to qualify or disqualify customers based on their activity.

### How early can I schedule a Reminder?

You can schedule Reminders from: 

* 90 days before the action date 
* 60 days after the action date. 

For added flexibility, you can even schedule them up to 370 days in advance or 60 days post-deadline.

### Is it possible to set up multi-day Reminders?

Yes. You can schedule multi-day, multi-channel reminders within a single campaign. For example, reminders sent “5 days before,” “on the day,” and “after a missed action.”

### How does automatic Reminder cancellation work?

To cancel future notifications automatically, the **Clear Reminder** event must carry the same unique Reminder ID (for example, bill ID) used in the **Set Reminder** event. This ensures reminders stop once the action is completed.

### Can Reminders be personalized for each customer?

Yes. You can tailor Reminder messages with personalized details such as customer names, due dates, product info, and past interactions for every reminder day, making messages more relevant and engaging.

### How are Reminders different from regular campaigns?

Unlike standard campaigns, Reminders are proactive, automated, and intelligently responsive. They deliver multi-day, personalized nudges in a single campaign, automatically cancel notifications when actions are completed, and reduce the need for manual setup. Regular campaigns, on the other hand, require separate setups for each date and do not support automatic cancellations.

### What makes CleverTap Reminders different from Journeys?

Reminders qualify customers for each event instance and support recurring, personalized multi-day nudges (for example, D-5, D-3, D-1). Journeys, on the other hand, qualify users only once per trigger and offer personalization within a 24-hour window. Additionally, Reminder campaigns allow edits and schedule changes even while running, whereas Journeys restrict content updates once live.
