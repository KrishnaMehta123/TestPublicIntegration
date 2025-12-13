---
title: Talon.One
excerpt: Loyalty Partner
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

[Talon.One](https://www.talon.one/) is a platform that allows you to create highly customizable promotional campaigns with the help of the *Campaign Manager* feature. With this integration, you can automate coupon generation and delivery to specific customer segments. You can embed Talon.One generated coupon codes directly into messages delivered through CleverTap. Thereby optimizing the reach by sending campaigns at the right time on the right channels.\
For any issues with this integration, contact [Talon.One Support team](mailto:support@talon.one).

# Prerequisites for Integration

The following are the prerequisites for setting up the integration:

* Must have integrated Talon.One SDK or API. For more information about detailed steps, refer to [Talon.One Integration](https://docs.talon.one/docs/dev/tutorials/integrating-talon-one).
* Must have access to CleverTap account.

# Send Talon.One Coupon Code Through CleverTap

To send the Talon.One coupon code through CleverTap:

1. [Set Up Webhook in Talon.One](doc:talonone#set-up-webhook-in-talonone)
2. [Set Up a Campaign in Talon.One](doc:talonone#set-up-a-campaign-in-talonone)
3. [Create a Campaign in CleverTap](doc:talonone#create-a-campaign-in-clevertap)

## Set Up Webhook in Talon.One

To set up a [webhook](https://docs.talon.one/docs/dev/getting-started/webhooks#using-parameters-in-a-webhook) in Talon.One:

1. Ensure that you set up the payload as per the parameter and authentication headers recommended by Clevertap. For more information, refer to [Upload Events API](https://developer.clevertap.com/docs/upload-events-api#section-http-method).

<Image title="Set up the webhook from Talon.One dashboard" alt={3006} align="center" border={true} src="https://files.readme.io/2279edc-Create_a_Webhook.png">
  Set Up a Webhook from Talon.One Dashboard  
</Image>

> 📘 *Display in Rule Builder* Checkbox
>
> Ensure that you select the *Display in Rule Builder* checkbox to enable webhook for your campaign.

2. Select the request *Verb* from the dropdown list and then enter the *URL*. The following table lists the API endpoint for the region of your account:

| Region                  | API Endpoint             | CleverTap Dashboard URL                                                                              |
| :---------------------- | :----------------------- | :--------------------------------------------------------------------------------------------------- |
| India                   | `in1.api.clevertap.com`  | [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/)   |
| Singapore               | `sg1.api.clevertap.com`  | [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/)   |
| United States           | `us1.api.clevertap.com`  | [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/)   |
| Indonesia               | `aps3.api.clevertap.com` | [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html#/) |
| Middle East (UAE)       | `mec1.api.clevertap.com` | [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html#/) |
| Europe (default region) | `api.clevertap.com`      | [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/)   |

3. Enter the following CleverTap account details to set up the authentication headers:
   * Project ID
   * Passcode

  These details are obtained by navigating to the *Settings* > *Project* page of the CleverTap dashboard.

<Image alt="CleverTap Project Details" align="center" border={true} src="https://files.readme.io/4ca0240-Project_Details.png">
  CleverTap Project Details
</Image>

4. Set up the parameters in the webhook payload for sending coupon codes and update them to match your campaign requirements.

```json Webhook Payload for Sending Coupon Codes
{
  "d": [
     {
         "type": "event",
         "evtName": "Coupon Generated",
         "$source": "Talon.One",
         "identity": "${$ProfileID}",
         "evtData": {
             "CouponGenerated":"${$CouponCode}"
         }
     }
     ]
     
 }
```

> 📘 Payload Parameters
>
> * The `evtName` parameter defines the EventName displayed on the CleverTap dashboard when selecting the campaign action. You can define the `evtName` as per your preference.
> * The `identity` is a mandatory parameter. This parameter is passed as the `userID`/`ProfileID`, which CleverTap uses to effectively trigger the required engagement action.

## Set Up a Campaign in Talon.One

To set up a campaign in Talon.One:

1. [Create a campaign](https://docs.talon.one/docs/product/campaigns/creating-campaigns#creating-a-campaign-from-scratch).
2. Ensure that you add the **Create a Coupon Code** [effect](https://docs.talon.one/docs/product/rules/effects/available-effects/#create-effects).
3. Select the *Store generated value in session* checkbox to send the effect-generated coupon code to CleverTap.

> 📘 Applying Effects to Campaigns
>
> When applying effects to the campaign, ensure that you [*Create the Coupon Code*](https://docs.talon.one/docs/product/campaigns/coupons/creating-coupons) and then *Create a Webhook Trigger*.

<Image title="Applying the effect to Talon.One campaign" alt={2474} align="center" border={true} src="https://files.readme.io/881db3d-Apply_Effects_to_Campaigns.png">
  Applying Effect to Talon.One Campaign
</Image>

> 📘 Identify User
>
> Use a universal ID as the `profile ID` to identify the user across Talon.One and CleverTap dashboards.

## Create a Campaign in CleverTap

You can use Email, SMS, and Push channels on the CleverTap dashboard to send coupon codes generated on Talon.One dashboard.

### Create an Email Campaign

1. Navigate to *Messages* > *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.

<Image title="Selecting Email messaging channel" alt={2720} align="center" border={true} src="https://files.readme.io/c12be0d-Selecting_Message_Channel.png">
  Create an Email Campaign from CleverTap Dashboard
</Image>

The *Campaign* page displays.

<Image title="New Email campaign page" alt={2628} align="center" border={true} src="https://files.readme.io/7038c36-Campaign_Creation_Page.png">
  New Email Campaign Page
</Image>

4. Select *Live behavior* under *Start here* section and then click **Done**.
5. *Select Service Provider* from the dropdown list.\
   You can also [Add a Service Provider](https://docs.clevertap.com/docs/generic-smtp) by clicking **Add a new service provider** link. After adding a provider, click **Refresh** to reflect the changes.

<Image title="Select Email Service Provider from the dropdown" alt={2612} align="center" border={true} src="https://files.readme.io/9f27992-Select_Email_Service_Provider.png">
  Select Email Service Provider
</Image>

6. Click **Done**.
7. (Optional) Set a goal for your campaign and then click **Done**.
8. Select *Single action:New segment* from the *Find user from segment* list with conditions as shown in the following figure:

<Image title="Select Target Segment for Email Campaign" alt={2600} align="center" border={true} src="https://files.readme.io/2d725a8-Selecting_the_evtName.png">
  Select Target Segment for Email Campaign
</Image>

9. Fetch the coupon code by typing “@” in the Email Editor under *What* section, which invokes a dropdown with the relevant event attributes. 
10. Select the coupon code that was pushed as the attribute in the webhook.

<Image title="Define Message Body and Fetch the Coupon Code in the Message Body" alt={2124} align="center" border={true} src="https://files.readme.io/da93788-Email_editor.png">
  Define Message Body and Fetch the Coupon Code in the Message Body
</Image>

<Image title="Email Campaign Preview" alt={2154} align="center" border={true} src="https://files.readme.io/21abd23-Email_campaign_preview.png">
  Email Campaign Preview
</Image>

For the remaining steps, follow the steps listed under the create campaign section of the respective messaging channels:

* [Create an Email Campaign](https://docs.clevertap.com/docs/create-message-email)
* [Create a Push Notification Campaign](https://docs.clevertap.com/docs/push-creation)
* [Create an SMS Campaign](https://docs.clevertap.com/docs/create-message-sms)
