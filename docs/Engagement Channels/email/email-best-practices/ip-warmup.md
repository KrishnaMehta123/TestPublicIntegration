---
title: IP Warmup
excerpt: Understand the IP warmup process for CleverTap's Email messaging channel.
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

IP warming is the process of gradually increasing the volume of marketing emails to the required limit. The gradual increase in volume, paired with positive user engagement, helps to establish a positive reputation with inbox providers such as Gmail, Yahoo, and Outlook, among others.

With CleverTap's Advanced Email Add-on pack, you warm up from the designated IP address before sending higher mail volumes. 

IP warming does not always guarantee a positive sending reputation. Following these guidelines can help lower your risk of developing a negative sending reputation and increase the chances of developing a positive reputation.

These recommendations also apply to customers who use their email provider and want to scale volume or add a new domain.

# Prerequisites of IP Warmup

CleverTap highly recommends using a separate subdomain for different objectives, such as promotional and transactional emails. Using separate subdomains ensures that a negative reputation does not affect the deliverability of another subdomain. For example, you can keep transactional emails out of the spam folder and in your subscribers' inboxes, even if your promotional emails get a negative reputation. The following is an example showing two different subdomains for Promotional and Transactional emails, respectively: 

**Example for Promotional domain**: mail.example.com\
**Example for Transactional domain**: support.example.com

After purchasing CleverTap's Advanced Email Add-on pack, you can complete the email onboarding form with your marketing and/or transactional domains. Once CleverTap's Email onboarding manager confirms that your domain and IP setup is tested and complete, you can begin IP warming with your marketing emails.

# Set Up IP Warmup

This process involves the following major steps:

1. [Identify your most engaged users](doc:ip-warmup#identify-most-engaged-users).
2. [Verify your email lists to avoid bounces](doc:ip-warmup#verify-email-lists-to-prevent-bounces).
3. [Set up a warm-up user property to target each group of users](doc:ip-warmup#set-up-a-warmup-user-property).
4. [Create a relevant campaign for IP warmup purposes](doc:ip-warmup#create-a-relevant-campaign-for-ip-warmup).
5. [Target segment for IP warmup Day 1](doc:ip-warmup#target-segment-for-ip-warmup-day-1).
6. [Set up the rest of your IP warmup emails](doc:ip-warmup#set-up-the-rest-of-your-ip-warmup-emails).
7. [Review your entire campaign settings before publishing](doc:ip-warmup#review-entire-campaign-settings-before-publishing).

## Identify Most Engaged Users

During the IP warmup, prioritize your most engaged subscribers, typically those who have opened emails in the last 0-3 months. Targeting these active users with a demonstrated interest in your emails boosts the likelihood of positive engagement, enhancing your reputation with inbox providers. 

Eventually, you can include some medium-risk users who have shown engagement within the last 4-6 months. Emailing the high-risk group (more than six months) is not recommended during the warmup process. However, if you need to include the high-risk group in the warmup sends, seek advice and assistance from CleverTap's Email team.

In the absence of access to historical email engagement data, you can target users based on their app engagement, such as their last active time or push opt-ins.

## Verify Email Lists to Prevent Bounces

In the absence of historical data, there might be a higher chance that you send emails to inactive or invalid users during the warmup process. These invalid addresses can cause the emails to bounce and damage the domain/IP reputation. We recommend verifying your email list before starting the warmup to avoid these bounces.

The following are some of the email verification tools: [Clearout.io](doc:clearout), [NeverBounce](https://neverbounce.com/), [ZeroBounce](https://www.zerobounce.net/), [BriteVerify](http://www.briteverify.com/?pcode=leanplum), [EmailOversight](https://www.emailoversight.com/), etc.

## Set Up a Warmup User Property

Proper preparation is crucial before beginning the warmup process. Identifying your most engaged users and setting their properties is an essential step. To upload your user list to the CleverTap warmup dashboard, use a [CSV upload](doc:csv-upload). You can add a custom property column (for example, Historical data) with a defined value to track specific users to target on each warmup day. For example, add "Day1" to 50 of your most engaged users, "Day2" to another 100 most engaged users, and so on (see figure below). This way, you can easily track the progress of the warmup and adjust the strategy if needed.

<Image alt="Sample CSV of Most Engaged Users" align="center" border={true} src="https://files.readme.io/06697f4-image.png">
  Sample CSV of Most Engaged Users
</Image>

The purpose of distributing users based on the warm-up schedule is to ensure proper and effective IP warming. If the number of engaged users is too low, multiple email campaigns may be needed to achieve the desired warmup results. This approach allows users to be targeted more than once, increasing the likelihood of positive engagement. For more information on creating a successful email campaign, refer to [Create Email Campaign](doc:create-message-email).

## Create a Relevant Campaign for IP Warmup

From the *Campaigns* page, create an email campaign that will remain relevant to users throughout the entire warmup period. It is recommended to use the most common campaign content, such as how-to guides, tutorials, or any content that remains engaging and relevant throughout the warmup process. This ensures that users continue to receive relevant content as they progress through the warmup period.

> 📘 Email Best Practices
>
> Select the content that has had a high open rate in the past six months. During the IP warmup period, it is important to build a good reputation with ISPs. Therefore, it is recommended to use your most successful content to achieve a high level of audience engagement.
>
> The following are some of tips for setting up the campaign:
>
> * Sending emails with good text-to-image ratios.
> * Sending image-only emails can cause accessibility issues.
> * Sending image-heavy emails can also trigger spam filters and emails might land in spam folder
> * Keeping the email size less 100 KB to avoid the message clipping from Gmail

## Target Segment for IP Warmup Day 1

During your warmup period, you must target users based on their email engagement history and the assigned properties. For the first day of the warmup, select the user property `7 Day Clicker`, which should be your smallest volume of users, no more than 115 users, based on the recommended IP warming schedule. You can check if the number of users matches the warmup schedule by clicking *Calculate* under the *Who* section of the CleverTap campaigns.

After preparing the email campaign content, you can either send the email immediately by selecting *Send now* under the *Date and Time* section or schedule it for later by selecting *Schedule for later* and specifying a date and time according to your warmup dashboard settings. It is crucial to ensure that you follow the warmup schedule and avoid sending large volumes of emails to inactive or churned email addresses during the initial phase.

Ensure that you always *Preview & Test* the email messages before publishing a campaign.

## Set up the rest of your IP Warmup Emails

To create the remaining IP warming emails, follow the warmup schedule and clone your IP Warmup Day 1 email for each day until you reach your desired highest daily sending volume. When cloning a campaign, ensure that you adjust the daily volume per campaign based on the warmup schedule. To do this, you can use the Target segment feature and select the user property for the respective date.

<Image alt="Clone Warmup Day 1 Email Campaign" align="center" border={true} src="https://files.readme.io/91886fdc9770f02bf0ec2b9dc4c5df2e24d3742d05644d64515a3eb6e3b945ee-ok_11.png">
  Clone Warmup Day 1 Email Campaign
</Image>

If the segment size exceeds the recommended volume for the day, set the target cap according to your warmup schedule. 

Also, from Day 2 onwards, you must add an additional condition under the "Who have not done" section. Click **Add event** and select *Notification sent* in the last 30 days (or more if your warmup takes longer). By doing this, you exclude all users who have received an email in the past 30 days (or the previous days of the warmup).

## Review Entire Campaign Settings Before Publishing

After creating all the campaigns, CleverTap recommends ensuring the following before publishing:

* Required Email Service Provider is selected.
* Target Segment and Target segment cap are correctly aligned with the warmup schedule.
* The email campaign is properly visualized upon delivery, and all links are working and redirecting to the respective pages by using the Preview & Test feature.
* To ensure proper pacing, it is necessary to space out your actions with a 1-day interval. The first email should have the smallest audience, and each subsequent message should have a larger audience (based on your IP warmup user properties).

# Monitor Campaign Stats

The success of your email campaign on a daily basis can be influenced by the inbox provider's filters, which constantly evaluate engagement patterns toward your messages. Therefore, it is crucial to be mindful of how your emails are performing and adjust accordingly.

To ensure that your campaign is on the right track, we recommend you closely monitor your engagement metrics after sending each warmup day campaign. Specifically, keep an eye out for views/opens and clicks. A significant decline in either of these areas indicates possible spam filtering or issues with your links.\
If you do notice a trending decline in engagement metrics, taking action and pausing any remaining sends is important. You must then contact your Email onboarding manager or [CleverTap Support](mailto:support@clevertap.com) for assistance.

It is worth noting that in some cases, the numbers may not be exact. However, this should not be a cause for concern as long as the difference is small. Overall, paying close attention to engagement metrics and being proactive in making adjustments will help ensure the success of your email campaign.

# IP Warming Schedule

As mentioned in the earlier sections, you must target your most engaged subscribers for the earlier days of the warmup, then add moderately engaged users later on as you progress through the warmup period. The following is the sample warmup schedule: 

<Image alt="Sample Warmup Schedule" align="center" width="50% " border={true} src="https://files.readme.io/21a13e13834b6e4f23bfd3d974f6546a7902d5ba634dce778e6bd6f51d0f08a7-IP_Warmup_Schedule.png">
  Sample Warmup Schedule
</Image>

# FAQs

### Q. How often is the sender's reputation evaluated?

Ans. Your IP's sender reputation is assessed on a rolling 30-day calendar basis. If you have reduced your sending frequency in the past 30 days, you must adhere to the IP warmup schedule to re-establish your reputation.

### Q. Why is IP warmup crucial?

Ans. Email providers use a reputation score to decide where to place emails, such as the inbox or the junk folder. When you start sending emails from a new domain or IP, your reputation is neutral, and sending a large volume right away can negatively affect it. To avoid any negative impact on your reputation, it is important to conduct a warmup process that gradually establishes a positive reputation with email providers.

### Q. What should I expect during the IP warmup?

Ans. You should expect the following points during the IP warmup:

* CleverTap recommends waiting for 24 to 36 hours after sending an email to allow time for recipients to engage with it, which will provide accurate reporting metrics. 
* If the email is sent from an IP and domain that has not undergone a warm-up process, inbox providers may block it, which is a common occurrence. 
* Each inbox provider has a unique spam threshold and method of assessing reputation, so it's possible for spam filtering to occur on one domain but not on another.

### Q. When can I send mail to my less engaged audience?

A. Send a win-back campaign after the IP warmup is complete. Consider sending a campaign with a special promo or CTA before adding these emails to the distribution list. For example, "It has been a while. Do you still want to hear from us?"). If users still do not engage, remove them from all future marketing mailings if users do not engage, using [email sunsetting](doc:email-sunsetting) journeys. Continually targeting these emails can cause negative engagement, preventing your engaged users from receiving your emails.

### Q. What are some common mistakes to avoid during email IP warmup?

Ans. The following are some common mistakes to avoid during email IP warmup:

* After completing the IP warmup process, we recommend sending win-back campaigns in small batches.
* Before reintroducing these emails to your distribution list, you may want to send a campaign featuring a special promotion or call-to-action, such as "Do you still want to hear from us? It's been a while." If recipients still do not engage, it is best to remove them from all future marketing mailings using [email sunsetting](doc:email-sunsetting) journeys. 
* Persistently targeting this group can result in negative engagement, which may negatively impact the engagement of your active users and affect their ability to receive your emails in the future.

# Additional resources

Establishing and preserving your sender reputation involves numerous factors contributing to warming your IP and domain. For more information, refer to [Email Best Practices](doc:email-best-practices).
