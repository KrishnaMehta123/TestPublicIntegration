---
title: Handling Identities - WIP
excerpt: Understand how to select the approach to manage Identities.
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

You can handle the identified profiles per your requirements on the CleverTap dashboard. To do so, navigate to _Settings_ > _Identity_ from the CleverTap dashboard and open the _User Identity_ page.  

Answer the following questions based on your requirements:

- How do you want to identify logged-in users?
- How do you want CleverTap to handle identified profiles?
- Do you want to use ADID and IDFA as device identifiers?

# How do you want to identify logged-in users?

Select how to identify users. You can use the following identifier options to identify logged-in users:

- Email ID
- Mobile number
- Identity

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25bc2e0-Identity_Identity_logged_in_Users.png",
        "Identity_Identity logged in Users.png",
        884
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

> 📘 Note
> 
> We recommend that you select the user's Email ID to identify users.

# Handle identified profiles

We recommend that you do not merge identifiers on the same device. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/54af1bb-How_Do_You_Want_CleverTap_to_Handle_Identified_Profiles.png",
        "How Do You Want CleverTap to Handle Identified Profiles.png",
        932
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

## Do Not Merge Identifiers on the Same Service

This method is recommended for setting up identity management on CleverTap to ensure that multiple users are not merged on the same device. Even if multiple users perform the signup or login operation on the same device, their user data is stored on separate user profiles. To use this option, the `OnUserLogin` method can be used while integrating the SDK.

For example, this option can be used when there are different user profiles for the same OTT platform that could log in from the same desktop. 

This is the ideal and recommended scenario as it ensures the correct isolation of user data and helps track events more efficiently. 

To configure this setting, perform the following steps:

1. Navigate to _Settings_ > _User Identity_ from the dashboard.
2. Under the _How do you want CleverTap to handle identified profiles?_ section, select _Do not merge identifiers on the same device_. 

## Allow Multiple Identities to Merge on the Same Device

Only use this option if your business requires a singular profile to track all the multiple users logging in through the same device.

To use this option, the `ProfilePush` method is used invoked for any signup or login. This ensures that even if multiple users perform the signup or login operation on the same device, their user data is stored on the same user profile, created using the first user’s operations. This ensures that the data for multiple users is stored on the first user's profile.

This scenario differs for different businesses as it pushes all the user data of multiple users to CleverTap profiles. This could be implemented when only one user could use one device.

To configure this setting, perform the following steps:

1. Navigate to _Settings_ > _User Identity_ from the dashboard.
2. Under _How do you want CleverTap to handle identified profiles?_, select _Allow multiple identities to merge on the same device_. 

# Use Device Identifiers

The Advertising ID (ADID) is a unique,  user-defined ID for advertising provided by Google Play services. Similarly, Identifier for Advertisers (IDFA) is a unique code that Apple assigns to each iPhone for third parties to track users for ad targeting.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1e3b52-Do_You_Want_to_Use_ADID_and_IDFA_as_Device_Identifiers.png",
        "Do You Want to Use ADID and IDFA as Device Identifiers.png",
        766
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

## Use ADID and IDFA as Device Identifiers

Conforming to the latest privacy policies designed by Apple, the latest CleverTap iOS SDK does not capture IDFA or other device IDs, such as IMEI. The Identifier for Vendors (IDFV) is used to create a CleverTap ID which is disclosed under _Other Data_.

During integration, the CleverTap SDK can capture the Google Ad ID (GAID) and IDFV. 

The current GDPR policies do not allow using the GAID and IDFA to track user data. So if your app conforms with the GDPR policies, using the GAID or the IDFA as device identifiers is not recommended.

If the GDPR policies do not govern your use case and region, you can use GAID to capture the user information.

When you use the GAID for creating a Clevertap ID/Profile, they display as `__g<google ad id without special characters>`. For Google, this displays as `-g<IDFA>`.

The Identifier for Vendors (IDFV) is a code assigned to all apps by one developer and is shared across all apps by that developer on your device. The IDFV value is the same for apps from the same developer running on the same iOS-enabled device. This displays as `-v<IDFV>`.

The CleverTap iOS SDK does not track IDFA. CleverTap’s iOS SDK uses IDFV to track anonymous users from SDK version 3.9 and above.

You can use IDFV to collect user data from CleverTap SDK versions 3.9 and above.

## Use a Custom Device Identifier

By default, the CleverTap Android SDK does not use the Google Ad ID to generate CleverTap IDs. In this case, you can set your custom identifiers or allow CleverTap ID to handle the ID creation for user profiles.

If the app is required to be GDPR compliant or if you do not want to use the Google AdID, you can use the \_\_<Random Alphanumeric String> notation to generate the CleverTap ID. 

When creating the CleverTap ID using the custom identifier, the format is the following: 

- \_\_h<unique id> for Android
- \-h<unique id> for iOS