---
title: Coupons
excerpt: >-
  Learn how to create, manage, and track coupons using CleverTap dashboard to
  boost engagement and drive conversions.
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

A coupon is a type of promotional reward that provides either an upfront discount or credits cashback points upon redemption. Coupons can be issued to all users or targeted to specific segments as part of a campaign.

CleverTap’s Coupons feature enables teams to create, configure, distribute, and track coupon-based promotions across web and mobile platforms. By leveraging this feature, businesses can encourage repeat purchases, boost customer loyalty, and optimize their promotional strategies.

Coupons follow a structured lifecycle, including coupon creation, activation, redemption, and expiration. Coupons can be assigned to users in the following two ways:

* **All Users Coupons**: Available to all customers without any specific rules and redeemed based on predefined criteria.
* **Campaign Users Coupons**: Distributed to specific users via promo campaigns based on segmentation or behavior.

# Coupon Configuration

The Coupon module allows you to configure how coupons are distributed, activated, shown, and redeemed. These settings help you tailor promotional strategies based on user behavior and business goals.

The following options are available to customize the coupon lifecycle:

* **Activation Settings**: Define when a coupon becomes active using one of the following options:
  * **Time-based**: Activation starts from a specific date and time.
  * **Event-based**: Activation is triggered by user actions. For example, app install, purchase, or any custom event.

* **Expiration Settings**: Define when a coupon expires using one of the following options:
  * **Fixed Expiry**: Valid until a specific date/time.
  * **Relative Expiry**: Valid for a defined period after activation. For example, 7 days from the date of assignment.

* **Coupon Distribution**: Define how coupons are issued to users. For more information, refer to [Select Coupon Type](doc:create-coupons#select-coupon-type).

* **Redemption Rules**: Define how coupons can be utilized using any one of the following options:
  * **Per-User Limit**: Maximum number of times a user can redeem the coupon.
  * **Global Limit**: Total number of redemptions allowed across all users.
  * **Redemption Window**: Optional start/end date within which redemption is allowed.

* **Visibility Options**: Configure coupon visibility in the user’s coupon tray.
  * **Visible**: Displayed to users for easy discovery and usage.
  * **Hidden**: Not shown in the tray but still redeemable by entering the code.

# Use Cases

The following are real-world examples that illustrate how businesses across industries use coupons:

* **E-commerce**: First-time purchase discounts, festive offers, cart abandonment recovery.
* **Food Delivery**: Time-bound coupons for free delivery or cashback during off-peak hours.
* **Travel and Hospitality**:Early-bird or last-minute booking discounts and loyalty rewards for repeat bookings.
* **Fintech/Wallet Apps**:UPI or wallet top-up incentives tied to specific payment methods.
* **Gaming**: In-App redemption coupons for limited-time promotions.

# Features

The Coupon module supports the following features:

* **Flexible Coupon Types**: Supports single static codes, bulk unique codes, and event-triggered coupon distribution.
* **Custom Discount Rules**: Apply discounts on the entire order, selected products, or custom order properties such as platform fees or shipping charges.
* **Qualifying Rules**: Configure based on user properties, product attributes, or cart conditions.
* **Advanced Redemption Controls**: Set per-user and global redemption limits, including daily, weekly, or monthly caps.
* **Scheduling**: Define start/end times or set recurring availability, such as weekends, happy hours, and so on.
* **Personalization Coupon Distribution**: Target all users or segments through promo campaigns.
* **User Property-Based Targeting**: Create coupons that apply only to specific user segments based on attributes such as location, language, user type, and so on.
* **Tracking and Analytics**: Monitor coupon performance in real-time with usage data and redemption insights.  
* **Bulk Code Management**: Seamlessly upload, manage, and track large sets of unique coupon codes via CSV.

# Resources

Refer to the following documents to understand CleverTap's Coupons feature:

<HTMLBlock>{`
 <div class="two-col-container">
  <div class="link-content">
    <ul>
      <li><a class="links" href="https://docs.clevertap.com/docs/view-coupons" target="_blank" rel="noopener noreferrer">View Coupons</a></li>
      <li><a class="links" href="https://docs.clevertap.com/docs/coupon-operations" target="_blank" rel="noopener noreferrer">Coupon Operations</a></li>
    </ul>
  </div>
  
  <div class="link-content">
    <ul>
      <li><a class="links" href="https://docs.clevertap.com/docs/create-coupons" target="_blank" rel="noopener noreferrer">Create Coupons</a></li>
      <li><a class="links" href="https://docs.clevertap.com/docs/coupon-stats" target="_blank" rel="noopener noreferrer">Coupon Stats</a></li>
    </ul>
  </div>
</div>
`}</HTMLBlock>
