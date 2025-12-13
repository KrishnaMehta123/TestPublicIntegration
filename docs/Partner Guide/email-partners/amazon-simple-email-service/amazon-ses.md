---
title: Amazon Simple Email Service
excerpt: Email Partner
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
[Amazon Simple Email Service (SES)](https://aws.amazon.com/ses/), a cloud-based email service provider, allows you to deliver high-volume email campaigns and manage incoming emails at scale. 

> 📘 Important Update
>
> The new Amazon SES configuration will use HTTP as the default protocol for integration, offering faster and more efficient performance compared to SMTP. If you are an existing customer with email campaigns running on SMTP, you can switch to HTTP by entering their Access Key ID, Secret Access Key, and Server Name (HTTP) on the *Settings* page of the CleverTap dashboard. For more information about this, refer to [Migrate Existing Amazon SES Provider Setup to HTTP](doc:amazon-ses#switch-existing-amazon-ses-provider-setup-to-http) .
>
> This is currently released in Private Beta.

# Integrate Amazon SES with CleverTap

To integrate Amazon SES with CleverTap:

1. From the CleverTap dashboard, go to *Settings* and click **Integrate Email**.
2. Select *Amazon SES* as a provider.

   <Image alt="Select Email Provider" align="center" border={true} src="https://files.readme.io/bb0eaed-small-Amazon_SES.png">
     Select Email Provider
   </Image>
3. Enter the endpoint in the *Server Name* field. To identify the endpoint, refer to [Service API Endpoints](https://docs.aws.amazon.com/general/latest/gr/ses.html#ses_region).
4. Enter the *Access Key ID* and *Secret Access Key*. To obtain this:

   1. Select the user name in the navigation bar on your AWS dashboard.
   2. Select *Security credentials* from the list.

      <Image alt="Select Security Credentials" align="center" border={true} src="https://files.readme.io/5ee1a345e2378ab76fb4cc9359ccb434abad83c6dc3f3862267d9df7bd1b535a-Select_Security_Credentials_from_the_List_.png">
        Select Security Credentials
      </Image>
   3. Scroll down to the *Access Key* section under the *AWS IAM credentials* tab and click **Create access key**.

      <Image alt="Click Create Access Key" align="center" border={true} src="https://files.readme.io/7d11367e8d3980379ef08220b73e292759593f4797c314cc0ed9531174c2d480-Create_Access_Key_.png">
        Click Create Access Key
      </Image>
   4. Select *Third-party service* and click **Next**.

      <Image alt="Select Access Key Best Practices and Alternatives" align="center" border={true} src="https://files.readme.io/9b905167b4d735dc4051140213d43b7f17a00a2c9b473dd8d790c4186c124000-Access_Best_Practices.png">
        Select Access Key Best Practices and Alternatives
      </Image>
   5. Enter *Description tag value* and click **Create access key**. You can copy *Access Key ID* and *Secret Access Key* or download the .csv file.

      <Image alt="Retrieve Access Keys" align="center" border={true} src="https://files.readme.io/8878385a6681a522f45563997e481a6fd1b319f60a0846898314bf881f12587a-Acess_Key_Created.png">
        Retrieve Access Keys
      </Image>
5. Copy the **Access Key ID** and **Secret Access Key** from the newly created access key and paste them into the corresponding fields on the CleverTap dashboard.
6. Enter the *From Address*. You can enter your preferred email address from Verified email addresses listed under *Configuration* > *Identities* on the Amazon SES dashboard.

<Image alt="Enter Verified Email Address Under From Address" align="center" border={true} src="https://files.readme.io/48507825c8509ec50bb4c9d8a34f36758387ae2de32bc89739bf08d77f8f4895-Select_Verified_Email_Under_From_Address.png">
  Enter Verified Email Address Under From Address
</Image>

7. Click **Save** to save the settings.
8. Click **Send a test email** and fill in your details to test the configuration details you entered. If you encounter any issues, refer to [Troubleshooting](doc:amazon-ses#troubleshooting).

## Switch Existing Amazon SES Provider Setup to HTTP

If you already have set up Amazon SES configuration under *Settings* > *Channels*> *Email* earlier using SMTP credentials, you can switch to *HTTP* to send subsequent email campaigns from the *Settings* page on the CleverTap dashboard. To do so, you must edit the current Amazon SES provider setup:

1. From the CleverTap dashboard, go to *Settings* > *Channels*> *Email*.
2. Click the existing Amazon SES Provider from the *Providers* tab.
3. Repeat *Step 4*, *6*, and *7* of [Integrate Amazon SES with CleverTap](doc:amazon-ses#integrate-amazon-ses-with-clevertap).

> 📘 Note
>
> You must add Access Key ID, Secret Access Key and update the server name to the HTTP server name.

# Enabling Bounce and Complaint Processing

When an email is classified as bounced, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered a good practice and helps improve your sender reputation.

To enable support for bounce processing, follow the steps below:

1. Navigate to *Amazon SNS*.
2. Create a *Topic*.
3. Select the *Topic* and navigate to *Actions* > *Subscribe to Topic*.
4. Select *HTTPS* as the *Protocol*.
5. As the *Endpoint* value, add the *Callback URL* as shown in your CleverTap *Email* page.

<Image title="Enter email provider credentials to enable bounce and complaint processing." alt={1900} align="center" border={true} src="https://files.readme.io/b7d933a-Callback_URL_v1_CLEVER-4714.png">
  Email Provider Credentials
</Image>

6. Save your settings by clicking on **Create Subscription**.
7. Navigate to *Amazon SES*.
8. Select the *Email Address* you had previously added to the CleverTap Dashboard.
9. Click on *View Details*.
10. Click on *Notifications* > *Edit Configuration*.

<Image title="Configure Amazon SES for email bounces, complaints and deliveries." alt={2862} align="center" border={true} src="https://files.readme.io/e5ae062-AWS_Domains_Notifications__v1_-_CLEVER-4714.png">
  Email Configurations
</Image>

11. Under *SNS Topic Configuration*, select the topics you created earlier such as *Bounces*, *Complaints*, and *Deliveries* by clicking on the **Include original headers** checkboxes.

<Image title="Edit Notification Configuration" alt={2785} align="center" src="https://files.readme.io/cc1da78-Edit_Notification_Configuration.png">
  Edit Notification Configuration
</Image>

12. Save the configuration.

# Handling Unsubscribe Requests

To handle unsubscribed user requests, refer to the steps listed under [Handling Unsubscribes](doc:handling-unsubscribes).

# Troubleshooting

This section outlines some troubleshooting scenarios and their solutions: 

* *Sandbox mode*: If you are getting an *Invalid Credentials* message when saving your settings, it could be that your *Amazon SES* account is a sandboxed one. You need a valid production-ready *Amazon SES* account to save your credentials. 
* *Spam*: Check your *Spam* folder to see if the message has been classified as *Spam* by your email provider.
* *Email rendering*: If your email does not render properly, check the subject line for new line characters or too many additional spaces. *Amazon SES* email converts data from UTF-8 format to a 7-bit ASCII format before sending it out. The new line characters or additional spaces may interfere with this conversion.
