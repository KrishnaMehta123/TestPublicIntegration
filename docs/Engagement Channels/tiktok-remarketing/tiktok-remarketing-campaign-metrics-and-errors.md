---
title: TikTok Remarketing Campaign Metrics and Errors
excerpt: Overview of TikTok Remarketing Campaign Metrics and Errors in CleverTap
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

This document provides a detailed overview of the key metrics available for TikTok remarketing campaigns within CleverTap. It outlines how to view and interpret these metrics and provides additional features for analyzing campaign performance.

# Key Metrics

After the campaign is live, you can view the campaign stats from the dashboard by navigating to the *Campaigns* page and selecting the campaign of interest to view the following stats: Unique Sent, Audience Size (old), Audience Size (Current), Conversions. 

**Sent**

* **Definition**: Indicates the number of sent audience from CleverTap to TikTok.
* **Purpose**: This tool helps gauge the reach of your ads by showing the total number of individual users targeted.

**Audience Size (Old)**

* **Definition**: Reflects the size of the remarketing audience at the start of the campaign.
* **Purpose**: Provides a baseline for comparison to see how the audience size has evolved since the campaign began.

**Audience Size (Current)**

* **Definition**: The "Audience Size (Current)" metric reflects the current size of your remarketing audience on TikTok. This number can fluctuate over time based on various factors, such as user engagement and the impact of different campaigns. The size may change if the same audience is updated through a different CleverTap campaign.
* **Purpose**: Understanding the size of your remarketing audience is crucial for several reasons: 
  * It allows you to gauge the effectiveness of your campaigns.
  * It helps you optimize targeting strategies for better results.
  * It enhances overall engagement with your target audience.

**Scenarios Affecting Audience Size**

* **Audience Not Found**: This indicates that the TikTok audience linked to your campaign no longer exists. This typically happens when a TikTok account manager deletes the audience from the account. If you encounter this issue, you must check with your account manager for potential solutions or alternatives.
* **Couldn't Fetch Audience Size**: When you open the campaign stats page, we attempt to fetch the audience size directly from TikTok. Occasionally, TikTok’s Audience Size fetch APIs may fail to return a response. This can result in the audience size not being displayed in TikTok Audience Export Campaigns. If this occurs, refresh the page or check back later, as it may be a temporary issue.
* **Audience Size Showing Up as 0**: There are two primary reasons why the audience size may display as 0: 
  * **Audience Uploaded to TikTok Hasn’t Been Matched Yet**: After uploading an audience, it can take 24-48 hours for the audience size to update on the Audiences page in TikTok’s Ads Manager. If you’ve just uploaded a new audience, patience may be necessary before the size reflects accurately.
  * **Matched User Count is Less Than 1000**: Due to data privacy policies, TikTok will show the audience size as 0 if the matched user count falls below 1000. This is to ensure user anonymity and data protection.

**Conversions**

* **Definition**: Represents the number of users who completed a desired action due to interacting with your remarketing ads.
* **Purpose**: Measures the effectiveness of your campaign in driving user actions such as purchases or sign-ups.

## Additional Metrics

1. **Message Trend**
   * **Definition**: Click on **Message Trend** to view trends based on Sent, Viewed, or Clicked metrics. You can analyze these trends on a daily, weekly, or monthly basis.
   * **Purpose**: Helps track the performance of your messages over time and identify patterns or anomalies.

2. **Conversion Performance**
   * **Definition**: Shows the conversion boost achieved from your campaign by comparing target group conversions with control group conversions. This helps assess the impact of the campaign on driving conversions.
   * **Purpose**: Provides insights into how effectively the campaign drove conversions compared to a baseline, allowing for a clear understanding of its effectiveness.

3. **Revenue Performance**

   * **Definition**: Displays the revenue boost achieved from your campaign by comparing the revenue generated from the target group with that from the control group. This measure reflects the campaign's financial impact.

   * **Purpose**: Helps assess the return on investment (ROI) of the campaign by evaluating the incremental revenue attributed to the campaign efforts compared to the baseline.\
     **Definitions**

   * **Target Group Conversions**: The number of conversions (e.g., purchases, sign-ups) generated from the audience exposed to the campaign. This metric indicates the effectiveness of the campaign in achieving its goals among the targeted demographic.

   * **Control Group Conversions**: The number of conversions achieved by a comparable group that was not exposed to the campaign. This serves as a baseline to measure the campaign's effectiveness and isolate its impact on conversions.

4. **Users Conversion Funnel**
   * **Definition**: Visualizes the conversion funnel through the stages: Sent > Converted.
   * **Purpose**: Helps identify where users drop off in the funnel, allowing for optimization of each stage to improve overall conversion rates.

Understanding these metrics and features allows you to evaluate the effectiveness of your TikTok remarketing campaigns and make informed decisions to optimize future efforts. For any further assistance, please refer to CleverTap support or the platform’s help resources.

## TikTok Integration Errors

The following errors can occur when integrating with TikTok, affecting your ability to create campaigns, manage connections, and ensure data accuracy.

| Errors                                                     | Description                                                                                                                                                                            |
| :--------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TikTok Audience Export Restricted                          | TikTok integration is unavailable in the region where your CleverTap project is hosted; contact support for further assistance.                                                        |
| TikTok Internal Error                                      | An internal error occurred while fetching the advertiser ID from TikTok. Ensure the TikTok advertiser account used in the campaign is active. If the issue persists, contact support.  |
| TikTok Advertising Account Connection Expired              | The connection to your TikTok Advertising account has expired. Reconnect to resume creating TikTok campaigns.                                                                          |
| Invalid TikTok Advertising Account Connection              | The connection to your TikTok Advertising account is not valid. Reconnect to resume creating TikTok campaigns.                                                                         |
| Invalid Campaign Parameters                                | The TikTok API request contains invalid parameters. Verify the campaign settings and try again.                                                                                        |
| Required Permission Missing with TikTok Account Connection | The connection to your TikTok Advertising account is missing mandatory permissions. Reconnect your TikTok account and approve all permissions to proceed.                              |
| Missing Required Fields in TikTok Campaign                 | Your TikTok campaign request is missing the necessary fields. Ensure all required information is included and try again.                                                               |
| TikTok Campaign Parameter Mismatch                         | An error occurred due to invalid parameters in your TikTok campaign setup. Review your campaign and try again.                                                                         |
| Incorrect Data Format in Exported User Profile             | Data exported from user profiles has incorrect formats. To export data successfully to TikTok, check and update the exported properties in the user profiles.                          |
| Audience Not Found in TikTok                               | The audience specified for the data upload does not exist in TikTok.Check your TikTok account to verify if the audience still exists or create a new campaign and audience to proceed. |
