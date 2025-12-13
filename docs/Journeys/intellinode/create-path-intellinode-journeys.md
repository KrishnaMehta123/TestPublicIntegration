---
title: Create an IntelliNODE Journey
excerpt: >-
  Understand how to create variations in journeys using IntelliNODE goals and
  paths.
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

An IntelliNODE journey can have multiple variations. This allows you to run multiple A/B tests to check the journey's success and test your assumptions. 

# Create an IntelliNODE Journey

To create an IntelliNODE journey:

1. Create a new Journey. 
2. Drag and drop **IntelliNODE** from the *Controllers* section to create an IntelliNODE journey.

<Image title="Drag and drop IntelliNODE controller to create a Journey" alt={1392} align="center" width="90% " border={true} src="https://files.readme.io/8fe2d01f8119c3de6ed6c51058bee384a426c046ef578b03bc81307b21b57bf3-2025-04-14_14-11-39_1.gif">
  Create an IntelliNODE Journey
</Image>

3. Click **IntelliNODE** in the canvas to set up the experiment.

<Image title="Setup user distribution for IntelliNODE Journeys" alt={1514} align="center" width="90% " border={true} src="https://files.readme.io/d3be1aa-InteliNODE_Set_Up.png">
  Setup IntelliNODE 
</Image>

4. Enter a name for the  IntelliNODE and select whether you want the experiments configured manually or automatically. We recommend entering a simple name you can remember, such as *abandoned cart experiment*. 
   * **Automated Mode**: This mode handles the distribution of qualifying users across all the connected paths. All paths start with equal distribution. However, the system automatically assigns a higher distribution to better-performing paths by re-evaluating the performance of each path every five minutes. The IntellNODE goal is used to determine the performance of each path. 
   * **Manual Mode**: This mode gives you control over the user distribution for each path. You can monitor the performance of your experiment and then change the distribution percentages of each path in the live journey. 

> 📘 Switching between Automated and Manual Modes
>
> You cannot switch modes in an IntelliNODE *after* publishing the journey.

5. Click **+Path** to add paths to a user journey.\
   You can add up to seven paths for the user journeys in the automated or manual mode.

## IntelliNODE Goals

An IntelliNODE goal is common for all the paths. The goal is used to calculate the conversion percentage. 

In automated mode, this conversion percentage determines the user distribution. To set up an IntelliNODE goal:

1. Enter the **IntelliNODE goal name**. The goal name must be easy to identify, for example, *cart abandon experiment*.
2. Define the preferred user action by using events and filters.
3. Click **+IntelliNODE Goal** to add more goals. You can add up to 3 goals.
4. Click *Save & Close* to save the goal. 

<Image title="Setup goals for IntelliNODE Journey" alt={1540} align="center" width="90% " border={true} src="https://files.readme.io/5266944-InteliNODE_Goals.png">
  Setup IntelliNODE Goals
</Image>

## Publish

Click **Publish** to make the journey live.

> 📘 Distribution changes in a manual mode
>
> For manual mode, only the latest ten edit logs are available.

Monitor the [IntelliNODE stats](https://docs.clevertap.com/docs/intellinode-stats) to check if your journey is progressing as planned.

# Automated vs. Manual IntelliNODE

The automated IntelliNODE does the heavy lifting for you. It verifies the conversion rate and adjusts the user distribution accordingly. The user distribution is eventually shifted in favor of the best-performing path. However, the other paths still receive some user distribution to account for seasonality. This way, you are insured against any change in user behavior. You can stop the experiment at any moment by declaring a path as the winner. The winning path is then utilized to engage *all* your users. 

<Image align="center" className="border" border={true} src="https://files.readme.io/9e0383b-AutoVSManual.png" />

The manual IntelliNODE gives you total control over user distribution. You can monitor the experiment's performance and change the user distribution for each path in a live journey.
