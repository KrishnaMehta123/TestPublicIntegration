---
title: Track Domain Reputation
excerpt: >-
  Learn how to monitor, track, and analyze your Email Domain Reputation directly
  in CleverTap with Google Postmaster integration.
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

The Email Domain Reputation feature lets you monitor and manage your domain reputation directly within the CleverTap dashboard. By integrating with Google Postmaster, you can view domain reputation scores without leaving the platform.

This integration helps you with the following:

* Detect and resolve issues faster.
* Improve email deliverability performance.
* Reduce dependency on multiple external tools.

> 📘 Private Beta
>
> Tracking Domain Reputation is released in Private Beta. If you want access to this feature, contact your Customer Success Manager.

# Prerequisites

Before enabling the Domain Reputation Tracking feature, ensure that:

* You have a Google Postmaster account.
* You grant *Read* access to your domains for CleverTap’s Postmaster Email ID.
* You have the appropriate role and permissions (access to campaign creation or email settings).

# Setup

To start monitoring your domain reputation in CleverTap, you need to perform the following two steps:

1. [Connect Google Postmaster with CleverTap Dashboard](doc:track-domain-reputation#connect-google-postmaster-with-clevertap-dashboard).
2. [Enable Domain Reputation Tracking on CleverTap dashboard](doc:track-domain-reputation#enable-domain-reputation-tracking-on-clevertap-dashboard).

## Connect Google Postmaster with CleverTap Dashboard

Assign *Read* permission to [service-postmaster@clevertap.com](mailto:service-postmaster@clevertap.com) so CleverTap can access the reputation data. Before doing this, you must add your domain to the Google Postmaster account. For more information, refer to [Set Up Postmaster Tools](https://support.google.com/a/answer/9981691?visit_id=638943148006465876-3162460208\&rd=2).

<Image alt="Add Email Domain to Google Postmaster" align="center" border={true} src="https://files.readme.io/a425e2e5d22f1bcdb29b672868d3165ddf5de71c841967ac2d80a47621b08436-Add_Domain_to_Google_Postmaster.png">
  Add Email Domain to Google Postmaster
</Image>

To grant Read access to CleverTap's Postmaster Email ID, perform the following step:

1. Go to Postmaster Tools, click the ![](https://files.readme.io/30051320648e0a9863c8ff3183a593878b3dfb21178d2266a84af3a018da1a5c-ellipses_icon.png)  icon for your added domain, and select *Manager Users* from the list.

<Image alt="Manage User from Domain List" align="center" border={true} src="https://files.readme.io/5a752135564ce709c3c72c5e0576b3e3c054019c3eb87430884f0eece868b548-Manage_Users_from_Domain_List_.png">
  Manage User from Domain List
</Image>

2. From the *Manage Domains* page, to the right of the domain name, click *More* > *Manage* in the bottom right, and click the ![](https://files.readme.io/8e2784208185fa7afb0ef020302d029abde537d284ef92bbdb4919e0d237af4e-Plus_Icon.png) icon.
3. In the window, enter the Google email address [service-postmaster@clevertap.com](mailto:service-postmaster@clevertap.com) to grant *Read* access for the domain.

   <Image alt="Assign Read Permission to CleverTap Service Account Email Address " align="center" border={true} src="https://files.readme.io/2ac0b38dfe8514e966cc0ead6f4a2ad69dce4e719709393055e69cc3e29fb38c-Assign_Read_Permission.png">
     Assign Read Permission to CleverTap Service Account Email Address 
   </Image>

## Enable Domain Reputation Tracking on CleverTap Dashboard

Once you connect your Google Postmaster to CleverTap, you need to enable Domain Reputation Tracking from the CleverTap dashboard, as follows:

1. From the CleverTap dashboard, go to *Settings* > *Channels* > *Email* and select the *Advanced Setup* tab.
2. Toggle on the *Domain Reputation Tracking* option. 

<Image alt="Enable Domain Reputation Tracking" align="center" border={true} src="https://files.readme.io/f8b94ae197b8e697408c0d32c6d11d584e748b226bc3c5e401e494d39fe67a4f-Enable_Domain_Reputation_Tracking_on_CleverTap.png">
  Enable Domain Reputation Tracking
</Image>

 Once enabled, your Google Postmaster tool is connected to the CleverTap dashboard.

# View Domain Reputation

Once you complete all the steps, you can view domain reputation scores from the following three pages on the CleverTap dashboard:

* ### From Provider List Page

  You can view the domain reputation score under the Provider Setup page of the Email channel. Reputation scores (Bad, Low, Medium, High) are displayed next to the configured email domains. 

  The reputation score displays as *Not Available* if you have not granted CleverTap *Read* access in Google Postmaster. Update your Postmaster settings to allow Read access for CleverTap to fetch the data.

<Image alt="Email Domain Reputation from Provider Setup Page " align="center" border={true} src="https://files.readme.io/cdf820d394e4544c8707cce0472058321cbe7d857baf7b7f97ad31d7336c495f-Email_Domain_Reputation_from_Provider_Setup_Page.png">
  Email Domain Reputation from Provider Setup Page 
</Image>

* ### When Adding New Provider

  When adding a new provider, hover on the ![](https://files.readme.io/7b50a83e1dc6ab1b658a880bf71bf0ea8397037a047e35da7b287caa4530a96a-Domain_Reputation.png) icon against the *From Address* to view the Email Domain Reputation.

  <Image alt="Email Domain Reputation When Adding New Provider" align="center" width="75% " border={true} src="https://files.readme.io/b02ee0a15c3fb9bfc3fe5de0ba99e76c2d6f4bfc60ccf9efbd74411af6244472-Email_Domain_Reputation_When_Adding_New_Provider.png">
    Email Domain Reputation When Adding New Provider
  </Image>
* ### From Campaign List Page

  You can view the Email Domain Reputation from the Campaign List page when you filter the campaign by Email channel. The reputation score shown in the campaign listing reflects the domain reputation when the campaign was published. This allows you to correlate campaign performance with domain reputation during that period.

  <Image alt="Email Domain Reputation from Campaign List Page" align="center" border={true} src="https://files.readme.io/55d11cb0e5c275607701b451a5b2f3de788e7ff5b611ef3a162bf9b3bf8b1d62-Email_Domain_Reputation_from_Campaign_List_Page_.gif">
    Email Domain Reputation from Campaign List Page
  </Image>
* ### From Campaign Creation page

  You can also view the Email Domain Reputation under the Email Service Provider section when creating a campaign.

  <Image alt="Email Domain Reputation from Campaign Creation Page" align="center" border={true} src="https://files.readme.io/a4225010f1c7e12fec416cde2c476b851347809f79566e05f4db2ea1ae65efe6-Email_Domain_Reputation_When_Creating_Campaign.png">
    Email Domain Reputation from Campaign Creation Page
  </Image>

  If the selected provider’s reputation is low, CleverTap displays a warning about potential email delivery issues. Selecting a provider with a higher reputation improves your campaign performance.

  <Image alt="Low Domain Reputation Warning" align="center" border={true} src="https://files.readme.io/8b48ec907d237ff297207f71aac19e5efa6a243642eb07e0e0fafcc99e205e73-Low_Domain_Reputation_Warning.png">
    Low Domain Reputation Warning
  </Image>

# View Email Domain Reputation Trend

You can track your domain reputation trends over time in the CleverTap dashboard. These insights help you spot patterns, measure campaign impact, and act quickly if your reputation declines.

To view the Email Domain Reputation Trend, perform the following steps:

1. Go to *Settings* > *Channels* > *Email* and select the *Providers* tab.
2. Click the ![](https://files.readme.io/4c1db785e3d7a7b7f03fec3d0e65baf97eb1253661d6def8d444adfa47741230-Trend_icon.png) icon for any provider. The Reputation trend opens for the domain as shown below:

<Image alt="View Email Domain Reputation Trend " align="center" border={true} src="https://files.readme.io/93069560b2bf3783a7576d015601bf8ae8a1d1e9c764d22aa17a88425a3c6b66-View_Domain_Reputation_Trend.gif">
  View Email Domain Reputation Trend 
</Image>
