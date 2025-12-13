---
title: WhatsApp Editor
excerpt: The WhatsApp editor allows you to edit and design your messages.
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

The WhatsApp Editor is a feature available when building a WhatsApp message in CleverTap. It enables you to add content to pre-built templates or customize and build them. After creating a WhatsApp template, you can use it in the current campaign or save it for future campaigns.

From the *What* section in the WhatsApp campaign builder, select *Message Type* and click **Go to Editor**.  The WhatsApp template selection displays. 

<Image title="Email Editor Templates" alt={1424} align="center" border={true} src="https://files.readme.io/34efc8b-WhatsApp_all_templates.jpg">
  Select WhatsApp Template
</Image>

# WhatsApp Templates

Select the template from the template window and start editing it. The mandatory content is already defined during template creation. You can personalize or edit this information only where permissible. To create a template from the CleverTap dashboard, refer to[WhatsApp Template using CleverTap BSP](https://docs.clevertap.com/docs/clevertap-bsp#creating-whatsapp-message-templates). 

There are two types of templates available for creating campaigns:

* Basic Templates
* Limited-Time Offer Templates

## Basic Templates

From the WhatsApp editor, select the *Message Type* and click **Go To Editor**.  Select the approved template. For more information on creating templates from the CleverTap dashboard, refer to [WhatsApp Templates](https://docs.clevertap.com/docs/whatsapp-message-templates) 

<Image title="Whatsapp Editor" alt="Personalize the placeholders based on user/event properties and craft the template" align="center" border={true} src="https://files.readme.io/98aa909-Whatsapp_editor_create_message.png">
  Personalizing Message
</Image>

### Header

Provide information if required, or use @ to [personalize](clevertap) the header.

### Body

The body text is populated based on the template. Enter the [personalized values for the placeholders](https://docs.clevertap.com/docs/personalize-message-whatsapp) in the body text.

```
Thank you for choosing ACME airlines as your flying partner for the journey from {{1}}  to journey {{2}}. Hope to serve you again soon. 


```

### Footer

The footer can contain information such as a phone number for support, or guide the user for actions such as opting out of a marketing campaign. This information has already been added.

### Call to Action Buttons

Call to Action (CTA) can be the following types:

* **Copy Code**:  Enter the Offer Code. The user can copy the code with this button.
* **Visit Website**: This is a website redirect for this button. The *Visit Website* CTA button in WhatsApp templates supports static and dynamic redirection URLs:
  * **Static**: Static Redirection URLs are defined in the templates and cannot be changed in the campaigns. Check the static URLs to ensure you are using the intended URLs. 
  * **Dynamic**:  WhatsApp allows users to use dynamic links that can be customized while creating the campaigns. URL prefix must be defined during template creation, and URL suffix can be customized during campaign creation. You can use a fixed suffix, or you can personalize it so that each qualified user in the campaign receives a  different website redirection.
* **CleverTap click tracking**: CleverTap click tracking allows you to personalize the entire URL while also tracking the clicks on these CTAs. This allows you to measure campaign performance more accurately. For more information, refer to [Track Clicks in WhatsApp Campaigns](https://docs.clevertap.com/docs/create-message-whatsapp#track-clicks-in-whatsapp-campaigns).

### Quick Reply Button

You can add up to five *Custom* buttons and one *Marketing Opt Out* button.

* *Custom Quick Reply*: These buttons are a great way to nudge your end-users to send specific replies to your WhatsApp campaigns. You can show the list of responses that your users can select with just a tap. You can add the custom payload (key values pairs) to track a specific quick reply button.
* *Marketing Opt Out*: You can add your unsubscribe keywords and allow users to easily opt-out from your future WhatsApp campaigns.

## Limited Time Offer Template

 Businesses can use the  Limited Time Offer Template from the CleverTap dashboard to send promotional messages containing time-sensitive offers to their customers.

> 📘 Limited Time Offer Template availability
>
> This template is available only for CleverTap Provider (WhatsApp Direct).

Meta offers various types of limited-offer templates, including:

* Product specific: Highlight deals on specific products or categories.
* Seasonal: Promote offers around holidays or special events.
* Flash sales: Advertise short-duration, high-discount offers.
* Subscription incentives: Encourage sign-ups with limited-time benefits.

Components of a limited-time offer.

The limited-time offer has the following components:

<Image alt="Limited Time Offer Message Components" align="center" width="50% " border={true} src="https://files.readme.io/cd2ade8-LTO_sample.png">
  Limited Time Offer Message Components
</Image>

### Header

Upload an image or use personalized [personalized](clevertap) media.

### Limited Time Offer Section

The offer title cannot be edited. Select an expiration timestamp.  It can be a fixed date and time or a personalized user property, such as an anniversary date. 

### Body

The body text is populated based on the template. Enter the personalized values for the placeholders in the body text. Following is an example:

```
Thank you for choosing ACME airlines as your flying partner for the journey from {{1}}  to journey {{2}}. Hope to serve you again soon. 


```

### Footer

A footer is not supported for the limited-time offer template.

### Call to Action Buttons

Call to Action (CTA) can be the following types:

* **Copy Code**:  Enter the Offer Code. The user can copy the code with this button.
* **Visit Website**: It is the website redirect for this button. The *Visit Website* CTA button in WhatsApp templates supports static and dynamic redirection URLs:
  * **Static**: Static Redirection URLs are defined in the templates and cannot be changed in the campaigns. Check the static URLs to ensure you are using the intended URLs. 
  * **Dynamic**:  WhatsApp allows users to use dynamic links that can be customized while creating the campaigns. URL prefix must be defined during template creation and URL suffix can be customized during campaign creation. You can use a fixed suffix, or you can personalize it so that each qualified user in the campaign receives a  different redirection. 
  * **CleverTap click tracking**: CleverTap click tracking allows you to personalize the entire URL while tracking the clicks on these CTAs. This allows you to measure campaign performance more accurately. For more information, refer to [Track Clicks in WhatsApp Campaigns](doc:create-message-whatsapp#track-clicks-in-whatsapp-campaigns).

### Quick Reply Button

You can have up to five *Custom* buttons and one *Marketing Opt Out* button.

* *Custom Quick Reply*: These buttons are a great way to nudge your end-users to send specific replies to your WhatsApp campaigns. You can show the list of responses that your users can select with just a tap. You can add the custom payload (key values pairs) to track a specific quick reply button.
* *Marketing Opt Out*: You can add your unsubscribe keywords and allow users to easily opt-out from your future WhatsApp campaigns.

The *Copy offer code* and Website redirection buttons are automatically added to the Limited Time Offer Template. You can add up to two website redirection buttons and a button for calling a phone number.

## Carousel Template

Businesses can use the Carousel templates to craft a single text message featuring up to 10 dynamic carousel cards. This enables the recipients to scroll horizontally through a series of engaging content.

<Image alt="Carousel Template" align="center" width="500px" border={true} src="https://files.readme.io/81e0485-carousel.webp">
  Carousel Template
</Image>

The Carousel template has the following components:

### Message Bubble

The Carousel message is populated based on the configured template. In the message field, enter the personalized values for the placeholders. For example

```
Hey {{1}},! The great billion day sale is live! Do not miss out on the flash sale.
```

### Carousel Card

You can add upto up to 10 carousel cards within a template, each comprising the following components:

* **Card Header**: Upload visually appealing images to promote the product or services (maximum of 10) within the header.
* **Card Body**: The body text is populated as per the configured template. Enter the personalized values for the placeholders in the body text. Following is an example:

```
Thank you for choosing ACME airlines as your flying partner for the journey from {{1}}  to journey {{2}}. Hope to serve you again soon. 


```

* **Card Buttons**: You can add up to three buttons for user action. These buttons prompt users to purchase, visit a website, or access additional content.
  * **Quick Reply** - *Quick Reply* buttons are a great way to nudge your end-users to send specific replies to your WhatsApp campaigns. You can show the list of responses that your users can select with just a tap.
  * **Call Phone Number** - The *Call Phone Number* instantly nudges users to make a call.
  * **Visit Website** -  The Visit Website button redirects your users to the desired web page.\
    The *Visit Website* CTA button supports static and dynamic redirection URLs. Static Redirection URLs are defined in the templates and cannot be changed in the campaigns. WhatsApp allows users to use dynamic links that can be customized while creating the campaigns. The URL prefix must be defined during template creation, and the URL suffix can be customized during campaign creation.

# Quick Reply

You can add up to five custom quick reply buttons and a Marketing opt-out button. It is recommended to add a marketing opt-out button to raise your reputation with WhatsApp.  Use *Body* to give clear instructions for Opt-outs, such as 'Tap Stop to Opt-out.' The Marketing opt-out button does not automatically unsubscribe users.  You must configure one of the [unsubscription flows](https://docs.clevertap.com/docs/whatsapp-subscription-management) based on incoming keywords.

## Quick Reply Button with Custom Payload

CleverTap's *Quick Reply* feature enables you to easily collect user information, track responses, and trigger chat workflows using custom payloads.

The custom payload can include custom attributes with the *Quick Reply* button in the Quick Reply templates when creating campaigns. These custom attributes are not visible to the end user. The purpose of these attributes is to track end-user responses when interacting with specific Quick Reply buttons.

To send a custom payload from the Quick Reply button, you can utilize the [WhatsApp Editor](https://docs.clevertap.com/docs/create-message-whatsapp#whatsapp-editor) provided by CleverTap. When users reply to the Quick Reply message, the custom payloads are returned along with their responses. These custom payloads can trigger chat workflows and enable further actions based on the user's reply.

To send a custom payload from the WhatsApp Editor, select a Quick Reply template and then select *Add Custom Payload*.  

Add a custom payload. You can also [personalize](https://docs.clevertap.com/docs/personalize-message-whatsapp#message-personalization) the custom payload.

<Image alt="Add a Custom Payload" align="center" border={true} src="https://files.readme.io/862aa69-small-quick_reply_button.png">
  Add a Custom Payload
</Image>

> 📘 Character Limit for Custom Payload
>
> Check that your custom payload is under **128** characters to ensure deliverability. Although CleverTap does not restrict characters in a custom payload, WhatsApp limits it to 128 characters.

For example, a bus service called ACME operates within a city. ACME wants to make it easy for regular passengers to confirm their daily bus rides. To do this, ACME sends reminder notifications in the evening and morning, matching each user's typical travel schedule.

When a passenger receives the notification, they see a *Confirm Ride* button. This button enables them to quickly respond and indicate their intention to travel with the bus service immediately. Now, depending on how ACME sets up its system, there are two possible scenarios:

* Without Custom Payload: If ACME does not use a custom payload when a user clicks on the *Confirm Ride* button, the user's response is sent directly to ACME's WhatsApp phone number. However, it is unclear to which specific notification the user is responding. For example, ACME does not know whether the user is confirming their ride for today's notification or a previous one. In this case, ACME needs more information, such as the ride details and route, to generate a payment link and complete the transaction.
* With Custom Payload - When ACME sends the WhatsApp notification, it includes personalized information about the user's route and timing. There is also a *Confirm Ride* button with a unique identifier attached as a custom payload. This allows ACME to distinguish between different notifications and campaigns. The response and custom payload are captured when the user clicks the *Confirm Ride* button. This means ACME knows the exact notification that received a user response. ACME can now directly share the payment link with the user to complete the transaction.

The custom payload feature simplifies the process for ACME and its passengers. It eliminates the need for additional confirmation workflows and ensures users receive the correct payment link for their intended ride. Ultimately, this helps ACME provide its customers with a smoother and more efficient experience.

# Track Clicks in WhatsApp Campaigns

The WhatsApp click tracking feature in Meta Dashboard allows you to track the clicks on the CTA (Call To Action) included in your WhatsApp messages. By enabling click tracking, you can gain valuable insights into user engagement and optimize the performance of your WhatsApp campaigns. 

<Image alt="WhatsApp Click Tracking Message " align="center" width="25% " border={true} src="https://files.readme.io/d82dc12-Whatsapp_click_track_end_user.jpg">
  WhatsApp Click Tracking Message
</Image>

> 🚧 Click Tracking Availability and Expiration for shortened links
>
> Click tracking is available only for CleverTap BSP. Additionally, the shortened URLs from the WhatsApp campaigns expire in seven days.  If you try accessing these shortened links after seven days you will receive a 404 error.

## Key Points to Remember

Let us understand how to track a click for various template fields in WhatsApp campaigns. 

### Headers

* Click tracking is available only for text headers.
* When using custom variables (for example, \{\{1}}) in text headers, the system automatically detects URLs in the input box and provides an option to enable click tracking.

<Image alt="Click Track Text Header" align="center" border={true} src="https://files.readme.io/e14bea3-Whatsapp_editor_click_track_header_.jpg">
  Click Track Text Header
</Image>

* *Example*: If you enter a URL such as  [https://example.com](https://example.com) in a custom variable, the system will automatically detect it and give you the option to enable click tracking. The link will be wrapped (for example, [https://ct1.io/8eytiry](https://ct1.io/8eytiry)), capturing click information before redirecting the user to the actual URL.

### Body

* When using custom variables (for example, \{\{1}}) in the message body, the system automatically detects URLs in the input box and provides an option to enable click tracking.

<Image alt="Click Track Message Body" align="center" border={true} src="https://files.readme.io/3234965-Whatsapp_editor_click_track_body.jpg">
  Click Track Message Body
</Image>

* *Example*: If you include a URL like [https://example.com](https://example.com) in a custom variable input box, the system will detect it and allow you to enable click tracking. The link will be wrapped (for example, [https://ct1.io/8eytiry](https://ct1.io/8eytiry)), capturing click information before redirecting the user to the actual URL.

### Footer

Click tracking is not supported for footers because footers cannot be dynamic.

### CTAs

* To track clicks on CTAs within WhatsApp templates, you must create *Dynamic URL type CTA* templates with CleverTap tracking domains in the WhatsApp Account Manager.
* Save these templates as *CleverTap click tracking type templates* in the CleverTap dashboard.
* *Example*: To track clicks on a *Visit Website* CTA, create a template with the CTA set as a CleverTap click tracking type. Enter the complete redirection URL in the *What* section during the campaign creation. The link will be wrapped (for example, [https://ct1.io/8eytiry](https://ct1.io/8eytiry)), capturing click information before redirecting the user to the actual URL.

<Image alt="Click Track CTA" align="center" border={true} src="https://files.readme.io/92ab31c-Whatsapp_editor_click_track_button.jpg">
  Click Track CTA 
</Image>

# Import Templates

> 🚧 Template Import Limitations for External Providers
>
> Importing templates is exclusive to CleverTap BSP, and for other providers, you must recreate templates separately within their interfaces.

You can also import templates when creating a new message. 

1. Click *Go To Editor* to create your message.
2. From the message editor, click **Import Templates**. A window for *Import Templates* displays.

<Image alt="Add or Replace Templates" align="center" width="60% " border={true} src="https://files.readme.io/d48c8e0-2023-09-25_17-21-03.jpg">
  Add or Replace Templates
</Image>

4. Click *Import* to replace all the templates on your CleverTap dashboard. 
5. Click **Continue** to replace templates.  The CleverTap dashboard shows the new templates. Your previous templates are mailed to your email account.

> 📘 Template Import Impact on Failing WhatsApp Campaigns
>
> Importing templates will not automatically resolve errors or issues related to the existing WhatsApp campaigns or journeys. These campaigns and journeys will continue to fail until you manually update the imported template in the affected campaign's *What* section.
>
> To address campaign failures resulting from template-related errors, please follow the below steps:
>
> 1. Identify the specific campaign or journey that is encountering the error.
> 2. Access the *What* section of the campaign or the specific journey node.
> 3. Edit the campaign or journey and select the specific imported templates.
