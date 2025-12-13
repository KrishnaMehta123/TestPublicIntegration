---
title: Licensing Fee
excerpt: >-
  Learn how to manage licensed seats and maximize the efficiency of your
  CleverTap experience.
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

Licensing Fee at CleverTap helps control and monitor the number of active users, ensuring compliance with the selected tier. This document provides insights into key concepts and considerations related to licensing, offering a comprehensive guide to understanding CleverTap's licensing structure.

# Key Concepts

The following are the fundamental concepts essential for comprehending CleverTap's licensing structure:

* [User Tiers](doc:licensing-fee#user-tiers)
* [Licensed User Calculation](doc:licensing-fee#licensed-user-calculation)
* [Licensed Seat Usage](doc:licensing-fee#licensed-seat-usage)
* [View and Download Licensed Users List](doc:licensing-fee#view-and-download-licensed-users-list)
* [Breach of Licensed Seats](doc:licensing-fee#breach-of-licensed-seats)
* [Fair Usage Policy (FUP)](doc:licensing-fee#fair-usage-policy-fup)

## User Tiers

CleverTap offers various licensing tiers to accommodate businesses of different sizes and requirements. Users are categorized into tiers based on the number of licenses the organization purchases. The following are the CleverTap licensed seat tiers:

* 20 seats
* 50 seats **(next 30)**
* 100 seats **(next 50)**
* Unlimited seats 

The term **next 30** alongside 50 seats refers to an extra 30 seats beyond the initial tier of 20 seats. In contrast, the same term alongside 100 seats implies an additional 50 seats beyond their respective initial tier of 50 seats. This setup allows flexibility in scaling up the number of licensed seats within specific tiers after reaching the initial seat limits.

## Licensed User Calculation

CleverTap calculates the average count of licensed users per month by adding the daily counts together and dividing the total by the number of days in that month. This monthly average is used to determine the pricing tier. 

**Licensed Users = (Sum of Daily Licensed User Counts) / (Number of Days in the Month)**, that is,

**Licensed Users = (U₁ + U₂ + ... + U₃₀) / 30**

Where:

* U₁ is the number of licensed users on Day 1
* U₂ is the number on Day 2
* U₃₀ is the number on Day 30

**Example** 

In a 30-day month:

* For 10 days, there were 40 users each day  
* For the next 10 days, there were 80 users each day  
* For the remaining 10 days, there were 60 users each day  

The calculation would be as follows:

* Licensed Users = \[(10×40) + (10×80) + (10×60)] / 30 = (400 + 800 + 600) / 30 = **60**

This ensures that the billing reflects user fluctuations across the month based on daily counts.

> 📘 User Status
>
> Only users with an *Active* status are counted as licensed users. Users with *Revoked* or *Invited* statuses do not count as licensed users.

## Licensed Seat Usage

CleverTap always informs you about license usage when you invite a new user, as shown in the following image:

<Image alt="Licensed Seats Usage Alert" align="center" border={true} src="https://files.readme.io/cc3a7e3-Licencing_Usage_Alert.png">
  Licensed Seats Usage Alert
</Image>

If the license usage reaches 95%, CleverTap warns you about the limited availability of remaining license seats.

<Image alt="Using 95% of the Licence Seats" align="center" border={true} src="https://files.readme.io/dabf76f-Breaching_License_Usage.png">
  Using 95% of the Licence Seats
</Image>

## View and Download Licensed Users List

You can view a summary of licensed seat usage within your CleverTap dashboard and download a detailed CSV file containing individual licensed user information.

### View Licensed Users List

View high-level *Licensed Seats Usage Details* for each project in your organization. This view helps you track overall usage and identify projects that are close to their seat limits.

#### To view licensed seat usage details

1. Go to *Organization* > *Billing* > *My Plan* in your CleverTap dashboard.
2. Under the *Usage* section, click *View licensed seats usage details* in the *Licensed Seats Usage* panel.
3. Select the desired Month and Year.
   * The screen displays the counts of *Daily Active Users* and *Billable Seats*, along with *Project Details* that show the user counts for each project.

<Image alt="Licensed Seats Usage Details screen showing project-level usage summary" align="center" width="95% " border={true} src="https://files.readme.io/b821dae4103cfcb0a2295ab274bad8adae5fb7271c1892d7e5f1dcad98e4af32-487fc9812b38812e458f7d8f30461349616d48acc37567d03185451177850b9e-image.png">
  Licensed Seats Usage Details screen showing project-level usage summary
</Image>

> 📘 Note
>
> The on-screen view shows only project-level counts. To see user-level details, download the CSV file.

### Download Licensed Users List

Download a CSV file to access detailed licensed user information, including email IDs and project assignments.

#### To download the list

1. From the *Licensed Seats Usage Details* view, click **Download CSV**.
2. The downloaded CSV file includes:
   * The total number of active and billable users.
   * Email IDs associated with each licensed user.
   * The user distribution across projects.

<Image alt="Download Licensed Users List" align="center" width="75% " border={true} src="https://files.readme.io/ae0c6c5978733ae18630e947f1c777be9524c40fb96b8d99c6da9574db497215-0b1ee0f4ee592a9b046026e231fad0e77bd3e83e521b4717ae67d29c4f6a4a69-image.png">
  Download Licensed Users List
</Image>

## Breach of Licensed Seats

Breaching the set tier leads to additional charges based on the next tier. If you exceed the allotted seats of your license tier, CleverTap notifies you about the breach on the *Invite Users* page.

<Image alt="Licence Seats Usage" align="center" border={true} src="https://files.readme.io/5018b37-Invite_Users.png">
  Breaching Licensed Seat Usage Alert
</Image>

CleverTap informs you about the same on the dashboard's nag bar and via an email alert.

## Fair Usage Policy (FUP)

CleverTap's Fair Usage Policy (FUP) ensures fair usage and adherence to the agreed licensing terms. For FUP, the maximum allowable licenses are capped at 10,000. Reaching the limit leads to restrictions on inviting new users.

# FAQs

The following are the frequently asked questions for CleverTap's licensing fee structure:

### Q. Does CleverTap charge individually per seat, or does it operate exclusively on tier-based pricing?

A. Licensing fees are solely based on tiers; there are no per-seat charges.

### Q. How is the billing calculated if the seat consumption fluctuates during the month?

A. Billing calculations are conducted monthly to accommodate scenarios with varying seat consumption.

### Q. Do licensing fees align with monthly usage or follow specific billing intervals?

A. Licensing fee aligns with monthly consumption.

### Q. Will accessing the CleverTap dashboard through Single Sign-On (SSO) utilize one of the licensed seats?

A. Using Single Sign-On (SSO) to access the CleverTap dashboard does contribute to the licensed seat count.

### Q. What should I do if I exceed the FUP limit?

A. Maximize usage efficiency by revoking access for existing *Active* or *Invited* users if you surpass your account's FUP limit before inviting new users.
