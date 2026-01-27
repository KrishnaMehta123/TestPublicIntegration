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

After configuring, mapping, and setting the frequency for the import, select **Import** to view the *Import Listing page*. This page shows a list of all imports created for the Snowflake database and can also be accessed from *Settings > Partners > Import Center > Filter by Snowflake.* 

> 📘 Private Beta
>
> SnowFlake is a private beta release. Contact your Customer Success Manager for access.

The Import Listing page will display the following:

<Table>
  <thead>
    <tr>
      <th>
        **Header**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        The unique name given to each import. This helps easily identify and differentiate between different Snowflake database imports.
      </td>
    </tr>

    <tr>
      <td>
        Partner
      </td>

      <td>
        The partner integration (for example, Snowflake) used for the import.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        The current state of the import <li>Running</li> <li> Scheduled </li><li>Paused </li><li>Draft </li><li>Stopped </li>
      </td>
    </tr>

    <tr>
      <td>
        Import Type
      </td>

      <td>
        Indicates whether the import is for user profile data or event data.
      </td>
    </tr>

    <tr>
      <td>
        Frequency
      </td>

      <td>
        Displays the frequency of the data import (for example, Repeat Intervals, Custom Schedule, or Manually Trigger).
      </td>
    </tr>

    <tr>
      <td>
        Health
      </td>

      <td>
        Indicates the health of the import:  <li>100% (Green): All data has been processed without issues. </li> <li> 50% - 99.99% (Yellow): Some errors in data processing. </li> <li>50% (Red): Less than half of the data processed, check data selection and mapping. </li>
      </td>
    </tr>

    <tr>
      <td>
        Last Run
      </td>

      <td>
        Shows the date and time when the import was last triggered.
      </td>
    </tr>

    <tr>
      <td>
        Created On
      </td>

      <td>
        Displays the date when the import was created.
      </td>
    </tr>

    <tr>
      <td>
        Created By
      </td>

      <td>
        Shows the user who created the import.
      </td>
    </tr>
  </tbody>
</Table>

The listing page can also be filtered based on the following criteria:

<Table>
  <thead>
    <tr>
      <th>
        **Filter Option**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Partner Name
      </td>

      <td>
        Filter imports by the name of the partner (for example, Snowflake) used for the integration.
      </td>
    </tr>

    <tr>
      <td>
        Sync Type
      </td>

      <td>
        Filter by **Event Data** or **User Profile Data** to view imports of a specific type of data.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        Filter by the status of the import: <li>Running</li> <li> Scheduled </li><li>Paused </li><li>Draft </li><li>Stopped </li>
      </td>
    </tr>

    <tr>
      <td>
        Frequency
      </td>

      <td>
        Filter by the frequency of the import: <li>Repeat Intervals </li><li>Custom Schedule</li><li>Manually Trigger </li>
      </td>
    </tr>

    <tr>
      <td>
        Created On
      </td>

      <td>
        Filter by the instance (Created, Triggered, etc.) and select the date using the calendar widget to display results for a specific timeframe.
      </td>
    </tr>

    <tr>
      <td>
        Created By
      </td>

      <td>
        Filter by the user who created the import by selecting a user from the drop-down. This helps you view imports created by specific users.
      </td>
    </tr>
  </tbody>
</Table>

Apply these filters by selecting relevant checkboxes to refine the import listings based on your requirements.

# Stats

**Stats** provides a detailed overview of data imports, including their status, success rate, and any errors encountered during the process. These stats help track the health of each import, ensuring data integrity and identifying any failed records that need attention. The stats table includes key metrics such as Total Records, Successful Syncs, Failed Syncs, and the overall health percentage of the import.

To access **Stats**, go to *Settings > Partners > Import Center > Edit selected import > Stats*.

<Table>
  <thead>
    <tr>
      <th>
        **Label**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Date & Time
      </td>

      <td>
        The timestamp when the import process was initiated.
      </td>
    </tr>

    <tr>
      <td>
        Imported On
      </td>

      <td>
        The date when the import was successfully recorded in Snowflake.
      </td>
    </tr>

    <tr>
      <td>
        Health
      </td>

      <td>
        Indicates the health of the import:  <li>100% (Green): All data has been processed without issues. </li> <li> 50% - 99.99% (Yellow): Some errors in data processing. </li> <li>50% (Red): Less than half of the data processed, check data selection and mapping. </li>
      </td>
    </tr>

    <tr>
      <td>
        Total Records
      </td>

      <td>
        The total number of records included in the import.
      </td>
    </tr>

    <tr>
      <td>
        Successful Syncs
      </td>

      <td>
        The number of records that were successfully imported into Snowflake without errors.
      </td>
    </tr>

    <tr>
      <td>
        Failed Syncs
      </td>

      <td>
        The number of records that encountered errors and failed to import during the import process.
      </td>
    </tr>
  </tbody>
</Table>

To review detailed import records and their processing status, follow these steps to navigate the Stats Table and access specific entry details in the right pane.

On the Stats Table, click on a specific import entry to view its detailed information in the right pane. The right pane will display individual entries from the selected import, including relevant details.  

* For *User Profile Data*, the right pane will show:  
  * **Result**: If the result is *Success*, it indicates that the user profile data has been successfully imported; if *Failed*, it means the user profile data has not been successfully imported.  
  * **CleverTap ID:** Unique identifier for the user profile.  
* For *Event Data*, the right pane will show:  
  * **Result:** If the result is *Success*, it indicates that the event data has been successfully imported; if *Failed*, it means the event data has not been successfully imported.  
  * **Clevertap ID:** Unique identifier associated with the event.  
  * **Event Name:** Name of the event processed in the import.

By following these steps, you can effectively track import performance, identify any errors, and ensure the accuracy and integrity of the imported data within Snowflake.
