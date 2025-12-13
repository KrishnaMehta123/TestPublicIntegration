---
title: Single Sign On (SSO) (COPY)
excerpt: >-
  Understand how to configure SSO for your CleverTap application using leading
  IdPs.
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

You can use Single Sign-On (SSO) to access your CleverTap dashboard. You must use an Identity Provider (IdP) or a custom SAML (Security Assertion Markup Language) implementation to use SSO with CleverTap. Note that you must be an account admin to set up an SSO.

> 📘 Key Benefits of New SSO Configuration
> 
> The migration steps for existing SSO customers moving to a new SAML SSO setup are the same as setting up the SSO configuration for the first time. 
> 
> Listed below are the key benefits of the new SAML SSO setup:
> 
> - Streamlined SSO configuration process without needing Account-Role Mapping on IdP.
> - Flexibility to manage users entirely on the CleverTap dashboard or by sending account lists through IdP and managing roles on the dashboard.
> - Enhanced security and simplified login experience for your team through email domain whitelisting.

# Set Up SSO Configuration

The SSO Configuration process includes the following two steps:

1. [Set up SSO configuration on CleverTap](doc:single-sign-on-sso#set-up-sso-configuration-on-clevertap).
2. [Configure CleverTap Application on your IdP](doc:single-sign-on-sso#configure-clevertap-application-on-your-idp)

### Set Up SSO configuration on CleverTap

To set up the SSO configuration on the CleverTap dashboard:

1. Navigate to _Organization_ > _SSO_ from the CleverTap dashboard. 
2. Click **Create SAML Connection**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1926a21-Create_SAML_Connection.png",
        null,
        "Create SAML Connection"
      ],
      "align": "center",
      "border": true,
      "caption": "Create SAML Connection"
    }
  ]
}
[/block]


The _Create SAML Connection_ window opens on the right side of the screen after you click **Create SAML Connection**, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3585acc-SSO_Connection.png",
        null,
        "Enter Details to Create SAML Connection"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Details to Create SAML Connection"
    }
  ]
}
[/block]


3. Enter the following details:
   - _Sign-in URL_
   - _Organization name_
   - _IDP Signing certificate_ (You can either paste the certificate details or upload the **.CER** file)
   - _SAML Eligible Email Domains_ 
     In order to claim ownership of a domain, it is necessary for the organization to have at least one active user associated with that particular domain.

4. Click **Create**.

> 📘 Note
> 
> - After you configure _Sign-in URL_ and  _IDP Signing certificate_, these  details are available from your respective identity providers. For more information about IdP configuration, refer [Okta](doc:single-sign-on-sso#okta-setup), [OneLogin](doc:single-sign-on-sso#onelogin-setup), [Azure](doc:single-sign-on-sso#azure-setup) and [Gsuite](doc:single-sign-on-sso#gsuite-setup).
> - CleverTap recommends avoiding a word processor for copy-pasting sensitive values like certificates; instead, you can use an IDE or terminal.

After creating the SAML connection successfully, SAML Service Provider details are displayed on the page, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5d6329d-SAML_Connection.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. Navigate to your respective IdP sections in the document and complete the steps mentioned to configure the connection.

> 📘 Configuration Updates
> 
> The following are the updates related to CleverTap's SSO configurations process:
> 
> - The IdP metadata XML is not accepted as a configuration parameter anymore.
> 
> - The domain discovery now recognizes email domains. It means you can now log in through an IdP using a specific email address (for example, [employee@clevertap.com](employee@clevertap.com)) instead of organization names (for example, CleverTap). All users must provide their email addresses, and the system automatically determines if they use SAML or basic authentication.
> 
> - All users must provide an email address on the new login page (the old login page still accepts the organization names).
> 
> CleverTap strongly recommends adding your email domains rather than public ones or other organizations. If you encounter errors during configuration, it may be because the email domain is public (for example, gmail.com, outlook.com) or already claimed by another organization. Contact our support team if you encounter an issue and want to claim an email domain.

### Configure CleverTap Application on your IdP

To configure CleverTap on your IdP, you must map the attributes. The following are the two methods for attribute mapping:

- [Add a list of names and emails only (Recommended)](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended)
- [Send a list of attributes along with accountList and an array of accountIds](doc:single-sign-on-sso#send-a-list-of-attributes-along-with-accountlist-and-an-array-of-accountids).

Based on the selected attribute mapping logic and your IdP, map the attributes as illustrated for specific IdPs:

- [Attribute Mapping for Okta](doc:single-sign-on-sso#map-attributes)
- [Attribute Mapping for OneLogin](doc:single-sign-on-sso#map-attributes-1)
- [Attribute Mapping for Azure](doc:single-sign-on-sso#map-attributes-2)
- [Attribute Mapping for Gsuite](doc:single-sign-on-sso#map-attributes-3)

# Identity Service Provider

Identity Provider (IdP) is an authority that verifies and asserts a user's identity and access to a requested resource (the "Service Provider"). Some examples of IdPs are Okta, GSuite, and so on.

# Attribute Mapping Logic for IdPs

You can set up your IdP attributes in the following two ways:

### Add a List of Names and Emails Only (Recommended)

Users onboarded before SAML SSO activation can continue to access their previous accounts. Users onboarded through SAML SSO for the first time are redirected to the no-access page and cannot access any accounts.

The user is onboarded to new accounts by sending an invitation to any account. Inviting a SAML user to an account may not send an email invite; instead, directly grant them access. However, the user needs to log out and then log in to view the new account assignments.

There are no organization-based checks in this method, as the provision of access is still in the hands of the admin of the target account.

### Send a List of attributes Along With _accountList_ and an Array of accountIds

In this case, the user can only access the accounts mentioned in the `accountList` attribute. The invitation flow does not work for gaining access to any account. The account must be added to the `accountList`.  An additional check is performed on the accounts present in the accountList to validate if they belong to a family of accounts for which the current SAML SSO connection is configured. For example, if a connection is made for customer A and tries to pass the account Ids of customer B, they would be blocked.

The optional attribute `accountList` must be added in the following manner:  
accountList : ["1000000001", "1000000002", "1000000003"].

> 🚧 Note
> 
> - If the user has access to any other account on the system apart from the ones present in the `accountList`, they would lose access to those accounts.
> - You must connect all your accounts to a parent account for which the SSO configuration is created.

# Configure IDPs

This section illustrates how to set up access for the following IDPs:

- [Okta](doc:single-sign-on-sso#okta-setup)
- [OneLogin](doc:single-sign-on-sso#onelogin-setup)
- [GSuite](doc:single-sign-on-sso#gsuite-setup)
- [Azure](doc:single-sign-on-sso#azure-setup)

> 📘 Note
> 
> You can configure any IdP that supports SAML SSO, following the recommended approach.

## Okta Setup

This section provides information about the Okta setup. The process involves the following major steps:

1. [Create an application](doc:single-sign-on-sso#create-an-application).
2. [Map the attributes](doc:single-sign-on-sso#map-attributes).
3. [Assign the CleverTap application to the user](doc:single-sign-on-sso#assign-clevertap-application-to-user).

### Create an Application

Start the setup by creating a CleverTap app in your IdP setup. All IdPs allow you to create an app you want to access using SSO. Consider the following example of setting up an app with Okta:

1. Navigate to your Okta admin dashboard.
2. Select _Applications_ from the left navigation and click **Create App Integration.**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/562223c-okta.png",
        "Creating New Application in Okta",
        2172
      ],
      "align": "center",
      "border": true,
      "caption": "Creating New Application in Okta"
    }
  ]
}
[/block]


3. After the _Sign-in method_ box appears, select _SAML 2.0_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f88a5bc-Okta_1.png",
        "New App Integration",
        1746
      ],
      "align": "center",
      "border": true,
      "caption": "New App Integration"
    }
  ]
}
[/block]


4. Enter your application details as shown in the image below and click **Next**:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc8ca2a-Okta_2_-_App_details.png",
        "App Configuration on Okta",
        1694
      ],
      "align": "center",
      "sizing": "% ",
      "border": true,
      "caption": "App Configuration on Okta"
    }
  ]
}
[/block]


5. Add the Single sign-on URL and Audience URI(Entity ID) values. (You can find these credentials on the _Create SAML connection_ page of the CleverTap dashboard).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/022dc3e-Okta_2.png",
        "SAML Settings for Okta App",
        1084
      ],
      "align": "center",
      "border": true,
      "caption": "SAML Settings for Okta App"
    }
  ]
}
[/block]


### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so, you must map the attributes:

1. Add three attributes - _name_, _email_  and _accountList_ appropriately, and map the attributes accordingly as shown in the image below:

> 📘 Note
> 
> If you proceed further with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - _name_, _email_  in the attribute mapping section appropriately. You need not add any custom attributes and hence you must skip _step 2_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebe57ff-okta_3_attributes.png",
        "Attribute Mapping",
        1166
      ],
      "align": "center",
      "border": true,
      "caption": "Attribute Mapping"
    }
  ]
}
[/block]


2. For the _accountList_ attribute, you must create a custom attribute: 

   i. Navigate to _Directory_ > _Profile editor_ > Select your application (CleverTap).  
   ii. Click **+ Add Attributes**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eba29d1-add_attribute.png",
        "Add Attributes",
        2416
      ],
      "align": "center",
      "border": true,
      "caption": "Add Attributes"
    }
  ]
}
[/block]


  iii. Define all the attribute values for `accountList`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9c0426e-add_account_list_attribute.png",
        "Add Account Attributes",
        1086
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]


 iv. Click **Save**

### Assign CleverTap Application to User

To assign your CleverTap application to users:

1. Navigate to _Applications_ > Select your application.
2. Select _Assign to People_ from the _Assign_ dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a9f24f2-assign.png",
        "Assigning an Applications to Users",
        1356
      ],
      "align": "center",
      "border": true,
      "caption": "Assigning an Applications to Users"
    }
  ]
}
[/block]


3. Select the user you want to assign and click _Assign_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2b07ad-assign_users.png",
        "Assign an Application to Users",
        1646
      ],
      "align": "center",
      "border": true,
      "caption": "Assign an Application to Users"
    }
  ]
}
[/block]


4. Ensure that the `accountList` value is populated against the accountList attribute in the dropdown. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a103b02-assign.png",
        "Account list Attribute Mapping",
        658
      ],
      "align": "center",
      "border": true,
      "caption": "Account list Attribute Mapping"
    }
  ]
}
[/block]


5. Click **Save and Go Back** and then click **Done**.

To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to _Applications_ > _Sign on_
2. Click **View SAML Setup** instruction available at the bottom right of the page. You can find the credentials as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/daad644-SAML_.png",
        "Credentials for SAML Connection",
        812
      ],
      "align": "center",
      "border": true,
      "caption": "Credentials for SAML Connection"
    }
  ]
}
[/block]


4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## OneLogin Setup

This section provides information about the OneLogin setup. The process involves the following major steps:

1. [Create an application.](doc:single-sign-on-sso#create-an-application-1)
2. [Map Attributes.](doc:single-sign-on-sso#map-attributes-1)
3. [Assign the CleverTap application to the user.](doc:single-sign-on-sso#assign-clevertap-application-to-user-1)

### Create an Application

To create an application:

1. Select _Applications_ tab and select _Applications_ from the menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7179a7d-one_login_1.png",
        "Create a New OneLogin Application",
        1474
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New OneLogin Application"
    }
  ]
}
[/block]


2. Click **Add App** and search for _SAML Custom Connector (Advance)_ in the search bar.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d69db6-1.png",
        "Create a New OneLogin Application",
        1566
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New OneLogin Application"
    }
  ]
}
[/block]


3. Select _SAML Custom Connector (Advance)_ and enter the _Display Name_.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c039dd3-2.png",
        "Add SAML Custom Connector",
        832
      ],
      "align": "center",
      "border": true,
      "caption": "Add SAML Custom Connector"
    }
  ]
}
[/block]


4. Click **Save**.

5. From the left panel,  navigate to the _Configuration_ section and enter the _ACS (Consumer) URL_ and_ Audience (EntityID)._ (You can find these credentials on the Create SAML connection page of the CleverTap dashboard).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61ffd10-SSO_CTD.png",
        "Configure Custom Connector",
        2614
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Custom Connector"
    }
  ]
}
[/block]


### Map Attributes

After configuring the application, ensure that correct values are passed to CleverTap by mapping the attributes:

1. From the left menu under _Applications_ tab, navigate to the _Parameter_ section and click the **+** sign to add new fields and ensure that the _Configured by admin_ button is selected.

2. Add three attributes - _name_, _email_  and _accountList_ appropriately, and map the attributes accordingly as shown below:

> 📘 Note
> 
> If you proceed further with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - _name_, _email_  in the attribute mapping section appropriately. You do not need to add any custom attributes and hence you must skip _step 4_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d17448a-Screenshot_2023-02-14_at_8.17.17_PM.png",
        "Map Attributes",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Map Attributes"
    }
  ]
}
[/block]


3. Add value as _FirstName_ and _Email_ for Name and Email, respectively, and click **Save**.

4. a. Add _accountList_ as _Name_  and click **Save**.

   b. Select _Value_ as _Macro_ from the dropdown and pass the account ID.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9df9451-Screenshot_2023-02-14_at_8.16.08_PM.png",
        "Map Custom Attribute",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Map Custom Attribute"
    }
  ]
}
[/block]


> 📘 Note
> 
> Ensure that you select the _Include in SAML assertion_ when adding all three attributes as shown in the  figure above.

### Assign CleverTap Application to User

To assign your CleverTap application to users: 

1. Navigate to _Users_ from the top panel and click **Users**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f42d6e-users.png",
        "User Assignment",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "User Assignment"
    }
  ]
}
[/block]


2. Select the user you want to assign to the CleverTap application. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ab0626a-Screenshot_2023-02-14_at_8.33.58_PM.png",
        "Assign an Application to Users",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Assign an Application to Users"
    }
  ]
}
[/block]


The _User Info_ page opens:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f85c617-Screenshot_2023-02-14_at_8.34.15_PM.png",
        "User Profile",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "User Profile"
    }
  ]
}
[/block]


3. Navigate to applications from the left panel, click **+**, and select CleverTap from the dropdown.
4. Click **Continue**
5. Verify all the values passed for that user from the _Edit CleverTap Login_ page and click **Save**

Now, you have successfully assigned the CleverTap application to the user.

To create a SAML connection on the CleverTap dashboard, you need two credentials, as mentioned in the beginning. To find your _Sign-in URL_ and _IDP Signing certificate_:

1. Navigate to the _Applications_ tab from the top panel, and select the CleverTap application
2. Navigate to _SSO_ from the left navigation and copy the _SAML 2.0 Endpoint(HTTP)_ for the SAML connection on CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c739f80-saml_2.0.png",
        " View SAML 2.0 Endpoint",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "SAML 2.0 Endpoint"
    }
  ]
}
[/block]


3. Click **View Details** for the IDP signing certificate  as shown below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/71b5bd0-certificate.png",
        "View IDP Signing Certificate",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "View IDP Signing Certificate"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/56b01bc-certificate_detail.png",
        "Copy IDP Signing Certificate",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Copy IDP Signing Certificate"
    }
  ]
}
[/block]


4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## Azure Setup

This section provides information about the Azure setup. The process involves the following major steps:

- [Create an application](doc:single-sign-on-sso#create-an-application-2).
- [Map the attributes.](doc:single-sign-on-sso#create-an-application-2)
- [Assign the CleverTap application to the user](doc:single-sign-on-sso#map-attributes-2).

### Create an Application

1. Start the setup by signing up and creating a CleverTap app on the [Azure Portal ](https://portal.azure.com/)
2. From the left navigation panel, select _Azure Active Directory._

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1b6307-a1.png",
        "a1.png",
        1734
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


3. Click _+ Add_  and select _Enterprise application_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2981515-az1.png",
        "az1.png",
        1890
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. Click **+ Create your application**.
6. Enter the name of the application.
7. Select the _Non-gallery application_ option as shown in the following image and click **Add**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7dcdffd-image_4.png",
        "image (4).png",
        2816
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. Click ** Set up single sign on**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a58404-image_5.png",
        "image (5).png",
        2282
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


 The _Single sign-on_ page opens. 

6. Click  **SAML**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0286a85-saml.png",
        "saml.png",
        2864
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


7. Click the _Edit_ icon available next to _Basic SAML configuration_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e3ae05-SAML1.png",
        "SAML1.png",
        1794
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


8. Add the _ACS_ and _Entity ID_. You can find these credentials on the _Create SAML connection_ page on CleverTap. To get these credentials:
   1. Navigate to _Organization_ > _SSO_ from the CleverTap dashboard. 
   2. Copy the _Entity ID_ and _Assertion Consumer Service URL_>_Create SAML Connection_.
9. Paste the respective values into the SAML configuration section as shown in the following screenshot and click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06684f2-SAML_Configuration_Azure.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so:

1. Under the _Attribute & Claims_ section, you must map the following two attributes: name and email appropriately and click **Save** (see following figure image below).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d6b809-small-Azure_Attributes.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


> 📘 Note
> 
> If you proceed further with the [recommended method](https://docs.clevertap.com/docs/single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), you need not add any custom attributes and hence you must skip _step 2_.

2. Refer to this [Azure support document](https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-feature-directory-extensions) to create a `accountList` custom attribute.

### Assign CleverTap Application to User

To assign your CleverTap application to users:

1. Navigate to the _Azure Active Directory_ > _Enterprise applications_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ea3826-Enterprise_applications.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


2. Select the _CleverTap_ application.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/11871d8-Azure_CleverTap_Applications.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


3. Select _Users and groups_ under the _Manage_ section from the left navigation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c11bf9-User.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


3. Click **+ Add user/group** and assign the respective user and groups to the application using the options available at the top of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c3992a-Users_and_Groups.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


4. Select the user and click **Select**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0b8cde-Select_user_to_assign.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. Click  **Assign** to assign that user or group to the SAML application as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7af340b-Assign_application.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to the _Azure Active Directory_ > _Enterprise applications_. 
2. Select the _CleverTap_ application.
3. Select _Single Sign On._
4. You can upload the Certificate **(.CER )**file directly after downloading it using the _Download_ button, as shown in the image below. 
5. Copy the _Login URL_(also known as the Sign-in URL) from the _Set up CleverTap_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/faa0f0e-small-Azure_SAML_connection.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## GSuite Setup

Log in to <https://admin.google.com/> and log in as Admin for your app. The GSuite setup involves the following two major steps:

1. [Create a SAML app.](doc:single-sign-on-sso#create-a-saml-app)
2. [Map attributes.](doc:single-sign-on-sso#map-attributes-2)
3. [Assign the CleverTap application to the user.](doc:single-sign-on-sso#assign-clevertap-application-to-user-2)

### Create a SAML App

To create a SAML app:

1. From the Gsuite admin dashboard, navigate to _Home_ > _Apps_ > _Web and Mobile apps_.
2. From the  _Add app_ dropdown, select _Add custom SAML app_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/287aefd-Gsuite1.png",
        "Add Custom SAML App",
        2430
      ],
      "align": "center",
      "border": true,
      "caption": "Adding a Custom SAML App"
    }
  ]
}
[/block]


3. Enter the _App name_ (here, CleverTap) and _Description_ on the_ App details_ page and click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf6d256-gsuite_2.png",
        "Add App Name",
        "Add App Name and Desciption"
      ],
      "align": "center",
      "border": true,
      "caption": "Add App Name and Description"
    }
  ]
}
[/block]


4. Click **Continue** on the next screen (IdP metadata page).
5. Add the _ACS URL_ and _Entity ID_. (You can find these credentials on the _Create SAML connection_ page on the CleverTap dashboard)
6. Select  _Signed Response_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/268ab79-gsuite3.png",
        "Creating Custom SAML App",
        "Configure Service Provider Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Service Provider Details"
    }
  ]
}
[/block]


7. Select **EMAIL** as the _Name ID Format_ for the default _Name ID_ (_Basic Information > Primary email_).
8. Click **Continue**.

### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so, you must map the attributes:

1. Click _ADD MAPPING_ after the Attribute mapping screen appears.
2. Under the Attribute mapping section, you must appropriately map three attributes - _name_, _email_  , and _accountList_ and click **FINISH** (see figure below).  

> 📘 Note
> 
> If you proceed with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - _name_, _email_  in the attribute mapping section appropriately. You need not add any custom attributes and hence you must skip _step 3_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d7c848-attribute_mapping.png",
        "Attribute Mapping",
        2212
      ],
      "align": "center",
      "border": true,
      "caption": "Mapping accountList Attribute"
    }
  ]
}
[/block]


> 📘 Adding accountList Attribute
> 
> To populate _accountList_ in Google directory attribute, you must add a custom attribute.

3. To create a custom _accountList_ attribute:

   i. From the left panel, navigate to _Directory_ > _Users_ > _More options_ > _Manage custom attributes_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5249a0-gsuite_4.png",
        "Manage Custom Attributes",
        2346
      ],
      "align": "center",
      "border": true,
      "caption": "Manage Custom Attributes"
    }
  ]
}
[/block]


   ii. Click **ADD CUSTOM ATTRIBUTES**.

   iii. In the _Category_ field, enter the value as `accountList` and add the _Description_ as per your understanding.

   iv. Under Add custom fields, enter _accountList_ as the _Name_. 

   v. Set _Info Type_ as Text, _Visibility_ as Visible to the organization and _No. of values_ as Single value.

  vi. Click **Add**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ee5dff-gsuite_5.png",
        "Manage Custom Attributes",
        2362
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Assign CleverTap Application to User

To assign your CleverTap application to users,

1. Navigate to the _Users_ screen from the left panel. 
2. From the list of users, select the user name you want to assign.
3. Click the _User Information_ dropdown. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9aa2f0b-gsuite_6.png",
        "Gsuite User Information Panel",
        2940
      ],
      "align": "center",
      "border": true,
      "caption": "Assigning User"
    }
  ]
}
[/block]


4. In the accountList custom attribute, pass the accountID and click **Save**, as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b53b65f-Gsuite_7.png",
        "Pass AccountList Attribute",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Pass the Account ID"
    }
  ]
}
[/block]


5. From the left panel, navigate to _Apps_ > _Web and mobile apps_  and select your app. 
6. Click the _User access_ dropdown and set the service status to _ON for everyone_.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03dd716-gsuite_8.png",
        "User Access Panel",
        2910
      ],
      "align": "center",
      "border": true,
      "caption": "User Access View"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d93636-gsuite_9.png",
        "Toggle on Service Status",
        2830
      ],
      "align": "center",
      "border": true,
      "caption": "Turn On Service Status"
    }
  ]
}
[/block]


To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to _Apps_ > _Web and mobile apps_ from the left navigation menu
2. Select the CleverTap application.
3. Click _DOWNLOAD METADATA_ to display the _SSO URL_, _Entity ID_, and _Certificate_, as shown in the following figure. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e75dad-gsuite_10.png",
        "Download Metadata",
        2082
      ],
      "align": "center",
      "border": true,
      "caption": "Download Metadata"
    }
  ]
}
[/block]


4. Use these credentials to create a SAML connection on the CleverTap dashboard.

# Sign In Using SSO

After you complete the setup, your SSO is activated from the subsequent login. 

When you click **Continue** after entering the email, you are redirected to your IdP login page. After completing your authentication, you are redirected to your CleverTap dashboard again.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5558d2a-SSO.png",
        null,
        "Login Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Login Page"
    }
  ]
}
[/block]


Non-SSO users must enter their password after clicking **Continue**.

> 🚧 Revoke Users and Delete Connection
> 
> - To revoke a user from a project, you must remove the account list for the user from the IdP. If the account list is not removed from the IdP, the user continues to have access to the project. The revoking action on the dashboard only works if the account list for the user is updated on the IdP.
> 
> - When a SAML connection is deleted, users must reset their password by clicking **Forgot Password** on the login screen and creating a new password. They can use this new password for future login.