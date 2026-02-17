---
title: Create Message
excerpt: Understand how to create a campaign for Google Ads
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

Create a campaign to deliver your Google Ads message.  
To create a new campaign:

1. From the CleverTap dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **Google Ads**.

<Image align="center" alt="Create a New Google Ads Campaign" border={true} caption="Create a New Google Ads Campaign" title="New Google Ads Campaign Creation Page" src="https://files.readme.io/aa80e95a72ae328b129a287bb5d22214794ec9a59461786d250b99fa8cf2a72c-google_adds.png" />

The _Campaigns_ page displays.

<Image align="center" alt="Google Ads Campaign Configuration Page" border={true} caption="Google Ads Campaign Configuration Page" title="Configure Google Ads Campaign" src="https://files.readme.io/1e69901-New_Google_Ads_Campaign.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The _Start here_ section displays the setup information.

This section has the following parts:

* Start here: Displays the information for the Google Ads platform account integration. Check that the required platforms are integrated and ready for campaigns. When the account set up is not done, the following warning message is displayed and you need to set up the account to be able to run campaigns:

<Image align="center" alt={2670} border={true} caption="Start the Google Ads Account Setup" title="Start Configuring the Google Ads Account Setup" src="https://files.readme.io/91067c7-Account_Setup_not_done.png" />

When the account setup is done, the following message is displayed and you can now create a campaign:

<Image align="center" alt={1510} border={true} caption="Google Ads Account Setup Completed" title="Google Ads Account Setup Completed" src="https://files.readme.io/597d0f3-Account_Setup_done.png" />

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. You can define your conversion goal further by filtering an event by event properties. This selection is optional.

  The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced for purchasing an X amount?_ to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ".

<Image align="center" alt={919} border={true} caption="Goal Conversion Tracking" title="Goal Conversion Tracking" src="https://files.readme.io/00215dc-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your Ads campaign. You can specify your target audience from the _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list.

For Past Behavior segments, you also calculate the _Estimated reach_.

<Image align="center" alt={961} border={true} caption="Segment Your Target Audience" title="Define Your Target Audience" src="https://files.readme.io/5a435b7-SMS_Who.png" />

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your Ads campaign. You can create the target based on past user behavior and user properties.

On this basis, you would then set up the _Who_ by choosing to send this campaign to all users who qualify or just a portion of the users who qualify under _Estimated reach_.

### Deliver Ads Notifications based on Past Behavior (PBS)

You can also target users their past user behavior. For past behavior campaigns, you also have an option to calculate _Estimated reach_. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria.

For example, you can send an Ads notification to English-speaking female users who live in the United States.

<Image align="center" alt={516} border={true} caption="Filter by User Properties" title="Filter by User Properties" src="https://files.readme.io/5851a66-campaigns_user_properties.png" />

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
        App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app, which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segmentation).

## Define the Message Content

Now, you can set up the _What_ section, that is, you can select the audience to which you want to export the user details.

### Ads Editor

You can either append an existing audience list **or** create an audience list. Select the user details such as Email or Phone that you want to upload to this list.

#### **Add qualified users using CleverTap**

> 🚧 Note
>
> Check that you have available CRM lists before adding users.

<Image align="center" alt="Configure Audience Type In What Section" border={true} caption="Configure Audience Type In What Section" title="Configure Audience Type" src="https://files.readme.io/909c65b-Google_Ads_-_What.png" />

#### **Create a new audience on Google using CleverTap**

<Image align="center" alt={978} border={true} caption="Create a New Audience on Google Using CleverTap" title="Select Create a New Audience on Google Using CleverTap Option" src="https://files.readme.io/082ca9c-Campaign_Adwords_What_create_audience.png" />

## Define the Campaign Schedule

You can set up the _When_ to schedule the campaign start and end using the options below:

The delivery preferences for Google Ads campaigns can be set as follows:

* Send Now: Select this option to send the campaign right away.
* Schedule for later: Select this option to send the campaign on a specific date and time.
* Set as Recurring: Select this option to send the campaign at specific intervals.

<Image align="center" alt="Define Campaign Schedule." border={true} caption="Define Campaign Schedule." src="https://files.readme.io/a463e2c-when.png" />

<br />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.

<Image align="center" alt={1193} border={true} caption="Publish Campaign" title="Publish Campaign" src="https://files.readme.io/b521e92-campaign_Publish.png" />
