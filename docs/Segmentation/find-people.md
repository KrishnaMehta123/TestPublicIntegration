---
title: Find People
excerpt: >-
  Understand how to find users and their segments using Find People feature in
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

One of the key features of CleverTap is its ability to filter and search for specific user profiles based on different parameters, including user ID.

# Find People

You can find users from the dashboard in two ways:

1. [Find Users by Identity](doc:find-people#find-users-by-identity)
2. [Find Users by Segmentation](doc:find-people#find-users-by-segmentation)

## Find Users by Identity

Find and target specific users with precision using the powerful Find Users by Identity feature in the CleverTap Dashboard.

To do so:

1. Navigate to _Segments_ > _Find People_ on the CleverTap dashboard.
2. Under _By identity_, enter the _Email_, _Identity_, or _CleverTap ID_ of the user you want to find and click **Find**.

<Image align="center" border={true} src="https://files.readme.io/5924323-Find_Users_by_Identity.png" className="border" />

The _User Profile_ appears.

<Image align="center" border={true} src="https://files.readme.io/ca4f53c-small-User_Profile_Find_People.png" className="border" />

> 📘 Search Users by Identity
>
> You can find a specific user using the following identities:
>
> * Email
> * Phone Number
> * Identity
> * CleverTap ID
>
> These identities can be configured in the _Settings > User Identity_ page on the CleverTap dashboard during the initial onboarding.

## Find Users by Segmentation

The Find People view in CleverTap allows you to create precise user segments, enabling you to tailor your marketing efforts and engage with specific user groups effectively. It lets you segment your users by actions taken, actions not taken, or user profile properties that match a set of criteria you have defined.

For example, suppose you have an e-learning app, and you want to identify users who have made a purchase in the past 30 days and have not completed any in-app tutorials. In the CleverTap dashboard, you can set up a segment using the Find People view by defining the following criteria:

1. Users who did _Charged_ in the last 30 days.
2. And did not do _Tutorial Completed_.

<Image align="center" alt="Find People" border={true} caption="Find People" src="https://files.readme.io/ceca1f6-Find_People_by_Segmentation.png" />

Once you set these criteria, CleverTap will generate a segment of users who meet these conditions. You can then use this segment for targeted messaging or personalized campaigns to encourage users to complete the in-app tutorials or offer them exclusive promotions to enhance their shopping experience.

You can view detailed engagement statistics, demographic, device, and location information for those users. You can view more details of individual user profiles and activity data. You can also run targeted Push, In-app, Email, and Web campaigns for these user segments from the _Find People_ view.

<Image align="center" alt="Save Segment" border={true} caption="Save Segment" src="https://files.readme.io/d590ce5-small-Save_Segment_Find_People.png" />

### Download Users

The _Find People_ section allows you to download the users in CSV format from any segment that you have created.

To download the users in CSV format:

1. Add the required criteria to filter out the segment for which you may want to download the users and click **View Details**.
2. Click the **Download** icon under the _Reachability_  section.

<Image align="center" border={true} src="https://files.readme.io/b87f458-small-Download_Icon.png" className="border" />

3. Select the required fields and click **Proceed**.

<Image align="center" border={true} src="https://files.readme.io/4cab592-small-Include_the_Required_Fields_and_Click_Proceed.png" className="border" />

> 📘 Mismatch in Segment Size and Number of Users Exported to CSV File
>
> The number of users displayed under the _Segment size and reachability_ section may vary from the number of users exported to the CSV file. This variation is due to the inclusion of blacklisted users under the _Segment size and reachability_ section.

# View User Details

You can view the following user details from a User Profile:

## Profile Details

The _Profile_ tab displays information about individual users, such as their name, email address, phone number, location, device details, and so on. These details are used to create a 360-degree view of the user, which helps marketers to personalize their communication and engagement strategies.

<Image align="center" alt="View Profile Details" border={true} caption="View Profile Details" src="https://files.readme.io/84c2e27-small-Profile_Find_People.png" />

## Activity Details

The _Activity_ tab shows the actions that users have performed within the app or website. This includes events such as app launches, page views, clicks, purchases, and so on. These details are useful in understanding user behavior and preferences, which can help marketers to create targeted and relevant campaigns.

<Image align="center" alt="View Activity Details" border={true} caption="View Activity Details" src="https://files.readme.io/0b0a537-small-Activity_Find_People.png" />

## Engagement Details

The _Engagement_ tab displays the Journeys with which the users interacted on the app or website. CleverTap tracks the engagement data to provide insights into how users respond to various campaigns and messages. By analyzing this data, marketers can optimize their engagement strategies and increase user retention.

<Image align="center" alt="View Engagement Details" border={true} caption="View Engagement Details" src="https://files.readme.io/e56e713-small-Engagement_Find_People.png" />
