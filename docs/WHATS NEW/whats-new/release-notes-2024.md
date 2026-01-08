---
title: Release Notes 2024
excerpt: >-
  Stay ahead with CleverTap's 2024 releases in customer engagement and
  retention.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Types of Product Releases

The following table describes the different types of product releases:

| Release                                              | Description                                                                                                                            |
| :--------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://files.readme.io/bbc3552-PrivateBeta.svg) | This release is rolled out to a selected set of customers as an early preview for use case validation and feedback.                    |
| ![](https://files.readme.io/7776b09-Beta.svg)        | This release is made available to a wider set of customers to test out deeper use cases and feedback.                                  |
| ![](https://files.readme.io/c30bf56-NewFeature.svg)  | This is a new functionality in the product, expanding its capabilities or solving new use cases.                                       |
| ![](https://files.readme.io/7f99f23-Tags-1.svg)      | Improvements or upgrades to existing product capabilities focused on increasing performance, usability, or adding minor functionality. |
| ![](https://files.readme.io/0c15d9f-Tags.svg)        | Updates to existing product capabilities, such as bug fixes, performance improvements, security enhancement, and so on.                |

*Any new feature, enhancement, or update without a Beta or Private Beta tag is considered a General Availability (GA) release.

# 2024

## December

### Introducing Reusable Content Blocks for greater efficiency ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to introduce Content Blocks in CleverTap’s Content Manager. Content Blocks are reusable snippets for standardized elements, such as footers, logos, or disclaimers.

<Image align="center" alt="Footer Standardization with Content Blocks" border={true} caption="Footer Standardization with Content Blocks" src="https://files.readme.io/686373549b6ac569fd3abb3ab7bafddabdd0b37236d60ce08b551e2a559309e1-image.png" />

These blocks are designed to simplify the reuse of content across email campaigns, saving you valuable time. They help you maintain consistent messaging and standardize your brand communication.

For more information, refer to [Content Blocks](doc:content-blocks) and [Content Block APIs](https://developer.clevertap.com/docs/content-blocks-api).

### Store Outgoing Messages Using Message Archiving ![](https://files.readme.io/7776b09-Beta.svg)

Message Archiving now supports Google Cloud Platform (GCP), allowing customers to store copies of outgoing messages across different channels in real-time directly in their GCP bucket. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets, Azure Blob, and GCP buckets.

For more information, refer to [Message Archiving](doc:message-archiving).

### Introducing Customizable URL Schema for SMS Campaigns ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to introduce a new enhancement that allows you to shorten and customize the links in your SMS messages. This means you can create links that match your brand, comply with TRAI regulations, and ensure smooth delivery to customers, all while improving campaign performance.

With this enhancement, you can include sender IDs in SMS URLs for seamless DLT whitelisting and create personalized URL structures that align with your branding. This ensures uninterrupted delivery and enhances customer engagement.

For more information, refer to [URL Whitelisting for SMS Marketing Campaigns](doc:sms-regulations#url-whitelisting-for-sms-marketing-campaigns).

### Enhanced Delivery Triggers for Web Pop-ups ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to unveil our new and improved web pop-up triggers that enable timely and relevant messaging. The new triggers are based on various user interactions, such as scrolling behavior, inactivity, encountering a timed delay, or attempting to exit the webpage on a desktop.

For more information, refer to [Triggers for Campaign Delivery](https://docs.clevertap.com/docs/create-message-web-popup#triggers-for-campaign-delivery).

### Analyze Notifications Sent Using Journeys Labels ![](https://files.readme.io/7f99f23-Tags-1.svg)

You can now use Journey labels in the _Analytics_ section to analyze the _Notifications Sent_ event. You can now easily track and derive insights from notifications sent through Journeys tagged with specific labels.

<Image align="center" alt="Analyze Journey Performance Using Journey Labels" border={true} caption="Analyze Journey Performance Using Journey Labels" src="https://files.readme.io/7f26df255f646c42fcdfbb0a6760afa7be9495d671c751f7d2d28431e2000008-Analyze_Journey_Performance_Using_Journey_Label.png" />

For more information, refer to [Assign Label to Journeys](doc:journeys-list#assign-label-to-journeys).

### Enhanced Entry Timelines in Journey Setup ![](https://files.readme.io/7f99f23-Tags-1.svg)

CleverTap has redesigned _Journey Entry Timelines_ to remove redundancies and improve usability. Also, the error handling has been improved to manage scenarios such as incorrect date or day of recurrence inputs.

These enhancements ensure a smoother, more intuitive Journey setup process for all CleverTap users.

For more information, refer to [Define Journey Entry Timelines](doc:setup-journey#define-the-journey-entry-timelines).

### Custom Headers and Message Extras for Enhanced Email Analytics ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

You can now enhance your email tracking and analytics capabilities with Custom Headers and Message Extras. This feature enables you to add key-value pairs to email headers and bodies, offering seamless integration with third-party tools and internal systems. It is available for users with Sendgrid, Amazon SES, Generic SMTP, and Infobip (Advanced Email Add-on).

For more information, refer to [Custom Headers](doc:create-message-email-custom-kv#custom-headers) and [Message Extras](doc:create-message-email-custom-kv#custom-extras).

## November

### AppsFlyer OneLink Integration for Email ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Introducing the updated AppsFlyer OneLink integration for Email. This new version makes it easier for users to set up and track clicks by managing everything from the AppsFlyer dashboard. You no longer need to configure anything on the CleverTap dashboard. The setup is now fully managed from the AppsFlyer dashboard itself, removing the need for configuration on CleverTap.

The older integration is no longer available, so you must switch to the new setup to keep using it. Currently, this integration supports Sendgrid ESP only. To enable it, contact [AppsFlyer support](https://www.appsflyer.com/company/contact/).

For more information, refer to [AppsFlyer OneLink Integration](doc:appsflyer-onelink#set-up-appsflyer-onelinks).

### Campaign ID Personalization for Email ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Campaign ID Personalization is now available in both the _Email HTML (Rich Media) Editor_ and _Drag & Drop Editor_, giving you more flexibility when personalizing email campaigns. You can create unique links and track engagements more accurately.

With Campaign ID Personalization, you can:

* Personalize URLs with campaign IDs for better attribution and tracking.
* Integrate easily with external tools to analyze engagement and meet custom analytics needs.
* Automate workflows using campaign IDs as payloads for custom key-value pairs.

For more information, refer to [Campaign ID Personalization](doc:personalize-message-email#campaign-id-personalization).

### Event Personalization Beyond 24 Hours for Email ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

You can now apply Event Personalization to _Live Action_ and _Date Time_ campaigns with a delay of more than 24 hours. Create highly personalized Email campaigns based on event properties broadening the window for event-triggered communications to create custom-tailored notifications, driving better targeting and relevance.

For more information, refer to [Personalize Message ](doc:personalize-message-email).

### OAuth 2.0 for Webhook Campaigns ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to offer a more secure and streamlined way to connect to your webhook endpoints. By adopting OAuth 2.0 authentication, we align with industry-standard security protocols to safeguard your interactions with external APIs while improving efficiency and ease of use.

Enhance your Webhook security and efficiency with:

* **OAuth 2.0 Authentication:** Robust security for webhook connections.
* **Flexible Grant Types:** Support for _Password Credentials_ and _Client Credentials._

For more information, refer to [OAuth 2.0](doc:setup-webhooks#oauth-20).

### Amazon SES Email Delivery via HTTP Protocol ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

CleverTap’s email delivery system now supports the HTTP protocol with Amazon Simple Email Service (SES), enabling faster and more efficient email delivery compared to the traditional SMTP protocol.

Existing Amazon SES integrations that are using SMTP can now switch to HTTP by updating the provider setup with the required additional details.

For more information, refer to [Amazon Simple Email Service (SES)](https://docs.clevertap.com/docs/amazon-simple-email-service).

### Support for Azure Blob in Message Archiving ![](https://files.readme.io/7776b09-Beta.svg)

Message Archiving now supports Azure Blob. It allows customers to store copies of outgoing messages across different channels in real-time. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets and Azure Blob.

For more information, refer to [Message Archiving](doc:message-archiving).

## October

### Elevate Your Marketing Strategy with TikTok Remarketing ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to announce that CleverTap now supports TikTok as a remarketing channel. This integration empowers our customers to leverage CleverTap’s powerful segmentation capabilities to upload user data into TikTok Audiences, enabling advanced retargeting campaigns.

> 📘 Private Beta
>
> TikTok Remarketing is currently released in Private Beta. For early access, contact your Customer Success Manager or Account Manager.

<Image align="center" alt="TikTok Remarketing" border={true} caption="TikTok Remarketing" src="https://files.readme.io/8989db3a6e9d984763aac232b75f7cee3e0cf1b269109c2653bf85970623f078-image.png" width="100% " />

Maximize your reach with targeted TikTok ads by:

* **Retargeting Campaigns**: Reach users who have previously engaged with your app or website, increasing conversion rates by connecting with them on TikTok, a frequently used platform.
* **Abandoned Cart Recovery**: Remind users who abandoned their carts with personalized TikTok ads, encouraging them to complete their purchases.
* **Lapsed User Re-engagement**: Reignite interest among users who have not interacted with your app or service recently, capturing their attention through TikTok ads.
* **Cross-platform Campaigns**: Boost user engagement by combining TikTok with other channels like Push or Email to create cohesive multi-channel remarketing strategies.
* **Lookalike Audience Expansion**: Identify converted user behaviors to create lookalike audiences, targeting potential new customers with similar characteristics.

For more information, refer to [TikTok Remarketing](doc:tiktok-remarketing).

### WhatsApp Carousel Templates Now Available for Gupshup ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce that carousel templates are now available for CleverTap using Gupshup with CleverTap. You can now create interactive WhatsApp campaigns with up to 10 dynamic carousel cards, allowing recipients to scroll through engaging content.

With Carousel Templates on CleverTap Gupshup, you can now:

* **Message Bubble**: Offers up to 1024 characters for detailed context.
* **Carousel Cards**: Each card includes:
  * **Card Header**: Add a media type which can be either Image or Video.
  * **Card Body**: Add up to 160 characters for concise messaging.
  * **Card Buttons**: Add up to two action buttons per card.

Use Cases:

* **E-commerce**: Showcase products or promote flash sales to drive purchases.
* **Fintech**: Highlight investment options or provide financial education.
* **Food Delivery**: Display menu highlights or specialty dishes to entice users.

For more information, refer to [Gupshup](doc:gupshup).

### Compare Trends Across Time ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

You can now compare an event across different time periods. For example, a user can display the count of users for the _Charged_ event for Week 1 and Week 2 in the same chart. The trend line for Week 2 will be displayed as a dotted line so that it is easy to distinguish it from the Week 1 trend line. It helps create a visual comparison to quickly spot trends and differences across time frames.

<Image align="center" alt="Compare Trends in different time periods" border={true} caption="Compare Trends Between Different Time Periods" src="https://files.readme.io/a105d0d551ff34f815b22214179e27afbc372155fd0719d07a83baf0bca32217-trends_compare.gif" />

For more information, refer to [Compare Trends Between Time Periods.](https://docs.clevertap.com/docs/trends-v2#compare-trends-between-time-periods)

### Notification Failed Event for Email Analytics ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Announcing a significant enhancement to our Email Analytics: the _Notification Failed_ event that gives you more deeper insights into campaign errors. With this update, CleverTap captures a _Notification Failed_ event, along with the reason for failure, enabling better targeting and resolution.

* **Improved Targeting:** Target users through alternate channels when errors occur. For example, if users encounter soft bounce errors, you can re-target them via other channels.
* **Cleaner Email List:** Unsubscribe users with persistent errors to maintain an accurate and engaged subscriber base.
* **Error Analysis:** Analyze the root causes of errors to resolve issues and optimize future engagements.

For more information, refer to [Notification Failed Event.](https://docs.clevertap.com/docs/events#:~:text=Notification%20Failed,in%20the%20campaign)

### Subscription Group Insights in Email Campaign Analytics ![](https://files.readme.io/7f99f23-Tags-1.svg)

The new Subscription Group Insights in Email Campaign Analytics will allow you to have a more granular view of unsubscribes by subscription group providing detailed insights, including:

* **Group-Level Unsubscribes and Resubscribes:** Track the number of unsubscribes and resubscribes for each targeted subscription group from your campaign stats.
* **Comprehensive Subscription View:** View the activities of the targeted subscription groups. Additionally, you can track any changes made through the Email Preference Center for other subscription groups.
* **Enhanced Analytics:** Understand user behavior better by analyzing how different subscription groups engage with your campaigns.

For more information, refer to the documentation links below:

* [Campaign Stats (for customers with cc/bcc Beta)](doc:email-campaign-stats-cc-bcc-group-unsubscribe)
* [Campaign Stats (all other customers)](doc:email-stats)

## September

### DND in Journeys ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

The updated DND feature sends notifications delayed by DND at their original scheduled time instead of right after the DND period ends. For example, a message was scheduled for 10 AM but was postponed due to a DND setup between Friday at 9 PM and Monday at 9 AM. The message will now be sent on Tuesday at 10 AM and not immediately after DND ends at 9 AM on Monday. This ensures a more controlled and user-friendly notification delivery experience.

<Image align="center" alt="DND in Journeys" border={true} caption="DND in Journeys" src="https://files.readme.io/6484ade9dd9a326b59d5028ee3e318bccc100934a463a0294fd65492907ba7ea-DND_in_Journeys.png" />

For more information, refer to [DND and Timezone](https://docs.clevertap.com/docs/dnd-in-journeys#dnd-and-timezone).

### Introducing Throttling in Journeys ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

You can now set throttling limits from the Journey Setup. This allows smoother regulation of message delivery rates during large-scale engagements.

<Image align="center" alt="Set Up Throttle Limits from Journeys" border={true} caption="Set Up Throttle Limits from Journeys" src="https://files.readme.io/a952feef88184d47da95cbeb1d8d8b7aef29b46eb2886a34a49c59bfba54c0a6-Set_Up_Throttle_Limits_from_Journeys.gif" />

With this enhancement, you can:

* Control message delivery rates directly within the Journey, ensuring more efficient communication.
* Prevent system overload and maintain optimal app and web performance, even during high-volume campaigns.

For more information, refer to [Throttling in Journeys](doc:messaging-frequency-caps#throttle).

### Introducing Folders in Content Manager ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to introduce the addition of folders to the Content Manager. This enhancement is designed to streamline file management, providing a more efficient organization of files.

<Image align="center" alt="Caption: Manage Content Folders in Files" border={true} caption="Manage Content Folders in Files" src="https://files.readme.io/03a1110c2de7b3575d14e09ae17df33348f6ead9fac4854bbb44a40486e95ec7-image-20241003-153613.png" />

With the new folders feature, you can now have:

* **Folders in Files**: Create folders within the Files section, making it easier to categorize and manage your digital assets.
* **Nested Folders**: Create up to 10 levels of nested folders, offering flexibility for organizing complex files.
* **Enhanced File Management**: Effortlessly copy, move, rename, and delete files within their respective folders.
* **File Search**: Quickly search within folders for faster access to files.

For more information, refer to [Organize Files Using Folders](doc:content-manager-files#organize-files-using-folders).

### Emoji Support within Push Notification Editor ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to introduce an enhanced Push Notification Editor that allows customers to effortlessly add emojis directly. You can access all personalization options from below the text field. This makes it easier and faster to create engaging messages.

<Image align="center" alt="Emoji Support Within Push Editor" border={true} caption="Emoji Support Within Push Editor" src="https://files.readme.io/62c28fee13c67880b112d93ff1062defd40c27cf4f9fc0b9d751cbc1acddd269-image-20241008-155442.png" />

For more information, refer to [Create Push Campaign](doc:create-message-push#push-editor).

### Personalized Sender and Reply-To Fields in CleverTap Email ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to introduce a new enhancement to our email personalization features. You can personalize the From Address and Reply-To fields using user and event properties. This allows for a more tailored email experience, enhancing engagement. It is currently available for Sendgrid, Amazon SES, and generic SMTP setups.

Transform your email strategy:

* **Streamlined Communication**: Direct interaction with designated contacts.
* **Enhanced User Engagement**: Increased interaction with personalized addresses.
* **Seamless Collaboration**: Reduces manual follow-ups and promotes smoother workflows.

For more information, refer to:

* [Provider Setup](doc:setup-sender-details)
* [Campaign Setup](doc:create-message-sender-details#sender-details)

### Auto-Append Link Parameters

We are excited to introduce Auto-Append Link Parameters, a new feature that automatically appends essential tracking parameters, such as UTM and campaign specific custom link parameters, into your email campaign links. For example, during a Seasonal Sale Campaign, an online clothing retailer uses Auto-append Link Parameters to automatically add UTM tags to email links. This saves time and ensures consistent tracking. They discover higher engagement with links tagged `utm_content=mens_clothing`, allowing for targeted marketing strategies. Overall, it simplifies link management and enhances campaign performance.

Key Features:

* **Global Link Parameters**: Set up and save key-value pairs for all your projects to automatically append UTM and custom parameters to your links.
* **Easy** Management: You can easily clone, edit, or delete link parameters—the changes do not impact already sent emails.
* **Effortless URL Creation**: Select saved parameters such as `utm_source`, `utm_medium`, `utm_campaign` and so on to eliminate the need for manual input. These parameters will be automatically applied to your campaign links.
* **Personalization Support**: Tailor links for your audience, allowing for more personalized experiences and improved performance tracking.

For more information, refer to [Auto Append Link Parameters](doc:auto-append-link-parameters).

### Introducing Real-time Message Archiving ![](https://files.readme.io/7776b09-Beta.svg)

CleverTap recently released Message Archiving, which allows customers to store copies of outgoing messages across different channels in real-time to their AWS S3 bucket. Key benefits include enhanced compliance evidence, improved trust and transparency, and minimal setup and maintenance. The feature is in Public Beta and available to all CleverTap customers using S3 buckets.

For more information, refer to [Message Archiving](doc:message-archiving).

### Uncover True Growth Drivers with CleverTap and AppTrove Integration ![](https://files.readme.io/c30bf56-NewFeature.svg)

We're thrilled to announce our latest integration with **AppTrove by Trackier**, a leading attribution platform that takes your marketing strategy to the next level! With this integration, you can now seamlessly transfer the attribution data for all your organic and non-organic app installations to CleverTap.

Key Benefits:

* **Precise User Acquisition Insights**: Understand exactly where your users are coming from and create tailored onboarding experiences to boost engagement and retention.
* **Optimized Acquisition Channels**: Identify the most effective user acquisition channels, allowing you to evaluate the quality of these acquisitions for more informed business and investment decisions.
* **Enhanced Campaign Effectiveness**: Utilize detailed attribution data to develop highly personalized and impactful campaigns, ensuring the right message reaches the right user based on their acquisition source and behavior.
* **Comprehensive Campaign Tracking**: Track ‘Install Events’ and ‘In-App Events’ effortlessly and measure campaign performance across multiple publishers from a unified dashboard.

For more information, refer to [AppTrove](doc:clevertap.com/docs/apptrove).

### Transform Your Email Template Creation with CleverTap and Taxi for Email Integration ![](https://files.readme.io/c30bf56-NewFeature.svg)

We're excited to announce our integration with **Taxi for Email**, a leading CMS platform for email marketers. Customers can now add their Taxi for Email email templates to CleverTap with just a single click. Marketing teams can now create high-quality emails quickly and accelerate time-to-market.

Key Benefits:

* **Streamlined Workflows**: Helps craft fully customized email templates and push them directly into CleverTap with a click.
* **Faster Time-to-Market**: Allows responding to quickly changing market trends by reducing the time it takes to move email campaigns from Taxi for Email Builder to the user's inbox.
* **Combined or Integrated Personalization Gains**: Drives higher engagement and conversion rates by combining Taxi for Email’s personalization features with CleverTap to tailor emails to each customer.

For more information, refer to [Taxi for Email](doc:taxi-for-email).

### Link Events to User Properties ![](https://files.readme.io/7776b09-Beta.svg)

We are excited to introduce the Link Events to User Properties feature in Public Beta. This feature enables you to trigger campaigns and actions based on changes in user properties. For example, in a gaming app, you can engage users whenever they complete a game level.

Key Features:

* **Time Series Updates**: Track changes to user properties over time for a complete view of user profiles.
* **Engagement Triggers**: Automatically activate campaigns when user properties change.

> 📘 Note
>
> This feature is available for Offline and In-App channels (CleverTap SDKs 7.0.0 and above).

For more details, refer to [Create Linked Event for User Property](doc:schema-create-linked-events#create-linked-event-for-user-property).

### Enhanced CleverTap Trends for Deeper Insights ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Unveiling the fresh new look of CleverTap Analytics! With enhanced user experience and updated visualization in CleverTap Trends, customers can quickly uncover valuable insights. Additionally, we now provide CSV export and the ability to compare date ranges.

<Image align="center" alt="vNext Trends" border={true} caption="Trend Analysis" src="https://files.readme.io/c0c5526d697e0b45b74c968ff830f17802a2ace2153488965ca9603fece1cc99-vNext_Trends.png" />

For more information, refer to [Trends](doc:trends-v2).

## August

### File Variables in Product Experiences NextGen ![](https://files.readme.io/c30bf56-NewFeature.svg)

The all-new Product Experiences comes with another exciting feature: File Type Variables. It is available to all customers with the CleverTap SDK 7.0.0 and a paid PE add-on. With File Type Variables, customers can remotely control any file asset in their Application or Web page and run A/B Tests.

File Variables are linked to CleverTap CMS, which helps manage and re-use customer assets across the CleverTap platform. For more information, refer to [Product Experiences](doc:product-experiences-nextgen).

### WhatsApp Carousel Templates Support For Generic Providers ![](https://files.readme.io/7f99f23-Tags-1.svg)

CleverTap now supports WhatsApp Carousel templates for Generic providers. This feature empowers you to create rich, interactive messages that enhance customer engagement.

**What are Carousel Templates?**

Carousel templates allow businesses to send a single text message with up to 10 dynamic carousel cards. Recipients can scroll horizontally through engaging content, providing a seamless navigation experience through various cards featuring interactive media and information.

<Image align="center" alt="WhatsApp Carousel Templates" border={true} caption="WhatsApp Carousel Templates" src="https://files.readme.io/25ac047-WhatsApp_carousel_graphic_2x.png" width="80% " />

The new WhatsApp Carousel templates can be used across various domains, such as:

* **E-commerce** Showcase new products, create new looks, and share gifting ideas.
* **Fintech** Display investment options, share educational videos, provide portfolio reports, and compare financial products.
* **Food & Delivery**: Highlight popular dishes and promote special offers.
* **Gaming**: Announce upcoming events, share player stats, and display leaderboards.
* **Subscriptions**: Promote new shows, recommend content, and up-sell premium plans.

This feature is available to all customers using CleverTap BSP, and those utilizing Generic Integrations. For more information, refer to [Carousel](doc:whatsapp-message-templates#carousel-template).

### Gmail Deal Annotations for Improved Email Discoverability and Engagement ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce that CleverTap's Gmail Deal Annotations, which was earlier in Public Beta, is now generally available. This feature empowers email marketers to showcase promo codes and expiration dates directly in the Promotions tab Subject Area, offering recipients a compelling preview before opening their emails.

For more information, refer to [Gmail Promotional Annotations](doc:gmail-promotional-annotations).

### New Journey Paths in WhatsApp and SMS Journey Nodes ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are thrilled to announce that customers can now utilize _Viewed_ and _Clicked_ paths with WhatsApp node in Journeys. The enhancement also introduces a new _Delivered_ path for SMS node in Journeys.

This enhancement enables all CleverTap customers to create targeted follow-up engagements based on user interactions with SMS and WhatsApp notifications.

Use Cases:

* **E-commerce**: Send follow-up discounts to users who viewed a cart-related WhatsApp notification.
* **Fintech**: Target users with specific messages after they view a credit card offer on WhatsApp.
* **Gaming**: Incentivize users with credits if they don't register after clicking on an in-game event notification.
* **Subscriptions**: Emphasize the value of subscriptions to users who viewed renewal reminders.

### Scribe for CleverTap Emails: Quick, Emotionally Intelligent Content Creation ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We’re excited to introduce **Scribe** in **CleverTap Email**, now available for **Subject** and **Pre-header** fields, and for the **Headline** field of Gmail Product Carousel Annotation. With Scribe, creating subjects and pre-header texts will be quicker and more emotionally compelling, leading to better open rates and engagement.

Key Benefits:

* **Auto-Generate Content**: Quickly create compelling email subject lines, pre-headers, and headline texts using simple prompts.
* **Analyze Emotions**: Easily assess and adjust the emotional tone of your email content to align with your goals.
* **Optimize Campaigns**: Test multiple versions of auto-generated text to enhance engagement and improve open rates.

The feature is available to customers only on the **Cutting Edge Plan**. For more information, refer to:

* [Campaign creation](doc:scribe-email#create-an-email-campaign-using-scribe)
* [Sample Prompt Syntaxes](doc:scribe-sample-syntax-for-email-campaigns)

### Introducing DND for Webhook Channel ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are thrilled to announce a new enhancement to our Webhook Channel: the Do-Not-Disturb (DND) feature. This feature optimizes webhook integrations by sending alerts and making endpoint calls at the most effective times, maximizing their impact and relevance.

The key benefit of this feature is that you can now configure different DND hours for each day of the week according to the account timezone or the user's timezone. This ensures user engagement at convenient times, leading to more positive interactions and higher engagement rates.

The Webhook currently supports the Do Not Disturb (DND) feature only in Campaigns, not in Journeys. For more information, refer to [Delivery Preferences in Webhook](doc:create-message-webhook#delivery-preferences).

### Elevate User Experience with Linked Content URL Personalization ![](https://files.readme.io/7f99f23-Tags-1.svg)

The Linked Content URL Personalization Enhancement, previously in Private Beta, is now available to all customers. This feature allows you to personalize URLs within your campaigns, enhancing user experience with more relevant and engaging content. For more information, refer to [Linked Content](doc:linked-content#personalize-linked-content-url).

### Seamless Personalization with the All-New Visual Editor ![](https://files.readme.io/c30bf56-NewFeature.svg)

We are thrilled to announce the launch of our revolutionary Visual Editor, designed to transform native website elements directly from the CleverTap dashboard without requiring any development effort.

**Current Challenge and Solution**

Customers often rely on technical support to personalize website content. With CleverTap's Visual Editor, users can now create personalized web experiences easily through a simple interface.

Simply paste the Website URL into the editor, select elements to personalize, and publish changes in real time.

<Image align="center" alt="Visual Editor" border={true} caption="Visual Editor" src="https://files.readme.io/bac5f5a-point_and_click_template_1.jpg" width="80% " />

Key Benefits:

* **Seamless Personalization**: Instantly customize text, images, CTAs, or any HTML element from the CleverTap dashboard without coding to deliver personalized web experience.
* **Real-Time Personalization**: Dynamically align content with customer preferences and behaviors in real time.

For more information, refer to [Visual Editor](doc:web-native-display-editor#visual-editor).

### Custom Font Support For Enhanced Email Design ![](https://files.readme.io/c30bf56-NewFeature.svg)

The Custom Font Support feature, previously in Private Beta, is now available to all customers. This feature allows you to upload and use custom fonts in campaigns and user journeys.

The feature is available to customers on the Advanced and Cutting Edge plans. For more information, refer to [Font Manager](doc:setup-email#font-manager).

### Control Web Pop-up Display with Enhanced Campaign Priority ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce our enhanced web pop-ups, which allow customers to define granular-level priority on a scale from 1 to 100 for their campaigns. This offers complete control over the sequence in which your campaigns are displayed, leading to a more engaging customer experience. For more information, refer to [Web Pop-up Campaign Priority](doc:create-message-web-popup#campaign-priority).

### Enhanced In-App Message Delivery for Better Engagement ![](https://files.readme.io/7f99f23-Tags-1.svg)

We're thrilled to introduce a series of enhancements to our mobile In-App campaigns. These enhancements help boost engagement and provide enhanced control over user experience.

Previously available only in Private Beta, this feature is now accessible to all users.  
Key Enhancements:

* **Priority levels (1 to 10)** for In-App messages ensure structured control for campaigns. Ensures enhanced visibility.
* **Improved Frequency Caps Control** offers customers more flexibility over campaign frequency limits. This latest update provides independent control at both Global and Campaign levels.
* **Advanced Display Trigger Rules** allow triggering In-App campaigns on the Nth occurrence of an event for personalized communication. This is ideal for scenarios such as gaming milestones and ensuring messages at specific events.

<Image align="center" alt="In-App Message Delivery Preferences" border={true} caption="In-App Message Delivery Preferences" src="https://files.readme.io/2df482a-image.png" width="80% " />

For more details, refer to [Delivery Preferences (In-App)](doc:create-message-inapp#delivery-preferences).

### Enhanced Recurring User Profile Export for Streamlined Data Management ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Previously, exporting recurring profile data from the point of integration to a run date led to duplication and higher storage needs. The new method uses scheduled transfers to manage resources more effectively and streamlines the workflow. We start with a full data export on the first run, followed by incremental updates that transfer only new or changed data.

Currently, this feature is in Private Beta and will be available to everyone after the first week of September. This means that the profile exports will include only required incremental updates.

**Key Benefits**

* **Cost-Efficient Storage**: Ensures that customers store only what they need, significantly reducing storage costs.
* **Resource Optimization**: Facilitates better resource utilization, allowing customers to focus their efforts where they matter most, without the unnecessary data clutter.
* **Streamlined Operations**: Ensures a smoother workflow with exports aligning precisely with customers’ actual data requirements.

For more information, refer to the Export Details section of the following Data Warehouse Partners:

* [AWS S3](doc:data-export-to-aws-s3#export-details)
* [Google Cloud Platform](https://docs.clevertap.com/docs/data-export-to-gcp#export-format:~:text=Important%20Announcement%3A%20Recurring%20User%20Profile%20Export)
* [Microsoft Azure](doc:microsoft-azure#export-details)

## July

### Customize the CleverTap-Hosted Email Preference Center ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to announce enhancements to the CleverTap Hosted Email Preference Center!

**Key Features:**

* Complete Customization: Tailor your preference center with HTML, CSS, and JavaScript to match your branding.
* Easy Management: Manage everything directly from the CleverTap dashboard.
* Real-Time Preview: Preview your customizations side-by-side instantly.

<Image align="center" alt="CleverTap Hosted Email Preference Center" border={true} caption="CleverTap Hosted Email Preference Center" src="https://files.readme.io/e457f73-2024-07-31_11-13-50_1.gif" />

This feature is currently in Private Beta. For more details, refer to [Manage Custom Email Preference Center](https://docs.clevertap.com/docs/manage-custom-email-preference-center).

## July

### Multi-Button Templates and Limited Time Offer Templates Now Supported with Gupshup ![](https://files.readme.io/0c15d9f-Tags.svg)

CleverTap now supports Multi-Button CTAs and Limited Time Offer (LTO) WhatsApp templates for Gupshup. Customers using Gupshup as their WhatsApp provider can now leverage these templates in their campaigns, enjoying the same benefits previously available to CleverTap BSP and generic WhatsApp customers.

<Image align="center" alt="WhatsApp" border={false} caption="Multi Button / Limited Time Offer" src="https://files.readme.io/1fd2637-WhatsApp.webp" width="100% " />

This enhancement allows for more dynamic and engaging messaging, providing customers with versatile options to enhance their campaigns and drive better engagement. For template details and detailed use cases, refer to this [blog](https://clevertap.com/blog/lead-the-way-in-conversational-messaging-with-whatsapps-new-cutting-edge-templates/). For steps on how to use these templates in campaigns, refer to [WhatsApp Templates](doc:whatsapp-message-templates#whatsapp-template-types).

## June

### CleverTap-Hosted Email Preference Center for Enhanced User Experience ![](https://files.readme.io/c30bf56-NewFeature.svg)

CleverTap’s Email Preference Center feature, previously in Private Beta, is now available to all users.

**Key Benefits**:

* **Seamless No Code User Experience**: Enhanced user experience with our intuitive, ready-to-use Email Preference Center, hosted and managed within CleverTap. Say goodbye to navigating external platforms!
* **"Global Unsubscribe" Made Easy**: Effortless opt-out of all subscriptions with a single click on the landing page. You also have the option to return to the preference center to modify specific preferences.
* **Focused "Group Unsubscribe"**: Direct users to a dedicated page displaying only the subscription groups associated with the campaign upon clicking on the _Unsubscribe_ link. They can easily opt-out or unsubscribe from all groups if needed.
* **Effortless Integration**: Easily insert group unsubscribe/email preference center links in the drag-and-drop editor using the "Special Links" dropdown, and use replacement tags in the custom HTML editor.

For more information, refer to [Manage Email Preferences](doc:manage-email-preferences).

### Unveiling External Trigger: Elevate User Engagement with Personalized Non-Promotional Alerts ![](https://files.readme.io/7776b09-Beta.svg)

We are thrilled to introduce External Trigger in Public Beta for CleverTap customers. With this feature, our customers can send critical, timely, non-promotional alerts based on business events, all managed directly within the CleverTap dashboard. This eliminates the need for extensive development efforts.

**Key Benefits**:

* **Multi-Channel Alerts**: Send alerts through push notifications, webhooks, and emails.
* **External API Integration**: Trigger alerts via an external API call with minimal development effort.
* **Streamlined Campaign Management**: Create and manage campaign content directly from the CleverTap dashboard.
* **Dynamic Personalization**: Insert personalization parameters dynamically into messages.

<Image align="center" alt="External Trigger Campaigns" border={true} caption="External Trigger Campaigns" src="https://files.readme.io/cb5bbce-image-20240613-102654.png" />

For more information, refer to [External Trigger](doc:external-trigger).

### Optimize Campaign Delivery Across Channels ![](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing a significant enhancement to our campaign Throttling Limits. This enhancement ensures a smoother and more efficient message delivery process across all offline channels. The messages are now evenly distributed across the entire 5-minute interval. This change helps prevent traffic spikes and better manage delivery rates. ﻿This enhancement is particularly beneficial because of recent changes by FCM, which mandate rate limiting at a minute level.

For more information, refer to [Messaging Frequency Caps](doc:messaging-frequency-caps#throttle).

### Group-Level One-Click Unsubscribe Enhancement ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are pleased to announce an enhancement to our One-Click Unsubscribe feature for email campaigns. This improvement unsubscribes users from the specific subscription groups targeted in the campaign, rather than from all emails entirely. This allows users to stay engaged with only preferred email groups, improving their overall experience. Also, it adheres to best practices in customer-centric email marketing, preserving both user satisfaction and engagement.

For more information, refer to [One-Click Unsubscribe](doc:one-click-unsubscribe).

### Enhanced Node Performance Comparison for Journeys Stats ![](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce a significant enhancement to the Journey Stats tab. This enhancement features a new section that displays each node’s performance in a tabular structure. You can now view and compare the performance metrics of individual nodes side by side, providing a clear and comprehensive understanding of their effectiveness.

<Image align="center" alt="Engagement Stats" border={true} caption="Engagement Stats" src="https://files.readme.io/af6a4ed-Engagement_Stats-20240618-095619.gif" />

**Key Benefits**

* **Improved Insights**: Easily compare the performance of individual nodes to identify high-performing and underperforming areas.
* **Enhanced Decision-Making**: Make more informed, data-driven decisions to optimize each node within the journey.
* **Increased Efficiency**: Save time by accessing all relevant performance data in a single, easy-to-read table.

For more information, refer to [Engagement Stats](doc:engagement-stats).

### WhatsApp Carousel Templates Support For CleverTap BSP ![](https://files.readme.io/c30bf56-NewFeature.svg)

CleverTap now supports WhatsApp Carousel templates. This feature empowers you to create rich, interactive messages that enhance customer engagement.

**What are Carousel Templates?**  
Carousel templates allow businesses to send a single text message with up to 10 dynamic carousel cards. Recipients can scroll horizontally through engaging content, providing a seamless navigation experience through various cards featuring interactive media and information.

<Image align="center" alt="WhatsApp Carousel Templates" border={true} caption="WhatsApp Carousel Templates" src="https://files.readme.io/25ac047-WhatsApp_carousel_graphic_2x.png" width="80% " />

The new WhatsApp Carousel templates in CleverTap BSP can be used across various domains, such as:

* **E-commerce**: Showcase new products, create new looks, and share gifting ideas.
* **Fintech**: Display investment options, share educational videos, provide portfolio reports, and compare financial products.
* **Food & Delivery**: Highlight popular dishes and promote special offers.
* **Gaming**: Announce upcoming events, share player stats, and display leaderboards.
* **Subscriptions**: Promote new shows, recommend content, and up-sell premium plans.

This feature is available to all CleverTap BSP customers. For more information, refer to [Carousel.](doc:whatsapp-message-templates#carousel-template)

### Introducing Experimentation Support for NPS and User Rating Templates ![](https://files.readme.io/7f99f23-Tags-1.svg)

CleverTap now supports experimentation for NPS and User Rating templates across the following campaign types:

* A/B Testing
* Split Delivery
* Message on User Property

With this support, CleverTap customers can now:

* Conduct impactful experiments to determine the most effective versions of their NPS and User Rating templates.
* Optimize copy, visuals, CTA options, colors, and more through data-driven insights.

## May

### One-Click Unsubscribe for Enhanced Deliverability & User Experience ![](https://files.readme.io/c30bf56-NewFeature.svg)

We are pleased to announce that CleverTap's One-Click Unsubscribe feature for email is now generally available. This functionality is enabled by default to ensure compliance and ease of use. However, customers with a custom setup for one-click unsubscribe (list-unsubscribe headers) via their ESP can disable this feature from the CleverTap dashboard if they prefer to use their own setup.

For more information, refer to [One-Click Unsubscribe](doc:one-click-unsubscribe).

## April

### Custom Key-Value Pairs in App Inbox Now Available to All Users ![](https://files.readme.io/7f99f23-Tags-1.svg)

Custom Key-Value Pairs in CleverTap's App Inbox, previously available in Private Beta, are now available to all users. This empowers you to create highly personalized user experiences like never before. You must upgrade to CleverTap’s SDK version 5.2.0 or higher to access this enhancement.

**Key Highlights:**

* **Personalized Experiences**: Tailor app content with additional payload parameters, delivering targeted notifications to each user.
* **Seamless Integration**: Easily integrate personalized inbox campaigns into your CleverTap dashboard for streamlined campaign management.
* **Data Correlation**: Leverage key-value pairs to correlate attribution data between CleverTap and your internal systems, optimizing campaign performance.
* **Boosted Engagement**: Drive user engagement with exclusive discounts and personalized offers, guiding users to dedicated discount pages via notifications.

For more information, refer to:

* [App Inbox](doc:create-message-app-inbox#custom-key-value-pairs)
* [Push Notification + App Inbox](doc:create-message-push#custom-key-value-pair)
* [Create Campaign API - App Inbox](https://developer.clevertap.com/docs/create-campaign-api#body-parameters---target-user-events--properties)

### Hyper-personalized Experiences With Support For Personalization In Email Test Campaigns ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Excited to introduce support for personalization in test messages for the Email channel. You can now view personalized content on devices using test or internal profiles before launching campaigns. With this feature, you gain deeper insights into end-user experience, helping you debug potential errors. It provides seamless support for various personalization features such as @Personalization, Liquid Tags, and Linked Content.

For more information, refer to [Send Test Personalization](doc:send-test-personalization-for-email).

### Variant-specific Conversion and Revenue Analytics for Effective Experimentation ![](https://files.readme.io/7f99f23-Tags-1.svg)

With this enhancement, you can now accurately measure the performance of each variant by considering the conversion metrics and target group revenue.

CleverTap allows you to analyze variant-specific conversions and revenues in A/B and multivariate tests directly from the dashboard and reports for campaigns and journeys.

For more information, refer to [Conversion Performance](doc:push-campaign-stats#conversion-performance).

### One-Click Unsubscribe For Enhanced Deliverability and User Unsubscription Experience  ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

CleverTap now supports One-Click Unsubscribe for emails to ensure compliance with [Gmail and Yahoo's latest email policies](https://clevertap.com/blog/acing-email-deliverability-in-2024-guide-to-yahoo-and-gmails-latest-email-security-updates/). This makes it easier for recipients to unsubscribe with just a single click. It also ensures transparency, respecting user preferences, and adhering to email marketing practices. As a result, this improves user trust, engagement, and overall sending efficiency.

The following images show how you can unsubscribe with just a single click from inbox or email body:

<Image align="center" alt="One-Click Unsubscribe from Inbox" border={true} caption="One-Click Unsubscribe from Inbox" src="https://files.readme.io/f012ff2-image-20240412-053706.png" />

<Image align="center" alt="One-Click Unsubscribe from Email Body" border={true} caption="One-Click Unsubscribe from Email Body" src="https://files.readme.io/0fa115b-image-20240412-053756.png" />

This functionality is now available in Private Beta for a few customers using Sendgrid as their ESP. It will be available for other providers soon.

For more information, refer to[ One-Click Unsubscribe](https://docs.clevertap.com/docs/one-click-unsubscribe).

### Hyper-personalized Experiences With Support For Personalization In Test Messages![](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing support for personalizing test messages! You can now view personalized content on devices using test or internal profiles before launching campaigns. With this feature, you also receive response details that help you gain deeper insights and debug potential errors. It provides seamless support for various personalization features such as @Personalization, Liquid Tags, Linked Content, and Constant Event Property.

<Image align="center" alt="Send Personalized Campaigns to Test Profiles" border={true} caption="Send Personalized Campaigns to Test Profiles" src="https://files.readme.io/68feacf-send-test-personalization-push-20240412-045513.gif" />

Currently available on the Push Notification channel in Campaigns & Journeys and will be made available on other channels soon. For more information, refer to  [Send Test Personalization](https://docs.clevertap.com/docs/send-test-personalization-for-push).

### Introducing the New Image Interstitial Editor for In-App Messages ![](https://files.readme.io/c30bf56-NewFeature.svg)

We're excited to announce the release of our Image Interstitial Editor, which is now available for advanced and cutting-edge plans!

Earlier, crafting custom In-App messages was a multi-step process involving design and HTML coding.

Using CleverTap's Image interstitial editor, customers can effortlessly create customizable In-App messages directly from images and clickable CTAs without any development effort. This streamlines engagement for game announcements, feedback requests, promotional offers, and more.

<Image align="center" alt="Image Interstitial Template" border={true} caption="Image Interstitial Template" src="https://files.readme.io/f5ccae3-animation-updated_1_1.gif" />

Key Highlights:

* **Enhanced Operational Efficiency**: Craft custom In-App messages effortlessly without developer intervention or coding expertise.
* **Multiple CTAs**: Create highly interactive experiences by adding up to 10 clickable regions on images, with unique actions for each.
* **Optimized Visual Consistency**: Ensure consistent image display across devices with dynamic scaling while maintaining in-app aspect ratio.
* **Seamless Integration**: Easily integrate with your existing setup. No SDK upgrades are required.

For more information, refer to [Image Interstitial Template](https://docs.clevertap.com/docs/in-app-editor#image-interstitial).

### Multi-button CTA and Limited Time Offer Templates for Urgency and User Interactivity ![](https://files.readme.io/c30bf56-NewFeature.svg)

CleverTap now supports Multi-Button CTA and Limited Time Offer (LTO) WhatsApp templates, empowering users to create dynamic, interactive, and time-sensitive messages.

Multi-Button CTA templates supports adding up to 10 CTAs (1 Copy Code, 2 redirection CTA, 1 Call Phone, and 5 Quick Reply Buttons) allowing various engagement options in a single notification. LTO templates display expiration dates and countdown timers, creating urgency, driving action, and boosting conversions.

<Image align="center" alt="Multi Button CTAs and Limited Time Offer Templates" border={true} caption="Multi Button CTAs and Limited Time Offer Templates" src="https://files.readme.io/8a92907-LTO_sample.png" width="70% " />

This feature is available to all CleverTap BSP and Generic WhatsApp provider customers. For more information, refer to [Sample payloads for Multi-button CTAs and Limited Time Offer](https://docs.clevertap.com/docs/generic-whatsapp#payload-samples-for-template-message).

## March

### Gmail Carousel Annotations for Improved Email Discoverability and Engagement ![](https://files.readme.io/c30bf56-NewFeature.svg)

In addition to Deal annotations released earlier, CleverTap has added a new feature called Product Carousel Annotations to their Gmail Promotional Annotations. With this feature, you can display up to **10 images** in a carousel format to make your promotions more attractive.

Currently, this feature is released in Private Beta. For more information, refer to [Gmail Promotional Annotations](https://docs.clevertap.com/docs/gmail-promotional-annotations-product-carousel#annotate-with-product-carousel).

### Enhanced Quick Reply Autoresponder For Streamlined Automated Conversations ![](https://files.readme.io/7f99f23-Tags-1.svg)

We're excited to introduce significant improvements to our WhatsApp Quick Reply Autoresponders, offering customers more flexibility and control over automated conversations. We now have more configurations and precise time controls that cater to customer needs:

**Between Time Periods**: Setting up time-controlled replies is now simpler; customers can simply define a date range, triggering quick replies within that range.

**During Specific Hours**: Enhanced granular control allows setting different time ranges for each day, including spanning across days for non-working hours.

These updates are available to all CleverTap WhatsApp customers. For more information, refer to [Setting up Quick Replies](https://docs.clevertap.com/docs/conversations#set-up-a-quick-reply).

## February

### Discontinuation of Xiaomi Push Service ![](https://files.readme.io/0c15d9f-Tags.svg)

Xiaomi Corporation made a significant announcement recently, notifying users about discontinuing the Xiaomi Push service beyond Mainland China due to operational concerns. This change will impact the App Push Notifications sent to Xiaomi devices via Xiaomi Push Service (XPS). Starting March 31, 2024, App Push on Xiaomi devices will be directed through the FCM service instead.

Action Required:

* Upgrade your app to CleverTap Android SDK v6.1.0 or above and promptly discontinue the use of the XPS SDK. The CleverTap Android SDK is expected to be released on February 20, 2024.
* Utilize our proprietary technology, [RenderMax™](https://docs.clevertap.com/docs/rendermax), to enhance your push notification campaigns on Xiaomi devices.

For more information, refer to [Discontinuation of Xiaomi Push Service](https://developer.clevertap.com/docs/discontinuation-of-xiaomi-push-service).

### Introducing Product Experiences NextGen ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

Product Experiences NextGen elevates our offering with a sleeker UI, enhanced user controls, and improved functionality. Here are its two new powerful capabilities:

* **Remote Config**: This feature eliminates the need for multiple updates on the app stores. It enables you to customize, manage, and configure your applications remotely with minimal development effort. You can swiftly adjust app design, user experience, and workflow for all users or specific user segments.

<Image align="center" alt="Product Experiences NextGen" border={true} caption="Product Experiences NextGen" src="https://files.readme.io/f4f17b8-Product-Experiences-P-B_1.gif" width="85% " />

* **Product A/B tests**: This feature allows you to experiment with different versions of your app's UI or functionality. After a detailed analysis of your A/B Tests, you can seamlessly deploy the most successful version based on the key performance indicators (KPIs).

For more details,  refer to the [Product Experiences](https://docs.clevertap.com/docs/product-experiences-nextgen).

## January

### Enhanced In-App Message Delivery for Better Engagement ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We're thrilled to introduce a series of enhancements to our mobile In-App campaigns. These enhancements help boost engagement and provide enhanced control over user experience.

Key Enhancements:

* **Assign Priority Settings**:  This feature allows you to control the visibility of your In-App campaigns by defining priority levels (1 to 10) for In-App messages. Priority provides structured control for diverse In-App campaigns, ensuring enhanced visibility.
* **Improved Frequency Caps Controls**: This enhancement offers customers greater flexibility over campaign frequency limits, allowing for more granular control. This latest update provides independent control at both Global and Campaign levels.
* **Advanced Display Trigger Rules**: Effortlessly trigger In-App campaigns on the Nth occurrence of an event, unlocking personalized communication. Ideal for scenarios such as gaming milestones, and ensuring messages at specific events.

<Image align="center" alt="In-App Delivery Preferences" border={true} caption="In-App Delivery Preferences" src="https://files.readme.io/6d21640-campaign_frequency_limits.png" width="80% " />

These features are currently in Private Beta, exclusively available to a select group of customers. For more details, refer to [Delivery preferences (In-App)](https://docs.clevertap.com/docs/create-message-inapp#delivery-preferences).

### Identity Personalization for Creating More Contextual User Experiences ![](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing Identity Personalization, a capability that enables CleverTap customers to **seamlessly leverage user identity values**—such as email ID, phone number, and user ID and **contextualize their campaigns**. You can easily use identity, email, and phone fields from within the @ Personalization and Liquid Tags for **flexible campaign creation**.

You can leverage this feature **across all messaging channels, spanning both Campaigns and Journeys**, ensuring a **consistent user experience**. This helps significantly broaden the scope of personalization on CleverTap, empowering users to create more targeted and engaging experiences for their customers.

For more information, refer to [ Identity Personalization](https://docs.clevertap.com/docs/personalize-message-all#identity-personalization).

### Elevate User Experience with Linked Content URL Personalization ![](https://files.readme.io/7f99f23-Tags-1.svg)

CleverTap's Linked Content URL Personalization feature empowers marketers to **personalize the endpoint URL** within Linked Content, allowing customers **to tailor message content** from third-party data sources for individual users based on their user attributes. You can **easily personalize the endpoint URL** using User Profile, Event Property, and Message Property **during Linked Content setup**. Also, it helps ensure a consistent and personalized user experience by **seamlessly integrating** Linked Content Personalization across all engagement channels, including Campaigns and Journeys.

For more information, refer to [Linked Content](https://docs.clevertap.com/docs/linked-content-url-personalization).

<HTMLBlock>{`
<style>
  nav#hub-sidebar { display: none; }

  .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  .markdown-body img{
    margin-left: 0;
  }
  /* .rm-Guides a.suggestEdits {
    display: none;
  } */
  @media (min-width: 769px) {
    .rm-Guides .rm-Article {
        max-width: 100%;
    }
  }
  .markdown-body summary {
    font-size: 20px;
    font-weight: bold; 
    text-transform: camelcase;
  }
  .toc-children img {
    display: none;
  } 
  #content {
    padding-left: 80px;
  }
  .heading-3  {
    margin-top: 50px !important;
  }
  .heading-2  {
    margin-top: 35px !important;
  }
  .heading-3 .heading-text {
    color: #384248;
  }
  details {
    margin-top: 35px !important;
  }
  .field-description h3, .markdown-body h3{
    font-size: 1.35em;
  }
  .markdown-body summary {
    font-size: 17px;
  }
  .heading-2 + .heading-3  {
    margin-top: 20px !important;
  }
  details .heading-4  {
    margin-top: 30px !important;
  }
  details .heading-3  {
    margin-top: 50px !important;
  }
  details h3{
    font-size: 1.5em !important;
  }
  details  h4{
    font-size: 1.35em !important;
  }
  #content-head h1 {
    font-weight: 500 !important;
    font-size: 35px !important;
  }
</style>
`}</HTMLBlock>
