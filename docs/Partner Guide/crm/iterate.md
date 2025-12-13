---
title: Iterate
excerpt: Customer Relationship Management
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

[Iterate](https://iteratehq.com/) is a survey platform that helps businesses collect user feedback across channels.

The CleverTap Iterate integration enables you to send surveys via CleverTap’s messaging channels, such as Email, Web Pop-Ups, and In-App Messages, and sync each response as a User Property or custom event.

Responses are automatically linked to the user’s CleverTap Profile Identity. You can collect personal details, feedback scores, preferences, or behavioral data to enrich user profiles, create intelligent segments, and deliver personalized engagement.

# Prerequisites for Integration

Ensure you have the following before setting up the integration:

* An active Iterate account with survey creation access
* An active CleverTap account with **Project ID** and **Project Passcode**
* (Optional) Access to CleverTap email, In-app, or web pop-up campaigns

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Iterate. The CleverTap and Iterate integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Iterate](mailto:support@iteratehq.com) for support and resolution.

# Integrate Iterate with CleverTap

To deliver personalized surveys through CleverTap and capture user responses seamlessly, you must complete the following three integration steps.

1. [Connect Iterate with CleverTap](doc:iterate#connect-iterate-with-clevertap).
2. [Create Survey in Iterate](doc:iterate#create-survey-in-iterate).
3. [Add Survey to CleverTap Campaign](doc:iterate#add-survey-to-clevertap-email-campaign).

## Connect Iterate with CleverTap

Link your Iterate account to CleverTap to enable automatic response syncing. To do so, perform the following steps:

1. In the CleverTap dashboard, go to *Settings* > *Project* > *Overview* and copy your **Project ID** and **Passcode** 
2. In Iterate, go to *Company Settings* > *Integrations*.
3. Under CleverTap, enter your CleverTap **Project ID**, account **Region**, and **Passcode**.

<Image alt="Connect Iterate with CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/6804bb90c3b0e98a6a17ca2fcac9fe561d8412ade9bf3880e585cce26e7b631e-image.png">
  Connect Iterate with CleverTap
</Image>

> 📘 Note
>
> If using CleverTap In-App or Web Pop-up messaging channel, contact Iterate Support via In-App chat to enable Monthly Active User (MAU) data sync.

## Create Survey in Iterate

Build your survey in Iterate before embedding it in a CleverTap campaign. For example, we will be sending surveys via CleverTap email campaigns. 

1. Go to the *Send Survey* tab and select *Integrations* > *CleverTap* in the Iterate dashboard.
2. Toggle on the *Send responses to CleverTap* option to update customer profiles in CleverTap with the responses.

<Image alt="CleverTap integration toggle" align="center" width="25% " border={true} src="https://files.readme.io/4f97ba4ba2554d081541ab80fd8a50e3bca6206ac96f82277362eea8f2ea6f9e-image.png">
  CleverTap Integration Toggle
</Image>

3. Copy the parameter `user_email={{ Profile.Identity | default: 'null' }}`, CleverTap replaces this with the `user_email` to associate responses.

## Add Survey to CleverTap Email Campaign

After creating the survey in Iterate, you can embed it into a CleverTap email campaign to collect responses directly from recipients. You can do so by using one of the following two options:

* [(Recommended) Embed First Question in Email Campaign](doc:iterate#recommended-embed-first-question-in-email-template) 
* [Link to Full Survey](doc:iterate#link-to-full-survey)

You can send Iterate surveys through CleverTap using:

* [Email campaigns](doc:create-message-email)
* [In-App Messages](doc:create-message-in-app)
* [Web Pop-Ups](doc:create-message-web-popup)

For detailed steps on sending surveys via CleverTap, refer to the [Iterate documentation](https://help.iteratehq.com/en/articles/11930835-delivering-surveys-via-clevertap-mobile-in-app-message-and-web-pop-up).

### (Recommended) Embed First Question in Email Template

1. In Iterate, go to *Send Survey* > *Integrations* > *CleverTap*.
2. Copy the Email Embed Code from the CleverTap integration section.
3. In CleverTap’s Email Campaign Editor, paste the embed code into the HTML of your email template at the location where you want the first survey question to appear. 

<Image alt="Email Embed Code" align="center" width="60% " border={true} src="https://files.readme.io/1346e3d471feca3b51b5b4bd8ebf7bd1a0428c61ed561f9646aff5227276a3cb-image.png">
  Email Embed Code
</Image>

### Link to Full Survey

1. In Iterate, go to the *Send Survey* > *Integrations* > *CleverTap*.
2. Copy the Survey Link from the CleverTap integration section.
3. In CleverTap’s Email Campaign Editor, add the survey link to a button or hyperlink in the email body.

When recipients click the link, they are directed to the full survey, starting from the first question.

## Publish Campaign

Before publishing the campaign, ensure your survey works correctly using the **Preview & Test** option. Once verified, publish the campaign. The user receives the survey as they qualify for the campaign (refer to the following image).  

<Image alt="Preview of an email containing the first question of an Iterate survey" align="center" width="60% " border={true} src="https://files.readme.io/7663e47c951353b1d04227bf9fbfe088279e06a3fd2bc6a2a8e0daeebb0ea270-image.png">
  Preview of Email Campaign with First Question from Iterate Survey
</Image>

# Log Custom Events in CleverTap

Once users respond, you can verify the following in the CleverTap dashboard:

* User Properties are updated with survey responses.
* The custom event `survey-question-response` is logged for each question answered.

<Image alt="CleverTap dashboard showing updated User Properties and logged survey events." align="center" width="65% " border={true} src="https://files.readme.io/b1e76686be2e34ac73fe486ca8009b821f05bccc296eddbe58b8938910de8480-image.png">
  CleverTap dashboard showing updated User Properties and logged survey events
</Image>

Iterate sends a `survey_question_response` event to CleverTap for each completed question. The event includes the following fields:

| Field Name       | Description                          |
| :--------------- | :----------------------------------- |
| question         | Survey question text                 |
| label            | Custom property name (if defined)    |
| response         | Readable version of the answer       |
| response\_int    | Numeric responses (for example, NPS) |
| response\_string | Open-ended or single-select answers  |
| response\_array  | Multi-select answers                 |

For triggering flows or campaigns based on these events in CleverTap, refer to [Custom Events](https://developer.clevertap.com/docs/events#custom-events).

# Pass CleverTap Properties to Iterate

You can send additional user profile properties from CleverTap to Iterate to filter responses and personalize surveys. By default, Iterate only receives the user’s CleverTap Identity ID and Email. You can pass more attributes, such as user type or preferences, for richer segmentation.

To understand this better, consider an example where the e-commerce marketplace may pass a property identifying a user as a `buyer` or `seller`. In Iterate, this allows filtering survey responses by role and tailoring survey content accordingly.

To do so, perform the following steps:

1. In the *Send Survey* tab in Iterate, click **Customize user properties** above the HTML code.
2. Enter the property name as you want it to appear in Iterate.
3. Enter the corresponding CleverTap template tag that will populate the value (for example, `@Profile - User Type`).
4. Select whether the property is a *User property* (persistent across sessions) or a *Response property* (specific to the current survey or session).

> 🚧 Important
>
> Once created, the property type (for example, string, number) cannot be changed. To use a different type, create a new key (for example, `user_id_string`) or contact [Iterate Support](mailto:support@iteratehq.com). For more details, refer to the [Iterate documentation](https://help.iteratehq.com/en/articles/11930835-delivering-surveys-via-clevertap-mobile-in-app-message-and-web-pop-up).

<Image alt="Customize User Properties in Iterate" align="center" width="35% " border={true} src="https://files.readme.io/512f76dc02c261ce6bdb2f375baafa984d8563905b5bb49ce2fb4a5c228fa876-image.png">
  Customize User Properties in Iterate
</Image>

Once configured, these properties are passed along with survey responses, enabling richer segmentation and more personalized experiences in both Iterate and CleverTap.
