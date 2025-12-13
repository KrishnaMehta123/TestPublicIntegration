---
title: Create Message
excerpt: Learn how to create a Web Inbox campaign using the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Campaign

To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **Web Inbox** 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74fcf43c62cc23757f5aac2b13909710759667fe55d7621e7fdf7adea825a7c2-web_inboc_l.png",
        "Click +Campaign to Create a New Web Inbox Campaign",
        "Create a New Web Inbox Campaign"
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Create a New Web Inbox Campaign"
    }
  ]
}
[/block]


The Campaign page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5627a89-web_inbox_1.png",
        "Expand all sections",
        2532
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Web Inbox Campaign Setup"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign

The _Start here_ section displays the setup information. 

This section has the following parts:

- **Set a goal**: Tracks your campaign conversions by setting a goal. This step is optional, but it helps you measure how effectively your campaign meets its goal.  
  You can define your conversion goal by selecting the _Event_ and specifying the _Conversion Time_. The _Conversion Time_ field accepts any numeric value along with a time unit such as Minutes, Hours, Days, Weeks, or Months. This allows you to define conversion windows such as 10 days, 72 hours, or 2 months. The value can range from a minimum of 1 minute to a maximum of 5 months.  
  For example, if you set the conversion time to 5 Minutes, the system counts conversions within 5 minutes of the goal event.  
  Your campaign goal can be as broad or as specific as you want. For example, you can answer questions such as: _How many users were influenced to purchase an X amount?_ or _How many first-time visitors purchased red shoes worth at least X and blue jackets worth at least Y?_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d960f90056d978b5c9f8832e66c2b3c15b6e387d3caa38ea6bc0b138c57d6b29-Conversion_Tracking.png",
        null,
        "Set Conversion Time"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Conversion Time"
    }
  ]
}
[/block]


## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a92d833-campaign_Who_Live_segment.png",
        "Define the Target Audience",
        964
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Target Audience"
    }
  ]
}
[/block]


Campaigns can be configured based on the following types of user interactions:

- Single action: User performs an action on one of your web pages.
- Page visit: User visits a particular web page on your website.
- Page referral: User visits your website via any specific referral URL.
- Page count: Number of web pages a user has visited so far in their session.

### Deliver Action Based Web Inbox Notifications

You can trigger a web inbox message based on an action. For example, a web inbox with a promo code can be shown to a set of customers who have just completed a purchase. This will help incentivize an existing user. Moreover, such messages make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign only to reach users who meet specific criteria. 

For example, you can send unique notifications to your customers based on their type of membership or subscription status.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f83ae62-Who_-Web_Inbox.png",
        "Filter on Past Behaviour and User Properties",
        2088
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Target Audience"
    }
  ]
}
[/block]


The following table explains the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](doc:user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Geography Radius",
    "3-1": "User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to this [document](https://developer.clevertap.com/docs/concepts-user-profiles#user-location-handling).",
    "3-2": "Locations = San Francisco, USA; Paris, France",
    "4-0": "Reachability",
    "4-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "4-2": "Unsubscribed email = No"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


To know more about what segments can be used, refer to [Segments](doc:segmentation).

### Calculate Estimated Reach

The Estimated Reach option allows you to preview how many users meet your targeting criteria in an online trigger campaign before publishing it. This helps you validate audience size and adjust filters to ensure the campaign reaches the intended users. 

Estimated Reach is particularly useful when you select the _Filter on past behavior and user properties_ option. You can view both the estimated user count and device count. 

To calculate the estimated reach, perform the steps below: 

1. Select **Filter on past behavior and user properties**. 
2. Click **Calculate** in the right panel. The result shows the estimated number of users or devices for that segment. You can view the following: 
   - **Total Users**: The number of users that match the filters. 
   - **Breakdown by Platform and Devices**: The users count on Android, iOS, or both, and on different devices. 
   - **Visual Indicator**: A chart summarizing the share by operating system.  
     The estimate, based on the latest available event data, updates each time you apply or modify filters. It reflects stored event data and is not a real-time count. This helps you plan and refine your audience before sending the campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44bb9f5c34466e181b1934a67365951c488221905a4373e546dfa48b7b152db8-2025-09-08_16-57-15_1.gif",
        "",
        "Calculate Estimate Reach"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Calculate Estimate Reach"
    }
  ]
}
[/block]


### Control Group

You can define the control group to compare and measure your campaign results. For more information, refer to [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2feef06-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Define Control Group"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Control Group"
    }
  ]
}
[/block]


### Targeting Cap

You can limit the number of users receiving the notification. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message. This way, you ensure it aligns precisely with the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

## Web Inbox Message Types

You can create the following types of messages for your web inbox campaigns:

- Single Message
- A/B Test 
- Split Delivery
- By User Property

Click _Go To Editor_ to create your message. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7692186-editor_web_inbox.png",
        "Web Inbox Editor",
        1986
      ],
      "align": "center",
      "border": true,
      "caption": "Web Inbox Single Message Editor"
    }
  ]
}
[/block]


### Single Message

In this campaign, we send the same notification to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get user clicks. You can test up to three message variants on a test group. The variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration. You can test up to three message variants.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. You can send up to 50 message variants to different users based on a user property. A good example would be when you want to send a localized update to people based on their preferred language. Similar to creating A/B test variants, click **+ Variant** to add multiple variants based on a user property value. 

## Web Inbox Templates

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e2f5c41-templates.png",
        "Select from Web Inbox Templates",
        1576
      ],
      "align": "center",
      "border": true,
      "caption": "Web Inbox Templates"
    }
  ]
}
[/block]


Marketers get instant access to ready-to-use message templates for creating engaging web inbox campaigns. CleverTap supports three types of templates:

- Text Only 
- Tex and Icon
- Text, Icon, and Image 

## Text Only

As the name suggests, the Text Only template primarily allows you to create and send text messages to your website users under the website's notification tray. 

You can craft the _Title_ and _Description_ fields as per your creativity to make the messages more engaging and personalized for better conversions. 

You also get the option to add a link and buttons for your web inbox message. You can also define the on-click actions for the buttons in the web inbox message for enhanced engagement.

Additionally, you can also assign a category to your message from all the categories you have defined in _Settings_.  For example, if the message to be sent is promotional, you can assign it to the _Promotions_ category. Learn more about assigning the categories in the _[Setup](doc:web-inbox-setup#web-inbox-window-configuration)_ section.

You can configure the number of days (or hours) to keep the web inbox message on the user's device by setting the _time to live_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6945bd9-Web_inbox_text_only.png",
        "Web Inbox Text Only Template",
        2550
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Web Inbox Message"
    }
  ]
}
[/block]


## Text and Icon

The _Text and Icon_ template is similar to the _Text Only_ template with an additional option of adding an Icon to the message. Adding an icon helps you make your web notification visually appealing. 

You can either upload the icon image directly or enter the URL of a hosted icon image.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/13093fc-web_inbox_text_with_image.png",
        "Web Inbox Text with Image template",
        2552
      ],
      "align": "center",
      "border": true,
      "caption": "Text with Icon Template"
    }
  ]
}
[/block]


## Text Icon and Image

This template is similar to the Text and Icon Template. As the name suggests, this template allows you to add an image along with the text and icon in your web inbox message. Adding an image primarily makes your web inbox messages visually appealing and increases the chances of conversions. Overall, it helps you improve engagement rates. The remaining configurations and layout are similar to the other two templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f13277-web_inbox_icon_and_image_with_text.png",
        "Text with Icon and Image Template for Web Inbox ",
        2552
      ],
      "align": "center",
      "border": true,
      "caption": "Text with Icon and Image Template"
    }
  ]
}
[/block]


> 🚧 Choosing the Right TTL
> 
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

> ❗️ Events via API
> 
> For live action campaigns, messages are not delivered to the Web inbox if the qualifying event is sent via API.

### Supported Media Types

The supported media types include:

| Media Type            | 16:9 Aspect Ratio | 1:1 Aspect Ratio | Max Size |
| :-------------------- | :---------------- | :--------------- | :------- |
| Image (jpg, png, gif) | Yes               | Yes              | 500 KB   |

### Preview

You can click _Preview_ to view the overall appearance of your web inbox message in a new tab.

## Define the Campaign Schedule

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9641c0e-web_inbox_when.png",
        "Define the Campaign Schedule",
        1680
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Define the Campaign Schedule"
    }
  ]
}
[/block]


You can set up the _When_ to schedule the campaign start and end using the following options:

Live campaigns can be set up on a specific event:

- In response to a user event.
- User event/inaction combination (for example, abandoned cart scenario).
- Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the _Exclude from campaign limits_ option from the dropdown or choosing the appropriate cadence on how often to send your campaign.

You can choose from any of the following:

- Exclude from campaign limits
- Once per session
- Once per day
- Once per user for the duration of this campaign

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf4c04a-DP.png",
        "Changes Based on Segment Selection",
        1298
      ],
      "align": "center",
      "border": true,
      "caption": "Delivery Preferences"
    }
  ]
}
[/block]


## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary and click **Publish Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Campaign",
        1193
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]