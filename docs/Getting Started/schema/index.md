---
title: Schema
excerpt: ''
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

Schema is a framework to maintain your data, organize, and structure it. It enforces rules to maintain data integrity, allowing you to avoid data quality issues later. Schema standardizes your data before you even begin using it. Since bad data leads to a high cost in effort and money, you can save a lot of manual effort on tracking your data in the long run.

To preserve data sanity, the schema table stores event and user properties in a pre-defined order. It ensures better output because it enforces standardization of the incoming data and avoids duplication or corruption of data. Better input leads to a better outcome in your campaigns and journeys. It also provides more accurate insights into your data analytics.

# Events

You can see your events under _Settings_ > _Schema Events_. On this page, you can view all the events you are working with, along with editing or discarding to searching and filtering them.

The _Events_ schema has four parts:

* [Custom events](https://docs.clevertap.com/docs/schema#section-custom-events)
* [System events](https://docs.clevertap.com/docs/schema#section-system-events)
* [Conversion event](https://docs.clevertap.com/docs/schema#section-conversion-event)
* [Qualifying event](https://docs.clevertap.com/docs/schema#section-qualifying-event)

# Custom Events

Custom events are events that you can define, edit, remove, and so on. These are your app events that you can fully control.

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. Click the **Custom events** tab.

If you have already defined your events, they are all present on this tab.

  View Custom Events

| Event Detail   | Description                                                                                                                                                                                                                                                                                                                                                         |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Event name** | The name of the event as it is displayed on the dashboard.                                                                                                                                                                                                                                                                                                          |
| **Type**       | There are two types:<ul><li>**Defined:** Events that are part of your schema definition.</li><li>**Undefined:** Events that are not defined in the schema but passed to CleverTap.</li></ul>                                                                                                                                                                        |
| **Status**     | An event can have any of the following statuses:<ul><li>**Active:** An event that has been passed to CleverTap.</li><li>**Inactive:** An event that has not yet been passed to CleverTap.</li><li>**Discarded:** An event for which all past data has been dropped. Any future data that is passed for the event with the same name will also be dropped.</li></ul> |
| **DRP**        | Data retention policy defines the length of time that the data is retained.                                                                                                                                                                                                                                                                                         |
| **This month** | The number of occurrences of the event in the current month.                                                                                                                                                                                                                                                                                                        |
| **Last month** | The number of occurrences of the event in the previous month.                                                                                                                                                                                                                                                                                                       |
| **Count**      | A count can be an event, event property, or a user property update.                                                                                                                                                                                                                                                                                                 |
| **Properties** | Attributes that provide additional context around the event. For more information, refer to [Event Property](doc:events#event-properties).                                                                                                                                                                                                                          |

## Add Event

You can add an event from the _Custom events_ tab.

1. Navigate to _Settings_ > _Schema Events_ > _Custom events_.
2. Click the **+Event** button to add an event.
3. Add the event name. This name must be unique in the schema.

![](https://files.readme.io/6a62a19-Add_New_Event.png "Click +Event. toAdd a Custom Event")  Add a Custom Event

For more information, refer to [Event Property](doc:events#event-properties).

## Edit Event

The name cannot be changed after the event is published.

1. Click the edit icon on the event row.
2. Edit the event name.
3. Click the checkmark.

## Set Data Retention Policy

The data retention policy (DRP) retains an event for the specified time before discarding it automatically. Your subscription plan will decide the default DRP limit.

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. From the System Events tab, click the ellipsis on the event row and click **Set DRP**.
3. Select _Custom_, then enter your specific time limit.

> 📘 CleverTap Essentials Plan Limit
>
> The default DRP for CleverTap Essentials Plan users is one year, which cannot be changed.

4. Click **Save**.

![](https://files.readme.io/ba7f979-SET_DRP.png "Select the Storage Time and Click Save")  Set Data Retention Policy (DRP)

## Remove Event

You must be careful before removing an event. If you ever need to remove an event from the schema, remove it from the event row on the _Events_ page. You can only remove an inactive event from your schema; however, the effects are minimal because the event is not active. This action does not drop another event coming in with the same name.

1. Click the ellipsis menu on the event row.
2. Click **Remove**.

![](https://files.readme.io/b6033f7-Custom_Events.png "Click Remove from the Ellipsis Menu to Remove the Event")  Remove an Event

After an event is removed:

* The entire event row is removed from the schema.
* If an event comes in with the same name, it is considered an undefined event.

## Discard Event

You can discard an active event from the schema. You can still see the event row in the schema; however, it will be marked as discarded.

> ❗️ Caution When Discarding an Event
>
> You can only discard an active event. Exercise extreme caution when discarding an event because this action cannot be undone. This action has an impact on your schema because it purges all data for the discarded event. It also drops any future incoming event with the same name.

1. Click the ellipsis menu on the event row.
2. Click **Discard**.

![](https://files.readme.io/6f94655-Discard_event.png "Click Discard from the Ellipsis Menu to Discard the Event")  Discard an Event

## Define Event

The events that are passed to CleverTap but not defined are marked as undefined events. You can define these events from the event row. Defining an event marks it as a recognized event in the schema, and therefore, when the event is received, this will not cause any error.

1. Click the ellipsis menu on the event row.
2. Select _Define Event_, and a new window displays.
3. Click **Define & Save**.

## Publish Schema/Events

To publish the events, perform the following:

1. Check that you have all the required events.
2. Click the **Publish Events** button.

| Event Name             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Property name**      | The name of the property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Type**               | The type of property:<ul><li>**Defined:** Properties that you have added to the schema.</li><li>**Undefined:** Properties that you have not added to the schema and are currently receiving data.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Status**             | An event property can have any of the following statuses:<ul><li>**Active:** An event property that has been passed to CleverTap.</li><li>**Inactive:** An event property that has not yet been passed to CleverTap.</li><li>**Discarded:** An event property for which all past data has been dropped. Any future data passed for this user property with the same name will also be dropped.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Required**           | Defines whether a property is mandatory for the event:<ul><li><p><strong>Yes:</strong> The property is mandatory. The event is dropped if it is received without the event property.<br /><em>Note:</em> Use with caution. If an event is received without the required property, the entire event is dropped. This helps keep data clean but may unintentionally drop valid events.</p></li><li><p><strong>No:</strong> The property is optional. The event is allowed even if it is received without the event property.</p></li></ul>                                                                                                                                                                                                                                                                                        |
| **Data type**          | Defines the data type of the event property:<ul><li>String</li><li>Integer</li><li>Float</li><li>Boolean</li><li>Mixed</li><li>List</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Data type fallback** | The fallback action if the event property is not in the defined format:<ul><li><strong>Drop event:</strong> Drops the incoming event if the data type does not match.<br /><em>Note:</em> This action cannot be undone and purges all past and future data for the event.</li><li><strong>Drop event property:</strong> Drops the incoming event property if the data type does not match.<br /><em>Note:</em> This action cannot be undone and purges all past and future data for the event property.</li><li><strong>Allow property:</strong> Allows the property even if the data type does not match.</li></ul>An error is reported for all actions. A <em>drop</em> has higher severity, while <em>allow</em> has lower severity. For more information, see [Error Stream](https://docs.clevertap.com/docs/error-stream). |
| **Created on**         | The date when the user property was created.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Description**        | The description of the event property. You can set this from the ellipsis menu on the event property row. The property is optional, and the event is allowed even if it is received without the event property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

> 📘 Effect of Changing the Data Type of an Event or User Property
>
> * If you change the user or event property's data type, then all the incoming data will be validated as per the schema definition once you publish the changes.
> * The values already present in the old data type will not change in the new data type.
> * For the users who already have the value of the user/event property in the old data type, you will have to again pass the user/event property with the value that will have a new data type.

## Add Event Property

To add an event property:

1. Click the number of properties shown in the _Custom events_ tab
2. Click **+Property**, then click **Add new**.  
   You can also add an event property from the catalog by clicking **Add from catalog**. For more information, refer to [Add Columns from a Catalog](doc:catalog-data-ingestion#add-columns-from-a-catalog).
3. Enter a property name and choose the relevant property details.
4. Select the checkmark.

![](https://files.readme.io/9a45a27-Add_property.png "Click +Property to Add Event Property")  Add Event Property

## Edit Event Property

You can edit any column; however, you can only edit names for unpublished event properties.

1. Click the edit icon on the property row from the _Custom events_ tab.
2. Edit the property name and any other appropriate property details.
3. Click the checkmark.

![](https://files.readme.io/804cbdc-Edit_Event_Property.png "Click the Edit Icon to Edit Event Property")  Edit Event Property

## Remove Event Property

You can remove an unpublished event property.

1. Click the ellipsis icon on the property row from the _Custom events_ tab.
2. Click **Remove**.

After an event property is removed:

* The entire event property row is removed from the schema.
* If an event property comes in with the same name, it is considered undefined.

## Discard Event

You can discard an active event from the schema. You can still see the event row in the schema; however, the event is marked as discarded. Post discarding, CleverTap removes the data after 16 days. However, you can choose to restore the discarded event after 24 hours. For more information, refer to [Restore Events](doc:schema#restore-event).

> ❗️ Caution When Discarding an Event
>
> You can discard only an active event. Discarding an event purges all data for that event and drops any future incoming events with the same name. This action impacts your schema. A discarded event can be restored, but only after 24 hours.

1. Click the ellipsis menu on the event row.
2. Click **Discard**.

![](https://files.readme.io/6f94655-Discard_event.png "Click Discard from the Ellipsis Menu to Discard the Event") Discard an Event

> 📘 Discard Access
>
> Only admin users can discard events.

## Restore Event

You can restore a previously discarded event, event property, or user property from the schema. Once restored, it becomes available again across Campaigns, Journeys, Analytics, and other features that use the schema.

> 🚧 Cooldown Period for Restore and Re-discard
>
> * After you discard an item, you cannot restore it for the next 24 hours.
> * After you restore an item, you cannot discard it again for the next 24 hours.
>
> These measures prevent accidental or repeated changes to your schema.

> 📘 Private Beta
>
> This feature is currently available in Private Beta for selected customers. To enable, contact your Customer Success Manager or raise a support ticket.

### Restore a Single Item

1. Go to the _Custom events_ page.
2. Locate the discarded event you want to restore.
3. Click the ![](https://files.readme.io/d1a1a29245a043e42fe9f768ccb6c41e50dc1693d8b3553ac09edd9cadcc8355-Restore_Icon.png) icon.
4. In the confirmation window, click **Restore**.

![](https://files.readme.io/b64c088b7f531e770b0e9b81441008e59bb5b099c0a00a2f8b0be2826e0b9568-image.png) Restore Custom Event

### Restore Multiple Items

1. Go to the Events, or Event Properties, or User Properties table on the _Custom events_ page.
2. Select the discarded items you want to restore.
3. Click the ![](https://files.readme.io/4f93c7fed376db11d7b36dd4e54539e1a2284761341d8dfc3e227322f366d3d5-Restore_Icon.png) icon from the toolbar.
4. In the confirmation window, click **Restore**.

![](https://files.readme.io/f3def79a65dda3e144e4a8711f3e4e0407dc1b61b35dbcb12699fbde4ba41230-image.png) Bulk Restore Discarded Items

> 📘 Restore Access
>
> Only admin users can restore the discarded events.

# User Properties

This section shows how to manage your user properties.

1. Navigate to _Settings_ > _Schema_ > _User Properties_.  All the user properties are listed on this page.
2. Click any of the properties on the user property row to see the property details.

From this page, you can also search and filter properties.

| Property Detail        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Property name**      | The name of the user property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Type**               | The type of property:<ul><li><strong>Defined:</strong> Properties that you have added to the schema.</li><li><strong>Undefined:</strong> Properties that you have not added to the schema and are currently receiving data.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Status**             | A user property can have any of the following statuses:<ul><li><strong>Active:</strong> A user property that has been passed to CleverTap.</li><li><strong>Inactive:</strong> A user property that has not yet been passed to CleverTap.</li><li><strong>Discarded:</strong> A user property for which all past data has been dropped. Any future data passed for this user property with the same name will also be dropped.</li></ul>                                                                                                                                                                                           |
| **Data type**          | Defines the data type of the user property:<ul><li>String</li><li>Integer</li><li>Float</li><li>Boolean</li><li>Mixed</li><li>List</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Data type fallback** | Includes the following actions:<ul><li><strong>Drop user property:</strong> Drops the incoming property if the data type does not match.<br /><em>Note:</em> Use with extreme caution. This action cannot be undone and purges all past and future data for the discarded user property.</li><li><strong>Allow property:</strong> Allows the property even if the data type does not match.<br />An error is reported for all actions. A <em>drop</em> has higher severity, while <em>allow</em> has lower severity. For more information, see <a href="https://docs.clevertap.com/docs/error-stream">Error Stream</a>.</li></ul> |
| **Created on**         | The date when the user property was created.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

## Add User Property

To add a user property from this page:

1. Click the **+Property** button.
2. Enter a property name and choose a data type.
3. Click the checkmark.

![](https://files.readme.io/fc5ba43-Add_User_Property.png "Enter a Property Name and Choose a Data Type to Add a User Property") Add User Property

## Edit User Property

You can edit any column; however, you can only edit names for unpublished user properties. To edit a property, click the edit icon on the property row.

1. Click the edit icon on the property row.
2. Edit the property name and the data type.
3. Click the checkmark.

![](https://files.readme.io/0afe960-Edit_User_Property.png "Click the Edit Icon to Edit the Property Name and Data Type") Edit User Property

## Remove User Property

You can remove an unpublished property.

1. Click the ellipsis icon on the property row.
2. Click **Remove**.

After a user property is removed:

* The entire user property row is removed from the schema.
* If a user property comes in with the same name, it is considered as an undefined user property.

## Discard User Property

You can discard a published user property from the schema. You can still see the property row in the schema; however, it will be marked as discarded.

1. Click the ellipsis icon on the property row.
2. Click **Discard**, and a new window displays.
3. Click **Discard** again.

![](https://files.readme.io/d75580c-Discard_User_Property.png "Click Discard Button to Discard User Property") Discard User Property

> ❗️ Caution When Discarding a User Property
>
> Exercise extreme caution when discarding a user property. This action cannot be undone. This action has an impact on your schema because it purges data for the discarded user property. It also drops any future incoming user property with the same name.

## Create Linked Event for User Property

You can link an event with a user property. This allows you to trigger campaigns, conversions, and exits based on changes in user properties. For example, a gaming app has a user property named `Game Level` that represents a user's progress in the game. You can link an event named `Game Level Upgraded` to the `Game Level` user property. By doing so, any change in this property to a higher level will activate a campaign. The campaign will congratulate the users and grant them a reward or a unique power corresponding to their achievement.

> 📘 Key Points to Remember
>
> * This feature is supported only for messaging channels such as Push, SMS, Email, In-App, Webhooks, and remarketing channels such as Google Ads and Facebook Audiences.
> * For In-App, CleverTap SDK v7.0.0 or higher is required.
> * User property updates via Journeys are not supported for this feature.

To link an event with a user property:

1. Navigate to _Settings_ > _Schema_ > _User Property_ from the CleverTap dashboard.
2. Click the ![](https://files.readme.io/01a6671-Ellipsis.png) icon and select _Create Linked Event_.
3. Enter the _Event Name_ and click **Create Event**.

![](https://files.readme.io/f3777e6-Create_Linked_Event_for_User_Property.gif) Create Linked Event

### Create Linked Events in Bulk

You can select multiple user properties at a time and link a required event to it.

To create linked events in bulk:

1. Select the user properties you want to link and click the ![](https://files.readme.io/9bd94d1-Bulk_Link.png) icon.

![](https://files.readme.io/6675b4f-Bulk_Link_Event.png) Bulk Link Events

2. Enter the events you want to link for each user property and click **Create**.

![](https://files.readme.io/7b5b7fd-Create_Linked_Events_in_Bulk.png) Create Linked Events in Bulk

### Discard Linked Event

You can discard a linked event from the user property.

To discard linked events:

1. Click the ![](https://files.readme.io/01a6671-Ellipsis.png) icon of the user property.
2. Select _Discard Linked Event_ and click **Discard**.

![](https://files.readme.io/5980787-Discard_Linked_Event.gif) Discard a Linked Event

> 📘 Key Points to Remember
>
> The following are the key points to consider when creating linked events:
>
> * You can link only one event with a user property.
> * You can link events only on active properties.
> * You cannot create a linked event with the same name as a system event.
> * Discarding a linked event from the user property:
>   * Delinks the event and the user property.
>   * Stops receiving additional data associated with the user property.
>   * Does not delete any data.

# System Events

System events are tracked automatically. CleverTap offers the capability to configure system events, enabling businesses to monitor and analyze user actions in their applications. However, some businesses may not have an immediate need for certain system events, resulting in potentially avoidable expenses. CleverTap allows businesses to configure those unused system events, providing a seamless process to address this issue.

## Configure System Events

To configure the tracking of system events:

1. Navigate to _Settings_ > _Schema_ > _Events_ from the CleverTap dashboard.
2. Select the event that you want to configure from the _System events_ tab.
3. Click the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon and select _Enable/Disable_ from the list.

![](https://files.readme.io/4454bcf-UTM_Tracking_Toggle_Off.gif)  Turn Off Toggle to Disable Tracking UTM Visited

Currently, you can enable or disable tracking for the following events from the CleverTap dashboard:

> 📘 Configuring Other System Events
>
> For the remaining system events, you can only change the DRP.

# Conversion Event

The conversion event helps track conversion.

To set a conversion event:

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. Click the **Conversion event** tab.

To track revenue, set the user conversion event and revenue property. This property must be a numeric value.

![](https://files.readme.io/5ba54c0-set_conversion.png "Set Conversion Event Details and Click Save")  Set Up Conversion Event

# Qualifying Event

To set a qualifying event:

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. Click the **Qualifying event** tab.

This event qualifies users as active if they have performed the event at least once in the defined time.

Currently, the [active %](https://docs.clevertap.com/docs/trends#section-active) tab uses the qualifying event on the _Trends_ page.

![](https://files.readme.io/5d67342-set_qualifying.png "Set Qualifying Event and Click Save")  Set Qualifying Event

# Download Schema Data from Dashboard

You can download the data for all events and user profiles from the CleverTap dashboard or via an API.

## Event Data

To download event data from the CleverTap dashboard in CSV format:

1. Navigate to _Settings_ > _Schema_ > _Events_. You can download event data from the _System events_ tab or the _Custom event_ tab.
2. Click the **Download as CSV** button, then the _Download CSV file_ window displays.
3. Select to download _Events_ or _Events with properties_.
4. Click **Download**.

## User Profile data

To download all event data from the CleverTap dashboard in CSV format:

1. Navigate to _Settings_ > _Schema_ > _User Properties_.
2. Click the **Download as CSV** button.

## Download with API

To download event data or user profile data with API, refer to the following:

* Use the [Events Schema API](https://developer.clevertap.com/docs/get-schema#section-get-events-schema-api) to download event data.
* Use the [User Properties Schema API](https://developer.clevertap.com/docs/get-schema#section-get-user-properties-schema-api) to download user profile data.

# Considerations

There are some specific validations when creating events and properties. For more information, refer to [Platform Considerations](doc:platform-considerations).

# FAQs

#### Q. Can we get all past behavior data for an event after discarding it?

A. No, we cannot get all past behavior data for an event after discarding it.

#### Q. Does a discarded event appear under the user profile in the user's activity?

A. No, a discarded event does not appear under the user profile in the user's activity.

#### Q. For how many days can I get the data of discarded events?

A.  You will not get any event data after discarding an event. We recommend you export that event before you delete it.

#### Q: If we disable the UTM Visited event from the schema, can it still be ingested through third-party mediums such as attribution tools like AppsFlyer or Customer Data Platforms (CDPs) like Segment?

A: When the UTM Visited event is disabled from the schema, it is dropped at the processing layer, rendering it inaccessible for ingestion from any third-party medium.

<HTMLBlock>{`
<style>
  .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  .markdown-body summary {
  font-size: 16px;
  font-weight: bold; 
  text-transform: camelcase;
}
  
details .rdmd-table {
   margin-bottom: 20px;
}
  details[open] summary { margin-bottom: 20px;
  }
</style>
`}</HTMLBlock>
