---
title: Exotel
excerpt: >-
  Learn how to integrate Exotel SMS capabilities with CleverTap to send
  personalized messages, automate sales and marketing engagements through
  ISO-certified secure SMS pipes.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Introduction

CleverTap users can now leverage the SMS capabilities of [Exotel](https://exotel.com/) to communicate with their customers for the following seamlessly:

* Sending just in time offers to customers to drive purchases
* Gathering feedback on the services 
* Keeping customers informed and more

In addition, businesses can automate sales and marketing engagements by sending personalized texts through ISO-certified secure SMS pipes.

# Prerequisites for Integration

The following are the prerequisites:

* You must have an account with SMS permissions from Exotel.
* You must have a CleverTap account with SMS setup enabled.
* You must have DLT-approved templates if the region of your account is in India. 

# Integrate Exotel with CleverTap

This process involves the following four steps:

1. [Configure Exotel Dashboard](doc:exotel#configure-exotel-dashboard)
2. [Find Exotel Details](doc:exotel#find-exotel-details)
3. [Configure CleverTap Dashboard](doc:exotel#configure-clevertap-dashboard)
4. [Send a Test SMS](doc:exotel#send-a-test-sms)

## Configure Exotel Dashboard

Per the DLT mandate, you must upload the following details to the **Settings** page of your Exotel Account to send an SMS:

* **Entity ID**: It is the unique ID provided to every business.
* **Sender ID**: The six-digit ID from which the SMS is sent.
* **Template ID**: It is the unique ID for each transactional or promotional SMS that you want to use.
* **Template Details**: These are the DLT-approved templates for the messages you want to send to your customers. You need to upload it to the Exotel dashboard. 
* **SMS Type**: It is used to classify different types of messages that you want to send to your customers. The following are the options available: transactional, service explicit, service implicit, and promotional.  

> 📘 Exotel Support
>
> For more information and queries pertaining to Exotel, visit [Exotel Support Center](https://support.exotel.com/a/solutions/articles/3000114660).

## Find Exotel Details

We recommend that you keep the following information handy before starting with configuration on the CleverTap dashboard:

* **Account sid and API Credentials**: To obtain this information, navigate to the [**API** > **API Settings**](https://my.exotel.com/Exotel/apisettings/site#api-credentials) page from the Exotel dashboard.

<Image title="Find Exotel account SID and API credentials" alt={2874} align="center" border={true} src="https://files.readme.io/e388cc6-API_Settings_page.png" />

* **Sender ID**: To obtain this information, navigate to [**Settings** > **Sender ID**](https://my.exotel.com/Exotel/settings/site#dltentity-settings) from the Exotel dashboard. 

<Image title="Find Exotel sender ID" alt={2868} align="center" border={true} src="https://files.readme.io/bfee62e-Sender_ID.png" />

* **Entity ID**: To obtain this information, navigate to [**Settings** > **SMS DLT Settings**](https://my.exotel.com/Exotel/settings/site#dltentity-settings). 

<Image title="Find Exotel entity ID " alt={2506} align="center" border={true} src="https://files.readme.io/22a84cd-SMS_DLT_Settings.png" />

* **DLT Template ID**: To obtain this information, navigate to [**Settings** > **SMS Templates**](https://my.exotel.com/Exotel/settings/site#dltentity-settings).

<Image title="Find Exotel DLT Template ID" alt={2876} align="center" border={true} src="https://files.readme.io/81c6ec8-SMS_Templates.png" />

## Configure CleverTap Dashboard:

To configure the CleverTap dashboard:

1. Navigate to **Settings** > **Engage** > **Channels** > **SMS** from the CleverTap dashboard.
2. Click **+ Add Provider**. The **Add SMS provider** screen displays.

<Image title="Add SMS provider credentials in CleverTap dashboard" alt={884} align="center" border={true} src="https://files.readme.io/c48e134-Add_Provider.png" />

3. Enter the following details:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Provider</td>
      <td>Select **Exotel** from the dropdown list.</td>
    </tr>
    <tr>
      <td>Nickname</td>
      <td>Enter the nickname for the SMS Provider to uniquely identify it.</td>
    </tr>
    <tr>
      <td>Callback URL</td>
      <td>Enter the URL where status callbacks must be posted after the SMS is sent.</td>
    </tr>
    <tr>
      <td>Account SID</td>
      <td>Enter your account identifier. For more information, refer to **Step 2**.</td>
    </tr>
    <tr>
      <td>API Key</td>
      <td>Enter API Key (Username) obtained in the [Find Exotel Details](https://docs.clevertap.com/docs/exotel#find-exotel-details) step.</td>
    </tr>
    <tr>
      <td>API Token</td>
      <td>Enter API Token (Password) obtained in the [Find Exotel Details](https://docs.clevertap.com/docs/exotel#find-exotel-details) step.</td>
    </tr>
    <tr>
      <td>Region</td>
      <td>
        - Select the **Region** of your Exotel account from the dropdown list.<br/>
        - For any queries, contact [Exotel Support Team](https://support.exotel.com/a/solutions/articles/3000114660).<br/>
        - The following are the available options:<br/>
          - Singapore: `api.exotel.com`. This is the default value.<br/>
          - Mumbai: `api.in.exotel.com`
      </td>
    </tr>
    <tr>
      <td>From/Sender ID</td>
      <td>
        - It is the ID from which the SMS is sent.<br/>
        - The format of this field is as follows: `<VN>/<SenderID>` where<br/>
          - `<VN>` is the Exotel Virtual Number/ExoPhone through which you send the SMS.
      </td>
    </tr>
    <tr>
      <td>SMS Type</td>
      <td>
        - Select the **None** from the dropdown if you have uploaded your templates on the Exotel dashboard.<br/>
        - It is used to skip template addition on Exotel Dashboard and configure SMS type based on the template registered on DLT in India.<br/>
        - The following are the options available:<br/>
          - None<br/>
          - **transactional**: Indicates that SMS consists of OTP or Service Implicit content.<br/>
          - **transactional_opt_in**: Indicates that the SMS consists of Service Explicit content.<br/>
          - **promotional**: Indicates that the SMS consists of Promotional content with a numeric header.<br/>
        - Default value for this field is None.<br/>
        - If not set or incorrectly passed, Exotel will look up if the content matches Templates added on Exotel for fetching SMS Type and DLT details.
      </td>
    </tr>
    <tr>
      <td>DLT Entity ID</td>
      <td>
        - Indicates the Content Template ID against the SMS body registered with Distributed Ledger Technology (DLT) portal of operators in India.<br/>
        - It is optional if you configure it on the Exotel dashboard. If not configured, enter the DLT-approved Entity ID for your legal entity here.<br/>
        - It is applicable only for SMS sent by Indian businesses to Indian destination numbers.
      </td>
    </tr>
    <tr>
      <td>Template ID</td>
      <td>
        - It is optional if you configure it on the Exotel dashboard. Enter the DLT-approved Template ID for your legal entity if not configured.<br/>
        - It is applicable only for SMS sent by Indian businesses to Indian destination numbers.
      </td>
    </tr>
  </tbody>
</Table>

4. Select the **Template ID** checkbox. 
5. Select the **Mark this as default** checkbox to make this SMS provider the default provider to send the SMS.
6. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful:

1. Click the **Send Test SMS** hyperlink before you start creating SMS campaigns and journeys.
2. Enter the following details: 
   * **Country Code and Mobile number**: Enter the country code and mobile number to which you want to send the message. 
   * **Message**: This is a test message powered by Exotel.

<Image title="Send a test SMS" alt={2232} align="center" width="80%" border={true} src="https://files.readme.io/476dbd6-Send_test_SMS.png" />

# Create Campaigns and Journeys

Now that your integration is successful, you can now create [SMS campaigns](doc:create-message-sms) and [journeys](https://docs.clevertap.com/docs/journeys).

# Troubleshooting

## Failed to send out test notifications

**Issue**  
The following error displays when saving Exotel credentials in the CleverTap dashboard

<Image title="Test notifications failed" alt={1536} align="center" border={true} src="https://files.readme.io/91f1ae3-Screenshot_2022-05-25_at_1.07.22_PM.png" />

**Resolution**  
The following are the steps to resolve the issue:

1. [Find your Exotel Credentials](doc:exotel#find-exotel-details). Ensure that the keys are added correctly as they are case-sensitive.
2. Raise the [CleverTap Support Request](https://help.clevertap.com/hc/en-us/requests/new?ticket_form_id=4416487002257) to get the error code if the issue persists.
3. Connect with the Exotel support team to get this resolved after you receive the error code from the CleverTap support team.

> 📘 Encoding
>
> The messages sent out from CleverTap are encoded in the UTF-8 charset.

# FAQs

**1. How can I check DLT guidelines for sending commercial SMS?**  
Ans: For information on TRAI regulations and DLT registration, refer to [TRAI Regulations on Commercial Communications (DLT portal) - SMS in India](https://support.exotel.com/support/solutions/articles/3000096504-trai-regulations-on-commercial-communications-dlt-portal-sms-in-india).

**2. What is an SMS template, and how to get it approved?**  
Ans: To know more about SMS templates, refer to [What is an SMS template and how can I get a template approved?](https://support.exotel.com/support/solutions/articles/38686-what-is-an-sms-template-and-how-can-i-get-a-template-approved-)

**3. How do I check Exotel Account settings?**  
Ans: To check Exotel Account Settings, refer to [How to choose an SMS sender ID?](https://support.exotel.com/support/solutions/articles/126794-how-to-choose-an-sms-sender-id-)

**4. How to choose an SMS Sender ID, and what is its significance?**  
Ans: To understand this, refer to [How to choose an SMS sender ID?](https://support.exotel.com/support/solutions/articles/126794-how-to-choose-an-sms-sender-id-)

**5. How to check the delivery status of SMS sent by me?**  
Ans: To know more about delivery status, refer to [How do I find the delivery status of the SMS I sent using Exotel API?](https://support.exotel.com/support/solutions/articles/48518-how-do-i-find-the-delivery-status-of-the-sms-i-sent-using-exotel-api-)

**6. We are seeing an Exotel API error under Campaign. What is the error about?**  
Ans: Exotel API Error is raised under two circumstances. Firstly, when we try to send a message to Exotel, they do not accept it due to some error. Secondly, when Exotel replies with the error code to CleverTap. For more information on this, refer to [Error Codes](https://developer.exotel.com/api/sms#send-sms).