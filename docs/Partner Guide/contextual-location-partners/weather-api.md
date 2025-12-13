---
title: Weather API
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

[WeatherAPI](https://www.weatherapi.com/) provides real-time and forecasted weather data for any global location. By integrating WeatherAPI with CleverTap, you can:

* **Trigger contextual campaigns** based on local weather
* **Deliver personalized messages** such as umbrella offers on rainy days or sunscreen promos on sunny days
* **Drive higher engagement** through dynamic targeting powered by weather conditions

This document shows you how to configure WeatherAPI in CleverTap using [Linked Content](https://docs.clevertap.com/docs/linked-content) and use it in a Push Notification campaign.

# Prerequisites for Integration

Before integrating WeatherAPI with CleverTap, check the following:

* An active WeatherAPI account
* Your WeatherAPI Key (from the WeatherAPI dashboard)
* Access to the CleverTap Dashboard with admin permissions

# Integrate WeatherAPI with CleverTap

The integration involves the following three important steps:

1. [Generate WeatherAPI Key](doc:weather-api#generate-weatherapi-key)
2. [Configure Linked Content in CleverTap](doc:weather-api#configure-linked-content-in-clevertap)
3. [Configure Personalized CleverTap Campaign](doc:weather-api#configure-personalized-clevertap-campaign)

## Generate WeatherAPI Key

An API key is required to authenticate requests to WeatherAPI. To retrieve the key, perform the following steps:

1. Log in to your [WeatherAPI dashboard](https://www.weatherapi.com/login.aspx).
2. Go to *My Account* > *API Key*.
3. Copy the key. You’ll use this to configure Linked Content in CleverTap.

<Image alt="Weather API Key" align="center" width="75% " border={true} src="https://files.readme.io/d526fb210e15ff6f14966ac60a1a570df21f34bc565dddd33ca8ba9ded3ad34b-image.png">
  Weather API Key
</Image>

## Configure Linked Content in CleverTap

Connect WeatherAPI with CleverTap to fetch weather data dynamically for each user.

1. Go to *Settings* > *Setup* > *Linked Content* on the CleverTap dashboard.
2. Click **+ Linked Content**.
3. Fill in the following values:

| Field           | Value                                                                 |
| --------------- | --------------------------------------------------------------------- |
| Name            | `Weather Lookup`                                                      |
| Method          | `GET`                                                                 |
| Destination URL | `https://api.weatherapi.com/v1/current.json?key=<API_KEY>&q={{city}}` |

Replace `<API_KEY>` with your actual WeatherAPI key. The `{{city}}` parameter will be dynamically mapped from each user's profile property.

4. Click **Test** to preview the API response. You should see an output in JSON, such as:

```json
{
  "location": {
    "name": "Paris",
    "country": "France"
  },
  "current": {
    "condition": {
      "text": "Sunny"
    },
    "temp_c": 25.0
  }
}
```

5. Click **Autofill Objects with Response** to map the JSON fields.
6. Click **Test and Save** to complete the setup.

<Image alt="Configure Linked Content in CleverTap" align="center" border={true} src="https://files.readme.io/425fc186723eb961720acb338b2d91e950eb2ed01dbaa9ff9059dee0315a1e58-2025-09-08_14-23-07_1.gif">
  Configure Linked Content in CleverTap
</Image>

## Configure Personalized CleverTap Campaign

Use the configured Linked Content inside a push notification campaign to dynamically personalize the message based on each user’s local weather. To do so, perform the following steps:

1. Go to *Campaigns*, click **+ Campaign** and select *Push Notifications* as a messaging channel.
2. Configure the *Who*, *When*, and *Where* sections based on qualifying requirements.
3. In the *What* section, click **Personalization** (top-right corner).
4. Select the link content configured in the previous step [Configure Linked Content in CleverTap](doc:weather-api#configure-linked-content-in-clevertap).
5. Map the `city` parameter in the Weather API to the appropriate user property in CleverTap (for example, `{{@Profile.city | default: 'Mumbai'}}`). and click **Apply**.

<Image alt="Personalization Setup" align="center" width="75% " border={true} src="https://files.readme.io/dd8f2cccb341f1267c3253da0f3625fd5555084da618205434512625b24cfb0d-image.png">
  Personalization Setup
</Image>

6. Personalize the *Title* or *Message* field using a Liquid snippet. Following is an example where the conditions defined in the Liquid snippet use the weather API to determine which message to send based on the current weather at the user's location.

```liquid
{% if Linked.WeatherLookup.current.condition.text == "Sunny" %}
🌞 Get 15% off on Sunscreens!
{% elsif Linked.WeatherLookup.current.condition.text == "Rain" %}
🌧️ Special deal on Umbrellas just for you!
{% else %}
🌤️ Enjoy shopping with us today!
{% endif %}
```

Messages can be customized further for weather types such as Cloudy, Storm, and so on. To learn more about Liquid syntax and available personalization tags, refer to [Liquid Tags in CleverTap](doc:personalize-message-all#liquid-tags).

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/852c2fba0499d0f7adeafd5a58393725904706376f3e0fa8e81c035df3a817eb-image.png" />

7. Click **Preview and Test** to validate output against a test profile.

The following is a personalized notification sample based on the user’s local weather data, fetched dynamically using WeatherAPI.

<Image alt="Push Notification" align="center" width="65% " border={true} src="https://files.readme.io/984829e73eb6d0c324f9a76e17096d4cced23129889adf1daf5689526dfe9a44-03a0b40c77607c43a783508588903a8184a956886a79fd4aadbe48a9cf385a5d-image.png">
  Push Notification
</Image>

8. After confirming accurate rendering, click **Publish** to launch the campaign.

Once live, the campaign will automatically personalize notifications based on each user’s real-time weather data.
