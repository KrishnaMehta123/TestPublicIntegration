---
title: Email Sender Reputation
excerpt: >-
  Ensure higher campaign performance with the majority of your emails landing in
  the users' inbox.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

The email sender reputation determines the swift acceptance of your emails by Inbox Service Providers (ISPs) and their subsequent delivery to users' inboxes. Each ISP evaluates this reputation metric over a 30-day rolling calendar period, reflecting the consistency and quality of your email sending practices. 

Maintaining a positive email sender reputation increases the chances of emails avoiding deferrals and landing directly in recipients' inboxes. Following [Email best practices](doc:email-best-practices) is crucial for maintaining a good sender reputation. Regularly monitoring reputation metrics is equally vital. By managing your sender reputation, you ensure consistent inbox delivery, fostering better audience engagement.

<Image align="center" className="border" border={true} src="https://files.readme.io/caba985-Email_Sender_ReputationV22x.png" />

# Best Practices

The following are the three practices that ensure a good email sender reputation:

* [Monitor Campaign Performance](doc:email-sender-reputation#monitor-campaign-performance)
* [Monitor Reputation and IP Health](doc:email-sender-reputation#monitor-reputation-and-ip-health)
* [Measure Actual Inbox Placement](doc:email-sender-reputation#measure-actual-inbox-placement)

## Monitor Campaign Performance

Monitoring your campaign performance is crucial for maintaining a positive email reputation and optimizing inbox placement. The more positive signals ISPs see for your emails, the higher your reputation is. In contrast, negative signals indicate that your email sending practices must improve for a better sender reputation with the ISPs. 

The following is the list of positive and negative signals that indicate your sender's good and bad reputation. Monitor these metrics to spot issues early and take corrective actions to protect your sender reputation for better email campaign efficacy.

### Positive signals

The following indicators highlight key aspects of your email sender reputation and contribute to successful delivery and engagement.

* **Consistent Sending Calendar**: Demonstrates a reliable sending pattern - The amount of emails you send on a daily and monthly basis needs to have a consistent pattern. You must avoid email blasts or long periods of inactivity. 
* **High Delivered per Sent Rate**: Indicates a healthy user list with active and engaged recipients, leading to a higher percentage of emails reaching their intended destination.
* **High Unique Open Rate**: Reflects user interest and engagement, signaling to ISPs that your emails are wanted and of interest to recipients. It is important to allow a sufficient time window (12-24 hours) after sending the emails to measure open rates accurately.
* **High Click Rate**: Similar to open rates, a high click-through rate suggests content relevance and engagement, reinforcing a positive sender reputation.
* **Additional User Engagement Actions**: Actions such as marking an email important, starring it, moving to a separate folder, replying, or forwarding emails indicate active user interaction and interest, further bolstering the sender's reputation and credibility.

### Negative Signals

The following indicators point to potential issues in your email sending practices that will harm your sender reputation and, therefore, your email program:

* **Inconsistent Calendar**: Watch out for spikes in email volume - A spike is when your total daily volume is more than twice your largest send for the last 30 days. Another inconsistency when it comes to your email sending calendar are long periods of inactivity.\
  **To avoid spikes** - If you need to send a large number of emails that exceed more than double your usual highest volume, you must break down the campaign into smaller increments and send it over a few days. To learn how to do this, refer to [IP Warmup Schedule](doc:ip-warmup). You may also have to start the IP warmup from scratch if you have not sent or sent very few emails in a long time.  
* **Low Delivered per Sent Rate with High Bounce Rate**: Let's say you experience a low rate of emails delivered per campaign combined with a high bounce rate. It could indicate issues with data collection practices or potential spam blocks on your domain or IP address. 
* **Low Open Rates**: When recipients consistently fail to open your emails, it indicates that they are unwanted. Over time, this can lead to your emails being diverted to spam folders by ISPs, negatively impacting your sender reputation.
* **High Unsubscribe Rates**: Similar to low open rates, high unsubscribe rates indicate that recipients are not finding value in your emails. ISPs interpret this as a sign that your emails are unwanted, thus lowering your sender reputation.
* **High Spam Complaint Rate:** This signal could significantly impact your sender reputation. If a large number of recipients consistently report your emails as spam, ISPs are likely to start placing all of your messages directly in spam. 
* **Other Negative User Actions:** Deleting emails without opening them; filtering emails to trash, or listing your *From address* in personal block lists. Such actions indicate dissatisfaction with your emails and can lead to a decline in your sender reputation.

## Monitor Reputation and IP Health

Besides analyzing email metrics, various tools and services can help assess your reputation effectively. Below is a list of such tools and services, along with brief descriptions of how each can contribute to your email reputation management strategy:

* **Check Block Lists with[MXToolbox](https://mxtoolbox.com/blacklists.aspx):** Utilize free tools such as MXToolbox to verify whether your domain or IP address is on any block lists. If your domain or IP address is present under any block lists, this impacts email deliverability.
* **Measure Sender Reputation Using Tools:** Measure your email reputation specifically within Gmail using Google Postmaster Tools. This can provide insights into factors affecting deliverability to Gmail users.
* **Assess Sender Reputation Using[Sender Score](https://senderscore.org/) and [Barracuda Central](https://www.barracudacentral.org/lookups)**: Use the following free tools to assess your sender reputation: 
  * *Sender Score* provides a numerical score based on various factors affecting email deliverability
  * *Barracuda Central* is a reputation and security service that checks if your domain or IP has been flagged for suspicious activity.
* **Access IP Stats via Microsoft SNDS:** Get insights into your email sender reputation within Microsoft's ecosystem by contacting  [emailteam@clevertap.com](mailto:emailteam@clevertap.com).

## Measure Actual Inbox Placement

Inbox placement refers to the successful delivery of an email into a recipient's inbox, ensuring visibility and engagement. 

The only way to measure your actual Inbox placement is via [seed testing](doc:email-seed-testing). Most marketers utilize third-party paid solutions such as [Return Path](https://www.validity.com/products/returnpath/), [Email on Acid](https://www.emailonacid.com/help-article/how-to-run-a-spam-test-via-seed-list/), [Litmus](https://www.litmus.com/pre-send-testing/) and so on. To send emails to a seed list, upload the list as *users* on CleverTap. Ensure each user possesses all required user properties, including email address and other identity information. Additionally, create a custom property to distinguish seed list recipients from other users within the platform. This structured approach facilitates targeted communication and precise campaign management.

If you want to understand your reputation and campaign performance or notice a significant drop in email metrics, contact [support@clevertap.com](mailto:support@clevertap.com). If you are sending emails through CleverTap's ESP (Sendgrid), contact [emailteam@clevertap.com](mailto:emailteam@clevertap.com)
