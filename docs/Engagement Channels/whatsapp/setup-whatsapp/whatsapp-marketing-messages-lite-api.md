---
title: WhatsApp Marketing Messages Lite API
excerpt: >-
  Learn how to enable and manage the MM Lite API for WhatsApp Direct in
  CleverTap.
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

The Marketing Messages Lite API (MM Lite API) is Meta’s lightweight, performance-optimized version of the [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api), designed exclusively for sending WhatsApp marketing messages. It is available only to CleverTap customers using [**WhatsApp Direct**](https://docs.clevertap.com/docs/whatsapp-direct-add-on).

MM Lite runs seamlessly in the background to optimize marketing message delivery, engagement, and cost—without requiring any changes to your [**campaign**](https://docs.clevertap.com/docs/campaigns) or [**journey**](https://docs.clevertap.com/docs/journeys) setup. Once enabled, CleverTap automatically routes eligible marketing messages via MM Lite, while continuing to use the Cloud API for support, authentication, and transactional communication. Your [**templates**](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines) remain unchanged and fully compatible.

If you're using **WhatsApp Connect** (via a third-party BSP), contact your provider to check for MM Lite API onboarding support.

# Benefits of Using MM Lite API

Brands using MM Lite API benefit from:

* **Better Delivery Performance**\
  Meta’s AI optimizes message delivery, dynamically prioritizing users most likely to engage, leading to higher delivery rates for marketing campaigns.

* **No Additional Setup**\
  Continue using your existing [**Campaigns**](https://docs.clevertap.com/docs/campaigns) and [**Journeys**](https://docs.clevertap.com/docs/journeys). Once MM Lite is enabled, CleverTap automatically routes eligible marketing messages via MM Lite.

* **Rich Analytics**\
  Access granular insights such as reads, clicks, and conversions through [WhatsApp Manager](https://business.facebook.com/wa/manage) (for WhatsApp Direct users) or via your BSP dashboard (for WhatsApp Connect, if supported).

* **TTL Control** *(Coming Soon)*\
  Set Time-to-Live (TTL) values on marketing templates to ensure timely, relevant delivery based on campaign urgency.

# Prerequisites

Before enabling MM Lite API for a WhatsApp Business Account (WABA), ensure the following conditions are met:

* The [**Facebook Business Manager**](https://www.facebook.com/business/help/1710077379203657) associated with your WABA is verified.
* The **phone number is registered** via the [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/get-started).
* At least **one marketing template** is approved via Meta’s [Message Templates](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines).

# Comparison: MM Lite API vs. Cloud API

The MM Lite API is built on top of Meta’s [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api), a general-purpose interface for sending and receiving messages on WhatsApp. The Cloud API supports a broad set of use cases, including support, authentication, transactional, and marketing communication. In contrast, the MM Lite API is designed specifically for outbound marketing messages and includes backend optimizations that improve delivery performance, lower cost per message, and unlock richer analytics—while leveraging the same Cloud infrastructure.

The table below highlights how the two APIs differ across key functional and performance dimensions:

| Aspect       | Cloud API                               | MM Lite API                                                                                      |
| ------------ | --------------------------------------- | ------------------------------------------------------------------------------------------------ |
| **Purpose**  | Multipurpose (Support, Auth, Marketing) | Dedicated to marketing messages only                                                             |
| **Delivery** | Bulk dispatch, no optimization          | AI-optimized delivery handled by Meta infrastructure for improved engagement                     |
| **Insights** | Basic metrics                           | Detailed analytics including reads, clicks, and conversions                                      |
| **TTL**      | Only for Utility templates              | TTL for marketing templates supported by Meta; CleverTap support for this feature is coming soon |

# Verify MM Lite API Eligibility

You can enable MM Lite API only if your WABA meets all the following criteria:

* Facebook Business Manager is verified.
* WABA is registered via the Cloud API.
* At least one approved marketing template exists.

## MM Lite API Status Indicators

The MM Lite API status indicates the current eligibility or activation state of a WhatsApp Business Account (WABA) within CleverTap. It helps you identify whether a WABA is ready for onboarding, has already been onboarded, or does not yet meet the necessary criteria. To view the status:

1. Go to *Settings > Channels > WhatsApp*.
2. Click the **WhatsApp Direct** tab, and check the *MM Lite Status* column in the WABA list.

The following table below describes the meaning of each status value:

| Status         | Description                                 |
| -------------- | ------------------------------------------- |
| *Not Eligible* | WABA does not meet the minimum requirements |
| *Eligible*     | Ready for onboarding                        |
| *Onboarded*    | MM Lite has been successfully enabled       |

> 📘 Note
>
> MM Lite API status is maintained at the WABA level and applies across all CleverTap projects associated with that WABA. If the same WABA is used in multiple projects, onboarding is required only once, and the status is reflected in each project.

<Image alt="MM Lite Status" align="center" border={true} src="https://files.readme.io/5483c1cdeed73e3825f5f1c6b1b007b226d357f2435aa31d0df5b9232b0d7603-MM_Lite_status.png">
  MM Lite Status
</Image>

# Enable MM Lite API for Your WABA

Once a WABA is eligible, you can start the onboarding process from within CleverTap:

1. Go to *Settings > Channels > WhatsApp*.
2. Select the **WhatsApp Direct** tab.
3. In the *MM Lite Status* column, find the WABA marked as *Eligible*. and click ![](https://files.readme.io/127ad2caa9f8ce7847485cc41635bd3e8e470b34712613e8dba704cc19c800cf-2025-06-25_11-28-30.png) next to the WABA.
4. In the popup dialog, click **Enable & Continue** to proceed. 

   <Image alt="Enable and Continue" align="center" border={true} src="https://files.readme.io/d13df176d109e9bd41983a2b2a400e94da3c733c59bf660ec5d98fa5b08566fd-MM_Lite_API_enable_and_continue.png">
     Enable and Continue
   </Image>
5. A Meta onboarding dialog will appear:

   * Select your **Facebook Business Manager**.
   * Review and **grant the required consents**.

     <Image alt="Meta Onboarding" align="center" width="65% " border={true} src="https://files.readme.io/e2cd9d210ee3bb583eda63615ec0812b0dbc2edfb5e6f9748768f540e4891183-meta_onboarding.png">
       Meta Onboarding
     </Image>

Once complete, the MM Lite Status will update to **Onboarded**.

> 📘 MM Lite Status
>
> After completing the onboarding flow, MM Lite API is enabled immediately from Meta and can be used for marketing campaigns. However, the **MM Lite Status** in the CleverTap dashboard may take up to **2–3 days** to reflect the updated state. This delay does not impact functionality—messages will be routed via MM Lite API as soon as onboarding is completed.

> ⚠️ Note
>
> Onboarding is irreversible. After onboarding, all marketing messages will be sent via MM Lite API.

# Click Tracking and Attribution

When marketing messages are sent via MM Lite API, Meta appends a **Click ID (fbclid)** to outbound links to support conversion tracking. This ID helps attribute user actions such as purchases, sign-ups, or app installs back to the original message, especially when integrated with Meta’s [Conversions API](https://developers.facebook.com/docs/marketing-api/conversions-api/), which allows businesses to send conversion events directly from their servers to Meta.

## URL Tracking Behavior in CleverTap

When [click tracking](doc:whatsapp-editor#track-clicks-in-whatsapp-campaigns) is enabled in a campaign, CleverTap does the following:

1. Shortens the destination URL using a tracked link (for example,`https://ct0.co/...`).
2. Logs clicks and redirects users to the original URL
3. Preserves all query parameters, including:

* Meta’s **fbclid**
* Any pre-existing **UTM parameters**

#### Example: Query Parameter Flow

| Step                 | URL                                                              |
| -------------------- | ---------------------------------------------------------------- |
| Original URL         | `https://yourbrand.com/offers?utm_source=whatsapp`               |
| CleverTap Short Link | `https://ct0.co/xyz`                                             |
| Meta Appended Click  | `https://ct0.co/xyz?fbclid=abc123`                               |
| Final Redirect       | `https://yourbrand.com/offers?utm_source=whatsapp&fbclid=abc123` |

> 📘 Note
>
> The `fbclid` parameter is appended by Meta only when the URL is placed in a button within the WhatsApp message. It is not added for plain text links. In some cases, the parameter may not appear due to limitations in Meta’s delivery logic, this is expected behavior and does not indicate an issue with the campaign setup.

# Handling Special Scenarios

The following scenarios explain how MM Lite API onboarding behaves in specific conditions across accounts, numbers, and system-level rollouts:

* **WABA Shared Across Projects**: Onboarding occurs once per WABA and is reflected across all projects.
* **New Numbers Under Onboarded WABA**: These inherit MM Lite access automatically.

# Frequently Asked Questions

This section addresses common questions about MM Lite API eligibility, onboarding, functionality, and feature behavior within CleverTap.

### Do I need to change how I build campaigns or journeys?

No. CleverTap automatically routes messages through MM Lite after onboarding.

### Are support and utility messages affected?

No. MM Lite is used only for marketing messages. All other messages use the Cloud API.

### Where can I check the eligibility of a WABA?

You can check the eligibility of a WABA by navigating to *Settings > Channels > WhatsApp > WhatsApp Direct* and reviewing the *MM Lite Status* column for each number listed.

### Can I disable MM Lite API after enabling it?

No. Onboarding is a permanent action.

### Is fbclid added to all links?

Only if the link is placed in a **button** and the message is sent via MM Lite. Even then, Meta may skip it in rare instances.

### Is TTL control available now?

TTL customization for marketing templates is under development and will be supported soon.
