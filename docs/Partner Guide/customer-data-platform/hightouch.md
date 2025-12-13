---
title: HighTouch
excerpt: Customer Data Platform
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

[HighTouch](https://hightouch.com/), a modern data integration platform, enables you to sync customer, product, or proprietary data from your warehouse to any app you choose.  The CleverTap and HighTouch integration allows seamless syncing of customer data from your data warehouse to CleverTap. This ensures data consistency and helps deliver superior customer experiences.

With this integration, you can:

- Sync user data from your data warehouse into CleverTap to create targeted, personalized campaigns.
- Sync customer events from HighTouch to CleverTap, ensuring your events are always up-to-date and consistent.
- Enhance user engagement by integrating data from other touchpoints, helping you deliver richer, more relevant experiences.

# Prerequisites for Integration

The following are the prerequisites for integration with HighTouch:

- Ensure you have access to your HighTouch account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by HighTouch. The CleverTap and HighTouch integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [HighTouch](mailto:support@hightouch.io) for support and resolution.

# Integrate HighTouch with CleverTap

The integration process involves the following three steps:

1. [Set Up CleverTap As Destination](doc:hightouch#set-up-clevertap-as-destination).
2. [Create a Model to Sync Data with CleverTap](doc:hightouch#create-a-model-for-data-synchronization).
3. [Synchronize Data with CleverTap](doc:hightouch#synchronize-data-with-clevertap).

## Set Up CleverTap As Destination

Configure CleverTap to HighTouch for data transfer and enable data flow between them.

1. Go to _Integrations_ > _Destination_ on the HighTouch dashboard.
2. Select **Add destination**, search for _CleverTap_ and select it as your _Destination_.
3. Enter the following details:

| Field            | Description                                                                                                                                                                                                                                    |
| :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Locate the Project ID under _Settings_ > _Project_. from the CleverTap                                                                                                                                                                         |
| Account Passcode | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                                 |
| Region           | Locate _Region_ for the API endpoint you want to select under Settings > Project. To find the API endpoint for your region, refer to, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

4. Test the connection, assign a name to this _Destination_, and click **Finish** to save the configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c08f3c7825ea39b3c9417294484aa599a3961c1913a17c6accb61bbe01b31215-hig_gg.gif",
        "",
        "Set Up CleverTap As Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Destination"
    }
  ]
}
[/block]


## Create a Model for Data Synchronization

Create a model to define how data is prepared and structured before syncing it to CleverTap as the destination. To do so:

1. Go to _Activations_ > _Models_ and click **Add Model**.
2. Select the required Data Source and define and finalize the model. For more information, refer to [Creating Models](https://hightouch.com/docs/models/creating-models).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e16b2e36b8c68a20a5894eaa27af0d1b035e3f24fa965ca46d8415ccdabb1723-hightouch_gif_1.gif",
        "",
        "Add Model"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Model"
    }
  ]
}
[/block]


## Synchronize Data with CleverTap

With your model and destination ready, you can sync data to CleverTap. For example, in an e-commerce use case, you can configure and synchronize transaction data, such as the _Charged_ event. This ensures accurate data flow and improves user engagement.

### Sync Data

1. **Set Up the Sync**

   1. Go to _Activations_ > _Models_ from the HighTouch dashboard and locate the model you created.
   2. Click **Add Sync**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e1b91bb7274fcb365f908560377d5e89351349a8113f2e7323accab4b5f866c-image.png",
        null,
        "Add Sync"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Sync"
    }
  ]
}
[/block]


2. **Select CleverTap and Data Type**
   1. Select _CleverTap_ as your sync destination.
   2. Choose the type of data to sync:

| Sync Option  | Description                                                          | Examples                                   |
| ------------ | -------------------------------------------------------------------- | ------------------------------------------ |
| **Objects**  | Sync user profiles with personal and behavioural attributes.         | Name, Email, Phone Number                  |
| **Events**   | Record user actions such as purchases or app interactions as events. | Transaction events such as Charged events. |
| **Segments** | Maintain user groups dynamically for campaigns or targeting.         | Excluded or targeted audiences.            |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23c9781f8c7f732f7c26acfaef65998a3f29c91b72a32b4ab063b0945decb880-image.png",
        null,
        "Configure Sync to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Sync to CleverTap"
    }
  ]
}
[/block]


3. **Map Data Fields**
   1. Match fields from your source to CleverTap:
      - `transaction_id` → `txnId`
      - `amount` → `amount`
      - `currency` → `currency`
      - `items` → `items` (e.g., `[{"name": "Product 1", "price": 50.25, "quantity": 1}]`)
   2. Add custom fields such as `payment_method` for more insights.
   3. Match your primary key (for example, `user_id`) with CleverTap’s Global Object ID. Enable profile creation for unmatched users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73a259039a9d9d0cb9ce54173b966a8c63b89afe46bdf8ccf1e41d6b48ecd07e-image.png",
        null,
        "Mapping fields"
      ],
      "align": "center",
      "border": true,
      "caption": "Mapping Fields"
    }
  ]
}
[/block]


4. **Test the Sync**. Run a test to ensure:
   - Correct mapping of user profiles and data fields.
   - Proper formatting for complex fields such as `items`.
   - No errors during sync.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1074693541a648cb1377f7534a6a91af41a1757f26114b6f5694b21ac715858d-image.png",
        null,
        "Testing Sync"
      ],
      "align": "center",
      "border": true,
      "caption": "Testing Sync"
    }
  ]
}
[/block]


5. **Verify Data in CleverTap**. Log in to the CleverTap dashboard and verify the following:
   - Synced events under **Events** (for example, Charged).
   - Accurate mapping of fields such as `txnId`, `amount`, and `items`.
   - Events linked to the correct user profiles.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f460d33d5dac404d1e6cd8f8efc871fea195f5fa561077dc5c8993403d404447-image.png",
        null,
        "Verify in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Verify in CleverTap"
    }
  ]
}
[/block]


# Troubleshooting and Best Practices

Here are the best practices to ensure smooth integration and optimize the performance of your CleverTap and HighTouch integration:

- Double-check credentials for both HighTouch and CleverTap connections.
- Ensure accurate field mapping to avoid data inconsistencies.
- Always test sync configurations before executing live syncs.