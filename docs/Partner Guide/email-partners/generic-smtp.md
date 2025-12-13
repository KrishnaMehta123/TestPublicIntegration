---
title: Generic SMTP
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
## Overview

While we highly recommend using a reputable email service provider (ESP) such as Amazon SES, Postmark, or SendGrid. You can also integrate any other SMTP gateway to send emails.

# Set Up Email Provider

This process involves the following three major steps:

1. [Set Up CleverTap dashboard](https://docs.clevertap.com/docs/generic-smtp#set-up-clevertap-dashboard).
2. [Handle Bounces](https://docs.clevertap.com/docs/generic-smtp#handle-bounces).
3. [Handle Unsubscriptions](https://docs.clevertap.com/docs/generic-smtp#handle-unsubscriptions).

## Set Up CleverTap Dashboard

To set up the CleverTap dashboard:

1. Navigate to _Settings_ > _Email_ from the dashboard and click **+ Provider**.
2. Select _SMTP_ from the _Provider_ dropdown.
3. Enter the following details:

| Field                 | Description                                                                                                              |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| Host                  | In the _Host_ text box, fill your publicly accessible IP address or hostname of your SMTP server                         |
| Port                  | In the _Port_ text box, fill in your SMTP port.                                                                          |
| Username and Password | _Username_ and _Password_ values must be your SMTP credentials needed to connect to the service.                         |
| From Address          | _From Address_ value is the sender’s email address. Most people will not open an email unless they recognize the sender. |

4. Click **Save** to save your settings.
5. Click **Send a test email**. You will receive an email in your inbox after the setup is complete. If you do not receive the email, refer to [Troubleshooting](https://docs.clevertap.com/docs/generic-smtp#troubleshooting).

## Handle Bounces

When a recipient’s email server rejects an email, it is called a bounce. There are two types of bounces: 

- Soft Bounces: Soft bounces typically indicate a temporary delivery issue to an address. Some reasons for a soft bounce could be that the recipient’s mailbox is full or the Mail Server is down. Soft bounces are included in the campaign reports; the users are not marked unsubscribed.
- Hard Bounces: A hard bounce indicates a permanent reason an email cannot be delivered. Hard bounces are included in the campaign reports; the users are marked as unsubscribed. 

To handle bounced email messages, you need to make an HTTP request to the callback URL specified under _Dashboard_ > _Settings_ > _Integration_ > _Email_ > _Setup provider tab_ > _Nickname_.

Ensure that the request is be of type HTTP POST with the payload in the following format:

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

## Handle Unsubscriptions

To share unsubscription data from custom pages directly, you need to make an HTTP request to the callback URL that is specified in _Dashboard_ > _Settings_ >  _Channels_ > _Email_ > _Setup_ tab. Ensure that the request is of type HTTP POST with the payload in the following format.

```json
// if you're not sure of the time of the unsubscribe, just set it to the current epoch

[
    {
        "event": "unsubscribe",
        "data": [
            {
                "e": "email1@emailprovider.com",  // email id of the user
                "ts": 1504632929                  // time of the unsubscribe
            },
            {
                "e": "email2@emailprovider2.com", // email id of the user
                "ts": 1500630929                  // time of the unsubscribe
            }
        ]
    }
]
```

For more information about handling unsubscription requests from users, refer to [Handling Unsubscribes](doc:handling-unsubscribes).

# Troubleshooting

- As you are using your SMTP gateway, some email providers, such as Gmail and Yahoo, might not deliver the email to your inbox.
- Check if you have set up DKIM and SPF correctly.
- Check if Spamhaus has blacklisted your IP/domain.

> 🚧 Unsubscription Link
> 
> The unsubscription link does not work for test emails sent from the notification creation page.

# Errors

The following table lists the errors that you may encounter after sending a campaign:

| Error                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| _SMTP invalid email ID_   | **Cause 1**: The _SMTP invalid email ID_ error occurs when the provided email address is not formatted correctly or does not exist. Typos or errors in the email address commonly cause this error. **Resolution**: Double-check the email address and ensure the email ID is valid to fix this error. **Cause 2**: This error can also occur if you are using a test email address. **Resolution**: We recommend using an actual email address. Contact your ESP's customer support for further assistance if the issue persists.                                                                                                                                        |
| _SMTP dispatching failed_ | **Cause**: The _SMTP dispatching failed_ error occurs when the email message cannot be delivered to the recipient's email address.Some of the other common causes could be:<ul> <li>The email address that you are trying to send to is incorrect.</li> <li>The email address's domain is invalid.</li> <li>The recipient's ESP blocks your IP address.</li> <li>The ESP is experiencing a temporary outage.</li> </ul>**Resolution**: To fix this error, you can check the recipient's email address and ensure that the email address is valid and that the email infrastructure is working correctly. If the issue persists, contact your provider's customer support. |
| _SMTP connection error_   | ** Cause**: The _SMTP connection error_ occurs when CleverTap is unable to establish a connection with your ESP's SMTP server.Some of the other common causes could be:<ul> <li>Incorrect server details such as the server's hostname, port, or credentials. You can check the server details you have entered to confirm they are correct. </li> <li>Network issue that prevents the application from connecting to the SMTP server. It could be a temporary issue on your ESP's end.</li> </ul>**Resolution**: Contact your provider's customer support for further assistance if the issue persists.                                                                  |
| _SMTP timeout_            | **Cause**: The _SMTP timeout_ error occurs when CleverTap cannot connect with your ESP's SMTP server, or the connection takes longer than expected. Some of the other common causes could be:<ul> <li>The email-sending process has taken longer than the allocated time frame for connection establishment or completion.</li> <li>The SMTP server of your ESP is experiencing high traffic. </li> <li>Your sending IP has been flagged as a source of spam.</li> <li>There is an issue with your ESP's infrastructure.</li> </ul>**Resolution**: Contact your provider's customer support for further assistance if the issue persists.                                 |