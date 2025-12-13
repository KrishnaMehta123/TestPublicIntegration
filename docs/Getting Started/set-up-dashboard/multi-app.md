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

> 📘 Enable Multi-App For Your Project
>
> You can only add multiple apps if the multi-app feature is enabled for your project. To enable this feature, contact your Customer Success Manager.

To add an app:

1. Go to *Settings* > *Project* and select the *App* tab.
2. Click **Add App**. After adding the app, configure Mobile Push for each platform your app supports on your CleverTap dashboard to use the multi-app feature.

   <Image alt="Mobile Push Integration for your App" align="center" border={true} src="https://files.readme.io/c68cd4b-Mobile_Push_Integration_For_Your_App.gif">
     Mobile Push Integration for your App
   </Image>

You can identify the event from an app by the event property. For example, if you have multiple apps called ctDemo, ctDemo1, ctDemo2, and so on. To distinguish the ctDemo1 from the other apps, you can use the event property called *CT App Name*. This property registers the name of the original app, such as ctDemo. You can then select the required app from the app list during campaign creation, as shown in the following image:

<Image alt="Target Segment Based on Property Name CT App Name" align="center" border={true} src="https://files.readme.io/62c3cf7-Cross-App_Segment_Targeting_.png">
  Target Segment Based on Property Name CT App Name
</Image>

> 📘 Integrate App and Attribute Events
>
> Use the *AppID* available under *Settings* > *Project* > *Apps* as the *Account ID* when integrating your app with the CleverTap SDK. This ensures that all events coming from the App are uniquely identifiable and can be correctly attributed to the App. For more information on integrating your app, refer to the following guides:
>
> * [Android Quickstart Guide](https://developer.clevertap.com/docs/android-quickstart-guide)
> * [iOS Quickstart Guide](https://developer.clevertap.com/docs/ios-quickstart-guide)

# Engage with Users Across Apps

Once your apps are added, profiles are created, and events begin flowing into CleverTap, you can start creating Campaigns to engage and target users across different apps. 

To create a campaign using the Multi-app feature:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. Select the messaging channel from the Messaging Channels list, and the campaign page will appear.

<Image alt="Create Campaign" align="center" border={true} src="https://files.readme.io/ba0f9d4-image.png">
  Create Campaign
</Image>

> 📘 Supported Channels
>
> The feature is available for Push Notifications and App Inbox in Campaigns and Push Notifications, App Inbox, and In-App Messages in Journeys. Channels like email and SMS are not supported because their delivery is based on the user's unique phone number or email ID, which remains the same across apps.

4. [Set up the campaign](doc:multi-app-setup#set-up-campaign).
5. Define the audience for your campaign.
6. Draft your campaign. Refer to the respective messaging channel documents to create your campaign message.
7. Define the schedule for your campaign and publish your campaign.

## Set Up Campaign

You can set up your campaign from the *Start here* section of the campaign page. Before moving ahead, ensure the required platforms are integrated and ready for campaigns.

#### Qualification Criteria

Setting up a multi-app campaign is simple. After selecting the messaging channel, select the type of campaign from the *Qualification Criteria* section.

#### Set a Goal

Setting a goal is optional. It allows you to measure your campaign effectively. You can define your conversion goal further by selecting the Event and Conversion time.

The campaign goal can be as generic or as specific as you want. It can answer questions such as "How many users were influenced to purchase an X amount?" or "How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ".

#### App for this campaign

Select the app for which you want to send the campaign. For example, the business operates both a music app and an OTT app and wants to target users who are active in the music app A2Z Music but do not have the OTT app A2Z TV, encouraging them to explore or engage more with the A2Z TV app based on their behavior in the music app. In this case, they will select the OTT app for this field.

<Image alt="Select the App to Send the Campaign" align="center" border={true} src="https://files.readme.io/9694ccf33e1ccd4570b623ad0467e5d46bd15699f4c74b612256d1c7a0e06292-select_app_to_send_campaign.png">
  Select the App to Send the Campaign
</Image>

## Define Audience

 Under the *Who* section, you can select your targeting criteria for the users you want to send the campaign. To send the campaign to users from other apps, you filter the target audience based on the *CT App Name* event property. 

> 📘 Uploading Events via API
>
> The *CT App Name* event property is not received when uploading events via API.

Let us consider the same example where the business has the following two apps: a music app named A2Z Music and an OTT app named A2Z TV. To target music app users to sign up for their OTT platform, filter the target audience as shown in the following image:

<Image alt="Select Target Audience" align="center" border={true} src="https://files.readme.io/878258a-image.png">
  Select Target Audience
</Image>

# Analyze Data Across Apps

You can analyze data for events across the platforms. To do so: 

1. Go to Analytics > Events from the CleverTap dashboard.
2. Select the event and click **View Details**. 
3. Scroll down to the Event property section and select *CT App Name* from the list as shown below: 

<Image alt="Analyze Data Across Apps" align="center" border={true} src="https://files.readme.io/f348dd3-Analyze_Data_Across_Apps.gif">
  Analyze Data Across Apps
</Image>
