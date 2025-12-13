---
title: Single Sign On (SSO)
excerpt: >-
  Learn how to configure SSO for your CleverTap application using leading
  Identity Providers (IdPs).
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

Single Sign-On (SSO) enables users to log in to CleverTap using their organization's identity provider (IdP) instead of managing separate credentials. This enhances security, streamlines user authentication, and simplifies access management.

CleverTap supports SAML-based SSO, allowing organizations to integrate their preferred IdP. Once SSO is configured, users can authenticate via the Single Sign-On process.

# Prerequisites for SSO Setup

To use SSO with CleverTap, ensure that:

* You use an Identity Provider (IdP) or a custom SAML (Security Assertion Markup Language) implementation.
* You have an Admin access to the account.
* You configure SSO on the parent (production) account, not on a child account. Once SSO is set up on the parent account, it is automatically enabled for all associated child accounts.

> 📘 SSO Configuration for Test and Child Accounts
>
> If you attempt to configure SSO from a test or child account, you will not have access to the required *Organization* settings.

# Benefits of the SSO Configuration

Here are the benefits of migrating to the SAML SSO setup:

* Flexibility to manage users entirely on the CleverTap dashboard or by sending account lists through IDP and managing roles on the dashboard.
* Enhanced security and simplified login experience for your team through email domain whitelisting.

# Set Up SSO Configuration

The SSO Configuration process includes the following two major steps:

1. [Set up SSO configuration on CleverTap](doc:single-sign-on-sso#set-up-sso-configuration-on-clevertap).
2. [Configure CleverTap Application on your IdP](doc:single-sign-on-sso#configure-clevertap-application-on-your-idp)

## Set Up SSO Configuration in CleverTap

To set up the SSO configuration on the CleverTap dashboard:

1. Navigate to *Organization* > *SSO* from the CleverTap dashboard. 
2. Click **Create SAML Connection**. 

<Image alt="Create SAML Connection" align="center" border={true} src="https://files.readme.io/1926a21-Create_SAML_Connection.png">
  Create SAML Connection
</Image>

The *Create SAML Connection* window opens on the right side of the screen after you click **Create SAML Connection**, as shown in the following figure:

<Image alt="Enter Details to Create SAML Connection" align="center" border={true} src="https://files.readme.io/3585acc-SSO_Connection.png">
  Enter Details to Create SAML Connection
</Image>

3. Enter the following details:
   * *Sign-in URL*
   * *Organization name*
   * *IDP Signing certificate* (You can either paste the certificate details or upload the **.CER** file)
   * *SAML Eligible Email Domains*\
     In order to claim ownership of a domain, it is necessary for the organization to have at least one active user associated with that particular domain.

4. Click **Create**.

> 📘 Note
>
> * After you configure *Sign-in URL* and  *IDP Signing certificate*, these  details are available from your respective identity providers. For more information about IdP configuration, refer [Okta](doc:single-sign-on-sso#okta-setup), [OneLogin](doc:single-sign-on-sso#onelogin-setup), [Azure](doc:single-sign-on-sso#azure-setup) and [Gsuite](doc:single-sign-on-sso#gsuite-setup).
> * CleverTap recommends avoiding a word processor for copy-pasting sensitive values like certificates; instead, you can use an IDE or terminal.

After creating the SAML connection successfully, SAML Service Provider details are displayed on the page, as shown in the following figure:

<Image align="center" className="border" border={true} src="https://files.readme.io/5d6329d-SAML_Connection.png" />

5. Navigate to your respective IdP sections in the document and complete the steps mentioned to configure the connection.

> 📘 Configuration Updates
>
> The following are the updates related to CleverTap's SSO configurations process:
>
> * The IdP metadata XML is not accepted as a configuration parameter anymore.
> * The domain discovery now recognizes email domains. It means you can now log in through an IdP using a specific email address (for example, `employee@clevertap.com`) instead of organization names (for example, CleverTap). All users must provide their email addresses, and the system automatically determines if they use SAML or basic authentication.
> * All users must provide an email address on the new login page (the old login page still accepts the organization names).
>
> CleverTap strongly recommends adding your email domains rather than public ones or other organizations. If you encounter errors during configuration, it may be because the email domain is public (for example, gmail.com, outlook.com) or already claimed by another organization. Contact our support team if you encounter an issue and want to claim an email domain.

## Configure CleverTap Application on your IdP

To configure CleverTap on your IdP, you must map the attributes. The following are the two methods for attribute mapping:

* [Add a list of names and emails only (Recommended)](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended)
* [Send a list of attributes along with accountList and an array of accountIds](doc:single-sign-on-sso#send-a-list-of-attributes-along-with-accountlist-and-an-array-of-accountids).

Based on the selected attribute mapping logic and your IdP, map the attributes as illustrated for specific IdPs:

* [Attribute Mapping for Okta](doc:single-sign-on-sso#map-attributes)
* [Attribute Mapping for OneLogin](doc:single-sign-on-sso#map-attributes-1)
* [Attribute Mapping for Azure](doc:single-sign-on-sso#map-attributes-2)
* [Attribute Mapping for Gsuite](doc:single-sign-on-sso#map-attributes-3)

## Update Renewed SSO Certificate

When your Identity Provider (IdP) renews or rotates its SSO signing certificate, update the certificate in CleverTap to ensure uninterrupted access. To update the certificate, follow the steps below:

1. Go to *Organization* > *SSO* from the CleverTap dashboard and open your existing SAML connection. 
2. Click **Add new certificate**.

<Image alt="Add New Certificate" align="center" border={true} src="https://files.readme.io/24d634b4f8d2c4e72aa4580411ff7038dd4317bb8cb9f0dd43c1e2c8fd4bc23b-image.png">
  Add New Certificate
</Image>

3. In the *SAML Configuration*, select either of the following:

* *Upload Certificate*: Select the renewed certificate file from your computer, or
* *Paste Certificate*: Copy the certificate text from your IdP and paste it into the text box.

4. Click **Save** to apply the update.

<Image alt="Upload or Paste Certificate" align="center" border={true} src="https://files.readme.io/88675306833edb91510006818d99182337fee76c39ad4154ba1015bb6ff003d4-image.png">
  Upload or Paste Certificate
</Image>

> 📘 Note
>
> Check that the renewed certificate matches the SSO domains configured in CleverTap to maintain domain verification and prevent login disruptions.

# Identity Service Provider

Identity Provider (IdP) is an authority that verifies and asserts a user's identity and access to a requested resource (the "Service Provider"). Some examples of IdPs are Okta, GSuite, and so on.

# Attribute Mapping Logic for IdPs

You can set up your IdP attributes in the following two ways:

### Add a List of Names and Emails Only (Recommended)

Users onboarded before SAML SSO activation can continue to access their previous accounts. Users onboarded through SAML SSO for the first time are redirected to the no-access page and cannot access any accounts.

The user is onboarded to new accounts by sending an invitation to any account. Inviting a SAML user to an account may not send an email invite; instead, directly grant them access. However, the user needs to log out and then log in to view the new account assignments.

There are no organization-based checks in this method, as the provision of access is still in the hands of the admin of the target account.

### Send a List of attributes Along With *accountList* and an Array of accountIds

In this case, the user can only access the accounts mentioned in the `accountList` attribute. The invitation flow does not work for gaining access to any account. The account must be added to the `accountList`.  An additional check is performed on the accounts present in the accountList to validate if they belong to a family of accounts for which the current SAML SSO connection is configured. For example, if a connection is made for customer A and tries to pass the account Ids of customer B, they would be blocked.

The optional attribute `accountList` must be added in the following manner:\
accountList : \["1000000001", "1000000002", "1000000003"].

> 🚧 Note
>
> * If the user has access to any other account on the system apart from the ones present in the `accountList`, they would lose access to those accounts.
> * You must connect all your accounts to a parent account for which the SSO configuration is created.

# Configure IDPs

This section illustrates how to set up access for the following IDPs:

* [Okta](doc:single-sign-on-sso#okta-setup)
* [OneLogin](doc:single-sign-on-sso#onelogin-setup)
* [GSuite](doc:single-sign-on-sso#gsuite-setup)
* [Azure](doc:single-sign-on-sso#azure-setup)

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
2. Select *Applications* from the left navigation and click **Create App Integration.**

<Image title="Creating New Application in Okta" alt={2172} align="center" border={true} src="https://files.readme.io/562223c-okta.png">
  Creating New Application in Okta
</Image>

3. After the *Sign-in method* box appears, select *SAML 2.0*.

<Image title="New App Integration" alt={1746} align="center" border={true} src="https://files.readme.io/f88a5bc-Okta_1.png">
  New App Integration
</Image>

4. Enter your application details as shown in the image below and click **Next**:

<Image title="App Configuration on Okta" alt={1694} align="center" width="% " border={true} src="https://files.readme.io/fc8ca2a-Okta_2_-_App_details.png">
  App Configuration on Okta
</Image>

5. Add the Single sign-on URL and Audience URI(Entity ID) values. (You can find these credentials on the *Create SAML connection* page of the CleverTap dashboard).

<Image title="SAML Settings for Okta App" alt={1084} align="center" border={true} src="https://files.readme.io/022dc3e-Okta_2.png">
  SAML Settings for Okta App
</Image>

### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so, you must map the attributes:

1. Add three attributes - *name*, *email*  and *accountList* appropriately, and map the attributes accordingly as shown in the image below:

> 📘 Note
>
> If you proceed further with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - *name*, *email*  in the attribute mapping section appropriately. You need not add any custom attributes and hence you must skip *step 2*.

<Image title="Attribute Mapping" alt={1166} align="center" border={true} src="https://files.readme.io/ebe57ff-okta_3_attributes.png">
  Attribute Mapping
</Image>

2. For the *accountList* attribute, you must create a custom attribute: 

   i. Navigate to *Directory* > *Profile editor* > Select your application (CleverTap).\
   ii. Click **+ Add Attributes**.

<Image title="Add Attributes" alt={2416} align="center" border={true} src="https://files.readme.io/eba29d1-add_attribute.png">
  Add Attributes
</Image>

  iii. Define all the attribute values for `accountList`.

<Image title="Add Account Attributes" alt={1086} align="center" className="border" width="80%" border={true} src="https://files.readme.io/9c0426e-add_account_list_attribute.png" />

 iv. Click **Save**

### Assign CleverTap Application to User

To assign your CleverTap application to users:

1. Navigate to *Applications* > Select your application.
2. Select *Assign to People* from the *Assign* dropdown.

<Image title="Assigning an Applications to Users" alt={1356} align="center" border={true} src="https://files.readme.io/a9f24f2-assign.png">
  Assigning an Applications to Users
</Image>

3. Select the user you want to assign and click *Assign*

<Image title="Assign an Application to Users" alt={1646} align="center" border={true} src="https://files.readme.io/c2b07ad-assign_users.png">
  Assign an Application to Users
</Image>

4. Ensure that the `accountList` value is populated against the accountList attribute in the dropdown. 

<Image title="Account list Attribute Mapping" alt={658} align="center" border={true} src="https://files.readme.io/a103b02-assign.png">
  Account list Attribute Mapping
</Image>

5. Click **Save and Go Back** and then click **Done**.

To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to *Applications* > *Sign on*
2. Click **View SAML Setup** instruction available at the bottom right of the page. You can find the credentials as shown in the following figure:

<Image title="Credentials for SAML Connection" alt={812} align="center" border={true} src="https://files.readme.io/daad644-SAML_.png">
  Credentials for SAML Connection
</Image>

4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## OneLogin Setup

This section provides information about the OneLogin setup. The process involves the following major steps:

1. [Create an application.](doc:single-sign-on-sso#create-an-application-1)
2. [Map Attributes.](doc:single-sign-on-sso#map-attributes-1)
3. [Assign the CleverTap application to the user.](doc:single-sign-on-sso#assign-clevertap-application-to-user-1)

### Create an Application

To create an application:

1. Select *Applications* tab and select *Applications* from the menu.

<Image title="Create a New OneLogin Application" alt={1474} align="center" border={true} src="https://files.readme.io/7179a7d-one_login_1.png">
  Create a New OneLogin Application
</Image>

2. Click **Add App** and search for *SAML Custom Connector (Advance)* in the search bar.

<Image title="Create a New OneLogin Application" alt={1566} align="center" border={true} src="https://files.readme.io/7d69db6-1.png">
  Create a New OneLogin Application
</Image>

3. Select *SAML Custom Connector (Advance)* and enter the *Display Name*.  

<Image title="Add SAML Custom Connector" alt={832} align="center" border={true} src="https://files.readme.io/c039dd3-2.png">
  Add SAML Custom Connector
</Image>

4. Click **Save**.

5. From the left panel,  navigate to the *Configuration* section and enter the *ACS (Consumer) URL* and *Audience (EntityID).* (You can find these credentials on the Create SAML connection page of the CleverTap dashboard).

<Image title="Configure Custom Connector" alt={2614} align="center" border={true} src="https://files.readme.io/61ffd10-SSO_CTD.png">
  Configure Custom Connector
</Image>

### Map Attributes

After configuring the application, ensure that correct values are passed to CleverTap by mapping the attributes:

1. From the left menu under *Applications* tab, navigate to the *Parameter* section and click the **+** sign to add new fields and ensure that the *Configured by admin* button is selected.

2. Add three attributes - *name*, *email*  and *accountList* appropriately, and map the attributes accordingly as shown below:

> 📘 Note
>
> If you proceed further with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - *name*, *email*  in the attribute mapping section appropriately. You do not need to add any custom attributes and hence you must skip *step 4*.

<Image title="Map Attributes" alt={2880} align="center" border={true} src="https://files.readme.io/d17448a-Screenshot_2023-02-14_at_8.17.17_PM.png">
  Map Attributes
</Image>

3. Add value as *FirstName* and *Email* for Name and Email, respectively, and click **Save**.

4. a. Add *accountList* as *Name*  and click **Save**.

   b. Select *Value* as *Macro* from the dropdown and pass the account ID.

<Image title="Map Custom Attribute" alt={2880} align="center" border={true} src="https://files.readme.io/9df9451-Screenshot_2023-02-14_at_8.16.08_PM.png">
  Map Custom Attribute
</Image>

> 📘 Note
>
> Ensure that you select the *Include in SAML assertion* when adding all three attributes as shown in the  figure above.

### Assign CleverTap Application to User

To assign your CleverTap application to users: 

1. Navigate to *Users* from the top panel and click **Users**.

<Image title="User Assignment" alt={2880} align="center" border={true} src="https://files.readme.io/9f42d6e-users.png">
  User Assignment
</Image>

2. Select the user you want to assign to the CleverTap application. 

<Image title="Assign an Application to Users" alt={2880} align="center" border={true} src="https://files.readme.io/ab0626a-Screenshot_2023-02-14_at_8.33.58_PM.png">
  Assign an Application to Users
</Image>

The *User Info* page opens:

<Image title="User Profile" alt={2880} align="center" border={true} src="https://files.readme.io/f85c617-Screenshot_2023-02-14_at_8.34.15_PM.png">
  User Profile
</Image>

3. Navigate to applications from the left panel, click **+**, and select CleverTap from the dropdown.
4. Click **Continue**
5. Verify all the values passed for that user from the *Edit CleverTap Login* page and click **Save**

Now, you have successfully assigned the CleverTap application to the user.

To create a SAML connection on the CleverTap dashboard, you need two credentials, as mentioned in the beginning. To find your *Sign-in URL* and *IDP Signing certificate*:

1. Navigate to the *Applications* tab from the top panel, and select the CleverTap application
2. Navigate to *SSO* from the left navigation and copy the *SAML 2.0 Endpoint(HTTP)* for the SAML connection on CleverTap.

<Image title=" View SAML 2.0 Endpoint" alt={2880} align="center" border={true} src="https://files.readme.io/c739f80-saml_2.0.png">
  SAML 2.0 Endpoint
</Image>

3. Click **View Details** for the IDP signing certificate  as shown below:

<Image title="View IDP Signing Certificate" alt={2880} align="center" border={true} src="https://files.readme.io/71b5bd0-certificate.png">
  View IDP Signing Certificate
</Image>

<Image title="Copy IDP Signing Certificate" alt={2880} align="center" border={true} src="https://files.readme.io/56b01bc-certificate_detail.png">
  Copy IDP Signing Certificate
</Image>

4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## Azure Setup

This section provides information about the Azure setup. The process involves the following major steps:

* [Create an application](doc:single-sign-on-sso#create-an-application-2).
* [Map the attributes.](doc:single-sign-on-sso#create-an-application-2)
* [Assign the CleverTap application to the user](doc:single-sign-on-sso#map-attributes-2).

### Create an Application

1. Start the setup by signing up and creating a CleverTap app on the [Azure Portal ](https://portal.azure.com/)
2. From the left navigation panel, select *Azure Active Directory.*

<Image title="a1.png" alt={1734} align="center" className="border" border={true} src="https://files.readme.io/b1b6307-a1.png" />

3. Click *+ Add*  and select *Enterprise application*

<Image title="az1.png" alt={1890} align="center" className="border" border={true} src="https://files.readme.io/2981515-az1.png" />

5. Click **+ Create your application**.
6. Enter the name of the application.
7. Select the *Non-gallery application* option as shown in the following image and click **Add**. 

<Image title="image (4).png" alt={2816} align="center" className="border" border={true} src="https://files.readme.io/7dcdffd-image_4.png" />

5. Click **Set up single sign on** . 

<Image title="image (5).png" alt={2282} align="center" className="border" border={true} src="https://files.readme.io/2a58404-image_5.png" />

 The *Single sign-on* page opens. 

6. Click  **SAML**.

<Image title="saml.png" alt={2864} align="center" className="border" border={true} src="https://files.readme.io/0286a85-saml.png" />

7. Click the *Edit* icon available next to *Basic SAML configuration*.

<Image title="SAML1.png" alt={1794} align="center" className="border" border={true} src="https://files.readme.io/3e3ae05-SAML1.png" />

8. Add the *ACS* and *Entity ID*. You can find these credentials on the *Create SAML connection* page on CleverTap. To get these credentials:
   1. Navigate to *Organization* > *SSO* from the CleverTap dashboard. 
   2. Copy the *Entity ID* and *Assertion Consumer Service URL*>*Create SAML Connection*.
9. Paste the respective values into the SAML configuration section as shown in the following screenshot and click **Save**.

<Image align="center" className="border" border={true} src="https://files.readme.io/06684f2-SAML_Configuration_Azure.png" />

### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so:

1. Under the *Attribute & Claims* section, you must map the following two attributes: name and email appropriately and click **Save** (see following figure image below).

<Image align="center" className="border" border={true} src="https://files.readme.io/1d6b809-small-Azure_Attributes.png" />

> 📘 Note
>
> If you proceed further with the [recommended method](https://docs.clevertap.com/docs/single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), you need not add any custom attributes and hence you must skip *step 2*.

2. Refer to this [Azure support document](https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-feature-directory-extensions) to create a `accountList` custom attribute.

### Assign CleverTap Application to User

To assign your CleverTap application to users:

1. Navigate to the *Azure Active Directory* > *Enterprise applications*.

<Image align="center" className="border" border={true} src="https://files.readme.io/7ea3826-Enterprise_applications.png" />

2. Select the *CleverTap* application.

<Image align="center" className="border" border={true} src="https://files.readme.io/11871d8-Azure_CleverTap_Applications.png" />

3. Select *Users and groups* under the *Manage* section from the left navigation.

<Image align="center" className="border" border={true} src="https://files.readme.io/3c11bf9-User.png" />

3. Click **+ Add user/group** and assign the respective user and groups to the application using the options available at the top of the screen.

<Image align="center" className="border" border={true} src="https://files.readme.io/3c3992a-Users_and_Groups.png" />

4. Select the user and click **Select**. 

<Image align="center" className="border" border={true} src="https://files.readme.io/e0b8cde-Select_user_to_assign.png" />

5. Click  **Assign** to assign that user or group to the SAML application as shown in the following figure:

<Image align="center" className="border" border={true} src="https://files.readme.io/7af340b-Assign_application.png" />

To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to the *Azure Active Directory* > *Enterprise applications*. 
2. Select the *CleverTap* application.
3. Select *Single Sign On.*
4. You can upload the Certificate **(.CER )**&#x66;ile directly after downloading it using the *Download* button, as shown in the image below. 
5. Copy the *Login URL*(also known as the Sign-in URL) from the *Set up CleverTap* section.

<Image align="center" className="border" border={true} src="https://files.readme.io/faa0f0e-small-Azure_SAML_connection.png" />

4. Use these credentials to create a SAML connection on the CleverTap dashboard. 

## GSuite Setup

Log in to [https://admin.google.com/](https://admin.google.com/) and log in as Admin for your app. The GSuite setup involves the following two major steps:

1. [Create a SAML app.](doc:single-sign-on-sso#create-a-saml-app)
2. [Map attributes.](doc:single-sign-on-sso#map-attributes-2)
3. [Assign the CleverTap application to the user.](doc:single-sign-on-sso#assign-clevertap-application-to-user-2)

### Create a SAML App

To create a SAML app:

1. From the Gsuite admin dashboard, navigate to *Home* > *Apps* > *Web and Mobile apps*.
2. From the  *Add app* dropdown, select *Add custom SAML app*.

<Image title="Add Custom SAML App" alt={2430} align="center" border={true} src="https://files.readme.io/287aefd-Gsuite1.png">
  Adding a Custom SAML App
</Image>

3. Enter the *App name* (here, CleverTap) and *Description* on the *App details* page and click **Continue**.

<Image title="Add App Name" alt="Add App Name and Desciption" align="center" border={true} src="https://files.readme.io/bf6d256-gsuite_2.png">
  Add App Name and Description
</Image>

4. Click **Continue** on the next screen (IdP metadata page).
5. Add the *ACS URL* and *Entity ID*. (You can find these credentials on the *Create SAML connection* page on the CleverTap dashboard)
6. Select  *Signed Response*.

<Image title="Creating Custom SAML App" alt="Configure Service Provider Details" align="center" border={true} src="https://files.readme.io/268ab79-gsuite3.png">
  Configure Service Provider Details
</Image>

7. Select **EMAIL** as the *Name ID Format* for the default *Name ID* (*Basic Information > Primary email*).
8. Click **Continue**.

### Map Attributes

In continuation of the above configuration, ensure that the correct values are passed to CleverTap. To do so, you must map the attributes:

1. Click *ADD MAPPING* after the Attribute mapping screen appears.
2. Under the Attribute mapping section, you must appropriately map three attributes - *name*, *email*  , and *accountList* and click **FINISH** (see figure below).  

> 📘 Note
>
> If you proceed with the [recommended method](doc:single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), add only two attributes - *name*, *email*  in the attribute mapping section appropriately. You need not add any custom attributes and hence you must skip *step 3*.

<Image title="Attribute Mapping" alt={2212} align="center" border={true} src="https://files.readme.io/7d7c848-attribute_mapping.png">
  Mapping accountList Attribute
</Image>

> 📘 Adding accountList Attribute
>
> To populate *accountList* in Google directory attribute, you must add a custom attribute.

3. To create a custom *accountList* attribute:

   i. From the left panel, navigate to *Directory* > *Users* > *More options* > *Manage custom attributes*.

<Image title="Manage Custom Attributes" alt={2346} align="center" border={true} src="https://files.readme.io/e5249a0-gsuite_4.png">
  Manage Custom Attributes
</Image>

   ii. Click **ADD CUSTOM ATTRIBUTES**.

   iii. In the *Category* field, enter the value as `accountList` and add the *Description* as per your understanding.

   iv. Under Add custom fields, enter *accountList* as the *Name*. 

   v. Set *Info Type* as Text, *Visibility* as Visible to the organization and *No. of values* as Single value.

  vi. Click **Add**.

<Image title="Manage Custom Attributes" alt={2362} align="center" className="border" border={true} src="https://files.readme.io/7ee5dff-gsuite_5.png" />

### Assign CleverTap Application to User

To assign your CleverTap application to users,

1. Navigate to the *Users* screen from the left panel. 
2. From the list of users, select the user name you want to assign.
3. Click the *User Information* dropdown. 

<Image title="Gsuite User Information Panel" alt={2940} align="center" border={true} src="https://files.readme.io/9aa2f0b-gsuite_6.png">
  Assigning User
</Image>

4. In the accountList custom attribute, pass the accountID and click **Save**, as shown in the following image:

<Image title="Pass AccountList Attribute" alt={2880} align="center" border={true} src="https://files.readme.io/b53b65f-Gsuite_7.png">
  Pass the Account ID
</Image>

5. From the left panel, navigate to *Apps* > *Web and mobile apps*  and select your app. 
6. Click the *User access* dropdown and set the service status to *ON for everyone*.  

<Image title="User Access Panel" alt={2910} align="center" border={true} src="https://files.readme.io/03dd716-gsuite_8.png">
  User Access View
</Image>

<Image title="Toggle on Service Status" alt={2830} align="center" border={true} src="https://files.readme.io/8d93636-gsuite_9.png">
  Turn On Service Status
</Image>

To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to *Apps* > *Web and mobile apps* from the left navigation menu
2. Select the CleverTap application.
3. Click *DOWNLOAD METADATA* to display the *SSO URL*, *Entity ID*, and *Certificate*, as shown in the following figure. 

<Image title="Download Metadata" alt={2082} align="center" border={true} src="https://files.readme.io/8e75dad-gsuite_10.png">
  Download Metadata
</Image>

4. Use these credentials to create a SAML connection on the CleverTap dashboard.

# Sign In Using SSO

After you complete the setup, your SSO is activated from the subsequent login. 

When you click **Continue** after entering the email, you are redirected to your IdP login page. After completing your authentication, you are redirected to your CleverTap dashboard again.

<Image alt="Login Page" align="center" border={true} src="https://files.readme.io/5558d2a-SSO.png">
  Login Page
</Image>

Non-SSO users must enter their password after clicking **Continue**.

> 🚧 Revoke Users and Delete Connection
>
> * To revoke a user from a project, you must remove the account list for the user from the IdP. If the account list is not removed from the IdP, the user continues to have access to the project. The revoking action on the dashboard only works if the account list for the user is updated on the IdP.
>
> * When a SAML connection is deleted, users must reset their password by clicking **Forgot Password** on the login screen and creating a new password. They can use this new password for future login.
