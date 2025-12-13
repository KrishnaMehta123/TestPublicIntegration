---
title: 'Email: Troubleshooting & FAQs'
excerpt: >-
  Refer to our frequently asked questions and troubleshoot any issues with your
  Email campaign.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
This section provides FAQs, troubleshooting help for your email setup, tips to raise your reputation from poor to good, and IP and domain monitoring. 

# FAQs

<details>

<summary>Email Builder Functionality</summary>

### Does linked content work in the email builder?

Yes. For more information, refer to [Linked Content](doc:personalize-message-email#linked-content).

### Does the recommendation feature work in the email builder?

Yes. For more information, refer to [Email Recommendations](doc:create-campaigns-using-recommendations#email-campaigns-with-recommendations).

### What does the _Do not stack on mobile devices_ mean?

Do not stack on mobile devices alerts you that it will disable the resizing and repositioning of the content per the device screen width. 

**With Stacking on Mobile**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ed477f-campaigns_email_Stack_images.png",
        "Email View with Stacking on Mobile",
        1080
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Email with Stacking on Mobile"
    }
  ]
}
[/block]


**Without Stacking on Mobile**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de9274d-campaigns_email_Not_Stack_images.png",
        "Email View without Stacking on Mobile",
        1080
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Email without Stacking on Mobile"
    }
  ]
}
[/block]


### How do you add a GIF file to an email?

You can add a GIF file using the content field image or custom HTML by following the steps below:

1. Select the _New Email with drag and drop_ template. 
2. From the _Content_ tab, click **Image**. 
3. Drag and drop the image icon in the email body. 
4. Click **Browse**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76f72c9-New_final_GIF_file_Browse.png",
        "Click Browse to Upload a GIF",
        1322
      ],
      "align": "center",
      "border": true,
      "caption": "Add a GIF"
    }
  ]
}
[/block]


4. Click **Upload** and select your GIF file.
5. In the _File manager_, find your GIF file and click **Insert**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6d322e-New_file_GIF_file_Upload.png",
        "Click Insert to Add the GIF",
        1318
      ],
      "align": "center",
      "border": true,
      "caption": "Insert a GIF"
    }
  ]
}
[/block]


> 📘 Note
> 
> - Images/GIFs must be less than 5 MB; however, we recommend the media must be less than 1 MB for optimal results. The media may not load in the user's inbox because all your users may not have a high-speed internet connection.
> - The media formats supported are JPEG, GIF, and MP4.

</details>

<details>

<summary>Email Sending and Configuration</summary>

### What IPs does CleverTap use to send out emails?

To view the IPs:

1. Navigate to _Settings_ > _Channels_ > _Email_ from the dashboard. 
2. In the _Providers_ tab, refer to the _Additional security_ note at the top highlighting the IPs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/213bdfe-Providers.png",
        "View CleverTap IPs for Sending Email",
        1422
      ],
      "align": "center",
      "border": true,
      "caption": "CleverTap IPs"
    }
  ]
}
[/block]


> 📘 Common IPs
> 
> These IPs are common for webhooks, SMS, and emails.

### How do you handle unsubscribes and bounce for callbacks, such as Mandrill or SendGrid?

CleverTap must be notified for any email classified as bounced, rejected, spam, or unsubscriptions by the user so that we do not attempt any further deliveries to their mailboxes.

For more information, refer to [SendGrid Bounces, Rejections, and Unsubscriptions](doc:sendgrid#section-step-2-bounces-rejections-and-unsubscriptions) and [Mandrill Bounces, Rejections, and Unsubscriptions](doc:mandrill#handle-bounce-rejection-spam-and-unsubscriptions).

A service provider tracks any user unsubscribes using the unsubscription link in your email. The service provider then sends this information to CleverTap through the callback URL. 

The communication preference for users is marked as false (MSG_Email=False).  
Hard-bounced and unsubscribed users both fall under unsubscription. Follow the steps below to find the number of users who have unsubscribed via email:

1. Navigate to _Segments_ > _Find People_. 
2. From the _Display_ common properties, select _Reachability_ > _Unsubscribed_ > _Yes_.

### What are the timeouts and retry limits for Email?

The following are the timeout and retry limits for Email:

| Channel            | Timeout (ConnectionRequest) | Retry Times |
| :----------------- | :-------------------------- | :---------- |
| Kenscio            | 5 Seconds                   | 0           |
| Email              | 15 Seconds                  | 2           |
| Sendgrid           | 10 Seconds                  | 0           |
| Mandrill           | Not applicable              | 0           |
| NetcoreCloud       | Not applicable              | 0           |
| PostMark           | 10 Seconds                  | 0           |
| Facebook           | Not applicable              | 5           |
| Amazon EventBridge | Not applicable              | 0           |
| mParticle          | Not applicable              | 0           |
| Segment            | Not applicable              | 0           |

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).

</details>

<details>

<summary>Email Customization</summary>

### How do you annotate an email?

Email annotations in the _Promotions_ tab bring email messages to life with images, deals, expiration dates, and more. The email annotation can be performed in the drag-and-drop email editor and also in the custom HTML email editor.

Use the <meta> tag in the drag-and-drop editor to annotate an email. Following is the sample code that can be used in the HTML block of the drag-and-drop editor:

```html
<p>
<div itemscope itemtype="http://schema.org/Organization">

<meta itemprop="logo" content="https://www.gstatic.com/images/branding/product/1x/googleg_48dp.png" />

</div>

<div itemscope itemtype="http://schema.org/DiscountOffer">

<meta itemprop="description" content="40% off" />

<meta itemprop="discountCode" content="DISCOUNTCODE" />

<meta itemprop="availabilityStarts" content="2020-03-20T08:00:00-07:00" />

<meta itemprop="availabilityEnds" content="2020-03-21T23:59:59-07:00" />

</div>

<div itemscope itemtype="http://schema.org/PromotionCard">

<meta itemprop="image" content="https://gmail-ads-markup-test.sandbox.google.com/sample.png" />

</div> This is metadata in HTML block of drag and drop editor</p>
```

For custom HTML implementation, refer to [Get started: How to annotate your email](https://developers.google.com/gmail/promotab/overview) in the Google documentation. The _Promotions_ tab capability works in custom HTML with both inline microdata and the script tag.

When you test this feature, check the following:

- The target audience email addresses are not GSuite emails.
- The availability start date must be far apart from the end date. If the values of the start date and end date are closer to the current date, then the mail is most likely to appear in the _Top Picks_ of the _Promotions_ tab.

### How do you add custom fonts in email?

You need the CleverTap custom HTML builder for your email campaigns.

You can add custom fonts to emails by adding a link tag to the header of your email HTML. It means the font must be hosted somewhere on the internet. Following is an example:

```html
<html>
<head>
    <link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet" type="text/css" />
</head>
<body>
<h1 style="font-family:'Roboto'">Test text</h1>
</body>
</html>
```

Custom fonts may not be supported by all email clients. If you are adding a custom font to emails, you may also want to specify fallback fonts. This ensures the latter font is picked up if the first font is unavailable. 

Following is an example:

```html
<h1 style="font-family: Lato, 'Lucida Grande', Tahoma, Sans-Serif;">Welcome</h1>
```

</details>

<details>

<summary>Email Unsubscribe and Metrics</summary>

### Why is my unsubscribe count lower than expected?

This is because the unsubscribe count is updated when a user unsubscribes from email communications overall and not to only specific subscription group(s). You can check the dashboard for users unsubscribed from specific subscription groups by searching for them on the [Find People](doc:find-people) page. Search for users by the _Channel Unsubscribed_ event and filter by event property _Group_.

</details>

<details>

<summary>Email Provider Integration</summary>

### Can I integrate an email provider that is not listed in documents?

Yes, you can use Generic SMTP to integrate any email provider of your choice. For more information, refer to [Generic SMTP](https://docs.clevertap.com/docs/generic-smtp).

</details>

# Troubleshooting

### 1. I received the error message: "Please set the email credentials." How do I fix it?

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e527565-Screen_Shot_2018-07-15_at_8.40.27_PM.png",
        "Error to Set the Email Credentials ",
        519
      ],
      "align": "center",
      "border": true,
      "caption": "Error Message"
    }
  ]
}
[/block]


This error message means you have not integrated your email provider with CleverTap. You can do this by following [this guide](doc:email-partners).

### 2. Raise your reputation from poor to good

Monitoring your domain health is an ongoing process that requires consistent nurturing. Your sending reputation is a decisive factor when it comes to the delivery of your emails. By complying with permission policies and best practices and carefully monitoring your email list performance, you will be well-positioned to develop and maintain a robust sending reputation.

Take the steps below to improve your domain and IP reputation.

### 3. Prime your IP for success

The job of ISP filters is to defend against spam emails. How do you tell these filters that your IP is valid and trustworthy? Start any email campaign by sending small batches of emails. Send these messages to email addresses that you know are engaged. As these emails are received and opened by engaged users, your IP will build trust with the ISP. Slowly increase the number of emails until you scale to your peak volume.

### 4. Create a new subdomain

We do not recommend everyone to create a new subdomain, but you may wish to create one if possible. Over time, users will come to trust the subdomain, which is an added benefit. The purpose is that this subdomain will allow for domain-specific monitoring of your IP reputation and succeed against some domain-based certification filters.

To add a new subdomain in SendGrid, perform the following steps:

1. Log in to your SendGrid account and navigate to the _Settings_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46f1e01-1_Settings.png",
        "SendGrid Settings",
        182
      ],
      "align": "center",
      "border": true,
      "caption": "Settings"
    }
  ]
}
[/block]


2. Click **Sender Authentication**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06c6adc-2_Sender_Authentication.png",
        "Click Sender Authentication",
        180
      ],
      "align": "center",
      "border": true,
      "caption": "Sender Authentication"
    }
  ]
}
[/block]


3. Click **Authenticate Your Domain** under _Domain Authentication_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/242cfc9-3_Authenticate_Your_Domain.png",
        "Authenticate Your Domain",
        424
      ],
      "align": "center",
      "border": true,
      "caption": "Domain Authentication"
    }
  ]
}
[/block]


4. Select the name of your DNS host provider.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ce2a25-4_name_of_your_DNS_host_provider.png",
        "Set Your DNS Host Provider Name",
        873
      ],
      "align": "center",
      "border": true,
      "caption": "Select DNS Host Provider"
    }
  ]
}
[/block]


5. In the second option on the same page, choose if you want the link branding or not and click **Next**.
6. Fill in the name of the domain/subdomain from which you wish to send your email campaigns. 
7. Select the _Use automated security_ option in the _Advanced Settings_ section and click **Next**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b395e61-5_Next.png",
        "Use Automated Security to Authenticate",
        502
      ],
      "align": "center",
      "border": true,
      "caption": "Advanced Settings"
    }
  ]
}
[/block]


8. The next screen will provide you the records which will be required to be updated on the DNS settings page of your domain host name provider.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3928608-6_records.png",
        "Verify DNS Records",
        1106
      ],
      "align": "center",
      "border": true,
      "caption": "Install DNS Records"
    }
  ]
}
[/block]


9. Once the provided records have been updated on the DNS settings page, click on the checkbox in the bottom right corner along with the option _I've added these records_ and click **Verify**.

This step will verify that the correct records are added to the domain DNS. Once the verification is complete, the added domain is listed on the _Sender Authentication_ page and is ready for use. If the verification fails, check if the records have been added to the DNS correctly and repeat the previous verification steps.