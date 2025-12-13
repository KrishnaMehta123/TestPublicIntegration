---
title: Email Best Practices
excerpt: >-
  Learn how to maintain a positive sender’s reputation and comply with Anti-spam
  laws.
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

Inbox Service Providers (ISPs) consider user engagement a significant determinant of the sender's reputation. The sender's reputation is crucial for ensuring successful email delivery and reaching the recipients' inboxes. Positive engagement, such as email opens and clicks, can enhance your reputation. However, negative engagement, such as marking emails as spam, can negatively impact your reputation as a sender.

This guide aims to assist you in enabling a more positive user experience and a healthier sender reputation by using industry best practices listed in the sections to follow.

# Best Practices

The following are some of the best practices that help maintain a positive and healthier sender’s reputation:

## Compliance

Ensure that you strictly adhere to marketing email regulations, including [CAN-SPAM](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business) and [CASL](http://fightspam.gc.ca/eic/site/030.nsf/eng/home), as well as [GDPR](https://gdpr-info.eu/), wherever applicable, alongside any other relevant local anti-spam policies.

## Sending Volume

Inbox Providers continuously monitor your messages for 30 days, seeking out any unusual occurrences, such as sudden surges in email volume or extended periods of inactivity. To keep the email volume consistent, avoid a gap of more than 30 days between sending messages.

## Email Data Collection

When it comes to optimizing your email marketing strategy, it is crucial to follow the points listed below:

- Enhance your sign-up process by incorporating the double opt-in method. Double opt-in involves utilizing an email address collection approach that involves sending a verification email (via a third-party tool) to the provided user address. Upon clicking the verification link in the email, the user's subscription is confirmed, while non-clicked links result in remaining unsubscribed.
- Validate historical users before importing and targeting them with CleverTap. There are several excellent options available, such as [Clearout.io](doc:clearout), [NeverBounce](https://neverbounce.com/), [ZeroBounce](https://www.zerobounce.net/), [BriteVerify](http://www.briteverify.com/?pcode=leanplum), and [EmailOversight](https://www.emailoversight.com/).
- Ensure that users explicitly opt-in for promotional emails during their sign-up process. Automatic opt-ins should be avoided, allowing users to make their own choices.
- Avoid purchasing or renting lists of users who have not explicitly subscribed to receiving your emails. It is essential to focus on building an engaged and consent-based subscriber base.

## Audience Selection

The following are some of the key points to remember for effective Email targeting:

- Focus on users who have explicitly opted-in to receive promotional emails and have shown engagement by opening or interacting with an email within the last six months. It is important to consider different risk levels based on engagement duration, with low risk for 0-3 months, medium risk for 4-5 months, and high risk for over six months. Remember that less engaged users are more likely to exhibit negative engagement behavior.
- During sign-up, set clear expectations for users regarding the type and frequency of promotions they will receive. Maintain a consistent sending cadence to establish reliability and avoid overwhelming users.
- Avoid targeting users with email addresses obtained from affiliate vendors or purchased lists, as these users have not explicitly opted-in. Instead, prioritize building a consent-based subscriber base.
- When introducing a new segment, gradually increase the sending volume according to [CleverTap's warm-up schedule](doc:ip-warmup). Where applicable, leverage the _Best Time_ feature to send emails when users are most likely to engage.
- [Implement a sunset policy](doc:email-sunsetting) by targeting users who have been inactive for over six months in small batches. Aim for an engaged vs. inactive user ratio of 80% to 20% on any given day. Periodically send win-back campaigns to non-engaged users, but if they do not respond, permanently exclude them from preserving your sending reputation and ensuring engaged users receive your campaigns effectively.

## Email Campaign Content

The following are some key tips for optimizing your email campaign messages:

- Use your CleverTap provisioned sending domain in the From address to maintain a consistent and reputable sender identity.
- Avoid using no-reply email addresses not designed to receive incoming emails. While they work well for transactional emails, such as confirmations or password resets, it's best to avoid them for promotional emails to subscribers.
- Tailor your subject lines, preheaders, and content to be relevant to each target segment of users.
- Make your emails easy to skim by organizing them, allowing readers to absorb information quickly.
- Consider conducting A/B tests when necessary to experiment with different elements and optimize your email performance.
- Personalize your emails to increase engagement, as users are more likely to respond to messages that feel tailored to them.
- Always include an unsubscribe link or your custom Unsubscribe tag in all promotional emails to comply with regulations and respect user preferences. Also, asking the user's reason for unsubscription is a good practice to gather feedback and improve your mailing strategy.
- Ensure that you are adhering to styling guidelines, such as:
  - Including a compelling call-to-action (CTA), 
  - Placing the primary CTA within the top 20% part of the email, 
  - Keeping the email size under 102kb
  - Maintaining a text-to-image ratio of 70% text to 30% image for marketing purposes
  - Adding ALT text and titles for images, ensuring clean HTML formatting, 
  - Checking for typos, verifying that links work correctly, using emojis sparingly, and avoiding excessive use of all caps or exclamation points in the subject.

Following these recommendations can optimize your email campaigns for better engagement and results.

## Images

The following are the key points to remember when using images in emails:

### Dimensions and image quality

Most email clients have a preview pane of 600 - 800 pixels maximum width. To support high-resolution (retina) displays, you must resize images 2x the desired display size.

### Image file size

More than 50% of emails are opened on mobile devices. Although it is recommended to use 2x (retina) images, increased image size may affect email load time and the subscriber's mobile data plan, resulting in a less-than-friendly user experience. The optimal total image data weight must be less than 1 MB.

### Image file format

The three most widely accepted file formats are as follows:

- The .JPGs files are the most compressed in terms of file size and, therefore, are the most suitable for photographs. 
- .PNG has a higher quality and can have a transparent background. However, greater quality leads to increased file size. Therefore, .PNG is recommended for smaller images that require greater color capacity, such as logos.
- .GIF allows animated loops but is the most limited in terms of colors. These color limits, however, help file size to remain small. .GIF format is mostly used for animated memes to convey a message in creative ways. 
- .SVG is also a popular image file format. However, it is not supported by Gmail and other popular email clients. Do not use SVGs in emails unless you are sure your subscribers' email clients support this file format.

### Alt Text

Alt Text is the text that appears if your image does not load. It also improves the accessibility of your email. Ensure to use Alt Text with images to avoid empty image placeholders. In general, it is recommended to create emails assuming that email clients block images or that some images might fail to load.

## Campaign Results Analysis

Examine engagement metrics within 12-24 hours after each email campaign and make necessary adjustments to targeting, content, and mailing frequency for future communications.