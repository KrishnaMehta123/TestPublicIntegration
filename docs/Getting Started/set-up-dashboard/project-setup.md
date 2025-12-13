---
title: Project Setup
excerpt: Learn how to set up your Project on the CleverTap dashboard.
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

A project can be an individual app, website, or product. You can combine multiple platforms, such as Android, iOS, Web, and so on, in a single project. You can also have separate projects for each platform, depending on your business goals. 

# Create a Project

After you log on to the CleverTap platform for the first time, you can create a project. From the setup page, perform the following steps:

1. Enter a _Project name_. 
2. Select the _Business category_ from the list. 
3. Define the Account Timezone. 

> 📘 What Affects Timezones
> 
> Campaign delivery, Journeys, and scheduled data exports are based on timezones.

4. Choose from the following platforms:
   - Android 
   - iOS
   - Web
   - API
5. Choose the platform for your app. Select _Native_ for native [Android](https://developer.clevertap.com/docs/android) and [iOS](https://developer.clevertap.com/docs/ios) apps. You can also select the other hybrid platforms for Android and iOS, such as:
   - [Cordova](https://developer.clevertap.com/docs/cordova)
   - [Unity](https://developer.clevertap.com/docs/unity)
   - [Xamarin](https://developer.clevertap.com/docs/xamarin)
   - [React Native](https://developer.clevertap.com/docs/react-native)
   - [Flutter](https://developer.clevertap.com/docs/flutter-sdk)
6. Click **Create Project**. A project with the specified name is created.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f493061-Chunk_1_-_Dashboard_setup_1.png",
        "Create a Project",
        462
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Create a Project"
    }
  ]
}
[/block]


## Create a Test Project

CleverTap automatically creates a _Test_ project for testing when you create a Live project. You can perform all your tests on this project before you actually roll out the changes. However, you also have the flexibility to create additional test projects within a Live project if needed.

> 📘 Permissions
> 
> To create a Live or Test project, you must have the Admin access.

To create a Test project:

1. Go to _Organization_ > _Projects_ from the CleverTap dashboard.
2. Click **+ Test Project**. 
3. Enter _Project name_.
4. Click **Add**.

The Test project is created on the _Projects_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7882f92-Create_a_Test_Project.gif",
        "",
        "Create a Test Project"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Test Project"
    }
  ]
}
[/block]


## Edit a Project Name

The admin can edit a project name later, and it will not affect the project in any other way except for the name change. To modify a project name, perform the following steps:

1. From the CleverTap dashboard, navigate to _Settings_ > _Project_.
2. Click the ![](https://files.readme.io/a581163-Ellipsis.png) icon next to the project name.
3. Modify the project name.
4. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1d3eb3-Edit_a_Project_Name.gif",
        "",
        "Change a Project Name"
      ],
      "align": "center",
      "border": true,
      "caption": "Change a Project Name"
    }
  ]
}
[/block]


# Add Billing Details

This section on the dashboard allows organization admins to configure and manage billing information for the CleverTap account.

To view the billing details, go to **Organization** > **Billing** > **Billing details** from the CleverTap dashboard. The **Billing details** page opens. It is split into three main areas:

- [Primary Billing Contact](doc:project-setup#primary-billing-contact) 
- [Secondary Billing Contacts](doc:project-setup#secondary-billing-contact)
- [Billing Details and Address](doc:project-setup#billing-details-and-address)

## Primary Billing Contact

This form specifies the primary individual responsible for receiving all billing-related communications. This person is the main recipient of billing emails and will be contacted for any payment or invoice issues.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1266a368a1c4ac82de7dbeeb130be60f6474983efa7c3aa98856eda64b63d67a-image.png",
        null,
        "Primary Billing Contact"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Primary Billing Contact"
    }
  ]
}
[/block]


This form has the following fields:

- **Name** _(Required)_: Enter the full name of the primary contact.
- **Email Address** _(Required)_: Select from a list of registered users.
- **Phone Number** _(Optional)_: Enter the phone number of the billing contact.

## Secondary Billing Contacts

This form allows you to add up to 10 additional users as secondary billing contacts. In addition to the primary contact, these users will also receive billing communications. This form has a searchable list to select multiple users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7eec679193112b2638f67bdad2e4f68b21ec74345611cda417ebee0990a5ec53-image.png",
        null,
        "Secondary Billing Contacts"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Secondary Billing Contacts"
    }
  ]
}
[/block]


## Billing Details and Address

These details are required for tax and legal compliance purposes. It includes organization and billing address details that are split into three main areas:

- [Billing Details](doc:project-setup#billing-details) 
- [Billing Address](doc:project-setup#billing-address)
- [Shipping Address](doc:project-setup#shipping-address)

### Billing Details

This section allows the user to provide details of the organization for tax and legal compliance.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c1873ff107920bb4e4044b004efee244161e945d90dc6d44df5ca0e1cb9b27b3-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true
    }
  ]
}
[/block]


This form has the following fields:

- **Organization Name** _(Required)_: Enter the legal name of the organization.
- **DBA (Doing Business As)** _(Optional)_: Specify any alternate business name.
- **Tax Number** _(Optional)_: Enter the tax identification number.

### Billing Address

This section allows the user to provide a billing address.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f259f4128509fd5d55e135eab83de36195b2ada482f7430b0470ed5959394743-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true
    }
  ]
}
[/block]


This form has the following fields:

- **Billing Address Line 1** _(Required)_: Street, apartment, or company address.
- **Billing Address Line 2** _(Required)_: Additional location details (area, sector, and so on).
- **Country** _(Required)_: Select from the list.
- **State/Province/Region** _(Required)_: Select from the list.
- **City/Town** _(Required)_: Enter the name of the city or town.
- **Postal Code** _(Required)_: Enter the postal/ZIP code.

### Shipping Address

This section allows the user to provide a different shipping address if necessary.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/72299150c6212635fc4aba2819cbfbcf17777e3af407a335ad72dcf2718a18ad-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true
    }
  ]
}
[/block]


This form has the following fields:

- **Checkbox**: _Same as billing address_ auto-fills the shipping address fields, same as billing address.
- **Shipping Address Line 1** _(Required)_: Apartment, unit, or suite.
- **Shipping Address Line 2** _(Required)_: Street address.
- **Country** _(Required)_: Select from the list.
- **State/Province/Region** _(Required)_: Select from the list.
- **City/Town** _(Required)_: Enter city or town name.
- **Postal Code** _(Required)_: Enter postal/ZIP code.