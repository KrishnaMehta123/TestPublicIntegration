---
title: Clearout
excerpt: Email Validator Partner
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

[Clearout](https://clearout.io/), an Email Verification and Email Finder tool, helps expand your reach, lower hard bounces, and improve deliverability rates. It is created to enhance sales and marketing efforts by simplifying how to discover and reach ideal prospects via email. This integration helps you solve the bounce rate issue and maintain the domain's reputation. 

To learn more about the Clearout and Clearout results file, refer to [Clearout documentation](https://clearout.io/help/). For any issues with this integration, contact [Clearout Support team](mailto:us@clearout.io).

# Prerequisites for Integration

The following are the prerequisites for this integration:

* You must have an account with Clearout.
* You must have an account with CleverTap.

# Integrate Clearout with CleverTap

This process involves the following four major steps:

1. [Connect CleverTap account](doc:clearout#connect-clevertap-account).
2. [Add the Email Lists](doc:clearout#add-email-list).
3. [Verify the Email Address List](doc:clearout#verify-email-list).
4. [Export the Verified Results](doc:clearout#export-verified-list).

## Connect CleverTap Account

To connect CleverTap account:

1. After logging in to the Clearout account, click the ![Menu](https://files.readme.io/298e857-menu_icon.png) icon and then select *Integrations* from the list.

<Image title="Navigating to Integrations page from Clearout dashboard" alt={1156} align="center" border={true} src="https://files.readme.io/04e27d1-Clearout_dashboard.png">
  Navigating to Integrations Page
</Image>

2. Scroll down and select *CleverTap* from the *Integrations* page and then click **Connect to CleverTap**.

<Image title="Select CleverTap from Integrations page and then click Connect to CleverTap" alt={276} align="center" width="smart" border={true} src="https://files.readme.io/8826dbd-Select_CleverTap.png">
  Click Connect to CleverTap
</Image>

3. Enter the following project details to authorize the connection:
   * **Account ID**: Enter your CleverTap Project ID.
   * **Account Passcode**: Enter your CleverTap passcode.
   * **Region**: Select the region of your CleverTap account.
   * **Account Name**: Enter the nickname to identify the account uniquely.

The above details can be obtained by navigating to the *Settings* > *Project* page on the CleverTap dashboard. To identify the region of your account, check the URL of your CleverTap account.

<Image alt="CleverTap Project Details" align="center" border={true} src="https://files.readme.io/4ca0240-Project_Details.png">
  CleverTap Project Details
</Image>

To identify the region for your account, refer to the following table:

| Dashboard URL                                                                                        | Region            |
| :--------------------------------------------------------------------------------------------------- | :---------------- |
| [https://eu1.dashboard.clevertap.com/login.html#/](https://eu1.dashboard.clevertap.com/login.html#/) | EU1               |
| [https://in1.dashboard.clevertap.com/login.html#/](https://in1.dashboard.clevertap.com/login.html#/) | India             |
| [https://us1.dashboard.clevertap.com/login.html#/](https://us1.dashboard.clevertap.com/login.html#/) | U.S               |
| [https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/) | Singapore         |
| [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html#/) | Indonesia         |
| [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html#/) | Middle East (UAE) |

## Add Email List

After the successful login, add the email list as follows:

1. Navigate to the *Email Verifier* tab from the Clearout dashboard.

<Image title="Navigating to Email Verifier tab to add email list for validation" alt={940} align="center" border={true} src="https://files.readme.io/12f6262-Select_Email_Verifier_tab.png">
  Navigating to Email Verifier Tab
</Image>

2. Select the email list from the existing CleverTap audience list for validation, and then click **Add to My List**. 

<Image title="Select the email list and click Add to My List" alt={3200} align="center" border={true} src="https://files.readme.io/200afc3-Add_to_My_lIst.png">
  Selecting the CleverTap Audience List for Validation
</Image>

## Verify Email List

To verify the email list, click **Verify** to start validating the added CleverTap list.

<Image title="Validate Audience list by clicking Verify from the Email Verifier page" alt={3200} align="center" border={true} src="https://files.readme.io/70f4586-Click_Verify.png">
  Click Verify to Validate Audience List 
</Image>

## Export Verified List

After the email validation is completed, the user can choose how to export the verified list to the CleverTap account. The user can export the result by choosing to unsubscribe or append or by selecting both.

* **Unsubscribe**: The user can unsubscribe the invalid/non-deliverable email addresses on the CleverTap list automatically, which removes all the non-deliverables from the mailing list.
* **Append**: The user can export the result and append the Clearout columns with the original file in the CleverTap account.

<Image title="Export the Verified Email list to CleverTap by clicking Export from the popup" alt={3200} align="center" src="https://files.readme.io/01eaec1-Export_Verified_List.png">
  Click Export
</Image>

# FAQs

**Q. How can I check whether the undeliverable user email addresses are handled in my CleverTap account?**\
Ans: CleverTap changes communication preferences to "Unsubscribed" for the users whose email addresses are marked as undeliverable by Clearout. You can check the same by going through the user profile under CleverTap and checking the communication preferences.

<Image title="Verify user Communication Preferences from the CleverTap dashboard" alt={2250} align="center" border={true} src="https://files.readme.io/fdd84f2-Communication_preferences.png">
  Verify Communication Preferences from CleverTap Dashboard
</Image>

**Q. How many lists can I validate at a time?**\
Ans: Three files can be validated simultaneously at a time.

**Q. Can I purchase credits from CleverTap?**\
Ans: No, you must purchase credits from [Clearout](https://app.clearout.io/dashboard/account/pricing) to validate your list.
