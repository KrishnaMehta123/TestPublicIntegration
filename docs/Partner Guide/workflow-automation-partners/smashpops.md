---
title: Smashpops
excerpt: Workflow Automation
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[SmashPops](https://www.smashpops.com/) provides gamified pop-ups to attract new subscribers and grow your customer base through your website or app. With coupons, weighted rewards, and customizable game rules, SmashPops helps brands increase engagement while collecting valuable customer data.

Integrating SmashPops with CleverTap via Zapier enables you to:

* **Sync User Profiles in Real Time**: Update user attributes in CleverTap whenever a game is played.
* **Trigger Automated Engagement**: Fetch events from SmashPops to CleverTap to trigger journeys and personalized campaigns.
* **Retarget Dormant Users**: Build custom CleverTap segments from SmashPops data and run win-back campaigns.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* Access to your **SmashPops** account
* Access to an active **Zapier** account
* A CleverTap account with **Account ID** and **Passcode**.

# Integrate SmashPops with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create Passcode on CleverTap Dashboard](doc:smashpops#create-passcode-on-clevertap-dashboard)
2. [Create Game in SmashPops](doc:smashpops#create-game-in-smashpops)
3. [Connect SmashPops and CleverTap via Zapier](doc:smashpops#connect-smashpops-and-clevertap-via-zapier)
4. [Add Integration Code to Your Website](doc:smashpops#add-integration-code-to-website)

## Create Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create Game in SmashPops

Consider an example where you want to run a gamified pop-up on your website, collect emails, and sync those users into CleverTap for retargeting. To do so, perform the following steps:

1. Go to the SmashPops dashboard and create a game you want to display on your website.

<Image align="center" alt="SmashPops Dashboard" border={true} caption="SmashPops Dashboard" src="https://files.readme.io/62c81ffa2e3d303de8115aba4db428370b1dd2d0bfadc1f9c70aca6ac7b1c1ed-image.png" width="65% " />

2. Configure game rules such as display settings, coupon codes, and reward weights.

<Image align="center" alt="Configure Game" border={true} caption="Configure Game" src="https://files.readme.io/19547a71155fda053868eafc9a114304d7f79a5aa575b8f3ee56c256481025f1-image.png" width="65% " />

3. Go to the **Data Collection** section, click **+ Link Another Integration**, and select **Zapier**.

<Image align="center" alt="Link Another Integration" border={true} caption="Link Another Integration" src="https://files.readme.io/88543d5857dea21b17dc4ae55e17c61d1292a9501281a3c10987a72bcbab1af1-image.png" width="65% " />

4. You will be invited to Zapier. Click **Accept Invite & Build a Zap**.

<Image align="center" alt="Accept Invite & Build a Zap" border={true} caption="Accept Invite & Build a Zap" src="https://files.readme.io/51e7bcbea8255782dbb2b6159a106886118e12d733c39a2431095a99485a9df3-Screen_Recording_2025-06-30_at_11.26.40_AM_1.gif" width="65% " />

Once Zapier is integrated into Smashpops, it can connect to SmashPops with CleverTap via Zapier.

## Connect SmashPops and CleverTap via Zapier

Zapier acts as the automation bridge between SmashPops and CleverTap. Each time a user plays a game, SmashPops sends interaction data to CleverTap through Zapier. This enables businesses to either:

* **Create or update user profiles** with player details such as email, coupons, or scores.

OR

* **Log each play as an event** to power segmentation, analytics, and personalized engagement campaigns.

The integration supports two options depending on your use case:

* [Create or Update User Profiles](doc:smashpops#create-or-update-user-profiles)
* [Upload Event](doc:smashpops#upload-event)

### Create or Update User Profiles

Consider an example where you want to sync game player data into CleverTap so that each new play updates or creates a user profile for personalized engagement. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as SmashPops.

<Image align="center" alt="Create a Zap on Zapier Dashboard" border={true} caption="Create a Zap on Zapier Dashboard" src="https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png" width="75% " />

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select SmashPops from the App section. This starts the Zap when a trigger event occurs on SmashPops.
   2. Select _Trigger Event_ from the dropdown list and then select _New Data_ for this use case.
   3. Select Account and sign in using your SmashPops account credentials.
   4. Enter your SmashPops API key. A link is provided in the popup to help you locate the API key in your SmashPops dashboard.

<Image align="center" alt="Set Up Trigger Event" border={true} caption="Set Up Trigger Event" src="https://files.readme.io/ad8a55ab9674b9af05c53fb362477d8cf45278ec5f3db21f95c172c923f8fbfa-Screen_Recording_2025-06-30_at_10.57.02_AM_3.gif" width="75% " />

3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.

<Callout icon="📘" theme="info">
  #### Skip Test if Trigger Fails

  If Zapier cannot pull sample data during the test, click **Skip Test**. The Zap will still run correctly once published and connected to live data.
</Callout>

4. Click **Publish**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Create/Update User Profile_ from the Action event dropdown. This implies that whenever new data is generated, a new user profile is created, or an existing user profile is updated with the new information on the CleverTap dashboard.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create Passcode on CleverTap Dashboard](doc:smashpops#create-passcode-on-clevertap-dashboard) step.
   4. Click **Continue** after your account is successfully connected.

<Image align="center" alt="Select the Action for Zap" border={true} caption="Select the Action for Zap" src="https://files.readme.io/6134aee716977c0b32583899e754ac14e80ea3375ec98bed30ee418e64f6428f-4ea42b86-ce46-4fd0-9dde-09becd5626dd.png" width="75% " />

6. **Configure the Action**. Map SmashPops data fields to CleverTap fields as follows:

| CleverTap Field    | SmashPops Field                                                                                                |
| ------------------ | -------------------------------------------------------------------------------------------------------------- |
| Identity           | Email or unique user ID collected via the game.                                                                |
| Object ID          | Leave blank if Identity is provided.                                                                           |
| Creation Date      | Date or time of gameplay.                                                                                      |
| Profile Properties | Game data in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "coupon": "WELCOME10"}`) |

<Callout icon="🚧" theme="warn">
  #### Mapping Identity and Object ID

  You can keep the Identity field blank if you provide an Object ID, and vice versa.
</Callout>

7. Click **Continue**, and click **Test Step** to test the Zap after mapping the fields.

<Image align="center" alt="Test Zap" border={true} caption="Test Zap" src="https://files.readme.io/6354738a5f26e47ce1cf2ca78e532e2759399140945b80179171586117f28f54-6fa41f8d-5816-4b2e-a294-d708b88257d2.png" width="75% " />

8. Check the CleverTap dashboard to confirm the user profile has been created or updated.

<Image align="center" alt="Verify on the CleverTap dashboard" border={true} caption="Verify on the CleverTap dashboard" src="https://files.readme.io/ef76ba31ab8daf8bb2c0918cb0e3b6a57e560712997a3f21b9cad1a129ee6125-image.png" width="75% " />

9. Once validated, click **Publish** to activate the Zap.

### Upload Event

Consider an example where you want to track game interactions in CleverTap as events, rather than updating user profiles. This ensures each play is logged for analytics, segmentation, and engagement campaigns. To do so, perform the following steps:

1. Follow _Step 1_ to _Step 4_ from [Create or Update User Profiles](doc:smashpops#create-or-update-user-profiles) to configure SmashPops as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create Passcode on CleverTap Dashboard](doc:smashpops#create-passcode-on-clevertap-dashboard) step.
   4. Click **Continue** after your account is successfully connected.

<Image align="center" alt="Select the Action for Zap" border={true} caption="Select the Action for Zap" src="https://files.readme.io/6134aee716977c0b32583899e754ac14e80ea3375ec98bed30ee418e64f6428f-4ea42b86-ce46-4fd0-9dde-09becd5626dd.png" width="75% " />

3. **Configure the Action**. Map SmashPops data fields to CleverTap fields as follows:

| CleverTap Field  | SmashPops Field                                                                                       |
| ---------------- | ----------------------------------------------------------------------------------------------------- |
| User ID          | Email or unique identifier.                                                                           |
| Event Name       | Descriptive event name, such as `"Game Played"` or `"Reward Won"`.                                    |
| Creation Date    | Date or time of gameplay.                                                                             |
| Event Properties | Event data in JSON format (for example, `{"reward": "10%OFF", "score": 450, "level": "Spin Wheel"}`). |

<Callout icon="🚧" theme="warn">
  #### Mapping Identity and Object ID

  You can keep the Identity field blank if you provide an Object ID, and vice versa.
</Callout>

4. Click **Continue** and click **Test Step** to test the zap after mapping the fields.
5. Click **Publish**.

Once published, each SmashPops play will be logged as an event in CleverTap.

## Add Integration Code to Website

For the integration to work as intended, you must add the SmashPops integration code to your website. To do so, perform the following steps:

1. In your SmashPops account, go to _Settings_ > _My Account_ > _Show Integration Code_.

<Image align="center" alt="Integration Code" border={true} caption="Integration Code" src="https://files.readme.io/e801dc33485473ddb448e22b0648267a6436412f11d3d1abe43d53582fda0943-image.png" width="75% " />

2. Copy the snippet and paste it into your website’s HTML (`<head>` or end of `<body>`). Ensure the website URL you configure in SmashPops matches the domain where you deploy the snippet. SmashPops only works on the registered domain.
3. Once added, your game will display according to the rules you have configured, and user actions will be tracked in the CleverTap dashboard.

<Image align="center" alt="Example workflow" border={true} caption="Example workflow" src="https://files.readme.io/2f31702ceae16594ce4f72542b3446a15b78bc95c2567914481259dada02c93d-Screen_Recording_2025-06-30_at_11.20.27_AM_1.gif" width="75% " />

You can also set up coupon codes and configure weights or chances of each reward in the SmashPops game settings.

# FAQs

### Can I use SmashPops with CleverTap Email Campaigns?

Yes. You can sync users who played games in SmashPops with CleverTap and then target them through email, push notifications, or In-App campaigns.
