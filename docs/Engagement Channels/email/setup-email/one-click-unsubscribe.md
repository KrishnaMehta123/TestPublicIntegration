---
title: One-Click Unsubscribe
excerpt: >-
  Learn how to implement List Unsubscribe header in CleverTap dashboard to
  comply with Gmail and Yahoo email sender guidelines.
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

Starting February 2024, Gmail will require the following for senders who send 5,000 or more messages a day to Gmail or Yahoo accounts: 

* Authenticate outgoing email, 
* Avoid sending unwanted or unsolicited emails, and 
* Simplify for recipients the process to unsubscribe.

To comply with the above guidelines, all email senders must follow the rules listed below:

* Set up SPF or DKIM email authentication for your domain. If you use an email provider, verify that your provider supports it, ensuring that your messages are not marked as spam.
* Ensure that sending domains or IPs have valid forward and reverse DNS records, also referred to as PTR records.
* Keep spam rates reported in Postmaster Tools below 0.3%.
* Set up DMARC email authentication for your sending domain. Your DMARC enforcement policy can be set to none.
* For direct mail, the domain in the sender’s "From" header must be aligned with either the SPF domain or the DKIM domain. This is required to pass DMARC alignment.
* [Enable one-click unsubscribe](doc:one-click-unsubscribe#set-up-list-unsubscribe-header) for subscribed messages as per the [RFC 8058](https://support.google.com/a/answer/81126?sjid=8891808360542719029-AP\&visit_id=638459311449008138-2006200939\&rd=1#subscriptions\&zippy=%2Crequirem) guidelines.

Bulk senders must implement one-click unsubscribe functionality in all commercial and promotional messages by June 1, 2024.

# Impact of Non-Compliance

Starting from February 2024, bulk senders failing to meet sender requirements will encounter temporary errors. These errors will be indicated by specific error codes, affecting a small portion of their non-compliant email traffic. This will assist senders in identifying email traffic that does not adhere to the guidelines, prompting them to address any issues causing non-compliance.

In April 2024, Google will commence rejecting a portion of non-compliant email traffic, gradually increasing the rejection rate over time. For instance, if 75% of a sender's traffic meets the requirements, Google will begin rejecting the remaining 25% of traffic that fails to comply.

# Set Up List Unsubscribe Header

Using the One-Click Unsubscribe feature, you can add a List Unsubscribe header, a hyperlink embedded in the header section of an email. Positioned adjacent to the From address at the top of email campaigns, this link allows recipients to easily opt out of further email communications. 

To set up the List Unsubscribe header:

1. Navigate to Settings > Channels > Email from the CleverTap dashboard.
2. Select *Advanced Setup* and toggle ON *One-click Unsubscribe*. 

<Image align="center" className="border" border={true} src="https://files.readme.io/e050e58-Enable_One-click_Unsubscribe.gif" />

3. Click **Enable** to confirm your action. The *One-click Unsubscribe enabled* message displays. 

<Image align="center" className="border" border={true} src="https://files.readme.io/a9e9da5-image.png" />

For recurring campaigns, the *Unsubscribe* link will be visible for the subsequent campaign runs.

> 📘 Note
>
> * The One-Click Unsubscribe feature is enabled by default. If you have a custom setup with your ESP, you can disable it if needed.
> * Once you toggle ON the *One-Click Unsubscribe* option, the LIST unsubscribe header will reflect in email campaigns for the subsequent campaign runs.

# Send Test Campaign

To ensure one-click unsubscribe URL is implemented successfully:

1. Create a test email campaign.

<Image alt="Sample Email Campaign" align="center" border={true} src="https://files.readme.io/3e8ae51-Sample_Email_Campaign.png">
  Sample Email Campaign
</Image>

2. Click **Preview & Test** to send a test campaign to any user profile or a Test profile.

   <Image alt="List Unsubscribe URL - Inbox Preview" align="center" border={true} src="https://files.readme.io/a8afce1-image.png">
     List Unsubscribe URL - Inbox Preview
   </Image>

   <Image alt="List Unsubscribe URL on Opening the Email Campaign " align="center" border={true} src="https://files.readme.io/529b2ff-image.png">
     List Unsubscribe Header on Opening the Email Campaign 
   </Image>

   When the user clicks on the *Unsubscribe* link, they are automatically removed from the specific subscription groups selected during the campaign creation process. This ensures that the user will not receive communications from those particular categories associated with the email they unsubscribed from going forward.

> 🚧 List Unsubscribe Header for Test Campaign
>
> When you send a test campaign using the *Preview & Test* option, clicking *Unsubscribe* does not actually unsubscribe the user although it shows the same message as that of an actual email campaign.

# FAQs

### Q. Why can't I find the Unsubscribe link in Gmail or Yahoo, despite seeing the list-unsubscribe and one-click unsubscribe headers in the original message or raw data?

A. Gmail and Yahoo ultimately decide whether to display the list unsubscribe or one-click unsubscribe header. In the case of new senders or senders with low sender reputation, this might result in the button not being displayed.

### Q. Do you check the message body for a one-click unsubscribe link when the List-unsubscribe: header is missing?

A. No. Google states that one-click unsubscribe should be implemented according to RFC 8058. As per RFC 8058 Email sender guidelines, you must add List Unsubscribe headers to outgoing promotional messages. Including a mailto link in the body of your messages does not meet Google's one-click unsubscribe requirement.

### Q. If I include an additional unsubscribe link in my message content, does it have to be a one-click unsubscribe link?

A. No. Google states that if the messages include a one-click unsubscribe using List Unsubscribe headers, as described in their Email sender guidelines, additional unsubscribe links in the message body are not required to be one-click. Any additional unsubscribe links in the message body can link to the specified web page.
