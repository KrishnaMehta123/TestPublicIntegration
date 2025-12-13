---
title: Storyly
excerpt: Understand how you can use CleverTap segments as an audience in Storyly
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

[Storyly](https://www.storyly.io/), an user engagement platform, enables brands to embed mobile-native stories in their mobile apps and websites through SDK integration. It creates an additional channel to deliver any marketing content in a full-screen and interactive format and communicate with users. This integrates helps with the following:

* Create Campaigns and Journeys to target the Past Behavior segments on CleverTap with stories or personalize their story experience
* Update your segment Storyly every time your Live Behavior segments on CleverTap are updated by their actions in your app.

For any issues regarding this integration, contact [Storyly Support Team](mailto:support@storyly.io).

# Prerequisites

The following are the prerequisites for this integration:

* Ensure that you complete the [Amazon EventBridge setup](doc:setup-amazon-eventbridge).
* Ensure that you pass Custom Parameter to the Storyly SDK. Also, ensure that the identifier you pass here is the same as that used with CleverTap, as it is used to identify the user. For more information on this, refer to [Passing Custom Parameter Recipe](https://docs.storyly.io/recipes/passing-custom-parameter).

# Connect CleverTap Audience with Storyly

This process involved the following two major steps:

1. [Set Up Amazon EventBridge](doc:storyly#set-up-amazon-eventbridge).
2. [Create an Audience for CleverTap on Storyly Dashboard](doc:storyly#create-an-audience-for-clevertap-on-storyly-dashboard).

## Set Up Amazon EventBridge

To set up Amazon EventBridge:

1. Log in to your CleverTap account and navigate to *Settings* > *Partners* page. Select *Amazon EventBridge* from the list.

<Image alt="Navigating to Partners Page" align="center" border={true} src="https://files.readme.io/38cb56585d54b2d24334f5d7e5e12892cb5cd9a0bbec7b79299f7813c886418c-Amplitude_Partner_Page.png">
  Navigating to Partners Page
</Image>

2. A popup opens on the right side of the screen. Enter the following details and click **Integrate**.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Field</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Partner Nickname</p>
      </td>

      <td>
        <p>Enter the <em>Nickname</em> for your integration.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>AWS Account ID</p>
      </td>

      <td>
        <ul><li>This user property is used as an identifier when sending event data to Amazon Eventbridge. </li><li>Enter <strong>374278225139</strong> in this field.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Region</p>
      </td>

      <td>
        <ul><li>Indicates the AWS account region to which the events need to be sent.</li><li>Select <em>EU (Ireland)</em> from the dropdown.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Enter Amazon EventBridge Project Details and click Integrate" alt={2366} align="center" border={true} src="https://files.readme.io/a9c4294-Integrate_raw_data_partner_-_Amazon_EventBridge.png">
  Enter Amazon EventBridge Project Details to Integrate
</Image>

## Create an Audience for CleverTap on Storyly Dashboard

After setting up the Amazon EventBridge on CleverTap, you need to create a unique token on the Storyly dashboard to complete the connection. To create a unique token on the Storyly dashboard:

1. Navigate to *Settings* from the Storyly dashboard and find *Audiences* under *Data Management* tab.
2. Click **+ New Audience** on the top right side and select *Create Audience for CleverTap*.

<Image title="Create an audience for CleverTap" alt={960} align="center" border={true} src="https://files.readme.io/01089f0-Create_audience_for_CleverTap.png">
  Create an Audience for CleverTap
</Image>

3. Enter the *Audience Name* to uniquely identify your audience and click **Continue**.\
   Storyly generates a *Key* and unique *Token* for your Audience. 
4. Copy the Key and Token values, as you will need them when creating Campaigns and Journeys on the CleverTap Dashboard.

You can now start creating Campaigns and Journeys with Amazon EventBridge on the CleverTap dashboard.

# Create Your First Campaign/Journey to Show Personalized Stories to Users

To create a campaign/journey:

1. Select *Amazon EventBridge* as the Messaging Channel when creating a campaign/journey.

<Image title="Create Amazon EventBridge Campaign or a Journey with Amazon EventBridge Engagement Channel" alt={1852} align="center" border={true} src="https://files.readme.io/78c7437-Select_Amazon_EventBridge.png">
  Create Amazon EventBridge Campaign or a Journey with Amazon EventBridge Engagement Channel
</Image>

2. Click **Go To Editor** under *What* section of campaign/journey.

<Image title="Create Amazon EventBridge Message - For Campaigns" alt={2850} align="center" src="https://files.readme.io/c90a214-Message_Editor_-_Campaigns.png">
  Create Amazon EventBridge Message - For Campaigns
</Image>

<Image title="Create Amazon EventBridge Message - For Journeys" alt={1047} align="center" border={true} src="https://files.readme.io/472d7ba-Message_Editor_-_Journeys.png">
  Create Amazon EventBridge Message - For Journeys
</Image>

3. Select *Custom Profile Attributes* and click *+ Key-Value Pair* to add the following mandatory key-value pairs and other key-value pairs as per your requirement:

* `storyly_token`\
  Enter the token you copied from the Storyly Dashboard in *step 4* of [Create an Audience for CleverTap on Storyly Dashboard](doc:storyly#create-an-audience-for-clevertap-on-storyly-dashboard) section.

* `operation`
  * For insert & update operations: upsert
  * To delete a user from the Audience: delete

<Image title="Adding Key-Value Pairs for Personalized Content" alt={2080} align="center" border={true} src="https://files.readme.io/35d7f52-Add_Key-Value_Pairs.png">
  Adding Key-Value Pairs for Personalized Content
</Image>

4. (Optional) Add user properties in the payload by adding new key-value pairs to personalize your content.
5. Click **Done**. 

For a detailed example of sending personalized stories, refer to this example listed in the [Storyly documentation](https://docs.storyly.io/page/connecting-clevertap-audiences-with-storyly).
