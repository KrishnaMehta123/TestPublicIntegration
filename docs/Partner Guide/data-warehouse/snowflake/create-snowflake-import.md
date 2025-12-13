---
title: Create Snowflake Import
excerpt: >-
  Learn how to import data from Snowflake into CleverTap to enable personalized
  targeting and optimized campaigns.
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

Once your CleverTap Snowflake integration is in place, you can seamlessly import data from Snowflake into CleverTap. To get started, set up your import by specifying your data source and query type and validating your setup.

This document guides you through setting up a new Snowflake import, including query creation and data validation, to ensure smooth and accurate data ingestion.

# Create Import

To begin importing from Snowflake to CleverTap, perform the following steps:

1. Go to *Settings* > *Partners* > *Import center* and click **Create Import**.
2. Select **Snowflake** from the *Create Import* popup.

<Image alt="Create Import" align="center" border={true} src="https://files.readme.io/0eeb72d7b7290f5b8310c21727a832b4f365e5cc8319c9ef96a2b12bb4bc8070-Create_Import.png">
  Create Import
</Image>

3. Under *Configure Import*, add the following details:

<Image alt="Configure Import" align="center" border={true} src="https://files.readme.io/3f51b9caf5b903a92785de33f10517efea3a0b47956bde1c6bc84d254671bf29-Import_Snowflake.png">
  Configure Import
</Image>

<Table>
  <thead>
    <tr>
      <th>
        **Field**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        A unique name to identify the import configuration in CleverTap. Choose a name that reflects the purpose of the import (for example, "User Data Import").
      </td>
    </tr>

    <tr>
      <td>
        Database
      </td>

      <td>
        Select the Snowflake database from the dropdown. Ensure the database has been integrated with CleverTap. For more information, refer to [Database Details](doc:snowflake-configuration#database-details).
      </td>
    </tr>

    <tr>
      <td>
        Query Type
      </td>

      <td>
        Specifies how data is selected from Snowflake for import into CleverTap. Available options are as follows:<li>**SQL**: Select SQL if you need custom control over filtering and joins. For more information on creating SQL queries, refer to [Snowflake’s SQL Reference](https://docs.snowflake.com/en/user-guide/querying-construct-at-runtime).</li><li>**table (Tab)**: Select Table if you directly want to import data from pre-defined data sets.</li>
      </td>
    </tr>

    <tr>
      <td>
        Preview Results
      </td>

      <td>
        Fetches a preview of query results to validate data accuracy before saving the configuration. When you select **Preview Results**, the provided SQL query or table selection is executed on the Snowflake database, and a limited number of rows are fetched to minimize processing time. The retrieved data is displayed, allowing you to validate the query or table selection. If there are any issues, such as syntax errors or access problems, they are highlighted to help with troubleshooting.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Preview Results
>
> Previewing results is solely for validation purposes and does not import any data into CleverTap.

Once you validate your data using *Preview Results*, click **Next** to move on to the mapping step. In this step, map **event data** or **user profile data** from your Snowflake database to ensure accurate data with the datatype is transformed before pushing it to CleverTap. For detailed instructions, refer to [Map Data for Snowflake Import](doc:map-data-for-snowflake-import).
