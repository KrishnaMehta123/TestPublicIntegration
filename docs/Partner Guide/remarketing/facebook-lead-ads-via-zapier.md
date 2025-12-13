---
title: Facebook Lead Ads
excerpt: Remarketing
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

[Facebook Lead Ads](https://www.facebook.com/business/ads/ad-objectives/leads?content_id=XAfELRfAhjcIFGt\&ref=sem_smb\&utm_term=facebook%20lead%20ads\&gclid=Cj0KCQiAs5i8BhDmARIsAGE4xHyoZICtbNqcYlfRPUINl7F5pneZ0zGBJDRdP6W1I56jmU4YEVtTAv4aAsm0EALw_wcB\&gad_source=1) simplifies lead generation by allowing users to submit their information directly on Facebook or Instagram through pre-filled forms. Businesses can customize forms, integrate leads with CRMs, and retarget users for better conversion. This tool captures accurate leads quickly, improves engagement, and drives conversions efficiently.

Using Zapier to integrate Facebook Lead Ads with CleverTap, you can do the following:

* **Keep CRM Data Synchronized**: When a new lead submits a Facebook Lead Ad form, [create a user profile](doc:facebook-lead-ads-via-zapier#createupdate-user-profiles) in CleverTap with details such as name, email, phone number, and so on. 
* **Remove Converted Users from Re-Engagement Campaigns**: When a user converts through a Facebook Ad (for example, completes a purchase), [update the user profile](doc:facebook-lead-ads-via-zapier#createupdate-user-profiles) in CleverTap (example, mark the profile as *Converted*).
* **Track Lead Source**: When a new lead submits a Facebook Lead Ad form, [upload an event](doc:facebook-lead-ads-via-zapier#upload-event) in CleverTap with details such as event name, lead source, campaign name, and lead contact information. You can then use the event data to add the lead to a Facebook Audience for tailored retargeting ads.

# Prerequisites for Integration

The following are the prerequisites for Facebook Lead Ads:

* Ensure you have access to your Facebook Lead Ads account.
* Ensure you have access to an active Zapier account to create the CleverTap app.
* Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

# Integrate Facebook Lead Ads with CleverTap using Zapier

 The integration process involves the following two major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:facebook-lead-ads-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
2. [Create/Update User Information](doc:facebook-lead-ads-via-zapier#createupdate-user-profiles). OR\
   [Upload Event](doc:facebook-lead-ads-via-zapier#upload-event)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create/Update User Profiles

Consider an example where you want to automatically sync leads from Facebook Lead Ads with CleverTap to trigger personalized engagement campaigns. This automation ensures that new leads from Facebook Lead Ads are added to CleverTap while existing leads are updated when details change. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Facebook Lead Ads.

<Image alt="Create a Zap on Zapier Dashboard" align="center" border={true} src="https://files.readme.io/9b71c999e832d4a3344a2216c4e72dfaacf78feabca42da8617b0ec20d049f49-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select *Facebook Lead Ads* from the *App* section. This starts the Zap when a trigger event occurs on Facebook Lead Ads.
   2. Select *Trigger Event* from the dropdown list and then select *New Lead* for this use case.
   3. Select *Account* and sign in using your Facebook Lead Ads account credentials. You can also connect a new account if your account does not appear in the dropdown.
   4. Click **Continue**. From the *Configure* section, fill in the mandatory detail. 
   5. Select the Facebook *Page* connected to your lead form. If you cannot see your form, find the [Facebook Page ID](https://www.facebook.com/help/1503421039731588) and set it as a [custom value](https://help.zapier.com/hc/en-us/articles/8496241696141-Add-custom-values-to-modal-fields-in-Zaps).
   6. Click **Continue**.

<Image alt="Set Up Trigger Event" align="center" border={true} src="https://files.readme.io/46226dc404584a7539ee18fc8c492122af2b38fe1260224dae65a9cddf28bb91-facebook_2_.gif">
  Set Up Trigger Event
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue**.
5. **Select the Action the zap must perform after the trigger event occurs.** To do so, perform the following steps:
   1. Select *CleverTap* from the *App* event dropdown.
   2. Select *Create/Update User Profile* from the *Action event* dropdown. This implies that whenever a new lead is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. 
   4. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained in the [Create a Passcode on CleverTap Dashboard](doc:facebook-lead-ads-via-zapier#create-a-passcode-on-the-clevertap-dashboard) step.
   5. Click **Continue** after successfully connecting your account.

<Image alt="Select Action for Zap" align="center" border={true} src="https://files.readme.io/35644d684111c5dcca76a5cb5f77638b48ed60937452b7091894abb2df27f094-facebook_3.gif">
  Select Action for Zap 
</Image>

6. **Configure the Action**. Map Facebook Lead Ads data fields to CleverTap fields as follows:

| **CleverTap Field**    | **Facebook Lead Ads Field**                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------------------- |
| **Identity**           | Facebook Lead Ads user ID field, email ID, or any unique identity field corresponding to the user. |
| **Creation Date**      | Date of the user’s creation in Facebook Lead Ads.                                                  |
| **Profile Properties** | Include user properties in JSON format (such as name, email, role, and other custom properties).   |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" border={true} src="https://files.readme.io/83b8fb0575cf5980c48c5dde708603f244e32bc61f1a0d721cffd0558c1ffdba-fackbook.gif">
  Configure the Action
</Image>

7. Click **Continue** and click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, a new user is created, or an existing user is updated on the CleverTap dashboard every time a trigger occurs. CleverTap uses the *Identity* field to identify if it is a new user or an existing user. You can verify this by checking your CleverTap dashboard to confirm the user profile has been created or updated.

<Image alt="Verify user in CleverTap" align="center" border={true} src="https://files.readme.io/22d496be8a5e1407f768b1da28e7e73561e1f39613a71b5229193767f597293e-image.png">
  Verify user in CleverTap
</Image>

## Upload Event

Consider an example where you want to upload an event to CleverTap with details such as event name, lead source, campaign name, and lead contact information. every time a new lead submits a Facebook Lead Ad form. This automation ensures that user actions or events tracked in Facebook Lead Ads are automatically recorded in CleverTap, enabling better tracking and personalized engagement strategies. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up a Trigger**. For this example, perform the following steps:
   1. Select *Facebook Lead Ads* from the *App* section. This starts the Zap when a trigger event occurs in Facebook Lead Ads.
   2. Select *Trigger Event* from the dropdown list and select *New Lead* in this case.
   3. Select *Account* and **Sign in** with your Facebook Lead Ads account credentials. If your account does not appear in the dropdown, you can also connect a new account.
   4. Click **Continue**. From the *Configure* section, fill in the mandatory detail. 
   5. Select the Facebook *Page* connected to your lead form. If you cannot see your form, find the [Facebook Page ID](https://www.facebook.com/help/1503421039731588) and set it as a [custom value](https://help.zapier.com/hc/en-us/articles/8496241696141-Add-custom-values-to-modal-fields-in-Zaps).
   6. Click **Continue**.

<Image alt="Set Up Trigger Event" align="center" border={true} src="https://files.readme.io/46226dc404584a7539ee18fc8c492122af2b38fe1260224dae65a9cddf28bb91-facebook_2_.gif">
  Set Up Trigger Event
</Image>

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly.
4. Click **Continue**.
5. Select the Action that the zap must perform after the trigger event occurs.  To do so, perform the following steps:
   1. Select *CleverTap* from the *App* event dropdown.
   2. Select *Upload Event* from the Action *event* dropdown. This implies that whenever a new event is generated, a new user profile is created, and an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. For more information about how to do this, refer to *step 5 (iii)* under [Create or Update User Profiles](doc:facebook-lead-ads-via-zapier#create-a-passcode-on-the-clevertap-dashboard).
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select Action for Zap" align="center" border={true} src="https://files.readme.io/c1ac12024e1038a14fb29d41f2460b33052b62de41747ea02bab2b06d2609a22-zapes_1.gif">
  Select Action for Zap
</Image>

6. **Configure the Action**. Map Facebook Lead Ads data fields to CleverTap fields as follows:

| **CleverTap Field**  | **Facebook Lead Ads Field**                                                                                                  |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **User ID**          | Facebook Lead Ads user ID field, email ID, or any unique identity field corresponding to the user.                           |
| **Creation Date**    | Event creation date.                                                                                                         |
| **Event Name**       | Select a predefined event or create a custom event. You can also map the event name using the Facebook Lead Ads data fields. |
| **Event Properties** | Include metadata in JSON format (for example, event type, priority, event properties).                                       |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

<Image alt="Configure the Action" align="center" border={true} src="https://files.readme.io/589eac4fe997e8fc84129cf4bea864a76387125aa62dde61edbac686a807e052-last_b.gif">
  Configure the Action
</Image>

7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs. CleverTap uses the *Identity* field to identify if it is a new user or an existing user.

You can verify this by checking your CleverTap dashboard to confirm if the event has been logged.

<Image alt="Verify Events in CleverTap" align="center" border={true} src="https://files.readme.io/97691b0eb7a10b805c2f2ee8f7bdc6afe85fc94f39d0a43e6e8d04500e553eb6-image.png">
  Verify Events in CleverTap
</Image>

# FAQs

### What happens if I do not map the required fields?

Not mapping required fields may result in incomplete data being transferred or failure to update user profiles and events correctly.
