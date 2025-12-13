---
title: Inkit
excerpt: Direct Mail
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

[Inkit](https://www.inkit.com) enables you to reach and communicate with customers through automated and personalized direct mail campaigns. It allows rendering of paperless documents at scale and validating customer mailing addresses with precision.

With the CleverTap Inkit integration, you can:

- Send personalized Inkit mailers (postcards, letters) to users or segments from CleverTap.
- Trigger document generation based on scheduled campaigns or qualifying user events.
- Deliver paperless communication through automated workflows.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- You must have an Inkit [Account](https://app.inkit.io/), an [API token](https://docs.inkit.com/docs/authentication#how-to-find-the-api-key-or-token-in-the-app), and a [Template ID](https://docs.inkit.com/docs/inkit-postcards-api#api-token-and-template-id) to send requests from CleverTap using webhook.
- You must have an account with CleverTap.

# Integrate Inkit with CleverTap

The integration process involves the following three major steps:

1. [Create a Template in Inkit](doc:inkit#create-a-template-in-inkit)
2. [Create Webhook in CleverTap](doc:inkit#create-webhook-in-clevertap)
3. [Create Webhook Campaign in CleverTap](doc:inkit#create-webhook-campaign-in-clevertap)

## Create a Template in Inkit

Create a reusable document template in Inkit that will be triggered from CleverTap. To do so, perform the following steps:

1. Log in to the Inkit platform.
2. Create or select a template you want to use in your CleverTap campaign.
3. Copy the **Template ID** from the URL. For example, in the URL:

```
< https://app.inkit.io/#/templates/design/<The_Template_ID> >
```

Refer to the [Inkit API documentation](https://docs.inkit.com/docs/api-endpoints) for guidance on template usage.

## Create Webhook in CleverTap

Connect CleverTap with Inkit by setting up a webhook that sends user-specific data to Inkit's API. To do so, perform the following steps:

1. Go to _Settings_ > _Channels_ > _Webhook_ in the CleverTap dashboard.
2. Click **+ Webhook** to add a new webhook.
3. Enter the following configuration:

| Field        | Value                                                                            |
| ------------ | -------------------------------------------------------------------------------- |
| Name         | Enter the nickname for your webhook to identify it uniquely. For example:`Inkit` |
| HTTP Method  | Select `POST`                                                                    |
| Endpoint URL | Paste the URL `https://api.inkit.com/v1/generate`                                |
| Content-Type | `application/json`                                                               |
| Headers      | `X-Inkit-API-Token: <API_token>`                                                 |

You can check out the [Inkit API documentation](https://docs.inkit.com/docs/api-endpoints) to learn about various endpoints, their uses, and the steps to set them up.

4. Click **Save** to register the webhook.

## Create Webhook Campaign in CleverTap

Trigger Inkit document generation based on user activity by configuring a Webhook Campaign in CleverTap. To do so, perform the following steps:

1. Go to _Campaigns_ > _+ Campaign_ > _Webhook_.
2. Select the Webhook configured in [Create Webhook in CleverTap](doc:inkit#create-webhook-in-clevertap).
3. In the _What_ section, under the Webhook Content section, select the Content Format as `JSON` and click the **Custom body** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ab0b354bf07f27edb8b2b69e846047973875036d02d27c478a4b3bd059a77b4-image.png",
        null,
        "Webhook Content"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Webhook Content"
    }
  ]
}
[/block]


4. Paste the following JSON payload:

```json
{
 "merge_parameters": {
   "Name": "{{ Profile.name | default: "test" }}",
   "email": "{{ Profile.Email | default: "-" }}",
   "phone number": "{{ Profile.Phone | default: "-" }}"
 },
 "template_id": "<id of the template you created at the start>",
 "description": "test"
}
```

Use the personalization toolbar `{`, `{{`, or `@` to dynamically populate user attributes. For more information about all the different types of payload Inkit supports for various use cases, refer to this doc [here](https://docs.inkit.com/reference/post_v1-generate-1).

5. Click **Preview and Test** to validate the setup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3226d69648a7889c7e617a6169797aff8f060098d9e7170c7e7e7a7fb33be0b1-2d2e9f55aa0bf4ce79a939757630cae0c292d6de50bd2d83f2e223deedd59768-image.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


6. Check the Inkit dashboard to confirm that the data has been received and processed under the _History_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dc0933d91ccd6ca65a6e40b22344708a266163162c21ded699488140121f2f86-inkits.png",
        "",
        "Verify the data on Inkit"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Verify the data on Inkit"
    }
  ]
}
[/block]


7. Once validated, click **Publish** in CleverTap.

By integrating Inkit with CleverTap, you can seamlessly extend your engagement strategy beyond digital channels, automating timely, personalised direct mail campaigns that resonate with your users at scale.