---
title: API Encryption
excerpt: >-
  Learn how PII Encryption for API protects sensitive API payloads in transit
  using HPKE, without changing existing API behavior.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

CleverTap provides API Encryption to protect sensitive data during transmission between your systems and CleverTap. This capability goes beyond standard transport-layer security by encrypting API request and response payloads in addition to HTTPS/TLS.

The feature is designed for customers operating in highly regulated or security-sensitive environments where TLS alone does not meet internal or regulatory requirements. It preserves existing API contracts, schemas, limits, and performance expectations while adding a layer of protection for data in transit.

Encryption is applied only during transmission and does not affect how data is processed or stored after ingestion. Encrypted and plaintext API requests can coexist during adoption, and encryption can be enabled without downtime or changes to existing integrations.

# Prerequisites

Before integrating API Encryption, check if the following prerequisites are met:

**Key Exchange**

* API Encryption requires a public key exchange between you and CleverTap.
* CleverTap provides a public key to encrypt API request payloads.
* You provide a public key to encrypt API response payloads.
* Each party securely stores its private key and does not share it.

**Feature Enablement**

API Encryption must be enabled on your CleverTap account before encrypted requests are accepted.

<Callout icon="📘" theme="info">
  To enable this feature, contact your Customer Success Manager.
</Callout>

# End-to-End API Encryption Workflow

API Encryption protects data in transit by encrypting API payloads before they leave the customer’s system and decrypting them securely within CleverTap. The exact mechanism applies in reverse for encrypted responses.

This section explains how CleverTap protects API requests using hybrid encryption, combining the speed of symmetric encryption with the security of public key cryptography.

1. [Customer Encrypts the Payload with an Ephemeral Key](doc:api-encryption-in-transit#customer-encrypts-the-payload-with-an-ephemeral-key)
2. [Customer Sends the Encrypted Request](doc:api-encryption-in-transit#customer-sends-the-encrypted-request)
3. [CleverTap Processes the Encrypted Request](doc:api-encryption-in-transit#clevertap-processes-the-encrypted-request)
4. [CleverTap Encrypts the API Response](doc:api-encryption-in-transit#clevertap-encrypts-the-api-response)
5. [Customer Decrypts the API Response](doc:api-encryption-in-transit#customer-decrypts-the-api-response)

The following image shows the API encryption workflow:

<Image align="center" alt="Diagram titled _End-to-End API Encryption Workflow_ showing how encrypted API communication works between a customer and CleverTap. The customer encrypts the API request using CleverTap’s public key and sends it to CleverTap. CleverTap decrypts the request using its private key, processes the data, then encrypts the response using the customer’s public key. The encrypted response is returned to the customer, who decrypts it with their private key to restore the original data." border={true} caption="End-to-End-API Encryption Workflow" src="https://files.readme.io/f027c56e77e8493ec24db17c40a9d6a08d5c650848edc2742320da7de9629d04-image.png" />

## Customer Encrypts the Payload with an Ephemeral Key

Before sending an API request, the customer encrypts the request payload using an ephemeral symmetric key generated specifically for that request. This one-time encrypted key, which contains the API payload, is further encrypted using CleverTap's public key and shared with CleverTap.

The one-time key encrypts the entire API payload, converting the original JSON data into encrypted binary content. As symmetric encryption is computationally efficient, this step works well even for large payloads and high-throughput API usage, without introducing performance overhead.

At the end of this step, the following happens:

* The API payload is fully encrypted using an ephemeral symmetric key.
* The one-time key is further encrypted by CleverTap's public key.
* The plaintext payload is no longer exposed and is ready for secure transmission.

This step ensures sensitive data is protected before it leaves the customer’s environment, laying the foundation for payload-level security in the encryption workflow. For more information on the keys, refer to [Key Management](doc:api-encryption-in-transit#key-management).

<Callout icon="📘" theme="info">
  **Header-Based Encryption Control**

  Encryption is applied only when explicitly requested through HTTP headers. Requests are processed as encrypted only when the following headers are present.

  * **Content-Type**: `application/octet-stream+hpke`
  * **Accept**: `application/octet-stream+hpke`

    For more information, refer to [API Encryption (In-Transit) - Integration and Reference](https://staging.docs.dev.clevertap.net/docs/api-encryption-in-transit-integration-and-reference).
</Callout>

## Customer Sends the Encrypted Request

The encrypted payload is sent to CleverTap as a single binary request. The request explicitly indicates that the payload is encrypted through the required headers, allowing CleverTap to process it correctly. While in transit, the payload remains opaque and unreadable to intermediaries, preventing sensitive data from being exposed at the network level.

## CleverTap Processes the Encrypted Request

When CleverTap receives the encrypted request, it automatically decrypts it using CleverTap's _private key_ and processes it.

* CleverTap detects that the incoming request is encrypted.
* The payload is decrypted internally using CleverTap’s private key, and it is further decrypted using the ephemeral key.
* The decrypted request, which contains the actual payload, is processed.

This approach preserves existing API behavior for both encrypted and plaintext requests.

## CleverTap Encrypts the API Response

After processing the request, CleverTap encrypts the API response using the _customer’s public key_. CleverTap handles response encryption as follows:

* Encrypts the response payload before it leaves CleverTap.
* Allows only the customer holding the corresponding private key to decrypt the response.
* Uses the same payload-only encryption approach as request encryption.

## Customer Decrypts the API Response

The customer uses the corresponding _private key_ to decrypt the encrypted response. No sensitive payload data is transmitted in plaintext at any point in this workflow.

After decryption, the customer does the following:

* Restores the original response payload.
* Receives the response in the standard API format.
* Requires no additional processing beyond decryption.

# Key Management

API Encryption uses public-key cryptography to protect API payloads and clearly define ownership boundaries for encryption and decryption.

## Key Types

The following are the two types of keys involved in the encryption and decryption processes:

**Public Keys**

* CleverTap's public keys are shared with customers to download and use to encrypt API requests.
* Customer-managed pubic keys are shared with CleverTap to encrypt API responses.

**Private Keys**

* CleverTap's private keys are used to decrypt the API requests sent by the customer.
* Customer-managed private keys are used to decrypt the API responses sent by CleverTap.

<Callout icon="📘" theme="info">
  **Key Roles**

  * Customer private keys never leave the customer’s environment and are never shared with CleverTap.
  * CleverTap does not request, store, or use customer private keys at any point in the encryption or decryption process.
  * CleverTap stores its private keys in encrypted form.
</Callout>

## Key Validation

All public keys are validated before use for encryption or decryption. This validation ensures that only supported and compatible keys are accepted, reducing the risk of runtime failures.

## Key Rotation

CleverTap rotates encryption keys on a fixed schedule to maintain strong security hygiene. Keys are rotated once every year, and rotation is handled automatically without impacting API availability or existing integrations.

# Backward Compatibility

API Encryption is designed to preserve full backward compatibility with existing integrations. All APIs continue to accept plaintext requests by default, and encrypted and plaintext requests can coexist within the same account. Existing authentication, authorization, validation logic, and API contracts remain unchanged. Encryption can be introduced incrementally while existing API integrations remain unchanged.

# API Behavior

All existing API constraints remain unchanged, including the following:

* Request and response schemas
* Payload size limits
* Rate limits and throttling rules
* Batch size and ingestion limits
* Timeout behavior

API Encryption functions strictly as an additional security layer. For more information, refer to [API Encryption (In-Transit) - Integration and Reference](https://staging.docs.dev.clevertap.net/docs/api-encryption-in-transit-integration-and-reference).

# Frequently Asked Questions

### Does enabling API Encryption require changes to existing integrations?

No. Existing API integrations continue to work unchanged, and plaintext requests are accepted by default.

### Does payload-level encryption change API limits or performance?

No. API schemas, limits, and performance behavior remain unchanged.

### Is encrypted data stored differently inside CleverTap?

No. Encryption applies only during transmission and does not affect data storage or processing.
