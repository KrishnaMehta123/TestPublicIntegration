---
title: Generic RCS
excerpt: Learn how to setup Generic RCS provider in CleverTap
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

> 📘 Private Beta
>
> Generic RCS is available as part of the RCS Connect add-on and is currently in Private Beta for select CleverTap accounts. For early access to this feature, contact your Customer Success Manager or Account Manager.

*Generic RCS* enables businesses to deliver rich, interactive text messages with branded content and multimedia by connecting their own Business Service Provider (BSP) to CleverTap via *RCS Connect*. This option is ideal if you already have an RCS-capable vendor and want to orchestrate campaigns, tracking, and automation from CleverTap.

By integrating Generic RCS with CleverTap, you can streamline RCS campaigns, configure templates, track delivery and engagement, and enable SMS fallback for reliable delivery when RCS is unavailable. In this document, Generic RCS refers to CleverTap’s provider option that connects your BSP to CleverTap using the Generic RCS API.

> 📘 RCS Messaging Support
>
> Your vendor must support the *CleverTap API for RCS messaging*. If not, a middleware is required to connect it.

# Prerequisites

Before you can start using *Generic RCS with CleverTap* at scale, check that the following prerequisites are completed:

* RCS agent approved with your BSP; refer [RCS Agent Onboarding](doc:generic-rcs#rcs-agent-onboarding).
* Vendor connectivity ready: supports Generic RCS API or middleware in place.
* Messaging endpoint available: vendor-provided HTTPS URL; refer [Messaging Endpoint](doc:generic-rcs#messaging-endpoint).
* Authentication decided: No authentication, Basic, or OAuth 2.0; refer [Authentication](doc:generic-rcs#authentication).
* Required headers identified: for example, `Content-Type`, `Authorization`; refer [Headers](doc:generic-rcs#headers).
* Delivery report callback URL confirmed with your vendor.
* RCS Sender ID provisioned by your BSP.
* Throughput guidance from the vendor to set *Custom Concurrency*.
* (Optional) SMS fallback ready: SMS Sender ID and body parameters; for India, DLT registration (Principal Entity ID and approved template IDs).
* Test assets prepared: at least one RCS-capable device/number and media URLs for cards/carousels.

## RCS Agent Onboarding

This section defines the RCS Agent and outlines the steps required before configuring the provider in CleverTap.

An *RCS Agent* is your brand’s verified business profile (sender) that is provisioned by your Business Service Provider (BSP) and approved by mobile carriers. CleverTap uses this sender as the *RCS Sender ID* during provider setup to authorize and deliver RCS traffic.

The onboarding process includes:

* Registering your business with the BSP as an RCS sender and creating the brand profile (name, logo, description, website).
* Submit brand and compliance details for carrier review and obtain approval for RCS messaging.
* Completing the BSP’s verification checks (for example, domain or business verification).
* Receiving the provisioned sender details from the BSP (agent ID and any region-specific identifiers) and mapping them to the *RCS Sender ID* in CleverTap during provider configuration.

## Set Up Generic RCS on CleverTap Dashboard

This section describes how to configure your vendor in the dashboard and send a test message. Go to *Settings > Channels > SMS > SMS Connect > + Add Provider*. Refer to [Generic RCS API ](https://developer.clevertap.com/docs/generic-rcs-api) for payload formats and delivery callbacks.

### Messaging Endpoint

To enable seamless integration between CleverTap and your RCS vendor, configure the following:

* **Request Type**: `POST` (or as required by your vendor).
* **HTTPS Endpoint**: Enter the **vendor-provided** HTTPS URL for their RCS send API. This endpoint is issued and maintained by your BSP/vendor; creation and management occur on the vendor side and are out of scope for this guide. Paste this URL into the field during provider setup.

### Authentication

Select the authentication method supported by your RCS vendor. CleverTap provides three options:

* **No Authentication**

  Select this option if your vendor does not require authentication. No additional fields need to be configured.

* **Basic Authentication**

  If your vendor requires basic credentials, provide the following:

  * *User ID*: The unique username issued by your vendor.
  * *Password*: The corresponding password provided by your vendor.

* **OAuth 2.0**

  If your vendor supports OAuth 2.0, configure the following fields:

  * *Client URL*: The OAuth token endpoint provided by your vendor.
  * *Client ID*: The unique client identifier assigned to your application.
  * *Secret Key*: The client secret used to authenticate your requests.

### Headers

Add the required HTTP headers as **key–value pairs**. These headers are included in each API call CleverTap makes to your RCS vendor and may include:

* `Content-Type`: Specifies the format of the payload (for example, `application/json` or `application/x-www-form-urlencoded`).
* `Authorization`: Used when your vendor requires bearer tokens or API keys in the header.
* Vendor-specific headers: For example, `api-key`, `vendor-id`, version, or feature flags.

Refer to the [Generic SMS provider](https://docs.clevertap.com/docs/generic-sms)  for detailed guidance on how headers are configured in CleverTap’s generic HTTP-based integrations.

### Custom Concurrency

Custom Concurrency allows you to define the **maximum number of parallel requests** that CleverTap will send to your RCS vendor’s API at any given time from provider setup on the CleverTap dashboard. This ensures your outbound traffic respects the vendor’s throughput limits and avoids throttling or request failures.

* If your vendor specifies a **recommended limit**, enter that value here.
* If left blank, CleverTap uses its default concurrency settings.
* Adjusting this value can help optimize delivery speed while maintaining stability with your vendor’s infrastructure.
* The maximum request rate is 4,600 requests per second.

> 📘 Note
>
> * Setting a higher concurrency than supported by your vendor may result in **rate limiting, message drops, or delayed delivery reports**. Always check with your RCS vendor before updating this field.

# RCS Setup in CleverTap

Once your RCS Agent is onboarded, configure RCS settings in CleverTap:

* Go to *Settings > Channels > SMS Connect* in your CleverTap dashboard.
* Select **Generic RCS Provider** as the provider and enter the required credentials.
* Configure message templates, sender IDs, and any additional settings needed for your use case.

# Set Up Generic RCS on CleverTap Dashboard

To successfully integrate your vendor with CleverTap, follow the steps below to configure your RCS settings.

1. Go to *Settings > Channels > SMS > SMS Connect* and click **+ Add Provider**

2. Add the following details: 

   <Image alt="Generic RCS - Provider Setup" align="center" width="60% " border={true} src="https://files.readme.io/7bd526c0c1839efcaa5fa05cca9349576f85cfd82dcfadd1c3ed384a6ca0854a-image_71.png">
     Generic RCS - Provider Setup
   </Image>

* ###### Provider

  Select Generic RCS Provider from the drop-down menu.

* ###### Nickname

  A customizable label for your Generic RCS integration. This name helps you easily identify and manage the integration within the CleverTap dashboard, making it convenient to distinguish between multiple configurations.

* ###### Messaging Endpoint

  Enter the [HTTPS endpoint](doc:generic-rcs#messaging-endpoint) provided by your vendor along with the appropriate request type (for example, POST).

* ###### Authentication

  Select the [authentication](doc:generic-rcs#authentication) type and provide the required credentials:

  * **No Authentication**: No credentials required.
  * **Basic Authentication**: Enter **User ID** and **Password**.
  * **OAuth 2.0**: Enter **Client URL**, **Client ID**, and **Secret Key**.

* ###### Headers

  Add the necessary [header](doc:generic-rcs#headers) parameters as key–value pairs. Examples include `Content-Type`, authorization tokens, or vendor-specific identifiers. See the [Generic SMS provider documentation](https://docs.clevertap.com/docs/generic-sms) for guidance on configuring headers in CleverTap.

* ###### Custom Concurrency

  Define the maximum number of parallel requests CleverTap should send to your vendor using [Custom Concurrency](doc:generic-rcs#messaging-endpoint). Always use the recommended limit shared by your vendor to avoid throttling. 

* ###### RCS Sender ID

  The RCS Sender ID is the unique identifier of your RCS Agent (business profile) used to send messages. It’s what recipients view as the sender of your RCS messages, typically a brand name or number associated with your business. This helps build recognition and trust with your audience. Depending on your region, the Sender ID may be provisioned by your vendor or telecom partner. 

* ###### RCS Body Parameters

  Add vendor-specific key–value pairs that must be included in the body of RCS requests.

* ###### Delivery Report Callback URL

  Enter the URL where your vendor will post delivery status updates for messages sent through this provider. These callbacks indicate whether each message was *delivered*, *failed*, or *queued*, enabling real-time tracking of your RCS campaigns.

* ###### SMS Configuration / Enable Fallback SMS

  SMS fallback ensures message delivery when RCS messages fail due to factors such as device incompatibility, lack of internet access, or carrier restrictions. If the recipient’s device doesn’t support RCS or is offline, the message is automatically sent as an SMS to maintain uninterrupted communication.

  To enable SMS fallback in the CleverTap–Generic RCS integration, the following configurations apply:

  * **SMS Sender ID**: Required if SMS fallback is enabled.

  * **SMS Body Parameters**: Add the required key–value pairs needed by your SMS vendor.

  > 📘 Note
  >
  > If you are sending messages in India, DLT (Distributed Ledger Technology) registration is mandatory. Check that you configure the **Principal Entity ID** and approved template IDs as per TRAI regulations.

* ###### Mark as Default

  Enable this option to set the Generic RCS provider as your primary service provider for RCS messaging.

3. Select **Send Test** to verify that the integration is functioning correctly. When you click **Send Test**, you will be prompted to enter the following details:

   * **Country Code & Mobile Number**: Specify the recipient’s country code and mobile number to test message delivery.
   * **RCS Message**: Enter the message content to be sent via RCS.

4. Select **Save** after you have successfully verified the integration.

Once the **Provider** is added, navigate to the *Provider Listing* page for [Provider Operations](doc:rcs-setup#provider-operations).

# Add a Template

The Add Template feature in the CleverTap Dashboard allows you to create, manage, and deploy RCS message templates for your campaigns. These templates ensure consistent messaging and, if applicable, can be submitted to your vendor or carriers for approval. If your vendor requires approval, create the template in the vendor portal first, then create the same template in CleverTap under Templates. Use the exact same Template Name in both systems so submissions map correctly.

To access templates, navigate to *Settings > Partners > SMS > SMS Connect > + Provider*. Select **Generic RCS Provider** from the list and click the *Templates* tab. CleverTap supports three template formats, including the following:

To access templates, navigate to *Settings* > *Partners* > *SMS* > *SMS Connect*. Select the required provider and switch to **Templates** . CleverTap supports three template formats, including the following:

* [Text](https://docs.clevertap.com/docs/rcs-message-templates#text)
* [Rich Card](https://docs.clevertap.com/docs/rcs-message-templates#rich-card-template) 
* [Carousel Template](https://docs.clevertap.com/docs/rcs-message-templates#carousel) 

This feature enables businesses to automate messaging workflows, maintain brand consistency, and enhance customer communication through RCS campaigns.
