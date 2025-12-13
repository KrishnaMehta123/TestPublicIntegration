---
title: Qualtrics
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

[Qualtrics](https://www.qualtrics.com) is a Customer Experience Management (CXM) platform that helps organizations collect and analyze customer insights. The integration with CleverTap enables automated distribution of Qualtrics surveys when users perform specific actions in your app or website.

With this integration, you can:

- Automatically trigger Qualtrics survey distributions based on CleverTap events.
- Configure survey payloads using user-specific data via Liquid tags.
- Track feedback loops directly tied to user behavior.

# Prerequisites for Integration

The following are the prerequisites for Qualtrics:

- A valid **Qualtrics API Key** and access to the **Qualtrics XM Directory**.
- Access to the **CleverTap dashboard** with permission to configure Webhook campaigns.

# Integrate Qualtrics with CleverTap

The integration process involves the following two major steps:

1. [Create Qualtrics Distributions via CleverTap](doc:qualtrics#create-qualtrics-distributions-via-clevertap).
2. [Create Webhook Campaign](doc:qualtrics#create-webhook-campaign).

## Create Qualtrics Distributions via CleverTap

This integration is enabled using CleverTap’s Webhook Campaigns, which allow you to send Qualtrics survey distribution payloads to targeted users.

### Configure Webhook in CleverTap

Set up a Webhook in CleverTap to send POST requests to the Qualtrics API whenever a user triggers a defined event.

> 🚧 Note
> 
> Contact [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new) to enable the Webhook channel on your account before proceeding.

To set up the Webhook:

1. Go to _Settings_ > _Channels_ > _Webhook_ in the CleverTap dashboard. Click **+ Add Webhook**.
2. Enter a name for the Webhook.
3. Set the _HTTP method_ to `POST`.
4. In the _Webhook URL_, enter:

   ```
   https://<yourdatacenterid>.qualtrics.com/API/v3/distributions
   ```

   Replace `<yourdatacenterid>` with the actual data center ID. You can find it in [Qualtrics Base URL](https://api.qualtrics.com/guides/get-started/).
5. Add the following headers:

| Key            | Value                      |
| :------------- | :------------------------- |
| `Content-Type` | `application/json`         |
| `X-API-TOKEN`  | `<Your Qualtrics API Key>` |

6. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8cd5b3f4eaf218399ab5bf05bc4c51ba3f0cffbe4d84f2cb726cb4430781bfa3-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true
    }
  ]
}
[/block]


Refer to the [Qualtrics API documentation](https://api.qualtrics.com/573e3f0a94888-create-distribution) for more information.

## Create Webhook Campaign

Create a Webhook campaign to distribute personalized Qualtrics surveys based on real-time user actions captured in CleverTap. To do so, follow these steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Webhook_ from the list of messaging channels.
2. Under the _What_ section, select the Webhook created in the [Configure Webhook in CleverTap](doc:qualtrics#configure-webhook-in-clevertap) section.
   - Select **JSON** as the content format.
   - Select **Custom Body**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ecb2568f744869aad55de0a83e8464e50ff5a3440212253f0e2b01b582af2bdd-image.png",
        null,
        "Webhook Content"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Webhook Content"
    }
  ]
}
[/block]


3. In the **Webhook Content**, paste the following sample payload:

```json
{
 "message": {
   "libraryId": "UR_1M4aHozEkSxUfCl",
   "messageId": "MS_0Vdgn7nLGSQBlYN",
   "messageText": "Example Message Text"
 },
 "recipients": {
   "contactId": "{{ Profile.QualtricID | default: 'test' }}"
 },
 "header": {
   "fromEmail": "apiexample@qualtrics.com",
   "replyToEmail": "apiexample@qualtrics.com",
   "fromName": "Test Name",
   "subject": "Example Subject"
 },
 "surveyLink": {
   "surveyId": "SV_cHbKMOdeT8NetF3",
   "expirationDate": "2025-02-24T14:15:22Z",
   "type": "Individual"
 },
 "embeddedData": {
   "property1": "string",
   "property2": "string"
 },
 "sendDate": "2025-02-24T14:15:22Z"
}
```

You can dynamically personalize values using [Liquid tags](doc:personalize-message-all#liquid-tags) (`{{ }}`). For example, `{{ Profile.QualtricID }}` picks the Qualtrics ID associated with the user.

4. Click **Preview and Test** to validate the payload and campaign behavior.
5. If everything works as expected, click **Publish**.