---
title: AccuWeather
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

[AccuWeather](https://www.accuweather.com/) offers global weather forecasting services through APIs that provide accurate, location-based data. With the CleverTap and AccuWeather integration, marketers can enhance campaign relevance by tailoring messages based on local weather conditions.

With this integration, you can:

* Recommend products based on local forecasts (for example, sunscreen during sunny weather)
* Send alerts when severe weather is predicted in a user's area
* Personalize content dynamically using user location and current conditions

# Prerequisites for Integration

Ensure the following before starting the integration:

* Ensure you have access to your CleverTap account.
* Ensure you have access to your AccuWeather account.
* Obtain your *AccuWeather API key* from the AccuWeather account manager.

 Read more on the AccuWeather API [here](https://apidev.accuweather.com/developers/).

# Integrate CleverTap with AccuWeather

To integrate AccuWeather with CleverTap, perform the following two major steps:

1. [Set Up AccuWeather APIs in CleverTap](doc:accuweather#set-up-accuweather-apis-in-clevertap)
2. [Create Personalized Campaign Using Linked Content](doc:accuweather#create-personalized-campaign-using-linked-content)

## Set Up AccuWeather APIs in CleverTap

Use [Linked Content](doc:linked-content) in CleverTap to connect to AccuWeather APIs and personalize campaign content dynamically. Configure the following APIs:

1. [Get Location Key](doc:accuweather#get-location-key-from-accuweather): Retrieves a location key based on the user’s city or postal code.
2. [Get Weather Conditions](doc:accuweather#get-weather-conditions-using-location-key): Returns current weather data for the specified location key.

For a complete list of available APIs and capabilities, refer to the [AccuWeather API](https://apidev.accuweather.com/developers/partner-code).

### Get Location Key from AccuWeather

Map a user’s city or postal code to an AccuWeather location key. This key is required to fetch weather data in [Create Personalized Campaign Using Linked Content](doc:accuweather#create-personalized-campaign-using-linked-content).

To configure this API in CleverTap, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* in CleverTap.
2. Click **+ Add Linked Content**.
3. Set the method to `GET` and enter the following endpoint URL:

```Text REST API
https://dataservice.accuweather.com/locations/v1/cities/search?apikey=<API KEY>&q={{city/pincode}}&top=0
```

4. Replace `{{city/pincode}}` with a custom parameter:`{{ Profile.city | default: "-" }}`.
5. Click Test Linked Content. You should get the following response:

```json
[{
        "Version": 1,
        "Key": "204847",
        "Type": "City",
        "Rank": 25,
        ...
    }]
```

<Image alt="Add Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/4970afad28b8459a3ee917028a2f4dfe4d946fc48e7018861f726e60c1eee824-image.png">
  Add Linked Content
</Image>

6. Click **Test and Save Changes**.

### Get Weather Conditions Using Location Key

Use this API to fetch the current weather condition for the user’s location based on the AccuWeather location key.

To configure this API in CleverTap, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* in CleverTap.
2. Click + Add Linked Content.
3. Set the method to `GET` and enter the following endpoint URL:

```Text REST API
https://datxaservice.accuweather.com/currentconditions/v1/{{key}}?apikey=<API KEY>
```

4. Replace `{{key}}` with a custom parameter: `{{ Linked["Get Location Key"].json[0].Key | default: "-" }}`
5. Click Test Linked Content. You should get the following response:

```json
[
    {
        "LocalObservationDateTime": "2025-03-06T11:22:00+05:30",
        "EpochTime": 1741240320,
        "WeatherText": "Sunny",
        ...
]
```

<Image alt="Add Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/94f91fb578a84c72b4b6e1d163d85a13447260e4d9e94dc54e80beea4877f941-image.png">
  Add Linked Content
</Image>

6. Click **Test and Save Changes**.

## Create Personalized Campaign Using Linked Content

With AccuWeather connected to CleverTap via Linked Content, you can now add weather-based personalization to your campaigns. For this example, let us create a short, personalized push notification.

To do so, perform the following steps:

1. Go to *Campaigns* from the CleverTap dashboard and click **+ Campaign**.

2. Select *Push Notification* from the *Messaging Channels* list.

3. Configure your campaign settings and navigate to the *What* section.

4. Click **Personalization**, then select both Linked Content entries:

   * Set the `city/pincode` parameter for [Get Location Key API](doc:accuweather#get-location-key-from-accuweather) to Custom and enter:`{{ Profile.city | default: "-" }}`
   * Set the `key` parameter for [Get Weather API](doc:accuweather#get-weather-conditions-using-location-key) to Custom and enter:`{{ Linked["Get Location Key"].json[0].Key | default: "-" }}`

<Image alt="Personalization" align="center" width="75% " border={true} src="https://files.readme.io/a3426893d073d48cd3fb0935e0fe137ba36b271e9abc1fc75f0b4903a698c5d7-image.png">
  Personalization
</Image>

5. Type `{`, `{{`, or `@` to view available personalization options. For more information about how to personalize a message using Linked Content, refer to [CleverTap Liquid tag](doc:personalize-message-all).

<Image alt="Create Personalized Message Using Linked Content" align="center" width="75% " border={true} src="https://files.readme.io/9d790140ea02efe54438005c76a9d51f2a87e09fd24ff4ddcc3d262ee54503f3-image.png">
  Create Personalized Message Using Linked Content
</Image>

For this example, we will use the [Linked Content Liquid tag](doc:personalize-message-all) below to iterate through the Get Weather API’s JSON response to get the Weather Text.

```json
{{ Linked["Get Weather"].json[0].WeatherText | default: "NULL" }}
```

We will also use conditional tags, like `assign` and `if-else`, to personalize the response according to the weather conditions. Here is a simple example we will be using. Refer to [CleverTap Liquid tag](doc:personalize-message-all).

```json
It's {{ Linked["Get Weather"].json[0].WeatherText | default: "NULL" }}
{% assign weather = Linked["Get Weather"].json[0].WeatherText %}
{% if weather == "Sunny" %}
Get 15% off on Sunscreen
{% else %}
Get 10% off on Umbrella
{% endif %} 
```

<Image alt="Preview and Test" align="center" width="75% " border={true} src="https://files.readme.io/848bbe83b0452f35d4c23fa25ef33ce053f0f75b35c4eb3b16bc75a0ef70724d-image.png">
  Preview and Test
</Image>

6. Click **Preview and Test** to confirm that fallback and weather-specific values render correctly.

<Image alt="Push notification" align="center" width="25% " border={true} src="https://files.readme.io/e24b5a7ae27d918710bc0504e7a26a000235a11afea5414c74a9e3d7cefda101-image.png">
  Push notification
</Image>

7. Click **Publish** to send the campaign.

Once live, users will receive highly contextual push notifications tailored to their local weather conditions.

By integrating AccuWeather with CleverTap, you can automate hyper-contextual marketing experiences across campaigns like [Push Notifications](doc:create-message-push), [Email](doc:create-message-email), [In-App Messages](doc:create-message-in-app), or [Web Pop-ups](doc:create-message-web-popup).
