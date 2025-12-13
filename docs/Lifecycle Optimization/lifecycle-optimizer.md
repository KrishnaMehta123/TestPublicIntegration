---
title: Lifecycle Optimizer
excerpt: >-
  Understand how to optimize lifecycle using frameworks, stages, and
  engagements.
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

Mobile marketing platforms often focus on the campaign and journey-level engagement. CleverTap developed the Lifecycle Optimizer to create a view of the entire user base. As the name suggests, CleverTap Lifecycle Optimizer provides you with a guided and end-to-end solution for your retention flow. 

Lifecycle optimizer enables you to : 

* Define lifecycle stages to understand users. 
* Connect with users to influence movement into the next stage.\
  To move users forward, you can run engagement experiments, measure their impact, and apply the winning variation to all users in a stage to optimize the lifecycle.

The stages for Lifecycle Optimizer are:

1. Map users to lifecycle stages based on qualifying actions to understand the entire user base.
2. Experiment and iterate with different approaches and roll out the winning Journey.
3. Engage users with relevant, timely messages to move them to the next stage

You can choose from two frameworks to achieve your retention goals: AIC or AARRR.

# Lifecycle Optimizer Steps

<Image title="Get Started with Lifecycle Optimizer" alt="Screenshot of the Lifecycle Optimizer dashboard, displaying the steps to get started." align="center" width="100%" border={true} src="https://files.readme.io/c88a2f0-LCO_Retention_Main_Steps.png">
  Get Started with Lifecycle Optimizer
</Image>

The steps to optimize a Lifecycle:

1. [Setup Lifecycle](https://docs.clevertap.com/docs/lifecycle-optimizer#setup-lifecycle)
2. [Create Engagement](https://docs.clevertap.com/docs/lifecycle-optimizer#create-engagement)
3. Test, Iterate, and Rollout to All Users in a Stage

# Current Retention

Let us begin by viewing our current retention. This is a good starting point because it shows the current state of your retention. We can benchmark all our improvements against these statistics. 

Select Lifecycle Optimizer from the main dashboard. The key metrics overview displays the current retention state. 

<Image title="Key metrics overview for all users" alt="Screenshot of the dashboard, displaying key metrics for all users across the customer lifecycle." align="center" border={true} src="https://files.readme.io/a3bd720-LCO_Current_Retention.png">
  Key Metrics Overview
</Image>

You will see the following trends with some presets. You can modify these presets by clicking edit![edit](https://files.readme.io/d0f481d-icon_edit.png). 

| Trend Name              | Events mapped                | Description                                                                                    |
| :---------------------- | :--------------------------- | :--------------------------------------------------------------------------------------------- |
| Usage Rate              | App Launched to App Launched | This indicates the app usage rate. It shows the percentage of active returning users.          |
| Current Conversion Rate | App Launched to Charged      | This is your current conversion rate. It shows the percentage of active users who converted.   |
| Repeat Conversion Rate  | Charged to Charged           | This is your repeat conversion rate. It is the percentage of active users who converted again. |

# Setup Lifecycle

To set up a lifecycle model:

1. [Select a Framework](https://docs.clevertap.com/docs/lifecycle-optimizer#select-framework)
2. [Define Lifecycle Stages](https://docs.clevertap.com/docs/lifecycle-optimizer#define-lifecycle-stages)
3. [Choose Preferred values](https://docs.clevertap.com/docs/lifecycle-optimizer#choose-preferred-values)

## Select Framework

Select a framework and click Next. 

<Image title="Select a customer lifecycle framework." alt="Screenshot of the dashboard, displaying options to choose framework for the lifecycle." align="center" border={true} src="https://files.readme.io/6f1756a-LCO_Setup_Framework_Select.png">
  Customer Lifecycle Framework
</Image>

### AIC Framework

Brands that choose the AIC framework tend to focus on the type of user actions. The core action or conversion event represents the most desirable user action and is generally used by Social Networking or Ad-based apps.\
This is a 3-stage customer lifecycle framework. 

| Sequence | Stage       | Indicative User Events                            | User Insight                     |
| :------- | :---------- | :------------------------------------------------ | :------------------------------- |
| 1        | Acknowledge | App open                                          | Action, low intent               |
| 2        | Interest    | Search, add to cart, share app, and so on.        | Investment in the app experience |
| 3        | Convert     | Book ride, post message, create board, and so on. | Complete core action             |

> 📘 Note
>
> This table is indicative. You can edit this stage with data points within the framework to suit your business needs.

### AARRR Framework

The acronym AARRR stands for Acquisition, Activation, Retention, Referral, and Revenue.\
The AARRR framework is based on customer lifecycle stages. You choose this framework if you look at users and their progression through defined stages to view clear revenue conversion events, and is generally used by eCommerce and Travel apps.\
This is a 5-stage customer lifecycle framework. 

| Sequence | Stage       | Indicative User Events                   | User Insight                                     |
| :------- | :---------- | :--------------------------------------- | :----------------------------------------------- |
| 1        | Acquisition | App open                                 | Trackable acquisition event in CleverTap         |
| 2        | Activation  | Register, likes, board created           | Action that indicated likely continued app use   |
| 3        | Retention   | Pin, wishlist, add to cart, view product | Core app activity, inherent to the app’s purpose |
| 4        | Revenue     | Purchase, subscribe                      | Revenue metrics                                  |
| 5        | Referral    | Share content, invite to app, add rating | Indicates advocacy                               |

> 📘 Note
>
> This table is indicative. You can edit any stage within the framework to suit your business needs.

[Setup Lifecycle](https://docs.clevertap.com/docs/lifecycle-optimizer#setup-lifecycle)

## Define Lifecycle Stages

Here you choose events that qualify users for each stage of the lifecycle. You can choose multiple events. Events are considered from the latest step. 

### AIC Events

<Image title="Choose AIC Events" alt="Screenshot of the dashboard, displaying options to choose AIC events that qualify users into each stage of the lifecycle." align="center" border={true} src="https://files.readme.io/360d773-LCO_select_events_AIC.png">
  Define Lifecycle Stages
</Image>

### AARRR Events

<Image title="Choose AARRR events" alt="Screenshot of the dashboard, displaying options to choose AARRR events that qualify users into each stage of the lifecycle." align="center" border={true} src="https://files.readme.io/9b58a11-LCO_select_events_AARRR.png">
  Define Lifecycle Stages
</Image>

[Setup Lifecycle](https://docs.clevertap.com/docs/lifecycle-optimizer#setup-lifecycle)

## Choose Preferred Values

The preferred value is the time period on which your model is based. The default value is 12 weeks.  This period can be edited. However, changing this default value will also change the model accordingly. 

<Image title="Choose preferred values" alt="Screenshot of the dashboard, displaying the options to select qualifying time frame, usage interval, and control group." align="center" border={true} src="https://files.readme.io/fee15f4-LCO_choose_preferred_values.png">
  Preferred-Value for Lifecycle Optimizer
</Image>

Select "Qualify users for different stages of customer lifecycle based on these preferred values"  and save the setup. 

You can save the model as a draft or click Publish to publish the model. 

<Image title="Lifecycle optimizer dashboard" alt="Screenshot of dashboard, displaying Lifecycle Optimizer model." align="center" border={true} src="https://files.readme.io/780b17b-LCO_Dashboard_Main.png">
  Lifecycle Optimizer Dashboard
</Image>

[Setup Lifecycle](https://docs.clevertap.com/docs/lifecycle-optimizer#setup-lifecycle)\
[Lifecycle Optimizer Steps](https://docs.clevertap.com/docs/lifecycle-optimizer#lifecycle-optimizer-steps)

# Create Engagement

You can create engagement tailored to each stage. 

1. Select *Lifecycle Optimizer*.
2. Under Engagement Snapshot, click *View Engagements*.\
   The Engagements page appears.\
    You can create engagement for your model from this page. 

<Image title="Create engagement for each stage." alt="Screenshot of the dashboard, displaying Engagement Stats." align="center" border={true} src="https://files.readme.io/3003dba-LCO_Enagement_Create.png">
  Create Engagement for Each Stage of the Lifecycle
</Image>

## Define Engagement

Define your engagement and roll it out to the selected percentage of users.

<Image title="Define engagement for users." alt="Screenshot of the dashboard, displaying how to define engagement for users." align="center" border={true} src="https://files.readme.io/db869fe-LCO_Engagment_Define.gif">
  Define Engagement
</Image>

> 📘 Tip
>
> Roll out this engagement to all users if you are confident that your engagement does not need improvement. However, if you wish to experiment first, you can experiment with a selected percent of users and then view the results. Rollout the engagement to all users if the results are satisfactory. Else, repeat the experiment.

## Define Engagement Modes

Create a Journey to engage your users in the selected stage. For example, create a Journey to onboard all your new users. To learn more, refer to [Journeys](https://docs.clevertap.com/docs/journeys).

After you create your Journey, you can save it as a draft or publish it. 

<Image title="Create a journey" alt="Screenshot of the dashboard, displaying how to define engagement node using a journey." align="center" border={true} src="https://files.readme.io/57b756c-LCO_Journey.png">
  Create a Journey
</Image>

The journey operations available are:

* Edit - You can edit a current Journey. 
* Stop - You can stop a Journey. However, a stopped Journey cannot be restarted. 
* Rollout to all users - If you are experimenting with a Journey and the results are good, then you can roll out the Journey to all of your users.

To learn more, refer to [Journey Operations](doc:journey-operations) 

### Journey Considerations

* Entry node is populated with the % of users in the stage. 
* Goals are populated with the qualification to a higher lifecycle stage.\
   For instance, if you're creating engagement in the acknowledgment stage, then the interested or converted\
   users who move to the next stage.
* System Control Group cannot be changed 

# Engagement Stats

Click *View Stats* to view the engagement statistics.

* Distribution Across Lifecycle Stages\
   shows the current percentage of users across the Lifecycle Stages. 

<Image title="Engagement statistics" alt="Screenshot of the dashboard, displaying distribution of the users across the lifestyle stages." align="center" border={true} src="https://files.readme.io/c7dfdb7-lifecycle_distribution_stages.png">
  Engagement Statistics
</Image>

* Change Over Time\
   Shows the differential change in each stage.\
   For example, if the Interest stage shows the user count at 17.41% on June 1st and 18.04 % on June 2nd, then\
   the differential increase in user interest is : **(18.01 - 17.41)  / 17.41 = 3.33%.**

<Image title="User change over time" alt="Screenshot of the dashboard, displaying change in user count between yesterday and the selected date." align="center" border={true} src="https://files.readme.io/422bd93-LCO_Stats_Change_over_time.png">
  User Change Over Time
</Image>

* Inter Stage Transition\
  shows how the users transitioned to a particular stage from each of the Lifecycle stages. 

<Image title="Interstage transition of users" alt="Screenshot of the dashboard, displaying how users transition across different stages." align="center" border={true} src="https://files.readme.io/59aa509-LCO_Stats_Inter_stage_Transitions.png">
  Inter Stage Transition of Users
</Image>

> 📘 Note
>
> Hover over a stage in the chord diagram to see the user transitions.

* Into a stage trend\
  Shows the trend of users who transitioned from other stages into the selected stage. 

<Image title="Daily user transition trends" alt="Screenshot of the dashboard, displaying daily user transition trends from other stages into the selected stage." align="center" border={true} src="https://files.readme.io/f94b25d-LCO_Stats_into_a_stage.png">
  Daily User Transition Trends From Other Stages into the Selected Stage
</Image>

* From a stage\
   Shows the trend of users who transitioned to other stages from the selected stage. If the model is set up\
   optimally, the users must transition from a lower stage to a higher stage. 

<Image title="Daily user transition trends" alt="Screenshot of the dashboard, displaying daily user transition trends from selected stage into other stages." align="center" border={true} src="https://files.readme.io/e10b9d6-LCO_Stats_from_a_stage.png">
  Daily User Transition Trends From Selected Stage into the Other Stages
</Image>

[Lifecycle Optimizer Steps](https://docs.clevertap.com/docs/lifecycle-optimizer#lifecycle-optimizer-steps)

# Video Tutorial

For further information, you can watch the following video on lifecycle optimizer:

<Embed url="https://www.youtube.com/watch?v=1YZuGQkxUtM&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=7" title="Product Demo: Lifecycle Optimizer" favicon="https://www.youtube.com/s/desktop/404f9720/img/favicon.ico" image="http://i.ytimg.com/vi/1YZuGQkxUtM/hqdefault.jpg" provider="youtube.com" href="https://www.youtube.com/watch?v=1YZuGQkxUtM&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=7" html="%3Ciframe%20class%3D%22embedly-embed%22%20src%3D%22%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Fsrc%3Dhttps%253A%252F%252Fwww.youtube.com%252Fembed%252F1YZuGQkxUtM%26display_name%3DYouTube%26url%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253D1YZuGQkxUtM%26image%3Dhttp%253A%252F%252Fi.ytimg.com%252Fvi%252F1YZuGQkxUtM%252Fhqdefault.jpg%26key%3Df2aa6fc3595946d0afc3d76cbbd25dc3%26type%3Dtext%252Fhtml%26schema%3Dyoutube%22%20width%3D%22854%22%20height%3D%22480%22%20scrolling%3D%22no%22%20title%3D%22YouTube%20embed%22%20frameborder%3D%220%22%20allow%3D%22autoplay%3B%20fullscreen%22%20allowfullscreen%3D%22true%22%3E%3C%2Fiframe%3E" />

By leveraging the Lifecycle Optimizer, you can segment users and create personalized campaigns. Learn more about maximizing engagement at each stage of the customer journey to improve [Customer Lifetime Value](https://clevertap.com/blog/customer-lifetime-value/) (CLV). You can also calculate the customer lifetime value using the CLV formula to boost retention.
