---
title: Multi-App Setup
excerpt: >-
  Learn how to set up multiple apps and engage with users across these apps on
  the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Managing several mobile apps is becoming increasingly important for modern businesses catering to diverse customer bases. For example, Global Mart, an e-commerce company, has distinct apps for each country it serves, offering a personalized shopping experience based on geographical dynamics and local references. With the Multi-app feature, Global Mart can effortlessly interact with users and analyze data from multiple countries.

# Set Up Multiple Apps

You can now add multiple apps under a single project. This feature is handy when a single marketing team manages multiple apps, as it enables cross-app targeting. For example, you can target users in a music app based on their interactions with a movie app.

[Create a project](doc:project-setup#create-a-project) quickly after logging on to CleverTap to add multiple apps.

> 📘 Private Beta
>
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Customer Success Manager.

To add an app:

1. Go to _Settings_ > _Project_ and select the _App_ tab.
2. Click **Add App**. After adding the app, configure Mobile Push for each platform your app supports on your CleverTap dashboard to use the multi-app feature.

   <Image align="center" alt="Mobile Push Integration for your App" border={true} caption="Mobile Push Integration for your App" src="https://files.readme.io/c68cd4b-Mobile_Push_Integration_For_Your_App.gif" />

You can identify the event from an app by the event property. For example, if you have multiple apps called ctDemo, ctDemo1, ctDemo2, and so on. To distinguish the ctDemo1 from the other apps, you can use the event property called _CT App Name_. This property registers the name of the original app, such as ctDemo. You can then select the required app from the app list during campaign creation, as shown in the following image:

<Image align="center" alt="Target Segment Based on Property Name CT App Name" border={true} caption="Target Segment Based on Property Name CT App Name" src="https://files.readme.io/62c3cf7-Cross-App_Segment_Targeting_.png" />

> 📘 Integrate App and Attribute Events
>
> Use the _AppID_ available under _Settings_ > _Project_ > _Apps_ as the _Account ID_ when integrating your app with the CleverTap SDK. This ensures that all events coming from the App are uniquely identifiable and can be correctly attributed to the App. For more information on integrating your app, refer to the following guides:
>
> * [Android Quickstart Guide](https://developer.clevertap.com/docs/android-quickstart-guide)
> * [iOS Quickstart Guide](https://developer.clevertap.com/docs/ios-quickstart-guide)

# Engage with Users Across Apps

Once your apps are added, profiles are created, and events begin flowing into CleverTap, you can start creating Campaigns to engage and target users across different apps. You can select one, multiple, or all apps while creating a campaign.

To create a campaign using the Multi-app feature:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. Select the messaging channel from the Messaging Channels list, and the campaign page will appear.

<Image align="center" alt="Create Campaign" border={true} caption="Create Campaign" src="https://files.readme.io/ba0f9d4-image.png" />

> 📘 Supported Channels
>
> * The feature is available for Push Notifications and App Inbox in Campaigns and Push Notifications, App Inbox, and In-App Messages in Journeys.
> * If Copy to Inbox is enabled for a Push campaign:
>   * The message is sent as a push notification to all selected apps.
>   * The same message is also delivered to the App Inbox of each selected app.
> * Channels such as Email and SMS are not supported because their delivery is based on the user's unique phone number or email ID, which remains the same across apps.

4. [Set up the campaign](doc:multi-app-setup#set-up-campaign). Here, select one or more apps for delivery.
5. Define the audience for your campaign.
6. Draft your campaign. Refer to the respective messaging channel documents to create your campaign message.
7. Define the schedule and publish your campaign.

## Set Up Campaign

You can set up your campaign from the _Start here_ section of the campaign page. Before moving ahead, ensure the required platforms are integrated and ready for campaigns.

#### Qualification Criteria

Setting up a multi-app campaign is simple. After selecting the messaging channel, select the type of campaign from the _Qualification Criteria_ section.

#### Set a Goal

Setting a goal is optional. It allows you to measure your campaign effectively. You can define your conversion goal further by selecting the Event and Conversion time.

The campaign goal can be as generic or as specific as you want. It can answer questions such as "How many users were influenced to purchase an X amount?" or "How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ".

#### App for this campaign

Select the apps for which you want to send the campaign. You can:

* Select a single app
* Select multiple apps

By default, the dropdown is pre-filled with the default app to maintain backward compatibility. Once selected, the campaign is delivered to all chosen apps using the same configuration.

<Image align="center" alt="Select the App to Send the Campaign" border={true} caption="Select the App to Send the Campaign" src="https://files.readme.io/39b78486162fb47905958c368a0ff01f12a4cafd9632dce8226e7a0ebea2df20-2026-01-08_14-50-20.png" />

> 📘 Note
>
> You can select a maximum of 10 apps per campaign.

## Define Audience

Under the _Who_ section, you can select your targeting criteria for the users you want to send the campaign. To send the campaign to users from other apps, you filter the target audience based on the _CT App Name_ event property.

> 📘 Uploading Events via API
>
> The _CT App Name_ event property is not received when uploading events via API.

Let us consider the same example where the business has the following two apps: a music app named A2Z Music and an OTT app named A2Z TV. To target music app users to sign up for their OTT platform, filter the target audience as shown in the following image:

<Image align="center" alt="Select Target Audience" border={true} caption="Select Target Audience" src="https://files.readme.io/878258a-image.png" />

# Review and Publish

Before publishing, the campaign overview page displays all selected apps, and the campaign configuration applied to each app. After publishing, the campaign details page lists all apps where the campaign is live.

App selection cannot be changed after the campaign is published. To modify the selected apps, create a new campaign.

# Campaign Stats

For campaigns sent to multiple apps, performance metrics can be viewed cumulatively to see combined performance across all selected apps.

# Analyze Data Across Apps

You can analyze data for events across the platforms. To do so:

1. Go to Analytics > Events from the CleverTap dashboard.
2. Select the event and click **View Details**.
3. Scroll down to the Event property section and select _CT App Name_ from the list as shown below:

<Image align="center" alt="Analyze Data Across Apps" border={true} caption="Analyze Data Across Apps" src="https://files.readme.io/f348dd3-Analyze_Data_Across_Apps.gif" />
