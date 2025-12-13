---
title: Branded Domain
excerpt: Learn how to leverage Branded Domains to create engaging customer experiences.
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

Branded Domains in CleverTap help you track clicks from SMS, WhatsApp, and RCS messages using a domain that reflects your brand. You can either customize a CleverTap-provided system domain with your brand prefix or configure your own custom subdomain. This improves user trust and can boost engagement rates.

## Manage Domains on CleverTap

CleverTap helps you add and manage branded domains for your campaigns. You can either use a system domain provided by CleverTap that is customizable with your brand prefix, or a custom domain, which allows you to configure your own subdomain for complete branding control. Once your domain is added, you can manage various settings, including selecting a default domain, customizing a 404 error page, and verifying the domain’s status.

1. **Add Domain**: This option allows you to either create a system domain provided by CleverTap or configure a custom domain for your brand. The system domain can be customized with your brand prefix, while the custom domain lets you use your own subdomain for complete brand visibility.
   * **System Domain**: A domain provided by CleverTap (such as `ct3.io`), which can be customized with a brand prefix without the need for DNS configuration.
   * **Custom Domain**: A fully custom subdomain (such as`links.yourbrand.com`) that you configure via your DNS provider to have complete control over the branding and tracking.
2. **Domain Listing and Operations**: Once your domain is set up, you can manage it by editing settings such as choosing a default domain, setting a custom 404 error page, or verifying the domain status.

## Add Domain

This section provides information about creating a branded domain for your campaigns. You can choose between two types of domains: 

**System Domain:** Provided by CleverTap, where you can customize the system generated short links with your brand's prefix for easy integration without the need for DNS configuration.

**Custom Domain:** Enables you to use your own subdomain for complete control over your branding and tracking. To use a custom domain, you will need to configure DNS records with your domain provider for proper verification and campaign tracking.

Both options allow you to define specific settings, such as the URL structure and 404 error page, ensuring your branded domain is set up to suit your needs. 

To create new System and Custom domains, follow the steps below:

## Add a System Domain

You can create a system domain to quickly start using branded links without DNS configuration. Follow these steps:

<Image alt="System Domain Creation" align="center" border={true} src="https://files.readme.io/9bc74aeb0814633f881aa3b1ddaadca049e395bb61df7f9f55379bad0c76a63c-image.png">
  System Domain Creation
</Image>

1. Go to *Settings > Set Up > Branded Domain*.

2. Click **+ Domain**, and select **System Domain**.

3. **Add a Nickname**: Provide a name to identify the domain (for example, "Sales Campaign").

4. The domain is auto-filled based on your account region. Below is the list of account regions and system domains mapping.

   | Dashboard URL                | System Domain | Region      | Example URL   |
   | :--------------------------- | :------------ | :---------- | :------------ |
   | eu1.dashboard.clevertap.com  | ct1.io        | EU          | ct1.io/25AlJz |
   | in1.dashboard.clevertap.com  | ct3.io        | IN          | ct3.io/52KlAz |
   | sg1.dashboard.clevertap.com  | ct4.io        | SG          | ct4.io/25ZlAz |
   | us1.dashboard.clevertap.com  | ct5.io        | US          | ct5.io/52ZlKa |
   | mec1.dashboard.clevertap.com | ct8.io        | Middle East | ct8.io/25ZaJz |
   | aps3.dashboard.clevertap.com | ct9.io        | Indonesia   | ct9.io/52KJz  |

5. Enter the **Adjoiner**: The adjoiner is a brand-specific path segment that connects the domain and short key, helping personalize your URLs. (for example, `/yourbrand`, `/clevertap/`).  

* **URL structure** : `domain/adjoiner/shortKey`
* **Example**: `ct3.io/clevertap/abc123`
* **Valid Adjoiner Rules:**
  * Must start and end with a slash (`/`). For example, `/yourbrand/`, `/promo2024/`.
  * Between the slashes you can add the string. The string must:
    * Begin with a lowercase alphabetic character (a–z).
    * End with an alphanumeric character (a–z or 0–9).
    * Cannot include special characters such as `@`, `_`, `&`, and so on.
    * Must be unique per domain.

6. Review the **URL Preview** to ensure that it appears as expected.
7. Choose your **404 Error Page**:\
   The 404 error page configuration allows you to customize the page displayed when a link is expired or no longer valid. This ensures that even in error scenarios, your brand's consistency is maintained, offering a user-friendly experience.
   * **System**: CleverTap  provider [system error page](https://ct.io).
   * **Custom URL**: Provide your own error page URL.
8. **Click Save**. The domain status will be set to **Active** immediately.

## Add a Custom Domain

Use your own subdomain (for example, `sales.yourbrand.com`) for maximum brand visibility. This option allows you to fully control the branding and tracking for your campaigns.

<Image alt="Custom Domain Creation" align="center" border={true} src="https://files.readme.io/a96ff7313f6c1a553f982b0ce5f798cccb8d3e04a1eb43b0b076a40443785aa4-image.png">
  Custom Domain Creation
</Image>

To configure your custom domain, follow these steps:

1. Go to *Settings > Set Up > Branded Domain*.
2. Click **+ Domain**, and select **Custom Domain**.
3. **Add a Nickname**: Provide a name to identify the domain (for example, "Sales Campaign").
4. Enter your preferred **Domain** (for example, links.yourbrand.com)
5. Enter the **Adjoiner**: The adjoiner is a brand-specific path segment (for example, `/yourbrand`).
   * **URL structure** : `yourdomain/adjoiner/shortKey`
   * **Example**: `track.zipfood.com/clevertap/abc123`
   * **Valid Adjoiner Rules:**
     * Must start and end with a slash (`/`), for example, `/yourbrand/`, `/promo2024/`
     * Between the slashes, the string must:
       * Begin with a lowercase alphabetic character (a–z).
       * End with an alphanumeric character (a–z or 0–9).
       * Cannot include special characters like `@`, `_`, `&`, etc.
       * Must be unique per domain.
6. Review the **URL Preview** to ensure that it appears as expected.
7. Choose your **404 Error Page**:\
   The 404 error page configuration allows you to customize the page displayed when a link is expired or no longer valid. This ensures that even in error scenarios, your brand's consistency is maintained, offering a user-friendly experience.
   * **System**: CleverTap  provider [system error page](https://ct.io).
   * **Custom URL**: Provide your own error page URL.
8. **Click Save**.The domain status will be set to **Pending Verification** immediately and DNS Records will be generated for you to configure with your Domain provider.

> 📘 Note
>
> You can add up to 5 unique custom domains per account.

### DNS Records

<Image alt="DNS Records" align="center" border={true} src="https://files.readme.io/46e37a4daf231fd72e9edb0de202487d8579cb3600d4e441d7f50147576882ad-image.png">
  DNS Records
</Image>

After saving a custom domain, CleverTap will generate three DNS records that must be configured with your domain provider (for example, GoDaddy, Hostinger, etc.).

#### Example DNS Records

You must configure the following DNS records: 

| Type  | Key (Name)                                                      | Value                                                                        | Description                                               |
| ----- | --------------------------------------------------------------- | ---------------------------------------------------------------------------- | :-------------------------------------------------------- |
| CNAME | \_c58ebcb5&#x63;**\*\***&#x35;f03bb6b174349.short.clevertap.com | \_0f8561a2d&#x63;**\*\*\***&#x39;ef25e32f6.xl\*\*\*\*vlj.acm-validations.aws | Used for domain ownership verification.                   |
| CNAME | short.clevertap.com                                             | short-clevertap-com.cltap.com                                                | Redirects branded links to CleverTap's short URL service. |
| TXT   | \_txt-&#x36;**-R**-R47Z.short.clevertap.com                     | ct0.co=2c1f96426804                                                          | Verifies domain association with CleverTap.               |

#### While Configuring DNS:

When configuring the DNS records with your domain provider, check the following:

* **Enter only the prefix part** in the **Name** field. Prefix is the portion before the main domain starts. Following are the examples for adding a Name: 
  * Example: For `_c58ebcb5c******5f03bb6b174349.short.clevertap.com`, enter `_c58ebcb5c******5f03bb6b174349.short`.
  * Example: For `short.clevertap.com`, enter `short`.
  * Example: For `_txt-6**-R**-R47Z.short.clevertap.com`, enter `_txt-6**-R**-R47Z.short`.

#### Verifying Custom Domain

Once your DNS records are saved:

1. Go back to the **Branded Domain** page on the CleverTap domain name.
2. Click the **Refresh** icon next to your domain.

DNS propagation may take up to 24 hours. If verification fails, check your DNS configuration with your domain provider. If the settings are correct, try refreshing after some time.

# Domain Listing

The Domain Listing section allows you to view and manage all your configured domains. You can easily edit domain settings, view DNS records, and make any necessary updates to check if your domains are properly set up and functioning.

Go to *Settings > Set Up > Branded Domain*. You’ll see a list of all your domains (system or custom), including the following details:

| Field             | Description                                                                                        |
| ----------------- | -------------------------------------------------------------------------------------------------- |
| *Domain Nickname* | A user-defined name for identifying the domain (for example, "Sales Campaign").                    |
| *Domain URL*      | The full URL of the domain being used for tracking links (for example, `ct3.io/clevertap/abc123`). |
| *Created By*      | The user who created the domain.                                                                   |
| *Status*          | The current status of the domain  can be **Active** or **Pending Verification**.                   |
| *Last Updated On* | The date when the domain settings were last updated.                                               |

## Key Domain Operations

Once you’ve added a domain, you can perform various operations on it:

* **Set Default Domain**: You can set any verified domain as the default. This domain will automatically be used for wrapping and tracking links in SMS, WhatsApp, and RCS campaigns (including template buttons). You can override it per campaign while creating new ones. 

* **Edit Domains**: For each domain (except system defaults), you can set a custom 404 error page. This page is displayed if users click on expired links (older than 7 days).

* **Verify Domain**: You can manually verify the domain by checking the status. If the verification fails, you can click the refresh icon next to the domain to retry.

* **View DNS Records:** You can  access and review the DNS settings associated with your domain. This includes details such as CNAME and TXT records, which are essential for domain verification and proper tracking. By viewing these records, you can ensure that the domain is correctly configured with your DNS provider for seamless integration and functionality.

## FAQs

1. **What is a branded domain, and why should I set it up?**\
   A branded domain is a custom or customized URL that tracks clicks from your SMS, WhatsApp, or RCS campaigns. It helps build brand trust, improves click-through rates, and complies with regulations like **DLT whitelisting** (especially in India).

2. **What’s the difference between a system domain and a custom domain?**  

* **System Domain**: Provided by CleverTap (for example, `ct3.io`) and ready to use. You can customize the path (`/brand/`) or query parameter (`?key=brand`) to brand it.  
* **Custom Domain**: Your own subdomain (for example, `links.yourbrand.com`) that you configure via your domain provider with DNS settings.

3. **What is an Adjoiner, and why is it needed?**\
   An **Adjoiner** is the part of the URL that appears between the domain and the short key. It adds brand identity and structure to the tracking URL. The adjoiner is required to create a valid branded domain URL.\
   Example:  

* **Path-based**: `ct3.io/yourbrand/abc123`  
* **Query-based**: `ct3.io?key=yourbrand&sk=abc123`

4. **Can I use special characters in the adjoiner?**\
   No. The **Adjoiner** can only contain lowercase letters, numbers, and hyphens. It must not start or end with a hyphen, and cannot contain special characters like `@`, `#`, `&`, and so on.

5. **Can I switch between path-based and query-based adjoiners?**\
   No, you must choose one format per domain — either **path-based** (`/yourbrand/`) or **query-based** (`?key=yourbrand`). You cannot mix both formats in a single domain configuration.

6. **What happens if a user clicks an expired link?**\
   If a link is older than 7 days, it expires. You can configure a **404 Error Page URL** for each domain, which will be shown to users who click on expired links. 

7. **What is the default domain and how does it work?**\
   The **Default Domain** is automatically used to wrap and track links in **SMS**, **RCS**, and **WhatsApp** campaigns (including template buttons). You can override the **Default Domain** per campaign by selecting a different domain from the dropdown when creating new campaigns.

8. **Will old campaigns use the new branded domain?**\
   No. Campaigns created before you set up a branded domain will continue using the **System Domain** unless you manually edit or recreate them with the new branded domain.

9. **How long does domain verification take?**\
   Custom domains require **DNS record configuration**. While CleverTap fetches DNS updates automatically, it may take up to **24 hours** for DNS changes to propagate globally. You can click the **refresh** icon to retry verification.

10. **I configured the DNS records, but my domain has still not been verified. What should I do?**\
    Check the following:  

* **DNS records** are entered exactly as shown in the CleverTap dashboard. 
* You’ve entered only the required prefix in the **Key** field (for example, short, not short.clevertap.com)  
* Wait up to 24 hours, then try refreshing again

11. **What are the best practices for adding a branded domain in CleverTap?**

Here are some tips to ensure your branded domain setup is effective and compliant:  

* **For System Domains** (like `ct3.io/yourbrand/abc123`):  
  * Choose a short and meaningful **Adjoiner** that clearly represents your brand or campaign type.  
  * Use lowercase letters and hyphens (`-`) if needed (for example, `/clevertap/`, `/new-user/`, `/sale2024/`).  
  * Keep it concise: Aim for 5–8 characters in the **Adjoiner** (excluding the slashes) to avoid long URLs in **SMS** or **WhatsApp** messages.  
  * Avoid vague terms like `/track/` or `/link/` — use something unique to your brand.  
* **For Custom Domains** (like `links.yourbrand.com`):  
  * Use a subdomain such as **links.**, **click.**, or **promo.** (for example,`links.yourbrand.com`, `click.yourbrand.com`).  
  * Keep the **Subdomain** short, relevant, and easy to remember.  
  * Avoid complex words, long phrases, or special characters in the **Subdomain** name.  
  * Ensure you configure **DNS records** exactly as shown after setup to avoid delays in verification.

**Avoid**:  

* Using more than 20 characters in the **Adjoiner** or **Subdomain**  
* Starting or ending **Adjoiners** with hyphens  
* Using non-brand-specific generic terms  

> 📘 Pro Tip: Buy a new short domain for campaigns
>
> If your existing domain is long or complex, consider purchasing a new, short domain for marketing messages. Ideally, the domain must be 5–8 characters long and phonetically similar to your brand name. This improves:  
>
> * Link trustworthiness  
> * User recall and voice-based sharing (for example, over phone or radio)  
> * Visual clarity in messages and notifications  
>
> **Examples**:  
>
> * If your brand is **MobiKart**, consider domains like **mobkt.in**, **mobik.in**, or **mkrt.co**.  
> * If your brand is **FreshBite**, try **frsbt.com**, **frbite.in**, etc.

11. When will a link preview be shown for my branded domain link?

A link preview is generated when the messaging platform (such as SMS, WhatsApp, or RCS) scans the URL included in your message and detects the required Open Graph metadata on the destination page. The following tags must be present and properly configured in the page’s HTML:

* `<meta property="og:title" content="...">`
* `<meta property="og:description" content="...">`
* `<meta property="og:image" content="...">`

If these tags are available and valid, the platform may display a visual preview containing a title, description, and image. A preview may not be shown in the following cases:

* The Open Graph tags are missing or incorrectly implemented
* The domain is blocked by `robots.txt` or firewalls
* The page is inaccessible to external crawlers

To validate whether your Open Graph metadata is implemented correctly, use any metadata testing tool or Open Graph debugger.

12. How do link previews work on iOS devices, and why might they not appear?

iOS devices running version 10 or above support link previews in the native Messages application. These previews may still appear for SMS-based messages, but several conditions must be met for reliable rendering.

**Preview requirements**

* Only one link should be included in the message. Messages with multiple links will not generate a preview.
* The link must be the final element in the message. No text, punctuation, or symbols should follow the link.
* The domain must be served over HTTPS and use a valid SSL certificate. Self-signed, expired, or incomplete certificates will block preview generation.
* The recipient must tap *Tap to Load Preview* for metadata to be fetched.

**iOS-specific behaviors and limitations**

* iOS delays metadata fetching until after the message is delivered, and in some cases, until the user interacts with the message.
* Devices may display cached metadata even after updates have been made to the page’s Open Graph tags.
* Certain third-party messaging apps may block previews by default unless explicitly enabled in settings.

These constraints can lead to inconsistent preview rendering on iOS devices even when metadata is correctly configured.
