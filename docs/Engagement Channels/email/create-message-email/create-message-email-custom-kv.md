---
title: Create Message
excerpt: Learn how to create an Email campaign using the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Campaign

Create a campaign to deliver your message.  
To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d72b84599813825ce05f1bf3ab90ddb652da8b3e97294369f7346fa1e0c05133-3.png",
        "Select Messaging Channel",
        "Select Messaging Channel"
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Select Messaging Channel"
    }
  ]
}
[/block]


The _Campaign_ page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Campaign Creation Page",
        1404
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create Campaign"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign Setup

The _Start here_ section displays the setup information. 

This section has the following parts:

- Qualification criteria: Deliver the notification by Past behavior/Custom list, Live behavior, or [External trigger](doc:external-trigger-1). For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments). 
- Email Service Provider: Select a provider.
- Set a Goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced for purchasing an X amount?_ to _How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_ ". 

Define the conversion period by selecting the _Conversion Time_. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](doc:events). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Set a Goal to Track Conversion",
        919
      ],
      "align": "center",
      "border": true,
      "caption": "Set a Goal"
    }
  ]
}
[/block]


## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list. 

For Past Behavior segments, you also calculate the estimated reach. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/030202d-Push_notification_editor_Who.png",
        "Define the Audience of your Campaign",
        1168
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Define - Who"
    }
  ]
}
[/block]


### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

> 🚧 Delay > 24 Hours
> 
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live _Inaction within time_ campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; that is the golden window within which most users transact on iOS and Android app platforms.

On this basis, you would then set up the _Who_ by sending this campaign to all users who qualify or limit the users who qualify under _Estimated reach_. 

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Deliver Messages based on Past Behavior (PBS)

You can also target users based on their past user behavior. For past behavior campaigns, you also have the option to calculate estimated reach. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users via mobile push.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d4faa2-Filter_By_User_Properties.png",
        "Filter with User Properties",
        486
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]


To know more about what segments can be used, see [Segments](doc:segments).

### Constant event property (Optional)

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define a control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c1847be-Email_Control_Group.png",
        null,
        "Control Group"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Control Group"
    }
  ]
}
[/block]


### Targeting Cap

You can limit the number of users receiving the message. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af07d3a-Set_Target_Segment_Cap_.png",
        null,
        "Target Cap"
      ],
      "align": "center",
      "border": true,
      "caption": "Target Cap"
    }
  ]
}
[/block]


This section explains the campaign creation flow when you are determining who to send your message to. Under the _Estimated Reach_ section, select the option to limit the delivery of the messages to a specified number.  
The campaign limits can also be configured using the following options: 

- **All target segment users**: Select this option to send the campaign to all the target segment users. You can also prevent sending out unwanted campaigns by _Don't send the campaign if target segment exceeds_ checkbox and entering the value for the number of users. When selecting this option, a campaign does not run if the number of qualified users exceeds the safety limit. The campaign creator receives an email alert for further action.
- **Only**: Select this option to limit the number of users for each run of a campaign.

For triggered campaigns based on live user segments, the users receive a message as they qualify until the total quantity specified has been delivered, after which the campaign ends. For campaigns based on _Past Behavior Segments_, we randomly select the users who receive the message.

### Override Communication Preferences for Email

You must use this option only when you want to send critical emails of a non-promotional nature, such as privacy policy updates, legal/regulatory information, and downtime/outage-related updates to customers. To do so, select _Send email to users who have opted out of your emails_ to send the emails to all qualified users, including those who have opted out (i.e., unsubscribed from email campaigns). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af08a90-image.png",
        null,
        "Override Communication Preferences for Emails"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Override Communication Preferences for Emails"
    }
  ]
}
[/block]


Once you select this option, you are prompted to confirm that this email is in compliance with spam regulations.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37c60cd-Compliance_Confirmation_Prompt.png",
        null,
        "Compliance Confirmation Prompt"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Compliance Confirmation Prompt"
    }
  ]
}
[/block]


As you cannot unsubscribe from this type of email, it is advisable to refrain from including unsubscribe links in these emails. If you still choose to use the unsubscribe links, clicking on the link results in the user being unsubscribed only from promotional emails. If the user is marked unsubscribed at the Email Service Provider's end, this email would still not be delivered to the end user. Therefore, this feature is most effective when using CleverTap’s [Handling Unsubscribes](doc:handling-unsubscribes) method instead of adding ESP-specific unsubscribe links to your emails.

> 🚧 Warning
> 
> To avoid spamming the recipient's inbox and potentially harming your domain reputation, exercise utmost caution when enabling this option for your email campaign. It is important to note that any legal issues resulting from the violation of relevant anti-spamming laws will not be the responsibility of CleverTap.

### Exclude Unsubscribe groups

Select the subscription groups to exclude from your campaign. For more information, refer to [unsubscribe subscription groups in campaigns](https://docs.clevertap.com/docs/group-unsubscribe)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b69404c-Email_subscription_group_include_exclude.png",
        "Select Subscription Group to Exclude or Include",
        926
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Select Subscription Groups"
    }
  ]
}
[/block]


### Include Selected Subscription Groups

Subscription groups allow users to select the content they want to receive, reducing unsubscription rates and fostering strong brand-user relationships. This approach enhances user satisfaction and builds a more personalized connection with your audience. 

Select the groups you want to include in your campaign from the _Select Subscription Groups_ list. This allows you to target users who have subscribed to all the groups you selected for the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18f16e4-Email_Control_Group1.png",
        "",
        "Select Subscription Groups"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Subscription Groups"
    }
  ]
}
[/block]


## Define the Message Content

Now, you can set up the _What_ which is the email campaign content where you have four different options. Click _Go To Editor_ to create your message. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/56de1b4-Email_editor.png",
        "Select Message Type of the Email Campaign",
        959
      ],
      "align": "center",
      "border": true,
      "caption": "Select Message Type"
    }
  ]
}
[/block]


### Email Editor

Select the templates and create a message. You can also get inbox previews and spam reports for your email message before you send out the campaign. For more information on the Email editor, see [Email Editor](https://docs.clevertap.com/docs/email-editor-templates). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e63eee8-Email_editor_main.png",
        "Select the Email Editor Type",
        1121
      ],
      "align": "center",
      "border": true,
      "caption": "Select Email Editor"
    }
  ]
}
[/block]


### Sender Details

After setting up the content of your campaign in the What section, you can configure how your email appears to recipients. This helps ensure that the email adheres to best practices for deliverability and compliance. All the fields under this section can be personalized (see the following image).

> 📘 Private Beta
> 
> You can now add **From **and **Reply To** fields in emails for the following providers: Sendgrid, Amazon SES, and Generic SMTP setup. This feature is released in Private Beta.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1012b8812dca83d9d8b782ebc591063eb690b8585bdbeafba95faebbeef60d51-Sender_Details.png",
        "",
        "Sender Details"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Sender Details"
    }
  ]
}
[/block]


The _Sender Details_ section encompasses the following:

- **From**: This is a mandatory field. This name is displayed as the sender of the email. It is important as it helps recipients recognize the sender, thereby increasing the likelihood of them opening the email. You can use the personalized value for this field when sending test campaigns, but only if the [Send Test Personalization](doc:send-test-personalization-for-email) feature is enabled for your account.
- **From Email Address**: This is a mandatory field. This field specifies the email address from which the campaign is sent to the recipient. A default email address that has been added during the setup under  _From Address_ field under the _Settings_ > _Email_ > _Providers_ >  _Setup_ page will be pre-populated in this field. You can use the personalized value for this field when sending test campaigns, but only if the [Send Test Personalization](doc:send-test-personalization-for-email) feature is enabled for your account.
- **Reply-to Email Address**: This is a mandatory field. This field determines the email address where replies will be directed, ensuring that responses from recipients are sent to the appropriate point of contact. A default email address that has been added during the setup under  _Reply-to-Address_ field under the _Settings_ > _Email_ > _Providers_ >  _Setup_ page will be pre-populated in this field. You can use the personalized value for this field when sending test campaigns, but only if the [Send Test Personalization](doc:send-test-personalization-for-email) feature is enabled for your account.
- **Subject**: This is a mandatory field. It is crucial for grabbing the recipient's attention and giving them a reason to open the email.
- **Preheader**: This is the short summary text that follows the subject line when the email is viewed in the inbox. It provides additional context and can encourage recipients to open the email. For example, if you are running a campaign for the Black Friday Sale, you can define this text as Get 50% OFF only for today.
- **Plain-Text For Body**: This text displays in the campaign body if the recipient's inbox provider does not support HTML or formatted text. It can only contain plain text and cannot include images, styled content, or hyperlinks.
- **CC/BCC**: This field allows you to send a copy of your email campaigns to additional recipients directly from the CleverTap dashboard. For more information, refer to the [CC/BCC](doc:create-message-email#ccbcc) section. 
- **Custom headers**: These are additional key-value pairs that you can define and include in your email headers. CleverTap supports adding these under the _What_ section of the campaign. For more information, refer to [Custom Headers](doc:create-message-email-custom-kv#custom-headers).
- **Custom extras**: These are additional key-value pairs that you can define and include along with your email body. CleverTap supports adding these under the _What_ section of the campaign. For more information, refer to [Custom Extras](doc:create-message-email-custom-kv#custom-extras).
- **Highlight with Gmail Promotional Annotations**: This field enables you to highlight your email on the Gmail Promotions tab. Your email can include additional information, such as promotion codes, a featured image, and deal expiration dates. For more information, refer to [Gmail Promotional Annotations](doc:gmail-promotional-annotations-product-carousel).

#### CC/BCC

> 📘 Private Beta
> 
> This feature is released in Private Beta. You can now add CC/BCC recipients in emails for the following providers: Sendgrid, Amazon SES, and Generic SMTP setup

This feature allows users to send a copy of their email campaigns to additional recipients directly from the CleverTap dashboard. Using this feature, brands can ensure that key stakeholders receive necessary email communications simultaneously, facilitating better tracking, compliance, and customer relationship management. Here are some of the use cases:

- E-commerce, Travel, and Hotel brands often need to send email campaigns to their customers and sellers while keeping the respective account managers informed. In this case, the marketers can use the CC feature to copy account managers on all relevant communications, ensuring they stay updated and can provide timely support.
- In the case of the Real estate industry, the realtors can use the CC feature to copy agents or brokers when sending emails to high-intent users to ensure these agents can track and nurture those prospects toward making a purchase. 
- FinTech companies can use the BCC feature to discretely send emails to their legal team, ensuring that all communications comply with legal standards without the primary recipient's awareness.

You can add up to a total of 20 CC and BCC recipients to your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2452c86-Adding_CC_BCC_recipients.png",
        null,
        "Adding CC/BCC Recipients to Email Campaigns"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Adding CC/BCC Recipients to Email Campaigns"
    }
  ]
}
[/block]


> 📘 Key Points to Remember
> 
> - In the case of Generic SMTP, ensure that your email service provider supports the CC/BCC feature to use it on CleverTap.
> - Using CC/BCC in emails lead to increased email consumption because the copy of each mail sent to the recipient is also sent to the CC and/or BCC recipients, resulting in greater email traffic.

<br />

#### Custom Headers

> 📘 Private Beta
> 
> Currently, this feature is released in Private Beta. If you want to access this feature, contact your Customer Success Manager (CSM).

Custom Headers allow you to define additional fields in the email headers section. You can add unique user identifiers, such as `campaign_id`, `user_id`, etc., to track engagement and correlate the stats with your CRM data.

For example, you can incorporate `gmail_feedback_id` as a custom key-value pair within your email headers to leverage [Gmail’s Feedback Loop (FBL)](https://support.google.com/a/answer/6254652?hl=en). This enables you to monitor campaigns with high complaint volumes from Gmail users and aids in early abuse detection.

Custom headers are supported for the following email service providers: SendGrid, Amazon SES, and Generic SMTP. Custom headers are also supported for Infobip if you are using CleverTap's Advanced Email Add-On:

> 🚧 Reserved Keys
> 
> - The following providers have certain reserved header keys. Ensure that you do not include any of these within Custom Headers, as doing so results in email delivery failure.
> 
> | Provider | Reserved Keys                                                                                                                                       |
> | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
> | Infobip  | `To`, `Cc`, `Bcc`, `From`, `Subject`, `Content-Type`, `DKIM-Signature`, `Content-Transfer-Encoding`, `Return-Path`, `MIME-Version`                  |
> | SendGrid | `x-sg-id`, `x-sg-eid`, `received`, `dkim-signature`, `Content-Type`, `Content-Transfer-Encoding`, `To`, `From`, `Subject`, `Reply-To`, `CC`, `BCC`. |
> 
> - The following keys are reserved by CleverTap. If these reserved keys are included in the payload, they are dropped.
> 
> | Provider          | Reserved Keys                                                                                       |
> | :---------------- | :-------------------------------------------------------------------------------------------------- |
> | SendGrid, Infobip | `List-Unsubscribe`, `List-Unsubscribe-Post`                                                         |
> | SMTP, Amazon SES  | `List-Unsubscribe`, `List-Unsubscribe-Post`, `X-CleverTap_META`, `X-CLEVERTAP_METADATA`, `X-Nep-Ff` |

#### Custom Extras

> 📘 Private Beta
> 
> Currently, this feature is released in Private Beta. If you want to access this feature, contact your Customer Success Manager (CSM).

Custom Extras allow sending additional information along with the email HTTP payload. You can include unique user identifiers, such as Campaign ID, Subscription Type, etc., in the email payload. This is helpful for post-processing, tracking, and custom analysis in your external systems. 

For example, you can include `category_name: "Loan"`in the email payload using Custom Extras. This data enables more granular tracking and analysis in your external systems based on the `cateogy_name` key and helps modify your strategies accordingly.

Custom Extras are supported if you are using SendGrid as the email service provider. For Amazon SES, this feature is currently available in Private Beta and is supported only for [HTTP protocol](doc:amazon-ses).

> 🚧 Reserved Keys
> 
> The following keys are reserved by CleverTap. If these reserved keys are included in the payload, they will be ignored.
> 
> | Provider | Reserved Keys                             |
> | :------- | :---------------------------------------- |
> | SendGrid | `iid`, `idn`, `pivot`, `targetID`, `meta` |

#### Add Custom Headers and Extras

1. Go to the **What** section of the email campaign and click **Go to Editor**.
2. Draft your email campaign and select the _Sender Details_ tab. 
3. Select **Custom Headers** and/or **Custom Extras** to add the respective key-value pairs.
4. Click **+ Header** and/or **+ Extra** to add the key and value in the respective fields. You can also personalize the value of the keys you want to add.

> 📘 Note
> 
> - When using the Generic SMTP integration, ensure that you use only custom headers. Any key-value pairs added within custom extras are dropped.
> - Including headers or extras for providers that do not support them, would result in those being dropped from the outgoing payload.
> - You can add a maximum of 10 parameters in both Custom Headers and Custom Extras respectively.
> - The combined size of Custom headers and Custom extras must not exceed 1KB.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f62d982b783e8113fe10dc4c281ef737a4951e1a9102fd8e49671df373f21a84-Add_Custom_Headers_and_Extras.png",
        "",
        "Sender Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Custom Headers and Custom Extras"
    }
  ]
}
[/block]


Once you have drafted your campaign, you can check how it appears to your target audience using the _Preview & Test_ option. The personalized values for the keys are rendered if you have the [Send Test Personalization](doc:send-test-personalization-for-email) feature enabled for your account.

### Preview & Test

After setting up the content of your campaign in the _What_ section, you can send a test email notification to any CleverTap user profile you have marked as a _Test profile_.  
Click the **Preview & Test** button from the message editor to test a message.

You can also check view [Inbox Previews](https://docs.clevertap.com/docs/email-editor-templates#inbox-previews-with-code-analysis) and [Spam Report](https://docs.clevertap.com/docs/email-editor-templates#spam-report).

### Message Types

You can create the following types of messages:

- Single Message
- A/B Test 
- Split Delivery
- By User Property

#### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

#### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most views is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

#### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

##### Split Delivery to Past Behavior Segments

For campaigns sent to _Past Behavior Segments_ (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

- If you are testing three messages (e.g., Variant A, Variant B, Variant C).
- Your campaign reach is 2,000,000 users.
- You choose a test population of 15% of campaign reach (300,000 users).

Then, we send:

- Variant A to 100,000 users.
- Variant B to 100,000 users.
- Variant C to 100,000 users.

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of views. We then automatically send the winning message to the remainder of your target audience, which is 1,700,000 users in this example.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

##### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of views and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

#### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

## Define the Campaign Schedule

You can set up the _When_ to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

- On a specific date and time.
- On multiple specified dates and times.
- Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

- In response to a user event.
- User event/inaction combination (e.g., abandoned cart scenario).
- Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

### Delivery preferences

Global campaign limits are limits you can apply to determine how many messages each app user receives per day. If you want to override these settings for an important campaign, you can click on the _Don’t apply global campaign limits to this campaign_ checkbox.

You can also _Do Not Disturb_ (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours are complete, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Notification delivery options](doc:notification-delivery-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1f9337-campaign_when_PBS.png",
        "Select Campaign Start/End Date and Time",
        1196
      ],
      "align": "center",
      "border": true,
      "caption": "Define - When"
    }
  ]
}
[/block]


> 📘 Recurring Day
> 
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish the Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]