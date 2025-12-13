---
title: Geofencing Campaign
excerpt: Send messages to your users based on their location.
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

A geofence is a virtual geographic area, represented as latitude and longitude pairs combined with a radius, forming a circle in a specific position on a map. CleverTap offers geofencing, a GPS location-based service. Customers can use this service to engage their audience by sending relevant messages to Android and iOS users. Geofences can vary in size, and a geofence cluster can contain up to 100 geofences. 

Customers can define geofences around the world from the CleverTap dashboard. Campaigns are delivered in real-time to users as they exit or enter geofences or sent as follow-ups hours or days later. CleverTap's location analytics create user data as the users enter or exit geofences. This data can be used for re-targeting. Geofence-specific analytics can generate insight into activities or locations of interest.

# Create Geofences

To create geofences, perform the following steps:

1. From the CleverTap dashboard, navigate to *Settings* > *Geofences*.
2. Click **+ Geofence Cluster** to create a new geofence cluster.

<Image title="Click +Geofence Cluster Button" alt={1403} align="center" border={true} src="https://files.readme.io/d47ee91-1_Geofence_Cluster.png">
  Geofence Cluster
</Image>

> 📘 Geofence and Cluster Limits
>
> You can create up to 100 geofences in each cluster and up to 100 clusters for your app.

3. Select the preferred unit of measure for tracking the location of the geofence clusters. For example, select the distance in kilometers or miles. 
4. Click **Save**.

<Image title="Select the Preferred Unit of Measure" alt={1404} align="center" border={true} src="https://files.readme.io/c40fcfa-2_Select_the_preferred_unit_of_measure.png">
  Set Up Geofence
</Image>

5. Click the *Search for location* window to select the area you want to display on the map or enter a location in the search bar. A setting pop-up window displays.
6. Enter a *Geofence* name.
7. Determine the radius that the geofence must cover.
8. Click **Add** on the pop-up window.
9. Click **Continue**.

<Image title="Enter the Geofence Name and Radius and Click Add" alt={1404} align="center" border={true} src="https://files.readme.io/bbcdb82-3_Add_a_geofence_name.png">
  Define Geofence Radius
</Image>

10. Enter a geofence cluster name.
11. Select the start and end time of tracking the users. If you select *Select date and time*, day and time options display beneath the radio buttons where you can choose a future start and end date and time.
12. Click **Activate** or **Schedule**.

<Image title="Add Geofence Cluster Details and Click Activate" alt={1675} align="center" border={true} src="https://files.readme.io/19f8208-2020-09-03_17-33-08_Creating_Cluster_Name.png">
  Activate Geofence
</Image>

## Do Not Disturb Feature (Optional)

When entering the details for the geofence cluster, you can select a Do Not Disturb (DND) window. The DND option prevents triggering an engagement for users who enter the geofence on specified days and times. 

<Image title="Select the Do Not Disturb Options and Click Schedule" alt={701} align="center" border={true} src="https://files.readme.io/da7e4a0-DND.png">
  Set Up Do Not Disturb Details
</Image>

> 📘 Add, Edit, or Delete Geofences
>
> Repeat the steps to add more geofences to your cluster. You can have up to 100 geofences in a cluster. In addition, you can edit or delete a geofence by clicking the location and clicking the edit or delete icon, respectively. You can also edit or delete geofences by selecting them from the list on the left.

## Use Geofence Events

CleverTap raises two system events every time a device enters or exits a geofence. The following events can be used to run campaigns, analytics, and segmentation:

* Geocluster Entered
* Geocluster Exited

> 📘 Note
>
> The geocluster name displays under event properties if the event has at least one occurrence.

For more information, refer to [System Events](doc:events#section-system-events).

# Example Use Case

A retail company that sells apparel wants to increase traffic to its physical stores in Mumbai. They have multiple store locations and want to send personalized promotions to customers close to their stores. Using CleverTap's geofence campaign, the retail company can target users who enter the specified radius around their store locations with real-time and location-based messages.

## Create a Geofence Campaign

To solve the above business use case, create a push notification campaign adding the geofence cluster. The retail company can target users most likely to visit their physical stores and increase footfall. By using CleverTap's geofence campaign, they can send real-time, location-based messages that are personalized and relevant to the user.

The following are the steps to create a push notification campaign with a geofence cluster for users who enter the geofence:

### 1. Set Up a Geofence Cluster

Set up a geofence cluster around the store locations from the CleverTap dashboard. You can specify the radius and location coordinates of each store location. To set up a geofence cluster, refer to [Create Geofences](https://docs.clevertap.com/docs/geofencing#create-geofences).

### 2. Create a Campaign

After you have set up the geofence cluster and created the segment, you can create a geofence campaign from the CleverTap dashboard. To do so, perform the following steps:

1. From the dashboard, navigate to *Campaigns*. 
2. Click **+ Campaign**.
3. Select *Push Notifications* as a messaging channel.

<Image title="Click +Campaign and Select Push Notification" alt={1571} align="center" border={true} src="https://files.readme.io/7801d002dd9b7622b57766862d0ad7db4e473b88d2a161ff5cc47e1aa7dcd388-Select_the_Push_Campaign.png">
  Create Campaign
</Image>

4. Select the *Live Behavior*.
5. Click **Done**.

<Image title="Select Live Behavior in Qualification Criteria and Click Done" alt={1096} align="center" border={true} src="https://files.readme.io/409c246-Live_Behavior.png">
  Set Qualification Criteria
</Image>

6. Select *Conversion Tracking* under the *Set a goal* section.
7. Select the conversion event, time, and revenue property.
8. Click **Done**.

<Image title="Set Conversion Tracking Rules and Click Done" alt="Set a Goal" align="center" border={true} src="https://files.readme.io/0d02449-Select_a_Goal.png">
  Set a Goal
</Image>

9. Select the *Geofence Entered* event with event property as *Geofence ID* from the *Who* section of campaign creation.

<Image title="Select the Target Segment Options and Click Done" alt="Define - Who" align="center" border={true} src="https://files.readme.io/204aeef-Target_Segment.png">
  Define - Who
</Image>

This ensures that the message is only sent to users close to the store locations.

10. Set up the message content and design. For more information, refer to [Define Message Content](https://docs.clevertap.com/docs/create-message-push#define-message-content).

### 3. Personalize the Message

You can also use CleverTap's personalization features to make the message more relevant to the user. For example, you can include the user's name or previous purchase history in the message. For more information, refer to [Personalize Meessage](doc:personalize-message-all).

### 4. Schedule the Campaign

Finally, schedule the campaign to be sent at a specific time or based on particular triggers; for example,  send a campaign when the user enters the geofence for the first time.
