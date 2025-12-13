---
title: Facebook Audience Network
excerpt: Remarketing
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: Create Campaign with Facebook Audience
---
# Overview

The benefit of integrating your Facebook Ads account with CleverTap is getting per-campaign, per-user cost data and the average revenue for users acquired via that campaign. This helps you understand the cost of a campaign versus the revenue earned with it.

To integrate your Facebook Ads account, perform the following steps:

# Step 1: Get Your Facebook Ads Account ID

- Log in to your [Facebook Ads account](https://www.facebook.com/ads/manage/home/).
- Navigate to _Settings_, and copy the _Account ID_ visible under _Account Information_.

# Step 2: CleverTap Dashboard Steps

- Log into your CleverTap Dashboard, and navigate to _Settings_ > _Channel_ > _Remarketing_. 

> 📘 Users with Multiple CleverTap Accounts
> 
> If you have multiple CleverTap accounts, make sure that you are using the correct one.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3849a5b-2d330c4-Facebook_remarketing_integration.png",
        "Set up Facebook Audience",
        1151
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Facebook Audience"
    }
  ]
}
[/block]

- Paste the _Account ID_ you copied in Step #1, and click **Connect**.
- Click **Okay** when prompted by Facebook to give access to CleverTap.

Once the connection is successful, the "Account connected successfully” message displays. The initial campaign data will display in two hours and is subsequently updated every two hours.

# Additional Notes

Ensure your Facebook Ad campaign links are tagged with the parameters below for them to show up in the _Campaign_ dashboard:

- wzrk_source=facebook
- wzrk_campaign=\<campaign_name>