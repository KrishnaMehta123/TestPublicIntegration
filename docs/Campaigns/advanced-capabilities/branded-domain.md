---
title: Branded Domain
excerpt: >-
  Learn how to configure system and custom domains to generate branded tracking
  links to boost engagement.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Branded Domains in CleverTap help you apply your brand to tracking across Email, SMS, WhatsApp, and RCS campaigns.

* For **SMS**, **WhatsApp**, and **RCS campaigns**, it is used to generate short, trackable links.
* For **Email campaigns**, it is used to brand links and open-tracking pixels using a custom domain.

Using branded domains improves user trust and can boost engagement rates.

<Callout icon="📘" theme="info">
  #### Private Beta

  This feature is currently released in Private Beta. If you want to access the feature, contact your Customer Success Manager.
</Callout>

# Domain Types

CleverTap supports two types of branded domains:

| Domain        | Description                                                                                                                                                                                                                         | Supported Channels         |
| :------------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------- |
| System Domain | Provided by CleverTap, where you can customize the system-generated short links with your brand's prefix for easy integration without the need for DNS configuration.                                                               | WhatsApp, SMS & RCS        |
| Custom Domain | Enables you to use your own subdomain for complete control over your branding and tracking. To use a custom domain, you will need to configure DNS records with your domain provider for proper verification and campaign tracking. | Email, WhatsApp, SMS & RCS |

Both options allow you to define specific settings, such as the URL structure and 404 error page, ensuring your branded domain is set up to suit your needs.

# Add Domain

This section provides information about creating a branded system and a custom domain for your campaigns. To add a domain, perform the following steps:

1. Go to _Settings_ > _Set Up_ > _Branded Domain_.
2. Click **Add Domain** and select the channel.
3. Enter the details you are prompted to provide based on the selected channel. For more information, refer to [System Domain](doc:branded-domain#add-system-domain) and [Custom Domain](doc:branded-domain#add-custom-domain).

<Image align="center" border={true} caption="Add Domain" src="https://files.readme.io/e3b88c267d2ff3601ff7e683443c73d9339f2eabce70810a1a9ad7c3522277ed-Add_Domain.png" />

3. Click **Save**.
   * For a System Domain, the status is set to Active immediately.
   * For a Custom Domain, the status is set to Pending Verification, and DNS records are generated for you to configure with your domain provider.

## Add System Domain

You can create a system domain to quickly start using branded links in your WhatsApp/SMS & RCS campaigns without DNS configuration. To add a system domain, enter the following details:

<Image align="center" border={true} caption="Add System Domain for WhatsApp/SMS & RCS" src="https://files.readme.io/e3ebb61fb60d716b8bf202001ecf73288241023274516357412e960838056f86-Add_System_Domian_for_WASMS__RCS.png" />

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
        Nickname
      </td>

      <td>
        Provide a name to identify the domain (for example, "Marketing").
      </td>
    </tr>

    <tr>
      <td>
        Channel
      </td>

      <td>
        Displays the channel for which the branded domain is being created.
      </td>
    </tr>

    <tr>
      <td>
        Domain Type
      </td>

      <td>
        A CleverTap-provided system domain that can be customized with your brand prefix. No DNS setup required. This is available only for WhatsApp/SMS & RCS channels.
      </td>
    </tr>

    <tr>
      <td>
        Domain
      </td>

      <td>
        The base domain used for branding and tracking. When adding a system domain, this is auto-filled based on your account region. For more information, refer to _Domain and Account Region Mapping for WhatsApp/SMS & RCS_ below the table.
      </td>
    </tr>

    <tr>
      <td>
        Branded URL Schema
      </td>

      <td>
        Defines the structure of the branded tracking URL. This is available for WhatsApp/SMS & RCS channels and is required for adding a system domain.

        URL Structure: `domain/adjoiner/Shortkey`

        This includes the following:

        * **Domain**: The domain entered above is prepopulated here.
        * **Adjoiner**: A brand-specific path separator that connects the Domain and Shortkey, helping personalize and group URLs. The **Adjoiner** can only contain lowercase letters, numbers, and hyphens. It must not start or end with a hyphen, and cannot contain special characters such as `@`, `#`, `&`, and so on.
        * **Shortkey**: A unique, auto-generated code added to the branded domain, helping track clicks on links within campaigns.

        For example, `ct3.io/clevertap/abc123`
      </td>
    </tr>

    <tr>
      <td>
        Error Page
      </td>

      <td>
        The page users see if a tracking link is invalid or has expired. You can use CleverTap’s system error page or provide a custom URL to maintain brand consistency even in error scenarios. Click _Preview Error Page_ to view and verify the error before the domain becomes active.
      </td>
    </tr>
  </tbody>
</Table>

Once you enter all the details, click **Save**. The status is set to **Active** immediately

<Callout icon="📘" theme="info">
  #### Domain and Account Region Mapping for WhatsApp/SMS & RCS

  | Dashboard URL                | Region      | System Domain | Example URL   |
  | :--------------------------- | :---------- | :------------ | :------------ |
  | eu1.dashboard.clevertap.com  | EU          | ct1.io        | ct1.io/25AlJz |
  | in1.dashboard.clevertap.com  | IN          | ct3.io        | ct3.io/52KlAz |
  | sg1.dashboard.clevertap.com  | SG          | ct4.io        | ct4.io/25ZlAz |
  | us1.dashboard.clevertap.com  | US          | ct5.io        | ct5.io/52ZlKa |
  | mec1.dashboard.clevertap.com | Middle East | ct8.io        | ct8.io/25ZaJz |
  | aps3.dashboard.clevertap.com | Indonesia   | ct9.io        | ct9.io/52KJz  |
</Callout>

## Add Custom Domain

Use your own subdomain (for example, `sales.yourbrand.com`) for maximum brand visibility. This option allows you to fully control the branding and tracking for your campaigns.

<Image align="center" border={true} caption="Add Custom Domain for Email" src="https://files.readme.io/8d921a0e9d530293aae02e8a11a57cb149a0cbec5a2e240c0d66704ff999bbb6-Add_Email_Custom_Domain.png" />

<Image align="center" border={true} caption="Add Custom Domain for WhatsApp/SMS & RCS" src="https://files.readme.io/f45e4906647bd7da1393c6e5433801296310555e301bf619b8e8d22e1825d782-Add_Custom_Domain_for_WASMS__RCS.png" />

| Field              | Description                                                                                                                                                                                                                                                                                                                                                             |
| :----------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nickname           | Provide a name to identify the domain (for example, "Marketing").                                                                                                                                                                                                                                                                                                       |
| Channel            | The channel this branded domain will be used for.                                                                                                                                                                                                                                                                                                                       |
| Domain Type        | Your own subdomain (for example, links.yourbrand.com) that requires DNS configuration.                                                                                                                                                                                                                                                                                  |
| Domain             | Enter your own subdomain to be used for branding and tracking                                                                                                                                                                                                                                                                                                           |
| Branded URL Schema | This is available for WhatsApp/SMS & RCS channels and is required for adding a custom domain. It defines the structure of the branded tracking URL.                                                                                                                                                                                                                     |
| Error Page         | Optional field. Available only for WhatsApp/SMS & RCS channels. Provide the page you want users to see if a tracking link is invalid or has expired. You can use CleverTap’s system error page or provide a custom URL to maintain brand consistency even in error scenarios. Click _Preview Error Page_ to view and verify the error before the domain becomes active. |

Once you enter all the details, click **Save & Generate DNS**. The domain status is set to **Pending Verification** immediately, and DNS Records are generated to configure it on your Domain provider dashboard. The generated records include two CNAME records and one TXT record

<Image align="center" border={true} caption="DNS Records Generated for Email" src="https://files.readme.io/6d90a8eaa27f1d56aae290b66bf962fcd1b1ee164bddfe3bc0779a7a310d4f48-image.png" />

<Image align="center" border={true} caption="DNS Records Generated for WhatsApp/SMS & RCS" src="https://files.readme.io/36972d396aadc92d070754a236802c008846a6a5f96c0b64a8b08268fc9eb8b3-DNS_Verification_for_WASMS__RCS.png" />

<Callout icon="📘" theme="info">
  #### Custom Domain

  You can add up to 5 unique custom domains per account per channel.
</Callout>

### Verify Custom Domain

After DNS records are generated, verify them so the domain becomes active and available for use. To do so, perform the following steps:

1. Go to the domain provider dashboard and configure the following DNS records. When configuring DNS records with your domain provider, enter only the prefix part in the Name field. The prefix is the part that precedes the main domain. For example, if the CNAME is `_c58ebcb5c******5f03bb6b174349.track.yourdomain.com`, enter `_c58ebcb5c******5f03bb6b174349.track` in the Name field.

| Type  | Description                                                                                                                                          |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| CNAME | Used for domain ownership verification.                                                                                                              |
| CNAME | Redirects branded links to CleverTap's short URL service for WhatsApp/SMS & RCS campaigns. For Email campaigns, it supports click and open tracking. |
| TXT   | Verifies domain association with CleverTap.                                                                                                          |

2. Once your DNS records are saved, go back to the **Branded Domain** page on the CleverTap dashboard.
3. Click the ![](https://files.readme.io/36be013543cabc562d762f02fd1eebc007f2caad03f95519a37dfff4f6e4c7ed-Refresh_icon.png) icon next to your domain to verify your domain and refresh the status on the CleverTap dashboard. DNS verification may take up to 24 hours to complete. If verification fails, check your DNS configuration with your domain provider to ensure it is accurate. If the settings are correct, try refreshing after some time.

# Best Practices for Adding Domain in CleverTap

Here are some tips to ensure your branded domain setup is effective and compliant:

* **For System Domains** (like `ct3.io/yourbrand/abc123`):
  * Choose a short and meaningful **Adjoiner** that clearly represents your brand or campaign type.
  * Use lowercase letters and hyphens (`-`) if needed (for example, `/clevertap/`, `/new-user/`, `/sale2024/`).
  * Keep it concise: Aim for 5–8 characters in the **Adjoiner** (excluding the slashes) to avoid long URLs in campaigns.
  * Avoid vague terms like `/track/` or `/link/` — use something unique to your brand.
* **For Custom Domains** (like `links.yourbrand.com`):
  * Use a subdomain such as **links.**, **click.**, or **promo.** (for example,`links.yourbrand.com`, `click.yourbrand.com`).
  * Keep the **Subdomain** short, relevant, and easy to remember.
  * Avoid complex words, long phrases, or special characters in the **Subdomain** name.
  * Ensure you configure **DNS records** exactly as shown after setup to avoid delays in verification.
* Avoid the following:
  * Using more than 20 characters in the **Adjoiner** or **Subdomain**.
  * Starting or ending **Adjoiners** with hyphens.
  * Using non-brand-specific generic terms.

<Callout icon="📘" theme="info">
  #### Pro Tip: Buy New Short Domain for Campaigns

  If your existing domain is long or complex, consider purchasing a new, short domain for marketing messages. Ideally, the domain must be 5–8 characters long and phonetically similar to your brand name. This improves:

  * Link trustworthiness
  * User recall and voice-based sharing (for example, over phone or radio)
  * Visual clarity in messages and notifications

  **Examples**:

  * If your brand name is long (for example, **ExampleStore**), consider short domain options like **exstr.in**, **exsto.co**, or **exst.co**.
  * For multi-word brand names (for example, **Example Food Market**), you could use shortened versions such as **exfdmr.com**, **efmkt.in**, or **xfmk.co**.
</Callout>

# Manage Branded Domains

The Domain Listing page allows you to view and manage all your configured domains. You can easily edit domain settings, view DNS records, and make any necessary updates to check if your domains are correctly set up and functioning.

Go to _Settings_ > _Set Up_ > _Branded Domains_. You can see a list of all your domains (system or custom), including the following details:

<Image align="center" border={true} caption="Branded Domains Page" src="https://files.readme.io/2fbb49c4e3a18c0744338f8f2db30ae4f28a3babf5c0f3eb1289f175dc099f41-Branded_Domain_Listing_Page.png" />

| Column            | Description                                                                                                                                                                                                                                                                                                                       |
| :---------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _Nickname_        | A user-defined name to help you identify the domain (for example, "Sales Campaign").                                                                                                                                                                                                                                              |
| _Domain URL_      | Displays the full URL of the branded domain being used for tracking links in the case of WhatsApp/SMS & RCS campaigns (for example, `ct3.io/clevertap/abc123`). Displays the branded domain being used for email campaigns (for example,  `track.yourdomain.com`).                                                                |
| _Created By_      | The email address of the user who created the domain.                                                                                                                                                                                                                                                                             |
| _Status_          | The current status of the domain. It can be: <ul><li>**Active**: Domain is verified and ready to be used in campaigns.</li><li>**Pending Verification**: Domain is awaiting DNS verification and cannot be used until verified.</li><li>**Failed**: Domain verification failed due to incorrect or missing DNS records.</li></ul> |
| _Last Updated On_ | The timestamp when the domain settings were last updated.                                                                                                                                                                                                                                                                         |

After adding the domain, you can perform the following operations by hovering it:

<Image align="center" border={true} caption="Manage Branded Domains" src="https://files.readme.io/a4ad7fef6b3c58d079a57876f5c3d45be43447b1298499d715bdf28d0e2dbafd-Manage_Branded_Domains.gif" />

* **Set as Default**: You can set one verified domain as the default for WhatsApp, SMS, and RCS, and a different verified domain as the default for Email. This domain is automatically used for wrapping and tracking links in SMS, WhatsApp, RCS, and Email campaigns (including template buttons). You can override it per campaign when creating new ones.

* **Edit**:  You can edit the nickname of the domain. Additionally, for WhatsApp/SMS & RCS campaigns, you can set a custom 404 error page (except for system defaults).

* **Verify Domain**: You can manually verify the domain by checking the status. If the verification fails, you can click the ![](https://files.readme.io/af7a9009c220dbcfb129f0528f3669b976d0d7f0de86557dca6e52c1444d6aed-Refresh_icon.png) icon next to the domain to retry after making the necessary corrections.

* **View DNS Records**: You can access and review the DNS settings associated with your domain. This includes details such as CNAME and TXT records, which are essential for domain verification and proper tracking. By viewing these records, you can ensure that the domain is correctly configured with your DNS provider for seamless integration and functionality.

# FAQs

### Can I switch between path-based and query-based adjoiners?

No, you must choose one format per domain — either **path-based** (`/yourbrand/`) or **query-based** (`?key=yourbrand`). You cannot mix both formats in a single domain configuration.

### What happens if my custom domain becomes unverified?

If a branded domain used for Email moves from Active to Pending Verification or Failed:

* CleverTap sends an email alert to inform you of the status change
* CleverTap automatically falls back to the system domain for email click and open tracking
* Email campaigns continue to send without interruption

Once the domain is verified again, it can be reused in future campaigns.

### Will old campaigns use the new branded domain?

No. Campaigns created before you set up a branded domain will continue using the **System Domain** unless you manually edit or recreate them with the new branded domain.

### I configured the DNS records, but my domain has still not been verified. What should I do?

Check the following:

* **DNS records** are entered exactly as shown in the CleverTap dashboard.
* You’ve entered only the required prefix in the **Key** field (for example, short, not short.clevertap.com)
* Wait up to 24 hours, then try refreshing again

### When will a link preview be shown for my branded domain link?

A link preview is generated when the messaging platform (such as SMS, WhatsApp, or RCS) scans the URL included in your message and detects the required Open Graph metadata on the destination page. The following tags must be present and properly configured in the page’s HTML:

* `<meta property="og:title" content="...">`
* `<meta property="og:description" content="...">`
* `<meta property="og:image" content="...">`

If these tags are available and valid, the platform may display a visual preview containing a title, description, and image. A preview may not be shown in the following cases:

* The Open Graph tags are missing or incorrectly implemented
* The domain is blocked by `robots.txt` or firewalls
* The page is inaccessible to external crawlers

To validate whether your Open Graph metadata is implemented correctly, use any metadata testing tool or Open Graph debugger.

### How do link previews work on iOS devices, and why might they not appear?

iOS devices running version 10 or above support link previews in the native Messages application. These previews may still appear for SMS-based messages, but several conditions must be met for reliable rendering.

**Preview Requirements**

* Only one link should be included in the message. Messages with multiple links will not generate a preview.
* The link must be the final element in the message. No text, punctuation, or symbols should follow the link.
* The domain must be served over HTTPS and use a valid SSL certificate. Self-signed, expired, or incomplete certificates will block preview generation.
* The recipient must tap _Tap to Load Preview_ for metadata to be fetched.

**iOS-specific Behaviors and Limitations**

* iOS delays metadata fetching until after the message is delivered, and in some cases, until the user interacts with the message.
* Devices may display cached metadata even after updates have been made to the page’s Open Graph tags.
* Certain third-party messaging apps may block previews by default, unless they are explicitly enabled in the settings.

These constraints can lead to inconsistent preview rendering on iOS devices, even when metadata is correctly configured.
