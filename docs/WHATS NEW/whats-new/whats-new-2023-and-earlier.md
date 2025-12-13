---
title: Release Notes 2023 and Earlier
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# 2023

## December

### Debugger ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to introduce the Debugger feature, designed to streamline and enhance your integration experience with CleverTap. This will significantly reduce the time-to-live for our valued customers while providing an enriched integration, auditing, and debugging experience.

Here are the key features: 

* **Single Data Stream View**: Gain a unified, comprehensive view of event and user property data from your App or Website. 
* **JSON Data View**: Effortlessly inspect incoming data with a detailed JSON view for a deeper understanding.
* **Enhanced Capabilities**: Upgrade your experience with the ability to view up to 1000 events within a seven-day timeframe. Additionally, experience Profile View for instant identity access and Reachability View to identify when a profile is reachable for various notifications.

For more information, refer to the [Debugger](https://docs.clevertap.com/docs/debugger) document.

### Support For Custom Key-Value Pair in App Inbox Campaigns For Enhanced Personalization ![](https://files.readme.io/bbc3552-PrivateBeta.svg)

CleverTap's App Inbox now supports Custom Key-Value Pairs, enabling users to include additional payload with notifications. This enhancement personalizes user experiences by allowing customers to send specific campaigns, tailoring the app content accordingly. For example, you can send additional campaign parameters like "CouponCode" with a value such as "50%OFF," signaling the app to display only those products where the promo coupon is applicable.

<Image alt="Custom Key-Value Pair" align="center" width="85%" border={true} src="https://files.readme.io/9eefefc-Custom_Key_Value_Pair.png" /> Custom Key-Value Pair

With support for custom key-value pairs in App Inbox, customers can now seamlessly extend this capability to their App Inbox and Push + App Inbox campaigns, adding a new layer of personalization to their engagement strategies. You can also extend this feature for journeys that include App Inbox and Push + App Inbox campaigns. This helps ensure a consistent user experience without losing context from the notification by enabling the app to cater more closely to the individual user’s preferences. 

Upgrading to SDK 5.2.0 or higher unlocks this flexibility, empowering the effortless execution of personalized app workflows. For more information, refer to the documentation.
### WhatsApp Template Creation and Approval Management ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing Native WhatsApp Template Creation and Approval Management in CleverTap's BSP dashboard! You can now create and manage WhatsApp Message Templates completely within CleverTap without duplicating efforts on the Meta dashboard. 

This new feature provides the following benefits:

* **Operational Efficiency**: Templates sync between CleverTap and Meta dashboards automatically.
* **Effortless Approval**: Submit templates, get a quick 24-hour review, and receive real-time notifications.
* **Centralized Operations**: Edit or delete templates easily from the CleverTap dashboard.

Note: This feature is exclusive to CleverTap BSP customers. For more details, refer to the [Creating WhatsApp Message Templates](https://docs.clevertap.com/docs/clevertap-bsp#creating-whatsapp-message-templates) document.

### Signed Call™ Now Available to All CleverTap Customers! ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We're thrilled to announce the general availability of Signed Call™. This groundbreaking, VoIP-enabled, in-app voice feature establishes trust and context during customer engagement. It allows seamless communication without leaving the app.

<Image align="center" className="border" border={true} src="https://files.readme.io/70b2de2-SignedCall.png" />

Unknown number voice calls can be risky, leading to spam labeling, potential scams, and damage to brand credibility and user relationships. Signed Call™ addresses these challenges by offering the following benefits:

* **Improved Trust**: Ensure higher privacy with secure and compliant in-app voice calls, preventing spam without sharing phone numbers.
* **Enhanced Conversions**: Brand your voice as a trusted communication channel to deliver contextual engagement and boost customer engagement.
* **Higher ROI**: Achieve top-notch call success, voice quality, low latency at no extra cost, saving on existing Public Switched Telephone Network (PSTN) calls.
* **Quick Time to Value**: Leverage our no-code solution with a lightweight voice SDK and pre-built use cases for easy implementation.

Experience the benefits of Signed Call™ available for CleverTap customers! For more details, refer to the [Signed Call](https://docs.clevertap.com/docs/signed-call) document. 

### Unveiling Powerful Upgrades to Our Exports Feature! ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)


We are pleased to announce significant enhancements to our Exports feature. It provides our valued customers with a more streamlined experience.

Here are key highlights of the latest enhancements:

* **Enhanced Listing and Searching of Exports**: Search export data by ID regardless of date range. Additionally, the listing feature covers a full year, extending from 30 days. It provides a more comprehensive view.
* **Editable Exports**: Customers can now edit the export criteria, such as formats, events, frequency, and buckets, without creating a new one. It saves both development effort and time. For more information, refer to the [Edit Exports](https://docs.clevertap.com/docs/data-export-to-aws-s3#edit-an-export) documentation. 
* **Detailed Export Overview**: You can now access a comprehensive view of the export information, such as frequency, events, buckets, and more, with just a single click. This streamlined process allows for easier adjustments and modifications, enhancing the overall experience.
* **Status Alerts for Exports**: You can now receive real-time notifications when exports are initiated or completed. It ensures smooth processes with specific URL notifications through webhooks. For more information, refer to the [Status Alerts for Exports](https://docs.clevertap.com/docs/status-alerts-for-exports) documentation.
* **Communication Preferences[Reachability Count for Push notifications]**: Communication preferences were previously determined at the device level, resulting in a discrepancy in the number of reachable users on the CleverTap dashboard and in exports. This update sets communication preferences at the user level. It ensures consistency between reachable users on any device and the CleverTap dashboard. 
* **Flexible Identity Selection for Exports to S3, GCP, and Azure**: You can now use various identifiers, such as identity, phone number, and email when exporting data to S3, GCP, and Azure. It provides greater control and customization. For more information, refer to the [Prioritize User Identity for Exports](https://docs.clevertap.com/docs/data-export-to-aws-s3#prioritize-user-identity-for-exports) documentation. 
* **Improved Internal Monitoring Systems**: We have enhanced our internal monitoring systems to swiftly and proactively identify and address any delay in exports, ensuring a timely action that results in a seamless experience for our customers.

This feature is available to all CleverTap customers with export features.


### Unveiling CSV Upload Enhancements for a Seamless Customer Experience  ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are pleased to announce significant enhancements to our CSV Upload feature, which is designed to offer a more intuitive and user-friendly experience.

<Image alt="CSV Upload" align="center" border={true} src="https://files.readme.io/7cb3657-CSVUpload.png" />  CSV Upload











Here are the key benefits of these latest enhancements:

* **1 GB File Size Limit**: The limit for CSV uploads has been boosted from 50 MB to 1 GB. It enables customers to effortlessly manage large datasets without compromising the upload speed.
* **Comprehensive Error Reports**: Customers will receive email notifications detailing error counts and specific reasons. The reports provide clear explanations for each issue.
* **Customizable User Property Data Types**: You can now categorize and specify user property data types according to your requirements. This allows you to store user property data in different formats, such as binary, date, and numeric. It offers more versatility than the previous restriction to alphanumeric formats.
* **Tailored Column Names**: Our enhanced CSV upload empowers customers to customize user property column names to align with their preferences. This offers greater flexibility and customization for file uploads.
* **AI-Powered Auto Suggestions**: CleverTap leverages built-in AI to offer intelligent auto suggestions for customer data types. This empowers customers to streamline their upload process with smart recommendations, making it faster and seamless.

 This feature is available to all CleverTap customers. For more information, refer to the [CSV Upload](https://docs.clevertap.com/docs/csv-upload) document.

### Device-Level Do Not Disturb (DND) Enhancements For Push Notifications on Android Devices  ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)
Introducing enhanced device-level Do Not Disturb (DND) support for push notifications on Android devices. Starting with Android 13, you must have user permission to send notifications. CleverTap now tracks opt-ins for Android version 13 and higher, allowing targeted messaging. With this update,  you can now track unsubscribed users, ensuring accurate impression rates and improved campaign analysis. To access this feature, ensure you upgrade to SDK version 50100 or higher. For more information, refer to the [Android Push](https://developer.clevertap.com/docs/android-push#push-notification-permission) document.

## November

### Elevate Your CleverTap Experience with Ask ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

CleverTap **Ask** harnesses the extensive knowledge embedded in CleverTap's documentation and blogs and gives swift, precise answers with just a click.

**What is Ask?**

* **Answers Instantly**: Sifting and searching through multiple pages of documents is going to be a distant past. Just click, submit your question, and get your answer!
* **Leverages a Rich Knowledge Repository**: Benefit from our comprehensive knowledge repository of documents and blogs, ensuring you have reliable information at your fingertips.
* **Learns Continuously**: **Ask** is not just a tool; it is a learning partner. Evolving continually, it adapts to your needs and enhances its responses based on your feedback.

**Where is Ask?**

Small, yet powerful! You will find it in the top-right corner of the CleverTap Dashboard.

**How Does Ask Work?**

* Click **Ask** and type your question.
* **Ask** gets you the answer from CleverTap Documents and Blogs.
* Help **Ask** to learn by providing feedback. 

Your journey with CleverTap just got smarter. Try **Ask** now and be a part of its evolution.

<Image align="center" className="border" border={true} src="https://files.readme.io/f8c930e-Ask_Release_Notes.gif" />

### Enhanced Subscription Management for the WhatsApp Channel   ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We have now introduced the WhatsApp DND Flag so that customers can unsubscribe phone numbers. This ensures all profiles associated with a single phone number are unsubscribed, preventing unintended messages to users sharing a phone number.

**Why is this important?**


* **Compliance**: It helps customers comply with user preferences and regulations, respecting communication choices.
* **Enhanced End-User Experience**: Effective subscription management provides a non-intrusive messaging experience for users.
* **Efficiency**: Preventing unintended messages saves costs and boosts the efficiency of messaging campaigns.
* **Improve Number Quality**: Ensures that only engaged users receive messages, reducing the risk of being blocked or reported, thus improving WhatsApp number quality.

**How does it work?**

The WhatsApp DND Flag is user-friendly, seamlessly integrating into the customer's workflow. They can set WhatsApp phone numbers as subscribed or unsubscribed directly through the Subscribe API, CSV Upload, User profile upload API, or using the SDK.

This feature is available to all CleverTap WhatsApp customers. For more information, refer to the [WhatsApp Subscription Management](https://docs.clevertap.com/docs/whatsapp-subscription-management) documentation.

### Funnels Customization in Boards  ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing the option to customize Funnels in Boards. This enhancement allows you to rename each Funnel Step and Legend on your Board to match your business needs and context. You can rename these labels without affecting the original event names. These new label names are visible to all user roles.

<Image align="center" className="border" border={true} src="https://files.readme.io/5c8eac3-Customize_a_Funnel_Card.gif" />

This enhancement has the following key benefits:

* **Ease of Use**: Streamline reporting with user-friendly labels such as Promo Expired instead of technical terms.
* **Clarity in Reporting**: Provide clarity and avoid confusion by changing a generic event name to something more contextual. For example, rename the Charged step to AirPods Purchase. 

For more information, refer to [Customize Cards](https://docs.clevertap.com/docs/custom-dashboards#customize-a-card).

### Visually Appealing Web Pop-Ups With the New Drag-And-Drop Editor  ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Create visually appealing and impactful web pop-ups effortlessly with the new drag-and-drop editor. Boost website conversions and engage with your audience through personalized pop-up campaigns. From abandoned cart recovery to product recommendations and announcements, the editor can help you with the following:


* Tailor, save, and reuse templates
* Ensure responsiveness across all devices
* Customize the CSS and HTML components to align with your brand guidelines. 

For more information, refer to the [Web Pop-up Editor](https://docs.clevertap.com/docs/web-pop-up-editor) documentation.

## October

### Enhance Campaign Analytics and Optimization with Campaign ID Personalization ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

> 📘 Note
>
> This feature is released in Private Beta. Contact your customer success manager to request early access to this feature.

Introducing Campaign ID Personalization for deeper insights into user engagement across campaigns. Customers can now personalize links using campaign IDs, helping them create unique URLs and seamlessly attribute clicks to specific campaigns. This enables you to seamlessly utilize external tools or solutions to analyze engagement across campaigns and meet any custom analytical requirements. You can also leverage campaign IDs as payloads for custom key-value pairs to automate workflows.

For Journeys, a similar approach can be applied to personalize Node IDs. For more information, refer to the [Campaign ID Personalization](https://docs.clevertap.com/docs/campaign-id-personalization) document.

### Explore Our Enhanced Audit Logs Feature! ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing a brand-new Audit Logs User Interface (UI) that takes your log management experience to the next level. Here's what you can expect from this update:

* **Enhanced Discoverability**: The new user interface now prominently displays unique identifiers within the table view. This lets you easily find and track your logs to discover the required information.
* **Select and Download Audit Logs**:  This feature gives you greater control over your data. It allows you to explore your logs with ease and precision. You can conveniently select and download your Audit Logs in a CSV file for in-depth analysis. 

For more information on downloading audit logs, refer to these [FAQs](https://docs.clevertap.com/docs/faq#can-i-download-my-audit-logs).

### Elevating Journey Personalization with Profile Update Node Enhancement ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)


Introducing enhancements to the Profile Update Node in Journeys. It allows you to use conditional statements with Liquid Tags to update user properties based on events triggered in preceding segments or engagement nodes. Using this capability, you can make Journeys more personalized and dynamic based on real-time user actions.

The possibilities are endless, but here are a few exciting use cases to illustrate the potential:

* **Dynamic Cart Discounts**: Update different offers based on the user’s abandoned cart value or product type. For instance, a customer’s cart includes the *Summer Collection* items. Using conditional logic, you can update their user property *Promotion Eligibility* with a 10% discount. 
* **Personalized Content Recommendations**: Update a user’s preferred or favorite movie based on the ratings the user provided for a movie using conditional logic. For example, update the user’s favorite movie only if the user rating for the movie is four or above, or else ignore it.
* **Loyalty Tier and Offers**: Update loyalty tiers and provide personalized offers based on purchase trends. For example, upgrade users to *Gold Tier* after three purchases in 6 months. 

This enhancement is now available to all CleverTap customers. For more information, refer to the [documentation](https://docs.clevertap.com/docs/construct-a-journey#using-user-profile-update-node) here.

### Configurable Inactivity Window ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

The CleverTap dashboard now allows you to configure the session inactivity timer per your preferences and security requirements. 

Previously, the fixed 30-minute session limit caused users to log in multiple times daily, leading to a less-than-optimal experience.

**Enhancements Benefits:**

* **Tailored Security Settings:** You can now set your session timer anywhere from a quick 30 minutes to a more relaxed 4 hours, catering to your preferences and security needs.
* **Flexible Control:** You can easily configure the session timer from your Organization page, enabling you to strike the perfect balance between convenience and security.

> 📘 Note
>
> The default session timeout remains 30 minutes, and only Admins can configure this feature.

For more information about this feature, refer to the [documentation](doc:faq#q-how-to-configure-the-session-invalidation-timer-for-your-dashboard).

## September


### Enhanced Data Analysis with Microsoft Azure  ![BETA](https://files.readme.io/7776b09-Beta.svg)

This integration is currently in Public Beta and is available for all CleverTap customers with export features.

The CleverTap and Microsoft Azure Blob storage integration allows you to export user and event data for deeper analysis in a secure manner. It is a valuable addition to CleverTap's integration lineup, which already includes AWS S3 and Google Cloud Platform. Microsoft Azure is leveraged by 20% of businesses globally, including some of our customers, for whom this integration will add significant value.

<Image alt="CleverTap and Microsoft Azure Integration" align="center" width="100% " border={true} src="https://files.readme.io/1e3b4b0-image_8.png" />  CleverTap and Microsoft Azure Integration











Here are the key benefits of this integration:

* **Quick Time-to-Value**: Ensures quick time-to-value for our customers as the integration is done in a few steps.
* **Seamless Data Export**: Enables streamlined export of user data and event information to Azure Blob Storage, thereby unlocking endless possibilities for data storage, management, and analysis.
* **Enhanced Data Security**: Adheres to the highest industry standards by using SAS tokens for secure data connection and transfer.
* **Increased Efficiency**: Automates data export workflows with CleverTap effortlessly, optimizing effort and cost. This allows scheduling or triggering exports based on specific events or conditions.

For more information, refer to the [Microsoft Azure](https://docs.clevertap.com/docs/microsoft-azure) documentation. Please contact your Customer Success Manager or CleverTap Support team for further queries.

### Elevate Engagement with Support for iOS 15+ Updates ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing the two powerful enhancements to support iOS 15+ updates. The following enhancements are designed to improve the user experience significantly.

* **Interruption Levels for Focus Mode:** With iOS 15+, Apple introduces Interruption Levels for Focus Mode. It gives you greater control over notification priorities and delivery timing. CleverTap enables you to classify push notifications into three categories from the Dashboard: Active, Passive, and Time-sensitive. This ensures important alerts are never lost among many notifications.
<Image alt="Time Sensitive Notifications" align="center" border={true} src="https://files.readme.io/7a31b2e-Time_Sensitive_Notifications.png" />  Time Sensitive Notifications











* **Relevance Scores for Notification Summary:** CleverTap empowers you to set Relevance Scores for the Notification Summary feature introduced in iOS 15+. These scores, ranging from 0 to 1, allow you to efficiently organize and display notifications within users' preferred time frames. The notifications are sorted based on their relevance scores. This ensures vital messages appear first during the user's chosen time slot. Assign higher relevance scores to critical notifications like time-bound sales alerts, ensuring they receive top priority.

<Image alt="Mapping of Relevance Score into Summary " align="center" border={true} src="https://files.readme.io/92f71f3-Mapping_of_Relevance_Score_into_Summary.png" />  Mapping of Relevance Score into Summary 











These features are available to all CleverTap customers. To learn more, refer to the [documentation](doc:create-message-push#advanced-ios-settings).

### Enhanced Integration with Amplitude Event Streaming ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We enhanced our integration with Amplitude, a leading player in product analytics. This enhancement empowers CleverTap customers with the following: 

* **Seamless Integration:** Allows you to integrate with a few steps seamlessly. Once the integration is complete, Amplitude events and their properties flow to CleverTap in real-time.
* **Real-time Insights:** Allows you to access real-time insights into user behavior. For example, track the pages users visit.
* **Personalized Experiences:** Allows you to craft personalized user experiences. For example, you can send information about a user's location or language preference. You can use this data to tailor your messages or content to specific needs.
* **Track Conversion:** Allows you to measure campaign performance and track user behavior throughout the funnel. For example, you can track the number of users who completed a transaction after receiving a CleverTap campaign.

For more information, refer to the [Amplitude Event Streaming](doc:amplitude-event-streaming) document.

### AMP for Email Enhancements ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

Introducing the following enhancements to our Accelerated Mobile Pages (AMP) for Email feature, now in Private Beta:
* **Easy-to-Use Templates:** Create AMP emails effortlessly with customizable templates for various use cases such as User Feedback, NPS Survey, Accordion, Carousel, and Tabs.
* **Code Validation and Preview:** Code using a built-in validator and side-by-side previews for error-free AMP emails.
* **AMP Experience for Non-AMP Supported Email Clients:** Extend AMP email access to non-supported email clients (for example, Apple Mail, Outlook) through View In Browser AMP tags.

For more information about this feature, refer to the [documentation](doc:ampforemail).

If you are on the Email Booster Max Add-on or the Advanced Email Add-on plans and want to enable this feature, contact your Customer Success Manager.

### Authentication through Auth0 and New Login Experience [All Regions] ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are thrilled to unveil an upgraded login experience for your CleverTap dashboard, with a strong focus on enhancing security and efficiency. It provides a smoother login process, Single Sign-On (SSO) streamlining, and integration with a new Identity and Access Management system. Here's a quick overview:


* **New Login Experience for All Users (SSO + Non-SSO Users)**: We have upgraded the login process to cater seamlessly to Single Sign-On (SSO) and Non-SSO users.
* **Universal Login URL for All Regions**: The new unified login page is accessible through all CleverTap login URLs. Our system guides you to the appropriate region where your account is hosted. It ensures a consistent login experience for all users.
* **Seamless Navigation Between Multiple Regions**: Our newly introduced Region Switcher allows you to seamlessly transition between regions without requiring separate logins. If you have access to multiple regions, this feature simplifies navigation, saving you valuable time.
* **Simplified SSO Configuration**: We have streamlined the configuration process for users utilizing Single Sign-On (SSO). This enhancement eliminates the need for Account-Role Mapping on your Identity Provider (IDP). It makes SSO authentication easier to manage.
* **Email Domain Whitelisting for SSO Users**:  We have also introduced email domain whitelisting for SSO users. It ensures that only authorized email domains can access your CleverTap dashboard. It also improves security and streamlines your team’s login experience.
* **2FA: Remember this Device for 30 Days**: This feature allows for a seamless login process throughout the entire 30-day period. It also eliminates the need to repeatedly enter the authentication code. This lets you enjoy quicker access to your account, leading to increased efficiency. 

To learn more about this feature, refer to the [documentation](https://docs.clevertap.com/docs/single-sign-on-sso). 

For more queries, feel free to raise a support ticket from the CleverTap Dashboard or contact your Customer Success Manager.

## August

### WhatsApp Click Tracking ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

WhatsApp Click Tracking enables you to analyze campaign performance more deeply. This feature is only available to CleverTap BSP users. With this capability, you can effortlessly attribute conversions, access comprehensive analytics, and conduct precise ROI analysis. This capability is currently in private beta, and you can contact our support team to enable this feature. For more inforamtion, refer to [Click Tracking](doc:whatsapp-stats#clicked) in our documentation.

### Increased Flexibility in CleverTap’s Campaign Approval Workflow ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)


Introducing enhancements to our campaign approval workflow, providing greater flexibility to the approval process. Currently, when a creator schedules a campaign for a specific time, and the approver fails to grant approval before the scheduled time, the campaign is sent out immediately upon approval, even if the approver had rescheduled the campaign for a future date/time. With the improved workflow, if a creator schedules a campaign for a specific time and the approver fails to grant approval before the scheduled time, the campaign expires. If the approver still wants to proceed with the campaign, the approver must clone the campaign and schedule it at their convenience for a future date/time.

For example, Amy, a marketing manager, plans a flash sale campaign for the weekend. The campaign is scheduled to be sent on Saturday morning. Her manager submits the campaign for approval by Friday evening. If John, the campaign approver, does not approve the campaign by Saturday morning, the campaign expires and does not get sent. If the marketing manager still wants to run the campaign, they must clone the expired campaign, make any necessary edits, and schedule the campaign for a later time.

This feature is available to all CleverTap customers. For more information, refer to [Campaign Approval Workflow](doc:campaign-approval-workflow).

### Message via Identity API for WhatsApp ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

The Message via Identity API for WhatsApp now empowers CleverTap BSP users to seamlessly link our WhatsApp solution with external tools and customer backend services. It enables you to expand beyond promotional use cases. Direct targeting based on user identity eliminates the need for event-based triggers, enhancing flexibility. This upgrade enables:

* **Essential Updates:** Notifications for order progress, payments, appointments, returns, and so on.
* **Cross-User Interaction:** Notifications for referrals, likes, views, and so on.
* **Custom Segmentation:** Utilize in-house segments for WhatsApp campaigns.
* **External Chat Integration:** Use CleverTap BSP for message delivery and backend-triggered replies.
* **Workflow Streamlining:** Integrate with Zapier, Zoho, etc., for automated processes.


This enhancement is available to all CleverTap BSP WhatsApp Add-on users. For more details, refer to the [target users by identities](https://developer.clevertap.com/docs/create-campaign-api#create-campaign-api---target-users-by-their-identities) documentation.

### Instant WhatsApp Template Import ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing the Instant WhatsApp Template Import feature that streamlines template creation and management on CleverTap. Previously, recreating Meta dashboard templates on CleverTap was manual, time-consuming, and prone to human error. This new functionality expedites campaign creation by enabling you to import templates from the Meta dashboard with a single click. This capability is available only to CleverTap BSP customers. For more information, refer to the [Template Import](doc:clevertap-bsp#import-templates) documentation.

### Send Emails to Opted-out Users for Critical Updates and Announcements ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

With this feature, CleverTap now supports sending emails to unsubscribed contacts. This empowers customers to share crucial information, such as service updates, privacy policy changes, downtime/outage notifications, regulatory notices, and more, to all users, including those who have opted out of promotional messages. 

We aim to assist brands in informing users about essential updates that are strictly non-promotional. This helps Brands prioritize privacy and user preferences and deliver only crucial messages for an excellent user experience. Previously, Brands used the SendGrid API for this purpose, which requires additional integration efforts and leads to data silos. However, Brands can now deliver an excellent email experience, beyond promotional emails, directly from the CleverTap dashboard.

For more information, refer to the [Override Communication Preferences for Email](doc:create-message-override-opt-out#override-communication-preferences-for-email) document.

### Elevate Your Personalization Strategy with CleverTap and mParticle 360-degree Integration ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are thrilled to announce a major milestone with the release of CleverTap’s 360-degree integration with mParticle - a leading customer data platform. 


This integration enables a seamless exchange of customer event attributes and enriched attributes between CleverTap and mParticle. Our integration with mParticle now supports ***Audiences***, enabling the creation of actionable audiences (segments) within mParticle by defining specific parameters. You can then forward them to CleverTap for enhanced engagement. With real-time data collection from various sources, our customers can leverage the 360-degree customer profile (*Audiences*) created in mParticle and get a unified view of their users for enhanced personalization through our diverse omnichannel engagement suite.

The benefits of this integration include:

* Consolidate data from various sources (mobile, web, CRM) for a comprehensive understanding of customer behavior, driving impactful marketing campaigns.
* Create **Audiences** within mParticle, seamlessly synced with CleverTap, facilitating hyper-personalized omnichannel experiences.
* Combine CleverTap's system data with mParticle's extensive customer profiles, thereby unlocking valuable insights and empowering informed decision-making.

<Image alt="mParticle Integration with CleverTap" align="center" border={true} src="https://files.readme.io/e344cf0-mParticle_Import-20230823-075709.png" />  mParticle Integration with CleverTap











This integration is available for all CleverTap customers. For more information, refer to the [mParticle Import](doc:mparticle-import-audience) documentation.

### Enhanced Generic SMS Integration With Comprehensive Campaign Analytics ![BETA](https://files.readme.io/7776b09-Beta.svg)

We are excited to introduce the Enhanced Generic SMS Integration with SMS Callbacks (Beta) to all CleverTap customers. This feature allows customers to analyze the SMS campaigns and provider performance directly from the CleverTap dashboard. Previously, customers using the Generic SMS Integration relied on their SMS provider's dashboards for detailed campaign metrics such as Delivered, Replied, Clicks, and Delivery-related errors. With this enhancement, all SMS Campaign data is seamlessly unified with behavioral data within CleverTap. This eliminates the need for separate data sources and enables effortless tracking of SMS campaign impact.

To start using this feature, customers can collaborate with their SMS providers to enable callbacks. For more information, refer to the [SMS Callbacks](https://docs.clevertap.com/docs/generic-sms#sms-callbacks) document.

## July
### Introducing Charged Items Personalization for Deeper Personalization ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are thrilled to introduce Charged Items Personalization, taking our customers' personalization efforts to new levels. Previously, personalization in the `Items` event property was not possible due to the presence of multiple products within the array. With this new enhancement, you can now personalize the message using liquid tags for customers who purchase multiple items in a single transaction.

This enhancement mainly benefits our e-commerce clientele, who facilitate multi-product purchases through their mobile apps or websites. Customers can now send personalized *thank-you* or *summary* messages, mentioning specific product names based on every user’s individual purchases. This promotes enhanced user satisfaction and boosts click-through rates by delivering a truly personalized and engaging experience.

<Image alt="Liquid Personalization in the Items Event Property" align="center" border={true} src="https://files.readme.io/90f52db-Final_1.png" />  Liquid Personalization in the Items Event Property











For more information, check out the [Events](doc:events#charged-event) document.

### Introducing New NPS and User Ratings Templates with Deeper Insights! ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

We've added two new templates to our Web Popup channel: *NPS with Followup Question\_and \_User Ratings with Followup Question*. You can get more personalized and contextual feedback from users by following up the rating popup with a question.

You can choose whether this follow-up question appears in a grid format or as a list of options, as shown below:

<Image alt="NPS and User Ratings with Follow-up Questions" align="center" width="100% " border={true} src="https://files.readme.io/3443660-NPS_and_User_Ratings_Templates_Final.gif" />  NPS and User Ratings Templates with Follow-up Questions











For more information, refer to the [Ratings Templates](doc:create-message-web-popup#ratings-template) documentation.

### WhatsApp Campaign and Journey Analytics Enhancements for Deeper Insights ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce enhancements to our WhatsApp Campaign Stats and Reports. It provides deeper insights and improved performance tracking. The enhancements include:
* **Accurate Tracking of Sent Notifications:** Enhanced the calculation logic to ensure accurate tracking of sent notifications, eliminating discrepancies caused by callback errors.
* **Simplified Error Categorization:** Errors are now categorized into Delivery and Dispatch errors, making it easier to understand campaign issues.
* **Enhanced Campaign Conversion Funnel:** Track campaign effectiveness at each funnel stage with greater granularity, optimizing campaigns effectively.
* **Detailed Campaign Reports (Private Beta):** Gain deeper insights with additional data points such as conversion count and WhatsApp template details.

These enhancements are available to all CleverTap customers, except for the Campaign Report enhancements, which are currently in Private Beta. Reach out to our Customer Support to enable this feature. For more information, refer to the documentation links below:

* [WhatsApp Campaign Stats](https://docs.clevertap.com/docs/whatsapp-stats)
* [Journey Reports](https://docs.clevertap.com/docs/viewing-journey-reports#journey-nodewise-report)
* [Campaign Reports](https://docs.clevertap.com/docs/campaign-reports)

## June

### CleverTap Timezone Library Update ![Update](https://files.readme.io/0c15d9f-Tags.svg)

We are excited to announce that the CleverTap Timezone library is successfully updated, ensuring accurate timezones, including Mexico.

This update guarantees precise time representation across features. Specifically, this update impacts the **(GMT-06:00) America/Mexico\_City** time zone in CleverTap.

By implementing this update, we aim to provide a smoother experience for our valued customers. We recommend verifying product sections that utilize the *Date and Time* widget and *Delivery Preferences* as part of this update.

For any inquiries or concerns, contact our support team.

### Quick Reply with WhatsApp ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)


Deliver a seamless experience on WhatsApp by automating personalized two-way conversations with the new and improved Quick Reply Button for WhatsApp Templates. Previously, personalizing responses and tracking campaign attribution posed challenges due to a lack of context. This enhancement allows sending key-value pairs with a Quick Reply button, enabling personalized responses and clear attribution. Custom payloads enhance CleverTap campaigns and journeys, aiding in the automation of various business workflows. For more information, refer to the [Quick Reply](doc:create-message-whatsapp#quick-reply-button-with-custom-payload) documentation.

## May

### Enhanced Optimization & Flexibility in CleverTap Best Time to Send ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

> 📘 Note
>
> This feature is released in Private Beta. Reach out to your customer success manager to request early access to this feature.

We are excited to share the following enhancements in the Best Time feature for enhanced optimization and added flexibility for our customers:

* Identify **contextual Best Time** for users with the ability to set Best Time Config (up to 10 configs) with event property filter.
* View the **time distribution** and select **fallback time accordingly**: For users whose best time is not available (due to inactivity or other reasons), customers get the **flexibility** to view the best time user distribution and choose the fallback time to notify such users.

For more information, refer to the [documentation](doc:best-time).

### Introducing Phone Number Support for Facebook Audiences Remarketing Campaigns ![](https://files.readme.io/1829079-Enhancement_tag.svg)

We are excited to announce that we have recently implemented phone number support for Facebook Audiences re-engagement campaigns, expanding the reach of our customers' re-engagement efforts.

Earlier, we supported remarketing campaigns for users who have logged into Facebook using their email ids. Now we support phone number-based logins as well. With our latest update, all users who have logged in using either their **email address** or **phone number** can be reached for remarketing campaigns using Facebook Audiences.

This feature is available in campaigns as well as journeys.

For more information, refer to the [documentation](doc:create-message-fb-audience#define-the-message-content).


### IntelliNODE for Journey is Now Live! ![BETA](https://files.readme.io/7776b09-Beta.svg)

> 📘 Note
>
> This Public Beta release is available to all CleverTap Enterprise customers.

We are excited to announce that IntelliNODE for Journey is now live. 

CleverTap customers can now orchestrate A/B experimentations in user journeys. You can conduct experiments based on time, channel, content, or message frequencies in your user journey.

IntelliNODE empowers customers to build the most effective path and engagement strategy for their users.

For more information, refer to our [IntelliNODE](https://docs.clevertap.com/docs/intellinode-use-cases) documentation.

<Image align="center" className="border" border={true} src="https://files.readme.io/00546ac-IntelliNODE_1.png" />

### Improved Message Dispatch Throughput with Enhanced Firebase API ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

CleverTap now supports Firebase APIs that enable the concurrent delivery of 500 personalized messages with a single API call. This enhancement significantly improves dispatch throughput for customers sending personalized campaigns at scale.

Campaign delivery performance being an important success metric, this API enhancement is an indicator of the overall effort by CleverTap to set new standards for performance and scale. To activate this enhancement, customers simply need to provide additional details from their Firebase account to the *Settings* > *Mobile Push* page of CleverTap, which is a one-time process.

For more information, refer to the [documentation](https://developer.clevertap.com/docs/android-push#configure-fcm).

### SMS Click Tracking and Link Shortening ![](https://files.readme.io/bbc3552-PrivateBeta.svg "PrivateBeta.svg")

> 📘 Note
>
> Currently, this feature is released in Private Beta. If you want access to this feature, contact your Account Manager.

We are excited to announce the launch of SMS Click Tracking and Link Shortening for CleverTap customers,  making CleverTap a more comprehensive SMS marketing solution that enables everything from SMS content creation, testing, and tracking to link shortening, all from the same platform without any reliance on third-party tools.

A single-part SMS comprises only 160 and 70 characters in the GSM-7 and Unicode encoded format. And any long URL, like URLs with UTMs, can use up most of these characters leaving less or no room for the marketer to create engaging SMS content.


With this feature, you can:

* Curate compelling hyper-personalized messages containing long URLs within the SMS character limit.
* Track clicks and use the click behavior data from previous SMS campaigns and optimize future campaigns by offering similar products and offers, identifying the effective time of delivery, type of content, channel preference, and more.
* Optimize messaging costs by efficiently managing message length by utilizing link-shortening capability.

<Image align="center" className="border" border={true} src="https://files.readme.io/3f21afe-small-SMS_Click_Tracking_1.png" />

### Elevate Your Personalization and Analytics Strategies with CleverTap X Amplitude Bi-directional Integration ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

Adding to our strong list of tech integrations, we are excited to announce the **bi-directional integration** of CleverTap with **Amplitude** - a leading digital analytics platform that helps companies unlock the power of their products. 

You could already export CleverTap engagement event data to Amplitude for deeper analysis, but with this new bi-directional integration, behavioral cohort (segment) data can also be pushed from Amplitude to CleverTap. It creates a seamless and iterative cycle, enabling customers to refine their analytics for hyper-personalized experiences continuously.

<Image align="center" className="border" border={true} src="https://files.readme.io/3e41ead-small-CT-Amplitude.png" />

Here are some key benefits of this integration for CleverTap customers:


* **Enhanced Cohort Management**: Leverage Amplitude's product analytics to create targeted cohorts in CleverTap for personalized messaging and engagement campaigns based on user behaviors and preferences captured in Amplitude.
* **Comprehensive Event Tracking**: Capture and analyze user interactions within CleverTap, such as app installs, uninstallations, push notifications, and in-app messages, in Amplitude for a holistic view of user engagement across both platforms.
* **Data-Driven Decision Making**: Make informed decisions and optimize your customer engagement strategies by leveraging the combined insights from CleverTap and Amplitude's powerful analytics engines.
* **Personalized and Relevant Campaigns**: Deliver contextual and relevant messaging to your users based on their behaviors and preferences captured in Amplitude, leading to higher engagement and conversion rates.
* **Streamlined Workflow**: Seamlessly push cohorts and system events between CleverTap and Amplitude with a simple and intuitive setup, saving you time and effort in managing your marketing campaigns.

To learn more about this integration and how it can benefit your business, refer to the [Amplitude Import](https://docs.clevertap.com/docs/amplitude-cohort-import) documentation.

## April

### WhatsApp Business API ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

We are proud to announce that CleverTap is officially a WhatsApp BSP now, and this functionality is generally available to all CleverTap customers. This release eliminates dependencies for third-party WhatsApp Business Service Providers (BSPs) and provides an integrated, no-code WhatsApp solution to engage your users.

With this release, you can run omnichannel campaigns, including WhatsApp channel through CleverTap, without relying on third-party integrations.

<Image align="center" className="border" border={true} src="https://files.readme.io/58f61b4-small-WhatsApp.jpg" />

The WhatsApp Business API provides offers the following key benefits:


* **No Code Integration and Hassle-Free Onboarding**: Get started with WhatsApp campaigns quickly with just a few clicks and zero code effort.
* **Omnichannel Campaigns**: You can easily integrate WhatsApp into your omnichannel campaigns and deliver a consistent user experience across multiple engagement channels.
* **Cost Savings**: Pay for only one tool. No additional third-party partner fees and significant cost reduction.
* **Campaign Analytics**: Real-time, actionable campaign analytics, including sent, delivered, read, and replied metrics.

Learn more about [CleverTaps’s WhatsApp Business API](https://docs.clevertap.com/docs/clevertap-bsp) and get ready to take your WhatsApp campaigns to the next level with CleverTap!

### WhatsApp Enhancements - Advanced Personalization Capabilities for Creating Powerful Customer Experiences ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are incredibly excited to announce three new WhatsApp channel enhancements that will enable CleverTap customers to deliver a more contextual customer experience on WhatsApp.

With these enhancements, customers can utilize:

* **Linked content for real-time information**: Create personalized WhatsApp messages by incorporating rich and contextual data from sources outside CleverTap. This includes dynamically updating information such as available flight prices, latest news updates, movie reviews, game scores, and more directly into your messages.
* **Liquid tags for conditional messaging**: Use conditional logic such as *if-else* statements to personalize messages for each customer within the same campaign. For instance, you can offer a 20% discount to customers with a "gold" loyalty tier, while a 10% discount for all other tiers.
* **Catalog Send-Time Personalization**: Personalize messages with information from a catalog, such as product price, product category, product images, available inventory levels, and more. This information is pulled from the catalog when sending messages to your users. This ensures that your users receive the latest information.

These enhancements will be available for all CleverTap customers using WhatsApp Add-on. For more information, you can refer to our [catalog personalization](https://docs.clevertap.com/docs/personalize-message-whatsapp) documentation.

### Concurrency and Global Throttle for WhatsApp ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)


We have now introduced greater control for WhatsApp concurrency and throttle.

* **Concurrency**: We have added concurrency control for WhatsApp providers integrated via Generic WhatsApp Integration API. You can now manage the number of concurrent requests to the WhatsApp provider based on the provider’s capacity. This feature makes it easier to handle large numbers of requests without overloading the system. These capabilities are available for all WhatsApp Add-on customers on CleverTap. For more information, refer to the [WhatsApp Add-on](https://docs.clevertap.com/docs/social) documentation.
* **Throttle Control**: We have added throttle control for WhatsApp notifications. This capability provides better control over WhatsApp notifications. It allows you to manage app traffic and run campaigns below WhatsApp's throughput limits, improving campaign performance and preventing overload.  For more information, refer to [Throttle control](https://docs.clevertap.com/docs/messaging-frequency-caps#defined-limit) documentation.

### Ad Hoc Throttle Control At Campaign Level ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We have introduced Adhoc throttle control at the campaign level for Push, Email, SMS, Web Push, Webhook, and Whatsapp channels. This feature allows users to use a custom throttle for a particular campaign without changing global settings. This means you can customize the throttle for each campaign according to its needs, giving you greater flexibility and control.

For more information, refer to [adhoc limits](https://docs.clevertap.com/docs/messaging-frequency-caps#ad-hoc-limit).

### Scribe: OpenAI-Powered Writing Assistant and Emotion Analyzer ![Private Beta](https://files.readme.io/bbc3552-PrivateBeta.svg)

> 📘 Note
>
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

CleverTap is excited to introduce Scribe, an AI-powered writing assistant that can analyze and adjust the emotional tone of your content. An emotionally resonant campaign is the next step in hyper-personalization. With Scribe, you can:


* Automatically detect the emotional tone of your copy to ensure it conveys the intended emotion.
* Generate emotionally engaging copies at scale with few text prompts and remove writer's block.
* Paraphrase the current copy with varying emotions. Select the emotion that resonates best with your audience, or paraphrase again.
* Create copy in the language of your choice.
* Automatically add emojis and hashtags to the copy to enhance its appeal and reach.

<Image align="center" className="border" border={true} src="https://files.readme.io/57a13d2-Scribe_2.0.gif" />

For more information about Scribe, refer to the [Scribe](https://docs.clevertap.com/docs/scribe) documentation or [schedule a demo](https://clevertap.com/scribe/) with us.

### Pin Pivots to Boards for Collaborative Analysis ![BETA](https://files.readme.io/7776b09-Beta.svg)

> 📘 Note
>
> This is a Public Beta release and is available to all CleverTap customers.

We are pleased to announce that pivots can now be pinned to a custom board, enabling users to save the output of their analysis for future consumption and collaborate with other users. Users can pin any type of pivot chart to a custom board of their choice to save the output of their analysis for future consumption. They can also share it with other users for collaborative analysis.

For more information, refer to [Custom Dashboard](https://docs.clevertap.com/docs/custom-dashboards).

### Introducing the New Image-Only and Lead Generation Templates to Boost Engagement

We are excited to announce the release of two newly created out-of-the-box templates for enhanced engagement:

* Image-Only Template for Web Pop-ups
* Lead Generation Template for In-App and Web Pop-ups

> 📘 Note
>
> These features are available for all CleverTap customers.

**Image-Only Template**

Customers can now create visually appealing Web Pop-up campaigns using the Image-Only Template, resulting in improved engagement. 

This template offers customization options, such as selecting image dimensions for various devices and choosing from a range of style options, including borders, margins, background, and more.

<Image align="center" className="border" width="80% " border={true} src="https://files.readme.io/d6c9fe2-Image-Only.png" />

> 📘 Template support
>
> Image Only template is only supported on the new [Web SDK](https://developer.clevertap.com/docs/web-quickstart-guide) .

**Lead Generation Template**


CleverTap's Lead Generation Templates are now available for both Web Pop-ups and In-App users. These templates enable you to capture visitor details, including their name, email, phone number, and other user attributes helping convert anonymous visitors into known customers.

<Image align="center" className="border" width="80% " border={true} src="https://files.readme.io/55c1cd7-Lead_Generation.png" />

## March

### Cross Node Personalization (CNP) in Journeys ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce Cross Node Personalization (CNP) in Journeys.  This is the next step in personalizing your user messages. Based on user action, you can now personalize not only your first message but also subsequent messages in the user journey. CNP's powerful personalization provides a consistent messaging experience to your users across multiple channels. 

For more information about Cross Node Personalization, refer to the [user documentation](https://docs.clevertap.com/docs/personalization-in-journeys#personalize-events-across-nodes).

### New and Improved Partner UI with Enhanced Features for Exports ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

We are excited to announce the launch of a new and improved user interface for Partners and Exports. The new interface enables our customers to seamlessly integrate with partner solutions, allowing for easy exports with added functionalities.

> 📘 Note
>
> The new Partner User Interface and associated features are available to all CleverTap customers, with the requisite export access.

Along with the new UI, you get access to the following additional features:

* **Multiple buckets for S3 and GCP**: Connect multiple buckets for S3 and GCP, allowing easy data segregation and streamlined workflows.
* **IAM Policy for S3**: Configure the S3 buckets on CleverTap using the IAM policy, thereby eliminating the need for password sharing or IP whitelisting. To learn more, refer to the [AWS S3](https://docs.clevertap.com/docs/data-export-to-aws-s3) document. The flow for IAM policy is as below:

<Image align="center" className="border" border={true} src="https://files.readme.io/ff000af-AWS.png" />

* **Flexible Date Range for Export**: Export data as per your requirement for improved analysis and better workflows - create export for a specific day, date range, previous month, current month, and more.


For more information about these enhancements, check out the [documentation](https://docs.clevertap.com/docs/data-export-to-aws-s3) page.

## February

### Discover True Sources of Growth with CleverTap and Airbridge Integration ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

CleverTap has integrated with Airbridge - a leading attribution and incrementality measurement platform, to measure true marketing effectiveness across the web and mobile.\
With this integration, customers can:

* Identify the source of user acquisition. It will help create a customized onboarding experience resulting in higher user engagement and retention rate.
* Identify the acquisition channels that deliver the most engaged users and analyze the acquisition quality for strategic business and investment decisions.
* Track information for ‘Install Events’ and ‘In-App Events’, and measure campaign performance across multiple publishers via a unified dashboard.

For more information about CleverTap and Airbridge integration, refer to CleverTap's [Developer Documentation](https://developer.clevertap.com/docs/airbridge).

### Introducing CleverTap's Web Inbox Channel ![Private Beta](https://files.readme.io/bbc3552-PrivateBeta.svg)

We are excited to announce the launch of our new Web Inbox channel. 

> 📘 Private Beta
>
> This is a Private Beta Release. Contact your Customer Success Manager to request early access to this feature.

The [**Web Inbox**](https://docs.clevertap.com/docs/web-inbox) channel lets you display personalized messages in a notification inbox to your website visitors. It allows web visitors to quickly view and interact with notifications anytime in one place - the web inbox. Use the *no-code setup and out-of-the-box templates* to create web inbox notifications that are entirely customizable to match the website's branding. With this channel, you can re-engage users, maximize campaigns' impact, and boost conversions.

The graphic below illustrates a sample web inbox that appears when the user clicks the bell icon.

<Image title="WebInbox.png" alt={3665} align="center" className="border" width="80%" border={true} src="https://files.readme.io/b69406f-WebInbox.png" />

For more information about Web Inbox setup, refer to CleverTap's [Developer Documentation](https://developer.clevertap.com/docs/web-inbox).

## January

### No-code Workflow Automation with CleverTap and Zapier Integration ![BETA](https://files.readme.io/7776b09-Beta.svg)


Introducing CleverTap and Zapier's integration. This is a Beta Release. 

CleverTap and Zapier's no-code integration allows you to seamlessly transfer user information and events from various apps such as Salesforce, Google, Intuit, Dropbox, and so on to the CleverTap dashboard. You can run personalization campaigns and journeys based on data captured through Zapier. 

<Image title="Zapier.png" alt={3590} align="center" className="border" width="smart" border={true} src="https://files.readme.io/3cb3c41-Zapier.png" />

For more information about CleverTap and Zapier integration, refer to CleverTap's [User Documentation](https://docs.clevertap.com/docs/zapier). 

### New Out-of-the-box Templates for the Web Native Display Channel ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

Unveiling the *Banner Carousel* and *Banner Carousel with Text* templates for the Web Native Display channel. Web visitors spend most of their page-view time on the first fold. These templates help web visitors discover relevant content such as recommended products, personalized offers, and more on your webpage before they drop off.

> 📘 Private Beta
>
> This is a Private Beta Release. Contact your Customer Success Manager to request early access to this feature.

<Image title="Product new.gif" alt={1971} align="center" className="border" width="80%" border={true} src="https://files.readme.io/2181e27-Product_new.gif" />

With these templates, you can:

* Completely customize the carousel banners, including the title and description copy, style, and placement of the carousel.
* Display up to seven rotating banners to deliver a wide variety of content within a limited website area.
* Optimize images for mobile devices to enhance the viewing experience.
* Configure the carousel autorotation with a customizable slider time.
* Enable the carousel dots and navigation arrows to enable manual scroll.

Refer to the [User](https://docs.clevertap.com/docs/web-native-display-create-message#banner-carousel) and [Developer](https://developer.clevertap.com/docs/web-native-display#banner-and-carousel-templates) documentation for Banner Carousel to try out this exciting feature.

### WhatsApp Channel Add-on ![Update](https://files.readme.io/0c15d9f-Tags.svg)

Introducing the newest addition to the CleverTap for Startups Add-ons list - the *WhatsApp Channel*!


<Image title="WhatsApp Channel Add-on.png" alt={1373} align="center" className="border" width="80%" border={true} src="https://files.readme.io/2e0cb9e-WhatsApp_Channel_Add-on.png" />

WhatsApp channel has high reachability and engagement rates, making it one of the most attractive channels of engagement for businesses. 

You can now use the CleverTap WhatsApp messaging channel without upgrading your plan. All you need to do is [integrate the WhatsApp channel](https://docs.clevertap.com/docs/social) with the Business Service Provider of your choice, and you are all set to [create a WhatsApp campaign](https://docs.clevertap.com/docs/whatsapp) from the CleverTap dashboard.

# 2022

## December

### No-code Web Native Display Campaigns with Ready-to-use Templates ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

Now add more visual flair to your website with our new templates - [Banner](doc:web-native-display-create-message#banner) and [Banner with Text](doc:web-native-display-create-message#banner-with-text). Create and deliver contextual content without any coding effort with CleverTap's Web Native campaigns.

Learn more in the [Web Native Display](https://developer.clevertap.com/docs/web-native-display) and [Web Native Display Templates](https://docs.clevertap.com/docs/web-native-display-create-message#web-native-display-templates) documentation.

<Image title="No code native display.png" alt={1800} align="center" className="border" width="80%" border={true} src="https://files.readme.io/ce1ea83-No_code_native_display.png" />

### Push Notification Opt-in with CleverTap Push Primer ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

All apps targeting [Android 13](https://developer.clevertap.com/docs/android-push#android-13-changes) or [iOS 10](https://developer.clevertap.com/docs/in-app-notification-ios#ios-push-primer) and higher must ask for permission before sending a notification. This check empowers users to provide their consent for receiving notifications. CleverTap Push Primer helps you with the following: 

1. Gives your users the context of push notifications (see figure below).
2. Convinces them to opt-in (see figure below).
3. Enables you to request the user again for a previously declined permission. The user can opt for notification without manually opening the device’s settings (see figure below).


<Image title="Push Primer.png" alt={1800} align="center" className="border" width="80%" border={true} src="https://files.readme.io/7b263d8-Push_Primer.png" />

For more information, refer to [Android Push Primer](https://clevertap.com/blog/android-13-push-notification-opt-ins/) and [iOS Push Primer](https://clevertap.com/blog/asking-for-ios-push-notification-permissions/).

### Superfast Campaign Reports ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

Get lightning-fast reports for up to 2000 campaigns in a minimum of 20 minutes - 20 times faster than before. But wait, there's more! Automate the ingestion of reports to your cloud partners, such as Amazon S3 or GCP.

Learn how to set up [Campaign Reports](doc:campaign-reports).

### Make Informed Decisions with our Webhooks ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Get a holistic view of your user’s information or data to make informed decisions.

> 📘 Availability
>
> This enhancement is available only on the new campaign interface.

You can now update your CRMs with holistic user information such as *lat/long,* *phone number*, *city*, and so on. You can also check the reachability of users on each messaging channel. 

Try [Creating a Webhook](https://docs.clevertap.com/docs/create-message-webhook) and test this new enhancement.

<Image title="Webhook Informed_Decisions.png" alt={1592} align="center" className="border" width="80%" border={true} src="https://files.readme.io/5354cb7-Webhook_Informed_Decisions.png" />

### Manage WhatsApp Providers on CleverTap ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing the new WhatsApp Provider Management enhancement on CleverTap! This enhancement allows you to:

* Edit, archive, or delete your WhatsApp providers from the dashboard, declutter your view, and stay organized. You can archive a provider to hide it from view. You can also delete provider and provider data completely. Archiving or deleting a provider stops the related campaigns and journeys.
* Edit provider settings and update configurations directly from the WhatsApp channel *Settings* page.

Learn more in the [Manage WhatsApp Providers](https://docs.clevertap.com/docs/setup-whatsapp#provider-operations) documentation. 

### Project Activity Dashboard v1.0 ![Enhancemnt](https://files.readme.io/7f99f23-Tags-1.svg)


Introducing our new adoption and usage tracking dashboard - exclusively available for *CleverTap for Startups* users. Supercharge your team's performance with this powerful tool by CleverTap.

With this enhancement, you can get the following:

* A holistic view of your user engagement channels and activity update. 

<Image title="Project_Activity_Dashboard1.png" alt={1010} align="center" className="border" width="80%" border={true} src="https://files.readme.io/4f52cf4-Project_Activity_Dashboard1.png" />

* Identify unused features and configurations and make the most of them with our recommendations. 

<Image title="Project_Activity_Dashboard2.png" alt={2020} align="center" className="border" width="80%" border={true} src="https://files.readme.io/913bd4b-Project_Activity_Dashboard2.png" />

### Seamless Email-to-App Experience with AppsFlyer's Deep Linking Suite ![Enhancement](https://files.readme.io/7f99f23-Tags-1.svg)

Introducing the ability to define AppsFlyer deep links in the CleverTap dashboard - a game-changing update that streamlines the email-to-app experience, quickly directs users to your app, and helps increase conversion rates. Create personalized journeys and measure campaign performance with AppsFlyer's Deep Linking Suite.

Refer to [AppsFlyer Onelink](https://docs.clevertap.com/docs/setup-email#appsflyer-onelink) for more information.

<Image title="CT AppsFlyer Integration.png" alt={1800} align="center" className="border" width="80%" border={true} src="https://files.readme.io/7195228-CT_AppsFlyer_Integration.png" />

### Create Mobile Push Campaigns using API ![Update](https://files.readme.io/0c15d9f-Tags.svg)

Introducing a powerful update to the *Create Campaign* API for mobile push campaigns. Set goals, goal conversion events, and revenue properties from the API. Control user reach and limit costs. Create timezone campaigns and DND preferences, and set up campaigns for multiple dates or set up recurring campaigns. Create effective push messages from the API using different keys such as Summary, Subtitle, Collapse key, and more.

For more information, refer to [Mobile Push Notification Parameters](https://developer.clevertap.com/docs/create-campaign-api#body-parameters---target-user-events--properties).

## November

### RenderMax<sup>TM</sup> - Push Notification Rendering Technology by CleverTap ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)


CleverTap's Push Notification Rendering Technology boosts push render rates up to 90%. With RenderMax, engage users you could not before and elevate your push campaigns’ ROI. 

While most other solutions focus only on increasing delivery rates, CleverTap RenderMax solves the challenge of delivering and *rendering* push notifications on Android OEM devices. It powers up the render rates of a push notification, amplifies reach, and maximizes user engagement.

To learn more about how you can improve push notification render rates, refer to [RenderMax](https://docs.clevertap.com/docs/rendermax) or [ask for a demo](https://clevertap.com/rendermax/).

<Image title="RenderMax.png" alt={1800} align="center" className="border" width="80%" border={true} src="https://files.readme.io/e1f02c9-RenderMax.png" />

### Supercharge WhatsApp Campaigns with Enhanced Experimentation and Optimization ![New Feature](https://files.readme.io/c30bf56-NewFeature.svg)

> 📘 Availability
>
> This enhancement is available only on the new campaign interface.

The WhatsApp channel is now powered with additional capabilities around experimentation and optimization, giving you the ability to:

* Experiment with A/B and multivariate testing to compare up to three message versions using different templates, copies, creative calls to action, or any combination, to identify what works best.
* Utilize Split Delivery to decide what percentage of the audience gets a particular message variant and compare variant stats to identify the winning variant.
* Create Multi-variant Campaigns optimized for location, demographics, purchase trends, and more. Create up to 50 variants of the same message based on a user property type (for example, language) to boost engagement and conversion.

For more information, refer to the [WhatsApp Message Types](https://docs.clevertap.com/docs/create-message-whatsapp#whatsapp-message-types).

### Push Amplification is now Pull Notification ![Update](https://files.readme.io/0c15d9f-Tags.svg)

The Push Amplification feature is now called Pull Notifications. The new name truly reflects the functioning and benefit of this feature because it pulls the pending notifications from the CleverTap server and successfully delivers them to mobile devices.

<Image title="Pull Notification.png" alt={1800} align="center" className="border" width="80%" border={true} src="https://files.readme.io/581c22f-Pull_Notification.png" />

## Previous Releases


Click the following link to view all the details related to previous releases.


<details>
  <summary>Click to expand</summary>

### October

#### Supercharging Web Channel Campaigns with Enhanced Experimentation, Optimization, and Personalization Features

We understand the importance of creating exceptional experiences for your users, whether they visit your app or website. In our drive to help create better omnichannel experiences, we are introducing enhancements to web channel campaigns run through CleverTap. With these enhancements, you can deliver exceptional web user experiences through better workflows, additional experimentation options, and improved analytics.

* With custom HTML templates utilizing click-tracking metrics, you will be able to measure the impact of your web pop-up and exit intent campaigns.
* Keeping the importance of visuals in mind, we are now providing you the ability to personalize images used in web channel campaigns based on user property, event property, and product recommendations. You can also host images for your web channel campaigns directly on CleverTap’s CDN, eliminating the dependence on third-party solutions. This will help you deliver user experiences that are even more contextual and hyper-personal.
* To help you experiment, you can now compare up to three message versions with different copies, calls to action, or a combination of these, in your web channel campaigns. This helps you experiment with more creative options and see the impact it generates on engagement and/or conversions.
* To optimize your web campaigns, you can now use the Split Delivery feature to decide what percentage of the audience gets a particular message variant and compare campaign stats to identify the winning variant, which can become the default variant. You can also optimize web campaigns based on user properties and create up to 50 variants of the same message to drive experimentation and engagement.

For more information, refer to the documentation for [Web Push](https://docs.clevertap.com/docs/create-message-web-push#web-push-message-types), [Web Pop-up](https://docs.clevertap.com/docs/create-message-web-popup#web-pop-up-message-types), and [Web Exit Intent](https://docs.clevertap.com/docs/create-message-web-exit-intent#web-exit-intent-pop-up-message-types) channels. Please note that these enhancements are available in the new Campaigns interface on CleverTap.

### July

#### 2FA Key Reset Within the CleverTap Dashboard

2FA key management is now available from within the CleverTap dashboard. With this feature, admin users can directly reset 2FA keys in case of loss of credentials, eliminating the dependency on the CleverTap support team. This feature can be accessed directly from the Security menu under Settings for any user within a project.

This feature will be available for all customers across all the plans. For more information, check out the documentation page [here](https://docs.clevertap.com/docs/account-2fa).

#### Personalize WhatsApp Notifications based on Past User Responses

The updated WhatsApp Notification Replied event now captures a lot more data comparatively as event properties such as incoming message type, incoming text, incoming media URL, and so on, enabling you to trigger & personalize WhatsApp notifications based on the user’s past response. 

With this update, you can:

* Create highly personalized Journeys and WhatsApp Campaigns utilizing the user’s WhatsApp response attributes.
* Build automated chat workflows to deliver quicker responses using the event property ‘incoming text’ as the triggering criteria.
* Analyze the behavior of their users based on their WhatsApp responses to identify trends and aggregate them into segments and engage them.

The feature will be available to all CleverTap WhatsApp add-on customers in both the new and legacy Campaigns experience. For more information, check out the documentation page [here](https://docs.clevertap.com/docs/events#system-events).

<Image title="Personalize Whatsapp Notifactions.png" alt={1536} align="center" className="border" width="80%" border={true} src="https://files.readme.io/eed703c-Personalize_Whatsapp_Notifactions.png" />

### June

#### Preview Dark Mode for Emails in the Drag and Drop Editor

We are excited to introduce the new dark mode email preview capability using the email drag and drop editor. 

Dark mode is a very popular feature used by end consumers; hence it is becoming an integral part of the email creation experience. Marketers must often test for light mode and dark mode compatibility across devices and email clients before sending emails.

Customers can now view how the email looks in the dark and light modes and switch the preview in real-time with a toggle button. 

This feature is available in the preview and test section of the email drag and drop editor and for desktop and mobile device previews in the new Campaign experience. 

Please visit the [documentation](https://docs.clevertap.com/docs/email-editor-templates#device-preview) for more information. 

#### Gmail Promotional Annotations (Beta) – Enhance Email Discoverability & Engagement

Gmail Promotional Annotations enable you to:

* Highlight key information such as images, logo, promo codes, the expiration date on deals, etc., along with the subject and the preheader text in Gmail’s Promotions tab 
* Showcase relevant information to recipients upfront, even before they open their emails
* Add expiry dates to promotional emails, which provides two opportunities for customer emails to get highlighted in the Promotions tab, first when the email was sent and second when the offer is about to expire without them having to send a second email 

Simply upload logos, images, discounts, offer code and start/end date, subject line, and the sender’s name you want to be highlighted while setting up emails in CleverTap.

Currently, Gmail provides annotations only for mobile inboxes. This capability may be extended to the desktop inboxes at a later date. 

This feature will be available across all the plans but only in the new CleverTap campaigns UI. For more information, check out the documentation page [here](https://docs.clevertap.com/docs/gmail-promotional-annotations).

<Image title="Gmail Promotional Annotations.png" alt={1536} align="center" className="border" width="80%" border={true} src="https://files.readme.io/e043eeb-Gmail_Promotional_Annotations.png" />

### May

#### Variant Specific A/B Test Analysis on the Notification Sent Event for Deeper Insights

CleverTap customers can now analyze users who were sent a specific variant of an A/B test campaign, from within the Analytics section.

Customers can leverage the **‘Variant’** event property filter of the **‘Notification Sent’** event, in addition to the other notification based events like notification clicked, viewed, etc. This helps perform even better analysis and query users across different sections (funnels, segments, etc). Customers can download the list of users who were sent a specific variant and save it as a segment for further actions.

This feature is available for all CleverTap customers.

#### Inclusion of Composite Events Within the Total Active Events Count on the CleverTap Dashboard

Composite events counts are now included within the Total active events count on the CleverTap dashboard, with a tooltip explaining the same. Although composite events count was always included in the total active events count in the backend, this enhancement ensures the same data reflects on the CleverTap dashboard with absolute transparency. Customers can now view the total active events count as a sum of active System, Custom, and Composite events on the dashboard. This would give customers an enhanced clarity on the number of events created so far and ascertain how many more can be added within the allotted limits. 

This feature is available for all CleverTap customers.

### April

#### WhatsApp as a Campaign Type in all WhatsApp-related System Events

WhatsApp has been added as a Campaign Type property value in all WhatsApp-related system events. You can now utilize this capability to easily analyze the performance of WhatsApp campaigns aggregated at a channel level. 

This feature will be available for all customers, across all the plans. 

<Image title="Whatsapp As a Campain Type (1).png" alt={768} align="center" className="border" width="80%" border={true} src="https://files.readme.io/433f05d-Whatsapp_As_a_Campain_Type_1.png" />

### March

#### Support for Multiple WhatsApp Numbers Within a CleverTap Project

Now you can create distinguished WhatsApp experiences for multiple business stakeholders, like customers of different products and business verticals, suppliers, partners etc. by utilizing separate WhatsApp numbers within a CleverTap project to deliver unique experiences.

With this capability you can:

* Use multiple phone numbers with a BSP or multiple BSP accounts within a single CleverTap project  
* Manage WhatsApp templates separately for each number
* Create campaigns and send notifications using any WhatsApp business number

This feature will be available across all the plans. For more information check out the documentation page [here](https://docs.clevertap.com/docs/gupshup).

#### Execute and Track NPS Surveys from within the CleverTap Dashboard

You can now run and track NPS surveys directly through the CleverTap dashboard. NPS survey has been added to the Web Pop-up & In-App Messaging template to enable set up, execution, and tracking of results, with ease. With this release you:

* No longer need to rely on external survey tools to capture NPS scores and manually import data into CleverTap to track it.  
* Can completely customize the NPS survey template to reflect their brand guidelines by changing the look and feel, labels, copy, CTA etc. 
* Can easily track the NPS scores and the campaign metrics from the pre-built NPS board.

Please note that this feature is available only for customers who have migrated to the new Campaigns UI. [Learn more](https://docs.clevertap.com/docs/web-pop-up).

#### IP Whitelisting Management Now Available within the CleverTap Dashboard

IP Whitelisting management is now available from within the CleverTap dashboard. Users with admin access can now view, add and remove IPs directly from the Security menu under Settings. This means complete control of the network access to your projects without any dependence on the CleverTap support team. 

This feature will be available for all customers, across all the plans. For more information check out the documentation page [here](https://docs.clevertap.com/docs/ip-whitelisting).

### February

#### SMS Provider Management Enhancement Now Live

SMS CRUD support allows CleverTap customers to delete or archive existing SMS providers.

Customers will be able to manage the campaigns and journeys running on archived and deleted SMS providers and will be able to shift them to their preferred SMS provider for continued engagement. 

SMS providers and customers can cut the unnecessary billing cost of discontinued campaigns, This will help in the accountability and the billing for SMS providers of customers.  

The feature is available for all customers, across all plans.

### January

#### Build More Engaging Emails and Streamline Email Campaign Creation with the Enhanced Email Editor

With the enhanced Email Editor you can:

* Build mobile-optimized email templates using the mobile view editor, without switching back and forth between editor and preview mode 
* Create more engaging emails by utilizing stickers and GIFs 
* Easily add titles to email templates using the Title block
* Streamline the way you add space to email templates using the Spacer block
* Easily manage saved rows with an option to delete, rename, and even re-organize rows from within the editor

This enhancement will be available for all CleverTap customers across all the plans and both in the old and new Campaigns experience.

<Image title="Build More Engaging Emails (1).png" alt={1536} align="center" className="border" width="80%" border={true} src="https://files.readme.io/18eca96-Build_More_Engaging_Emails_1.png" />

<br />

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
</details>