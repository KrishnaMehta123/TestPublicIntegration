---
title: Sendgrid
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
CleverTap supports sending emails through SendGrid. 

# Integrate SendGrid with CleverTap

1. In the dashboard, navigate to Settings > Engage > Channels > Email. 
2. Click the + Provider button. The Provider credentials page appears.
3. Select SendGrid from the provider list.
4. Provide a nickname for your integration.
5. Enter the SendGrid API key. For more information on generating the key, see [Creating an API key in SendGrid](https://sendgrid.com/docs/ui/account-and-settings/api-keys/#creating-an-api-key).
   > 🚧 Note
   >
   > As of December 2020, SendGrid only requires an API key for authentication. Username and password are no longer needed.
   >
   > For any clarifications, contact your SendGrid Account Executive or SendGrid Support.
6. From Address – This value is used as the sender's email address. Most people will not open an email unless they recognize the sender.
7. Reply Address - This value is used as the reply address. You can receive replies to this address.
8. Save your settings.
9. Finally, click Send a test email and fill in your details to test the configuration details you entered. Has it arrived in your inbox? If not, see the troubleshooting steps below.

> 🚧 Note
>
> If you are using SendGrid credentials with SMTP integration, then enter **apikey** as username and \<API\_KEY\_VALUE> as password.

# Set Up Email Delivery Status Callbacks

Emails sent to users can be bounced or rejected, and delivered emails may end up in spam or be marked as unsubscribed by users. To maintain a strong sender reputation, CleverTap must be notified to prevent further deliveries to such mailboxes. 

To set up callbacks for **Spam, Bounced, Dropped,** and **Unsubscribed** emails, follow these steps:

To enable support for these, follow the steps:

1. Navigate to *Settings* > *Email* Settings and enable Event Notification.

2. Navigate to Settings from within Event Notification.

3. In the HTTP Post URL input box, add the *Callback URL* from the CleverTap dashboard, which is found under *Settings* > *Email* > *Provider* > *Sendgrid*.

   <Image alt="Add Callback URL" align="center" border={true} src="https://files.readme.io/39730b0-SendGrid_Email_Provider.png">
     Add Callback URL
   </Image>

4. Check the following from the *Deliverability Data* and *Engagement Data* in the SendGrid Dashboard: Dropped, Bounced, Unsubscribed From, and  Marked as Spam.

5. Save your settings.

<Image title="Enable event notifications for emails via SendGrid" alt={669} align="center" border={true} src="https://files.readme.io/c7c968d-Email_Sendgrid_Settings.png">
  Enable Event Notifications for Emails via SendGrid
</Image>

> 📘 Handling Inactive Email Addresses
>
> * When an email bounces, drops, or the user unsubscribes, CleverTap marks the user’s email address as inactive.
> * The count of email bounces is shown on the email report screen.

# Troubleshooting

Check your SPAM folder to see if the message has been classified as SPAM by your email provider.
