---
title: Identity Management Overview - WIP
excerpt: >-
  Understand the concept of identity, identity management, and its significance
  in CleverTap.
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

All the user data is always stored against a user profile. When a user profile is created, several attributes are assigned to a profile to uniquely identify or reference the user. These attributes or a combination of more than one can be used to identify the user uniquely.

# Identity Management

Identity management is defining your user information uniquely on the CleverTap dashboard by providing each user with a unique identifier. By uniquely identifying users, you can maintain unique user profiles even if the user uses multiple devices or when multiple users use the same device. 

The CleverTap user profile stores all the events performed by the user. CleverTap uses different identifiers to attribute these events and their properties to the user profile. To know more about events and properties, refer to [Events](doc:events) and [User Profiles](https://docs.clevertap.com/docs/user-profiles).

## Maintain Identities

The following are some of the key reasons to maintain identities: 

* Map the user activities and profile attributes to a specific profile.
* Target intended users using Campaigns or Journeys, user-level personalization, and recommendations.

# Types of Identifiers

The following types of identifiers are captured for user profiles on the CleverTap dashboard:

* CleverTap ID
* Identity
* Email ID
* Phone Number 

<Image title="User_Identity_Profile.png" alt={1989} align="center" className="border" border={true} src="https://files.readme.io/5eff36b-User_Identity_Profile.png" />

## CleverTap ID

CleverTap generates a device-level identifier called CleverTap ID (CT ID)

You can create your own unique identifiers for end-user devices using the custom CleverTap ID capability. For more information, refer to [Set CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id#section-rules-for-setting-the-clever-tap-id).

You can have a device identifier across all your systems without maintaining a mapping of the device ID across different systems. To know more about generating GDPR-compliant and non-GDPR complaint CTID, refer to [Create a User Profile](https://developer.clevertap.com/docs/sdk-changes-for-gdpr-compliance).\
A GDPR-compliant ID is prefixed by **\*\***, For example, \*\*g45sder2r.

## Identity

Identity is a unique ID you define for your internal database to uniquely identify your user. The selection of the primary key depends on the nature of the business.

Use *Identity* to identify the user uniquely. CleverTap allows you to use any unique ID on your systems as an identifier on the CleverTap dashboard. Some of the common examples are `customerID`, `userID`, `registrationID`, `databaseID`, and so on.

The identity can differ from the Email or Phone Number for a specific business.

## Email ID

In today's digital world, an email ID is a preferred way of identifying users. The email must be unique to be set as an identity. For example, users can use an email ID as a unique identifier for subscription-based services such as online grocery or music streaming applications.

## Phone Number

Businesses can now use mobile phone numbers as a valid form of identity because of the accessibility of smartphones and the applications installed on them. Users can sign up for any product on their mobile application and have a great onboarding experience. 

For example, Fintech services use mobile phone numbers as a unique identifier for quicker login and signup.
