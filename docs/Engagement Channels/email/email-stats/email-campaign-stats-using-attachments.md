---
title: Email Campaign Stats
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

Once the campaign is published, you can view the detailed campaign stats under the All Campaigns page. The Stats tab displays the overall conversion performance and errors.

# View Email Campaign Stats

After the email campaign is live, the following events are raised in case of email campaigns:

* *Notification Sent* when the email campaign is sent to the user.
* *Notification Viewed* when the user opens the email campaign.
* *Notification Clicked* when the user clicks on the email campaign. 

You can view its stats by navigating to *Campaigns* from the CleverTap dashboard. To do so:

1. Click *Campaigns* from the dashboard. The *All Campaigns* page displays.
2. Select the email campaign for which you want to view the stats. You can also filter campaigns using the **Filter** button (see figure below).

<Image title="Filter Email Campaign from All Campaigns" alt="Filter Email Campaigns" align="center" border={true} src="https://files.readme.io/5ef8ad422137f9919071243c4ecfcfaaa803bea361cf851096c76eb82c5f44a6-11.png">
  Filter Email Campaigns
</Image>

3. Click the campaign to open it. The *Stats* tab displays the following campaign stats: Sent, Viewed, Clicks, CTR, and Converted users (refer to the image below).

<Image alt="Overall Campaign Performance" align="center" border={true} src="https://files.readme.io/f7f4138f5d3338f644a451020649a04c8bba11679bfe3ee012f09dfc9fe80d2f-main_stats.png">
  Overall Campaign Performance
</Image>

> 📘 Unique Stats
>
> You can view unique count for Sent, Delivered, Viewed, Clicks, CTR, and Converted users. The feature is currently released in Private Beta. For more information, refer to [Email Campaign Unique Stats ](doc:email-campaign-stats-uniqueclicks). To gain access, contact your Customer Success Manager.

<Table>
  <thead>
    <tr>
      <th>
        **Metric**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Sent**
      </td>

      <td>
        Displays the total number of emails delivered. This count excludes the count of emails sent to CC and BCC recipients.
      </td>
    </tr>

    <tr>
      <td>
        **Viewed**
      </td>

      <td>
        Displays the aggregate open percentage for your message, which is calculated as `(Viewed/Sent)*100`. It also shows the total number of emails opened. The views of CC/BCC recipients are attributed to the main recipient. <br /> • **AMP for Email Viewed**: Displays the percentage of your total emails rendered as [AMP emails](https://docs.clevertap.com/docs/ampforemail). Displayed in case of AMP Email campaigns. <br /> • **HTML Viewed**: Displays the percentage of your total emails rendered as HTML.
      </td>
    </tr>

    <tr>
      <td>
        **Delivered**
      </td>

      <td>
        This metric enhances reporting accuracy by providing a clearer view of emails that have successfully reached users' inboxes. It is currently in Private Beta. To gain access, contact your Customer Success Manager, and for more details, refer to [Email Delivered Stats](doc:email-campaign-stats-delivered).
      </td>
    </tr>

    <tr>
      <td>
        **Clicks**
      </td>

      <td>
        Displays the aggregate percentage of clicks from the total sent messages. It is calculated as `(Clicks/Sent)*100`. It also shows the total number of clicks on the emails. The clicks of CC/BCC recipients are attributed to the main recipient. <br /> • **AMP for Email Clicks**: Displays the percentage of clicks on emails rendered as AMP. Displayed in case of AMP Email campaigns. <br /> • **HTML Clicks**: Displays the percentage of clicks on emails rendered as HTML.
      </td>
    </tr>

    <tr>
      <td>
        **CTR**
      </td>

      <td>
        The clickthrough rate of the campaign. It is calculated as `(Click/Viewed)*100`.
      </td>
    </tr>

    <tr>
      <td>
        **Converted users**
      </td>

      <td>
        Displays the percentage of total users who performed the conversion event, for example, purchasing an item. It also shows the number of users who converted after receiving the campaign.
      </td>
    </tr>

    <tr>
      <td>
        **Errors**
      </td>

      <td>
        Displays the number of errors for the campaign. These can be technical errors, such as email provider errors, or non-technical errors, such as message frequency exceeded.
      </td>
    </tr>

    <tr>
      <td>
        **Control group**
      </td>

      <td>
        Displays the number of users considered part of a control group for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        **Global Unsubscribes**
      </td>

      <td>
        Displays the total number of unsubscriptions. The unsubscription is attributed to the primary recipients who qualify for the campaign only if you use the `unsubscribe(isReEncode)` method to [unsubscribe from an email campaign](doc:handling-unsubscribes).
      </td>
    </tr>

    <tr>
      <td>
        **CC/BCC Metrics**
      </td>

      <td>
        CC (Carbon Copy) and BCC (Blind Carbon Copy) are used to send copies of emails to additional recipients. CC recipients can see all other recipients, while BCC recipients are hidden from each other and from other recipients. Note: The CC/BCC feature is currently in Private Beta. To gain access, contact your customer success manager and for more details, refer to [Sender Details](doc:create-message-private-beta#sender-details).
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Note
>
> Tracking delivery related errors like Unsubscribes, Bounces, and Report as Spam are not available for CC/BCC recipients.

## Message Trend

Click **Message Trend** to view the message trends by Sent, Viewed, or Clicked. You can view the daily, weekly, or monthly trends.

<Image title="View Message Trend Stats of Email Campaign" alt={2680} align="center" border={true} src="https://files.readme.io/27a73a8-Email_Stats_Message_Trend.png">
  Message Trend
</Image>

## Conversion Performance

Click *Conversion Performance* to view conversion, revenue performance, and users' conversion funnel. 

<Image title="View Conversion Stas of Email Campaign" alt={2726} align="center" width="85% " border={true} src="https://files.readme.io/32d1f59-Email_stats_conversion_performance.png">
  Conversion Performance
</Image>

You can view stats for each variant under the User conversion funnel for A/B test, split delivery, and message on user property campaigns.

**Conversion Performance**

The conversion performance section shows the conversion boost achieved from your campaign.  You can compare your campaign conversions with the control group conversions to see the impact of your campaign. 

<Image title="View Conversion Performance Stats of Email Campaign" alt={1310} align="center" width="85% " border={true} src="https://files.readme.io/7bf34ea-Email_Stats_Conversion_Conversion_hero.png">
  Conversion Performance Stats
</Image>

**Revenue Performance**

The *Revenue Performance* section shows the revenue boost achieved from your campaign. The following information is displayed in this section:

* *Incremental revenue due to this campaign*: Indicates the additional income directly attributed to a specific campaign. It is calculated as:\
  [(ARPU of Target Group – ARPU of Control Group) x Number of Users to whom the campaign was sent], where ARPU is calculated as: (Revenue generated / Number of users to whom the camapign was sent)
* *Boost in revenue due to this campaign*: Indicates the percentage increase in revenue achieved as a result of running the campaign compared (revenue generated from Target Group) to the baseline revenue that would have been generated without it (revenue generated from Control Group). It is calculated as:\
  \{\[(Target Group ARPU – Control Group ARPU) / Control Group ARPU] x 100}
* *Target Group Revenue*: Indicates the total revenue generated by users who were targeted by the campaign.
* *Control Group Revenue*: Indicates the total revenue generated by users who were not targeted by the campaign (control group).

  <Image alt="Revenue Performance" align="center" width="75% " border={true} src="https://files.readme.io/07478a68a9d980cffaae04f57fbe73aa4ee73c6fc627762d07185a54379a6c2f-revenue_performance.png">
    Revenue Performance
  </Image>

## Users Conversion Funnel

Shows the conversion funnel, that is *Sent* > *Viewed* > *Clicked* > *Converted*. You can understand the drop-offs at each step of the campaign.

<Image title="View Users Conversion Funnel of Email Campaign" alt={2592} align="center" border={true} src="https://files.readme.io/9e1b1ae-Email_Stats_Conversion_Performance_with_Viewed.png">
  Users' Conversion Funnel
</Image>

### Hide Viewed

The *Viewed* numbers in a report can sometimes be unusually high because of virus scanners, email forwards, email groups, and so on. For more information, refer to [Unusually High Email Opens and Clicks](doc:troubleshooting-open-click-tracking). In this case, you can hide the viewed step by selecting the \_Hide Viewed\_button.

<Image title="Hide Viewed Funnel of Users Conversion" alt={2698} align="center" border={true} src="https://files.readme.io/b4954e5-Email_Stats_Conversion_Performance_No_Viewed.png">
  Hide Viewed Funnel
</Image>

> 📘 Key Points to Remember
>
> The Conversion Performance number for *All Variants* may be equal to or less than the combined Conversion Performance number for each individual variant. For example, if the Conversion Performance number for All Variants is 10500, with Variant A at 5575 and Variant B at 5053, the total for Variants A and B combined is 10628, exceeding the total for *All Variants*.
>
> This scenario can occur due to the following reasons:
>
> * For Live campaigns, different variants are delivered to various devices, identified by different GUIDs for the same user. Consequently, the Conversion Performance number for All Variants might not match the sum of the Conversion Performance numbers for each variant. For instance, a user may receive Variant A before uninstalling the app and then receive Variant B after reinstalling it until their identity is established.
> * For Recurring campaigns (user property campaigns), the user can qualify more than once when and receive different message copy each time. For example, the user upgrades to a new plan. In this case, the message copy received by the user before and after upgrading the *Membership type* can be different.
>
> In both the cases, the same user is counted twice, once for Variant A and once for Variant B. However, when calculating the Conversion Performance number for *All Variants*, each user is counted only once.

## Split of Clicks

You can track the distribution of clicks on each link that you include in your email campaign.  For example, you want to send an email promotion for an upcoming movie on your video streaming app. You can create an email campaign, add links for reviews, promotions, movie merchandise, and so on, and then send the campaign.  We will record the clicks for each link in the email, and you can see them on the Campaign Stats page. 

> 📘 Click Heat Map
>
> Click Heat Map lets you see exactly where users are clicking within your emails through a visual, color-coded overlay. Use these insights to optimize content placement, refine CTAs, and improve campaign performance across teams. It is currently in Private Beta. To gain access, contact your Customer Success Manager. For more information, refer to [Link Clicks](doc:email-campaign-stats-heatmap#link-clicks).

<Image title="View Split of Clicks for Clicked Links" alt={2708} align="center" border={true} src="https://files.readme.io/8dc04dc-Email_Stats_Split_Clicks.png">
  Split of Clicks
</Image>

### User Details of Clicks

You can view the details of users who clicked on your email campaign using the *View details of users who clicked* link present on the *Split of Clicks* tab. You are navigated to the *Events* page. Click the *People* tab to view user details. 

<Image title="View Event Analysis for Notification Clicked" alt={1049} align="center" border={true} src="https://files.readme.io/d55d148-Email_stats_notification_clicked.png">
  Event Analysis for Notification Clicked
</Image>

## Errors

You can view campaign errors from the *Stats* > *Errors* tab.

<Image title="View Email Campaign Errors" alt={2702} align="center" border={true} src="https://files.readme.io/579eaeac43e3f43aab26ed06c0762a092c6ab44a783beb1e81c23538f3e8372c-Email_-_Errors.png">
  Email Campaign Errors
</Image>

These errors can be broadly categorized into two categories:

* Dispatch Errors
* Delivery Errors

### Dispatch Errors

Dispatch errors occur when a campaign is triggered but fails to reach the Email Service Provider (ESP) for delivery.

| Error                         | Description                                                                                                                                                                                                                                                                                                                                                                                                      |
| :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Email Dispatch Error          | Occurs when an attempt to send an email to a user fails before it can be successfully dispatched.                                                                                                                                                                                                                                                                                                                |
| SendGrid email dispatch error | Occurs when an email sent via CleverTap using SendGrid as the ESP fails to be dispatched. This implies that the email was not successfully handed off to SendGrid for delivery, preventing it from reaching the recipient inbox.                                                                                                                                                                                 |
| Attachment errors             | Occurs due to an issue with the attached file while sending the campaign, preventing the email from being delivered. A soft bounce is recorded and listed under the *Errors* tab on the campaign *Stats* page. However, the **recipient is not unsubscribed** from future emails. Additionally, the **Notification Failed** event is also triggered, with the event property *Error* set to *Attachment errors*. |

> 📘 Private Beta
>
> The Email Attachments feature is currently released in Private Beta. The feature is currently available for **SendGrid** and **Infobip** (with Advanced Email Add-on) providers. For early access, contact Customer Success Manager.

### Delivery Errors

Delivery errors occur after an email campaign has been successfully dispatched to the ESP but fails to reach the recipient inbox. These errors indicate that the ESP accepted the message but was unable to deliver it for various reasons.

#### Soft Bounce

A soft bounce indicates that the email bounced due to one of the following reasons, even though the email address was valid and the email message reached the recipient email server:

* The mailbox was full (the user has exceeded their storage quota)
* The recipient server was down
* The message was rejected as spam
* The message was too large for the recipient's inbox.

CleverTap campaign reports include soft bounces and do not mark the users as unsubscribed.

#### Hard Bounce

A hard bounce indicated that the email was returned to the sender and was completely undeliverable. However, common reasons it got rejected include:

* The email address is invalid
* The email address does not exist
* The recipient's email server has rejected the email

CleverTap campaign reports include hard bounces and mark the users as unsubscribed.

> 📘 Deferred emails
>
> The time for retrying a deferred email and the number of retries depend on the sending ESP. For SendGrid, the retry period is set to 72 hours.

# View Detailed Engagement Stats

You can also view the user details for notifications *sent*, *viewed*, *clicked*, and *bounced* from the *Analytics* page of the CleverTap dashboard. For more information about viewing such stats, refer to [Analyze an Event ](doc:events-analytics#analyze-an-event). 

<Image title="View Event Analysis for Notification Viewed" alt={2658} align="center" border={true} src="https://files.readme.io/46340b1-Events.png">
  Event Analysis for Notification Viewed
</Image>
