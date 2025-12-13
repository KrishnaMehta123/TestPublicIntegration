---
title: Brand Indicators for Message Identification
excerpt: Learn how to stand out in the inbox with BIMI
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

Brand Indicators for Message Identification (BIMI) is an emerging email standard that enables brands to display their logos in supported email clients, reinforcing brand trust. By implementing BIMI, your brand’s logo appears alongside your emails in compatible inboxes, serving as a visual indicator of authenticity. This helps recipients quickly verify that an email is from a legitimate source, reducing the risk of phishing and spam.

While [SPF](doc:email-sender-authentication#sender-policy-framework-spf), [DKIM](doc:email-sender-authentication#domainkeys-identified-mail-dkim), and [DMARC](doc:email-sender-authentication#domain-based-message-authentication-reporting-and-conformance-dmarc) are the three pillars of email authentication, BIMI is a standard that provides a visual indicator to help recipients identify legitimate messages.

<Image alt="BIMI" align="center" border={true} src="https://files.readme.io/526f9a8d8db4ac2a57ad99c3a3de3ea4ec5bdb2e9e528669a91d5ef483052b77-BIMI-2.png">
  Boost Email Trust with BIMI
</Image>

# How BIMI Works

BIMI relies on existing email authentication protocols ([SPF, DKIM, and DMARC](https://docs.clevertap.com/docs/email-sender-authentication)) and a DNS TXT record  

A Domain Name System (DNS) TXT record is a type of DNS record that allows domain owners to store text-based information. It is commonly used for verification and authentication purposes, including email security measures such as SPF, DKIM, DMARC, and BIMI.

For BIMI, a TXT record in the sender’s DNS contains details about the brand logo, allowing email services to retrieve and display it when the email is authenticated.

<Image alt="BIMI Process" align="center" border={true} src="https://files.readme.io/cab582af917efc5fb44e086245ac6bce7419a0cf10bd5eea0139768d25589650-BIMI-process.png">
  BIMI Process
</Image>

To display a brand logo using BIMI, the email must pass authentication checks and meet BIMI requirements. The following steps outline how BIMI works.

1. When an email is delivered, the recipient’s email service checks for SPF, DKIM, and DMARC compliance.
2. If authentication is successful, the email service retrieves the BIMI TXT record from the sender’s DNS.
3. The BIMI record specifies the logo URL, typically an SVG file. A Verified Mark Certificate (VMC) may also be required.
4. If the email provider supports BIMI and all criteria are met, the logo is displayed in the recipient’s inbox alongside the email.

# Prerequisites for BIMI

To display your brand logo in supported inboxes, ensure that your emails are properly authenticated. First, configure [SPF, DKIM, and DMARC](doc:email-sender-authentication).  

> 📘 CleverTap Email Authentication
>
> * If you have the Advanced Email add-on, SPF and DKIM are configured during the email onboarding.  
> * For accounts with Advanced Email add-on onboarded after February 2024, DMARC is also configured as part of the setup.

Before setting up BIMI, ensure the following requirements are met:  

* **Authenticate all outgoing emails**  
  * Emails must pass DMARC validation checks.  
  * The DMARC policy for both the [RFC5322.From domain](https://datatracker.ietf.org/doc/html/draft-ietf-dmarc-dmarcbis-28#name-use-of-rfc5322from) and the Organizational Domain (if different) must be set to:  `p=quarantine` with `pct=100` or  `p=reject`  

* **Publish a BIMI record in your domain’s DNS**  
  * The record must point to a brand logo in SVG format.  
  * A Verified Mark Certificate (VMC) is required for email providers that mandate it.  

> 📘 BIMI Setup and Support
>
> BIMI setup occurs outside the CleverTap platform. CleverTap does not provide direct support for its configuration. You must work with your domain host or a BIMI service provider to complete the implementation. For additional guidance, refer to [BIMI Group’s FAQ](https://bimigroup.org/faqs-for-senders-esps).

# BIMI Impact on Email Deliverability

While BIMI does not directly impact email deliverability, it can have an indirect positive effect:

* **Increased Engagement**: By enhancing brand recognition and trust, BIMI encourages recipients to engage with your emails.
* **Improved Sender Reputation**: Higher engagement signals to BIMI-supporting mailbox providers that your messages are wanted, reducing the likelihood of them being marked as spam. 

Additionally, as BIMI works alongside SPF, DKIM, and DMARC, to authenticate senders, its implementation can contribute to overall email deliverability improvements.
