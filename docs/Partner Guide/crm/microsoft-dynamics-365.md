---
title: Microsoft Dynamics 365
excerpt: Customer Relationship Management
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Integrate [Microsoft Dynamics 365 Customer Insights](https://www.microsoft.com/en-gb/dynamics-365/products/customer-insights) with CleverTap to import customer segments as user profiles and drive personalized engagement. When a segment is exported from Dynamics, each user is identified in CleverTap using their unique identity fields. If a matching profile already exists, it is updated with the latest data; if not, a new user profile is created. Once imported, these profiles can be targeted using CleverTap’s engagement channels, such as push notifications, email, in-app messages, and more. Follow the steps below to establish the connection and configure data exports from Microsoft Dynamics 365 Customer Insights to CleverTap:

* [Set Up the Connection](doc:microsoft-dynamics-365#set-up-the-connection)
* [Configure an Export](doc:microsoft-dynamics-365#configure-an-export)
* <Image alt="Microsoft and CleverTap Integration" align="center" border={true} src="https://files.readme.io/46b042268a28ae49b3147a196e89bde849f7026615cafa493fb484caa770b71b-Microsoft_Dynamics_CleverTap.png">
    Microsoft and CleverTap Integration
  </Image>

## Prerequisites

Before configuring the integration, ensure you meet the following requirements:\
**CleverTap Dashboard**:

| Field            | Description                                                                                                                                                                                                                              |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under *Settings* > *Project* from the CleverTap dashboard.                                                                                                                                                         |
| Account Passcode | Locate the Passcode under *Settings* > *Project* from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region           | Locate *Region* for the API endpoint you want to select under *Settings* > *Project*. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

**Microsoft Dynamics 365 Dashboard**

To configure the integration, you must have Administrator permissions in Customer Insights on the Microsoft Dynamic 365 dashboard.

## Set Up the Connection

To enable future data exports, set up a secure connection from Microsoft Dynamics to CleverTap using your Region, Project ID, and Account Passcode mentioned in the [Prerequisites](doc:microsoft-dynamics-365#prerequisites)  section.

1. In your Microsoft Dynamics 365 Customer Insights dashboard, navigate to *Admin > Connections*.
2. Click **Add connection**.
3. From the list of available connectors, choose **CleverTap**.
4. In the *Display name* field, enter a meaningful name for the connection.
5. In the *Who can use this connection* section, specify access control:

   * By default, only Administrators can use the connection.
   * To allow contributors, refer to [Allow Contributors to use a connection for export documentation](https://learn.microsoft.com/en-us/dynamics365/customer-insights/data/connections#allow-contributors-to-use-a-connection-for-exports).
6. Enter the Region, Project ID, and Account Passcode from your CleverTap account. For more details, refer to the [Prerequisites](doc:microsoft-dynamics-365#prerequisites)  section.
7. Review the [data privacy and compliance terms](https://learn.microsoft.com/en-us/dynamics365/customer-insights/data/connections#data-privacy-and-compliance), check *I agree*, and click **Connect** to establish the integration.
8. Once connected, select **Add yourself as export user** and authenticate using your Customer Insights credentials.
9. Click **Save** to complete the setup.

## Configure an Export

After establishing the connection, define what customer data should be exported from Dynamics into CleverTap and how it should be mapped. Ensure you have permission to configure this connection type. For more details, refer to the [Microsoft Dynamics documentation](https://learn.microsoft.com/en-us/dynamics365/customer-insights/data/export-destinations#set-up-a-new-export)  about setting up new exports.

1. Navigate to *Data > Exports*.
2. Click **Add export** to create a new export configuration.
3. In the *Connection for export* field, select the **CleverTap** connection you configured.
4. Under the *Data matching* section, map the customer identity fields in CleverTap, which can include the following:

   * **Identity**: A unique identifier for the user, such as an email, phone number, or custom ID. This field is mandatory for identifying users.

   * **Email**: The user's email address, used for communication and as an identifier. 

   * **Phone Number**: The user's phone number in international format (e.g., +14155551234), used for communication and as an identifier.

   * **Name**: The full name of the user, used for personalization in messages. 

   * **First Name**: The user's first name used for personalized greetings and messages.

   * **Last Name**: The user's last name, used for personalization and identification.\
     Refer to [User Profiles](https://developer.clevertap.com/docs/concepts-user-profiles)  CleverTap documentation for more detailed information.
5. Click **Save** to store the export configuration.

Saving an export does not immediately transfer data. The export will run during each [scheduled refresh](https://learn.microsoft.com/en-us/dynamics365/customer-insights/data/schedule-refresh) or when you [export data on demand](https://learn.microsoft.com/en-us/dynamics365/customer-insights/data/export-destinations#run-exports-on-demand).

This integration ensures that customer segments from Microsoft Dynamics are automatically ingested as user profiles in CleverTap. These profiles become immediately available for engagement through CleverTap’s messaging channels, enabling timely, personalized, and contextual communication across platforms.
