---
title: Handle Duplicate Voucher Codes
excerpt: >-
  Learn how CleverTap handles duplicate voucher codes to maintain data integrity
  and prevent redemption conflicts.
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

To maintain data integrity and prevent redemption conflicts, CleverTap enforces strict duplicate checks when uploading voucher codes. The system validates voucher codes based on the combination of List Tag and Partner across all active voucher lists (lists that are not archived).

This document outlines the rules, scenarios, and best practices for handling duplicate voucher codes in CleverTap.

# Duplicate Voucher Code Rules

CleverTap follows a structured approach to prevent duplicate voucher codes while ensuring flexibility where needed.

## Duplicate Voucher Codes Blocked

CleverTap prevents duplicate codes within the same partner and list tag to avoid unintended voucher conflicts and redemption errors.

- A voucher code cannot be uploaded again within the same voucher list (if the List Tag and Partner are the same).
- A voucher code cannot be uploaded to another list under the same Partner if the List Tag already contains that code in any active voucher list.

The following table illustrates different scenarios of voucher code duplication across lists. The **Available Codes** column represents the existing codes in active voucher lists, helping you verify duplication before uploading new codes.

| List Name | Partner   | List Tag   | Available Codes       | Codes Uploaded        | Duplication Allowed?                    |
| --------- | --------- | ---------- | --------------------- | --------------------- | --------------------------------------- |
| List D    | Partner A | List Tag A | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Not Allowed (Same Partner and List Tag) |

## Duplicate Voucher Codes Allowed

In certain cases, CleverTap permits duplicate codes to enable cross-partner distribution and list reusability. This ensures businesses can manage vouchers effectively without unnecessary upload restrictions.

- A voucher code can be uploaded under the same List Tag but with a different Partner, as each partner operates independently.
- Once a voucher list is archived, its codes are no longer checked for duplication, allowing the same codes to be uploaded again.

The following table illustrates different scenarios of voucher code duplication across lists. The **Available Codes** column represents the existing codes in active voucher lists, helping you verify duplication before uploading new codes.

| List Name | Partner   | List Tag              | Available Codes       | Codes Uploaded        | Duplication Allowed?                                |
| --------- | --------- | --------------------- | --------------------- | --------------------- | --------------------------------------------------- |
| List A    | Partner A | List Tag A            | -                     | `Code1, Code2, Code3` | Allowed (First-time upload)                         |
| List B    | Partner A | List Tag B            | `Code1, Code4, Code5` | `Code1, Code4, Code5` | Allowed (Different List Tag under the same Partner) |
| List C    | Partner B | List Tag A            | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Allowed (Different Partner, different redemptions)  |
| List E    | Partner A | List Tag A (Archived) | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Allowed because List A is archived                  |

# Manage Duplicate Voucher Codes Across Partners

Consider a scenario where Customer X runs a New Year sale campaign and collaborates with multiple partners to distribute discount vouchers. Each partner, such as Partner A and Partner B, operates independently, managing their own set of voucher codes.

As each partner controls their own redemption platform, CleverTap enforces duplication checks within the same partner but allows the same code across different partners.

[block:parameters]
{
  "data": {
    "h-0": "Scenario",
    "h-1": "Action",
    "h-2": "Allowed?",
    "h-3": "Reason",
    "0-0": "Uploading `Code 1` under different partners",
    "0-1": "<li>Code1 is uploaded under Partner A (similar to List A).</li><li>Code1 is uploaded under Partner B (similar to List C).</li>  \n  \n<br />",
    "0-2": "Yes",
    "0-3": "Different partners operate independently, preventing redemption conflicts.",
    "1-0": "Uploading `Code 1` again under the same partner",
    "1-1": "<li>Code1 was already uploaded under Partner A (similar to List A).</li><li>Customer X attempts to upload Code1 again under Partner A in another active list (similar to List D).</li>  \n  \n<br />",
    "1-2": "No",
    "1-3": "Partner A already has an active list with `Code 1`. CleverTap prevents duplicates within the same partner across active lists.",
    "2-0": "Re-uploading `Code 1` after archiving the original list",
    "2-1": "<li>`Code 1` was in List A (archived).</li><li>Customer X attempts to re-upload `Code 1` under a new list (similar to List E).</li>  \n  \n<br />",
    "2-2": "Yes",
    "2-3": "Once a list is archived, its codes are no longer checked for duplication, allowing re-upload."
  },
  "cols": 4,
  "rows": 3,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]