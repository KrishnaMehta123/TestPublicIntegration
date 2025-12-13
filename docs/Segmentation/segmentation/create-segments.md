---
title: Create Segments
excerpt: Learn how to create Segment in CleverTap.
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

Creating segments in CleverTap empowers you to target and engage specific groups of users precisely based on various criteria. This flexibility enables you to design segments based on past behavior and live user interaction with the app. The steps to create Segments vary based on the type of segment you want to create.

# Create Past Behavior Segments

Consider the example of creating an action-based segment where users qualify if they purchased a particular product at least once in the past 30 days.

To create the above example segment, perform the following steps:

1. Navigate to *Segments* > *Segments* from the dashboard.
2. Click **+Segment**.
3. Select the *Past Behavior* segment type.
4. Click **Add a rule group to start building your query**.
5. Select the *Event (Did)* rule from the *User Behavior* option.
6. Select the *Charged* event where the count is one and then click **Refresh Data**.

<Image alt="Create Past Behavior Segment" align="center" border={true} src="https://files.readme.io/002d2c9-Create_Past_Behavior_Segment.gif">
  Create Past Behavior Segment
</Image>

The qualified segment of users for the defined rule is calculated.

<Image alt="View Reachability of Qualified Users" align="center" border={true} src="https://files.readme.io/a842acb-Reachability_Stats.png">
  View Reachability of Qualified Users
</Image>

7. Click **Save Segment**.
8. Enter the *Segment name* and click **Save**.

<Image alt="Save Segment" align="center" border={true} src="https://files.readme.io/1379c79-Save_Past_Behavior_Segment.gif">
  Save Segment
</Image>

Your new segment, *Charged Users* , can now be seen in the main section on the *Segments* page.

To know more about creating more complex rules, refer to the [Segmentation Rules](https://docs.clevertap.com/docs/segmentation-rules).

# Create Live User Segments

Consider the example of creating an *Inaction in Time Frame* segment for which users will qualify in real-time as soon as they add a product to the cart but do not purchase it within 10 minutes.

> 📘 Golden Window for Mobile Transactions
>
> The golden window within which most users transact on our iOS and Android app platforms is within 10 minutes.

To create the above example segment, perform the following steps:

1. Navigate to *Segments* > *Segments* from the dashboard.
2. Click **+ Segment**.
3. Select the *Live - Inaction in Time Frame* segment type.
4. Select the *Added to Cart* event and set the *DOES NOT DO Charged within* as **10** *minutes*.
5. You may select the *Filter on past behavior and common properties* checkbox to apply filters to past actions, inactions, or common user property filters.
6. Click **Save segment**.
7. Enter the *Segment name* and click **Save**.

<Image alt="Create Live - Inaction in Time Frame Segment" align="center" border={true} src="https://files.readme.io/5e2370b-Create_Live_User_Segment.gif">
  Create Live - Inaction in Time Frame Segment
</Image>

Your new segment, *Added to cart but no charge within 10 minutes*, can now be seen in the main section on the *Segments* page.

> 📘 Segment Naming Best Practices
>
> Convey the core meaning of the segment while keeping the name brief.

## Create Live Segments with Multiple Triggers

The Multi-Triggers feature lets you segment users based on one or more events. Consider an example of *Live - User Actions* segments where users qualify as soon as they perform any of the following events:

* App Launched
* UTM Visited
* Notification Clicked

To create a live user segment with multiple triggers:

1. Navigate to *Segments* > *Segments* from the dashboard.
2. Click **+ Segment** and select the *Live - User Actions* segment type.
3. Click **Add Event** and select the events from the list. In this example, select the *App Launched*, *UTM Visited*, and *Notification Clicked* events.
4. Click **Save segment**.
5. Enter the *Segment name* and click **Save**.

<Image alt="Multi-Triggers in Segments" align="center" border={true} src="https://files.readme.io/cb4347e-Multitrigger_in_Segments.gif">
  Create Live Segments with Multiple Triggers
</Image>

> 📘 Note
>
> * You can add a maximum of 10 events for multi-trigger.
> * Multi-Triggers are exclusive to the *Live - User Actions* segment.

# Create Custom - List Based Segments

You can create a custom list segment by uploading user lists via the dashboard or API. 

> 📘 File Size
>
> You can upload a maximum file size of 50 MB from the dashboard. The maximum file size allowed from an API upload is 5GB.

## File Format

Only CSV file format is supported for upload. Also, the list of users for your segment must follow a specific format. You can upload the profiles with identity type as *CleverTap ID* (g) or *GUID* and *identity* (i). 

The format of the CSV file is as follows:

| Type | Identity                                        |
| :--- | :---------------------------------------------- |
| g    | a1e2723cba7c4518bea8ef95b036ac83                |
| i    | [user@clevertap.com](mailto:user@clevertap.com) |

The Type and Identity columns are mandatory for successfully uploading a custom list segment in the above format.  

The **Type** field specifies the type of identity used for each segment user. This can be either `g` for CleverTap ID or GUID for a third-party identifier, and `i` for identity.

The **Identity** field contains the sample value of the identifier for each user, which can be a string or a number, depending on the identifier type. For example, if using the `i` type, the identity field might contain email addresses, phone numbers, or your custom identifier for each user.

> 🚧 User Profiles
>
> A Custom - List Based segment can only contain user profiles that are on the CleverTap dashboard. It does not create any new profiles or update the attributes for the existing user profiles.

## Create from Dashboard

1. Navigate to *Segments* > *Segments*. 
2. Click **+ Segment**. 
3. Click **Custom - List Based**. 

<Image title="Click Select to Create a Custom List Segment" alt={2836} align="center" border={true} src="https://files.readme.io/30191c1-Custom_-_List_Based_Segment.png">
  Custom - List Based Segments
</Image>

The **Create Segments** page is displayed. 

4. Enter the *Segment name*.
5. Click **Browse** and select the CSV file to be uploaded.

<Image title="Click Browse to Upload a CSV File" alt={1714} align="center" border={true} src="https://files.readme.io/b04d46e-Create_New.png">
  Upload CSV File
</Image>

> 📘 Sample custom list CSV
>
> It is recommended to download the Sample custom list CSV file and format your custom list information as per the downloaded sample file.

6. Click **Save Segment**.

You will receive an email with the details after the file is processed. 

<Image title="An Email is Sent After the File is Processed" alt={1109} align="center" border={true} src="https://files.readme.io/0cd90b7-View_Segment_Details.png">
  View Segment Details - Email
</Image>

The uploaded segment is now available for use. 

## Create from API

You can create a custom list segment from API. For detailed steps, refer to [Custom list API](https://developer.clevertap.com/docs/custom-list-endpoints).

## Replace via Dashboard

You can replace a custom list segment from the dashboard. However, if the segment is currently in use for engagement through a Campaign or Journey, then you must stop the Campaign or Journey before replacing the segment. 

To replace a segment:

1. Click the ellipsis ![](https://files.readme.io/b15093f-ellipses_icon.png) icon from the segment you want to replace.
2. Click **Replace**.

<Image title="Click the Ellipsis of the Segment you Want to Remove and Click Replace" alt={1222} align="center" border={true} src="https://files.readme.io/7550fa3-Replace_Custom_List.png">
  Replace a Segment
</Image>

2. Click the Re-upload user list and select the CSV file.  
3. Upload the CSV file.
4. Name the file and save it. Wait for it to be processed. 
5. You will receive an email with the details after the file is processed. 

The uploaded segment is now available for use. 

## Troubleshoot Upload

### File size exceeds 50 MB

This error occurs when the file size exceeds 50 MB. 

<Image title="The File Size Exceeds 50 MB Occurs" alt={1552} align="center" border={true} src="https://files.readme.io/ad225fc-File_size_exceeds.png">
  File Size Exeeds 50 MB - Error
</Image>

> 📘 Note
>
> If the file size is more than 50 MB, it can be uploaded via [Custom list API](https://developer.clevertap.com/docs/custom-list-endpoints).

### Error uploading the file

You can see the following message when trying to upload the file.

<Image title="An Email is Sent if the Error Occurs" alt={1107} align="center" border={true} src="https://files.readme.io/e6fcff0-File_Upload_Error.png">
  File Upload Error - Email
</Image>

If the file is not uploaded correctly, you can upload it again. 

| Segment issue         | Resolution                                                                                                                                                                                                                            |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| File upload failed    | The segment could not be created from the uploaded file. Fix the errors and re-upload the file.                                                                                                                                       |
| File re-upload failed | The segment could not be refreshed with the latest file. The segment will be available with the last successful update. Refer to the [View Segment Details](doc:create-segments#view-segment-details) page for the last updated file. |

> 📘 Segment processing
>
> The custom list segment is available for use only after the process of creating or updating is complete.

## View Segment Details

The segment details can be viewed from the Segment dashboard. The segment details page shows all the available information for the segment, such as:

* *Segment Trend*: If the users have increased or decreased over time. 
* *Campaigns and Journeys*: The number of campaigns and Journeys currently using the custom list segment. 
* *Segment size and reachability*: The total number of users in the segment and their reachability across various engagement channels. 
* *Sample Users*: These are samples from your list. You can open any of them to check their details. 

> 📘 Tip
>
> Click the ![](https://files.readme.io/8967517-Download_Segment_Icon.png) download icon to download all the users in your segment.

<Image title="Click to Hide/Show the Segment or Download the Segment CSV File" alt={1193} align="center" border={true} src="https://files.readme.io/81840d5-Segments_Custom_lists_report.png">
  Hide/Show Segment or Download as CSV
</Image>

# Use Custom List Segment

When creating a campaign, you can use the custom list segment from the *Who* section. All the custom list segments are listed under the WHO section of the *Campaigns* page. 

<Image title="Use the Custom List Segment from the Who Section of Campaign" alt={2744} align="center" border={true} src="https://files.readme.io/1742312-Target_Custom_List_Segment.png">
  Use Custom List Segment in Campaign Creation
</Image>
