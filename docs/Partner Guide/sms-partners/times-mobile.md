---
title: Times Mobile
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

Times Mobile(part of Times Internet Limited) is a leading communication platform that empowers businesses to connect with their users through SMS channels. This document highlights the integration of CleverTap and Times Mobile, empowering businesses to elevate their SMS communication using Times Mobile's infrastructure.

CleverTap's integration with Times Mobile facilitates sending bulk SMS campaigns, receiving real-time delivery updates, and automating personalized texts for your sales and marketing engagement using Times Internet's auto-scalable infrastructure.

For any queries or further assistance, contact [support@timesmobile.in](mailto:support@timesmobile.in).

# Prerequisities for Integration

Before you begin with integration, ensure you have:

* A CleverTap account with SMS setup enabled.
* A Times Mobile SMS account with respective SMS Push API details.
* The DLT-approved information, including templates and headers, if your account region is in India.

# Times Mobile Setup

This process involves the following three significant steps:

1. [Configure Times Mobile dashboard](doc:times-internet#configure-times-internet-dashboard).
2. [Add Times Mobile details to CleverTap dashboard](doc:times-internet#configure-clevertap-dashboard).
3. [Send a test SMS](doc:times-internet#configure-clevertap-dashboard).

## Configure Times Mobile Dashboard

Configuring the Times Mobile dashboard involves the following steps: obtaining SMS Push API credentials and setting up the CleverTap DLR Callback webhook.

To configure the Times Mobile dashboard:

1. Log in to the Times Mobile Dashboard using your credentials.

   <Image align="center" className="border" border={true} src="https://files.readme.io/ce13378-Times_Internet_.png" />
2. Navigate to *Sender ID Management* > *Request Sender* and click **Request For Sender** to request a new sender ID. 
3. Enter the following DLT-approved header details: **Sender Name**, **Account Type** (either trans or pro), and  **DLT Principal Entity Id**. **Sender Name** should be six characters or digits as per your account type.

<Image alt="Configure Sender IDs " align="center" width="100%" border={true} src="https://files.readme.io/8dae093-Times_Internet_Request_Sender.png" />  Configure Sender IDs
4. After adding the header details, click  **Create Sender Request** to create the sender request.
5. Navigate to *Bulk SMS* > *HTTP* from the Times Mobile dashboard to access your SMS Push API credentials. These credentials are required for configuration within the CleverTap platform. CleverTap recommends keeping these credentials handy before configuring them on the CleverTap dashboard.

<Image alt="Configure CleverTap DLR Callback Webhook" align="center" border={true} src="https://files.readme.io/3d80859-SMS_Push_Credentials-_Times_internet.png" />  Obtain SMS Push API Credentials











6. Click **Username** > **Profile** from the Times Mobile Dashboard. 
7. Under the **Delivery Report Post Back URL** section, configure the CleverTap DLR Callback Webhook for real-time SMS delivery updates. For more information, refer to the callback URL column in the [Configure CleverTap Dashboard ](doc:times-internet#configure-clevertap-dashboard) section.

<Image alt="Obtain SMS Push API Credentials" align="center" border={true} src="https://files.readme.io/a12ee6f-Times_Internet-_Delivery_Report_Post_Back_URL.png" />  Configure CleverTap DLR Callback Webhook











If you encounter any issues while configuring, contact [support@timesmobile.in](mailto:support@timesmobile.in) for further assistance.

## Configure CleverTap Dashboard

To add Times Mobile details on the CleverTap dashboard:

1. From the CleverTap Dashboard, navigate to *Settings* > *Engage* > *Channels* > *SMS*.
2. Click **+Add Provider**. The *Add SMS Provider* page opens. 

<Image alt="Add SMS Provider" align="center" width="90% " border={true} src="https://files.readme.io/090cf81-SMS_Add_Provider.png" />  Add SMS Provider











3. Select the *Setup* tab and enter the following details:
<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        *Provider*
      </td>

      <td>
        Select *Other(Generic)* from the dropdown list.
      </td>
    </tr>

    <tr>
      <td>
        * *Nickname*
      </td>

      <td>
        Uniquely identifies the provider.
      </td>
    </tr>

    <tr>
      <td>
        * *Callback URL*
      </td>

      <td>
        Enter the callback URL with Times Mobile to post or update the Message Delivery Status to CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        *Request Type*
      </td>

      <td>
        Select *GET* or *POST* based on the HTTP endpoint.
      </td>
    </tr>

    <tr>
      <td>
        *HTTP Endpoint*
      </td>

      <td>
        Enter the Times Mobile SMS Push endpoint along with its respective credentials.
      </td>
    </tr>

    <tr>
      <td>
        *Authentication*
      </td>

      <td>
        Select from the following authentication types:  

        <li> No Authentication_ : For GET_  endpoint, select this option.</li><li>_Basic Authentication_ : For _POST_ endpoint, select this option. Also, provide Times Mobile API _Username_ and _Password_ details.</li><li>_OAuth 2.0_: Enter client URL, client ID, secret key, and key-value pairs (optional).</li>
      </td>
    </tr>

    <tr>
      <td>
        *Parameters*
      </td>

      <td>
        Select *x-www-form-unlenencoded* or *JSON* for *Type* column.\
        For the *POST* endpoint, select *JSON* and enter the JSON payload structure. This field appears when you select *POST* in the *Request Type* column.\
        POST endpoint: `https://bsms.timesapi.in/ct/api/v1/message`\
        For more information, refer to the following:  

        <li> [Get endpoint](https://bsms.timesapi.in/ct/api/v1/send?username=%3Capiusername%3E&password=%3Capipassword%3E&unicode=false&from=%3Csenderid%3E&to=$$To&text=$$Body&dltContentId=$$TemplateID&corelationid=$$MessageID)</li>
        <li> [Post endpoint](https://bsms.timesapi.in/ct/api/v1/message)</li>
        <li> [Sample Payload](doc:times-internet#set-up-message-payload)</li>
      </td>
    </tr>

    <tr>
      <td>
        *Headers*
      </td>

      <td>
        For the *POST* endpoint, enter the following key-value pairs:  

        1. *Key*: Content-Type | *Value*: application/JSON  
        2. *Key*: Accept | *Value*: application/JSON
      </td>
    </tr>

    <tr>
      <td>
        *Custom Key-value pairs in campaign*
      </td>

      <td>
        Select this option to pass custom key-value pairs when sending your campaigns.
      </td>
    </tr>

    <tr>
      <td>
        *Mark this as default*
      </td>

      <td>
        Select *Mark this as default* to make this SMS provider the default provider to send the SMS.
      </td>
    </tr>
  </tbody>
</Table>
**\*The fields marked with asterisk mark (\*) are mandatory fields.**

<Image alt="Add Times Internet as an SMS Provider" align="center" width="70%" border={true} src="https://files.readme.io/7946b37-Times_Internet_Provider.png" />  Add Times Mobile as an SMS Provider

4. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful, send a test SMS as follows:

1. Click the *Send Test SMS* option before creating SMS campaigns and journeys.
2. Enter the following details:

   * *Country Code* and *Mobile Number*: Enter the country code and mobile number you want to send the message to.
   * *Message*: This is a test message.

   <Image alt="Send a Test SMS" align="center" width="75%" border={true} src="https://files.readme.io/8543b05-Send_a_Test_SMS_.png" caption="Send a Test SMS" />

3. Click **Send Test** to send the test campaign.

# Times Mobile Callbacks

In the default setup, Times Mobile sends the information to CleverTap's callback URL as follows:

1. CleverTap generates the callback that customers need to set up on the Times Mobile dashboard. 
2. TimesInternet sends the callback directly to CleverTap on the default URL.
3. CleverTap processes the callback.

Upon receiving callbacks from Times Mobile, the comprehensive stats are displayed on the CleverTap dashboard. For more information, refer to the [Stats](doc:times-internet#stats) section. 

## Set Up Message Payload

This section provides information about the sample request payload sent to SMS providers.

# Stats

CleverTap displays comprehensive stats such as Errors, Delivered, Clicked, and CTRs upon receiving callbacks from Times Mobile. After setting up the provider on the CleverTap dashboard, you can view these statistics from the following pages on the CleverTap dashboard:

* For [SMS Stats](https://docs.clevertap.com/docs/sms-stats), select the *Stats* tab of the Campaigns.
* For [Provider Stats](https://docs.clevertap.com/docs/sms-provider-operations), select the *Stats* tab under *Provider* setup. 

# Troubleshooting
If you encounter issues when sending test messages or saving the configuration, check that the Times Mobile endpoint and parameters are correctly added. Endpoints are case-sensitive. If the issue persists, raise a support ticket with the CleverTap team to obtain error codes. Once you have the error codes, connect with the  [Times Mobile Support](mailto:support@timesmobile.in) team.

# Frequently Asked Questions (FAQs)

Explore the FAQs for comprehensive insights and answers to common queries.

### Where can I check DLT guidelines for sending service/promotional SMS?

A. You can check the DLT guidelines for sending service/promotional SMS [here](https://docs.timesmobile.in/cpaas/DLT.pdf).

### What are DLT-approved SMS templates, and what is the approval process?

A. You can find more details about DLT-approved SMS Templates [here](https://docs.timesmobile.in/cpaas/DLT.pdf).

### What is a DLT-approved Header/Sender ID, and how do you get it approved?

A. You can find more details about DLT-approved Header/Sender ID [here](https://docs.timesmobile.in/cpaas/DLT.pdf).