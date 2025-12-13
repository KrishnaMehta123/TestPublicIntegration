---
title: Two-Factor Authentication (2FA)
excerpt: Understand how 2FA configuration works on the CleverTap dashboard.
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

Keeping your data safe is of utmost importance. Two-Factor Authentication (2FA) adds extra security because it requires CleverTap Dashboard to provide a unique verification code from an authenticator app and their sign-in credentials when they log into the CleverTap.

> 📘 Important
>
> From December 01, 2022, all CleverTap projects will have mandatory 2FA enabled except for the projects that use Single-Sign On (SSO). For any questions, refer to [FAQs](doc:account-2fa#faqs).

# Set Up 2FA

Once 2FA is enabled, CleverTap generates a unique QR code for each user trying to log in.

<Image alt="Set-up Two factor Authentication" align="center" border={true} src="https://files.readme.io/098da8a-2fa_QR.png" /> Set up Two-factor Authentication

To set up 2FA:

1. Download the Google Authenticator app from Google [Play Store](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2\&hl=en_IN\&gl=US\&pli=1) or the Apple [App Store](https://apps.apple.com/us/app/google-authenticator/id388497605).
2. Scan the QR code.
3. Enter the verification code generated on the Authenticator app and click **Continue**.

Ensure that the device used for accessing CleverTap and the one with your authenticator app have synchronized time.

After this setup, for the subsequent login, you should enter the 2FA verification code from the *Authenticator* app, as shown in the following image:

<Image alt="Two Step Verification Screen" align="center" border={true} src="https://files.readme.io/e0d66e3-2fa_otp.png" /> Two-Step Verification Screen

# Reset the 2FA Key

> 📘 2FA Key Reset
>
> Only administrator of the respective dashboard can reset the 2FA key for their members.

If you cannot provide a verification code during log-in, either due to losing access to the Google Authenticator app or losing the device, raise a request to the dashboard administrator to reset their 2FA key from the dashboard.

To reset a 2FA key for a user, the administrator must perform the following steps:

1. Navigate to *Settings* > *Security* > *Two-Factor Authentication*. This displays the list of all user email addresses with 2FA enabled.

2. Click the icon <img src="https://files.readme.io/38f387c-image.png" height="15px" width="15px" /> icon adjacent to the user you want to reset the 2FA key.

<Image alt="Reset 2FA Key" align="center" border={true} src="https://files.readme.io/7e16dfd-2023-09-22_14-26-21_1.gif" /> Reset 2FA Key
After an administrator resets a key for a project, the user is prompted to set up 2FA on their next login, as shown in the following image:

<Image alt="Set up Authenticaor" align="center" width="400px" border={true} src="https://files.readme.io/83a0a40-scan_qr.png" /> Set up Authenticator











If none of the administrators can access the dashboard, raise a support ticket via [Help Center](https://help.clevertap.com/).

# FAQs

### What should I do if I do not have a verification code?

Contact the admin in your project to reset your 2FA key. After resetting, you can set up the 2FA authentication on your desired device.

### What should I do if I lose my device that had 2FA configured?

Contact the admin in your project to reset your 2FA key. After resetting, you can set up the 2FA authentication on your desired device.

### Why am I not able to toggle the project-level 2FA?

Two-factor authentication is mandatory for security reasons. If you face any issues, raise a support ticket from your CleverTap dashboard or contact your Customer Success Manager.

### Is 2FA applicable for SSO users?

SSO supersedes 2FA. A user will not be prompted for a 2FA verification code if SSO is enabled for their project.