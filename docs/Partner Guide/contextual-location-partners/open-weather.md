---
title: OpenWeather
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

[OpenWeather](https://openweathermap.org/) provides fast and elegant access to weather forecasts, nowcasts, and historical data globally. This enables businesses to integrate with [CleverTap](doc:linked-content) for targeted campaigns. CleverTap and OpenWeather integration allows you to fetch the user's location and weather updates in real time and send personalized campaigns to your users. For instance, retail companies can send localized notifications recommending weather-appropriate products such as umbrellas during rainy seasons. This document is a comprehensive guide for integrating OpenWeather with CleverTap.

# Prerequisites

You must have the following for this integration:

- An OpenWeather account 
- API key for OpenWeather. To get the API, contact your OpenWeather account manager.
- A CleverTap account 

> 📘 Note
> 
> Ensure that you are tracking user coordinates (latitude and longitude) as user attributes on CleverTap.

# Integrate CleverTap with OpenWeather

This process involves the following three major steps:

1. [Get the API key from OpenWeather](doc:open-weather#get-api-key-from-openweather).
2. [Set Up CleverTap dashboard](doc:open-weather#set-up-clevertap-dashboard).

## Get API Key from OpenWeather

You need to generate an API key from the OpenWeather dashboard to integrate with CleverTap:

1. Log in to your OpenWeather dashboard. 
2. Select _My API Keys_ from the dropdown list from your account. You can also select the _API keys_ tab directly. 
3. Enter your _API key name_ under the _Create Key_ field and click **Generate**. OpenWeather also creates a default _API key_ when you log in to the dashboard for the first time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bce6db3-generate_KEY_OPENWEATHER.png",
        "",
        "Generate OpenWeather API Key"
      ],
      "align": "center",
      "border": true,
      "caption": "Generate OpenWeather API Key"
    }
  ]
}
[/block]


## Set Up CleverTap Dashboard

To set up CleverTap dashboard:

1. Go to _Settings_ > _Setup_ > _Linked Content_ and click **+ Linked Content**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1437fb1-OpenWeather_Clevertap_Linked_Content.png",
        "",
        "Linked Content Setup"
      ],
      "align": "center",
      "border": true,
      "caption": " Set Up Linked Content"
    }
  ]
}
[/block]


2. Enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Parameters",
    "h-1": "Description",
    "0-0": "API Name",
    "0-1": "Enter the name to uniquely identify your API.",
    "1-0": "Endpoint URL",
    "1-1": "Select **GET** from the dropdown list and use the Open Weather API endpoint URL that most suits your purpose. For our use case, we want to fetch current weather data for the user's location. Enter the following endpoint URL: <https://api.openweathermap.org/data/2.5/weather?lat={{latitude}}&lon={{longitude}}&appid=f2b6d7ac90dcc08639e4118621673bdb&exclude={{part}}>  \n  \nFor more information about OpenWeather's available APIs, refer to [Weather API](https://openweathermap.org/api).  \n  \n**Note**: You must update the API URL based on your OpenWeather subscription. ",
    "2-0": "Parameters",
    "2-1": "Declare the parameters to replace them with the personalized value while running the campaigns/journey. For our use case, we are declaring the following parameters: <li> latitude </li> <li> longitude </li> <li> part </li> Mark _latitude_ and _longitude_ as mandatory fields."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c95d18a-set_up_linked_content_openweather.png",
        "",
        "Set Up Linked Content"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Linked Content"
    }
  ]
}
[/block]


3. (Optional) Click **Test Linked Content** to ensure that the Linked Content is set up correctly. 
4. Fill in the required mapping according to your requirements, or click **Auto-fill Objects with Responses**. Once you do this, click **Test & Save changes** to proceed with the campaign creation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19f08d0-auto-fill_objects_with_response.png",
        "",
        "Auto-Fill Objects with Response"
      ],
      "align": "center",
      "border": true,
      "caption": "Auto-Fill Objects with Response"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f63cb3-OpenWeather_Test__Save_Changes.png",
        "",
        "Test & Save Changes"
      ],
      "align": "center",
      "border": true,
      "caption": "Test & Save Changes"
    }
  ]
}
[/block]


Here is an example of the response: 

```json JSON
{
  "coord": {
    "lon": -94.04,
    "lat": 33.33
  },
  "weather": [
    {
      "id": 803,
      "main": "Clouds",
      "description": "broken clouds",
      "icon": "04d"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 305.36,
    "feels_like": 311.36,
    "temp_min": 303.15,
    "temp_max": 305.36,
    "pressure": 1014,
    "humidity": 62,
    "sea_level": 1014,
    "grnd_level": 1003
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.54,
    "deg": 340
  },
  "clouds": {
    "all": 75
  },
  "dt": 1720188172,
  "sys": {
    "type": 1,
    "id": 6094,
    "country": "US",
    "sunrise": 1720177934,
    "sunset": 1720229345
  },
  "timezone": -18000,
  "id": 4736096,
  "name": "Texarkana",
  "cod": 200
}
```

# Create a Campaign on CleverTap

Once you set up the Linked Content on CleverTap, you can now run personalized campaigns from the CleverTap dashboard. OpenWeather will be available in Push, SMS, Email, WhatsApp, Web Push, and Webhook campaigns. In our case, the retail company wants to send a personalized email campaign recommending weather-appropriate products such as umbrellas during rainy seasons and so on. To do so:

1. Go to _Campaigns_ and click **+ Campaigns**.
2. Select _Emails_ from the list of messaging channels. 
3. Click **Go To Editor** from the What section and select _Email with Rich Media_ template to create an email campaign. 
4. Click the ![](https://files.readme.io/c486f61-Personalization_icon.png) icon and select the _Linked Content_ tab. 
5. Slect the _API_ you configured while setting up the Linked Content on the CleverTap dashboard.
6. Map the API Parameters to attributes in the users' profile and click **Apply**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d4a3c1-image_7.png",
        "",
        "Personalization Set up"
      ],
      "align": "center",
      "border": true,
      "caption": "Personalization Set up"
    }
  ]
}
[/block]


7. Create the campaign message using the Linked Content as shown in the following image: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22151a3-image_6.png",
        "",
        "Map Linked Content to create an Email"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Personalized Email Campaign Using Linked Content"
    }
  ]
}
[/block]


```json
{% if Linked.OpenWeather-Demo.weather[0].main == "Clouds"%}
  Hey! it looks cloudy, are you ready for the monsoons? Avail 50% off on all monsoon gear.
{% else %}
   Avail early bird discounts on all monsoon gear.
{% endif %}
```

8. Define all the campaign sections and click **Publish**. You can also send a test campaign before publishing it to a broader audience.