---
title: Apxor
excerpt: Workflow Automation
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

[Apxor](https://www.apxor.com/) is an app intelligence platform that enables mobile apps to deliver hyper-contextual In-App experiences such as walkthroughs, tooltips, coachmarks, spotlights, In-App messages, and surveys. By integrating Apxor with CleverTap, product and marketing teams can sync user segments from CleverTap to Apxor and trigger targeted, personalized In-App interactions for onboarding, feature adoption, activation, and announcements, driving measurable product-led growth.

With this integration, for example, a product manager can identify users who have not tried a new feature in CleverTap, sync that segment to Apxor, and automatically launch a contextual walkthrough inside the app to encourage adoption.

# Prerequisites for Integration

Ensure you have the following before setting up the integration:

* Access to the [Apxor Dashboard](https://apxor.com/).
* [Apxor Android SDK](https://guides.apxor.com/getting-started-with-apxor/sdk/android-x) is integrated into your app.
* Access to your CleverTap account.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by Apxor. The CleverTap and Apxor integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Apxor](mailto:contact@apxor.com) for support and resolution.

# Integrate CleverTap with Apxor

To integrate Apxor with CleverTap, perform the following three major steps:

1. [Set Up Apxor for Integration](doc:apxor#set-up-apxor-for-integration).
2. [Set Up Webhook in CleverTap](doc:apxor#set-up-webhook-in-clevertap).
3. [Create Webhook Campaign in CleverTap](doc:apxor#create-webhook-campaign-in-clevertap).

## Set Up Apxor for Integration

Ensure Apxor is fully set up to receive cohort data by completing its initial setup. Proper configuration at this stage helps guarantee a smooth, error-free sync when you connect the two platforms. To do so, follow these steps:

1. Log in to your [Apxor Dashboard](https://apxor.com/).
2. Verify that the Android SDK integration is complete and active. If not, refer to [Apxor Android SDK](https://guides.apxor.com/getting-started-with-apxor/sdk/android-x).
3. Locate your App ID, which will be required during the CleverTap setup.
4. (Optional) Review [Apxor API Guides](https://guides.apxor.com/getting-started-with-apxor/api-guides) for advanced customization.

## Set Up Webhook in CleverTap

To send data to your Apxor account, set up a webhook in CleverTap:


1. Go to *Settings* > *Channels* > *Webhooks* from the CleverTap dashboard.
2. Click **Add Webhook** and provide a meaningful name for the webhook.
3. In the *Create webhook template* popup, enter the following details:

   <Image alt="Create Webhook" align="center" width="60% " border={true} src="https://files.readme.io/199136f60ef9126ef7335a1b29dbf260229ae1feb4defdf30beb972e0f3fad39-image.png" />

   <Table align={["left","left"]}>
     <thead>
       <tr>
         <th>
           Field
         </th>

         <th>
           Description
         </th>
       </tr>
     </thead>

     <tbody>
       <tr>
         <td>
           Name
         </td>

         <td>
           Enter the name for your webhook.
         </td>
       </tr>

       <tr>
         <td>
           HTTP Method
         </td>

         <td>
           Set the HTTP Method to *POST*.
         </td>
       </tr>

       <tr>
         <td>
           Destination URL
         </td>

         <td>
           Enter the following destination URL: `https://server.apxor.com/v1/track/external/clever-tap/sync/<app-id>`  

           Replace {'<app-id>'} with your  Apxor App ID. For more information about your App ID, refer to  [Apxor Application Identifier](https://guides.apxor.com/getting-started-with-apxor/adding-a-new-app#step-5-copy-the-application-identifier).
         </td>
       </tr>
     </tbody>
   </Table>
4. Enable **Basic Authorization** and enter the username and password provided by Apxor.
5. Click **Save**.

The webhook can now sync CleverTap segments with Apxor cohorts.

## Create Webhook Campaign in CleverTap

Once the webhook is ready, configure a campaign to send user data to Apxor.

1. Go to *Campaigns* on the CleverTap dashboard, click **+ Campaign** and select *Webhook* from the list of messaging channels.

<Image alt="Create Webhook Campaign" align="center" width="70% " border={true} src="https://files.readme.io/7385f799646e6e0bd1514d5f53cd2661f27b6c09e575a326990c9377a5f24e92-image.png" />

2. Configure the following campaign settings: qualification criteria, target segment, and delivery preferences.
3. Under the *What* section, select the webhook created in [Set Up Webhook in CleverTap](doc:apxor#set-up-webhook-in-clevertap).
4. Click **Go to Editor**, select Custom Profile Attributes under the *Webhook Content* and enter the following details:
   * Key: `apx_cohort_name`
   * Value: The name of the cohort in Apxor. You can also insert a dynamic variable (for example, `{'{{Cohort Name}}'}`) to send personalized cohort data.

<Image alt="Webhook Content" align="center" width="70% " border={true} src="https://files.readme.io/59c582a46fd495aa0bce988fe98ade7348351d12f55219a92109fc5a3711b525-image.png" />

6. Click **Preview & Test** to validate that the data sync works correctly.
7. Once verified, click **Publish**.

<Image alt="Publish" align="center" width="70% " border={true} src="https://files.readme.io/fe0b1bc4f485eb6760fa965b93acec9c1fe00d55f360aeefe65ea099cc9a4caa-image.png" />

A dynamic cohort appears in your Apxor dashboard, ready to be targeted for In-App experiences. Completing this integration establishes a seamless connection between CleverTap's segmentation power and Apxor's personalization capabilities. This helps deliver the right experience to the right user at the right time.