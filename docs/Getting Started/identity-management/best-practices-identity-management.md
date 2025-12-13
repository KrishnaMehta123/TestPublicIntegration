---
title: Best Practices - Identity Management - WIP
excerpt: Understand what are the best practices of Identity Management in CleverTap.
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

When working with identity management, it is recommended to follow best practices as you set up your identities. 

# Best Practices to Consider

Here are some best practices:

* Always perform multiple tests before going live on a production account. 

> 📘 Account Reset
>
> Account reset is only available in a test environment.

* To maintain data quality, you must never change an identity.
* Avoid resetting or deleting a user profile. Always consult your customer success manager first.
* If your app allows you to change email addresses, enable *Do not merge identifiers on the same device* on your CleverTap dashboard. For the steps, refer to [How Do You Want CleverTap to Handle Identified Profiles?](https://docs.clevertap.com/docs/troubleshooting#how-do-you-want-clevertap-to-handle-identified-profiles).
* Do not set an identity if it is not present. 

> 👍 Example
>
> Setting an identity as *None* to multiple users will group all events under that *None* identity together.
>
> Any user with the *None* identity is assumed to be the same user. You can always set the identity later and CleverTap has in-built logic that will merge the anonymous events to the identified user. 
>
> For more information, refer to [Use Case #2: Identity Is Assigned after Anonymous Events](https://docs.clevertap.com/docs/use-cases-1#use-case-2-identity-is-assigned-after-anonymous-events).

* Do not assign an identity that might change later. If someone’s email can change within your app, then it is not a good idea to set it as an identity, as CleverTap will mark the person as a new user if they change their email.

Assigning user IDs can be tricky, so if you run into issues assigning an identity, contact us for help by creating a support ticket from your dashboard.
