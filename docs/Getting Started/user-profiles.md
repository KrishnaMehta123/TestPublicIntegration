---
title: User Profiles
excerpt: ''
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

After integrating our SDK, the platform creates a user profile for each person who launches your app or visits your website.

<Image title="View User Profile Details" alt={1423} align="center" border={true} src="https://files.readme.io/fb9b378-1_User_Profile.png">
  User Profile
</Image>

A CleverTap user profile has a set of default fields, such as email, phone number, and language. You can also extend the default user profile by adding custom fields that are specific to your business. 

> 👍 Custom Profile Field Example
>
> If you offer a subscription service in your app, you can create a custom profile field to track what type of plan the user purchased.

<Image title="View User Properties" alt={685} align="center" border={true} src="https://files.readme.io/908f59f-2_User_properties.png">
  User Properties
</Image>

The benefit of adding more information to a CleverTap user profile means the ability to:

* Create a user segment for people who have a specific profile property you have defined, then build a campaign to engage with that segment. 
* Personalize your campaign messaging with information. 
* [Personalize your app](https://developer.clevertap.com/docs/app-personalization) based on information from that person's CleverTap user profile.

# User Profile Data Model

A CleverTap user profile consists of three parts:

* Identifiers: Each user profile is given a unique CleverTap ID. You can also add other identifiers to recognize the user including email, phone number, Facebook ID, or your own custom identifier.
* Properties: This is information stored about the user such as age, gender, device, and location. You can also extend the default user profile by adding custom fields that are specific to your business. 
* Events: This is a log of actions taken by a user in your app such as a product viewed, a video watched, or an item added to cart.

## User Profile Types

The CleverTap user profile type changes automatically depending on the information set in them. A user profile can only belong to one type.

* Anonymous: Anonymous profiles do not contain uniquely identifiable information about the user.
* Identified: Identified user profiles (also referred to as addressable profiles) can be reached either via email or push notifications. They contain uniquely identifiable information such as email or user ID.

### User Scenarios for Anonymous Profiles

When tracking anonymous profiles, CleverTap tries to retain guest events as much as possible. The following scenarios explain how anonymous profiles are logged in the system. 

**Scenario 1**\
Anonymous user X performs event A from desktop A > Logs in > Performs event B.

**Scenario 2**\
The same user now uses a separate browser and performs event A anonymously > Logs in (as the same user) > Performs event B. Event B will be mapped to this user X. 

In scenario 2, all the events done before the user identifies themselves are mapped to an anonymous profile. All events post login is mapped to user X and is visible on the profile. As a best-case scenario, the platform shows all the events on the same user X except that any events done in an anonymous mode are shown in gray; these grayed-out events will not be considered for analytics or segmentation. The events before the login event will not be remapped to user X because they are done in an anonymous mode.

Since the user has performed the events anonymously, we consider this user as a different user, even though, this is mapped to an already existing identified profile.

# Updating the User Profile

Adding user properties to your user profiles can help you enrich your user information, segment your audience better, and hyper-personalize your messages. CleverTap provides different methods to update user profile properties. By leveraging these methods, businesses can effectively engage with users and drive growth. The following are the different ways to update user profile properties on the CleverTap dashboard:

* [Update User Profile via SDK](doc:user-profiles#update-user-profile-via-sdk)
* [Update User Profile via API](doc:user-profiles#update-user-profile-via-api)
* [Upload CSV File](doc:user-profiles#upload-csv-file) 
* [Import User Profiles via SFTP](doc:user-profiles#import-user-profiles-via-sftp)
* [Track an Event from the SDK](doc:user-profiles#track-an-event-from-sdk)

## Update User Profile via SDK

You can use the CleverTap SDK to update user profiles and enrich the profile further to send personalized campaigns. The `Onuserlogin` method is used to identify individual users on a device. However, if additional user properties such as gender and date of birth are required, the profiles can be updated using the `profilePush` method.

For more information, refer to [Update User Profile via SDK](https://developer.clevertap.com/docs/concepts-user-profiles#updating-the-user-profile).

## Update User Profile via API

You can also update user profile properties using CleverTap's RESTful API. The API allows you to update user profiles and supports updates at scale. To do so, use the CleverTap API to update the user profile property. The CleverTap server receives the update and applies it to the respective user profile.

For more information, refer to [Upload User Profile API](https://developer.clevertap.com/docs/upload-user-profiles-api).

## Upload CSV File

This feature helps update user profile properties in bulk at once. CSV upload is a manual process that requires the user to upload the data directly from the local system to the CleverTap dashboard in CSV format.

To learn more, refer to [CSV Upload](doc:csv-upload).

## Import User Profiles via SFTP

With CleverTap's Imports via SFTP feature, you can update user profile properties by importing the file to the SFTP server. SFTP import is an automated process that helps update user profile properties at regular intervals, such as daily or weekly updates, without manual intervention.

To learn more, refer to [Imports via SFTP](https://developer.clevertap.com/docs/imports-via-sftp).

## Track an Event from SDK

With CleverTap events, you can track all individual actions users perform in your app or website. After the event is triggered, the user profile is automatically updated with the latest property value. The CleverTap server receives the event and updates the user profile property.

For more information, refer to [Update User Profile](https://developer.clevertap.com/docs/events#custom-events).

# Mark a User Profile as a Test Profile

CleverTap provides a test user profile feature to update the user profile to a test profile. This feature helps with the following:

* Test messages (including personalized messages) before sending them to the target audience
* Test user segmentation

To mark a particular user profile as a test profile:

1. Select the required profile from the *Find People* page.
2. Select *Mark as test profile* from the *Profile* page.

<Image title="Mark a User Profile as a Test Profile" alt="Mark as Test Profile" align="center" border={true} src="https://files.readme.io/ede8cf9-Test_Profile.png">
  Mark as Test Profile
</Image>

When we mark the user profile as a Test profile, the CleverTap server receives the event and updates the user profile with an additional property, `ct_is_test_user`, with the value `Yes`. The `ct_is_test_user` property is of type String.

## Exclude Users from the Control Group

You can exclude specific users from being placed into a control group by marking them under the **Exclude user from all control groups** setting in their user profile.

This setting ensures that the selected users are always included in campaigns and never placed in control groups for A/B tests or split delivery experiments.

> 📘 Limit
>
> You can exclude up to 20 profiles using this setting.

This feature ensures that certain high-priority users or test accounts receive all campaign variations without exclusion.

<Image alt="Exclude Users from Control Groups" align="center" width="50% " border={true} src="https://files.readme.io/592b966226b6bc53ffcfb96a69570c8b9cd3b51efd3466b287fd474ebaaf8f04-image.png">
  Exclude Users from Control Groups
</Image>

# System User Properties

System user properties are derived from the user information received from your application after integrating CleverTap SDK.

<Image title="View System User Properties" alt={1188} align="center" border={true} src="https://files.readme.io/722dc07-Test_user_Segments.png">
  System User Properties
</Image>

The following are the system user properties available in CleverTap:

* Name
* Email
* Identity
* Phone
* Gender
* DOB
* Timezone
* MSG-email
* MSG-push
* MSG-sms 
* MSG-whatsapp

> 📘 Calculating Age
>
> If the `birthday` or `DOB`is available as a profile property, CleverTap automatically calculates the age for the user profile.

Using *Age* you can create and target segments, such as all users between 25 to 30 years.

<Image title="Target User Properties and Click View Details" alt={1934} align="center" border={true} src="https://files.readme.io/63927fe-Screenshot_2019-10-22_at_6.26.26_PM.png">
  Target User Properties
</Image>

# FAQs

This section provides answers to some commonly asked questions about User Profiles.

### Q. What is the difference between a User not reachable and a Profile not reachable error?

A. These errors mean the following:

**User not reachable**: This error is raised when the qualifying device is unreachable on the selected communication channel. For example, if a user performs a qualifying action on the web for a mobile push live campaign.

**Profile not reachable**: This error is raised when the qualifying profile is not reachable on the selected communication channel. For example, a user blocks push notifications on iOS but qualifies for a campaign. This user does not receive the campaign and is marked as a profile not reachable.

### Q. What is a Duplicate Platform ID error?

A. The *Duplicate Platform ID* error occurs in one of the following scenarios:

* When a single token is assigned to multiple profiles, both profiles qualify for the campaign. CleverTap sends the notification to the profile that qualifies first, and the other profile is marked as a *Duplicate Platform ID*.
* When the same mobile number is assigned to multiple profiles, they qualify for the campaign. Only one profile receives the notification; the other profiles are marked as a *Duplicate Platform ID*.
