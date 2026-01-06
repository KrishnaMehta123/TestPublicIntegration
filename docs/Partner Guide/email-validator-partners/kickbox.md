---
title: KickBox
excerpt: Email Validator
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[Kickbox](https://kickbox.com) enables businesses to verify email addresses in real time and ensure that only valid, deliverable emails are used in marketing communication. Integrating Kickbox with CleverTap lets you verify user email addresses in real time within _In-App Messages_, helping you display dynamic feedback to users based on email validity.

This integration allows you to:

* Verify and enrich existing email addresses before launching campaigns.
* Prevent messages from being sent to invalid or disposable email addresses.
* Personalize communication based on email verification results.

<Callout icon="🚧" theme="warn">
  #### Support for Integration

  This integration is managed and continuously improved by Kickbox. The CleverTap and Kickbox integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Kickbox](https://kickbox.com/contact/) for support and resolution.
</Callout>

# Prerequisites for Integration

The following are the prerequisites:

* Access to your Kickbox account and dashboard.
* Permission to create and configure API Keys.
* Access to your CleverTap Dashboard with rights to create and manage Linked Content and Campaigns.

# Integrate Kickbox with CleverTap

Integrating Kickbox with CleverTap allows you to verify user email addresses dynamically using Linked Content. When a campaign is triggered, CleverTap calls the Kickbox API in real time to validate the email address associated with each recipient and can adjust messaging accordingly.

The process includes the following three key steps:

1. [Obtain Kickbox API Key](doc:kickbox#obtain-kickbox-api-key)
2. [Configure Linked Content](doc:kickbox#configure-linked-content)
3. [Use Kickbox Verification in Campaigns](doc:kickbox#use-kickbox-verification-in-campaigns)

## Obtain Kickbox API Key

Begin the integration by generating an API Key in Kickbox. This key will authenticate CleverTap requests to the Kickbox API. To do so, perform the following steps:

1. Log in to your Kickbox Dashboard.
2. Go to _Settings_ > _API Keys_.
3. Click **Generate API Key** to create a new key.
4. Assign permissions as required for your use case. For this example, full permissions are granted.

<Image align="center" alt="Obtain Kickbox API Key" border={true} caption="Obtain Kickbox API Key" src="https://files.readme.io/37c1b638e9e07285f2cd8821829f7ccc489440b607e563e0b02a1fc7860846e6-Screen_Recording_2025-07-01_at_1.29.40PM_1.gif" width="75% " />

The API Key acts as your authentication token, allowing CleverTap to securely communicate with Kickbox during each email validation request. For more information about Kickbox response parameters, refer to the [Kickbox API documentation](https://docs.kickbox.com/docs).

## Configure Linked Content

Linked Content allows CleverTap to fetch dynamic data from external APIs at message rendering time. Here, it’s used to query Kickbox and verify the validity of each user’s email before sending a message.

To configure Linked Content:

1. Go to _Settings_ > _Setup_ > _Linked Content_ from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Name**
      </td>

      <td>
        Provide a name for the Linked Content. For example: `Kickbox Email Verification`
      </td>
    </tr>

    <tr>
      <td>
        **Request Type**
      </td>

      <td>
        Select `GET` method.
      </td>
    </tr>

    <tr>
      <td>
        **Endpoint URL**
      </td>

      <td>
        Enter the following endpoint URL: `https://api.kickbox.com/v2/verify?email={{Profile.Email}}&apikey=YOUR_API_KEY`

        * Replace `YOUR_API_KEY` with your actual Kickbox API key.
        * `{{Profile.Email}}` dynamically passes each user’s email to Kickbox for validation.
      </td>
    </tr>
  </tbody>
</Table>

3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "success": true,
  "result": "deliverable",
  "reason": "accepted_email",
  "disposable": false,
  "free": true,
  "email": "example@gmail.com",
  "domain": "gmail.com"
}
```

<Image align="center" alt="Linked Content Setup" border={true} caption="Linked Content Setup" src="https://files.readme.io/4da2809a5c062849472c7c319df6572f5b54b5f0528b0dc2290e63b61a0aa6fc-image.png" width="75% " />

This response confirms that the connection between CleverTap and Kickbox is active and functioning correctly.

4. Click **Test and Save** to complete your Linked Content configuration.

<Image align="center" alt="Test and Save" border={true} caption="Test and Save" src="https://files.readme.io/f3c8d36cb3a3c519913e7ce1264832eb7b72bfda7d84994768ac5441f5834d8c-image.png" width="45% " />

CleverTap can now access the Kickbox API response dynamically within campaigns.

## Use Kickbox Verification in Campaigns

Once Linked Content is configured, you can use Kickbox verification results to show personalized In-App content to users based on whether their email is valid.

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _In-App_ from the list of messaging channels.
2. Define the campaign target segment, qualification criteria, and delivery schedule.
3. Click **Go to Editor** under the _What_ section and perform the following steps:
   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content](doc:kickbox#configure-linked-content).
   3. Map the email parameter to:
      ```
      {{ Profile.Email | default: "NULL" }}
      ```

This mapping ensures that CleverTap passes the user’s email to Kickbox for verification each time the campaign is triggered.

<Image align="center" alt="Personalization Setup" border={true} caption="Personalization Setup" src="https://files.readme.io/e81e3c810f5e9fae180f94c11d62748afd622a71a92bff3aa8c2890d9a33fb56-image.png" width="75% " />

4. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message based on email validity.

```liquid
{% assign emailCheck = linkedcontent.result %}
{% if emailCheck == "deliverable" %}
  Your email address is verified! You’ll receive updates and offers soon.
{% else %}
  The email address you entered appears invalid. Please update your profile to continue receiving notifications.
{% endif %}
```

This allows you to show different text based on whether the user’s stored email address is valid.

<Callout icon="📘" theme="info">
  #### Note

  When using _Linked Content_ responses, extract only the specific fields needed for display to maintain clarity and prevent unnecessary data exposure.
</Callout>

5. Click **Preview and Test** to verify that the response values from Kickbox appear as expected.
6. Once confirmed, click **Publish** to activate the campaign.

### Example Output

The following examples show how the In-App message dynamically changes based on the Kickbox verification result.

* If the email is valid:

<Image align="center" alt="Verified email confirmation message" border={true} caption="Verified email confirmation message" src="https://files.readme.io/bbf5dd74a7c8c68dd28e9d2ce8ce1cb1057415542499dc9ac889b8c78355bb68-image.png" width="35% " />

* If the email is invalid:

<Image align="center" alt="Invalid email prompt" border={true} caption="Invalid email prompt" src="https://files.readme.io/68acbb6106b8caea8cca7475dcdd79cbbb00e26b97412a1edb8365b78012af38-image.png" width="35% " />

The Kickbox-CleverTap integration enables real-time email validation, ensuring clean and reliable data across your campaigns.
