---
title: Preview and Send In-App
excerpt: >-
  Learn how to send and test personalized In-App campaigns from the CleverTap
  dashboard.
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

Marketing teams can test In-App campaigns with personalized values before publishing them. This helps them verify the app experience before sending it to the user.

For example, marketers can send a personalized In-App message that highlights a user’s recently viewed product or shows a tailored offer based on their behavior, and first test it with an internal audience. The results of this test help verify that the personalized elements in the campaign are displayed correctly in the In-App experience before sending it to customers.

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send an In-App notification to any CleverTap user profile that you have marked as a _Test profile_.

<Image align="center" alt="Preview and Test In-App Popup" border={true} caption="Preview and Test Popup" src="https://files.readme.io/b3dd6c42a81215da3451bda8fe61def4514507530a0768fb8e1f8120dd5df0c9-image.png" />

<Callout icon="📘" theme="info">
  #### &#x20;Note

  The Preview & Test feature for sending tests on a real device requires minimum SDK versions (Android SDK v7.7.0 and CleverTap iOS SDK v7.4.0 or later). For lower SDK versions, send the campaign exclusively to a specific user for testing, then recreate and send it to your full audience.
</Callout>

# Test by Users and Devices

Select the _Notification channel_ to send your test message. You can test your message by device or by user profiles. You can combine event personalization with other In-App personalization options such as user profile properties, inline `@` personalization, recommendations, linked content, and Liquid tags to fully tailor the In-App experience. For more information, refer to [In-App Personalization](https://docs.clevertap.com/docs/personalize-message-inapp).

## By Devices

With this option, you can focus your test on specific devices. In the _Send test on_ section, click _Device tokens_.  The Android and iOS device token sections are displayed.  This is useful when a user has multiple devices, and you want to validate the In-App experience on specific form factors (for example, phone vs. tablet) or operating systems.

<Image align="center" alt="Test In-App by Device Tokens" border={true} caption="Test by Device Tokens" src="https://files.readme.io/840b7a81f738f2a8f77e5c04c4ced6eb18caa7e0f624cb52b0ac6fce69a29425-image.png" />

## By User

CleverTap provides the following options to select the users to send a personalized test In-App message:

* From Test Profiles
* From Any Profile

### From Test Profiles

You can select multiple [profiles that are marked as test profiles](doc:user-profiles#mark-a-user-profile-as-a-test-profile) and send a test In-App message to them. Test profiles are ideally your internal users.

<Image align="center" alt="Select In-App Test Profiles" border={true} caption="Select Test Profiles" src="https://files.readme.io/46023949c5e927e96692bfa9b04ebd42de857a51a3f9edcfa19e16e3ab304850-image.png" />

### From Any Profile

Search for a user profile from _Select from Profiles_. In this case, you can search for any recipient profile that is already present on your dashboard and send them a test In-App message by email address, CleverTap ID, or identity.

<Image align="center" alt="Search Additional Profiles for In-App Testing" border={true} caption="Search Additional Users for Testing" src="https://files.readme.io/658964c28f6632b34ab661b66eb1a7832b10ae9296f34f7c75b7f46a6014b6ff-image.png" />

### Test Devices

You can further filter the messaging by devices for each selected user and send them a test message. The _Test Devices_ section lists only devices on which your app is installed. So you test only on devices that can actually render the In-App message.

<Image align="center" alt="Select Test Devices for Test Profiles" border={true} caption="Select Test Devices for Test Profiles" src="https://files.readme.io/244d35c8029f378ac5816168bba4cb4184f58aed020666efbc827220d7df6c63-image.png" />

After configuring all the required fields, you can preview the In-App campaign with personalized values for the selected user profile before sending the message. If you select multiple profiles, you can select the user from the list under the _Preview_ section on the right to test the rendering for each profile.

Consider a scenario where your In-App message includes profile personalization, meaning you want to send an In-App message to each user based on their native language.  You can test the rendering of this message for each language based on the selected user in the list. This also allows you to detect issues early; for example, the message may exceed the character limit in German, but it displays correctly in other languages.

### Test Event Personalization

The events selected in your message will be displayed here. You can change the values to preview the message with the updated values. For example, change the discount value and preview it.

<Image align="center" alt="Change and Preview default event values" border={true} caption="Change and Preview Event Values" src="https://files.readme.io/078b3be86763413d9731b255816e2a21555048097e22e4b1c898195385f7a00b-image.png" />

### Test Custom User Personalization

If the user you want to test is not listed in the preview section, or if you are unsure who matches your criteria, enter the email address, CleverTap ID, or identity of a profile for which you have the details. This will give you an instant preview of your message with the applied personalization.

<Image align="center" alt="Test and Preview Custom User Values" border={true} caption="Change and Preview User Profile Values" src="https://files.readme.io/2d070f6c7d5603825efd1ca8354506cdbf9570cebe9bece3b52004f34e40c22c-image.png" />