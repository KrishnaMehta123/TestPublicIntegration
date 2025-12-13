---
title: SquareSpace
excerpt: Dynamic Content
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

[Squarespace](https://www.squarespace.com/) is a no-code website builder that allows users to create websites, landing pages, and forms without writing code. SquareSpace forms are used to capture user responses, such as newsletter subscriptions or contact inquiries.

This guide explains how to do the following by integrating Squarespace with CleverTap via [Zapier](https://zapier.com):

* Automatically create or update users on the CleverTap dashboard when they submit a Squarespace form.
* Upload custom events to CleverTap when users interact with Squarespace forms.

# Prerequisites for Integration

The following are the prerequisites for integrating Squarespace with CleverTap via Zapier:

* Ensure you have access to your Squarespace account.
* Ensure you have access to an active Zapier account to create the CleverTap app.
* Ensure you have a CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Squarespace with CleverTap

The integration process involves the following four major steps:

1. [Create Passcode on CleverTap Dashboard](doc:squarespace#create-passcode-on-clevertap-dashboard).
2. [Generate Squarespace API Key](doc:squarespace#generate-squarespace-api-key).
3. [Create Zap in Zapier](doc:squarespace#create-zap-in-zapier).
4. [Set Up CleverTap Action](doc:squarespace#set-up-clevertap-action).

## Create Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API request must include the Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Generate Squarespace API Key

To allow Zapier to access and monitor your Squarespace forms, you need to generate an API key from your Squarespace account. This key is used to authenticate and authorize communication between Squarespace and Zapier. To do so, perform the following steps:

1. Go to *Settings* > *Developer Tools* > *External API* from your Squarespace dashboard.
2. Click **Generate Key** and perform the following steps:
   1. Enter the *KEY NAME* and select the appropriate permissions.
   2. Click **GENERATE KEY**.
   3. Once the API key is generated, click **COPY KEY**  and save for use in Zapier.

<Image alt="Generate Squarespace API Key" align="center" width="80% " border={true} src="https://files.readme.io/b248c9516a071cb5beab9e955181f34d0db34bedf322fe79a05392c189264534-squrespace.gif">
  Generate Squarespace API Key
</Image>

You can now securely connect Squarespace to Zapier using this API Key and proceed with setting up automation without any manual form data handling. This key authenticates and authorizes communication between Squarespace and Zapier.

## Create Zap in Zapier

Create a Zap to automate the flow of data from Squarespace to CleverTap. The Zap captures responses from Squarespace form submissions and sends the data to CleverTap based on the configured action. Either creating or updating a user profile or event. To do so, follow these steps:

1. Log in to the [Zapier Dashboard](https://zapier.com/) and click **+ Create Zap**.
2. Set the **Trigger App** as *Squarespace Forms*.
3. Select the **Trigger Event**. For example, select *New Form Submission* from the dropdown. This ensures the Zap is triggered every time a user submits a form on your Squarespace website.
4. Connect your Squarespace account using the API key.

<Image alt="Connect Squarespace" align="center" width="85% " border={true} src="https://files.readme.io/3ce97671967aab885de07afee5155960369cab008f30e61164f84ae2cd1f84ac-Screen_Recording_2025-07-03_at_11.06.09_AM_1.gif">
  Connect Squarespace
</Image>

5. Select the form from which you want to transfer data to CleverTap.

<Image alt="Select Form Type" align="center" width="85% " border={true} src="https://files.readme.io/79a3bbbbf1efa3c5a100ce710fa152ac9085bf874eeaae3382cde37c6c837f1e-Screen_Recording_2025-07-03_at_11.08.04_AM_1.gif">
  Select Form Type
</Image>

6. Test this step to ensure the correct configuration.

## Set Up CleverTap Action

Configure the action that Zapier will perform in CleverTap using the form data. To do so, follow these steps:

1. For the **Action App**, select *CleverTap*.

<Image alt="CleverTap Action" align="center" width="65% " border={true} src="https://files.readme.io/08e73fd34488daeecdb2da873d4a3603d8d60244da52e7de2d5a483a27987499-image.png">
  CleverTap Action
</Image>

2. Select one of the following **Action Events**:
   * *Create/Update User Profile*
   * *Upload Event*

<Image alt="Select Action for Zap" align="center" width="55% " border={true} src="https://files.readme.io/4903bc675ec319b63eb13e8c8f1ff835fa184285b74afd1f3374cc8a212e9636-image.png">
  Select Action for Zap
</Image>

3. Connect your CleverTap account:
   * Enter **Account ID**, **Passcode**, and **Region**. Refer to [Create a Passcode on the CleverTap Dashboard](doc:squarespace#create-passcode-on-clevertap-dashboard) for detailed steps.
4. Map Squarespace form data to CleverTap fields:

   | **CleverTap Field** | **Description**                                                                                                              |
   | ------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
   | User ID             | Unique ID, email, or user identifier from a *Form* field.                                                                    |
   | Object ID           | Unique object reference.                                                                                                     |
   | Creation Date       | (Optional) Timestamp when the form is submitted.                                                                             |
   | Event Name          | Custom event (for example, `subscribed_to_newsletter`).                                                                      |
   | Event Properties    | A JSON object containing extra details from the form, such as topic or submission type, (for example,`topic`, `newsletter`). |

> 🚧 Map Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" width="65% " border={true} src="https://files.readme.io/1ae9dd6f7db0682b2b12389dd1ce66fdb3466a75711455fe2b6be4a895939fec-image.png">
  Configure the Action
</Image>

5. Click **Test & Review** to validate the setup.
6. Check your CleverTap dashboard for the test event.

<Image alt="Verify Events in CleverTap" align="center" width="55% " border={true} src="https://files.readme.io/77189e52be50fb12dff7718776955bb2ef87a515068468d99b6d47004d2f475e-image.png">
  Verify Events in CleverTap
</Image>

7. Click **Publish** to activate the Zap.

<Image alt="Publish Zap" align="center" width="65% " border={true} src="https://files.readme.io/1eb484d6965aee528a5af4c05cb2147f1f0737dae8a6724351cf87863480efcf-image.png">
  Publish Zap
</Image>

# Verify Integration Results

After publishing the Zap:

* If you selected *Upload Event*, CleverTap logs a new event each time a form is submitted on your Squarespace site. Events appear in the *Events* section of the CleverTap dashboard.
* If you selected *Upload/Update User Profile*, CleverTap uses the `Identity` field to determine whether to create or update a user profile.

This automation allows you to seamlessly capture form data into CleverTap, enabling personalized engagement without manual intervention on the CleverTap dashboard.

# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data being transferred or failure to update user profiles and events correctly.
