---
title: SurveySparrow
excerpt: Dynamic Content
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

[SurveySparrow](https://surveysparrow.com/) is a survey and feedback automation platform that enables businesses to design, distribute, and analyze surveys across channels. With its intuitive interface, logic branching, and webhook support, SurveySparrow helps organizations capture user feedback and sync it seamlessly with other platforms.

Integrating SurveySparrow with CleverTap enables you to:

- **Collect Data Seamlessly**: Capture user responses from surveys embedded in CleverTap campaigns and send them directly to CleverTap.
- **Update User Profiles in Real Time**: Map survey responses to CleverTap user profile properties using webhooks. For example, when a user selects _Premium Plan_ in a survey, a webhook updates their CleverTap profile with the property `subscription_plan = Premium`.
- **Trigger Personalized Campaigns**: Log survey submissions as events in CleverTap and use them to power segmentation and Flows. For example, if a user answers _Yes_ to a satisfaction survey, CleverTap can trigger a Flow that sends them a referral campaign. If they answer _No_, the Flow can instead send a feedback request.

# Prerequisites for Integration

Check that you have the following before setting up the integration:

- An active SurveySparrow account
- An active CleverTap account with **Project ID** and **Project Passcode**

# Integrate SurveySparrow with CleverTap

The integration involves the following two steps:

1. [Connect SurveySparrow with CleverTap](doc:surveysparrow#connect-surveysparrow-with-clevertap)
2. [Configure CleverTap Campaign](doc:surveysparrow#configure-clevertap-campaign)

## Connect SurveySparrow with CleverTap

Consider an example where you want to collect Name and Email through a contact survey and sync this data with CleverTap. To do so, perform the following steps:

1. Go to the SurveySparrow dashboard and create a new survey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23963d299560473f33d6f8a1e5c7f4169144dee4755dd62c6dcca213c822ab8f-image.png",
        null,
        "Create a New Survey"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Create a New Survey"
    }
  ]
}
[/block]


2. (Optional) Use _URL parameters_ or _global variables_ in the survey link to pass identifiers (for example, Email or Identity from CleverTap) for accurate mapping.  
   - _URL parameters_: Values you append to the survey link itself. For example:  
     `https://surveysparrow.com/survey?email={{Profile.Email}}`  
     These are unique to each survey link and are replaced at runtime with the user’s actual CleverTap profile data.  
   - _Global variables_: Predefined values set at the survey level. They are available throughout the survey and remain the same across responses. For example, setting a global variable `campaign=Summer2025` tags every response from that campaign without relying on the link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7b7bd75c87acc9e38b73106d8c2438543dbc272939547c00d5d071581c7fae74-image.png",
        null,
        "Custom Variables"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Custom Variables"
    }
  ]
}
[/block]


3. Once your form is ready, go to _Integrate_ > _Webhook_ and click **+ New Webhook**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/309b073a955b0e8eef4bdba55bb4dd811a758d560cfe07c4487fdae8aeb73bdc-image.png",
        null,
        "New Webhook"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "New Webhook"
    }
  ]
}
[/block]


4. Configure the webhook as follows:
   1. Callback URL: `https://<your-clevertap-region>.api.clevertap.com/1/upload`
   2. Request Type: _POST_
   3. Add the following headers in your webhook configuration to authenticate the request and ensure CleverTap accepts the payload:

| Header                 | Description                      | Example Value                          |
| ---------------------- | -------------------------------- | -------------------------------------- |
| X-CleverTap-Account-Id | Your CleverTap Account ID        | `"X-CleverTap-Account-Id: ACCOUNT_ID"` |
| X-CleverTap-Passcode   | Your CleverTap Account Passcode  | `"X-CleverTap-Passcode: PASSCODE"`     |
| Content-Type           | Always set to `application/json` | `"Content-Type: application/json"`     |

5. For the _Content_, define your payload. For this example, we will create or update user profiles in CleverTap:

```json
{
  "d": [
    {
      "identity": "{question_1003038259}",
      "type": "profile",
      "profileData": {
        "Name": "{question_1003038258}",
        "Email": "{question_1003038259}"
      }
    }
  ]
}
```

You can map survey fields into the payload by clicking the **?** icon in SurveySparrow’s webhook editor. To update a profile, set the type as `"type": "profile"`. For event, set the type as `"type": "event"`. For more information, refer to [CleverTap’s API documentation](https://developer.clevertap.com/docs/upload-events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/89ccc6e8666ca94e6e227ffc0d44896251132fe7954aa9291a1e20f91e7ce0ed-image.png",
        null,
        "Content Payload"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Content Payload"
    }
  ]
}
[/block]


6. Click **Save Details** to save the webhook.
7. Go to the _Distribute_ tab and copy the survey URL.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4c2380c6d6694c946f2804f9df82d146f136dd4b40565174eb185f8c77b5c524-image.png",
        null,
        "Copy Survey URL"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Copy Survey URL"
    }
  ]
}
[/block]


Use this survey URL in the CleverTap campaign to display the survey to users and capture their responses in real time.

## Configure CleverTap Campaign

Consider an example where you want to show the survey inside a CleverTap In-App Message campaign so users can respond directly within your app. To do so, perform the following steps:

1. Go to the CleverTap dashboard, create a new **In-App Message** campaign (or Email/Web Popup campaign).
2. Configure the campaign. In the _What_ section, select a _Custom HTML Template_ (for example, _Interstitial_).
3. Paste the following snippet into the _Custom HTML_ editor and replace `<survey url>` with the copied SurveySparrow link from Step 7 of [Connect SurveySparrow with CleverTap](doc:surveysparrow#connect-surveysparrow-with-clevertap) :

```html
<iframe src="<survey url>" style="width:100%; height:100%; border:none;"></iframe>
```

4. Click **Preview and Test** to check that the survey loads correctly.
5. Publish the campaign. Your users will receive an In-App message survey as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68dcc3c70d649a9e107fad6bca0dfa22ed4bd952fa44b5ff0c240cc8caba18a5-image.png",
        null,
        "In-App message"
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "In-App message"
    }
  ]
}
[/block]


The responses to the survey will create or update the user profile on the CleverTap dashboard. To view the changes, navigate to _Segments_ > _Find People_ in the CleverTap dashboard. You can search for users by their Email, Identity, Phone Number, or CleverTap ID. Once you locate a user, their updated profile will display all the latest properties and activity captured from the survey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/feadf7567aa54780374aa8f90799f758065ccf18c68e04fcbe7f1aa615e7851d-image.png",
        null,
        "Verify User and Events in CleverTap"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Verify User and Events in CleverTap"
    }
  ]
}
[/block]


# FAQs

### Can I log SurveySparrow responses as events in CleverTap?

Yes. By changing the payload type in the webhook from `"profile"` to `"event"`, you can upload survey submissions as events instead of profile updates.