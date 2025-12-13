---
title: Send Test Personalization
excerpt: >-
  Learn how to send personalized test email campaigns from the CleverTap
  dashboard.
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

In modern marketing, creating personalized campaigns is crucial for connecting with audiences. The Send Test Personalization feature streamlines this by enabling marketing teams to test campaigns with personalized values, ensuring a seamless display of tailored content. This empowers marketers to scrutinize individualized elements within the message with precision.

For example, if your campaign includes customized promotions, event details, or tailored offers, this feature helps you test and preview the seamless functionality of these personalized elements with an internal audience before sending it to your customers.

You can send test campaigns with personalized values using the *Preview & Test* option from the campaign page.

<Image alt="Preview & Test Popup" align="center" width="90% " border={true} src="https://files.readme.io/2597389-Preview__Test.gif">
  Preview & Test Popup
</Image>

You will be able to use [personalized values for the From and Reply-to Email Address fields](doc:create-message-sender-details#sender-details), a feature released in Private Beta, for the following providers: SendGrid, Amazon SES, and Generic SMTP setup.

# Ways to Send Personalized Test Message

CleverTap provides the following three ways to select the users to send a personalized test message:

* **Select from Test Profiles**: In this case, you can select multiple [profiles that are marked as test profiles](doc:user-profiles#mark-a-user-profile-as-a-test-profile) and send a test message to them.

<Image alt="Select a Profile from the Test Profiles" align="center" width="95% " border={true} src="https://files.readme.io/de6383f-Select_Test_Profiles-_1.png">
  Select a Profile from the Test Profiles
</Image>

* **Search and Add from All Profiles**: In this case, you can select the email address, CleverTap ID, or identity of the profiles that are already present on your dashboard and send them a test message.

<Image alt="Search and Add from All Profiles on the CleverTap Dashboard" align="center" border={true} src="https://files.readme.io/212a96f-image.png">
  Search and Add from All Profiles on the CleverTap Dashboard
</Image>

* **Email Address**: In this case, you can manually enter the email address of the profiles to which you want to send a test message. 

<Image alt="Manually Add Email Address " align="center" width="95% " border={true} src="https://files.readme.io/23fd956-Email_Address.png">
  Manually Add Email Address 
</Image>

After configuring all the required fields, you can preview the campaign with personalized values for the selected user profile before sending. If you select multiple profiles for sending test messages, you can select the user from the dropdown under the *Preview* section on the right to preview the message for that user.

<Image alt="Select User Profile to Preview Campaign with Personalized Values" align="center" border={true} src="https://files.readme.io/4cbf819-image.png">
  Select User Profile to Preview Campaign with Personalized Values
</Image>

> 📘 Note
>
> * You can add a maximum of 20 profiles in total for sending test messages using the following options: *Select From Test Profiles* and *Search and Add from All Profiles*.
> * The profiles entered in the *Email Address* field will receive the default values except for Linked Content personalization. 
> * The *Inbox Previews* and *Spam Reports* will use default values.

# Send Test with Event Personalization

Consider a scenario where your message includes event personalization, that is, you want to send a personalized value for the event properties in your message. You can only use the event properties of the triggering event you selected in the WHO section.

For sending test messages using selected profiles, CleverTap introduces Event Personalization features. There are two options for event personalization:

* **Default property**: This option allows the utilization of default values established in the campaign content. You can also modify the default value exclusively for the test message.
* **Sample Property**: The top 20 event property values associated with the same event that occurred within the last five days are listed under the *Event Personalization* section. You can select from the list or add the value that you want to send in your test message. 

The value that you select here will be sent to all the selected profiles.

For example, if you are a subscription platform and you want to send a reminder campaign to your subscribers to resume watching the series from where they left off. Here, the event will be *Video Watched*, and the event property will be Series Name.

<Image alt="Event Personalization Example " align="center" border={true} src="https://files.readme.io/d75767a-Send_test_personalization_-_Email.gif">
  Event Personalization Example 
</Image>

# Send Test Response

You can view the response details as soon as you send the test message. To do so, click **Send Test** from the *Preview & Test* popup. The Send Test Response window opens, where all the response details are classified into the following categories. Click the + sign against each user to view all the details (refer to the following image):

* Details of the message sent successfully
* General Errors, if any
* Linked Content Response: You can copy the responses by clicking the ![](https://files.readme.io/7534549-Copy_icon.png) icon against the respective response.
* Liquid Tags Error, if any

<Image alt="Send Test Reponse" align="center" border={true} src="https://files.readme.io/b3918f4-Send_Test_Response_Per_User_.png">
  Send Test Response Per User
</Image>

This ensures a thorough examination of the test response, offering valuable insights into the success and potential errors associated with the sent test messages.
