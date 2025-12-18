---
title: Manage Email Preferences
excerpt: >-
  Allow users to customize the communication preference and host a subscription
  management page using CleverTap's Email Preference Center feature.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

CleverTap's Email Preference Center feature allows you to customize user communication preferences. We provide a ready-to-use preference management page, empowering users to control their communication experience. This ensures they stay engaged with the content that matters most to them. Subscription groups allow users to select the content they want to receive, reducing unsubscription rates and fostering strong brand-user relationships. This approach enhances user satisfaction and builds a more personalized connection with your audience.

# Configure Email Preference Center

When setting up the email provider, you can choose between using CleverTap's _Email Preference Center_ page or your custom subscription management page URL. To ensure a consistent and user-friendly experience, CleverTap's Unsubscribe page or Email Preference Center is displayed in the same language as the user's browser language. However, the subscription group names and descriptions appear exactly as defined under _Settings_ > _Setup_ > _[Subscription Groups](doc:group-unsubscribe)_. Currently, CleverTap supports the following languages: French, English, Spanish and Hindi.

<Callout icon="📘" theme="info">
  #### Note

  Ensure that the language of the subscription group names and descriptions is consistent with the browser language of your user base for seamless user experience.
</Callout>

To configure the Email Preference Center:

1. From the dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _Email_.
2. Click **+ Provider** to add a provider and [enter all the provider details](doc:setup-email#setup-provider).
3. Select _System_ from the _Email Preference Center_ dropdown to use a pre-built preference center with a sample preview. If you select the <img src="https://files.readme.io/6f15938-image.png" height="30px" width="30px" /> icon, a preview popup window opens. This displays the sample of how the _Email Preference Center_ appears to the user. The [subscription groups](doc:group-unsubscribe#subscription-groups) within the Email Preference Center changes based on your preferences in case of an actual campaign.

<Image align="center" alt="Set up Email Preference" border={true} caption="Set Up Email Preferences" src="https://files.readme.io/6952660-image.png" />

4. Click **Save** to save your provider configuration.

<Image align="center" alt="Provider Configuration Added" border={true} caption="Provider Configuration Added" src="https://files.readme.io/ce4ff5a-image.png" />

<Callout icon="📘" theme="info">
  #### Advanced Setup

  You can also preview the _Email Preference Center_  by navigating to _Channels_> _Email_. Select the _Advanced Setup_ tab.

  <Image align="center" alt="Email Preference Center" border={true} caption="Email Preference Center" src="https://files.readme.io/f4ae755-image.png" />
</Callout>

# Manage User Preferences for Email Campaigns

Navigate to the email Provider _Setup_ page and select _System_ from the _Email Preference Center_ dropdown. After completing the provider Setup, you can add either _Group Unsubscribe_ or _Email Preference Center_ links to manage unsubscriptions from within the campaign. However, the users continue to receive emails sent if you select the _[Send email to users who have opted out](doc:create-message-override-opt-out#override-communication-preferences-for-email)_ option when creating an email campaign.

<details>
  <summary> Group Unsubscribe </summary>

  This enables users to opt out of the subscription groups associated with the specific campaign. The functionality may differ based on whether subscription groups are set up in your CleverTap project.

  ### Manage Group Unsubscribe for Associated Subscription Groups

  When the user clicks on the unsubscribe link, they are unsubscribed from the subscription groups associated with the campaigns. If the users want to modify their preferences for subscription groups, they can do so by clicking the  [Manage Email Preference ](doc:manage-email-preferences#manage-preferences-from-the-email-center) link.

  <Image align="center" border={true} src="https://files.readme.io/75ee439-Manage_Group_Unsubscribe_for_Configured_Subscription_Groups.png" alt="Manage Group Unsubscribe" />

  After preferences are successfully saved, a success message appears:

  <Image align="center" border={true} src="https://files.readme.io/35a8186-image.png" alt="Email Preferences Saved" />

  ### Manage Group Unsubscribe Without Subscription Groups

  Two distinct scenarios occur when the campaign is not associated with any subscription group or when no subscription groups are created on the dashboard. The following sections provide information about managing unsubscribes for such cases.

  #### Subscription Groups Not Associated with Campaigns

  If you have not selected any subscription groups from the *When* section during campaign creation but have configured them under *Settings* > *Setup* > *Subscription Groups*, users can manage their email preferences using the  *[Manage Preferences](doc:manage-email-preferences#manage-preferences-from-the-email-center)*  option. In this case, if you add the *Group Unsubscribe* link, the user is unsubscribed from all the emails when they click this link.

  > 📘 Recommendation
  >
  > As part of email best pratices, CleverTap strongly recommends incorporating subscription groups for campaigns to guarantee that your content resonates with the intended audience. This ensures that they receive the information that matters most to them.

  #### No Subscription Groups Configured on Dashboard

  If your account has no subscription group created, users are directly unsubscribed from all communication when they click the *Group Unsubscribe* link from the email campaign. The users are directly unsubscribed from all your future email communications. Users also have the option to subscribe back to their communications using the *Resubscribe* link.

  <Image align="center" border={true} src="https://files.readme.io/091b00f-image.png" alt="Unsubscribe from Email" />

  > 📘 Note
  >
  > When using the send test option during email campaign creation, clicking the *Group Unsubscribe* link allows you to view the *Group Unsubscribe* page with all the subscription groups present on your dashboard. However, your preferences are not saved.
</details>

<details>
  <summary>Email Preference Center</summary>

  This option allows users to manage all their subscription group preferences and unsubscribe from all groups at once. The functionality may differ based on whether subscription groups are set up in your CleverTap project.

  ### Manage Email Preferences for Configured Subscription Groups

  When the user clicks the unsubscribe link, they are directed to the *Manage Email Preferences* page, showcasing their current email preferences for all subscription groups. Here, users can select or deselect the emails they want to receive.

  <Image align="center" border={true} src="https://files.readme.io/cc38488-image.png" alt="Manage Email Preference" />

  Users can opt out of all groups by setting the *All communication* toggle to *No*. When *All communication* toggle is set to *No*, all the other respective toggles are automatically set to *No*. After successfully saving their preferences, users are redirected to a success message page. This page includes an option to navigate back to the *Manage Email Preferences* page for further modifications.

  <Image align="center" border={true} src="https://files.readme.io/35a8186-image.png" alt="Email Preferences Saved" />

  ### Manage Email Preferences Without Subscription Groups

  Two distinct scenarios occur when the campaign is not associated with any subscription group or when no subscription groups are created on the dashboard. The following sections provide information about managing email preferences for such cases.

  #### Subscription Groups Not Associated with Campaigns

  If the campaign is not associated with any subscription group but you have configured subscription groups on the dashboard. In that case, the users can still manage their email preferences using the  *[Manage Preferences](manage-email-preference#manage-preferences-from-the-email-center)*  option.

  > 📘 Recommendation
  >
  > As part of email best pratices, CleverTap strongly recommends incorporating subscription groups for campaigns to guarantee that your content resonates with the intended audience. This ensures that they receive the information that matters most to them.

  #### No Subscription Groups Configured on Dashboard

  If your account has no subscription group created, you must not include the link to manage email preferences in your campaign. As there are no subscription groups available for users to modify their preferences, only the unsubscribe link must be added. This allows users to unsubscribe from future communications.

  > 📘 Note
  >
  > When using the  *Send test* option during email campaign creation, clicking the *Email Preference Center* link allows you to view the *Manage Email Preferences* page. However, your preferences are not saved.
</details>

# Add Email Preference/Group Unsubscribe Link Within Campaign

You can add **Email Preference**/**Group Unsubscribe** links within the campaigns. Whenever the user clicks on the link to modify and save preferences, the _Channel Unsubscribed_ event and its event properties are raised.

To set up your email campaign, refer to [Create Email Message](doc:create-message-email).

* **For Email with Rich Media Template**

  When using the _Email with rich media_ template, you must add `*|CT_MANAGE_PREFERENCES|*` (for Email Preference Center) and `*|CT_GROUP_UNSUBSCRIBE|*`(for Group Unsubscribe).

  <Image align="center" alt="Adding Links Using Email with Rich Media Template" border={true} caption="Adding Links Using Email with Rich Media Template" src="https://files.readme.io/9a77a69-image.png" />

**Example**: As shown in the image above, the HTML code `<a href="*|CT_MANAGE_PREFERENCES|*">Manage My Preferences</a>` is for creating hyperlinks in an email campaign to manage preferences. `*|CT_MANAGE_PREFERENCES|*` is the mandatory tag for redirecting users to _Email Preference Center_ to manage their preferences.

* **For Email with Drag and Drop Template**

  1. Select the text in the campaign to which you want to add links and click **More** after drafting your campaign message.
  2. Select the _Special links_> _Unsubscribe_ option, and select either [Email Preference Center](doc:manage-email-preferences#manage-user-preferences-for-email-campaigns) or [Group Unsubscribe](doc:manage-email-preferences#manage-user-preferences-for-email-campaigns).

  <Image align="center" alt="Add Special Links using Email Drag and Drop Template" border={true} caption="Add Special Links using Email Drag and Drop Template" src="https://files.readme.io/39ed807-Add_Special_Links_Using_Email_Drag_and_Drop_Template.gif" />

**Example**: As shown in the image above, _unsubscribe_ is the text that is displayed as a clickable link. When the user clicks the text, it takes the user to the _Group Unsubscribe_ page.

# Errors

If users encounter any errors while managing Email Preferences/Unsubscribe in CleverTap, refer to the following guidelines to address and resolve common issues swiftly:

### Failed to save your preferences _OR_ We could not retrieve your email address

If users encounter these error messages, they must ensure the following:

* Ensure the internet connection is stable.
* Disable any ad blockers, as they might interfere with the retrieval process.
* Ensure that JavaScript is enabled in the browser settings.

If the issue persists, contact our Customer Success Team for further assistance.

### 404 error while trying to access Email Preference Center _OR_ when clicking on the unsubscribe link

After some time, you can try clicking the unsubscribe link. If the issue persists, contact our Customer Support Team for further assistance.

<HTMLBlock>{`
<style>
 /* nav#hub-sidebar { display: none; }*/
  .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  .markdown-body img{
  	margin-left: 0;
  }
 /* .rm-Guides a.suggestEdits {
    display: none;
  }*/
  @media (min-width: 769px) {
    .rm-Guides .rm-Article {
        max-width: 100%;
    }
  }
  .markdown-body summary {
  font-size: 20px;
  font-weight: bold; 
  text-transform: camelcase;
}
  .toc-children img {
    display: none;
  } 
  #content {
    padding-left: 80px 
  }
  .heading-3  {
    margin-top: 50px !important;
  }
  .heading-2  {
    margin-top: 35px !important;
  }
  .heading-3 .heading-text {
    color: #384248;
  }
  details {
    margin-top: 35px !important;
  }
  .field-description h3, .markdown-body h3{
    font-size: 1.35em;
  }
  .markdown-body summary {
    font-size: 20px;
  }

  .heading-2 + .heading-3  {
    margin-top: 20px !important;
  }
  details .heading-4  {
    margin-top: 30px !important;
  }
  details .heading-3  {
    margin-top: 50px !important;
  }
  details h3{
    font-size: 1.5em !important;
  }
  details  h4{
    font-size: 1.35em !important;
  }
  .rm-Guides #content-head h1 {
    font-size: 40px;
  }
</style>
`}</HTMLBlock>
