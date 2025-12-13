---
title: Partner Vouchers
excerpt: >-
  Learn how Partner Vouchers simplify voucher management for enabling seamless
  promotions and user rewards.
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

Businesses often collaborate with brand partners to offer incentives, such as discounts or exclusive offers, to drive user engagement, increase retention, and boost conversions. The Partner Vouchers reward module allows you to upload, manage, and distribute vouchers received from your partners to your app or website users.

Vouchers can be uploaded for a partner along with their metadata, such as code name, description, and expiry date. The uploaded vouchers can then be mapped to a Promo Campaign to distribute a unique voucher to your users based on the intended actions defined in the Campaign.

When a user receives a voucher, the Promo engine triggers an event called _CT Partner Voucher Rewarded_ with its event metadata. Based on this event, you can create a live-action engagement campaign, and the event metadata can be used as Liquid Tags to send a communication message to the user upon receiving the reward.

# Features

The following are the features of Partner Vouchers:

- **Voucher List Management**: Upload, manage, and distribute voucher codes.
- **Status Tracking**: Track the current state of voucher lists (Active, Expired, Paused, Archived).
- **Campaign Mapping**: Map voucher lists to one or multiple Promo Campaigns. Each campaign can define specific conditions for voucher distribution. You can also track which campaigns are linked to a voucher list directly from the voucher list page.
- **Voucher Utilization Tracking**: Track the number of codes issued against the total number of codes uploaded for each voucher list.
- **Top-up Codes**: Top up the voucher list with a new set of codes when used codes exceed a threshold limit.

# Voucher Distribution Workflow

A business using CleverTap partners with various brands to offer discount vouchers as part of its promotional campaigns. The business receives vouchers from these partnered brands, uploads them to the CleverTap platform, and then distributes them to eligible users based on predefined campaign conditions. Customers who meet the campaign criteria receive a unique voucher code and redeem it on the partnered brand platform.

Alternatively, if the business has an internal coupon engine to manage voucher redemption directly, it can upload internally generated vouchers to CleverTap for distribution. In this case, customers redeem the vouchers on the business's platform instead of an external partner's.

This setup ensures seamless voucher management, whether sourced externally from partners or internally from the business's systems.

# Voucher Distribution: Key Participants

Voucher distribution and redemption involve multiple participants, each playing a crucial role. The following table outlines each participant and their role in the voucher distribution and redemption workflow:

| Participants                      | Responsibility                                                                                                                                                                                                                                 |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Business (CleverTap Customer)** | Defines campaign eligibility criteria and distributes voucher codes through CleverTap. If partnering with brands, the business receives voucher codes from them. If using an internal coupon engine, it manages voucher redemption internally. |
| **Brand Partners**                | Supplies voucher codes to a business for distribution, if applicable. Customers redeem these vouchers on the brand platform.                                                                                                                   |
| **CleverTap**                     | Enables businesses to upload, manage, and distribute vouchers through the Partner Vouchers feature. It ensures vouchers are assigned to eligible users based on campaign conditions and tracks their usage.                                    |
| **Customer (End User)**           | Performs the required campaign actions to earn a voucher, then redeems it either on the partnered brand’s platform (if applicable) or the business’s platform if it manages redemptions internally.                                            |

# Resources

Refer to the following documents to explore how Partner Vouchers can transform your voucher distribution strategy and elevate your engagement efforts to new levels:

[block:html]
{
  "html": "<div class=\"two-col-container\">\n  <div class=\"link-content\">\n    <ul>\n      <li><a class=\"links\" href=\"https://docs.clevertap.com/docs/create-and-manage-voucher-lists\" target=\"_blank\" rel=\"noopener noreferrer\">Create and Manage Voucher Lists</a></li>\n      <li><a class=\"links\" href=\"https://docs.clevertap.com/docs/handle-duplicate-voucher-codes\" target=\"_blank\" rel=\"noopener noreferrer\">Handle Duplicate Voucher Codes</a></li>\n      \n    </ul>\n  </div>\n  \n  <div class=\"link-content\">\n    <ul>\n      <li><a class=\"links\" href=\"https://docs.clevertap.com/docs/use-partner-vouchers-in-campaigns\" target=\"_blank\" rel=\"noopener noreferrer\">Use Partner Vouchers in Campaigns</a></li>\n      <li><a class=\"links\" href=\"https://docs.clevertap.com/docs/troubleshooting-faqs\" target=\"_blank\" rel=\"noopener noreferrer\">Troubleshooting & FAQs</a></li>\n    </ul>\n  </div>\n</div>"
}
[/block]