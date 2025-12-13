---
title: Email Seed Testing
excerpt: >-
  Send your email campaign to a seed list for accurate Inbox vs Spam placement
  insights.
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

Seed Testing for inbox placement involves sending emails to a predetermined list of email addresses representing various email providers and devices. Marketers gain insights into the effectiveness of their email delivery strategies by monitoring where test emails land within recipients' inboxes (primary, promotions, spam). This helps identify potential improvements needed for optimal inbox placement. 

Measuring campaign performance and checking IP/domain reputation through free sources like Google Postmaster, Microsoft SNDS, and block lists can provide some insight into email delivery. However, the only way to measure Inbox placement accurately is through seed testing, which third-party companies offer.

<Image alt="Email Seed Listing" align="center" border={true} src="https://files.readme.io/256bf41-Email_Seed_Listing.png">
  Email Seed Listing
</Image>

# Seed List

Seed accounts are dummy email addresses established across various Inbox Service Providers (ISPs). These accounts, managed by popular service providers like [Validity](https://www.validity.com/products/returnpath/features/), [Email on Acid](https://www.emailonacid.com/help-article/how-to-run-a-spam-test-via-seed-list/), [Litmus](https://help.litmus.com/article/137-perform-a-spam-test), and [InboxMonster](https://app.inboxmonster.com/), are created and used solely to measure inbox placement. 

## Upload Seed List to CleverTap

To send an email to a seed list, you must upload the list to CleverTap. You can import users via [CSV Upload](https://docs.clevertap.com/docs/csv-upload#:~:text=To%20upload%20user%20profiles%3A,Settings%20%3E%20Engage%20%3E%20CSV%20Uploads.) or [API Upload](https://developer.clevertap.com/docs/upload-user-profiles-api). 

When uploading the seed list file to CleverTap:

* **Include Email Address and Identity**: Each entry in the file must contain an email address and an identity field. This helps to uniquely identify the users on the CleverTap dashboard.
* **Add Custom Property**: You can optionally include an additional custom property to further distinguish seed list users from regular users. This property can be any relevant identifier or attribute that aids segmentation and targeting.

Once the upload is complete, you must target the list separately before deploying the campaign. This is to avoid skewing the metrics, as these accounts do not engage.

# Benefits of Seed Testing

The following are the benefits of Seed Testing:

* **Customization for Accuracy**: Customize the seed list to accurately reflect your user base. For example, if your user base does not extend to Russian or Chinese ISPs, you need not incorporate seeds from these providers. However, if your users are primarily in Europe, you must include seeds from popular local providers instead.
* **Pre-Campaign Testing**: Utilize seed testing to pre-test each campaign by targeting the seed list first. This proactive approach provides insights into campaign performance beforehand.
* **ISP Acceptance Speed**: Seed testing also allows you to assess the speed at which your emails are accepted across various ISPs. This information aids in optimizing delivery strategies for faster acceptance rates.
* **Blockage Identification and Content Optimization**: Through seed testing, identify ISPs that may block your emails and determine which content and subject lines yield the best results. This helps refine email content and strategies for improved deliverability and engagement.

> 📘 Contact Support
>
> If you need support with the file upload process or with optimizing inbox placement, contact [support@clevertap.com](mailto:support@clevertap.com).
