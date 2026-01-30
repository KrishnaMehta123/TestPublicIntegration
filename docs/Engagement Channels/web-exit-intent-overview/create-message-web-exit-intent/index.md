---
title: Create Message
excerpt: Learn how to create a Web Exit Intent campaign using the CleverTap dashboard
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Web Exit Intent Campaign

To create a new Web Exit Intent Popup campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **Web Exit Intent**.

<Image align="center" alt="Select Messaging Channel" border={true} caption="Select Messaging Channel" title="Campaign Button Lists All Channels" src="https://files.readme.io/433cc61458805652a698e4754aeea242d2a12fade8b8da3471cb9b8ddfe45056-wepuchs.png" />

The campaign page displays.

<Image align="center" alt={976} border={true} caption="Create Campaign" title="Expand Each Section" src="https://files.readme.io/03e2e61-Web_exit_intent_editor_main.png" width="80%" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The _Start here_ section displays the setup information.

* **Set a goal**: Tracks your campaign conversions by setting a goal. This step is optional, but it helps you measure how effectively your campaign meets its goal.  
  You can define your conversion goal by selecting the _Event_ and specifying the _Conversion Time_. The _Conversion Time_ field accepts any numeric value along with a time unit such as Minutes, Hours, Days, Weeks, or Months. This allows you to define conversion windows such as 10 days, 72 hours, or 2 months. The value can range from a minimum of 1 minute to a maximum of 5 months.  
  For example, if you set the conversion time to 5 Minutes, the system counts conversions within 5 minutes of the goal event.  
  Your campaign goal can be as broad or as specific as you want. For example, you can answer questions such as: _How many users were influenced to purchase an X amount?_ or _How many first-time visitors purchased red shoes worth at least X and blue jackets worth at least Y?_

<Image align="center" alt="Set Conversion Time" border={true} caption="Set Conversion Time" src="https://files.readme.io/d960f90056d978b5c9f8832e66c2b3c15b6e387d3caa38ea6bc0b138c57d6b29-Conversion_Tracking.png" width="75% " />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the segment list.

<Image align="center" alt={964} border={true} caption="Define Target Segment - Who" title="Define the Target Segment" src="https://files.readme.io/bf4a5f0-campaign_Who_Live_segment.png" />

Campaigns can be set up as follows:

* Single action: User does an action on one of your web pages.
* Page visit: User visits one of your specific webpage URLs.
* Page referral: User visits your website via any specific referral URL.
* Page count: Number of your web pages a user has visited so far in their session.

### Deliver Action Based Web Exit Intent Notifications

You can trigger a web exit intent popup based on an action. For example, a web exit intent popup with an irresistible discount voucher can be shown to a set of customers who have just viewed a specific product page. This will help in incentivizing an existing customer. Moreover, such exit intent popups make notifications more contextual and result in increased conversion.

### Deliver Messages based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you can show a web exit intent popup to customers who had recently added products to the cart but didn't complete the purchase.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria.

For example, you can send a web exit Intent popup to customers from **Mumbai** who have added items to the cart but didn't complete the transaction in the past 10 days.

<Image align="center" alt={2242} border={true} caption="Filter by User Properties" title="up.png" src="https://files.readme.io/0141dfe-up.png" />

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
        Geography Radius
      </td>

      <td>
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.
      </td>

      <td>
        Locations = San Francisco, USA; Paris, France
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

To know more about what segments can be used, see [Segments](doc:segments).

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

<Image align="center" border={true} caption="Calculate Estimate Reach" src="https://files.readme.io/3729719638ae87877e293f4392593f4eec3ad53701e9d6e97dbd083893b08dee-2026-01-30_19-12-06_1.gif" width="85% " />

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image align="center" alt={1480} border={true} caption="Control Group" title="Control Group and Targeting Cap" src="https://files.readme.io/fd0d08b-cg.png" />

## Web Exit Intent Pop-up Message Types

You can create the following types of messages for your web exit intent pop-ups:

* Single Message
* AB Test
* Split Delivery
* By User Property

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best in the pop-up to get users' clicks.  
You can test up to three pop-up message variants on a test group. The variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

<Image align="center" alt="A/B Test Variant Distribution" border={true} caption="A/B Test Variants" src="https://files.readme.io/a575c38-B_Test_Variant.png" />

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the campaign's duration.

<Image align="center" alt={2322} border={true} caption="Split Delivery Variant Distribution" title="Control Variant Distribution" src="https://files.readme.io/90063a5-split_delivery_web_exit.png" />

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, click **+ Variant** to add multiple variants based on a user property value. You can send up to 50 message variants to different users based on a user property. In the example below, we have used the _Language_ user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language (English, Hindi, etc.)

<Image align="center" alt={2324} border={true} caption="Message Variant by User Property" title="Upto 50 Message Variants" src="https://files.readme.io/33b57c0-User_property_exit_intent.png" />

## Define the Message Content

After you select a particular message type, you need to choose a template. CleverTap supports two types of templates for web exit intent pop-up creation:

* **Interstitial** -  It's a center-aligned pop-up mainly used for driving better engagements. The image below represents the editor for a sample Interstitial template.

<Image align="center" alt={2564} border={true} caption="Interstitial Message" title="Create, Preview and Personalize Interstitial Message" src="https://files.readme.io/f98671a-web_exit.png" />

For web exit intent pop-ups, you can specify a button with text. Upon a web pop-up click, you can either do nothing, open a link, or invoke a JavaScript function.

* **Custom HTML**  - Here the marketers have a choice to customize their exit intent pop-up's appearance for the Interstitial template. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor.

> 🚧 Manually Configured Click Tracking?
>
> If you are already raising the Notification Clicked event manually in your template, then ensure to disable the  _Enable click tracking for Custom HTML_ checkbox to avoid overcounting.

To track the campaign stats such as the number of total clicks and CTRs, marketers need to ensure that they check mark the _Enable click tracking for Custom HTML_ checkbox.

<Image align="center" alt={1528} border={true} caption="Track Campaign Stats" title="Disable if Clicks Recorded Manually" src="https://files.readme.io/2c23c02-Screenshot_2022-10-07_at_6.21.52_PM.png" />

## Define the Campaign Schedule

Each web exit intent campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the _Start date and time_ and _End date and time_. You can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on _Done_, the campaign will be triggered and terminated as per the defined timings.

<Image align="center" alt={1904} border={true} caption="Campaign Schedule" title="Define When the Campaign is Sent" src="https://files.readme.io/0b43104-when.png" />

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the _Exclude from campaign limits_ option from the dropdown or choose the appropriate cadence on how often to send your campaign.

<Image align="center" alt={1298} border={true} caption="Delivery Preferences" title="Changes Based on Segment Selection" src="https://files.readme.io/bf4c04a-DP.png" />

## Publish Campaign

* After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image align="center" alt={1193} border={true} caption="Publish Campaign" title="Publish Final Campaign" src="https://files.readme.io/b521e92-campaign_Publish.png" />

# Assigning Priorities for Web Exit Intent Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown.

To assign the priority:

1. Navigate to the _Campaigns_ dashboard and select the specific campaign from the campaign list.
2. Click the _Web priority_ marker icon below each campaign to open the priority list.

<Image align="center" alt="Assign Priority to Web Popups" border={true} caption="Assign Priority to Web Popups" title="Define the Order of Popup Display" src="https://files.readme.io/cd3b8255c7a3b8f95619daebc2c75b09e2b3481f9786b92933738bd40e4d65de-priotrity.png" width="auto" />

Set the priority as per your choice and click **Save**

<Image align="center" alt="Priority List" border={true} caption="Priority List" title="Select Web Popup Priorty" src="https://files.readme.io/84809ccd683476fc6a595be30d4f0428170cb4300169b8939e5959c70ed6099f-low_hight.png" width="100%" />
