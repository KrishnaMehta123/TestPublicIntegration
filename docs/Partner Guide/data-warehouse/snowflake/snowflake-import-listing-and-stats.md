---
title: Snowflake Import Listing and Stats
excerpt: Learn how to track and monitor Snowflake imports.
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

After configuring, mapping, and setting the frequency for the import, select **Import** to view the _Import Listing page_. This page shows a list of all imports created for the Snowflake database and can also be accessed from _Settings > Partners > Import Center > Filter by Snowflake._ 

> 📘 Private Beta
> 
> SnowFlake is a private beta release. Contact your Customer Success Manager for access.

The Import Listing page will display the following:

[block:parameters]
{
  "data": {
    "h-0": "**Header**",
    "h-1": "**Description**",
    "0-0": "Nickname",
    "0-1": "The unique name given to each import. This helps easily identify and differentiate between different Snowflake database imports.",
    "1-0": "Partner",
    "1-1": "The partner integration (for example, Snowflake) used for the import.",
    "2-0": "Status",
    "2-1": "The current state of the import <li>Running</li> <li> Scheduled </li><li>Paused </li><li>Draft </li><li>Stopped </li>",
    "3-0": "Import Type",
    "3-1": "Indicates whether the import is for user profile data or event data.",
    "4-0": "Frequency",
    "4-1": "Displays the frequency of the data import (for example, Repeat Intervals, Custom Schedule, or Manually Trigger).",
    "5-0": "Health",
    "5-1": "Indicates the health of the import:  <li>100% (Green): All data has been processed without issues. </li> <li> 50% - 99.99% (Yellow): Some errors in data processing. </li> <li>50% (Red): Less than half of the data processed, check data selection and mapping. </li>",
    "6-0": "Last Run",
    "6-1": "Shows the date and time when the import was last triggered.",
    "7-0": "Created On",
    "7-1": "Displays the date when the import was created.",
    "8-0": "Created By",
    "8-1": "Shows the user who created the import."
  },
  "cols": 2,
  "rows": 9,
  "align": [
    null,
    null
  ]
}
[/block]


The listing page can also be filtered based on the following criteria:

[block:parameters]
{
  "data": {
    "h-0": "**Filter Option**",
    "h-1": "**Description**",
    "0-0": "Partner Name",
    "0-1": "Filter imports by the name of the partner (for example, Snowflake) used for the integration.",
    "1-0": "Sync Type",
    "1-1": "Filter by **Event Data** or **User Profile Data** to view imports of a specific type of data.",
    "2-0": "Status",
    "2-1": "Filter by the status of the import: <li>Running</li> <li> Scheduled </li><li>Paused </li><li>Draft </li><li>Stopped </li>",
    "3-0": "Frequency",
    "3-1": "Filter by the frequency of the import: <li>Repeat Intervals </li><li>Custom Schedule</li><li>Manually Trigger </li>",
    "4-0": "Created On",
    "4-1": "Filter by the instance (Created, Triggered, etc.) and select the date using the calendar widget to display results for a specific timeframe.",
    "5-0": "Created By",
    "5-1": "Filter by the user who created the import by selecting a user from the drop-down. This helps you view imports created by specific users."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    null,
    null
  ]
}
[/block]


Apply these filters by selecting relevant checkboxes to refine the import listings based on your requirements.

# Stats

**Stats** provides a detailed overview of data imports, including their status, success rate, and any errors encountered during the process. These stats help track the health of each import, ensuring data integrity and identifying any failed records that need attention. The stats table includes key metrics such as Total Records, Successful Syncs, Failed Syncs, and the overall health percentage of the import.

To access **Stats**, go to _Settings > Partners > Import Center > Edit selected import > Stats_.

[block:parameters]
{
  "data": {
    "h-0": "**Label**",
    "h-1": "**Description**",
    "0-0": "Date & Time",
    "0-1": "The timestamp when the import process was initiated.",
    "1-0": "Imported On",
    "1-1": "The date when the import was successfully recorded in Snowflake.",
    "2-0": "Health",
    "2-1": "Indicates the health of the import:  <li>100% (Green): All data has been processed without issues. </li> <li> 50% - 99.99% (Yellow): Some errors in data processing. </li> <li>50% (Red): Less than half of the data processed, check data selection and mapping. </li>",
    "3-0": "Total Records",
    "3-1": "The total number of records included in the import.",
    "4-0": "Successful Syncs",
    "4-1": "The number of records that were successfully imported into Snowflake without errors.",
    "5-0": "Failed Syncs",
    "5-1": "The number of records that encountered errors and failed to import during the import process."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    null,
    null
  ]
}
[/block]


To review detailed import records and their processing status, follow these steps to navigate the Stats Table and access specific entry details in the right pane.

On the Stats Table, click on a specific import entry to view its detailed information in the right pane. The right pane will display individual entries from the selected import, including relevant details.  

- For _User Profile Data_, the right pane will show:  
  - **Result**: If the result is _Success_, it indicates that the user profile data has been successfully imported; if _Failed_, it means the user profile data has not been successfully imported.  
  - **CleverTap ID:** Unique identifier for the user profile.  
- For _Event Data_, the right pane will show:  
  - **Result:** If the result is _Success_, it indicates that the event data has been successfully imported; if _Failed_, it means the event data has not been successfully imported.  
  - **Clevertap ID:** Unique identifier associated with the event.  
  - **Event Name:** Name of the event processed in the import.

By following these steps, you can effectively track import performance, identify any errors, and ensure the accuracy and integrity of the imported data within Snowflake.