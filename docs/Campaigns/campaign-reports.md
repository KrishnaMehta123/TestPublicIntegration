---
title: Campaign Reports
excerpt: View Comprehensive reports for your Campaigns.
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

Campaign reports provide you with campaign performance at a glance. Using these reports, you can compare the performance of campaigns and understand engagement trends. You can email or export the summary report of all campaigns sent out for a specific period or even for a particular day. This report includes metrics such as campaign deliveries, engagements, conversions, and errors. To optimize dashboard performance, the data in the report is cached, allowing you to receive data that has been generated up to 4 hours prior. The report may take up to 6 hours, depending on the other activities that are happening when the report is requested.

The following are the two types of campaign reports that you can fetch from the CleverTap dashboard:

* **One-Time Reports**: The report encompasses comprehensive campaign statistics for the chosen campaigns, considering the applied filters.
* **Recurring Reports**: You can set up either *Daily* or *Weekly* recurring reports. When you select *Daily*, the reports encompass statistics for all campaigns from the preceding day, taking into consideration the applied filters. When you select *Weekly*, the reports encompass statistics for all the campaigns from the last seven days, taking into consideration the applied filters. The reports include statistics for a campaign marked as *Completed* as long as data is available for the campaign based on the applied filters.

# Generate Reports

The campaigns list page allows you to view the campaigns. From here, you can email a report or export it to a storage bucket on Amazon S3, Google Cloud Storage, or Azure Blob Storage.

To view a report:

1. Navigate to the *Campaigns* page from the main menu. The Campaign List page opens.
2. Select the campaigns or select the filter criteria to export the reports for the required campaigns.

<Image alt="Generate Campaign Reports" align="center" border={true} src="https://files.readme.io/6caeacd51cb3c43b2e542f0b29f11f43b7e44cd533279050ec9c10b6e75a5da0-image.png" />  Generate Campaign Reports











3. Click **Subscribe to reports**. The Campaign Report window opens on the right side.
4. Configure the following settings:
<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>

        Field

        </p>
      </th>

      <th>
        <p>

        Description

        </p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Report name</p>
      </td>

      <td>
        <p>Enter the name to identify your report uniquely.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Create a report. for</p>
      </td>

      <td>
        <p>Select from the following options for which you want to create a report:</p>
        <ul>
          <li>Selected Campaigns - Generates reports only for the campaigns selected from the list. </li>
          <li>All campaigns with filters applied - Generates report for all the campaigns displayed after applying filters on the campaigns list page.</li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Data to include</p>
      </td>

      <td>
        <p>Select the data from the following options that you want to include in the report:</p>
        <ul>
          <li>Campaign overview</li>
          <li>Campaign stats</li>
          <li>Campaign detailed stats</li>
          <li>Campaign errors</li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Split all data by</p>
      </td>

      <td>
        <p>Select the option to split your data. The following are the available options:</p>
        <ul>
          <li>Day</li>
          <li>OS</li>
          <li>Variant type</li>
        </ul>
        <p><strong>Note:</strong> Split data by day is unavailable if the date range is more than 60 days on the campaigns page.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Frequency</p>
      </td>

      <td>
        <p>Select the export frequency for your report. The following are the available options:</p>
        <ul>
          <li>One-time</li>
          <li>Recurring</li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Delivery Method</p>
      </td>

      <td>
        Select from the following delivery options:
        <ul>
          <li><strong>Email</strong>: You must enter the recipient's email address when you select this option. </li>
          <li><strong>Partner Export</strong>: Select any one from the following export partners and then select the bucket where you want to export the reports:
            <ul>
              <li>Amazon S3 </li>
              <li>Google Cloud Platform</li>
              <li>Azure Blob Storage</li>
            </ul>
          </li>
        </ul>
        <br />The reports are always exported in CSV format.<br />
        For more information, refer to [Report Delivery Method](). 
      </td>
    </tr>
  </tbody>
</Table>
> 📘 **Note**
>
> * You can include *Campaign stats* and *Campaign overview* in the campaign report for a maximum of 2500 campaigns. Also, you can include *Campaign detailed stats* in the campaign report for a maximum of 2000 campaigns.
> * You can also use the [Get Campaign Report API](https://developer.clevertap.com/docs/get-campaign-report-api) to programmatically generate campaign reports.

# Subscribe to Reports

You may want to subscribe to a report in various scenarios. For example, select and subscribe to 4 campaigns on a monthly recurrence, or only subscribe to push campaigns that you created with a label for a monthly/daily recurrence.

The subscriptions are displayed on the *Subscriptions* tab of the *Campaign Report* window. To create a new report or create a new report subscription, refer to [Generate Reports](doc:campaign-reports#generate-reports).

> 📘 **Important**
>
> For Message via Identity campaigns using tag groups, the default download and subscription reports display consolidated statistics, such as Sent, Viewed, and Clicked, for all tag groups in a single row.
>
> To access a detailed breakdown with each tag group displayed in its own row, you can:
>
> * Download the report for the specific Message via Identity campaign, or
> * Create an individual subscription for that campaign.

# Report Delivery Method

If your preferred storage partner is not yet integrated, click the respective partner link in the setup window to complete the configuration.

<Image alt="Configure Partner for Campaign Reports" align="center" width="50%" border={true} src="https://files.readme.io/d1e00ad1f69b8b3413dfe9b0a0b3845d30fc6e50077bae9edc5b580c9beff005-image.png" />  Configure Partner for Campaign Reports

You can refer to the detailed configuration guides for each supported partner:

* [Amazon S3](doc:data-export-to-aws-s3#setup)
* [Google Cloud Storage](doc:data-export-to-gcp#integrate-gcp-with-clevertap)
* [Microsoft Azure Blob Storage](doc:microsoft-azure#setup)

Exported report files follow this naming convention: *\{ReportName}*\{Timestamp}.\{Extension}*, where the Timestamp indicates the time when the report is delivered. For example,\_WeeklyPerformance\_2025-11-04.csv*. You can view your campaign reports by navigating to `<accountID>/reports/` from your partner bucket.
> 🚧 **SAS Token Expiration for Azure Blob Storage**
>
> When configuring Azure Blob Storage as a storage partner, note that the SAS Token expires after a set period. Update the token before it expires to ensure uninterrupted report delivery.

# Edit or Delete Reports

The existing schedule for the reports is displayed on the *Subscribe* tab. To edit or delete a subscription to a report,  

1. Click **Subscribe to Reports** on the campaign list page. The Campaign Summary Emails pane appears.
2. Select the *Subscriptions* tab and click the ![](https://files.readme.io/394983a901844f1518d88ea2bf7a337445f1848952c21fe510ba4315f63a3f68-ellipses_icon.png) icon to edit or delete a report subscription.

<Image title="Edit_subscriptions.gif" alt={570} align="center" border={true} src="https://files.readme.io/95f9da4-Edit_subscriptions.gif" />  Edit or Delete a Report Subscription

# Campaign Report Data

The following table provides all the report columns based on the selected data group. For example, the first column, Campaign ID, will be included in each report, regardless of the data group.\
However, the Campaign Name appears as a column in your report only if you select *Campaign overview* when requesting the report.
<Table align={["left","left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Report Column
      </th>

      <th>
        Campaign Overview
      </th>

      <th>
        Campaign Stats
      </th>

      <th>
        Campaign Detailed Stats
      </th>

      <th>
        Campaign errors
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Campaign ID</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>
        <p>The unique ID for the campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Campaign Name</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The name provided for the campaign during its creation.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Channel</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The channel, such as Email, Mobile Push, and so on, that is used for the campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Delivery</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The campaign delivery, such as Action, Inaction, One-time, and so on.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Type</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The type of campaign, such as single message, message on user property, or A/B test.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Variant</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The message variant. Applicable only to A/B test messages and message on user property.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>OS</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The device operating system, such as iOS and Android.Not applicable to WhatsApp.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Device</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Devices such as mobile, TV, or a Tablet.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>DND / set campaign frequency</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>DND or campaign frequency setting configured at the time of campaign creation.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>timezone</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Configuration for the delivery in the user timezone.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>cutoff</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Configuration of the cutoff period after which the campaign is not delivered.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>fcap (global campaign limits)</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Configuration for the maximum number of messages that a user can receive in a day, taking into account all active devices and across different communication channels.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>throttle</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Configuration for the throttle limits applied to the campaigns.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Safety check limit</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The campaign is not sent to any user if the number of qualified users exceed the limit.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Campaign per day limit</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Number of maximum messages sent per day for the campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Campaign overall limit</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Number of maximum messages sent overall for the campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>estimated reach</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Estimated qualification of users.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reach (Send to all / last active)</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Send to all devices or the last active device. Not applicable to WhatsApp</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>WHO query</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The who query defined in the campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Constant event property</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Shows whether the Constant event property is applicable or not.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Title</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The title of the notification. Values must be added for the WhatsApp header. </p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Message</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Message of the notification. Values must be added for the WhatsApp body.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>iOS Rich Media type</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Media type, such as Single or Carousel for iOS push notifications</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS Rich media URL</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Image URL  for iOS push notifications</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS sound file</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>iOS sound or the file URL if custom.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS Badge Count</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Badge count on IOS notification</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS Category</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Category for iOS push notifications (if applicable).</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS Deep link / External URL</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Deep link for iOS push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>IOS Mutable content</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Shows whether the content is mutable. The values are Yes/No. Not applicable to WhatsApp.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Subtitle</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Subtitle of the Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Image URL</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Image URL for Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Summary</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Summary text for Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android large Icon URL</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Large icon for Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Small App Icon colour</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Small app icon for Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Deep link / External URL</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>Deep link for Android push notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Android Sound File</p>
      </td>

      <td>
        <p>Yes</p>
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        <p>The values are:</p><ul><li>NA </li><li>Default OS sound</li><li>file URL,  if the file is custom</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Android Notification tray priority
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Shows the priority of display in the tray of an Android device
      </td>
    </tr>

    <tr>
      <td>
        Android Notification delivery priority
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Server priority for Android push notifications
      </td>
    </tr>

    <tr>
      <td>
        Collapse notification
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Shows whether the notification is collapsible or not
      </td>
    </tr>

    <tr>
      <td>
        Notification channels
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Communication channel for which user consent has been received.
      </td>
    </tr>

    <tr>
      <td>
        Badge ID
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Badge ID for Android push notifications.
      </td>
    </tr>

    <tr>
      <td>
        Badge Icon
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Badge count Android push notifications.
      </td>
    </tr>

    <tr>
      <td>
        Send to App Inbox as well
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Applicable only for push. Sent to the App Inbox as well or not.  

        * \*Note\*\*: When you select the Send Copy of Push Campaign to App Inbox option, it appears as a single campaign on the *All Campaigns* page on the dashboard. However, you will see two separate entries for the campaign in the campaign reports.
      </td>
    </tr>

    <tr>
      <td>
        Time to live
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Time for the notification to live on the user's device.
      </td>
    </tr>

    <tr>
      <td>
        SMS/ Email/ WA service provider
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The service provider.
      </td>
    </tr>

    <tr>
      <td>
        Start Date
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Start date of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Start Time
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the start time of the campaign. Displays the time value if the campaign is set to Best Time.
      </td>
    </tr>

    <tr>
      <td>
        Conversion Event
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The conversion is tracked for this event in the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Conversion Time (in minutes)
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Time period within which conversion is tracked for the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Campaign URL
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The URL of the campaign to access it on the CleverTap dashboard.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Current status of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Created By
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The creator of the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Created time
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Time of creating the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Labels
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The Labels/tags used to identify and organize campaigns.
      </td>
    </tr>

    <tr>
      <td>
        AmplifiedByInbox
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Shows whether the campaign was amplified by sending it to the Inbox as well.
      </td>
    </tr>

    <tr>
      <td>
        AmplifiedByPush
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        If Enhanced Push Delivery is applied or not.
      </td>
    </tr>

    <tr>
      <td>
        Web Priority
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Priority of web notifications. It can be High, Medium or low.
      </td>
    </tr>

    <tr>
      <td>
        Run Date
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Applicable for Day-wise reports only. Displays the run date.
      </td>
    </tr>

    <tr>
      <td>
        Total Sent (users)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count for the sent users. Shows as N/A for channels that are not supported, such as In-app.
      </td>
    </tr>

    <tr>
      <td>
        Total Viewed (users)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of the users who viewed the notification.
      </td>
    </tr>

    <tr>
      <td>
        Total Clicked (users)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of the users who clicked the notification.
      </td>
    </tr>

    <tr>
      <td>
        Total Sent (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total events. Total number of devices (if 'Send to all' is applied)
      </td>
    </tr>

    <tr>
      <td>
        Total Viewed (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total events. Total number of devices (in case of 'Send to all' is applied)
      </td>
    </tr>

    <tr>
      <td>
        Total Clicked (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total events. Total devices (in case of 'Send to all' is applied)
      </td>
    </tr>

    <tr>
      <td>
        Total HTML Viewed (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of HTML emails viewed.
      </td>
    </tr>

    <tr>
      <td>
        Total AMP Viewed (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of AMP emails viewed.
      </td>
    </tr>

    <tr>
      <td>
        Total HTML Clicked (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of clicks in the fallback HTML version when using the AMP feature.
      </td>
    </tr>

    <tr>
      <td>
        Total AMP Clicked (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the total count of clicks in the AMP version when using the AMP version.
      </td>
    </tr>

    <tr>
      <td>
        Total AMP Unsubscribe (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the count of unsubscribes through the AMP version when using the AMP feature.
      </td>
    </tr>

    <tr>
      <td>
        Total HTML Unsubscribe (events)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Displays the count of unsubscribes through the HTML version when using the AMP feature.
      </td>
    </tr>

    <tr>
      <td>
        Errors
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Errors
      </td>
    </tr>

    <tr>
      <td>
        Click through conversions
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total converting users ( as per funnel, including the clicked step).\
        For WhatsApp campaigns created using external providers, these are total converting users ( as per funnel, excluding the clicked step).
      </td>
    </tr>

    <tr>
      <td>
        Click through conversions %
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total converting users ( as per funnel, including the clicked step)/ Total sent users.\
        For WhatsApp campaigns created using external providers, these are total converting users ( as per funnel, excluding the clicked step)/ Total sent users.
      </td>
    </tr>

    <tr>
      <td>
        Click through conversion revenue
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to Total conversions (as per funnel, including the clicked step).  For external providers, it is Revenue as per the revenue property related to Total conversions (as per funnel, excluding the clicked step).
      </td>
    </tr>

    <tr>
      <td>
        Total control group count
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total number of users in the control group.
      </td>
    </tr>

    <tr>
      <td>
        Total control group conversions
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total number of control group users converting.
      </td>
    </tr>

    <tr>
      <td>
        Total control group conversions %
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total number of control group users converting / Total number of users in the control group.
      </td>
    </tr>

    <tr>
      <td>
        Total control group revenue
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Revenue as per revenue property related to conversion.
      </td>
    </tr>

    <tr>
      <td>
        Total Delivered (users)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total number of unique users who receive Email, SMS, or WhatsApp notifications.  

        * \*Note\*\*: For email campaigns, Delivered is currently released in Private Beta for Infobip (in the case of the Advanced Email add-on) and Sendgrid email providers. Contact your Account Manager for access.
      </td>
    </tr>

    <tr>
      <td>
        Total Delivered (Events)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Total number of Email, WhatsApp, or SMS notifications delivered to the end users.  

        * \*Note\*\*: For email campaigns, Delivered is currently released in Private Beta for Infobip (in the case of the Advanced Email add-on) and Sendgrid email providers. Contact your Account Manager for access.
      </td>
    </tr>

    <tr>
      <td>
        Template Name
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Represents the Template name used in the WhatsApp campaign.
      </td>
    </tr>

    <tr>
      <td>
        Provider Name
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Represents the nickname of the WhatsApp service provider.
      </td>
    </tr>

    <tr>
      <td>
        WABA number
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Represents the source phone number.
      </td>
    </tr>

    <tr>
      <td>
        Unique Sent (users)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Unique users who were sent notifications.  

        * \*Note\*\*: For Email campaigns, this is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        Unique Viewed Within Conversion Time
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Unique users who viewed the notifications within the set conversion time.
      </td>
    </tr>

    <tr>
      <td>
        Unique Clicked Within Conversion Time
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Unique users who clicked the notifications within the set conversion time. Not available for WhatsApp campaigns created using external providers.
      </td>
    </tr>

    <tr>
      <td>
        Unique Converted Within Conversion Time
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Unique users who converted within the set conversion time.
      </td>
    </tr>

    <tr>
      <td>
        Revenue Within Conversion Time
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to conversion.
      </td>
    </tr>

    <tr>
      <td>
        Influenced Conversions
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Numbers populated from the sent > converted funnel.  

        If the Push Impression is enabled for the account, the numbers are populated from the View > Converted funnel.
      </td>
    </tr>

    <tr>
      <td>
        Influenced Conversions %
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Percentage of users converted in sent > converted funnel.  

        If the Push Impression is enabled for the account, it indicates the percentage of users who converted in the View > Converted funnel.
      </td>
    </tr>

    <tr>
      <td>
        Influenced Revenue
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Revenue from users shown as converted in the sent > converted funnel.  

        If the Push Impression is enabled for the account, it indicates the revenue from the user shown as converted in the View > Converted funnel.
      </td>
    </tr>

    <tr>
      <td>
        View through Conversions
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Users who were sent a message and converted. Referred to as influenced conversions on the dashboard.
      </td>
    </tr>

    <tr>
      <td>
        View through Conversions %
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Influenced conversion (above) / Total sent users
      </td>
    </tr>

    <tr>
      <td>
        View through conversions Revenue
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to conversion.
      </td>
    </tr>

    <tr>
      <td>
        System Control Group Conversions
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of system control group users converting.
      </td>
    </tr>

    <tr>
      <td>
        System Control Group Conversions %
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of system control group users who converted / Total number of users in the system control group.
      </td>
    </tr>

    <tr>
      <td>
        System Control Group Revenue
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to conversion.
      </td>
    </tr>

    <tr>
      <td>
        Campaign Control Group Conversions
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of campaign control group users converting
      </td>
    </tr>

    <tr>
      <td>
        Campaign Control Group Conversions %
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of campaign control group users who converted / Total number of users in the campaign control group.
      </td>
    </tr>

    <tr>
      <td>
        Campaign Control Group Revenue
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to conversion
      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Conversions
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of custom control group users who have converted.
      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Conversions %
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of custom control group users who converted / Total number of users in the custom control group.
      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Revenue
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Revenue as per the revenue property related to conversion.
      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Name
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Name of the custom control group.
      </td>
    </tr>

    <tr>
      <td>
        System Control Group Count
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of users in the system control group.
      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group count
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of users in the custom control group.
      </td>
    </tr>

    <tr>
      <td>
        Campaign Control Group count
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Total number of users in the campaign control group.
      </td>
    </tr>

    <tr>
      <td>
        Invalid FCM key
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        App uninstalled(Android)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Wrong FCM API key
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Invalid APNS certificate
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS error
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS Format error
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS Account Temporarily Blacklisted
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        App Uninstalled(iOS)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Invalid Profiles
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Duplicate APNS Token
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Invalid token - FCM
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Unknown error - FCM
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Dispatch error
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Internal error due to amplification
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Global frequency cap exceeded
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Campaign frequency cap exceeded
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Campaign limit reached for day
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Campaign limit reach for run
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Profile not reachable
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Campaign stopped
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        User DND
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Duplicate profile for channel
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS bad topic error
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS disallowed topic
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS bad device token
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS device token and topic mismatch
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS inactive device token for topic
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS wrong environment certificate
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS bad certificate
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS idle timeout
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS missing certificate topic
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        APNS Bad Priority
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        FCM payload too large
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        User not reachable
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        User not qualified
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Notification during campaign DND
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        Campaign cut-off time reached
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Campaign error description.
      </td>
    </tr>

    <tr>
      <td>
        CC Sent
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        The number of emails sent to users in CC. This column is included only when you add CC/BCC recipients to the email campaign. The feature for adding CC/BCC recipients is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        BCC Sent
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        The number of emails sent to users in CC. This column is included only when you add CC/BCC recipients to the email campaign.  

        * \*Note\*\*: CC/BCC feature is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        CC Errors
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        The number of emails failed to be sent to CC users. This column is included only when you add CC/BCC recipients to the email campaign.  

        * \*Note\*\*: CC/BCC feature is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        BCC Errors
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        The number of emails failed to be sent to BCC users. This column is included only when you add CC/BCC recipients to the email campaign. The feature for adding CC/BCC recipients is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Rate (Total)
      </td>

      <td>

      </td>

      <td>
        Yes 
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        The percentage of emails successfully delivered to recipients, calculated as `[(Total Delivered / Total Sent) * 100]`. A high delivery rate indicates a strong sender reputation and effective email deliverability.  

        * \*Note\*\*: For Email campaigns, Delivered is currently available in Private Beta for Infobip (in the case of the Advanced Email add-on) and SendGrid email providers. Contact your Account Manager for access.
      </td>
    </tr>

    <tr>
      <td>
        Delivery Rate (Unique)
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>
        The percentage of emails successfully delivered to unique recipients. Calculated as [(Unique Delivered/Unique Sent) * 100]  

        * \*Note\*\*: For Email campaigns, Delivered is currently available in Private Beta for Infobip (in the case of the Advanced Email add-on) and SendGrid email providers. Contact your Account Manager for access.
      </td>
    </tr>

    <tr>
      <td>
        Open Rate (Unique)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        Average percentage of users who opened the email during the selected time period. Calculated as `[(Unique Viewed/Unique Delivered)* 100]`.  

        * \*Note\*\*: For Email campaigns, Unique stats are currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        CTR (Total)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        The percentage of email views where at least one link was clicked. Calculated as `[(Total Clicked/Total Viewed) * 100]`.  

        * \*Note\*\*: For Email campaigns, this is currently available in Private Beta.
      </td>
    </tr>

    <tr>
      <td>
        CTR (Unique)
      </td>

      <td>

      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>

      </td>

      <td>
        The percentage of unique email views where at least one link was clicked. Calculated as \`[(Unique Clicked/Uique Viewed) * 100]  

        * \*Note\*\*: For Email campaigns, this is currently available in Private Beta.
      </td>
    </tr>
  </tbody>
</Table>


> 📘 **Conversion Tracking Rules**
>
> To understand how CleverTap tracks conversions, it is essential to note the following rules:
>
> * User is considered converted if they complete a conversion event within the conversion timeline.
>
> * User is only counted as converted once for a particular conversion event within a campaign. For example, if a user completes the same conversion event multiple times within the same conversion timeline, it will only be counted once.
>
> * If a user completes a conversion event within the same timeline for multiple campaigns, it is attributed to all the campaigns.
>
> * A user is considered converted even if they do not open or click the message as long as they complete the conversion event within the conversion timeline. This is known as an influenced conversion.