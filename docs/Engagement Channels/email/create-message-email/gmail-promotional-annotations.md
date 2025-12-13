---
title: Gmail Promotional Annotations
excerpt: >-
  Understand how to put the most valuable parts of email right at people's
  fingertips.
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

[Gmail Promotional Annotations](https://developers.google.com/gmail/promotab/) enables you to highlight your email on the Gmail Promotions tab. Your email can include additional information, such as promotion codes, a featured image, and deal expiration dates. This information is visible to your email subscribers before opening the email. It is an excellent way to excite your users to open your message by setting it apart from other emails in the user's inbox. CleverTap provides you with a no-code way to annotate your email messages. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6fd6c27-Annotated_Email.png",
        "Annotated Email Promotion",
        990
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Email with Deal Annotation"
    }
  ]
}
[/block]


# Create A Deal Annotation

Follow the steps listed below to annotate emails in an email campaign:

1. [Create an email campaign](https://docs.clevertap.com/docs/create-message-email). 
2. [Define the message content](https://docs.clevertap.com/docs/create-message-email#define-the-message-content) from the Email Editor. 
3. Click **Sender details**. 
4. To annotate your email, select **Highlight with Gmail promotional annotations **. The following options display:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0d538da-Gmail_Promotional_Annotation_.png",
        "Highlight the Gmail Promotional Annotations",
        1136
      ],
      "align": "center",
      "border": true,
      "caption": "Annotate Emails"
    }
  ]
}
[/block]


5. Add the required information. 

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "h-2": "Best Practices",
    "0-0": "Sender name",
    "0-1": "Add your business name.",
    "0-2": "This field is populated automatically using the _From_ part of the _Sender Details_.",
    "1-0": "Subject line",
    "1-1": "Add a unique and relevant subject line for the inbox. We recommend a 44-character limit for optimal rendering.",
    "1-2": "This field is populated automatically using the _Subject_ part of the _Sender Details_. This alternative subject will only be displayed if the discount code or sale badges are also displayed. For example, if the original subject was _20% Off Sale Ends Today_ and the offer badge is _20% Off_, add a subject line that says **Sale Ends Today** to avoid duplication.",
    "2-0": "Company logo",
    "2-1": "Upload an image or add a URL. Check that the URL is https (not http).",
    "2-2": "Ensure that you use an https (not http) URL. This logo selection only shows in the email preview. To add your organization’s logo to outgoing email messages sent from your organization, the logo must adhere to the Brand Indicators for Message Identification (BIMI) standard. For more information, refer to the [Add a brand logo to email with BIMI](https://support.google.com/a/answer/10911320?hl=en) article.",
    "3-0": "Discount offer",
    "3-1": "Highlight any offerings such as _20% off_ or _Free Shipping_. We recommend a 20-character limit for optimal rendering.",
    "3-2": "Avoid using more than four words or full sentences in this space, as it competes with your subject line. When your email text space is full, the offer title truncates (for example, \"...\").<ul> <li> <p>Do not repurpose. Use promotional offerings to ensure clarity and simplicity. Do not utilize it for other actions like <em>Open now</em>.</p> </li> <li> <p>Do not use run-on sentences. Avoid saying things such as <em>25% off unless you’ve already purchased from us in which case other ...</em> Long sentences are truncated.</p> </li> </ul>",
    "4-0": "Offer code",
    "4-1": "Add the promo code. We recommend a 20-character limit for optimal rendering.",
    "4-2": "Only use a discount code if it is featured in the email. Do not repurpose this space, as it always says _Code_ before the text.",
    "5-0": "Offer period",
    "5-1": "Select the offer date range.",
    "5-2": "Using this feature allows an email to be previewed twice at the top in a bundle:<ul> <li>once when it is first sent.</li> <li>again within three days of the offer expiry.</li> </ul>When personalizing _Offer period_, specify the time and timezone. For example, _2018-12-30T23:59:59-0700_."
  },
  "cols": 3,
  "rows": 6,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


6. Click **Preview & Test** to preview the annotated email message.

> 📘 Supported Inboxes
> 
> The Gmail app for iOS, Android, and desktop supports highlighting emails with promotional annotations.

# Test Annotation

Create a unique Gmail testing account ending with [promotabtesting@gmail.com](mailto:promotabtesting@gmail.com) for your team. For example, [_mycompany.promotabtesting@gmail.com_](mailto:_mycompany.promotabtesting@gmail.com_.). This unique account will have a more aggressive email ranking and bundling to make testing easier and faster.

# Troubleshooting

Before troubleshooting a problem, check your account-level settings in your Gmail app. Check that you have enabled the following settings to test the latest experiences in the Gmail promotions tab. These are the default settings: 

- Images: Always show.
- Conversation view: On.
- Enable Bundling of Top Email: On.

The following sections discuss common issues encountered when attempting to test:

### Not seeing email bundles at all.

- Check that the device has the latest version of the Gmail app. Then, refresh your email under the _Promotions_ tab.
- Try restarting your device.
- If the issue is still unresolved, try viewing the bundle on another device. For example, a tablet may have a different Gmail version and show the bundle differently.

> 📘 Email is held up
> 
> There is a chance your email could be in a holdback group. If none of the measures worked, create a new account ending with [_promotabtesting@gmail.com_.](mailto:_promotabtesting@gmail.com_.) For example, create [_mycompanypromotabtesting@gmail.com_](mailto:_mycompanypromotabtesting@gmail.com_) and use that new account for testing.

### Cannot see your brand's annotated email in a bundle.

- Check if the email is on the Gmail Promotions tab.
- Annotated emails are currently not available for Gmail for Business accounts. Ensure that you are testing on your personal Gmail address.
- Check that the email was not opened or sent on the previous day.
- An email does not populate in a bundle on another device after viewing it on one device. You must send a new test email to preview.
- Create multiple testing accounts if you want to visualize on multiple devices. One of your team members might open the email, thus making it unavailable in the bundle for the rest of the team.
- Check that the annotation is not past the expiration date.
- Check that you are using the latest version of the Gmail app. Try viewing it on another device. For example, a tablet may have a different version of the Gmail app and show email differently.
- Refresh the Gmail app by pulling down the Gmail Promotions tab screen.
- Check that you are not using sensitive categories in the Gmail Promotions tab. For example, adult content or debt collection.

### Email does not show up on the _Promotions_ tab.

Use the following measures:

- Check if the marketing email was sent from the usual subdomain. Sending from less recognized subdomains can confuse the Gmail tab classifier and prevent an email from being placed on the Promotions tab.
- Check that your account has no email filters that send email to the primary tab because annotations are only visible on the Promotions tab.
- Send from different sender subdomains to ensure the email lands under the correct tab. For more information about the Gmail classifier, refer to [Bulk Senders Guidelines](https://support.google.com/mail/answer/81126).
- If you use a [_promotabtesting@gmail.com_](mailto:_promotabtesting@gmail.com_) account, the first email does not appear on the Promotions tab. Drag the email onto the Promotions tab, and send an email from the same sender address, with a different subject line, to the testing account.

### The email bundle is visible on one device but not another.

- Check that you are viewing from the same email account.
- If the email is opened on one device first, the ranking of the bundle may be changed on another device.

# Frequently Asked Questions (FAQs)

This section describes the FAQs for Deal Annotations.

### Why can I not see my brand's annotated email despite following all the steps?

Annotated emails are currently not available for Gmail for Business accounts. Ensure that you are testing on your personal Gmail address.