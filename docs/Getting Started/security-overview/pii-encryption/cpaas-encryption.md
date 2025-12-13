---
title: CPaaS Encryption
excerpt: >-
  Learn how CPaaS encryption protects every message exchange between CleverTap
  and CPaaS providers with end-to-end data security.
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

CleverTap supports full payload encryption for outbound engagement messages and inbound callbacks exchanged with Communication Platform as a Service (CPaaS) providers. This feature ensures that sensitive customer data, such as email addresses, phone numbers, and message content, remains protected and compliant with enterprise security standards.

With CPaaS encryption enabled, CleverTap encrypts all engagement payloads before sending them to the CPaaS provider, and the CPaaS provider encrypts all callbacks before sending them back to CleverTap.

CPaaS encryption is currently supported for the following communication channels:

- [Email](doc:cpaas-encryption#email-encryption-setup)
- [SMS](doc:cpaas-encryption#sms-encryption-setup)

CleverTap’s universal CPaaS encryption framework supports any HTTP-based CPaaS integration configured through the Generic HTTP API.

## Encryption Workflow

CleverTap secures communication between its platform and CPaaS providers by encrypting outbound message payloads and decrypting inbound callbacks. This workflow ensures complete end-to-end encryption for all supported channels, _Email_ and _SMS_, throughout message delivery and reporting.

The process includes the following steps:

1. **Encryption Keys**  
   CleverTap generates AES-256 encryption keys and securely shares them with CPaaS providers through a controlled key exchange process. Each key is versioned to ensure secure rotation and backward compatibility.

2. **Outbound Encryption (CleverTap → CPaaS)**  
   CleverTap encrypts the entire outbound message payload before transmitting it to the CPaaS provider through the Generic HTTP API. Each encrypted payload includes the following:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "h-2": "Data Type",
    "0-0": "`ciphertext`",
    "0-1": "Encrypted email content",
    "0-2": "String",
    "1-0": "`X-AES-IV`",
    "1-1": "Initialization vector, sent as a request header",
    "1-2": "String",
    "2-0": "`X-AES-KEY-VERSION`",
    "2-1": "Identifier for the key version used to encrypt  \nthe payload, sent as a request header",
    "2-2": "String"
  },
  "cols": 3,
  "rows": 3,
  "align": [
    null,
    null,
    "left"
  ]
}
[/block]


3. **Callback Encryption (CPaaS → CleverTap)**  
   The CPaaS provider encrypts callback payloads (such as delivery reports, bounce events, or engagement data) before sending them back to CleverTap. CleverTap decrypts these payloads using the key version and IV specified in the callback headers.
4. **Decryption and Processing**  
   CleverTap decrypts the callback data received, validates its integrity, and updates message delivery, engagement metrics, or status reports in real time.

This unified workflow defines how encrypted data is exchanged in both directions, ensuring that all sensitive user and message information remains protected from transmission to reporting.

# Configuration and Key Management

To enable CPaaS encryption, you must configure the encryption keys that secure data exchange between CleverTap and your CPaaS provider. This section explains how to obtain and manage these keys to maintain a secure and reliable encryption framework.

Follow these steps to complete the setup:

1. [Obtain Encryption Keys](doc:cpaas-encryption#obtain-encryption-keys)
2. [Manage Keys](doc:cpaas-encryption#manage-keys)

## Obtain Encryption Keys

Before you enable CPaaS encryption, you must obtain encryption keys that secure all data exchanged between CleverTap and the CPaaS provider. These keys form the foundation of the encryption framework and ensure that each payload, including outbound messages and inbound callbacks, is encrypted and decrypted correctly.

CleverTap manages this process by the following:

- Generating and maintaining AES-256 encryption keys internally.
- Assigning each key a unique UUID-based version identifier.
- Sharing the keys securely with the CPaaS provider through an approved exchange process.
- Ensuring CleverTap and the provider securely store the keys within their environments.

## Manage Keys

CleverTap manages the complete encryption key lifecycle to maintain continuous data protection and compliance with enterprise-grade security standards.

The following are the essential key management practices:

- Keys are stored using CleverTap’s enterprise-grade secret management systems.
- Keys are securely shared with each CPaaS provider during setup.
- Each encrypted payload includes a version identifier that allows CleverTap to fetch the correct key for decryption.

### Key Rotation

CleverTap periodically rotates encryption keys to maintain a high level of security without disrupting service. Each payload’s key version ensures backward compatibility, allowing CleverTap to decrypt messages encrypted with older keys until all in-flight payloads are processed. Key rotation intervals are managed internally by CleverTap to ensure seamless continuity and security compliance.

# Channel-Specific Setup

The Channel-Specific Setup section provides detailed instructions for enabling encryption on each communication channel. It explains configuration fields, authentication options, and example payloads that ensure secure data exchange between CleverTap and CPaaS providers.

Once encryption is enabled, it applies automatically to outbound requests and inbound callbacks, ensuring end-to-end data security.

The setup section of each channel outlines the configuration steps, encryption behavior, and testing procedures required to enable CPaaS encryption.

## Email Encryption Setup

The Email Channel Setup page helps administrators configure authentication and encryption settings for email campaigns. Users can access it under _Settings > Channels > Email > Setup_, where they can define sender details, authentication type, and enable encryption for outbound email payloads.

### Authentication Configuration

Use this section to define sender details and enable encryption for outbound emails.

| Field                                   | Description                                                                              | Required/Optional |
| --------------------------------------- | ---------------------------------------------------------------------------------------- | :---------------- |
| Authentication Type                     | Choose between _No Authentication_ or _Basic Authentication_, depending on the provider. | Required          |
| Default From Name                       | Display name visible to recipients.                                                      | Optional          |
| Default From Email Address              | Sender’s email address (for example, `rg@clevertap.com`).                                | Required          |
| Default Reply-to Email Address          | Address for replies (for example, `chinmay@clevertap.com`).                              | Optional          |
| Email Preference Center                 | Select a preference center (for example, _CleverTap Preference Center_).                 | Optional          |
| Add custom key–value pairs in campaigns | Include metadata or personalization fields.                                              | Optional          |
| Enable encryption                       | Encrypts all outbound email payloads when selected.                                      | Required          |

> 📘 Enabling Encryption for Email
> 
> To ensure all outbound email payloads are securely encrypted, make sure to select the **Enable encryption** before saving your settings.

The following image shows the _Email Setup_ page in the CleverTap dashboard, where users can enable encryption and define authentication settings for their email channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/161f3cae1299cf36dc14d95a24c662ba0b854a5f62f338b1cc0fdcff2ef39810-image.png",
        null,
        "Enable Encryption in Email Setup"
      ],
      "align": "center",
      "border": true,
      "caption": "Enable Encryption in Email Setup"
    }
  ]
}
[/block]


When encryption is enabled, CleverTap encrypts all outbound email payloads using AES-256 before sending them to the CPaaS provider. This ensures message and user data confidentiality.

### Payload Encryption

CleverTap encrypts both outbound email payloads and inbound callbacks using AES-256 symmetric encryption.

**Outbound Request Example (CleverTap → CPaaS)**

When CleverTap sends an encrypted email payload, it follows this process:

1. CleverTap retrieves the active encryption key and generates a random initialization vector (IV).
2. CleverTap encrypts the email content and metadata using AES-256 encryption.
3. CleverTap includes the ciphertext, IV, and key version in the request payload.
4. CleverTap transmits the encrypted payload securely to the CPaaS provider through the Generic HTTP API.

**Encrypted Callback Example (CPaaS → CleverTap)**

When the CPaaS provider sends an encrypted callback to CleverTap:

1. CleverTap identifies the correct key using the `X-AES-KEY-VERSION`.
2. CleverTap decrypts the payload using AES-256 and the provided initialization vector (IV).
3. CleverTap parses message delivery, open, or bounce data and updates campaign analytics accordingly.

## SMS Encryption Setup

The SMS Channel Setup enables administrators to configure authentication and encryption for SMS campaigns.  
Users can access this under _Settings > Channels > SMS > Setup_ where they define provider details, authentication type, and encryption preferences for outbound and callback payloads.

### Provider Configuration

The following table lists the various fields while configuring the provider:

| Field                        | Description                                                   |
| ---------------------------- | ------------------------------------------------------------- |
| Provider                     | Select _Other (Generic)_.                                     |
| Nickname                     | Enter a name for this configuration (for example, _encrypt_). |
| Delivery Report Callback URL | Endpoint for delivery status updates.                         |
| Inbound Message Callback URL | Endpoint for inbound SMS messages (if applicable).            |
| Request Type                 | Select _POST_.                                                |
| HTTP Endpoint                | Enter the CPaaS provider’s endpoint for outbound requests.    |

### Authentication Configuration

Under the _Authentication_ tab, perform the steps below:

1. Choose the authentication type — _No Authentication_, _Basic Authentication_, or _OAuth 2.0._
2. (Optional) Select _Custom Key–Value pairs in campaigns_ to include additional fields.
3. Select the **Enable encryption** to activate AES-256 for outbound requests and accept encrypted callbacks.

> 📘 Enabling Encryption for SMS
> 
> To ensure all outbound SMS payloads are securely encrypted, make sure to select the **Enable encryption** before saving your settings.

The following image shows the _SMS Setup_ page in the CleverTap dashboard, where administrators can configure authentication and enable encryption for SMS campaigns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/92e990e2854c12f76f0141c2822e032840f9fdb4c206fc33fd2f496dcb4bc9ef-image.png",
        null,
        "Enable Encryption in SMS Setup"
      ],
      "align": "center",
      "border": true,
      "caption": "Enable Encryption in SMS Setup"
    }
  ]
}
[/block]


### Payload Encryption

CleverTap encrypts both outbound SMS payloads and inbound callbacks using AES-256 symmetric encryption.

**Outbound Request Example (CleverTap → CPaaS)**

When CleverTap sends an SMS request to the CPaaS provider, Clevertap follows a secure encryption process to protect message data during transmission:

1. CleverTap retrieves the active encryption key and generates a random initialization vector (IV).
2. CleverTap encrypts the message payload using AES-256 encryption.
3. CleverTap includes the ciphertext, IV, and key version in the HTTP request payload.
4. CleverTap transmits the encrypted payload securely to the CPaaS provider.

**Encrypted Callback Example (CPaaS → CleverTap)**

When the CPaaS provider sends an encrypted callback to CleverTap:

1. CleverTap identifies the correct key using the `X-AES-KEY-VERSION`.
2. CleverTap decrypts the payload using AES-256 and the provided initialization vector (IV).
3. CleverTap parses and records delivery or inbound message details in the platform.

### Testing and Validation

After configuration, validate encryption to ensure successful setup and accurate callback processing. Follow the steps below to test and validate the encryption:

1. Send a test SMS from CleverTap.
2. Verify that the CPaaS provider receives an encrypted ciphertext instead of plain text.
3. Confirm that callback payloads from the provider are also encrypted.
4. Ensure that delivery and engagement metrics display accurately after decryption.

# FAQs

### Who manages encryption keys?

CleverTap generates, manages, and securely shares all encryption keys with CPaaS providers.

### Does CleverTap encrypt the full payload?

Yes. The entire outbound and inbound payload is encrypted using AES-256 symmetric encryption.

### Which encryption standard is used?

CleverTap uses AES-256-CBC encryption with a random initialization vector (IV).

### How does key rotation work?

Each payload includes a key version. CleverTap retrieves the corresponding key and decrypts the payload seamlessly, ensuring no service disruption.

### Can other channels use CPaaS encryption?

Encryption is currently available for _Email_ and _SMS._

### Is there a UI to manage keys?

No. Key management is handled internally by CleverTap.