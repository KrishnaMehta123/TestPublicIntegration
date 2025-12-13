---
title: Product Experiences (Legacy)
excerpt: This document explains our Legacy Product Experience features.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
> 📘 Feature Availability
>
> A new and enhanced version of [Product Experiences ](https://docs.clevertap.com/docs/product-experiences-nextgen)is now available. New customers (CleverTap for Enterprise or CleverTap for Startups) who have not enabled the legacy functionalities can use this feature. The [methods](https://developer.clevertap.com/docs/may-2023#may-05) for the legacy Product Experiences feature have been deprecated and will be removed from the code. The existing users can continue to use the legacy Product Experiences till September 2024.

## Overview

With *Product Experiences*, you can change the behavior and appearance of your app remotely without an update. This helps you to deliver in-app personalization experience to your app users and test their response. You can use *product config* to modify app behavior and feature flags to add or remove features from your app without performing an app store deployment.

You can remotely configure your app with product config. The configuration can be anything, including the look and feel of the app and the workflow for users.

For example, you want to enable dark mode on your app; however, you want the following additional options:

* You want to test it first on iPhone users who live in New York. 
* You must also be capable of disabling the feature if it needs more work. 

You can create a product config for this improvement and test the response to your app.  Before using product config, you must complete the necessary setup. 

# Set up

To run a product config or a feature flag, you must create keys and segments for your app. 

## Create Keys

These are the keys that you have defined in your app code. You can map these keys from the CleverTap dashboard and control the configuration of your app. 

To create keys:

1. Navigate to *Product Experiences* >  *Setup* > *Keys*
2. Click **+Key** to create a new key. 

> 📘 Note
>
> The name of the key defined here must match the name of the key defined in the app. This name cannot be changed later. You can add up to 500 keys.

3. Add the *Key* definition. 

You can now activate or deactivate the dark mode based on the keys. The default value that the app is expecting for this key is `3`.  These values are set in your app. Assume the key value 3 means activate the feature, and 4 means to deactivate the feature. 


<Image title="Add key details and define the default value" alt={2880} align="center" border={true} src="https://files.readme.io/eafa5c2-product_exp_keys.png" />











4. Click **Save**. The `dark_mode` key is now listed on the *Manage Keys* page. 

### Edit/Archive Keys

To edit/archive keys:

1. Navigate to *Product Experiences* >  *Setup* > *Keys*. The *Keys* page displays. 
2. Click the ellipsis menu to edit or archive a key. Only the default value and description can be edited after saving a key.

You can view all the archived keys by selecting the *Archived Keys* box at the bottom of the key's list.  If a key is used in a product config or feature flag then it cannot be archived. 

## Create Segments

The segments are the target users who will receive app changes. 

To define the segments:

1. Navigate to *Product Experiences* >  *Setup* > *Segments*
2. Click **+Segment** to create a new segment.
3. Name the segment.
4. Create a segment by users who performed and/or did not perform an event.  You can also create segments for user properties such a demographics, geography, and so on. For our example, create a segment of iPhone users living in New York. 
5. Save the segment. 

<Image title="Define segments who will receive app changes" alt={1182} align="center" width="100%" border={true} src="https://files.readme.io/483d933-ProductExp_Segment_Create.png" />











## Edit/Clone a Segment

To edit/clone a segment:

1. Navigate to *Product Experiences* >  *Setup* > *Segments*. The *Segments* page displays. 
2. Click the ellipsis menu to edit or clone a segment. For example, you may want to edit the city and create another user segment for Miami. 

# Product Config

## Create Product Config

You can have multiple members of your team create product config with multiple keys and segments. You can then group these keys. 

To create a product config:
1. Navigate to *Product Experiences* > *Product Config*.  The *Product Config* page displays. 
2. Click the **+Product Config** button to create a new product config. The create a *Product Config* page displays. 
3. Enter the name and description for your product config. For our example, name the product config as *dark mode*. 
4. Select the *Segments* and *Keys* for your product config group. The *keys* are the keys that you have assigned in your app for each element or feature and the *segments* are the group of users who will receive this feature. 

For example, select the "iPhone users in New York"  and "iPhone users in Miami" as *Segments* and "Dark*Key" as the\_Product Config Key*. For more information on creating keys, refer to [Keys](https://docs.clevertap.com/docs/product-experiences#section-create-keys).

> 📘 Note
>
> A key can only be used in one product config.

5. Add the value and set the priority for your product config keys. Drag the <img src="https://files.readme.io/b3f4cdd-Move_icon.png" height="30px" width="30px" /> icon up or down to change segment priority. 
6. Publish your product config or schedule it to be published at a later date. 

<Image title="Create product config" alt={777} align="center" width="100%" border={true} src="https://files.readme.io/fc9b178-ProductExp_Product_Config_Create.png" />











## Edit/Archive Product Config

To edit a product config:

1. Navigate to *Product Experiences* > *Product Config*.  The *Product Config* page displays. 
2. Click the ellipsis menu to edit or archive a product config.  

> 📘 Note
>
> Any changes to a product config are saved in a new version. You can always revert to an earlier version.

## View Statistics

The stats will show you the distribution and value of the key stats for your product config. To view stats for a product config:

To view product config stats:

1. Navigate to *Product Experiences* > *Product Config*.  The *Product Config* page displays. 
2. Click the product config from the list and scroll down to view the stats. 

You can view the following information:

1. You can see a trend of the total number of keys delivered for all segments or a particular segment from the first chart.
2. In the second box, you can further break it down to get the count of each type of key value-wise.

<Image title="View product config stats" alt={720} align="center" width="100%" border={true} src="https://files.readme.io/f5d39be-Product_Exp_Keys_Stats.png" />











## Product Config Version

A new version is created every time you edit a product config. If the current config is not working for some reason, you can always revert to an older version of the product config.

To revert to an older version:

1. Navigate to *Product Experiences* > *Product Config*.  The *Product Config* page displays. 
2. Click the ellipsis menu to edit a product config.  The versions appear on the right side.
3. Click the required version number and publish. The selected version becomes active and the current version becomes inactive. 

<Image title="Creating product config versions" alt={1157} align="center" width="100%" border={true} src="https://files.readme.io/1b1bd88-ProductExp_product_config_versioning.png" />











# Feature Flags

You can have canary releases using feature flags. You can remotely turn on or turn off features on your app. 

For example, you want to want to enable an automatic playlist of recommended videos on your app. This is a really great feature but it freezes the app screen for some versions of iOS. You want the following options:

* You must be able to target iPhone users.  
* You want to test it on 20% of New York users and 30 % of Miami users before you roll it out to all users. 
* You must also be capable of disabling the feature if it needs more work. 

Feature flags can enable or disable a feature with a simple toggle. You can also test the feature on your users before you make it available to everyone. Your users will now have access to the feature and add to a better experience. 

## Create Feature Flags

To create feature flags:

1. Navigate to *Product Experiences* > *Feature Flags*.  The *Feature Flags* page displays. 
2. Click the **+Feature Flag** button to create a new feature flag. The create a *Feature Flag* page displays. 
3. Enter the name and description for your feature flag. For example, create an *Auto Playlist Feature Flag*.
4. Select the *Segments* and *Keys* for your feature flag. The *keys* are the keys that you have assigned in your app for each feature and the segments are the group of users who will receive this feature. 

For example, select the "iPhone users in New York" and "iPhone users in Miami" segment.  Select the key called *Auto Playlist* key.  For more information on creating keys, refer to [Keys](https://docs.clevertap.com/docs/product-config#section-create-keys).
> 📘 Note
>
> A feature flag can have only boolean values, that is, true or false. A key can only be used in one feature flag.

5. Under *Key value and priority*, add the key value for each segment. 
6. Toggle the selected segment and define the percentage of users who will receive this change. 

<Image title="Create feature flags" alt={779} align="center" width="100%" border={true} src="https://files.readme.io/683d874-ProductExp_Feature_Flag_Create.png" />

6. Publish your feature flag or schedule it to be published at a later date. 

<Image title="Schedule or publish a feature flag" alt={698} align="center" border={true} src="https://files.readme.io/88c5406-ProductExp_feature_flag_schedule.png" />

## Edit/Archive Feature Flags

> 📘 Note
>
> Any changes to a feature flag are saved in a new version. You can always revert to an earlier version.

## View Statistics

The stats will show you the distribution and value of the key stats for your feature flag. To view stats for a feature flag:

To view feature flag stats:

1. Navigate to *Product Experiences* > *Feature Flags*.  The *Feature Flag* page displays. 
2. Click the feature flag from the list and scroll down to view the stats. 

You can view the following information:

1. You can see a trend of the total number of keys delivered for all segments or a particular segment from the first chart.
2. In the second box, you can further break it down to get a count of each type of key value-wise

<Image title="View feature flag stats" alt={723} align="center" border={true} src="https://files.readme.io/be9202d-ProductExp_Feature_Flags_Stats.png" />

## Feature Flag Version

A new version is created every time you edit a feature flag. If the current feature is not working for some reason, you can always revert to an older version of the feature flag:

1. Navigate to *Product Experiences* > *Feature Flag*.  The *Feature Flag* page displays. 
2. Click the ellipsis menu to edit a feature flag.  The versions appear on the right side.
3. Click the required version number and publish it. The selected version becomes active and the current version becomes inactive. 

<Image title="Create feature flag versions" alt={1181} align="center" width="100%" border={true} src="https://files.readme.io/83b192d-ProductExp_feature_flag_versioning.png" />

# Role-Based Access Control for Product Experiences

Role-based access control (RBAC) is supported for *Product Experiences*. If you have advanced RBAC enabled for your account, admins can customize permissions and access roles. There are three standard system roles: *Admin*, *Creator*, and *Member*. 

If you do not have advanced RBAC, the *Admin* role will have read and write access for all setups (keys, segments, goals, and settings), product config, feature flags, and A/B tests. *Creator* will have read and write access to experiences and experiments. The creator will have only read access to setup (keys, segments, and goals), and the *Member* role will have only read access for product config, feature flag, and A/B tests. Members will also have read access to set up. 

For more information, refer to [Role-Based Access Control](doc:role-based-access-control-2).

# Video Tutorial

For further information, you can watch the following video on product configs and feature flags:

<Embed url="https://www.youtube.com/watch?v=tfHhsvWvPxk" favicon="https://www.google.com/favicon.ico" image="http://i.ytimg.com/vi/tfHhsvWvPxk/hqdefault.jpg" provider="youtube.com" href="https://www.youtube.com/watch?v=tfHhsvWvPxk" typeOfEmbed="default" title="undefined" html="%3Ciframe%20class%3D%22embedly-embed%22%20src%3D%22%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Fsrc%3Dhttps%253A%252F%252Fwww.youtube.com%252Fembed%252FtfHhsvWvPxk%26display_name%3DYouTube%26url%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253DtfHhsvWvPxk%26image%3Dhttp%253A%252F%252Fi.ytimg.com%252Fvi%252FtfHhsvWvPxk%252Fhqdefault.jpg%26key%3D7788cb384c9f4d5dbbdbeffd9fe4b92f%26type%3Dtext%252Fhtml%26schema%3Dyoutube%22%20width%3D%22854%22%20height%3D%22480%22%20scrolling%3D%22no%22%20title%3D%22YouTube%20embed%22%20frameborder%3D%220%22%20allow%3D%22autoplay%3B%20fullscreen%3B%20encrypted-media%3B%20picture-in-picture%3B%22%20allowfullscreen%3D%22true%22%3E%3C%2Fiframe%3E" />