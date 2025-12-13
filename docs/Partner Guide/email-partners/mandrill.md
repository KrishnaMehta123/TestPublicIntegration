---
title: Mandrill
excerpt: Email Partner
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

[Mandrill](https://mailchimp.com/en-gb/features/email/), a paid Mailchimp add-on, allows you to send data-driven emails, including targeted e-commerce and personalized one-to-one messages. With this integration, you can send email campaigns from the CleverTap dashboard through Mandrill.

# Prerequisites for Integration

The following are the prerequisites:

* A Mandrill account with all the required setup and permissions to send email campaigns.
* A CleverTap account.

# Integrate Mandrill into CleverTap

This process involves the following two steps:

1. [Find Mandrill Project Details](doc:mandrill#find-mandrill-project-details).
2. [Configure Settings on CleverTap Dashboard](doc:mandrill#configure-settings-on-clevertap-dashboard).

## Find Mandrill Project Details

To find Mandrill project details:

1. Log in to your Mandrill account.
2. Navigate to the *Settings* page from the Mandrill dashboard.
3. Click *SMTP & API Info* to view the Mandrill project details.

<Image title="View SMS and API info for Mandrill project" alt={2836} align="center" border={true} src="https://files.readme.io/facb6bb-SMS__API_Info.png">
  SMS and API Details for Mandrill Project
</Image>

> 📘 Note
>
> Keep the following details handy, as you will need them to configure the CleverTap dashboard:       
>
> * Host
> * Port
> * API Key

## Configure Settings on CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Channels* > *Email* from the CleverTap dashboard.

<Image title="Configure email settings on CleverTap dashboard" alt={1422} align="center" border={true} src="https://files.readme.io/fe94349-Add_Email_Provider.png">
  Email Settings on CleverTap Dashboard
</Image>

2. Click **+ Provider**. The *Setup* page opens.
3. Enter the following Provider credentials:

| Field                       | Description                                                                                                                                                                                   |
| :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Provider                    | Select *Mandrill*.                                                                                                                                                                            |
| Nickname                    | Enter the *Nickname* to identify your saved provider uniquely.                                                                                                                                |
| Callback URL                | *Callback URL* is used to get the bounce, rejection, and subscription information from Mandrill to CleverTap. This is a read-only field that is auto-populated with CleverTap's callback URL. |
| Host                        | Enter the *Host* value as **smtp.mandrillapp.com**.                                                                                                                                           |
| Port                        | Enter the *Port* value as **587**.                                                                                                                                                            |
| Username                    | Enter your Mandrill username in this field.                                                                                                                                                   |
| API Key                     | Enter your Mandrill *API Key* obtained after *step 3* of [Find Mandrill Project Details](doc:mandrill#find-mandrill-project-details).                                                         |
| From Address                | Enter the *From* email address. This is the same as the sender's email address. Most people will not open an email unless they recognize the sender.                                          |
| Unsubscribe page (Optional) | Enter your custom *Unsubscribe page* URL.                                                                                                                                                     |

4. Click **Save** to save the provider settings.

<Image title="Setup email provider credentials" alt={1179} align="center" border={true} src="https://files.readme.io/1b89dca-Setup_Provider_Credentials.png">
  Setup Email Provider Credentials
</Image>

> 🚧 API Key Encryption
>
> CleverTap stores your credentials in an encrypted format. So, we recommend that you save the API Key somewhere. If you do not have this information, contact [Mandrill support](https://us1.admin.mailchimp.com/support/).

You can click **Send Test Email** and fill in your details to test the configuration details you have entered. Has it arrived in your inbox? If not, refer to [Troubleshooting](doc:mandrill#troubleshooting).

# Handle Bounce, Rejection, Spam, and Unsubscriptions

When an email is classified as bounced or rejected or when a user unsubscribes or marks a particular email ID as spam, CleverTap must be notified so that it does not attempt any further deliveries to that mailbox. This is considered a good practice and helps improve your sender's reputation. A good sender reputation virtually guarantees better delivery rates.

To obtain such information, you need to create a webhook. To do so:

1. Navigate to *Settings* > *Webhooks* from the Mandrill dashboard.
2. Click **Add a Webhook**.
3. Ensure to select the following from the available options: 
   * *Message Is Soft-Bounced*
   * *Message Recipient Unsubscribes*
   * *Message Is Bounced* 
   * *Message Is Marked As Spam*, and 
   * *Message is Rejected*.
4. Enter the CleverTap callback URL (from your CleverTap *Email Settings* section) in the *Post To URL* field.
5. Click **Create Webhook**.

<Image title="Create a Webhook" alt={2880} align="center" border={true} src="https://files.readme.io/9841d64-Create_Webhook.png">
  Create a Webhook
</Image>

## Enable Unsubscribe Footer

Mandrill provides a default email unsubscribe template, which gives the email recipient an option to unsubscribe from the email list. When you select this option, the unsubscribe template is added at the bottom of all the outgoing emails. 

Here is an example of the default unsubscribe footer of Mandrill:

<Image title="Sample unsubscribe message on footer" alt={1052} align="center" border={true} src="https://files.readme.io/6ab2a08-Unsubscribe_Footer.png">
  Sample Unsubscribe Message on Footer
</Image>

To enable adding the default Unsubscribe Footer:

1. Navigate to *Settings* > *Sending Defaults* from the Mandrill dashboard.
2. Select *Add Unsubscribe Footer*.
3. Click **Save**.

<Image title="Add default unsubscribe footer" alt={2709} align="center" border={true} src="https://files.readme.io/a5ab5c2-Sending_Defaults.png">
  Add Default Unsubscribe Footer
</Image>

# Troubleshooting

If you encounter an error when sending a test email, ensure the following:

* Check your SPAM folder to see if the message has been classified as SPAM by your email provider.
* IP address does not restrict your Mandrill API key.
* Your Mandrill API key is active.
