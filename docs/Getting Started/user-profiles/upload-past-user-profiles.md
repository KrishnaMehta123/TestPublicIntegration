---
title: Upload Past User Profiles
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

This section covers how identified user profiles are treated in the CleverTap dashboard.

# Already Identified User

When previously identified users visit your app or website from another device or browser, CleverTap creates a new anonymous profile for them. Once they identify themselves (for example, by logging in), CleverTap merges the anonymous profile into the existing identified profile. Any anonymous events generated are transferred into the identified profile and become available for segmentation, funnels, and engagement targeting.

# Existing Profiles

If a user has an existing profile stored in your CleverTap account and if the user buys a new device and downloads your app and perform some events on this app without sign-up or log-in, the device does not know that this user has an existing profile. Therefore, the system creates an anonymous profile and stores the events in this newly created profile.

Once the user shares her identity (e.g., email, mobile phone number, or Google advertising ID) to the anonymous profile for example while login, then this profile gets merged with the user's original profile but the events captured before passing the identity are saved in an orphan profile with only a CleverTap ID and no email, mobile phone number, and other useful properties.

In this case, there is no use in qualifying orphan profiles in campaigns or journeys. However, to keep clear data as to how many profiles have been created on the CleverTap dashboard, we include the orphan profiles in the _Find People_ count but these profiles are not included when downloaded.
