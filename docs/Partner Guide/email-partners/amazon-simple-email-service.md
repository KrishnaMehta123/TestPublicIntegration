---
title: Amazon Simple Email Service
excerpt: Learn how to integrate Amazon SES as an Email provider on CleverTap.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
CleverTap supports sending emails through _Amazon SES_.

# Integrating Amazon SES with CleverTap

To integrate Amazon SES with CleverTap, follow the steps below:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_> Email
2. Click **+Provider**
3. Select _Amazon SES_ from the provider dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb0eaed-small-Amazon_SES.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


4. Paste the _Server Name_ and _Port_  from your Amazon SES account. Navigate to _Amazon SES_ > _Dashboard_ > _SMTP Settings_ to locate these credentials.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/234ce8d-small-CleverTap_Amazon_SES_Integration.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. _Username_ and _Password_ values should match your SMTP credentials from _Amazon SES_. These are not your AWS account credentials.
6. _From Address_ should have one of the values from _Amazon SES_ > _Dashboard_ > _Verified Senders_ > _Email addresses list_. Most people will not open an email unless they recognize the sender. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24dbaf5-small-amazon_ses_.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


7. Click **Save**
8. Click **Send a test email** and fill in your details to test the configuration details you entered. If you are not able to successfully test the email, refer to the troubleshooting steps below.

# Enabling Bounce and Complaint Processing

When an email is classified as bounced, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered a good practice and helps improve sender reputation.

To enable support for bounce processing, follow the steps below:

1. Navigate to _Amazon SNS_.
2. Create a _Topic_.
3. Select the _Topic_ and navigate to _Actions_ > _Subscribe to Topic_.
4. Select _HTTPS_ as the _Protocol_.
5. As the _Endpoint_ value, add the _Callback URL_ as shown in your CleverTap _Email_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7d933a-Callback_URL_v1_CLEVER-4714.png",
        "Enter email provider credentials to enable bounce and complaint processing.",
        1900
      ],
      "align": "center",
      "border": true,
      "caption": "Email Provider Credentials"
    }
  ]
}
[/block]


6. Save your settings by clicking on **Create Subscription**.
7. Navigate to _Amazon SES_.
8. Select the _Email Address_ you had previously added to the CleverTap Dashboard.
9. Click on _View Details_.
10. Click on _Notifications_ > _Edit Configuration_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5ae062-AWS_Domains_Notifications__v1_-_CLEVER-4714.png",
        "Configure Amazon SES for email bounces, complaints and deliveries.",
        2862
      ],
      "align": "center",
      "border": true,
      "caption": "Email Configurations"
    }
  ]
}
[/block]


11. Under _SNS Topic Configuration_, select the topics you created earlier such as _Bounces_, _Complaints_, and _Deliveries_ by clicking on the **Include original headers** checkboxes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc1da78-Edit_Notification_Configuration.png",
        "Edit Notification Configuration",
        2785
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Notification Configuration"
    }
  ]
}
[/block]


12. Save the configuration.

# Handling Unsubscribe Requests

To handle unsubscribed requests from users, refer to the steps in [Handling Unsubscribes](doc:handling-unsubscribes).

# Troubleshooting

The following explains some troubleshooting scenarios: 

- Sandbox mode: If you’re getting an _Invalid Credentials_ message when saving your settings, it could be that your _Amazon SES_ account is a sandboxed one. You need a valid production-ready _Amazon SES_ account to save your credentials. 
- Spam: Check your _Spam_ folder to see if the message has been classified as _Spam_ by your email provider.
- Email rendering: If your email does not render properly, check the subject line for newline characters or too many additional spaces. _Amazon SES_ email converts data from UTF-8 format to a 7-bit ASCII format before sending it out. The next line characters or additional spaces may interfere with this conversion.

## Dispatch Failed Error

The Dispatch Failed Error occurs in the following situations:

- Email credentials are incorrectly passed, making it impossible to establish a connection with the Email Service Provider.
- When the payload is sent from CleverTap's end to the Email Service Provider, and CleverTaps does not receive a "200 OK" response from their end, resulting in the error.

This error typically happens when the Email Service Provider is unable to handle the concurrent limit with which we make an SMTP connection.

If the selected credentials and configurations are correct, the error may occur due to intermittent unavailability of the service provider, causing the endpoint to be unavailable and resulting in the "SMTP Dispatch Failed" error.  
To resolve this error, we recommend contacting the Email Service Provider for assistance.