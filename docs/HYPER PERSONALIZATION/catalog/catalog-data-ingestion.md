---
title: Catalog Data Ingestion
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
## Overview

Catalog data ingestion provides the ability to add more information from a catalog as event properties to an existing event which means you can still receive additional information without updating the app version on the user's device. 

> 👍 Example
>
> When a user adds an item to cart, the product catalog information (e.g., product rating, category, and SKU) can be stored as event properties. These new event properties can be used like any other event property.

# Upload a Catalog

A product catalog lists all items and the information relevant to them. You must upload the catalog in the specified format, so this information can be available in your app. For more information, refer to [Create a New Catalog](https://docs.clevertap.com/docs/catalog#section-create-a-new-catalog).

# Map a Catalog

Map the event to the catalog fields. For more information, refer to [Map Catalog Columns](https://docs.clevertap.com/docs/catalog#section-map-catalog-columns).

> 📘 Note
>
> Catalog mapping is not supported for the items stored in the `Charged.Items` array.

> 👍 Example
>
> A user performs an event *Added to cart* for a product with a product name called *Nike shoe*. In order to fetch additional information for this product from the catalog, you must indicate that this event property called *product name* is the same as the *Name* column in the catalog.

# Add Columns from a Catalog

Add the required columns from a catalog to the event in the [schema](doc:schema) using the following steps:

1. Navigate to *Settings* > *Schema* > *Events* > *Custom events*.
2. Click the desired event properties.
3. Click the **+Property** button and select *Add from catalog*. The *Add properties* window displays. 

<Image title="Catalog_schema_upload_from_catalog.png" alt="Add Properties from Catalog" align="center" src="https://files.readme.io/41aea22b6494a6ef9dfe5e0d55f5af4289ff0da2e72dae8b51594bbac5362399-Image_6.jpeg">
  Add Properties from Catalog
</Image>

4. Select the catalog from the list.
5. Select the columns in the list to add as event properties. 

<Image title="Catalog_map_property.png" alt={562} align="center" width="80% " border={true} src="https://files.readme.io/47dbe37-Catalog_map_property.png">
  Select Properties
</Image>

6. Click the **Add** button. 

> 📘 Map Columns in the Schema
>
> If the catalog is not mapped already, you can still import the columns; however, you will be asked to map the columns in the schema before you can start using them.

7. Navigate back to the *Custom events* page and ensure that none of the events are selected.
8. Click **Publish Events**. 

<Image title="Publish events.png" alt={4980} align="center" border={true} src="https://files.readme.io/e3ab7ba-Publish_events.png">
  Publish Events
</Image>
