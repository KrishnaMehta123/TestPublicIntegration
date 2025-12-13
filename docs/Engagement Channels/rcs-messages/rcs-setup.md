---
title: Setup
excerpt: Understand how to set up RCS as a channel for your marketing campaigns
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

CleverTap supports RCS (Rich Communication Services) messaging natively, enabling businesses to deliver interactive and engaging messages directly to their users—without needing to rely on external integrations. This simplifies your messaging setup and ensures greater control, speed, and reliability.

To get started with RCS as a communication channel for your organization, please reach out to your CleverTap Account Manager or write to us at [sales@clevertap.com](mailto:sales@clevertap.com).

# Getting Started

Once RCS has been enabled for your organization, here are the key steps to help you get started:

- **RCS Agent Onboarding**: Your brand will need to be registered as an RCS agent with the selected provider. This process typically includes submitting business details, brand assets (like logos and color schemes), and use case descriptions. Your CleverTap Account Manager will guide you through the requirements and timelines.
- **[RCS Provider Setup](doc:rcs-setup#rcs-provider-setup) **: Learn how to set up RCS provider, including adding provider credentials, enabling click tracking, and managing provider settings such as editing, archiving, or deleting.  
- **[Create Template](doc:rcs-setup#create-template)**: Understand how to create, manage, and track the approval status of RCS templates. This section also covers cloning, testing, deleting templates, and using custom variables for personalization.  
- **[Create Message](doc:rcs-setup#create-message)**: Use the campaign builder to create and launch RCS message campaigns by selecting templates, configuring the message content, and publishing it to your target audience.  

This documentation ensures that you can deliver personalized, interactive RCS experiences at scale—while maintaining compliance and tracking performance effectively.

# RCS Provider Setup

To add a RCS  provider, perform the following steps:

1. From the dashboard, navigate to _Settings_ > _Channels_ > _SMS_ and select _SMS Direct_.
2. Click **+ Add Provider**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea1f1a5-1_Add_Provider_dashbboard.png",
        "Click +Add Provider to Add an SMS Provider",
        1074
      ],
      "align": "center",
      "border": true,
      "caption": "Add Provider"
    }
  ]
}
[/block]


3. Enter all the required information. To understand detailed steps of integrating RCS service providers with CleverTap, refer to this [document](doc:infobip-rcs).

   [block:image]{"images":[{"image":["https://files.readme.io/4564b5a071f19b50685b66e02b82156aa54f9f939050b7b0bb02e9b592b7ddf5-image.png",null,"RCS Provider Setup"],"align":"center","border":true,"caption":"RCS Provider Setup"}]}[/block]
4. Click **Save**.

## Provider Operations

This section describes the different user actions for the available RCS Message service providers.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f477e8e65c86770207384e2cd17fcbe6eecd4f4c8bff66d6cda4395cccbde59-RCS_Provider_Operations.png",
        "",
        "Service Provider Operations"
      ],
      "align": "center",
      "border": true,
      "caption": "Service Provider Operations"
    }
  ]
}
[/block]


### Edit Settings

You can edit the RCS provider settings to update the provider configurations.

Follow the steps to edit provider settings:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _SMS > SMS Direct_ > Providers tab.
- Click the ellipsis next to the provider.
- Select _Edit settings_ from the list. The provider credentials window displays.
- Update the required information.
- Click Send Test RCS Message to check that the provider is working correctly.
- Click **Save**.

### Archive Service Providers

You can archive any of the existing RCS service providers from the Settings section. Archiving a provider will impact any active Campaigns or Journeys associated with it, so it is important to review and stop any ongoing engagements before proceeding. Once archived, the RCS provider will no longer be available for use in the future. 

Follow the steps to archive an RCS Message service provider:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _SMS > SMS Direct_ > Providers tab.
- Click the ellipsis next to the provider.
- Select _Archive_ from the list. 

### Delete Service Providers

You can delete any of the current RCS service providers from the settings. Deleting a provider will impact any active Campaigns or Journeys associated with it, so it is important to review and stop any ongoing engagements before proceeding. The deleted provider will not be available for use in the future.

Follow the steps to archive an RCS Message service provider:

- From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _SMS > SMS Direct_ > Providers tab.
- Click the ellipsis next to the provider.
- Select _Delete_ from the list.

### Opt-in Users into RCS

Most people do not like receiving unsolicited messages via RCS. Therefore, it is important for you to explicitly request permission before sending RCS messages to your users. 

CleverTap does not require a separate subscription flag for RCS messages. Instead, we use the existing SMS subscription flag to manage preferences for both SMS and RCS. This approach aligns with how end users experience these messages—both SMS and RCS are delivered to the same inbox on supported devices.

If a user is subscribed to SMS, they are automatically eligible to receive RCS messages as well. Similarly, to opt users out of receiving both SMS and RCS notifications, you can set the SMS communication preference to false.

```json
"MSG-sms":false
```

You have the following two ways to opt-in users for RCS Messaging:

- [Opt-in via updating the user's profile property](https://developer.clevertap.com/docs/concepts-user-profiles#section-updating-the-user-profile). 
- [Opt-in via the API profile update](https://developer.clevertap.com/docs/upload-user-profiles-api). 

### Enable Click Tracking for RCS Messaging

You can track button clicks from your RCS messages. To enable click tracking:

1. From the dashboard, navigate to _Account > Settings > Engage > Channels > SMS_. Select _SMS Direct_.
2. Click one of the Provider names.
3. Click **+ Template** .
4. Add a CTA button. 
5. Select the URL type. 
   1. Static : Add a static link.
   2. Dynamic: Add a dynamic link. 
   3. CleverTap Link Tracking : Add the link for tracking user clicks. For example, [www.ct1.io/{{1}}](http://www.ct1.io/{{1}}). The URL will be automatically displayed for CleverTap BSP.

# Create Template

The [Add Template](doc:rcs-setup#create-message) feature in the CleverTap Dashboard allows you to create & monitor approval for RCS message templates for Indian users seamlessly. These templates ensure consistent messaging and are automatically submitted to registered providers (e.g., Vodafone, Jio) for approval and distribution.

- Once submitted, the template status is typically updated within 24 hours, and you can track its approval progress directly within the dashboard.
- By using pre-approved RCS templates, businesses can run personalized and engaging messaging campaigns while ensuring compliance with local telecom regulations.
- CleverTap supports three template formats:
  - [Text  ](doc:rcs-message-templates#text)
  - [Rich Card](doc:rcs-message-templates#rich-card-template)
  - [Carousel](doc:rcs-message-templates#carousel)

This feature enables businesses to automate messaging workflows, maintain brand consistency, and enhance customer communication through RCS campaigns.

To create or access templates:

1. Navigate to \_Settings > Partners > SMS > SMS Direct .
2. Select the provider setup where you want to add new templates.
3. Go to the _Templates_ tab.

## Clone

Cloning an RCS template allows you to quickly create a new version based on an existing one. This is useful for reusing layouts or content with slight modifications.

1. Navigate to _Settings > Channels > SMS > SMS Direct > RCS Provider > Templates > Select RCS Template_.
2. Click the ellipsis (three dots) next to the template you want to clone.
3. A window will open displaying the existing template's content. Enter a new template name and update any fields or media as needed.
4. Click **Save** to create the cloned template.

## Refresh Status

The **Refresh Status** option lets you manually check whether an RCS template has been approved by the provider. It ensures you’re working with the latest status before using the template in a campaign.

1. Navigate to _Settings > Channels > SMS > SMS Direct > RCS Provider > Templates > Select RCS Template_.
2. Click the ellipsis (three dots) next to the template whose status you want to refresh.
3. Select **Refresh Status**. The current status will be updated and displayed.

## Send Test

Sending a test RCS message allows you to preview how the template renders and behaves before using it in a live campaign.

1. Navigate to _Settings > Channels > SMS > SMS Direct > RCS Provider > Templates > Select RCS Template_.
2. Click the ellipsis (three dots) next to the template you want to test.
3. In the popup window, choose a test recipient using one of the following options:
   - **Select from Test Profiles**: Choose from predefined test user profiles within CleverTap.
   - **Search from Existing Profiles**: Look up and select real user profiles from your database.
   - **Send to Mobile Number**: Enter a specific mobile number manually to send the test message directly.
4. Click **Send Test** to deliver the test message.

## Delete

You can delete RCS templates that are no longer in use. This helps maintain a clean dashboard and prevents outdated templates from being used in future campaigns. Deleting a template will also stop any campaigns currently using it.

1. Navigate to _Settings > Channels > SMS > SMS Direct > RCS Provider > Templates > Select RCS Template_.
2. Click the ellipsis (three dots) next to the template you want to delete.
3. Select **Delete**. A confirmation window will display all campaigns that are using this template.
4. Click **Delete** to confirm. Any ongoing or scheduled campaigns using the template will be stopped.

### Custom Variables in RCS Messaging Templates

In CleverTap, when creating RCS message templates, you can include placeholders to personalize your messages. These placeholders are represented by double curly braces containing unique numbers, such as `{{1}}`, `{{2}}`, etc. Each placeholder corresponds to a variable that will be dynamically replaced with specific user information when the message is sent.

For Example: If you want to create a message like: "Hello [Name], Congratulations on your ticket booking. Here is your ticket number: [TicketNumber]. Please ensure you visit us on [VisitDate]. Enjoy your experience."

You should format the template as: "Hello {{1}}, Congratulations on your ticket booking. Here is your ticket number: {{2}}. Please ensure you visit us on {{3}}. Enjoy your experience.

Here, `{{1}}`, `{{2}}`, and `{{3}}` are placeholders that will be replaced with the user's name, ticket number, and visit date, respectively, when the message is sent.

**Important Guidelines:**

- **Unique Placeholders:** Ensure that each placeholder number is unique within the template to avoid any conflicts during personalization.

- **Consistent Numbering:** Maintain a consistent numbering sequence for placeholders to ensure clarity and proper mapping of variables.

This approach allows you to tailor your RCS messages to each recipient, enhancing engagement and providing a personalized experience.

# Create Message

To send RCS messages through CleverTap, you can use the [Create Message](doc:create-message) flow within the Campaigns section. This allows you to select your RCS provider, choose or create a message template, and configure your campaign settings—all within a streamlined builder designed for rich messaging experiences.

1. From the CleverTap dashboard, navigate to _Campaigns_.  
2. Click **+ Campaign**.  
3. Under the _Messaging Channels_ list, select **SMS**. In the SMS Campaign Builder, open the **Provider** dropdown and select **RCS Message Provider**.  
4. Go to the [Editor](doc:rcs-message-editor) section to use a pre-approved template or create a new one.  
5. Define all necessary sections of the message and click **Publish** to launch the campaign.