---
title: Gmail/Google Apps
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
You can use the SMTP integration if you want to use your existing Gmail or Google Apps account to send emails.

# Gmail Settings

You need to generate an App password with Google. To do so:

1. Activate the 2-Step Verification process.
2. Visit the *App passwords* page, follow the steps listed here, and save your generated password.

# Integrate Gmail into CleverTap

1. From the dashboard, navigate to *Settings* > *Channels* > *Email*.
2. Click **+Provider**.
3. Select *SMTP* from the *Provider* dropdown and *SMTPS* from the *Scheme* dropdown.
4. Enter the *Host* value as **smtp.gmail.com**.
5. Enter the *Port* value as **465**.
6. *Username* and *Password* must be your email address and the App password you generated, respectively.
7. Enter the sender's email address in the *From Address* field.
8. Click **Save**.

You can send a test email by clicking **Send Test Email**.

# Understand Bounces

When a recipient's email server rejects an email, it is called a bounce.\
There are two kinds of bounces:

* **Soft Bounces**: Soft bounces typically indicate a temporary delivery issue to an address. Some reasons for a soft bounce could be that the recipient's mailbox is full or the mail server is down. Campaign reports include soft bounces and do not mark the users as unsubscribed.
* **Hard Bounces**: A hard bounce indicates a permanent reason an email cannot be delivered. Campaign reports include hard bounces and mark the users as unsubscribed.

## Processing Bounces

To process bounced email messages, you need to make an HTTP request to the *Callback URL* specified in *Dashboard* > *Settings* > *Channel* > *Email* > *+Provider*.

The request must be of the type HTTP POST with the payload in the following format:

```json
// if you're not sure of the time of the bounce, just set it to the current epoch
[
    {
        "event": "softbounce",
        "data": [
            {
                "e": "email1@emailprovider.com",  // email id that soft bounced
                "ts": 1435322805                  // time of the bounce
            },
            {
                "e": "email2@emailprovider2.com", // email id that soft bounced
                "ts": 1435322805                  // time of the bounce
            }
        ]
    },
    {
        "event": "hardbounce",
        "data": [
            {
                "e": "email3@emailprovider.com",   // email id that hard bounced
                "ts": 1435322805
            }
        ]
    }
]
```

# Handling Unsubscriptions

To handle unsubscription requests from users, you can follow the steps mentioned [here](doc:handling-unsubscribes).
