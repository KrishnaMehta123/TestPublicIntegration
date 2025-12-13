---
title: Manage Personal Information
excerpt: >-
  Understand different ways in which CleverTap protects end-user personal
  information.
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

Personally Identifiable Information (**PII**) is any data that can identify an individual. PII may be used alone or with other relevant data to identify an individual.

PII may include the following:

- Name
- Address
- Email
- Telephone Number
- Date of Birth
- Passport Number
- Fingerprint
- Credit or Debit Card Number
- Social Security Number

CleverTap does not automatically collect PII information, such as usernames, advertising identifiers, email addresses, mailing addresses, phone numbers, precise locations (such as GPS coordinates of four decimal places or more), etc. PII data must be explicitly pushed to CleverTap for it to be collected.

# Manage PII

To manage PII for end-users, you may use any or a combination of the following practices:

- [Mask PII](doc:manage-personal-information#mask-pii)
- [Audit Your Integration](doc:manage-personal-information#audit-your-integration)
- [Use Non-PII Identifiers](doc:manage-personal-information#use-non-pii-identifiers)
- [Use Server-Side Implementation](doc:manage-personal-information#use-server-side-implementation)
- [Track Malicious Users](doc:manage-personal-information#track-malicious-users)

## Mask PII

PII masking is the process of hiding or obscuring sensitive information to protect the privacy and security of individuals. PII masking is commonly used in data storage and transmission, especially in cases where the data needs to be shared with third parties or stored in a less secure location. Organizations need to use PII masking techniques to prevent data breaches and protect the privacy of their customers or users.

CleverTap lets you mask PII information to ensure security. For more information, refer to [Enable PII Masking](doc:pii-masking) and [Masking Personally Identifiable Information](https://docs.clevertap.com/docs/role-based-access-control#mask-personally-identifiable-information-and-events).

## Audit Your Integration

While planning your Integration, you should consult your internal legal counsel before pushing sensitive information such as PII to CleverTap. Get your [Event Design](https://docs.clevertap.com/docs/sample-events-by-business-verticals) document audited to prevent any _arbitrary data_ from being pushed to CleverTap. We recommend only pushing the _data needed_ to achieve the business objectives. For live integrations, use our Schema framework for auditing the data pushed to CleverTap.

## Use Non-PII Identifiers

CleverTap's client-side SDKs automatically assign a unique random identifier called a CleverTap ID. You can associate the _CleverTap ID_ with an identifier such as an email address, phone number, or database ID via client-side SDKs or APIs. We strongly recommend using a non-PII identifier. 

## Use Server-Side Implementation

CleverTap SDKs are open source and can be viewed in the [CleverTap Github Repository](https://github.com/CleverTap). You can also push data to CleverTap using our APIs or SFTP. We recommend a hybrid approach of client-side SDKs and APIs wherein the APIs pass sensitive information to CleverTap when required.

## Track Malicious Users

CleverTap SDKs use iOS or Android native storage. If a device's security is compromised or a user roots their Android device or jail breaks their iOS device, the data may be available for access to other third-party apps. We recommend using Non-PII identifiers and [Server-Side Implementation](https://developer.clevertap.com/docs/upload-user-profiles-api) for PII data. It can help you avoid any leakages.

# GDPR Compliance

CleverTap does not collect any of the data types by default, thus ensuring GDPR compliance for our clients. We go to great lengths to ensure customer data security, privacy, and confidentiality. We provide a role-based app­ level access control to customers to manage access to their data.

For more information, refer to [SDK Changes for GDPR Compliance](https://developer.clevertap.com/docs/sdk-changes-for-gdpr-compliance).