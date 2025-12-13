---
title: Radar
excerpt: Contextual Location Partner
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

[Radar](https://radar.io) is a comprehensive location platform offering geofencing, geocoding, and mapping services to empower location-based experiences across millions of devices.

With the CleverTap and Radar integration, you can enhance your marketing campaigns with location-based intelligence as follows:

* Triggering promotional campaigns when users are near a physical store.
* Showing nearby service centers via In-App messages.
* Engage with users based on geolocation history.

# Prerequisites for Integration

To integrate Radar with CleverTap, ensure the following prerequisites are met:

* You have a Radar account with access to the [Publishable API Key](https://radar.com/dashboard/settings).
* You have an active CleverTap account.
* Latitude and longitude values are stored in CleverTap user profiles, preferably as custom user properties.

# Integrating Radar with CleverTap

The integration process involves the following three major steps:

1. [Locate Radar API Key](doc:radar#locate-radar-api-key)
2. [Configure Linked Content API](doc:radar#configure-linked-content-api)
3. [Create Personalized Campaign](doc:radar#create-personalized-campaign)

## Locate Radar API Key

To complete the integration process, you will need your Radar API key. After logging into your Radar account, go to *Home* section to find the key.

<Image alt="Radar API Key" align="center" width="65% " border={true} src="https://files.readme.io/dd86462bb504e8463c2dbdf3b4e85fc9236cd295948a72d913ec2e6a05e9bc59-image.png">
  Radar API Key
</Image>

## Configure Linked Content API

To integrate Radar's Search Places API with CleverTap, configure the Linked Content API. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

| Field        | Value                                                                                                                             |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| Name         | Provide a name for the Linked Content. For example:` Radar`                                                                       |
| Request Type | Select `GET` method.                                                                                                              |
| Endpoint URL | Enter the following endpoint URL:`https://api.radar.io/v1/search/places?near={{Latitude}},{{Longitude}}&chains={{place}}&limit=5` |

This endpoint uses the following three parameters:

* `Latitude` and `Longitude` pulled from user profile (custom properties)
* `place`: chain name to search near the user (for example, `starbucks`)

<Image alt="Configure the Linked Content API" align="center" width="65% " border={true} src="https://files.readme.io/7c8b4bac5ead7ca4be970a4d5a511180526ee546e75d9374ead587d33e5e4dfa-image.png">
  Configure Linked Content API
</Image>

3. Under *Headers*, add the following:
   * Authorization: `<your-api-key>`

<Image alt="Key value pair" align="center" width="65% " border={true} src="https://files.readme.io/af0983589c0a48b7f821f042e6250164b9c2a28194abc3f66b57d82060904c8d-image.png">
  Key Value Pair
</Image>

4. Click **Test the Linked Content** using sample values. The following is a sample response:

```json
{
  "meta": { "code": 200 },
  "places": [
    {
      "_id": "61dda2c10bb02c4952d5005e",
      "name": "Starbucks",
      "location": {
        "type": "Point",
        "coordinates": [72.83543684530189, 19.172690329535484]
      },
      "categories": ["food-beverage", "cafe"],
      "chain": {
        "slug": "starbucks",
        "name": "Starbucks",
        "domain": "starbucks.com"
      }
    }
  ]
}
```

5. Click **Auto-Fill Objects with Response** to automatically handle responses and populate objects.
6. Click **Test and save changes** to complete the setup.

<Image alt="Test And Save" align="center" width="45% " border={true} src="https://files.readme.io/8030a9a04bd63c0f4f466c005c6801db77703cf1e2e4df9ef7e3edb93568a2a3-image.png">
  Test And Save
</Image>

> 🚧 Caution
>
> Radar's Search Places API has a default rate limit of 100 requests/min. Plan campaign traffic accordingly.

## Create Personalized Campaign

You can use the Linked Content API integration with Radar to power location-based personalization in your CleverTap messaging campaigns.

To integrate a Radar into your CleverTap Push campaign, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Push Notification* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section.

   1. Click **Personalization**.
   2. Select the Linked Content configured under [Configure Linked Content API](doc:radar#configure-linked-content-api) and click **Apply**.

<Image alt="Personalization" align="center" width="65% " border={true} src="https://files.readme.io/08ea6f76636a194fcad355b6b2a9c6237a42d997e83a4f99c57e58a84961fb36-2025-06-18_15-50-28_1.gif">
  Create a Personalized Email Campaign
</Image>

3. Map the required API parameters to personalize the message:
   * **Latitude** → `{{ Profile.lat }}`
   * **Longitude** → `{{ Profile.long }}`
   * **Place** → chain slug (for example, `starbucks`)

<Image alt="Set API Parameters" align="center" width="65% " border={true} src="https://files.readme.io/31bd864ca0da27e2db1309db3663ee64fb1af3a9e080762ecc0c99a89458b046-image.png">
  Set API Parameters
</Image>

4. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize the message with nearby place data from the Linked Content API. The dynamic fields in the API response let you insert real-time location details directly into the message. For example:\
   **Example 1: Display the First Nearby Place**
   ```
   Welcome to {{ Linked["Nearby Radar Places"].places[0].name | default: "our store" }}
   ```
   **Example 2: List Up to 5 Nearby Places**
   ```
   Explore nearby spots:
   {% for place in Linked["Nearby Radar Places"].places limit:5 %} 
   - {{ place.name | default: "store" }}
   {% endfor %}
   ```
   **Example 3: Show Places Only If Available**\
   Use a conditional check to ensure the campaign is only sent if at least one nearby place is detected.
   ```
   {% if Linked["Nearby Radar Places"].places and Linked["Nearby Radar Places"].places.size > 0 %}
   Check these places near you:
   {% for place in Linked["Nearby Radar Places"].places limit:5 %} 
   {{ place.name | default: "store" }}
   {% endfor %}
   {% endif %}
   ```
5. Click **Preview and Publish** to test and launch the campaign.

<Image alt="Push notification" align="center" width="30% " border={true} src="https://files.readme.io/3b8615108fd083c573b857a474a5373d0ef120686a4c19ea9a0bf6a43fb0353b-image.png">
  Push Notification
</Image>

By combining Radar’s location intelligence with CleverTap’s personalization engine, you can deliver hyperlocal, context-aware campaigns that drive real-world engagement and customer delight.
