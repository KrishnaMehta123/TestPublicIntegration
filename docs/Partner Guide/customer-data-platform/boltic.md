---
title: Boltic
excerpt: Customer Data Platform
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

[Boltic](https://boltic.io/), a powerful platform for AI-driven workflows and automation, allows you to seamlessly connect various tools and services for efficient data synchronization and automation. 

Boltic offers two seamless ways to integrate with CleverTap, allowing you to push user profiles and events (custom and predefined) efficiently. You can choose between:

* [API-based Integration (using Webhooks and API calls)](doc:boltic#method-1-api-based-integration) for real-time, event-driven automation.
* [Data Hub Stream integration](doc:boltic#method-2-data-hub-stream-integration) for direct, scalable data synchronization from multiple sources.

Boltic helps centralize user data, automate workflows, and enhance engagement campaigns in CleverTap. Common use cases include:

* **Subscription Management**: Send payment and subscription events (for example, renewals, cancellations, and so on) to CleverTap to drive targeted messaging.
* **Lifecycle Marketing**: Send key lifecycle events (for example, Signup, Login, Purchase, and so on) to CleverTap to trigger automated engagement workflows.
* **E-Commerce Feedback**: Send events to CleverTap after closing a support ticket, enabling feedback collection and engagement.

# Prerequisites for Integration

The following are the prerequisites for Boltic:

* For [API-based Integration](doc:boltic#method-1-api-based-integration):
  * Boltic account with Webhook and API action permissions.
  * CleverTap account with valid **Account ID**, **Passcode**, and **Region**.
* For [Data Hub Stream Integration](doc:boltic#method-2-data-hub-stream-integration):
  * A Boltic account with access to Data Hub.
  * A CleverTap account with appropriate permissions to receive streamed data.

# Integrate Boltic with CleverTap

Boltic offers two methods to integrate with CleverTap, allowing you to push user profiles and event data seamlessly:

* [Method 1: API-based Integration](doc:boltic#method-1-api-based-integration)
* [Method 2: Data Hub Stream Integration](doc:boltic#method-2-data-hub-stream-integration)

## Method 1: API-based Integration

With this method, you can directly transfer event and user profile data using Webhooks and API calls. To set up this integration, perform the following steps:

1. [Create Passcode on the CleverTap Dashboard](doc:boltic#create-passcode-on-clevertap-dashboard)
2. [Send Data to CleverTap (Using Webhooks & API Actions)](doc:boltic##send-data-to-clevertap-using-webhooks--api-actions)


### Create Passcode on CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include the Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

### Send Data to CleverTap (Using Webhooks & API Actions)

Boltic allows you to send user profiles and event data to CleverTap using triggers such as Webhooks, Fynd, Slack, Calendly, and Webflow. These triggers help automate data flow based on predefined conditions.

For example, you want to automate user engagement with CleverTap to run an E-commerce mobile app and want to:

* **Track New User Sign-ups**: Every time new users register, their profile details (such as name, email, and phone number) should be updated in CleverTap to personalize their experience.
* **Capture Purchase Events**: When a user makes a purchase, the event data (such as product ID, price, and currency) should be sent to CleverTap to trigger relevant engagement campaigns such as order confirmations, loyalty rewards, or cross-sell recommendations.

For this specific use case, we will use the Webhook trigger to send real-time data updates to CleverTap, tracking new user sign-ups (user profiles) and capturing purchase data (event data). To do so, follow these steps:


1. Go to *Workflows* on the Boltic dashboard and click **+ Create Workflow** and assign it a unique name.
2. **Set Up a Trigger** to initiate actions when specific criteria are met, streamlining automation processes:
   1. Select *Webhook* from the *Trigger* dropdown.
   2. Click **Webhook** for configuration (refer to the following GIF):
      1. Select the appropriate authentication type from the dropdown.
      2. Enter a test payload in JSON format per the use case. The following are sample JSON payloads for pushing data.
         * Sample Payload for Sending User Profile Data (Track New User Sign-ups)
           ```coffeescript json
           //for pushing user profile
           {
             "payload": {
               "name": "John D",
               "user_id": "1717"
             }
           }
           ```
         * Sample Payload for Sending Event Data (Capture Purchase Events)
           ```coffeescript json
           //for pushing events 
           {
             "payload": {
               "user_id": "1717",
               "event_name": "Product Purchased",
               "properties": {
                 "amount": 499.99,
                 "currency": "USD",
                 "product_id": "98765"
               }
             }
           }
           ```
3. Click **Save** to test and save the trigger.

<Image alt="Set Up a Trigger" align="center" border={true} src="https://files.readme.io/cb7e3928d47e82889cb218e08e3d3d5dff4aa01489e017e066d457f91855ef3b-boltic_step_1_.gif" />

4. **Select the API Action** to send the events or user profiles to CleverTap from Boltic whenever the trigger event occurs. Follow these steps:
   1. Drag the **API** block from the *Helpers*  panel on the left and drop it below the **Webhook** block in the workflow.
   2. Click **API** for configuration:
      1. Set the *HTTP Method* to *POST* to send the events and user profiles to CleverTap.
      2. Enter the following *CleverTap API endpoint URL*, where you need to replace `<region>` with the region of your CleverTap account. To know the region of your account, refer to [API Quick Start Guide](https://developer.clevertap.com/docs/api-quickstart-guide):
         ```
         https://<region>.api.clevertap.com/1/upload
         ```

<Image alt="Select the API Action" align="center" border={true} src="https://files.readme.io/7fa13b1de6b61af8a238de9f75a0599066559dd417f36c5997a962b336a6d1b0-bolt_api_.gif" />

5. Configure *Headers* to connect the CleverTap Account. To do so, perform the following steps:
   1. Enter the required details in the headers to connect the CleverTap account.
      Use the same passcode obtained during the [Create a Passcode on CleverTap Dashboard](doc:boltic#create-a-passcode-on-the-clevertap-dashboard) step.
   2. Add the following key-value pairs in the headers:

| **Header Key**             | **Description**           |
| -------------------------- | ------------------------- |
| **Content-Type**           | `application/json`        |
| **X-CleverTap-Account-Id** | Your CleverTap Account ID |
| **X-CleverTap-Passcode**   | Your CleverTap Passcode   |

<Image alt="Configure Headers" align="center" border={true} src="https://files.readme.io/ec929b2cfeb58893c16e9e7795fa67aa9f21227c1325056b119340409e23bbf6-image.png" />

6. **Configure the Request Body**. Based on your use case, you can send user profiles or events (custom/predefined). Use the following payload structure in the API body:

```json Sending User Profiles
{
  "d": [
    {
      "identity": "{{payload.user_id}}",
      "type": "profile",
      "profileData": {
        "Name": "{{payload.name}}",
        "Email": "{{payload.email}}"
      }
    }
  ]
}
```

```json Send Events
{
  "d": [
    {
      "objectId": "{{payload.user_id}}",
      "type": "event",
      "evtName": "{{payload.event_name}}",
      "evtData": {
        "Product ID": "{{payload.properties.product_id}}",
        "Amount": "{{payload.properties.amount}}",
        "Currency": "{{payload.properties.currency}}"
      }
    }
  ]
}
```

7. Click **Save** to save the API configuration.

<Image alt="Save API configuration" align="center" border={true} src="https://files.readme.io/d933e5fa2afb27527ee712c9a5bf14c37cb246435aee13c110d0a489e8885826-image.png" />

8. Click **Test** to verify the workflow. Check the inputs, outputs, and logs to verify:
   * Successful API requests.
   * Data reflecting accurately in CleverTap.

<Image alt="Test and Publish" align="center" border={true} src="https://files.readme.io/41578b61a7a03a6c636d925dd28786cc375ec2cf10b6010b6e08eccbb97580b2-done_boltic.gif" />

9. Click **Publish** to activate the workflow after testing is successful.

After publishing the workflow for updating user profiles or uploading events, a new user is created, an existing user is updated, or an event is uploaded to the CleverTap dashboard every time a trigger occurs. CleverTap uses the *Identity* field to determine whether the action applies to a new or existing user.

## Method 2: Data Hub Stream Integration

This method leverages Boltic Data Hub to automate event and user profile data flow from various sources to CleverTap.

To integrate using this method, perform the following steps:

1. [Create and Configure Data Stream](doc:boltic#create-and-configure-data-stream)
2. [Install and Verify the Data Flow](doc:boltic#install-and-verify-the-data-flow)

### Create and Configure Data Stream

Setting up a data stream in Boltic allows you to collect, process, and forward data to CleverTap. This method is ideal for handling large-scale event flows without manual intervention. To do so, follow these steps:

1. Go to your Boltic Dashboard and select *Data Hub* > *Streams* from the left navigation panel.
2. Click **+ Create Stream** to start setting up a new data stream.

<Image alt="Create Stream" align="center" border={true} src="https://files.readme.io/7a904e83231aa09949b3086151c011e6002d7613321b910bcfe15898d5485555-image.png" />

3. Select the data source you want to connect from the *Select source* dropdown to create for stream.
4. If the source is not yet configured, click **Add Source** and follow the setup instructions.

<Image alt="Add Source" align="center" border={true} src="https://files.readme.io/8ef27bf0035e195fb31dfe0d8d00beb76b5977abf395ab871f2db3f21a2f69fa-image.png" />

5. For this case, use the *Javascript* Source Integration.

<Image alt="Select type of source" align="center" border={true} src="https://files.readme.io/25ffca6e719736b7ea8099f2dd5b1991caf350833f5ada7c003e8e302eaf7f4b-image.png" />

### Install and Verify Data Flow

Once your stream is configured, the next step is to install the stream snippet at the source and verify that data is successfully flowing to CleverTap. This ensures a seamless integration with real-time event tracking. To do so, follow these steps:

1. From the *Destination* dropdown, select *CleverTap*.
2. If CleverTap is not yet configured, click **Add Destination** and enter your CleverTap account details.

<Image alt="Add Destination" align="center" border={true} src="https://files.readme.io/7b6a90bfe8f7fc36a7d8b908fee4fa22a308dd382fb32df70e29c7efc0453f5b-Screen_Recording_2025-02-19_at_12.02.45_PM_1.gif" />

3. Click **Test and Save** to validate the configuration.
4. After selecting the Source and Destination, click **Create Stream**. The newly created stream will now be visible in the Streams list in Boltic.

<Image alt="Stream" align="center" border={true} src="https://files.readme.io/0be998dc0e975bcd3830edc4c3aa681dc2c1f0d2a2739ccb411dd0282e2d6508-image.png" />

5. Open the stream you created and scroll down to find the *Install the stream snippet on your website* for your selected source. 
6. Follow the installation instructions carefully, as steps vary depending on the source type.

<Image alt="Install the stream snippet on your website" align="center" border={true} src="https://files.readme.io/b627ebfe560bb7edb9cbd12359347de3cd62505b8f8daa5ad080364f488760c6-image.png" />

Once the stream snippet is installed, real-time event data flows from the source to CleverTap.

<Image alt="Stream data" align="center" border={true} src="https://files.readme.io/2018f054d398b7736290e83aed403b782a8b5cf662a7e4a7ab4064e4347cc52f-image.png" />

7. To ensure the data is successfully reflected in CleverTap, go to the CleverTap Dashboard and check if the events and user profiles are updating as expected.

<Image alt="Verify data uploaded in CleverTap " align="center" border={true} src="https://files.readme.io/6d945963834b4cb16e95cb30b30a04ade3ed6a2cf2cc3730d76a6665014a910f-Screen_Recording_2025-02-19_at_12.12.20_PM_1.gif" />

This alternative integration method offers an automated and scalable way to sync user data and events between Boltic and CleverTap, enabling enhanced tracking and engagement workflows.

# FAQs

### What are the key differences between API-based integration and Data Hub Stream integration?

| Integration Type                       | Best For                                        | Pros                                                          | Con                                                                      |
| -------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **API-based (Webhooks & API Actions)** | Real-time event-driven automation               | Provides instant updates and requires a simple setup          | Requires API familiarity and may need rate-limiting                      |
| **Data Hub Stream Integration**        | Bulk data synchronization from multiple sources | Scales well for large datasets and does not require API calls | It may introduce slight latency and require a more complex initial setup |

Choosing the right method:  

* Use **[API-based integration](doc:boltic#method-1-api-based-integration)** for real-time updates.  
* Use **[Data Hub Stream integration](doc:boltic#method-2-data-hub-stream-integration)** for large-scale data synchronization.  

### Why is data not appearing in CleverTap?

Check the following if the data is not appearing in CleverTap:  

* Ensure the **CleverTap API keys (Account ID and Passcode)** are correct.  
* Verify that the **endpoint URL** is correct for API-based integration (`https://<region>.api.clevertap.com/1/upload`).  
* Confirm that the **source is correctly configured** in Boltic for Data Hub Stream integration.  
* Activate the **workflow** after testing.