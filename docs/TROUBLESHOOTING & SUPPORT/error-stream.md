---
title: Error Stream
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

All errors are displayed on the _Error Stream_ page by count, type, sources, and occurrence times. 

# View Errors

To view errors:

1. Click **Errors** from the main menu, then the _Error Stream_ page displays. 
2. Use the scroll down to select the time period for the errors from the number of days list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30b435b-Error_stream_main.png",
        "View Error Stream.png",
        1365
      ],
      "align": "center",
      "border": true,
      "caption": "Error Stream"
    }
  ]
}
[/block]


3. Click any of the errors to view the error detail. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fdf15f8-Error_stream_detail.png",
        "View Error Details.png",
        1365
      ],
      "align": "center",
      "border": true,
      "caption": "Error Details"
    }
  ]
}
[/block]


4. Click the **+** sign next to an error to see the error trend. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/296e2c1-Error_stream_trend.png",
        "View Error Trend.png",
        1339
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Error Trend"
    }
  ]
}
[/block]


# List of Errors

The list of errors consists of:

| Error                                                                   | Description                                                                                                                                                                                                                                                                                   | Possible Action                                                                                                                                                                             |
| :---------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Mandatory event property not passed; violation handler dropped event    | Event property was declared as mandatory for the said event in the schema. Incoming data did not have the mandatory event property, hence, the event was dropped.                                                                                                                             | <ol> <li>Fix the incoming data from SDK/API to ensure the said. event property is always passed</li> <li>Remove the validation for the said event from the schema.</li> </ol>               |
| Undefined event found and dropped                                       | When schema was published, _Undefined Data Handling_ was set to drop the event. When an event came in for the account which was not defined in the schema, it was dropped.                                                                                                                    | <ol> <li>If the event is valid, define the said event in the schema along with its properties; data will start flowing in.</li> </ol>                                                       |
| Undefined event found and accepted                                      | When schema was published, _Undefined Data Handling_ was set to allow event. When an event came in for the account which was not defined in the schema, it was accepted leading to polluted data.                                                                                             | <ol> <li>If the event is not valid, discard the said event in the schema.</li> <li>Set data handling to drop undefined events to ensure data sanity.</li> </ol>                             |
| Undefined event property found and event dropped                        | When schema was published, _Undefined Data Handling_ was set to drop event when an undefined event property is identified. When an event property came in for the account which was not defined in the schema, the entire event was dropped.                                                  | <ol> <li>If the event property is valid, define the said property in the schema. Event along with the property will start flowing in.</li> </ol>                                            |
| Undefined event property found and event property dropped               | When schema was published, _Undefined Data Handling_ was set to drop the said event property when an undefined event property is identified. When an event property came in for the account which was not defined in the schema, the event property was dropped.                              | <ol> <li>If the event property is valid, define the said property in the schema. Event property will start flowing in.</li> </ol>                                                           |
| Undefined event property found and event property accepted              | When schema was published, _Undefined Data Handling_ was set to accept the said event property when an undefined event property is identified. When an event property came in for the account which was not defined in the schema, the event property was accepted, leading to polluted data. | <ol> <li>If the event property is not valid, discard the said event property in the schema.</li> <li>Set data handling to drop undefined event properties to ensure data sanity.</li> </ol> |
| Mismatched event property data type found and event dropped             | In the schema, the data type for event property was defined. The incoming data did not follow the defined data type. The data type fallback definition was to drop the event.                                                                                                                 | <ol> <li>Update the data type fallback definition to allow the event.</li> <li>Update the data coming from API/SDK to the correct data type.</li> </ol>                                     |
| Mismatched event property data type found and event property dropped    | In the schema, the data type for event property was defined. The incoming data did not follow the defined data type. The data type fallback definition was to drop the event property.                                                                                                        | <ol> <li>Update the data type fallback definition to allow the event property.</li> <li>Update the data coming from API/SDK to the correct data type.</li> </ol>                            |
| Mismatched event property data type found and event accepted            | In the schema, the data type for event property was defined. The incoming data did not follow the defined data type. The data type fallback definition was to allow the event.                                                                                                                | <ol> <li>Update the data coming from API/SDK to the correct data type.</li> </ol>                                                                                                           |
| Maximum event properties for event exceeded                             | Event property limit of 256 for the event exceeded. Properties outside the limit dropped.                                                                                                                                                                                                     | <ol> <li>Remove unwanted properties from the event.</li> </ol>                                                                                                                              |
| Maximum event limit exceeded due to undefined events                    | Event limit for the project exceeded. Events outside the limit dropped.                                                                                                                                                                                                                       | <ol> <li>Remove unwanted events from the project.</li> </ol>                                                                                                                                |
| Event property defined but not used in the last three months            | No instance of a defined event property in the schema found in a 90-day period.                                                                                                                                                                                                               | <ol> <li>Validate incoming data from SDK/API to ensure event is configured correctly.</li> </ol>                                                                                            |
| Unaccepted characters found in event property values                    | Illegal characters found in the event property value.                                                                                                                                                                                                                                         | <ol> <li>Remove the illegal characters from API/SDK configuration.</li> </ol>                                                                                                               |
| Unaccepted characters found in event property keys for undefined events | Illegal characters found in the event property key.                                                                                                                                                                                                                                           | <ol> <li>Remove the illegal characters from API/SDK configuration.</li> </ol>                                                                                                               |
| No event found in last three months                                     | No instance of a defined event in the schema found in a 90-day period.                                                                                                                                                                                                                        | <ol> <li>Validate incoming data from SDK/API to ensure event is configured correctly.</li> </ol>                                                                                            |
| Undefined user property found and dropped                               | When schema was published, _Undefined Data Handling_ was set to drop user property when undefined. When a user property came in for the account which was not defined in the schema, the same was dropped.                                                                                    | <ol> <li>If the user property is not valid, discard the said event in the schema.</li> <li>Set data handling to drop undefined user properties to ensure data sanity.</li> </ol>            |
| Undefined user property found and accepted                              | When schema was published, _Undefined Data Handling_ was set to allow user property when undefined. When a user property came in for the account which was not defined in the schema, the same was accepted.                                                                                  | <ol> <li>If the user property is not valid, discard the said user property in the schema.</li> <li>Set data handling to drop undefined user properties to ensure data sanity.</li> </ol>    |
| Mismatched and user property data type found and dropped                | In the schema, the data type for user property was defined. The incoming data did not follow the defined data type. The data type fallback definition was to drop the user property.                                                                                                          | <ol> <li>Update the data type fallback definition to allow the user property.</li> <li>Update the data coming from API/SDK to the correct data type.</li> </ol>                             |
| Mismatched user property data type found and accepted                   | In the schema, the data type for user property was defined. The incoming data did not follow the defined data type. The data type fallback definition was to accept the user property.                                                                                                        | <ol> <li>Update the data coming from API/SDK to the correct data type.</li> </ol>                                                                                                           |
| Unaccepted characters found for user property values                    | Illegal characters found in the user property value.                                                                                                                                                                                                                                          | <ol> <li>Remove the illegal characters from API/SDK configuration.</li> </ol>                                                                                                               |
| Unaccepted characters in user profile property key                      | Illegal characters found in the user property key.                                                                                                                                                                                                                                            | <ol> <li>Remove the illegal characters from API/SDK configuration.</li> </ol>                                                                                                               |
| Maximum characters exceeded for user property value                     | User property limit for the project exceeded. User Properties outside the limit dropped.                                                                                                                                                                                                      | <ol> <li>Remove unwanted user properties from the project.</li> </ol>                                                                                                                       |