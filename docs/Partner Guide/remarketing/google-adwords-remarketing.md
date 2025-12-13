---
title: Google Ads Remarketing
excerpt: Remarketing
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

If you integrate your Google Ads and CleverTap accounts, you will be able to segment your users in CleverTap, and automatically upload those users to Audience lists in your Google Ads account. 

This integration will enable you to easily run remarketing campaigns where you show ads to specific segments of your users across Google Search Network, YouTube, and Gmail.

# Step 1: Get Your Ads Customer ID

1. Log in to your [Google Ads account](https://adwords.google.com/home/).
2. Navigate to the settings section and copy the Customer ID listed under the Account Information of the Settings section of the Google Ads dashboard. For more information about finding your Ads Customer ID, refer to [Google Support](https://support.google.com/adwords/express/answer/6083253).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29fc1a6-image2.png",
        "Copy Customer IF from Google Ads account",
        215
      ],
      "align": "center",
      "border": true,
      "caption": "Copy Customer ID from Google Ads Account"
    }
  ]
}
[/block]

# Step 2: Connect Google Ads Account

The process involves adding Google Ads Customer ID to the CleverTap dashboard. To do so: 

1. Log in to the [CleverTap Dashboard](https://dashboard.clevertap.com/). 
2. Navigate to _Settings_ > _Channels_ > _Remarketing_.
3. Enter the _Google ads account ID_, and then click **Connect**.
4. (Optional) Enter your Manager account ID for a linked [Manager Account](https://ads.google.com/intl/en_in/home/tools/manager-accounts/).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b74ffb0-google_ads_manager_id.png",
        "Enter required details to integrate Google Ads account",
        1600
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate Google Ads Account"
    }
  ]
}
[/block]

> 📘 Admin User
> 
> The user with Admin rights on the Google Ads Platform can integrate Google Ads and CleverTap accounts.

5. Click **Continue** when prompted by Google to give access to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/944d50f-google_ads_allow_r.png",
        "Click Continue to give access to CleverTap",
        400
      ],
      "align": "center",
      "border": true,
      "caption": "Click Continue to Give Access to CleverTap"
    }
  ]
}
[/block]

> 🚧 Verify Credentials
> 
> If you have multiple CleverTap accounts, check that you are using the correct account. Similarly, if you have multiple Ads accounts, verify it is the correct account.

# Step 3: Create a New Campaign for Ads Remarketing

When you create a new campaign in CleverTap, you can select Google Ads as the channel of communication.

Navigate to the _Campaigns_ page, click on **+ Campaign**, and then select Google Ads.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5eb84f0-6d4ced6-campaign1.png",
        "Navigate to Campaigns page and click + Campaign",
        1042
      ],
      "align": "center",
      "border": true,
      "caption": "Click + Campaign to Create a Campaign"
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6141265-Campaigns_Channels.png",
        "Select Google Ads from Messaging List",
        1375
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Select Google Ads from Messaging List"
    }
  ]
}
[/block]

After you select the segment of users you want to target, you can either add the selected segment to an existing Audience list from your Google Ads account or you can create a new one.  

Once you create this campaign in CleverTap, Google will update the audience list within 48 hours. You can then add these audience lists to your ad groups in Ads and start serving them ads. 

# Additional Notes about Google Ads Remarketing

- Since it takes up to 48 hours for an Audience list to be populated with members, you will most likely see an "In Progress" status within the Google Ads UI when you update an audience list.
- Email addresses must be associated with a Google account.
- Only @gmail.com addresses can be used for targeting in Gmail.
- For privacy purposes, the user list size will show as zero until the list has at least 1,000 members. After that, the size will be rounded to the two most significant digits.
- Google matches the email/phone according to the process [mentioned here](https://support.google.com/adwords/answer/7474263). This means the number of people uploaded may be less than the number of people actually shown on your Google Ads account.

# Google Ads Help Center Links

- [Customer Match](https://support.google.com/adwordspolicy/answer/6299717)
- [Customer Matching Process](https://support.google.com/adwords/answer/7474263)
- [Fix Customer Match Issues with List Upload](https://support.google.com/adwords/answer/7474166)