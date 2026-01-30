---
title: Create Message
excerpt: Learn how to create a Web Popup campaign using the CleverTap dashboard
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Create a New Web Pop-up Campaign

Create a campaign to deliver your Web Popup message. Follow the steps below to create a new web popup campaign:

1. From the dashboard, navigate to _Campaigns_.
2. Click **+ Campaign** button.
3. From the _Messaging Channels_ list, select _Web Popup._

<Image align="center" alt="Select Messaging Channel" border={true} caption="Select Messaging Channel" title="Campaign Button Lists All Channels" src="https://files.readme.io/905892d13c4a67624587e05e7d1ee992dbabc7408451c23f659114fa590a25aa-wepuchs.png" />

The campaign page displays.

<Image align="center" alt={1100} border={true} caption="Create Campaign" title="Expand Each Section" src="https://files.readme.io/4bf6219-Web_pop_up_Editor_main.png" width="80%" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The _Start here_ section displays the setup information.

* **Set a goal**: Tracks your campaign conversions by setting a goal. This step is optional, but it helps you measure how effectively your campaign meets its goal.  
  You can define your conversion goal by selecting the _Event_ and specifying the _Conversion Time_. The _Conversion Time_ field accepts any numeric value along with a time unit such as Minutes, Hours, Days, Weeks, or Months. This allows you to define conversion windows such as 10 days, 72 hours, or 2 months. The value can range from a minimum of 1 minute to a maximum of 5 months.  
  For example, if you set the conversion time to 5 Minutes, the system counts conversions within 5 minutes of the goal event.  
  Your campaign goal can be as broad or as specific as you want. For example, you can answer questions such as: _How many users were influenced to purchase an X amount?_ or _How many first-time visitors purchased red shoes worth at least X and blue jackets worth at least Y?_

<Image align="center" alt="Set Conversion Time" border={true} caption="Set Conversion Time" src="https://files.readme.io/d960f90056d978b5c9f8832e66c2b3c15b6e387d3caa38ea6bc0b138c57d6b29-Conversion_Tracking.png" width="75% " />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

<Image align="center" alt={2448} border={true} caption="Define Target Segment - Who" title="Define Target Audience" src="https://files.readme.io/6e9cb3a-Web_Popup_Segment_.png" />

Campaigns can be configured based on the following types of user interactions:

* Single Action: Target users based on action on one of your web pages.
* Page Visit: Target users visiting specific web pages. For example, a page such as _[https://ctcart.com/black_friday_sale](https://ctcart.com/black_friday_sale)_, where you can create a campaign to target users that visit the Black Friday sale on your website. You can add multiple pages.
* Page Referral: Target users visiting your website via any referral web page. For example, users who have visited your website through a Black Friday sale advertisement on google, such as  
  _[https://ctcart.com/redirect?utm_medium=google&utm_campaign=black_friday_sale](https://ctcart.com/redirect?utm_medium=google\&utm_campaign=black_friday_sale)_.
* Page Count: Target users based on the specified number of web pages visited in a single session.

### Deliver Action Based Web Popup Notifications

You can trigger a web popup message based on an action. For example, a web popup with a promo code can be shown to customers who have just completed a purchase. This will help incentivize an existing user. Moreover, such popups make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria.

For example, you can send a web popup notification to female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

<Image align="center" alt={2202} border={true} caption="Filter by User Properties" title="Add Multiple User Properties" src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png" />

The following table explains the various property types:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Type
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Properties
      </td>

      <td>
        Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
      </td>

      <td>
        Customer Type = Platinum
      </td>
    </tr>

    <tr>
      <td>
        Demographics
      </td>

      <td>
        Demographics filters include _Age_ and _Gender_.
      </td>

      <td>
        Age = 25 to 40 years  
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States  
        State = California  
        City = San Francisco
      </td>
    </tr>

    <tr>
      <td>
        Reachability
      </td>

      <td>
        Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.
      </td>

      <td>
        Unsubscribed email = No
      </td>
    </tr>

    <tr>
      <td>
        App Fields
      </td>

      <td>
        App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segmentation).

> ℹ️ Web Pop-ups Require Web SDK Events
>
> Web pop-up campaigns are not supported for events triggered via API. They are exclusively rendered for events raised from the device through the Web SDK.

### Calculate Estimated Reach

The Estimated Reach option allows you to preview how many users meet your targeting criteria in an online trigger campaign before publishing it. This helps you validate audience size and adjust filters to ensure the campaign reaches the intended users.

Estimated Reach is particularly useful when you select the _Filter on past behavior and user properties_ option. You can view both the estimated user count and device count.

To calculate the estimated reach, perform the steps below:

1. Select **Filter on past behavior and user properties**.
2. Click **Calculate** in the right panel. The result shows the estimated number of users or devices for that segment. You can view the following:

   * **Total Users**: The number of users that match the filters.
   * **Breakdown by Platform and Devices**: The users count on Android, iOS, or both, and on different devices.
   * **Visual Indicator**: A chart summarizing the share by operating system.  
     The estimate, based on the latest available event data, updates each time you apply or modify filters. It reflects stored event data and is not a real-time count. This helps you plan and refine your audience before sending the campaign.

   <Image align="center" border={true} caption="Calculate Estimate Reach" src="https://files.readme.io/7d5d08ea1d6ba307004edba25c570ba1dd85fb0f8fe6f80f23cc054186da2f38-2026-01-30_19-12-06_1.gif" width="85% " />

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups)

<Image align="center" alt={2338} border={true} caption="Control Group" title="Control Group and Targeting Cap" src="https://files.readme.io/ca9ad92-Screenshot_2021-10-22_at_1.25.05_PM.png" />

## Web Pop-up Message Types

You can create the following types of messages for your web exit intent pop-ups:

* Single Message
* AB Test
* Split Delivery
* By User Property

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best in the pop-up to get clicks from users.  
You can test up to three pop-up message variants on a test group. The variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

<Image align="center" alt={2326} border={true} caption="A/B Test Variant Distribution" title="Identify Best Variant" src="https://files.readme.io/561e7ef-Web_popup_AB_test.png" />

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the duration of the campaign.

<Image align="center" alt={2344} border={true} caption="Split Delivery Variant Distribution" title="Control Variant Distribution" src="https://files.readme.io/b3026b1-pop-up_slit_delivery.png" />

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the _+ Variant_ button to add multiple variants based on a user property value. In the example below, we have used the _Language_ user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language.

<Image align="center" alt={2320} border={true} caption="Message Variant by User Property" title="Upto 50 Message Variants" src="https://files.readme.io/3d9b2da-hindi_sale.png" />

## Define the Web Pop-up Message Content

After you select a particular message type, you need to choose a template. CleverTap supports four types of templates for Web popup creation - _Basic_, _Ratings_, _Lead Generation_,  _Custom HTML_, and Drag & Drop Editor template.

<Image align="center" alt="Web Popup Template Types" border={true} caption="Web Popup Template Types" src="https://files.readme.io/cc4878c-webpopup_template_drag_and_drop.jpg" />

## Web Pop-up Editor

Select the templates and create a message. For more information on the  Web Pop-up Editor, see [Web Pop-up Editor](https://docs.clevertap.com/docs/web-pop-up-editor) .

### Preview

Once you are all done setting up the content of your Web Popup campaign in the _What_ section, you have the option to preview how your popup would look to your end-users.

Click **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the _Start date and time_ and _End date and time_. You also have the option to start a campaign immediately by selecting _Now_.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on _Done_, the campaign will be triggered and terminated as per the defined timings.

<Image align="center" alt={1904} border={true} caption="Campaign Schedule" title="Define When the Campaign is Sent" src="https://files.readme.io/429532e-when.png" />

### Delivery preferences

#### Web Campaign Priority

A user may qualify for multiple web popup campaigns simultaneously. In this case, you may want to prioritize the web popup that provides the highest business value.

Example:

A Fintech website may want to show web popups to its users for credit cards, car loans, and also personal loans. The business team considers that credit card sales provide higher returns than other offers. In this case, you can assign a higher priority to the web popup campaigns for credit cards.

<Image align="center" alt="Define Campaign Priority for Web Popup" border={true} caption="Define Campaign Priority" src="https://files.readme.io/a7a6a05-campaign_priority.jpg" />

The _Web Campaign Priority_ option enables you to set priority levels from 1 (lowest) to 100 (highest), with 1 being the default priority. Configuring Web Campaign Priority allows you to prevent priority conflicts, particularly for campaigns configured on the same triggers.

_Example_:  
Consider a scenario where two Web Popup campaigns are triggered on the _Add to cart_ event  campaign A with priority 8 and campaign B with priority 10. Both campaigns qualify per the defined trigger; however, end users will receive campaign B because the priority level is higher.

> 📘 Web Popup Campaign with Same Priority
>
> If two campaigns have the same trigger and campaign priority, any one of the campaigns may be displayed.

#### Triggers for Campaign Delivery

Triggers are conditions that determine when to show a web popup campaign to a user. You can activate the campaign based on actions,  such as user qualification, inactivity, scrolling behavior, or detecting when the user is about to leave the page. You can select one or multiple triggers, and the campaign is delivered as soon as any selected trigger condition occurs. This helps you streamline your marketing strategy.

<Image align="center" alt="Triggers for Campaign Delivery" border={true} caption="Triggers for Campaign Delivery" src="https://files.readme.io/1b6924a-Delivery_preferences_web_triggers.jpg" />

You can leverage either or all of the following triggers:

* **As soon as user qualifies**:
  * The campaign message is triggered immediately once the user meets the campaign criteria.
* **Specific Trigger:**  
  This option lets you set specific conditions to display the message popup. Select from any of the following triggers:
  * **After qualification, send in:**  
    The campaign is triggered after a specified delay once the user qualifies. You can set the number of seconds to wait before showing the popup.
  * **If inactive for:**  
    The campaign is triggered if the user does not interact with the page for a set duration. You can set the number of seconds of inactivity.
  * **Scroll percentage:**  
    The campaign is triggered when the user scrolls down beyond a certain point on the page. You can set the percentage of the page the user must scroll to trigger the campaign.
  * **Exit intent (about to leave page):**  
    The campaign is triggered when the system detects the user is about to leave the page. This is often used for exit-intent campaigns.

You can choose one or multiple triggers from the options provided. If multiple triggers are selected, the campaign is delivered as soon as the first trigger occurs.

#### Set Frequency

You might not want a campaign to run actively in certain scenarios on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the _Exclude from campaign limits_ option from the dropdown or choosing the appropriate cadence on how often to send your campaign.

<Image align="center" alt={1298} border={true} caption="Delivery Preferences" title="Changes Based on Segment Selection" src="https://files.readme.io/dcab498-DP.png" />

> 📘 Global Session Limits
>
> In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x'  web popup campaigns, and even the same web popup campaigns are counted.
>
> As per CleverTap's web SDK, for versions below `2.0.0`, for a given web popup campaign, it will only be shown once per session. With version `2.0.0` you can configure the amount of times you want to show it in a session.

#### Campaign frequency limits and display rules

This feature offers the additional flexibility of specifying the frequency at which the Web Pop-up campaign is delivered based on a defined trigger count.

Example:  
Consider a scenario where you want to configure a Web Pop-up campaign to:

* Display once per session
* Display thrice per week
* Show a maximum of five times throughout its duration
* Trigger when a user performs a specific action multiple times (such as _adding to cart_ three times in a session)

In this case, the message will be delivered once per session and thrice per week but will stop showing once the user has received it five times. Additionally, for event-based triggers, the message can be configured to appear exactly when the user performs the action a specified number of times. In this case, the message will be delivered exactly when the user completes adding to cart thrice in one session. Alternatively, you can select **every** or **exactly** display conditions based on your business requirements.

> 📘 Display Rules for Time-Based Frequency
>
> * If the Times in Frequency is set in days or weeks, the message is displayed according to the calendar day or week.
> * However, if the frequency is set in days or weeks, the message delivery is not considered as per the calendar week. For example, if a campaign is set to display 5 times in a week, it will be shown up to 5 times over the last 7 days.
> * If SDK version on your website is lower than `2.0.0`, then messages will be delivered 1 time per session for following cases:
>   * If value entered in any field is above 1.
>   * If multiple limits are added.
>   * If unit of time is seconds, minutes, hours, or weeks.
> * If SDK version on your website is lower than `2.0.0`, then:
>   * For display when trigger occurs, users will not qualify if value entered is above 1.
>   * _exactly_ operator will work the same as _every_ operator.

<Image align="center" alt="Campaign frequency limits and display rules" border={true} caption="Campaign frequency limits and display rules" src="https://files.readme.io/743efab0ed196318073f00fb21490968b53bffc1d2e3b187e1ade40546b5ef2f-web_pop-up.png" />

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image align="center" alt={1193} border={true} caption="Publish Campaign" title="Publish Final Campaign" src="https://files.readme.io/b521e92-campaign_Publish.png" />

# Assigning Priorities for Web Pop-up Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, if multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown.

To assign the priority:

1. Navigate to the Campaigns dashboard and select the specific campaign from the campaign list.
2. Click the Web priority marker icon below each campaign to open the priority list.

<Image align="center" alt="Assign Priority to Web Pop-up Campaign" border={true} caption="Assign Priority to Web Pop-up Campaign" src="https://files.readme.io/cc78f53c50ff995b73151f6d1c8f508c46ffd4c45dcf24865f9adc6451567737-Web_Pop-up_Priority.png" />

Set the priority as per your choice and click _Save_.

<Image align="center" alt="Priority List for Campaigns" border={true} caption="Priority List for Campaigns" src="https://files.readme.io/b18d568435064f0c3acdf49a44cc430de2fa5be7b77c4bb24c06d2ebf1c11ea4-image.png" />
