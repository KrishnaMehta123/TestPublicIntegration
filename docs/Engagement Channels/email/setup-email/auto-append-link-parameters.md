---
title: Auto-Append Link Parameters
excerpt: Discover how you can append tracking parameters to URLs in email campaigns.
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

> 📘 Private Beta
>
> Currently, this feature is released in Private Beta. if you want to access this feature, contact your Customer Success Manager (CSM).

The Auto-append Link Parameters feature simplifies adding UTM or other tracking parameters to URLs in your email campaigns. Automatically appending the required parameters to all links eliminates the need for manual input, ensuring each link is properly tagged with just one click. This makes tracking and analyzing campaign performance easier and provides valuable insights into user engagement and behavior.

Auto-append link parameters allow personalized link tracking through the following parameters: 

* **Global Link Parameters**: These are key parameters that you can append to links in most email campaigns. Examples of global link parameters include`utm_source`, `utm_medium`, `utm_campaign`, and so on. These parameters help attribute conversions to specific track traffic sources, user engagement, and conversions, providing valuable insights into campaign performance. As a result, they help marketers refine their strategies and optimize future efforts for better results.
* **Custom Link Parameters**: These are additional parameters added to links only to a specific campaign. Depending on your tracking requirements, you can use them with or without global link parameters.

You can also personalize link parameters to tailor links for each user separately while tracking campaign performance more effectively. For example, a link might display "View Profile, \{\{ Profile.name | default:'ABC' }}", where `Profile.name` is replaced with the user's actual name (or defaults to "ABC" if not available), and `campaign_id` to associate it with a specific campaign. This will personalize the user experience and provide deeper insights into the performance of individual campaigns.

# Auto-Append Parameters to URLs

This process involves the following two main steps:

1. [Set Up Global Link Parameters on the CleverTap dashboard](doc:auto-append#set-up-global-link-parameters).
2. [Append Link Parameters to Email Links](doc:select-parameters-to-append-for-email-campaign-links).

## Set Up Global Link Parameters

To append parameters to the link in the email campaign, you must set up the parameters on the CleverTap dashboard:

1. Go to *Settings > Channels > Email > Advance Setup page* to add a new Global Link Parameter.

<Image alt="Advance Setup" align="center" border={true} src="https://files.readme.io/20c642d-Auto_append_setup.png">
  Advance Setup
</Image>

2. Click **Global Link Parameters** and click **Add Link Parameter**. 

<Image alt="Add Link Parameters" align="center" border={true} src="https://files.readme.io/42965ba-Auto_append_2.png">
  Add Link Parameters
</Image>

3. Pair the Key with a Value. You can use **@Personalization** or **Liquid Tags** to fetch a personalized value for the key. You can personalize global link parameters with user properties and campaign ID.

<Image alt="Pair Key Value" align="center" width="50% " border={true} src="https://files.readme.io/9340454-Auto_append_add_link.png">
  Pair Key Value
</Image>

> 📘 Campaign ID Personalization
>
> When using Campaign ID personalization, the default value is applied to the parameter when sending test messages.

4. Enable the parameter to make it available for appending and tracking in all future scheduled campaigns.

<Image alt="Enable Global Link Parameters" align="center" border={true} src="https://files.readme.io/17a6663-2024-08-15_10-59-58_1.gif">
  Enable Global Link Parameters
</Image>

## Append Parameters to Email Links

Once you add the Global Link Parameters to the dashboard, you can select the parameter you want to append to the links in the email campaign. You can also add your custom link parameters when creating an email campaign. To do so: 

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Email* from the messaging channel list.

<Image alt="Email Campaign" align="center" border={true} src="https://files.readme.io/c039949-Auto_append_campaign.png">
  Email Campaign
</Image>

2. [Create an email campaign](https://docs.clevertap.com/docs/email-editor-templates).
3. Go to *Sender Details* under the *What* section after drafting an email campaign.
4. Select *Global link parameters* to append the parameters to the links included in the campaign. After you select this option, all the parameters set up in Step 1 are visible. 

<Image alt="Global Link Parameters" align="center" border={true} src="https://files.readme.io/b5fa54d-2024-08-15_21-57-13_1.gif">
  Global Link Parameters
</Image>

5. Select *Custom link parameters* if you want to add your custom parameters: 
   1. Click **+ Parameters** to add parameters to parameters.
   2. **Map key to a value**. You can add a static value or a personalized value. For example, you may want to personalize the URL to serve region-specific promotions and track performance by location, making the campaign more relevant to the user.

<Image align="center" className="border" border={true} src="https://files.readme.io/368c1e981d363709869c836732c7d58925260af27d4fc34b81ae28308d826c9f-Add_Custom_Link_Parameters.png" />

> 🚧 Limitations
>
> 1. Here is a list of reserved characters that cannot be used in parameters: `:`, `/`, `?`, `#`, `@`, `!`, `$`, `&`, `'`, `()`, `+`, `*`, `,`, `;`, `=`, and `[]`.
> 2. When using the Auto-Append feature for Link Parameters, users can add up to 20 Global link parameters and up to 10 Custom link parameters.

6. Publish the Email campaign. The links used in the Email are appended with the selected global and/or custom link parameters for efficient tracking. The indicative order of parameters appended to the URL is displayed in the Link Parameters field under the *Sender Details* tab on the left. The Parameters are appended in a top-to-bottom sequence, meaning the parameter at the top of the list is added to the URL first, followed by those listed below.

   <Image alt="Preview Order of Parameters Appended to URLs" align="center" border={true} src="https://files.readme.io/ebb6ed41de44b15af8ac55f7fe5d8e4fe3acb4a45fa7300b83b3f611a1e9c2ab-Preview_Links_Appended_to_URL.png">
     Preview Order of Parameters Appended to URLs
   </Image>

# Manage Global Link Parameters

You can edit, clone, or delete a particular Global Link Parameter. Once a campaign runs, any changes made to the Global Link Parameters—enabling, disabling, or deleting them—take effect in subsequent scheduled email campaigns. 

<Image alt="Global Link Parameters Navigations" align="center" border={true} src="https://files.readme.io/9ac7f2c-auto_append_6.png">
  Manage Global Link Parameters
</Image>
