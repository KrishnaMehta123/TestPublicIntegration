---
title: Census
excerpt: Customer Data Platform
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

[Census](https://www.getcensus.com/) is a Reverse ETL platform that makes it easy to connect your data warehouse to sales, marketing, and other customer-facing tools that drive your business.

With CleverTap and Census integration, you can:

- Import user data from Census into CleverTap to create personalized campaigns.
- Import customer events into CleverTap to keep them updated with data from the Census.
- Enhance customer experiences by integrating data from other interactions, such as website visits or app usage.

This powerful combination boosts customer engagement and drives impactful marketing and business results.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by Census. The CleverTap and Census integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Census](mailto:support@getcensus.com) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

- Ensure you have a Census account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Census with CleverTap

This process involves the following two major steps:

1. [Add CleverTap as a Destination on Census](doc:census#add-clevertap-as-a-destination-on-census).
2. [Connect Data Source in Census](doc:census#connect-data-source-in-census).

## Add CleverTap as a Destination on Census

To add CleverTap as a destination in Census:

1. Go to _Connections_ from your Census dashboard and click **+ New Destination**.

2. Search for _CleverTap_ and select it.

3. Enter the following details:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

4. (Optional) Click **Test**  to test the connection and verify your entered credentials.
5. Click **Finish** to add CleverTap as a destination once the connection is verified.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d33e88b846d5495e75b278a7bee42e8601d3431f161fb578e3393f3c9268de05-image.png",
        null,
        "Add New Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Add New Destination"
    }
  ]
}
[/block]


## Connect Data Source in Census

Set up your preferred data source in Census to sync and manage data efficiently. To do so:

1. **Add a Data Source**:
   1. Go to the _Sources_ section from the Census dashboard and click **+ New Source**. 
   2. Select your preferred data source (For example, Google Sheets, databases, or data warehouses). 
   3. Follow the on-screen prompts to configure the connection and provide the required credentials, authentication tokens, or endpoint URLs as needed, based on the source.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/128c8f952e6cc023e8d2eb56b3e749ca621fead8c9743c3c977d91debabf1b68-image.png",
        null,
        "Add New Source"
      ],
      "align": "center",
      "border": true,
      "caption": "Add New Source"
    }
  ]
}
[/block]


2. **Test the Connection**: After completing the setup, click **Test** to verify the details and ensure the source is successfully connected.

For detailed instructions, refer to [Census](https://docs.getcensus.com/sources/overview).

# Send Data from Census to CleverTap

Import customer data, including user profiles and events, from your data sources into CleverTap to enhance targeting and engagement.

> 🚧 IMPORTANT
> 
> If your data source, such as Google Sheets, does not update in real-time, the information sent from Census to CleverTap might not capture the latest user actions or events. For instance, if a user updates their profile or makes a purchase but the Google Sheet has not synced yet, CleverTap receives outdated data until the sheet is refreshed. To maintain up-to-date information, consider syncing the data more frequently or switching to a real-time data source.

## Send Profiles to CleverTap

To import user profiles from your data warehouse into CleverTap: 

1. Go to _Syncs_  and **+ Create a new Sync** from your Census Dashboard.

2. Under _Select a Source_, choose a connection and its source. 

3. Select the schema and the table you want to sync.

4. Select _CleverTap_ as a _Connection_ from the _Select a Destination_ dropdown and select _Profile_ under the _Object_ dropdown.  
   For more detailed instructions, refer to the [Census Documentation on CleverTap Integration](https://docs.getcensus.com/destinations/available-destinations/clevertap).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f18676993dd8c381c2112ac4c163572605a258fa17b46e6f543c24f5478d3bab-image.png",
        null,
        "Select a Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Select a Destination"
    }
  ]
}
[/block]


5. Select a _Sync Behavior_. CleverTap supports _Update or Create_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebcedc087324a96b4fd68d9fad9a901713233ed6fb6a5776d7f073e1109dee6e-image.png",
        null,
        "Sync Behavior."
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Behavior."
    }
  ]
}
[/block]


6. _Select a Sync Key_ defines the key identifier for matching data in CleverTap. Census uses this key to determine which data to sync during each run. The column and field must have the same unique value.  
   For example, use `user_id` as the primary identity key (mapped to _User Identity_ in CleverTap). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e781ed5595327bf3a3ad23eda38fac06a03383a5ea38c95e864aca8464fd5f46-image.png",
        null,
        "Select a Sync Key"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Key"
    }
  ]
}
[/block]


7. Under **Set Up CleverTap Field Mappings**, select _Specific Columns_ properties or _Sync All Columns_ properties.
   - _Specific Columns_: Specify exactly which columns apply to the destination.
   - _Sync All Columns_: Sync all columns from the source to the destination. Any new columns will be automatically added.  
     Map source columns to CleverTap profile fields (for example, `username ➔ Name`, `email ➔ Email`). When you add a mapping, Census automatically matches some of the standard properties in CleverTap. You can also opt to create new properties inside CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf0670666767126810e649f32be901d7cce4576a17bdc7467ec8f25094b566a7-image.png",
        null,
        "Set Up CleverTap Field Mappings"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up CleverTap Field Mappings"
    }
  ]
}
[/block]


8. **Confirm Sync Details**: After configuring the sync, confirm your sync details and click **Create Sync** to set up the new sync.
9. **Set Sync Trigger**: Configure either a manual (One-Time Sync) or automatic (Periodic Sync) trigger for the sync.
   - _One-Time Sync_: To trigger an immediate sync, select **Run Sync Now**. This initiates an instant, one-time data sync.
   - _Periodic Sync_: To schedule regular updates, select _Sync Trigger_ and define the schedule to run sync automatically. This ensures that data between Census and CleverTap remains up-to-date, with profiles and events continuously updated.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/621caae7e177270298d628563d40198e85622b0f184ef66ece097b2b3f5c873d-pero.gif",
        "",
        "Set Sync Trigger"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Sync Trigger"
    }
  ]
}
[/block]


Go to the _Segments_  page from the CleverTap to confirm the synced profile data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0bf527c3ed911738e2aea29ea042200007a4e778501445a41c9b1c982d97032-image.png",
        null,
        "Segments"
      ],
      "align": "center",
      "border": true,
      "caption": "Segments"
    }
  ]
}
[/block]


## Send Events to CleverTap

To send events from your data warehouse to CleverTap:

1. Go to _Syncs_ and click **+ Create a new Sync** on your Census Dashboard.

2. Under _Select a Source_, choose a connection and its source. 

3. Select the schema and the table you want to sync.

4. _Select a Destination_:
   1. Under _Select a Destination_, choose _CleverTap_ as a connection. 
   2. Under _Object_, select _Event_.  
      For detailed instructions, refer to the [Census Documentation on CleverTap Integration](https://docs.getcensus.com/destinations/available-destinations/clevertap).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a49a11318aad2f7200098a4c54898f4b4ab14804de7c9ef7067146230dd72f4a-image.png",
        null,
        "Select a Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Select a Destination"
    }
  ]
}
[/block]


5. _Select a  Sync Behavior_. The sync behavior determines how changes are handled between the source and CleverTap. If you select **Send**, an event is created on CleverTap every time new records are detected in the source system.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5499b9ecfbc6529fe13f60d6e5443f740ee37c4cf0a88cb4fa2a89587f99ab23-image.png",
        null,
        "Sync Behavior"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Behavior"
    }
  ]
}
[/block]


6. _Select a Sync Key_. The Sync Key is a column that identifies unique records in the source, such as `user_id`. When a new sync key is detected, an event is raised on Clevertap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e40f881cf95cb17bdcecef096a14901d565975f7f4fae8c30fd80fe080d86129-image.png",
        null,
        "Select a Sync Key"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Key"
    }
  ]
}
[/block]


7. Under _Set Up CleverTap Field Mappings_, select whether you want to sync specific or all properties.  
   When you add a mapping, Census automatically matches standard properties in CleverTap. You can also create new properties in CleverTap if needed. Syncing **Event Name** (Action) and **User Identity** (Customer ID) is mandatory.
   - **Configure Event Syncing**: Use `user_id` or another unique identifier to link events to user profiles. Map source columns to CleverTap event fields, such as:  `transaction_value ➔ Transaction Value`  or `currency ➔ Currency`
   - ** Map Columns**: Map the source columns (for example, `user_email`) to corresponding fields in CleverTap. This ensures the correct data is sent to the proper fields.
   - **Assign Data Type**: Ensure each field is assigned the correct data type (for example, String, Number, Date, Boolean) for proper data processing.  
     The following example shows the mapping for the _Charged_ event 
     - `transaction_value ➔ Transaction Value`  
     - `currency ➔ Currency`  
     - `product_category ➔ Product Category`  
     - `discount_applied ➔ Discount Applied`

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6b21015a5c0936487caca2f942f432e46bd91bedda63b41cb5a958f0770e90b-image.png",
        null,
        "Set Up Field Mapping"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Up Field Mapping"
    }
  ]
}
[/block]


8. **Confirm Sync Details**: After configuring the sync, confirm your sync details and click **Create Sync** to set up the new sync.
9. **Set Sync Trigger**: Configure either a manual (One-Time Sync) or automatic (Periodic Sync) trigger for the sync.
   - _One-Time Sync_: To trigger an immediate sync, select **Run Sync Now**. This initiates an instant, one-time data sync.
   - _Periodic Sync_: To schedule regular updates, select _Sync Trigger_ and define the schedule to run sync automatically. This ensures that data between Census and CleverTap remains up-to-date, with profiles and events being updated continuously.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b79600a50a37e8f3fecf8b281c0e542c4aa8f9ac948c79b82b6afa2f5e1208d4-eevveesy.gif",
        "",
        "Sync Trigger"
      ],
      "align": "center",
      "border": true,
      "caption": "Sync Trigger"
    }
  ]
}
[/block]


You can verify the synced event data by navigating to _User Profiles_ or _Event Analytics_ from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9ce9d8f75bf67f5276b1e2c91c71b41a687bf8787e9c9010f28121f6ddd9dd9-image.png",
        null,
        "CleverTap Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "User Profiles CleverTap Dashboard"
    }
  ]
}
[/block]


# FAQs

### What types of data can I sync to CleverTap from Census?

You can sync user profiles and event data from different data sources supported by Census, including data warehouses, Google Sheets, and databases.

### How frequently can I sync data?

Syncs can be scheduled periodically or triggered on demand based on the business requirements.

### What happens if I map a field incorrectly?

Incorrect mapping can lead to inaccurate data being updated in CleverTap. You can modify the field mapping in Census to resolve the issue and re-sync.

### Can I sync historical data?

You can configure Census to include historical data during the initial sync.

### Who should I contact for support?

For any issues or queries, contact Census at [support@getcensus.com](mailto:support@getcensus.com).