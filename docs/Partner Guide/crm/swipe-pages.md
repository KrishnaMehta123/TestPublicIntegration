---
title: Swipe Pages
excerpt: Customer Relationship Management
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[Swipe Pages](https://swipepages.com/) is a no-code landing page builder that helps create high-converting, mobile-optimized pages using a drag-and-drop interface. You can integrate Swipe Pages with CleverTap using Zapier to capture lead data from landing page forms and create or update user profiles in CleverTap.

With the CleverTap and Swipe Pages integration, you can:

* Automatically create or update user profiles in CleverTap from Swipe Pages form submissions.
* Trigger welcome emails or onboarding campaigns when a user signs up.
* Add users to specific journeys, such as event reminders or product interest flows.
* Segment users based on form inputs (for example, topic of interest) and send personalized follow-ups.

# Prerequisites for Integration

The following are the prerequisites for integrating Swipe Pages with CleverTap via Zapier:

* A Swipe Pages account with access to create landing pages and generate API keys.
* An active Zapier account.
* A CleverTap account with **Account ID** and **Passcode**.

# Integrate Swipe Pages with CleverTap

The integration process involves the following three major steps:

1. [Create Passcode on CleverTap Dashboard](doc:swipe-pages#create-passcode-on-clevertap-dashboard)
2. [Create Landing Page in Swipe Pages](doc:swipe-pages#create-landing-page-in-swipe-pages)
3. [Configure Zapier in Swipe Pages](doc:swipe-pages#configure-zapier-in-swipe-pages)

## Create Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API request must include the Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create Landing Page in Swipe Pages

To create a landing page in Swipe Pages where form submissions will be collected. To do so, perform the following steps:

1. Log in to your [Swipe Pages](https://app.swipepages.com/signup) dashboard.
2. Go to _Integrations_ > _Landing Pages_ from the left panel.
3. Click **Create New Page** to create your landing pages. Refer to [Creating a new landing page in Swipe Pages](https://docs.swipepages.com/en/articles/4761649-creating-a-new-landing-page).

<Image align="center" alt="Create Landing Page in Swipe Pages" border={true} caption="Create a Landing Page in Swipe Pages" src="https://files.readme.io/eb23182763d908e0300e2c6c4731698fa791677d9bd8c11358b0088393a867ea-image.png" />

## Configure Zapier in Swipe Pages

Zapier acts as the automation bridge between Swipe Pages and CleverTap. To enable this connection, you must configure Zapier within Swipe Pages. To do so, perform the following steps:

1. Go to _Integrations_ from the left panel on the Swipe Page dashboard
2. Click on **Zapier** and click **Create a New Zap**.

<Image align="center" alt="Configure Zapier in Swipe Pages" border={true} caption="Configure Zapier in Swipe Pages" src="https://files.readme.io/dd48f2d3928df662f5ee7e13cab401695bfe39b8e735874b566828eefd4083fc-image.png" />

3. To create the connection, you will be provided with a Swipe Pages API key here.
4. Copy it and keep it safe.

Now that Zapier is configured in Swipe Pages, proceed further to set up the Zapier workflow with [Swipe Pages as the trigger](doc:swipe-pages#set-up-swipe-pages-trigger) and [CleverTap as the action](doc:swipe-pages#set-up-clevertap-action).

### Set Up Swipe Pages Trigger

A trigger determines when your Zap will run. In this case, the trigger is a form submission on your Swipe Pages landing page. To set up swipe pages as a trigger, perform the following steps:

1. Set the **Trigger App** as _Swipe Pages_.
2. Select the _Trigger Event_. In this case, select _New Form Submission_ from the dropdown. This ensures the Zap is triggered every time a user submits a form on your Swipe Pages.

<Image align="center" alt="Set Up Swipe Pages Trigger" border={true} caption="Set Up Swipe Pages Trigger" src="https://files.readme.io/98b0004f3361e4ef45f170e4ccab762a3d9efa615406798032a6bb0536810d1a-image.png" width="65% " />

3. Connect your Swipe Pages account using the previously generated **API Key** from _step 4_ of [Configure Zapier in Swipe Pages](doc:swipe-pages#configure-zapier-in-swipe-pages).
4. Select the specific form whose submissions you want to capture.

<Image align="center" alt="Select Record" border={true} caption="Select Record" src="https://files.readme.io/77b1a7d9e5b3a2fbc906749f021fd6629dc8e4c95d8c33f6fab5e581eca8e891-image.png" width="65% " />

<Callout icon="📘" theme="info">
  #### Note

  Submit a test form on Swipe Pages to fetch sample data during setup.
</Callout>

### Set Up CleverTap Action

Once the trigger is defined, you need to configure what happens in CleverTap. This is done by setting up an action in Zapier. To set up CleverTap as an action, perform the following steps:

1. From the _Action App_, select _CleverTap_.

<Image align="center" alt="CleverTap Action" border={true} caption="CleverTap Action" src="https://files.readme.io/08e73fd34488daeecdb2da873d4a3603d8d60244da52e7de2d5a483a27987499-image.png" width="65% " />

2. Select one of the following **Action Events**:
   * _Create/Update User Profile_
   * _Upload Event_

<Image align="center" alt="Select Action for Zap" border={true} caption="Select Action for Zap" src="https://files.readme.io/4903bc675ec319b63eb13e8c8f1ff835fa184285b74afd1f3374cc8a212e9636-image.png" width="55% " />

3. Connect your CleverTap account by entering **Account ID**, **Passcode**, and **Region** of your CleverTap account. For detailed steps, refer to [Create a Passcode on the CleverTap Dashboard](doc:swipe-page#create-passcode-on-clevertap-dashboard).

<Image align="center" alt="Connect your CleverTap account" border={true} caption="Connect your CleverTap account" src="https://files.readme.io/b249b681569c721f0d90fa2b828b02f9630ac2f9fe80a59f764063453e0d1b3f-image.png" width="75% " />

4. Map Swipe Pages data to CleverTap fields:

| **CleverTap Field**  | **Description**                                                     |
| -------------------- | ------------------------------------------------------------------- |
| Identity / Object ID | Unique identifier (email, phone, or internal user ID)               |
| Creation Date        | (Optional) Timestamp of form submission                             |
| Profile Properties   | JSON object of additional attributes (for example, `name`, `email`) |
| Event Name           | (If uploading event) for example, `submitted_landing_form`          |
| Event Properties     | JSON of contextual details (for example, `page`, `campaign`)        |

<Callout icon="🚧" theme="warn">
  #### Map Identity and Object ID

  You can keep the Identity field blank if you provide an Object ID, and vice versa.
</Callout>

<Image align="center" alt="Configure the Action" border={true} caption="Configure the Action" src="https://files.readme.io/6bd1cbfe817149f9bfb66dee8f27c341c8cd38cf03ccf28fd158cbf0b5e02088-Screenshot_2025-06-24_at_2.28.31_PM.png" width="65% " />

5. Click **Test & Review** to validate the setup.
6. Check your CleverTap dashboard for the test event.

<Image align="center" alt="Verify Events in CleverTap" border={true} caption="Verify Events in CleverTap" src="https://files.readme.io/045e57607db544d69b46f0dca5b31fceea96f7c84a122b0ab912bca075f0b8f1-9d5935f4-d6eb-410a-9309-e1d8a5305ac6.png" width="65% " />

7. Click **Publish** to activate the Zap.

# Verify Integration Results

After publishing the Zap:

* If you selected _Upload Event_, CleverTap logs a new event each time a form is submitted on your Swipe Pages site. Events appear in the _Events_ section of the CleverTap dashboard.
* If you selected _Upload/Update User Profile_, CleverTap uses the `Identity` field to determine whether to create or update a user profile.

This automation enables you to seamlessly capture form data into CleverTap, allowing for personalized engagement without manual intervention on the CleverTap dashboard.

# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data being transferred or failure to update user profiles and events correctly.
