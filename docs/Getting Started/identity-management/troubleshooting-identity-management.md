---
title: Troubleshooting Identity Management - WIP
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

This section will help you with troubleshooting identity management issues.

# Identity Lifecycle \<\<@saby, can we make a table out of this for our internal users on the KB ?>>> This already exists in the system events documentations-> Not needed here

\-- Identity Set  
Dropped History (true,false)  
ID ( value of identity )  
Source ( SDK, API)  
Type ( New User, Merged, Appended )  
-- Identity Error  
ID ( value of identity )  
Source ( SDK, API)  
-- Identity Reset  
ID ( value of identity )  
Source ( SDK, API)

# Identity Protection

![](https://files.readme.io/ea711dc-Identity_Protection.png "Identity Protection.png")

# How to Validate Identity Management \<\<@saby can we use this in the [identifcation methods](https://docs.clevertap.com/docs/identification-methods) docs ? ?>> yes

![](https://files.readme.io/748f314-1_audit.png "1 audit.png")

## Marketer Audit \<\<@saby, should we add this to our identity management docs to check if the identity is indeed being pushed to the CT dashboard?>> In the this needs to be explained to the marketer it would be ideal if we can simplify and make it less verbose

If you don't have access to the tools, you can simply leverage the CleverTap dashboard to perform the same  
validation. Confirm with your tech team the identity that the identity is being pushed to CleverTap on Login/Registration.  
It can be your database identity or an email address.  
Simply login/register into the app. Now using the identity/email you can search for the user profile in the CleverTap dashboard to validate the events/user properties being pushed.

![](https://files.readme.io/035da46-5_Marketer_Audit1.png "5 Marketer Audit1.png")

It will load the User Profile.

![](https://files.readme.io/9d98815-5_Marketer_Audit2.png "5 Marketer Audit2.png")

# Developer Audit \<\<@saby can we add this to the developer docs in Android profiles ?>> -No, this is already there. 

This will require a developer audit for Android & iOS and then a test from the CleverTap dashboard.

## Android

Add the following code snippet to your Application/Delegate class :

- Android - `CleverTapAPI.setDebugLevel(1277182231)`

### Android Debug Log

For Android, the logs will be visible in the Android Studio Logcat.  
After you run the application with the code snippet, the Logcat window of Android Studio will allow you to see all the events trigger in real-time.

![](https://files.readme.io/0748f90-2_android1.png "2 android1.png")

To find the same profile in the CleverTap dashboard, you can simply fetch the "g"(CleverTap ID) value available in logs. Enter this CleverTap ID in the CleverTap dashboard under _Segment_ > _Find People_.

![](https://files.readme.io/b9dd683-2_android2.png "2 android2.png")

## iOS \<\<@saby can we add this to the developer docs in iOS profiles ?>> No this should not be done, as once the SDK team updates the verbose logs you would have to keep updating the screenshot. It is better we mention that it would be seen in the verbose section

Add the following code snippet to your Application/Delegate class:

- iOS - `CleverTap.setDebugLevel(1277182231)`

### iOS Debug Area Logs

![](https://files.readme.io/31e10d3-3_iOS_Debug_Area_Logs.png "3 iOS Debug Area Logs.png")

## Audit from CT Dashboard \<\<@saby can we use this information somewhere ?>> Yes, we can use our segmentation section to explain better about our query builder and there we can cover this aspect as well

Go to Segments -> Find People and search for the ‘g’ value to find your Profile page.

![](https://files.readme.io/8695c97-4_Steps_in_CT_Dashboard1.png "4 Steps in CT Dashboard1.png")

This will redirect you to a CleverTap profile wherein you will find the events and user properties

![](https://files.readme.io/712fe9d-4_Steps_in_CT_Dashboard2.png "4 Steps in CT Dashboard2.png")