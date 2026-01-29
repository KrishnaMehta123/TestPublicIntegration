---
title: Snowflake
excerpt: >-
  Learn how configuring Snowflake with CleverTap enables data sync for
  personalized engagement and growth.
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

Configuring Snowflake with CleverTap enables seamless data import and export, ensuring synchronization and access to relevant information for analysis, personalized engagement, and data-driven growth.

<Callout icon="📘" theme="info">
  #### Private Beta

  Snowflake is a Private Beta release. Contact your Customer Success Manager for access.
</Callout>

# Quick Start Guide for Existing Users

<details>
  <summary><b>Expand for quick setup if you have previously configured a Snowflake workspace.</b></summary>

  <hr />

  This section is intended for users who already have a configured Snowflake account and are familiar with the CleverTap dashboard.

  ## Prerequisites

  Before you begin, ensure you have the following details:

  * Snowflake Account Identifier
  * Warehouse
  * Database
  * Role (Optional)
  * Schema (Mandatory for exports)
  * Username

  ## Configure Snowflake Credentials in CleverTap

  To set up the Snowflake credentials in CleverTap, perform the following steps:

  1. Go to *CleverTap Dashboard > Settings > Partners > Snowflake*.
  2. Enter the following details: **Account Identifier, Warehouse, Database, Role, Schema and Username**.
  3. Generate the key pair and assign it to your user.
  4. Click **Test Connection** and **Save**

  After setting up the configuration, you can [import](doc:snowflake-import) or [export ](doc:snowflake-export) data from Snowflake into CleverTap.
</details>

# Prerequisites for Integration

If you are setting up Snowflake for the first time, ensure you have the following before proceeding with the CleverTap configuration:

* **CleverTap Access** to configure Snowflake
* **Snowflake Account Details**:
  * Account Identifier: Go to _Admin_ > _Accounts_ in Snowflake and copy the account Identifier from the URL.
  * Role: Must include the necessary permissions for database access and query execution.
  * Warehouse: Use an existing warehouse or create a new one.
  * Database and Schema: Ensure a database and schema are available (existing or newly created)
* **Snowflake User Account Requirements**:
  * Permissions: The user should have read/write access to the specified database and schema.
  * Authentication Method:  
    Choose from the following: Password Authentication and Key Pair Authentication.

    <Callout icon="📘" theme="info">
      #### Key Pair Authentication

      If your organization requires Key Rotation, refer to [Snowflake's Key Rotation Guide](https://docs.snowflake.com/en/user-guide/key-pair-auth#rotating-keys).
    </Callout>

# Set Up Snowflake for Integration

You can set up Snowflake using one of the following ways:

* For new users who need to provision Snowflake resources from scratch: [Create a new Database, Warehouse, User, and Role](doc:snowflake#create-role)
* For users who already have configured resources in Snowflake: [Use existing Snowflake Credentials](doc:snowflake#use-existing-snowflake-credentials)

## Create New Snowflake Setup

If you do not already have a Database, Warehouse, User, and Role configured in Snowflake, you must create them before proceeding. These components are required to ensure CleverTap can securely access, store, and process your data.

To create each resource, perform the following steps:

1. [Create a Database](doc:snowflake#create-database)
2. [Create a Warehouse](doc:snowflake#create-warehouse)
3. [Create a User](doc:snowflake#create-user)
4. [Create a Schema ](doc:snowflake#create-schema): Required only to export data from CleverTap to Snowflake.
5. [Create a Role](doc:snowflake#create-role)

### Create Database

To get your Snowflake data in CleverTap, you first need to create a database. Follow these steps:

1. Log in to your Snowflake account and open a new SQL worksheet.
2. Run the following SQL command to create a database:

   ```sql SQL
   -- Create a new database for CleverTap data storage
   CREATE DATABASE CLEVERTAP_DB;

   -- Verify database creation
   SHOW DATABASES;
   ```

**Expected Output**

```sql
+--------------+------------------+

| name         | created_on       |

+--------------+------------------+

| CLEVERTAP_DB | 2025-02-20 12:00 |

+--------------+------------------+
```

### Create Warehouse

To avoid conflicts with other operations in your cluster, CleverTap recommends that you create a new warehouse just for CleverTap loads. An X-Small warehouse is large enough for most CleverTap customers when they first configure their Snowflake.

Run the following command to create a warehouse:

```sql
-- Create a warehouse for query execution

CREATE WAREHOUSE CLEVERTAP_WH WITH  

WAREHOUSE_SIZE = 'XSMALL'  

AUTO_SUSPEND = 600  

AUTO_RESUME = TRUE;

-- Verify warehouse creation

SHOW WAREHOUSES;
```

<Callout icon="📘" theme="info">
  #### Note

  To avoid extra costs, set `AUTO_SUSPEND` to ~10 minutes on the Snowflake dashboard (or 600 if using SQL) and enable `AUTO_RESUME`.  This ensures efficient usage since Snowflake charges on a [per-second billing model](https://docs.snowflake.com/en/user-guide/warehouses-considerations#automating-warehouse-suspension).
</Callout>

### Create Role

To ensure proper access control, assign a role specifically for CleverTap integration:

1. Create a role for CleverTap integration:
   ```sql SQL
   CREATE ROLE CLEVERTAP_ROLE;
   ```
2. Grant necessary privileges as follows
   * **For importing data to CleverTap**:
   ```sql SQL
   -- Grant required privileges
   GRANT USAGE ON DATABASE CLEVERTAP_DB TO ROLE CLEVERTAP_ROLE;
   GRANT USAGE ON WAREHOUSE CLEVERTAP_WH TO ROLE CLEVERTAP_ROLE;
   GRANT ALL PRIVILEGES ON SCHEMA CLEVERTAP_DB.PUBLIC TO ROLE CLEVERTAP_ROLE;
   GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA CLEVERTAP_DB.PUBLIC TO ROLE CLEVERTAP_ROLE;
   GRANT SELECT, INSERT, UPDATE, DELETE ON FUTURE TABLES IN SCHEMA CLEVERTAP_DB.PUBLIC TO ROLE CLEVERTAP_ROLE;
   ```
   * **For exporting data from CleverTap**:  
     To enable export functionality, CleverTap requires write access to the schema where export tables are created. If you are using the `PUBLIC` schema, the permissions listed above are sufficient.  
     However, if you are using a custom schema, replace the`<schema name>` with the actual schema name and grant the following privileges:
   ```sql
   -- Grant required privileges
   GRANT USAGE ON DATABASE CLEVERTAP_DB TO ROLE CLEVERTAP_ROLE;
   GRANT USAGE ON WAREHOUSE CLEVERTAP_WH TO ROLE CLEVERTAP_ROLE;
   GRANT USAGE ON SCHEMA CLEVERTAP_DB.<schema_name> TO ROLE CLEVERTAP_ROLE;
   GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA CLEVERTAP_DB.<schema name> TO ROLE CLEVERTAP_ROLE;
   GRANT SELECT, INSERT, UPDATE, DELETE ON FUTURE TABLES IN SCHEMA CLEVERTAP_DB.<schema name> TO ROLE CLEVERTAP_ROLE;
   ```

### Create User

To manage access securely, create a dedicated user for the CleverTap configuration by executing the following SQL query:

```sql

-- Create a dedicated user for CleverTap integration

CREATE USER CleverTap_USER WITH DEFAULT_ROLE = CLEVERTAP_ROLE DEFAULT_WAREHOUSE = CLEVERTAP_WH PASSWORD = '<YOUR_PASSWORD>';


Change
25 of 49

Copy

Copy

-- Grant the role to the user

GRANT ROLE CLEVERTAP_ROLE TO USER ClEVERTAP_USER;
```

### Create Schema (for exports)

After creating the database, you must create a schema to organize CleverTap-related objects. This step is required only to export data from CleverTap to Snowflake. To do so, perform the following steps:

1. Ensure you are using the correct database context:

   ```sql SQL
   -- Switch to the CleverTap database
   USE DATABASE CLEVERTAP_DB;
   ```

2. Execute the following SQL command to create a schema:

   ```sql SQL
   -- Create a new schema for CleverTap data
   CREATE SCHEMA ClEVERTAP_SCHEMA;

   -- Verify schema creation
   SHOW SCHEMAS IN DATABASE CLEVERTAP_DB;
   ```

Expected Output

## Use Existing Snowflake Credentials

If you already have Snowflake set up, perform the following steps to find each detail on the Snowflake dashboard.

* [Obtain Your Snowflake Account Identifier](doc:snowflake#obtain-your-snowflake-account-identifier)
* [Find Existing Database](doc:snowflake#find-existing-database)
* [Find Existing Warehouse](doc:snowflake#find-existing-warehouse)
* [Find and Assign Existing Role](doc:snowflake#find-and-assign-existing-role)
* [Find Existing Schema](doc:snowflake#find-existing-schema) (for exports)

### Obtain Your Snowflake Account Identifier

To configure the integration, you need your Snowflake account identifier. Follow these steps to find it:

1. Log in to Snowflake and navigate to **Admin > Accounts**.

2. Click ![](https://files.readme.io/ad0880e14157a8d9ab232c369d6fd326e4dd0d0e41496d08e55da5dea9df94c2-Screenshot_2025-03-03_at_11.28.40_AM_1.png) and select _Manage URL_ from the dropdown and copy the **Account identifier**, which is typically in the following format:

```
https://<organization_name>-<account_id>.snowflakecomputing.com
```

### Find Existing Database

If you need to check for existing databases in your Snowflake account, follow these steps:

1. Log in to Snowflake and open the **Snowflake Web UI**.
2. Select the **Databases** tab from the left panel to view a list of all available databases.
3. Alternatively, run the following SQL command to retrieve the database names:

### Find Existing Warehouse

Instead of creating a new warehouse, you can use an existing one by retrieving the name:

1. Log in to Snowflake and open the **Snowflake Web UI**.
2. Select the **Warehouses** tab from the left panel to view a list of all available warehouses.
3. Alternatively, run the following SQL command to retrieve the warehouse names:

### Find and Assign Existing Role

To verify or assign a role to a user, perform the following steps:

1. Log in to Snowflake and go to _Admin_ > _Users & Roles_.
2. Select the **Users** tab to view all users.
3. Select the CleverTap user and go to the _Privileges_ section.
4. Check the assigned roles and update if necessary using the following SQL command:

### Find existing Schema

To find existing schemas in a specific database that are needed for CleverTap exports, perform the following steps:

1. Log in to Snowflake and open the **Snowflake Web UI**.
2. Select the **Databases** tab on the left panel and select the desired database.
3. Select the **Schemas** tab to view all available schemas within that database.
4. Alternatively, run the following SQL command to retrieve the schema names:

# Set Up CleverTap Dashboard for Integration

To connect Snowflake with CleverTap, go to _Settings > Partners_ > Snowflake from the CleverTap dashboard and select **Add Database** and configure the following:

* [Database Details](doc:snowflake#database-details)
* [User Details](doc:snowflake-configuration#user-details)

## Database Details

Enter the _Database Details_ in the integration setup form. To create or retrieve details from your Snowflake account, refer to [create a new Database, Warehouse, User, and Role](doc:snowflake#create-role)  or [use existing Snowflake credentials](doc:snowflake#use-existing-snowflake-credentials).

<Image align="center" border={true} caption="Database Details" src="https://files.readme.io/c87f29fe4e49eae0b16f46fe7c154934edc8cc4b947601c23f5e6e4174ccddef-snowflake_databse_details.png" />

| Field                | Description                                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Connection name      | A unique name which you will use further to identify your configuration while setting up imports or exports.        |
| Account Identifier   | The unique identifier for your Snowflake account. It usually follows the format:`<organization_name>-<account_id>`. |
| Role                 | The Snowflake role CleverTap uses to connect to the database.                                                       |
| Warehouse            | The compute warehouse for processing queries.                                                                       |
| Database             | The name of the Snowflake database being integrated.                                                                |
| Schema (for exports) | The specific schema within the database that contains the data to be exported into CleverTap.                       |

## User Details

Provide the **Username** and the corresponding credentials (Password or Key) during setup in the CleverTap dashboard. CleverTap supports the following two authentication methods:

* [Key Pair Authentication](doc:snowflake#key-pair-authentication) [Recommended]
* [Password Authentication](doc:snowflake#password-authentication)

### Key Pair Authentication [Recommended]

To generate a Key for Key Pair Authentication, perform the following steps:

1. Select **Key** as your authentication method.
2. Click **Generate Key** to display the public key.
3. Add this public key to your Snowflake database user:
   1. Log in to Snowflake and go to _Users > Public Keys_.
   2. Follow [Snowflake’s key pair setup instructions](https://docs.snowflake.com/en/user-guide/key-pair-auth.html) to attach the public key to the database user.
4. (Optional) Rotate keys using CleverTap's **Regenerate Key** option if your IT policies require periodic key changes. Using the _Edit_ option, go to the same section and click **Regenerate Key** on the CleverTap dashboard. Attach the newly generated public key to your Snowflake database user as an additional RSA key. For more information about this, refer to [Snowflake Key Rotation document](https://docs.snowflake.com/en/user-guide/key-pair-auth.html#rotating-keys).

<Callout icon="📘" theme="info">
  #### Saving Regenerated Key

  * Once you save the connection with the new key, the previous key will no longer be used.
  * If you generate a new key but close the edit form without saving, CleverTap will continue using the existing key, and the newly generated key will be deleted.
  * If the new key is not attached to the Snowflake user before saving, imports and exports may fail.
  * For detailed guidance on setting up and managing key pair authentication in Snowflake, refer to [Snowflake’s Key Pair Authentication Documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth.html).
</Callout>

<Image align="center" border={true} caption="User Credentials - Key" src="https://files.readme.io/c8b490bb84fc69169cb1dd26c268ba5288416467daa9b1b6f252cec89b0e32e1-snowflake_user_credentials_key.png" />

5. Click **Test Connection** or **Save** to start the import or export after adding the details:
   * **Test Connection**: Verifies if the database credentials and setup are correct. A successful test confirms the connection, while a failure prompts you to review your settings.
   * **Save**: Saves the connection details, enabling you to proceed with the data import or export process.
6. After saving the Snowflake Connection, _[create Import](doc:snowflake-import)_ from the _Import Connections_ dashboard or _[Create Export](doc:snowflake-export)_ from the _Export Connections_ .

### Password Authentication

The unique identifier for your Snowflake user account. Find your Snowflake _Username_ and _Password_ in your Snowflake account details.

1. Log in to the **Snowflake** dashboard and go to _Users_ under the _Security_ tab.
2. Set or reset the user password, ensuring it complies with Snowflake password policies.
3. Enter the username and password under the _User Credentials_ section on the CleverTap dashboard.

<Image align="center" border={true} caption="User Credentials - Password" src="https://files.readme.io/6bce82ac0999297f38bdb32d599e99de9748da8d01b395290aa1c36fcdf49a62-snowflake_user_credentials_-_password.png" />

# FAQs

### How can I delete a connection that has running imports?

Go to _Import Connections_, select the connection, click _Delete_, review the list of running imports, and confirm **Delete**.  This will stop all imports that were running before deleting the connection.

### How can I filter import connections?

Use the **Filter** option on _Import Connections_ to refine displayed databases:

* **Connected On**: Select a date range to view connections created within that timeframe.
* **Connected By**: Filter by email IDs of users who created the connections.

### How can I whitelist IPs for CleverTap integration?

To ensure seamless communication between CleverTap and your systems, whitelist the required IP ranges. To access the list of IPs to whitelist for export integrations, refer to [CleverTap IP Ranges](https://developer.clevertap.com/docs/clevertap-ip-ranges#ip-ranges).
