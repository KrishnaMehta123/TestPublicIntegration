---
title: Exotel
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
# Introduction

CleverTap users can now leverage the SMS capabilities of [Exotel](https://exotel.com/) to communicate with their customers for the following seamlessly:

- Sending just in time offers to customers to drive purchases
- Gathering feedback on the services 
- Keeping customers informed and more

In addition, businesses can automate sales and marketing engagements by sending personalized texts through ISO-certified secure SMS pipes.

# Prerequisites for Integration

The following are the prerequisites:

- You must have an account with SMS permissions from Exotel.
- You must have a CleverTap account with SMS setup enabled.
- You must have DLT-approved templates if the region of your account is in India. 

# Integrate Exotel with CleverTap

This process involves the following four steps:

1. [Configure Exotel Dashboard](doc:exotel#configure-exotel-dashboard)
2. [Find Exotel Details](doc:exotel#find-exotel-details)
3. [Configure CleverTap Dashboard](doc:exotel#configure-clevertap-dashboard)
4. [Send a Test SMS](doc:exotel#send-a-test-sms)

## Configure Exotel Dashboard

Per the DLT mandate, you must upload the following details to the _Settings_ page of your Exotel Account to send an SMS:

- **Entity ID**: It is the unique ID provided to every business.
- **Sender ID**: The six-digit ID from which the SMS is sent.
- **Template ID**: It is the unique ID for each transactional or promotional SMS that you want to use.
- **Template Details**: These are the DLT-approved templates for the messages you want to send to your customers. You need to upload it to the Exotel dashboard. 
- **SMS Type**: It is used to classify different types of messages that you want to send to your customers. The following are the options available: transactional, service explicit, service implicit, and promotional.  

> 📘 Exotel Support
> 
> For more information and queries pertaining to Exotel, visit [Exotel Support Center](https://support.exotel.com/a/solutions/articles/3000114660).

## Find Exotel Details

We recommend that you keep the following information handy before starting with configuration on the CleverTap dashboard:

- **Account sid and API Credentials**: To obtain this information, navigate to the [_API_ > _API Settings_](https://my.exotel.com/Exotel/apisettings/site#api-credentials) page from the Exotel dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e388cc6-API_Settings_page.png",
        "Find Exotel account SID and API credentials",
        2874
      ],
      "align": "center",
      "border": true,
      "caption": "Find Exotel Account SID and API Credentials"
    }
  ]
}
[/block]


- **Sender ID**: To obtain this information, navigate to [_Settings_ > _Sender ID_](https://my.exotel.com/Exotel/settings/site#dltentity-settings) from the Exotel dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bfee62e-Sender_ID.png",
        "Find Exotel sender ID",
        2868
      ],
      "align": "center",
      "border": true,
      "caption": "Find Exotel Sender ID"
    }
  ]
}
[/block]


- **Entity ID**: To obtain this information, navigate to [_Settings_ > _SMS DLT Settings_](https://my.exotel.com/Exotel/settings/site#dltentity-settings). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22a84cd-SMS_DLT_Settings.png",
        "Find Exotel entity ID ",
        2506
      ],
      "align": "center",
      "border": true,
      "caption": "Find Exotel Entity ID"
    }
  ]
}
[/block]


- **DLT Template ID**: To obtain this information, navigate to [_Settings_ > _SMS Templates_](https://my.exotel.com/Exotel/settings/site#dltentity-settings).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81c6ec8-SMS_Templates.png",
        "Find Exotel DLT Template ID",
        2876
      ],
      "align": "center",
      "border": true,
      "caption": "Find Exotel DLT Template ID"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard:

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Engage_ > _Channels_ > _SMS_ from the CleverTap dashboard.
2. Click **+ Add Provider**. The _Add SMS provider_ screen displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c48e134-Add_Provider.png",
        "Add SMS provider credentials in CleverTap dashboard",
        884
      ],
      "align": "center",
      "border": true,
      "caption": "Add SMS Provider Credentials in CleverTap Dashboard"
    }
  ]
}
[/block]


3. Enter the following details:

| <p>Field</p>          | <p>Description</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :-------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Provider</p>       | <p>Select <em>Exotel</em> from the dropdown list.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <p>Nickname</p>       | <p>Enter the nickname for the SMS Provider to uniquely identify it.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <p>Callback URL</p>   | <p>Enter the URL where status callbacks must be posted after the SMS is sent.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <p>Account SID</p>    | <p>Enter your account identifier. For more information, refer to <em>Step 2</em>.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <p>API Key</p>        | <p>Enter API Key (Username) obtained in the <a href="https://docs.clevertap.com/docs/exotel#find-exotel-details">Find Exotel Details</a> step.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <p>API Token</p>      | <p>Enter API Token (Password) obtained in the <a href="https://docs.clevertap.com/docs/exotel#find-exotel-details">Find Exotel Details</a> step.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p>Region</p>         | <ul><li>Select the <em>Region</em> of your Exotel account from the dropdown list. </li><li>For any queries, contact <a href="https://support.exotel.com/a/solutions/articles/3000114660">Exotel Support Team</a>.</li><li>The following are the available options:<ul><li>Singapore: `api.exotel.com`. This is the default value.</li><li>Mumbai: `api.in.exotel.com`</a></li></ul></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <p>From/Sender ID</p> | <ul><li>It is the ID from which the SMS is sent. </li><li>The format of this field is as follows:<br><code><VN>/<SenderID></code> where <ul><li><code><VN></code> is the Exotel Virtual </li><li>Number/ExoPhone through which you send the SMS.</li></ul></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p>SMS Type</p>       | <ul><li>Select the <em>None</em> from the dropdown if you have uploaded your templates on the Exotel dashboard.</li><li>It is used to skip template addition on Exotel Dashboard and configure SMS type based on the template registered on DLT in India. </li><li>The following are the options available:<ul><li>None</li><li><strong>transactional</strong>: Indicates that SMS consists of OTP or Service Implicit content.</li><li><strong>transactional_opt_in</strong>: Indicates that the SMS consists of Service Explicit content.</li><li><strong>promotional</strong>: Indicates that the SMS consists of Promotional content with a numeric header.</li></ul></li><li>Default value for this field is None.</li><li>If not set or incorrectly passed, Exotel will look up if the content matches Templates added on Exotel for fetching SMS Type and DLT details.</li></ul> |
| <p>DLT Entity ID</p>  | <ul><li>Indicates the Content Template ID against the SMS body registered with Distributed Ledger Technology (DLT) portal of operators in India.</li><li>It is optional if you configure it on the Exotel dashboard. If not configured, enter the DLT-approved Entity ID for your legal entity here.</li><li>It is applicable only for SMS sent by Indian businesses to Indian destination numbers.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <p>Template ID</p>    | <ul><li>It is optional if you configure it on the Exotel dashboard. Enter the DLT-approved Template ID for your legal entity if not configured.</li><li>It is applicable only for SMS sent by Indian businesses to Indian destination numbers.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

4. Select the _Template ID_ checkbox. 
5. Select the **Mark this as default** checkbox to make this SMS provider the default provider to send the SMS.
6. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful:

1. Click the **Send Test SMS** hyperlink before you start creating SMS campaigns and journeys.
2. Enter the following details: 
   - **Country Code and Mobile number**: Enter the country code and mobile number to which you want to send the message. 
   - **Message**: This is a test message powered by Exotel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/476dbd6-Send_test_SMS.png",
        "Send a test SMS",
        2232
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Send a Test SMS"
    }
  ]
}
[/block]


# Create Campaigns and Journeys

Now that your integration is successful, you can now create [SMS campaigns](doc:create-message-sms) and [journeys](https://docs.clevertap.com/docs/journeys).

# Troubleshooting

## Failed to send out test notifications

**Issue**  
The following error displays when saving Exotel credentials in the CleverTap dashboard

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/91f1ae3-Screenshot_2022-05-25_at_1.07.22_PM.png",
        "Test notifications failed",
        1536
      ],
      "align": "center",
      "border": true,
      "caption": "Test Notifications Failed"
    }
  ]
}
[/block]


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

**2. What is an SMS template, and how to get it approved? **  
Ans: To know more about SMS templates, refer to [What is an SMS template and how can I get a template approved?](https://support.exotel.com/support/solutions/articles/38686-what-is-an-sms-template-and-how-can-i-get-a-template-approved-)

**3. How do I check Exotel Account settings?**  
Ans: To check Exotel Account Settings, refer to [How to choose an SMS sender ID?](https://support.exotel.com/support/solutions/articles/126794-how-to-choose-an-sms-sender-id-)

**4. How to choose an SMS Sender ID, and what is its significance?**  
Ans: To understand this, refer to [How to choose an SMS sender ID?](https://support.exotel.com/support/solutions/articles/126794-how-to-choose-an-sms-sender-id-)

**5. How to check the delivery status of SMS sent by me?**  
Ans: To know more about delivery status, refer to [How do I find the delivery status of the SMS I sent using Exotel API?](https://support.exotel.com/support/solutions/articles/48518-how-do-i-find-the-delivery-status-of-the-sms-i-sent-using-exotel-api-)

**6. We are seeing an Exotel API error under Campaign. What is the error about?**  
Ans: Exotel API Error is raised under two circumstances. Firstly, when we try to send a message to Exotel, they do not accept it due to some error. Secondly, when Exotel replies with the error code to CleverTap. For more information on this, refer to [Error Codes](https://developer.exotel.com/api/sms#send-sms).