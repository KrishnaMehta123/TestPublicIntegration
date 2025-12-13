---
title: MSG91
excerpt: WhatsApp Provider
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

[MSG91](https://msg91.com/in) offers robust WhatsApp messaging solutions that enable businesses to engage with customers through rich media messages, feedback collection, and automated processes. By integrating MSG91 with CleverTap, you can enhance your customer communication strategies by:

* Sending engaging carousels and interactive messages to deliver dynamic content to captivate your audience.
* Collecting valuable customer feedback to gain insights to improve your services.
* Building automated flows and enabling seamless payment processes to streamline operations and enhance user experience.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by MSG91. The CleverTap and MSG91 integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [MSG91](mailto:support@msg91.com) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

* You must have WhatsApp add-on enabled on the CleverTap account in addition to the Basic or Essentials Plan.
* Ensure that WhatsApp onboarding for the phone number to be used with CleverTap is completed. If you want to activate a new phone number with WhatsApp Business API via MSG91, contact your Account Manager or send an email to [partners@msg91.com](mailto:partners@msg91.com).
* Ensure that you have the API URL and credentials from MSG91.

# Integrate MSG91 with CleverTap

This process involves the following two steps:

1. [Configure CleverTap Dashboard](doc:msg91-whatsapp#configure-clevertap-dashboard).
2. [Set Up CleverTap Callbacks in MSG91](doc:msg91-whatsapp#set-up-clevertap-callbacks-in-msg91).

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* from the CleverTap dashboard.
2. Click **+ Add Provider** and select *Generic (Other)* from the dropdown.

<Image alt="Provider Setup" align="center" width="65% " border={true} src="https://files.readme.io/885f26f7e2110aab22dd2bda2eba90bc4c3e187863d865a407301bc495da3a4d-image.png">
  Provider Setup
</Image>

3. Enter the following details:

| Field          | Details                                                                                                                                                       |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nickname       | Enter the nickname as *MSG91* or MSG91 \<10-digit phone number> for easy reference.                                                                           |
| Mobile Number  | Add your WhatsApp Integrated number with country code (for example, 918889500122)                                                                             |
| Request Type   | Ensure the Request Type is *POST*.                                                                                                                            |
| HTTP End Point | Enter HTTP Endpoint as the following:[https://api.msg91.com/api/v5/whatsapp//outbound/clevertap/](https://api.msg91.com/api/v5/whatsapp//outbound/clevertap/) |
| Authentication | Select Basic Authentication and enter the Username of your MSG91 account.                                                                                     |

4. (Optional) Select *Mark this as default to make this service provider the default provider* to send a WhatsApp message via MSG91.
5. (Optional) Select *Set auto-reply for users not tracked on CleverTap* to automatically reply to users who message on WhatsApp but are not tracked on the CleverTap dashboard.
6. (Optional) Set the *Maximum Concurrent API requests* between 30 and 1000. Consider your requirements and the provider's limitations when defining this value.

## Set Up CleverTap Callbacks in MSG91

To set up CleverTap callbacks in MSG91, follow the steps below:

1. **Locate Callback URLs in CleverTap**: Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *MSG91* from the CleverTap dashboard. You will find the required Callback URLs on the *Provider Configuration* page.

<Image alt="Callback URLs" align="center" width="65% " border={true} src="https://files.readme.io/223edc0dd9395b8efbd83593933324956c2341e18a79097859d8ff3285b8efbf-image.png">
  Callback URLs
</Image>

2. **Configure Inbound Message Callback in MSG91**: Copy the *Inbound Message Callback URL* from the CleverTap dashboard and paste it into the *Inbound Messages* section of the webhook in the MSG91 panel.

<Image alt="Configure Inbound Message Callback in MSG91" align="center" border={true} src="https://files.readme.io/0983f272d9b7981e56f98dd7f2af74f3a3f09d10f46cd2e14f51169021033d33-image.png">
  Configure Inbound Message Callback in MSG91
</Image>

3. **Configure Outbound Message Callback in MSG91**: Copy the *Delivery Report Callback URL* from the CleverTap dashboard and paste it into the *Outbound Messages* section of the webhook in the MSG91 panel.

<Image alt="Configure Outbound Message Callback in MSG91" align="center" border={true} src="https://files.readme.io/8117a35d118ccfe4b13d8c780341fcc7d162eac2027a4345a32ab7f3c49cb8fb-image.png">
  Configure Outbound Message Callback in MSG91
</Image>

4. Add the following header values to your webhook configuration in the CleverTap dashboard:

| Field        | Details                                                                                                                                                                                                    |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Authkey      | Enter your MSG91 Authkey. This is a unique key used to authenticate API requests. Refer to the [MSG91 Auth](https://msg91.com/help/api/where-can-i-find-my-authentication-key) key to obtain your Authkey. |
| Content-type | Set this to `application/json` to indicate that the request body is in JSON format.                                                                                                                        |
| Accept       | Set this to `application/json` to specify that the response should be in JSON format.                                                                                                                      |

<Image alt="Configure Headers" align="center" width="50% " border={true} src="https://files.readme.io/e47df80c73ea34c89ba02cbd904cf9c685e08845c768ae77ae8b75ad0d96734e-image.png">
  Configure Headers
</Image>

5. Enable the CleverTap toggle in the MSG91 panel's WhatsApp number settings before clicking the **Save** button.
6. Test the integration, then click **Save** to finalize the setup.

> 📘 Note:
>
> You have to get your templates approved on the MSG91 dashboard. Once approved, add the same templates in the CleverTap dashboard for sending out messages. For more information and queries about the MSG91 integration, write to [support@msg91.com](mailto:support@msg91.com).

## Adding Message Templates

To create WhatsApp campaigns, you must have pre-approved WhatsApp message templates saved in the CleverTap dashboard. To add the templates, follow these steps:

1. Go to *Settings* > *Channels* > *WhatsApp* > *WhatsApp Connect* > *Provider Nickname* in the CleverTap dashboard. Further, Select the *Templates* option and click **+Template**.

<Image title="Create a New Template" alt="Create a New Template" align="center" border={true} src="https://files.readme.io/70d1653-non_CT_approved_templates.jpg">
  Create a New Template
</Image>

2. Enter the template name.
   > 📘 Naming WhatsApp Templates
   >
   > Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
   >
   > For example, if you have multiple provider configurations, such as Phone\_1 and Phone\_2, you can use the a particular template name once within Phone\_1 and Phone\_2.
3. You can also choose the language in which you want to display the message.
4. Select the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, or *Location*.
5. Create a [Limited Time Offer Template](doc:whatsapp-message-templates#limited-time-offer-templates), if required. 
6. Enter the message content.
7. Select *Footer* to add a footer text and a button (Quick Reply or a Call To Action).

<Image alt="Define Template Content" align="center" border={true} src="https://files.readme.io/5bd5090-Generic_template_create.jpg">
  Define Template Content
</Image>

8. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Right-click the ellipsis below the template. 
2. Click **Send Test**.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click **Send Test**.  

<Image title="Test a Message Template" alt={1304} align="center" border={true} src="https://files.readme.io/fbf00f7-test_template.png">
  Test a Message Template
</Image>

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the MSG91 team to debug the issue, as shown in the following figure:

<Image title="Successful Delivery Response" alt="Screen shows the format of a successful delivery response after sending a WhatsApp Message" align="center" width="smart" border={true} src="https://files.readme.io/2fc576b-Whatsapp_Infobip_send_test.png">
  Successful Delivery Response
</Image>

## Create Campaign

For detailed instructions on creating a WhatsApp campaign using MSG91 as the provider, refer to [Create a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

## Creating a Journey

For detailed instructions on creating a WhatsApp journey using MSG91 as the provider, refer to [Create a WhatsApp Journey](https://docs.clevertap.com/docs/engagement-nodes-whatsapp).
