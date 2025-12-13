---
title: AppsFlyer OneLink
excerpt: ''
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

Deep linking gives your app users the most seamless experience possible by securely and contextually guiding them to In-App information.

CleverTap automatically wraps all links in the email body to track clicks. When a user clicks on any of the links in the email, this may lead to multiple redirects. Turning off click tracking for deep links is one option for marketers who want to send users straight to the content.

The other option is to leverage the AppsFlyer OneLink with branded links. Doing so can give your app users the greatest experience possible by directing them to a specific landing page, app store, or in-app content. All this while, CleverTap tracks the click and assists in boosting conversion rates.

<Image title="CleverTap + AppsFlyer Integration New Scenario" alt={3840} align="center" width="smart" border={true} src="https://files.readme.io/c7cedb7-CT_AF_Integration.png">
  AppsFlyer OneLink Integration
</Image>

# Set Up AppsFlyer OneLink(s)

 AppsFlyer has updated its integration process. This requires existing users to set up the integration with AppsFlyer again, as they have deprecated the old integration.

> 📘 Closed Beta
>
> AppsFlyer has released this integration in Closed Beta. The integration steps outlined in the document apply only if you are using the SendGrid as the provider. To enable this integration, contact AppsFlyer Support.

If you are an existing customer who has already set up AppsFlyer OneLink integration with CleverTap in the past, go to *Settings* > *Channel* > *Email* > *Advanced Setup* and remove all the OneLink URLs added under *AppsFlyer OneLink*, as those are related to the older integration.

<Image alt="Delete OneLink URLs from CleverTap Dashboard" align="center" border={true} src="https://files.readme.io/5bd0865ba24a91d4298f625a073fb35f3791c867732fd591f9265d7a01f25808-Delete_OneLink_URL.gif">
  Delete OneLink URLs from CleverTap Dashboard
</Image>

## Prerequisites

The following are the prerequisites before you set up the AppsFlyer OneLink:

1. Create a new click-tracking domain link branding on your provider dashboard, such as `click.client.com`. For example, if you are using SendGrid, you can refer to [Set Up Link Branding](https://docs.sendgrid.com/ui/account-and-settings/how-to-set-up-link-branding) to create a new click-tracking domain. If you are an existing user, you can continue using your current click-tracking domain from SendGrid and update the CNAME records as needed. For more information, refer to *Step 8* of [Integrate CleverTap with AppsFlyer Dashboard ](doc:appsflyer-onelink#integrate-clevertap-with-appsflyer-dashboard).
2. [Create a OneLink Template](https://support.appsflyer.com/hc/en-us/articles/207032246#procedures). 
3. Configure the app to support the following:
   1. [App Association Files](doc:appsflyer-onelink#configure-app-to-support-app-association-files).
   2. [Deeplinking](doc:appsflyer-onelink#configure-app-to-support-deeplinking).
   3. [App Links or Web Links](doc:appsflyer-onelink#configure-app-to-support-esp-app-links-or-web-links).

### Configure App to Support App Association Files

AppsFlyer hosts app association files for your app to enable Universal Links (iOS) or App Links (Android). Follow the steps below to configure your app to access these files:

* **For iOS**: Configure the SDK to support an Apple App Site Association (AASA) file, enabling [Universal Linking](https://support.appsflyer.com/hc/en-us/articles/360000732237#universal-links) from the email message to your app. To do so:

  1. Select your project from the Xcode and select the *Capabilities* tab.
  2. Toggle ON *Associated Domains* and click + (plus), enter your click domain. For example,\<applinks:click.example.com>.

     <Image alt="Configure SDK to Support an AASA file" align="center" border={true} src="https://files.readme.io/78a28ba-image.png">
       Configure SDK to Support an AASA file
     </Image>
* **For Android**: Configure the app to support the Digital Assets Links (DAL) file, enabling [App Linking](https://support.appsflyer.com/hc/en-us/articles/360000732237#universal-links) from the email message to your app. In the Android manifest, add the click domain and the required prefix to the activity tag of the activity you want to link to, as shown in the following sample XML code:

  ```xml
  <activity android:name=".DeepLinkActivity">
                <intent-filter android:autoVerify="true">
                          <action android:name="android.intent.action.VIEW" />
                                   <category android:name="android.intent.category.DEFAULT" />
                                   <category android:name="android.intent.category.BROWSABLE" />
                                   <data android:scheme="https"
                                    android:host="click.example.com"
                                    android:pathPrefix="/campaign" />
                   </intent-filter>
      </activity>
  ```

  <br />

### Configure App to Support Deeplinking

When a user clicks on an App Link or Universal Link, the user is directed to a specific In-App activity (for example, a specific page in the app) as soon as the app opens. To enable the app to process the deeplink correctly, follow the steps listed below:

1. **Set Up the Click Recording Domain**:\
   Provide the click recording domain to the SDK API `resolveDeepLinkURLs`. Ensure to call this API before initializing the SDK.
   * For Android
     ```java
     public static final String[] ESP_DOMAINS = {
                 "click.example.com"
         };
     ```
   * For iOS
     ```objectivec
     [[AppsFlyerLib shared] resolveDeepLinkURLs = @[@"click.example.com"];
     ```
2. **Extract and Handle Deep Link Data**:\
   Use the `onAppOpenAttribution` API to fetch the deeplink parameters and handle the deep link data.

For more information about SDK deeplinking, refer to the following documents:

* [Android Unified Deep Linking](https://dev.appsflyer.com/hc/docs/dl_android_unified_deep_linking)
* [iOS Unified Deep Linking](https://dev.appsflyer.com/hc/docs/dl_ios_unified_deep_linking)

### Configure App to Support App Links or Web Links

When a user clicks on an App Link or Universal Link, you must regulate the functionality of wrapped links within an email campaign. You specifically address two types: weblinks intended to open a website and links designed to open the app through a universal link or App link.

For more information, refer to the following:

* [iOS Deep Linking ESP 2.0](https://dev.appsflyer.com/hc/docs/dl_ios_esp_2_setup)
* [Android Deep Linking ESP 2.0](https://dev.appsflyer.com/hc/docs/dl_android_esp_2_setup)

## Integrate CleverTap with AppsFlyer Dashboard

To integrate CleverTap with AppsFlyer:

1. Go to *Engage* > *ESP integration* from the ESP dashboard. 

<Image alt="Integrate ESP with AppsFlyer dashboard" align="center" width="25% " border={true} src="https://files.readme.io/c369366c65ef36c5bb45731970b9708de32258a73f3b8ddf5274d5aff566e4a0-image.png">
  Integrate ESP with AppsFlyer dashboard
</Image>

2. Select *CleverTap* from the ESP section to set up the integration.

<Image alt="Select your ESP for Setting Up Integration" align="center" width="65% " border={true} src="https://files.readme.io/aadba290bf5d1b3ec157261e5c806258bb316d2ffe20041fc744decb9d0302c4-image.png">
  Select your ESP for Setting Up Integration
</Image>

3. Select the Onelink *Template ID*, created on the AppsFlyer dashboard, to use for email campaigns.

<Image alt="Select OneLink Template" align="center" width="50% " border={true} src="https://files.readme.io/7a9b929e9bd48ffd35a01a3ca7c67d231e310460dd94f336df9c82cb0910351e-image.png">
  Select OneLink Template
</Image>

4. Click **Next**.
5. Enter the click tracking domain (for example, `click.example.com`) and CleverTap server endpoint. To know the server endpoint for your region, refer to the following table:

   <br />

   | Region            | CleverTap Server Endpoint                                | CleverTap Dashboard URL                                                                                |
   | :---------------- | :------------------------------------------------------- | :----------------------------------------------------------------------------------------------------- |
   | Europe            | [wizrocketmail.net](https://wizrocketmail.net)           | [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html)       |
   | India             | [in1.wizrocketmail.net](https://in1.wizrocketmail.net)   | [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html)       |
   | Singapore         | [sg1.wizrocketmail.net](https://sg1.wizrocketmail.net)   | [https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/)   |
   | United States     | [us1.wizrocketmail.net](https://us1.wizrocketmail.net)   | [https://us1.dashboard.clevertap.com/login.html#/](https://us1.dashboard.clevertap.com/login.html#/)   |
   | Middle East (UAE) | [mec1.wizrocketmail.net](http://mec1.wizrocketmail.net)  | [https://mec1.dashboard.clevertap.com/login.html#/](https://mec1.dashboard.clevertap.com/login.html#/) |
   | Indonesia         | [aps3.wizrocketmail.net](https://aps3.wizrocketmail.net) | [https://aps3.dashboard.clevertap.com/login.html#/](https://aps3.dashboard.clevertap.com/login.html#/) |

<Image alt="Enter Click Tracking Domain and CleverTap Endpoint" align="center" width="50% " border={true} src="https://files.readme.io/89cb63c61b53a0f825c45665d642074de3cbd7d9e9fac7674e99dd78f279ba9a-Enter_Click_Tracking_Domain_and_CleverTap_Endpoint.png">
  Enter Click Tracking Domain and CleverTap Endpoint
</Image>

6. Click **Validate connection** to ensure that the domain points to the correct endpoint.
7. Click **Next** when done.
8. Configure Link Redirection to AppsFlyer. To do so, copy and send the customized pre-fabricated instructions in AppsFlyer to your IT or domain administrator. They will need to reroute your email campaign traffic from the ESP servers to the AppsFlyer servers by updating your DNS CNAME records with the new domain provided by AppsFlyer.\
   As a result, every time a link is clicked, the click will be redirected to AppsFlyer, which in turn will redirect it to the CleverTap server endpoint.

<Image alt="Link Redirection to AppsFlyer " align="center" width="65% " border={true} src="https://files.readme.io/41ccdb2c2768706263d52dfe732e93f8fc030cf3797c4cb4f18ca163495eaf9c-Route_Link_Traffic_to_AppsFlyer.png">
  Link Redirection to AppsFlyer 
</Image>

> 📘 Note
>
> * The ESP integration status will be currently displayed as *Pending* and will only start working after mapping the CNAME record.
> * It can take up to 24 hours after mapping for a new integration to start working and become active.

5. Customize the OneLink URL for your email campaign.
   1. [Create a OneLink URL](https://support.appsflyer.com/hc/en-us/articles/208874366-Create-a-OneLink-link#create-a-onelink-link) from the *OneLink management* page (or manually). 
   2. Add Recommended Parameters in the URL as query parameters:
      * pid (media source): Use a media source such as Email to signify this usage. This helps in viewing all related data in the AppsFlyer dashboard.
      * c (campaign): Add the campaign name.\
        af\_web\_dp: Specify where to redirect users clicking the link on a desktop.
      * af\_ios\_url: Specify where to redirect iOS users who do not have the app.
      * af\_android\_url: Specify where to redirect Android users who do not have the app.
      * is\_retargeting=true: Add this parameter to indicate that the link is from a retargeting campaign, which is essential for universal app opens. For more information, refer to [Retargeting Attribution Guide](https://support.appsflyer.com/hc/en-us/articles/207033786-Retargeting-attribution-guide)
   3. Ensure that all parameter values are URL-encoded.

> 📘 Note
>
> You need not turn off click tracking from your CleverTap or SendGrid for OneLink redirection to function as intended. CleverTap and SendGrid will receive the click data directly from AppsFlyer.

> ❗️ Invalid AppsFlyer Branded OneLink
>
> AppsFlyer does not send the click data for invalid OneLink URLs configured in an Email campaign to CleverTap.
