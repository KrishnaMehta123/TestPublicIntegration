---
title: View Coupons
excerpt: >-
  Learn how to view and manage all coupons in your CleverTap dashboard using the
  centralized list view.
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

The Coupons list page provides a centralized view to filter, search, and manage all coupons created in your account. You can view the list of coupons by navigating to _Promotions_ > _Rewards_ > _Coupons_ from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/10d8ebbe18c50adc7cf55d1d5583d3742edd603300069de39fe8318135a0f2c5-image.png",
        null,
        "View Available Coupons"
      ],
      "align": "center",
      "border": true,
      "caption": "View Available Coupons"
    }
  ]
}
[/block]


This page is divided into the following two tabs based on the coupon lifecycle status:

- **Available**: Displays the coupons that are active, scheduled, paused, or in draft state. These coupons are still active, editable, or scheduled for future use.
- **Archived**: Displays the coupons that have expired or been manually archived. These coupons are no longer active and are view-only. You can use this tab to review historical coupon data and past promotions.

Each tab displays key details for every coupon in a tabular format, including status, type, usage, linked campaigns, and more.

| Column Name          | Description                                                                                                                                                                                                                                                                                                                                                                                                            |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coupon Code/Name** | <p>Displays either the coupon code or the coupon name along with the coupon ID, based on the coupon type.</p><ul><li>In the case of single code coupons, it indicates the coupon code and ID.</li><li>In the case of bulk codes, it indicates the coupon name and ID.</li></ul><p>Clicking the coupon opens the coupon details page.</p>                                                                               |
| **Status**           | Shows the current status of the coupon, such as _Active_, _Paused_, _Draft_, _Scheduled_, _Ended_, or _Archived_. For more information, refer to [Status and Actions](doc:coupon-operations#status-and-actions).                                                                                                                                                                                                       |
| **Updated On**       | Displays the date and time when the coupon was last updated.                                                                                                                                                                                                                                                                                                                                                           |
| **Coupon Type**      | <p>Indicates how the coupon is distributed and redeemed based on the format and triggering method. The following are the available options:</p><ul><li>Single code for all users</li><li>Single code based on user actions</li><li>Downloadable bulk unique codes</li><li>Bulk unique codes based on user actions</li></ul>For more information, refer to [Select Coupon Type](doc:create-coupons#select-coupon-type). |
| **Limit Per Code**   | Displays the maximum number of times the coupon code can be redeemed. It applies to single code coupons only, and the value can be set to either unlimited or a fixed number of redemptions per code.                                                                                                                                                                                                                  |
| **Redemptions**      | Shows the number of times the coupon has been redeemed.                                                                                                                                                                                                                                                                                                                                                                |