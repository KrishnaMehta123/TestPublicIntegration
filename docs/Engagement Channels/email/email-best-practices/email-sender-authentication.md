---
title: Email Sender Authentication
excerpt: >-
  Discover the significance of Еmail sender authentication and learn about the
  different email authentication protocols - Sender Policy Framework (SPF),
  DomainKeys Identified Mail (DKIM), and Domain-based Message Authentication,
  Reporting, and Conformance (DMARC).
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

**Еmail sender authentication** is a process for inbox providers to verify that CleverTap is authorized to send emails on your behalf. Proper sender authentication is mandatory for successfully delivering your emails to all inbox providers (for example, Gmail, Yahoo, MSN, and so on). It helps distinguish between legitimate senders, such as those sending transaction updates or promotional offers, and potential spammers or scammers attempting to overwhelm users' inboxes with unsolicited or malicious emails. Inbox providers utilize email authentication protocols to achieve verified sender identity when emails arrive at their receiving mail servers. 

To set up sender authentication, you must incorporate a set of Domain Name System (DNS) records into your domain’s hosting service. A DNS translates or resolves a hostname (for example, [www.clevertap.com](https://clevertap.com/)) into a compiler-specific language (for example, an IP address). These DNS records associate your sending domain with CleverTap. Consequently, when an inbox provider processes your email, they refer to your domain instead of CleverTap's Email Service Provider (ESP - Sendgrid). 

# Authentication Record Protocols

Email authenticators such as [Sender Policy Framework (SPF)](doc:email-sender-authentication#sender-policy-framework-spf), [DomainKeys Identified Mail (DKIM)](doc:email-sender-authentication#domainkeys-identified-mail-dkim), and [Domain-based Message Authentication, Reporting, and Conformance (DMARC)](doc:email-sender-authentication#domain-based-message-authentication-reporting-and-conformance-dmarc) are essential protocols for verifying email authenticity and preventing spoofing and phishing attacks. 

When an email is sent by an ESP (Email Service Provider) such as SendGrid:

1. The recipient's email server checks if the sender's domain has published SPF records specifying which servers can send emails on its behalf.
2. The ESP signs the email with a private key associated with the sender's domain and publishes a public key in DNS. The recipient's server verifies this signature.
3. DMARC policies instruct the recipient's server on how to handle SPF and DKIM results, ensuring emails are authenticated and handled according to specified policies.

<Image alt="Email Sender Authentication Records" align="center" border={true} src="https://files.readme.io/c6fd258-image.png">
  Email Sender Authentication Records 
</Image>

> 👍 Compliance
>
> As of February 2024, Gmail and  Yahoo have enforced new sending requirements, which require email marketing senders with volumes greater than 5,000 a day to have a valid SPF, DKIM, and DMARC record.

## Sender Policy Framework (SPF)

SPF is an open standard to prevent sender address forgery. It validates that the IP address used to send an email is authorized to send messages on behalf of the domain listed in the email's Envelope From or Return. Without SPF or similar authentication records, a malicious actor can readily assume a sender's identity, deceiving the recipient into engaging in actions or disclosing information they would otherwise refrain from.

*In the postal mail analogy, you would contact the sender to verify if the postman can be trusted to deliver their letter.* Let's look at the following image to understand the flow of email authentication.

<Image alt="Sender Policy Framework (SPF) Authentication" align="center" border={true} src="https://files.readme.io/aa36f08-DMARC_FINAL.png">
  Sender Policy Framework (SPF) Authentication
</Image>

## DomainKeys Identified Mail (DKIM)

DKIM is a validation method to help Internet Service Providers (ISPs) detect and prevent malicious email delivery. DKIM uses public-key cryptography to sign email message headers - optionally, the message body may also be signed. This signature allows receiving email servers to determine whether a domain owner sent a message and whether the message was altered in transit.

*In the postal mail analogy, this implies that the envelope has a stamped seal that proves that the letter inside was not altered by anyone who could have had access to the envelope, and the stamp can be verified to be from the sender on the envelope. This can be different from the sender mentioned in the letter.*

<Image alt="DKIM Authentication" align="center" border={true} src="https://files.readme.io/41ff156-DKIM_FINAL.png">
  DKIM Authentication
</Image>

## Domain-based Message Authentication, Reporting, and Conformance (DMARC)

DMARC is an additional layer above SPF and DKIM. It validates SPF and DKIM outcomes and verifies if the Header From domain aligns with those used in the SPF and DKIM checks. The *Header From* address represents the sender's email address and is visible to recipients in their email clients.

<Image alt="DMARC Authentication" align="center" border={true} src="https://files.readme.io/f9ba461-SPF_FINAL.png">
  DMARC Authentication
</Image>

When SPF and DKIM validations fail or are incongruent with the *Header From* address, the recipient server must adhere to the DMARC policy. This can involve actions such as quarantining (p=quarantine), rejecting (p=reject), or disregarding the results and delivering the email (p=none) (refer to the following image).

<Image alt="Email Authentication Process with DMARC " align="center" border={true} src="https://files.readme.io/5de4461-image.png">
  Email Authentication Process with DMARC 
</Image>

Visualize your email server as a vigilant individual managing your incoming messages. Without SPF, DKIM, and DMARC implementation, this individual accepts envelopes from any source, opens them, and places the content on your desk without verification. Consequently, discerning the trustworthiness of the sender's identity becomes challenging. 

*For an analogy, if you work at a government office and require two ID proofs for someone to receive a document. If someone brings only one proof, or if someone’s ID fails in some way (such as the addresses on the IDs not matching), you would halt the process and either ask for additional information or refuse to hand over the document.*

For more details on DMARC, refer to [DMARC Resources ](https://dmarc.org/resources/) or [Google's Help Center](https://support.google.com/a/answer/2466563?hl=en\&ref_topic=2759254).

> 📘 Note
>
> For CleverTap customers with Advanced Email (an email-sending service integrated with CleverTap), SPF, DKIM, and, as of recently, DMARC is configured during Еmail onboarding with CleverTap.
