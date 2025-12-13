---
title: WhatsApp Subscription Management
excerpt: Learn to manage WhatsApp subscriptions effectively.
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

CleverTap, your partner in user engagement and marketing automation, offers a comprehensive solution for managing WhatsApp subscriptions for your business. With CleverTap, you can control who receives WhatsApp messages and effortlessly manage opt-ins and opt-outs. This is your guide to utilizing CleverTap to manage WhatsApp subscriptions effectively. It ensures that your communication on this influential platform is both compliant and engaging.

# Advantages of WhatsApp Subscription Management

Managing user subscriptions actively for the WhatsApp Business API is crucial for several reasons:

- **Compliance with WhatsApp Policies**: WhatsApp has strict policies and guidelines for businesses using their API. Managing subscriptions ensures that you comply with these policies, which can help you avoid potential penalties, account restrictions, or even suspension.
- **User Experience**: Active subscription management allows you to respect users' preferences. By unsubscribing users who want to opt-out and resubscribing those who want to receive messages, you enhance the user experience and reduce the likelihood of annoying or spamming your audience.
- **Reduced Costs**: Sending messages to users who have unsubscribed or are not interested can lead to unnecessary costs. By managing subscriptions, you can reduce messaging costs by targeting only engaged and interested users.
- **Relevance**: Keeping your user base up-to-date ensures that your messages remain relevant. You can send timely information, promotions, and updates to users who have expressed interest, leading to higher conversion rates.
- **Legal Compliance**: In many regions, there are laws and regulations governing electronic communications and user consent. Active subscription management helps you comply with these regulations and protects your business from legal issues.
- **Brand Reputation:** Consistently respecting user preferences and managing subscriptions effectively contributes to a positive brand image. Users are more likely to trust and engage with businesses that respect their choices.
- **WhatsApp Number Quality**: Customers can report a business number as spam and block the number. WhatsApp uses the count of spam reports and blocks to monitor the quality of messages sent. If the report/block rate goes beyond a certain threshold, then WhatsApp downgrades the quality rating of the Business’s WhatsApp, which results in downgrading messaging limits. If the business does not improve its engagements, this may lead to the business’s WhatsApp being blocked.

# Best Practices for WhatsApp Subscription Management

Managing subscriptions for WhatsApp Business Messaging requires specific practices to ensure compliance and maintain a positive user experience. It plays a vital role in maintaining user trust, complying with regulations, and providing a positive messaging experience. It helps build a strong relationship with your audience using WhatsApp for Business communication.

Here are the best practices for managing WhatsApp Business Messaging subscriptions:

- Obtain Clear and Explicit Consent: Before sending any messages via WhatsApp, ensure that users have given clear and explicit consent to receive messages from your business. Make the consent process transparent and easy to understand. You can ask for your user’s consent during important steps of their journey in your app.  
  For example:
  - App’s Signup or sign-in flow.
  - Outflows in the app.
  - Any In-app engagement
- Offer simple _Opt-In_ and _Opt-Out_ Mechanisms: Provide users with clear and simple opt-in and opt-out options. Users must know how to subscribe or unsubscribe from WhatsApp messages, and the process should be easy. CleverTap recommends using WhatsApp chats to allow users to opt in and out of WhatsApp communications.
- Differentiate Message Types: Differentiate between utility and promotional messages. Utility messages are essential for user interactions (for example, order confirmations).  However, the purpose of promotional messages is marketing and should only be sent to users who have explicitly opted in for such content.
- Respect Opt-Out Requests: Honor opt-out requests immediately. Once a user unsubscribes from WhatsApp messages, stop sending them promotional content. However, transactional messages may still be sent for essential communication.
- Update Subscription Preferences Regularly: Encourage users to update their subscription preferences anytime. This flexibility ensures that users receive the content they want.
- Automate Subscription Management: Implement automation to manage user subscriptions. Automation ensures prompt and accurate updates, reducing the risk of manual errors.
- Collect Feedback:  Encourage users who opt out to provide feedback on their reasons. This feedback can guide improvements in your subscription management and messaging practices.

# Subscription Flags

CleverTap provides the following two essential subscription flags to manage WhatsApp subscriptions:

## MSG-whatsapp

The `MSG-whatsapp` flag allows you to control the subscription status of a single user profile. By setting this flag to `false`, you can unsubscribe a user from WhatsApp messages. Setting it to `true`subscribes the user back to WhatsApp messages. The default value for this flag is `false`, so if businesses don’t set this flag, then users are considered as opted out.

## MSG-dndWhatsApp

This flag allows businesses to unsubscribe all the profiles associated with a single phone number. This ensures that a customer does not receive any WhatsApp messages from CleverTap engagements, even when a user has multiple profiles with the same phone number.  
When set to `true`, it sets the phone number to DND and unsubscribes all associated profiles. To resubscribe a user, you must set this flag to `false`. The default value for this flag is `false`, so if you do not set this flag, then users will not be considered to be added to the WhatsApp DND and will be considered opted-in if the `msg-whatsapp` flag is set to `true` for the user.

Both of the above flags work together with each other, and the user’s reachability depends on the values of both of these flags.

| msg-whatsapp | msg-dndWhatsApp | Subscription status |
| :----------- | :-------------- | :------------------ |
| Not set      | Not set         | Unsubscribed        |
| Not set      | True            | Unsubscribed        |
| Not set      | False           | Unsubscribed        |
| True         | Not set         | Subscribed          |
| True         | True            | Unsubscribed        |
| True         | False           | Subscribed          |
| False        | Not set         | Unsubscribed        |
| False        | True            | Unsubscribed        |
| False        | False           | Unsubscribed        |

# Set Up Subscription Flags

CleverTap provides multiple methods to set up and manage these subscription flags:

## Using App or Web SDK

You can use CleverTap's App and Web SDKs to send the values of these flags directly from your application or website. This allows you to manage WhatsApp subscriptions in real time based on user actions.

```json Android
// Do not call onUserLogin directly in the onCreate() lifecycle method


HashMap<String, Object> profileUpdate = new HashMap<String, Object>();
profileUpdate.put("Name", "Jack Montana"); // String
profileUpdate.put("Phone", "+14155551234"); // Phone (with the country code, starting with +)
profileUpdate.put("MSG-whatsapp", true); //Optional Flag. Enable WhatsApp notifications
profileUpdate.put("MSG-dndWhatsApp", true); // Optional Flag. Add selected profile/ phone number to the DND list.
CleverTapAPI.getInstance(getApplicationContext()).onUserLogin(profileUpdate);

```
```Text iOS (Objective-C)
// each of the below mentioned fields are optional
// with the exception of one of Identity, Email, or FBID
NSDictionary *profile = @{
@"Name": @"Jack Montana", // String
@"Phone": @"+14155551234", // Phone (with the country code, starting with +)
@"MSG-whatsapp": @YES,  //Optional Flag. Enable WhatsApp notifications
@"MSG-dndWhatsApp": @YES,  // Optional Flag. Add selected profile/ phone number to the DND list.
};
[[CleverTap sharedInstance] onUserLogin:profile];


```
```objectivec iOS (Swift)
// each of the below mentioned fields are optional
// with the exception of one of Identity, Email, or FBID
let profile: Dictionary<String, AnyObject> = [
"Name": "Jack Montana", // String
"Phone": "+14155551234", // Phone (with the country code, starting with +)
"Gender": "M", // Can be either M or F


// optional fields. controls whether the user will be receive WhatsApp .
"MSG-whatsapp": true,  //Optional Flag. Enable WhatsApp notifications
"MSG-DNDwhatsapp": true,  // Optional Flag. Add selected profile/ phone number to the DND list.
] 
CleverTap.sharedInstance()?.onUserLogin(profile)

```
```json Web
// each of the below mentioned fields are optional
// with the exception of one of Identity, Email, or FBID
clevertap.onUserLogin.push({
"Site": {
"Name": "Jack Montana", // String
"Phone": "+14155551234", // Phone (with the country code


// optional fields. controls whether the user will be sent email, push etc.
"MSG-whatsapp": true,  //Optional Flag. Enable WhatsApp notifications
"MSG-DNDwhatsapp": true,  // Optional Flag. Add selected profile/ phone number to the DND list.
}
});


```

## Using Subscription APIs

The Subscribe APIs provide the ability to set a WhatsApp phone number status as subscribed or unsubscribed. This is important so that you do not send a message to your users accidentally unless they have explicitly opted for it. There may be cases when multiple users share a WhatsApp phone number; however, once a phone number is marked as unsubscribed (DND), communication is stopped for all users using the specified number.

For example, a user opts out of receiving messages. You can pass the phone number and the status as `Unsubscribe` in the Subscribe API.  After the user opts to receive messages again, the phone number can be changed back to `Resubscribe`.

```json json
{
	"d": [
		{	
			"type": "whatsapp",
			"value": "+919213231415",
			"status": "Unsubscribe"
		},
		{
			"type": "whatsapp",
			"value": "+919213231416",
			"status": "Resubscribe"
		}
	]
}
```

## Using APIs

CleverTap offers APIs that enable you to send the values of subscription flags programmatically. This method is useful for automating the subscription management process and integrating CleverTap with your existing systems. For more information, see upload [user profiles](https://developer.clevertap.com/docs/upload-user-profiles-api). Following is an example of subscribing a user for WhatsApp messaging: 

```json
{
"d": [
{
"identity": "1189549",
"type": "profile",
"profileData": {
"MSG-whatsapp": true,//Optional Flag. Enable WhatsApp notifications
"MSG-dndWhatsApp": true  // Optional Flag. Add selected profile/ phone number to the DND list.
}
]
}


```

## Using CSV Upload

For a manual and bulk update of subscription flags, you can upload a CSV file. This is particularly useful for managing subscriptions in bulk or performing one-time updates. The following are the conditions for updating the flags:

- The _objectId_ or _identity_ must be the first column in the uploaded CSV file.
- The _Phone_ column is mandatory, and phone numbers must have the country code. For example, +14155551234. Following is a table that displays the CSV columns:

| Identity                                            | Email                                       | Phone       | MSG-whatsapp | MSG-dndWhatsApp |
| :-------------------------------------------------- | :------------------------------------------ | :---------- | :----------- | :-------------- |
| [john.doe@johndoe.com](mailto:john.doe@johndoe.com) |                                             | 14155551234 | FALSE        | FALSE           |
| 14155551235                                         |                                             |             | FALSE        | FALSE           |
| 14155551234                                         |                                             | 14155551234 | FALSE        | FALSE           |
| \_234853412                                         | [mary@gmail.com](<>)                        | 14155551234 | FALSE        | FALSE           |
| [adam@johndoe.com](mailto:adam@johndoe.com)         | [adam@johndoe.com](mailto:adam@johndoe.com) | 14155551234 | FALSE        | FALSE           |
| [bob@johndoe.com](mailto:bob@johndoe.com)           | [bob@johndoe.com](mailto:bob@johndoe.com)   |             | FALSE        | FALSE           |

## Using WhatsApp Messages

CleverTap's Journeys feature allows you to set and manage subscription flags using the _Update User Profile_ node. You can create dynamic user journeys that automatically handle subscription changes based on how your users engage with your notifications. 

The following use cases will help you visualize the possibilities:

### Use case 1: Automatically Opt-out Users Basis User Replies

WhatsApp recommends an easy way for users to opt out of WhatsApp communication. This is usually done by asking users to send a keyword such as _STOP_  in the WhatsApp chat window. This reply is then captured in CleverTap as a _Notification replied_ event along with the incoming text. This event can qualify the users in the journey and use the update profile node to manage the WhatsApp subscription. The following sections provide information about how your users can opt-out based on their replies:

##### Prerequisites

You need the following to opt-out users:

- Access to WhatsApp add-ons
- Approved Opt Out acknowledgment message template

##### Steps

Follow the steps to create a journey and opt-out users:

1. Go to _Messages_ > _Journey_ and create a new journey.

2. Go to the Setup section and change the following configuration:

   1. Entry criteria: Change to Live behavior.
   2. Journey entry timelines: Select the start time as _Now_ and the end time as _Never_. Also,  allow users to re-enter the journey.
   3. DND & Timezone: Do not select any boxes.
   4. Control group: Clear the option.
   5. Timeout: Keep the time out as low as possible, preferably in minutes.  
      The following image shows the setup:

   <br />

   [block:image]{"images":[{"image":["https://files.readme.io/be9943c-image.png",null,"Journey Setup"],"align":"center","border":true,"caption":"Journey Setup"}]}[/block]

3. After setup, drag an Action node from the Segments section in the journey canvas and configure it as follows:

   1. Use the _Notification Replied_ event and _incoming text_ as a property filter.
   2. Enter the keywords you want to use as opt-out keywords. For example, _STOP_,  or _Stop promotions_.  We recommend always using _Stop promotions_ in the opt-out Journey as this is the button text used in Marketing opt-out buttons. The following image shows the final  setup:

   <br />

   [block:image]{"images":[{"image":["https://files.readme.io/a4b3993-W1.jpeg","","Configure Action Node"],"align":"center","border":true,"caption":"Configure Action Node"}]}[/block]

4. Once done with the action node, drag a WhatsApp engagement node in the Journey canvas and connect with the _Yes_ path from the previous action node.  
   This node will acknowledge the user’s opt-out request, confirm that they have opted out, and share the steps with the users if they want to re-subscribe. The following image displays the node setup:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9c71f12-w2.jpeg",
        "",
        "Configure WhatsApp Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure WhatsApp Node"
    }
  ]
}
[/block]


5. Once the acknowledgment message has been configured successfully, drag a _user profile update_ node in the journey canvas and connect the sent, unreachable, and failed path to this _user profile update_ node. Once you have connected the _user profile update_ node with the WhatsApp engagement node, configure the profile update node as below:
   1. Click  **+ User property**, select `MSG-whatsapp` and set the value to `FALSE`.  
      The following image shows the final setup:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4acc83-w3.jpeg",
        "",
        "Configure User Profile Update Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure User Profile Update Node"
    }
  ]
}
[/block]


6. Once the_ User profile update_ node is configured, drag a _Force exit_ node and connect it with the  _user profile node_ to force exit the users from this journey. The final journey setup will look as follows.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc77c0f-w4.jpeg",
        "",
        "Configure Force Exit Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Force Exit Node"
    }
  ]
}
[/block]


After configuring the Journey and reviewing it with your peers, publish it. This journey automatically qualifies users who reply with defined keywords and prevents those users from future WhatsApp campaigns.

### Use case 2: Automatically Opt-in Users Basis User Replies

Like Opt-out, you can also prompt your users to subscribe or resubscribe to your updates on the WhatsApp channel by sending specific keywords, such as _START_, _Subscribe_, _OPT IN_, and so on. 

This reply is then captured in CleverTap as a _Notification replied \_event along with the \_incoming text_. This event can qualify the users in the journey and use the update profile node to manage the WhatsApp subscription. The following sections provide information about how your users can opt-in on the basis of their replies:

#### Prerequisites

You need the following to opt-in users:

- Access to WhatsApp add-ons
- Approved Opt-in or welcome message template.  

#### Steps

Follow the steps to create a journey and opt-in users:

1. Go to Messages > Journey and create a new journey.
2. Go to the Setup section and change the following configuration:

   1. Entry criteria: Change to Live behavior.
   2. Journey entry timelines: Select the start time as Now and the end time as Never. Also, allow users to re-enter the journey.
   3. DND & Timezone : Do not select any boxes.  
      Control group: Clear the option.
   4. Timeout: Keep the time out as low as possible, preferably in minutes.  
      The following image shows the setup:

   [block:image]{"images":[{"image":["https://files.readme.io/e716a63-image.png",null,"Overall Journey Setup"],"align":"center","border":true,"caption":"Overall Journey Setup"}]}[/block]
3. After setup, drag an _Action_ node from the Segments section in the journey canvas and configure it as below:
   1. Use the _Notification Replied_ event and _incoming text_ as a property filter.
   2. Enter the keywords you want to use as opt-in keywords. For example, _START_, _Subscribe_, _OPT IN_, and so on. The following image shows the final setup:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/10a7e80-Who_1.jpeg",
        "",
        "Setup Action Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Setup Action Node"
    }
  ]
}
[/block]


<br />

4. Once the _Action_ node has been configured successfully, drag a _user profile update_ node in the journey canvas and connect the _Yes_  path to the _user profile update_ node. After you have connected the _user profile update_ node with the _Action_ node, configure the profile update node as follows:
   1. Click the **+ user property**, select the `MSG-whatsapp` flag and set its value to`TRUE`.  
      The following image shows the final setup:

<br />

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bcf50fc-setup_1.jpeg",
        "",
        "Configure Profile Update Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Profile Update Node"
    }
  ]
}
[/block]


5. Once done with the _user profile update_ node, You must drag a WhatsApp engagement node in Journey canvas and connect with the _updated_ path from the previous node.  
   This node will acknowledge the user’s opt-in request, confirm that they have been subscribed or resubscribed, and share the steps with the users if they want to unsubscribe. The following image shows the WhatsApp node setup:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a10350b-user_profile.jpeg",
        "",
        "Configure WhatsApp Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure WhatsApp Node"
    }
  ]
}
[/block]


6. Once the _WhatsApp_ node is configured, drag a _Force exit_ node and connect the _Sent, Failed, and  Unreachable_ paths with the _Force exit_ node to force exit the users from this journey. The following image shows the final Journey setup:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03f1319-image.png",
        null,
        "Final Journey Setup"
      ],
      "align": "center",
      "border": true,
      "caption": "Final Journey Setup"
    }
  ]
}
[/block]


After the configuration of the Journey has been done and reviewed by your peers, publish the journey. This Journey will automatically qualify the user to reply with the defined keywords and opt-in those users for future WhatsApp campaigns.