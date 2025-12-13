---
title: Domain Whitelisting for Web SDK
excerpt: Learn how to configure domain whitelisting on the CleverTap dashboard.
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

Domain Whitelisting is a security feature by CleverTap that ensures only approved domains can send data to your CleverTap account. This helps prevent unauthorized data ingestion, protects against data pollution, and safeguards campaign execution.

> 🚧 SDK Compatibility
> 
> Domain Whitelisting for Web is compatible with SDK version 1.17.0 and above. To check your Web SDK version, use the `clevertap.getSDKVersion` method.

By default, the Web SDK accepts events from all domains. When domain whitelisting is enabled, CleverTap checks the source of each Web SDK request. If the domain matches one of the entries in your allowlist, the data is accepted; otherwise, it is rejected. When the feature is disabled (the default setting), data is accepted from all domains without restriction.

> 📘 Note
> 
> - You can add up to 20 domains per account.
> - Only admins can make changes to domain whitelisting. This permission cannot be assigned to custom roles.

# Set Up Domain Whitelisting

To set up Domain Whitelisting:

1. Click **Settings**, then go to _Security > Domain Whitelisting_.
2. Click **Whitelist Domain**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90f87a74bc28dbc20ae1268c38b8f148f5ea66ac917c6438d909a5d89b9f8871-Domain_Whitelisting_New.png",
        "",
        "Domain Whitelisting"
      ],
      "align": "center",
      "border": true,
      "caption": "Domain Whitelisting"
    }
  ]
}
[/block]


3. Enter a domain name and a name for identification.
4. Click **Whitelist** to add the domain to your allowlist.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b27bd56432747994603ea3d2655939ce18f9369947c8c129f93a85382c8d2e8-Whitelist_Popup.png",
        "",
        "Enter Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Details"
    }
  ]
}
[/block]


5. Use the toggle switch in the dashboard to enable or disable domain whitelisting. 

> 📘 Note
> 
> - Whitelisting only takes effect after at least one domain is added and the toggle is switched on.
> - When domain whitelisting is enabled or disabled, an email is sent to the account admin to notify the change.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d8993351541eaa3f07113005bb7f0c62a9a3c6f85791fc39c593720826a7a148-Domain_Whitelisting_new_image.png",
        "",
        "Enable Whitelist"
      ],
      "align": "center",
      "border": true,
      "caption": "Enable Whitelist"
    }
  ]
}
[/block]


7. You can edit and delete domains from the list at any time.

# Domain Name Guidelines

Adhere to the following domain name guidelines when adding domains to your allowlist. The following are valid domain name formats:

- `www.example.com`
- `example.com` 

The following are invalid domain name formats and can not be saved:

- `https://example.com` or `example.com/path` - Do not include protocols `(https://)` or paths. Use only the root domain, such as `example.com`.
- Duplicate or conflicting domains are not allowed. For example,  `www.example.com` and `example.com`.