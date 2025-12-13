---
title: Edit a Journey
excerpt: >-
  Learn how to iterate, optimize, and evolve your journeys using the editing
  feature.
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

You can now edit live journeys in CleverTap, helping you refine your user flows in real-time, whether you want to fix a campaign message or an error, add new touchpoints, or optimize engagement. This document provides information on how to edit journeys. There are two types of edits available:

* **Partial Editing**\
  Used when you want to make non-structural changes directly to the current version of a *Running* journey. This includes modifying the following: *What* section, User distribution in an IntelliNODE journey, and Service Provider. For more information, refer to [Edit What Section](doc:edit-a-journey#option-1-edit-what-section). 
* **Full Editing**\
  Used when you want to make structural or behavioral changes that require creating a new version of the journey. This allows you to evolve the journey logic while preserving continuity for in-progress users and maintaining a record of changes across versions. Selecting this option allows you to change all the journey components, such as: 
  * Add, remove, or rearrange nodes
  * Change entry criteria, conversion goals, delays, paths, or conditions\
    For more information, refer to [Make Structural Changes](doc:edit-a-journey#option-2-make-structural-changes). 

# Edit Journey

To edit and publish an updated journey version, perform the following steps:

1. From the *Journeys* section, select the journey you want to edit.
2. Click the ![](https://files.readme.io/83228df00854230893cae44b546618d79d0c2bf8bab434103b15fa2e4900a8cc-Edit_icon_-_Journeys.png) icon in the top-right of the canvas to edit a Journey. If the journey is not in *Draft* state, the *Edit Journey* popup opens with the following options:

   <Image alt="Edit Journey Popup" align="center" border={true} src="https://files.readme.io/cf8a4772101e6c5bef7811b3a9f6ea2b331267c40caf21488c6e13d7509dd0ca-Edit_Journey_Popup.png">
     Edit Journey Popup
   </Image>

   * **Partial editing (same version)**: Select this option if you just want to edit the message content or engagement settings.
   * **Full editing (create new version)**: Select this option if you want to change nodes, paths, or entry criteria. When you select this option, a new version of the current journey version is created, where you can make all the changes.
3. Click **Save** to retain work in draft, or **Publish** to make the new version live. During publishing, choose how to handle the current version:
   * Stop it completely and exit users from the older journey version. OR
   * Move it to Restricted, allowing current users to finish the flow. 

For more information, refer to the section below.

# How Journey Editing Works?

Let us consider that you have launched a journey targeting users who added items to their cart but did not complete the purchase in the last 7 days. The goal here is to convert these users with timely nudges using push and email campaigns.

<Image alt="Current Journey" align="center" border={true} src="https://files.readme.io/67fa67ddb149a7e651a22463f0ef087bf833f5903826755ced814fd763279133-Current_Journey_-_Purchase_in_last_7_days.png">
  Current Journey
</Image>

The journey is running, and users are progressing through the flow, as shown in the image above. After publishing the journey, you want to make some edits. 

Based on the type of change, CleverTap offers the following options:

## Option 1: Edit *What* section

In this case, you can make minor updates, such as modifying the message content, modifying the user distribution in an IntelliNODE journey, or changing the provider settings. You can still do that without impacting the users' progress in the journey. Once the changes are published, they are applied to new messages sent from this journey.

## Option 2: Make Structural Changes

 In this case, you can make structural changes to the journey by creating a new version. You can also practically edit everything by creating a new draft version and making the changes to that version. For example, you want to add an IntelliNODE and split the journey into Push-led and Email-led variants. When you initiate the editing and publish the new versions, you have two options (refer to the following image): Restrict Previous Version and Stop Previous Version. 

<Image alt="Stop Old Journey to Publish New Version" align="center" width="65% " border={true} src="https://files.readme.io/8103c7adbb4a6c74336aa7899550d4a9c6a33542fb16535742b04139fe3e74cb-image.png">
  Options When Publishing New Version
</Image>

### Scenario 1: Restrict Previous Version

When you publish the new version, you can choose to mark the older version as **Restricted**.

* The existing users continue progressing in the original journey.
* New users who meet the updated entry criteria are routed into the new version of the journey.

<Image alt="Restricted State - Journey Workflow " align="center" border={true} src="https://files.readme.io/7254c0ade86a85c9e7e3b153991364cbc04e85ae1b2765a39a54809e6f98912d-Restricted_state_-_Static_New_Journey.png">
  Restricted State - Journey Workflow 
</Image>

This approach avoids disruption and allows a smooth switchover to the new version. This ensures a smooth switchover where live users are not force-exited, but all future activity happens in the updated version. Use this to preserve the experience for users already in progress, while activating new logic for upcoming users.

### Scenario 2: Stop Previous Version

If you want all users to move to the new logic immediately, you can stop the previous version while publishing the new one.

* All users in the previous version are forced to exit the journey.
* The new journey version transitions to the Scheduled state on Publish and automatically moves to the Running state after two hours.
* The users who exited the previous version would be eligible to qualify for the new version.

<Image alt="Stopped State - Journey Workflow" align="center" border={true} src="https://files.readme.io/98f98016b7614737330d4092365eda08609abbd6d986cf494a60b276a5b10cdd-Stopped_State_Edit_a_Journey.png">
  Stopped State - Journey Workflow
</Image>

This ensures that all future activity, including the users currently moving through the previous version, is governed by the new journey version. 

# Editing Options by State

<Table>
  <thead>
    <tr>
      <th>
        **Journey State**
      </th>

      <th>
        **Edit What Section**
      </th>

      <th>
        **Create New Version**
      </th>

      <th>
        **Notes**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Draft**
      </td>

      <td>
        Allowed
      </td>

      <td>
        Not Required
      </td>

      <td>
        Full editing allowed. All changes happen within the draft.
      </td>
    </tr>

    <tr>
      <td>
        **Scheduled**
      </td>

      <td>
        Allowed
      </td>

      <td>
        Not Allowed
      </td>

      <td>
        Limited edits are allowed to the *What* section of engagement nodes, such as message content, providers, and manual distribution percentages.
      </td>
    </tr>

    <tr>
      <td>
        **Running**
      </td>

      <td>
        Allowed
      </td>

      <td>
        Allowed
      </td>

      <td>
        The older version can be stopped or moved to the Restricted state when creating a new version. Existing users continue to progress along the older journey. You choose what happens to the older version.
      </td>
    </tr>

    <tr>
      <td>
        **Paused**
      </td>

      <td>
        Allowed
      </td>

      <td>
        Allowed
      </td>

      <td>
        The older version can be stopped or moved to the Restricted state when creating a new version. Existing users continue to progress along the older journey. You choose what happens to the older version.
      </td>
    </tr>

    <tr>
      <td>
        **Completed**
      </td>

      <td>
        Not Allowed
      </td>

      <td>
        Allowed
      </td>

      <td>
        Once you publish a new version, you can:<li>**Force exit from version**, if you want all users to immediately move to the new version.</li><li>**Keep moving in the version** if you want to allow existing users to continue moving through it. The new users who meet the updated entry criteria are routed into the new version of the journey.</li>
      </td>
    </tr>

    <tr>
      <td>
        **Stopped**
      </td>

      <td>
        Not Allowed
      </td>

      <td>
        Allowed
      </td>

      <td>
        You can make changes to a stopped journey by creating a new draft version. This allows you to modify all aspects of the journey, including nodes, paths, goals, and qualification criteria.
      </td>
    </tr>

    <tr>
      <td>
        **Restricted**
      </td>

      <td>
        Allowed
      </td>

      <td>
        Allowed
      </td>

      <td>
        Existing users continue to progress along the older journey. You choose what happens to the older version.
      </td>
    </tr>
  </tbody>
</Table>

# Version Management

Only one version of a journey can be in the **Running** state at any given time. Version 1 is automatically assigned when a journey is first created and published. Every time you create a new version by editing a journey not in the Draft state, the system increments the version number: Version 2, Version 3, ..., up to Version 10. When you publish a new version:

* It becomes the active Running version that qualifies new users.
* The previous version cannot remain running and must be transitioned to either:
  * Stopped: The previous version is fully deactivated, halting all user progress and entry.
  * Restricted: The previous version is active only for users already progressing inside the Journey, allowing them to complete it but preventing new entries.

> 📘 **Version Limit**
>
> You can maintain up to **10 versions** of a single journey entity. If you want to edit this journey entity after reaching this limit, you must clone the desired version of the journey.

You can view all the Journey versions by clicking **All Versions** from within the Journey canvas.

<Image align="center" className="border" border={true} src="https://files.readme.io/1c7b4727cbe265a07649fc0b10082bf87461a7cd10123865d512dcb66ee1516a-View_All_Journey_Versions.png" />

# Advantages of Editing Journey

Editing a journey introduces flexibility and experimentation into Journey management. Each version:

* Has its own flow configuration and conversion goals
* Maintains entry/exit logic independently
* Tracks node-level and engagement stats

This allows you to test variations, optimize performance, and evolve journeys based on insights, without overwriting historical data or affecting the ongoing user flows.

For example, a marketing team wants to change a Running journey that sends a single push notification after 3 days of inactivity. In the new version, they added a reminder email on day 2. By comparing the metrics across versions, they can determine which approach yields the higher reactivation rate.

# FAQs

Find answers to the following common questions about editing a Journey.

### What can I edit in a journey?

There are two ways to make edits:

* **Partial Edit**: Using this option, you can make non-structural changes directly to the current version of a *Running* journey. This includes modifying message content, user distribution in the IntelliNODE journey, and the service provider. 
* **Full Editing**: Using this option, you can make structural or behavioral changes requiring the creation of a new journey version. Selecting this option allows you to change all the journey components. This allows you to evolve the journey logic while preserving continuity for in-progress users and maintaining a record of changes across versions.

For more information about editing, refer to [Edit a Journey](doc:edit-a-journey). 

### What happens to the old version and users in it when I publish a new one?

The previous version either moves to the Restricted or Stopped state. If you choose to move the older journey version to the Restricted state:

* The users who had entered the journey continue progressing in the older journey version. No new users enter the restricted journey version, and user entry to this version is stopped.
* New users who meet the updated entry criteria are routed into the new journey version.

If you choose to move the older to the Stopped state:

* All users in the previous version are forced to exit the journey version.
* The new journey version transitions to the Scheduled state on Publish and automatically moves to the Running state after two hours.
* The users who exited the older version could qualify for the new version.

 Journey versioning ensures that older versions, including their design and performance data, remain accessible for reference. Only one version can be in the *Running* state at any given time. For more information, refer to [Journey States](doc:journey-states-edit-a-journey). 

### What happens to user entry and movement in the journey with the creation of a new version?

In a journey entity with multiple versions:

* Users entry is stopped in all the older versions in the Restricted or Paused state.
* Users are allowed to enter only the latest running version per the entry criteria.

For more information, refer to [Journey States](doc:journey-states-edit-a-journey).

### How can I view Stats for a particular version?

Each journey version has its own set of stats. Use the Version dropdown in the journey stats view to toggle between versions and analyze performance metrics independently. You can compare outcomes across versions.

<Image alt="Select Version to View Stats " align="center" border={true} src="https://files.readme.io/a2c0b26710978fb399659fac7678116e176ebb9ff05daa580232f022bb808d22-Select_Version_from_Dropdown.png">
  Select Version to View Stats 
</Image>

### Will creating a version consume journey limits, and how many versions can be created for a journey?

Version creation consumes the journey limits. Journeys in *Paused*, *Running*, and *Restricted* state consume the journey limit. You can create up to **10 versions** of a single journey entity. If you want to edit this journey entity after reaching this limit, you can clone the desired journey version. 

### What would be the impact on reporting?

Each journey version maintains its own set of reports and stats. You can choose to generate reports for: *All versions of the journey*, or *Selected versions only*. This flexibility ensures that you get precise, contextual insights, whether you analyze individual journey versions or compare performance across versions. For more information, refer to [View Journey Reports](doc:viewing-journey-reports-edit-a-journey). 

### What happens to user movement between versions?

The user would remain in one version in a journey entity. The user would move between versions only when the user exits the previous version and qualifies for the new version entry criteria. For more information, refer to [Edit a Journey](doc:edit-a-journey).

### What is the difference between Paused and Restricted journeys?

A journey in the Paused state is temporarily halted manually. It does not allow new user entries, but users who have already entered continue to progress through the journey as configured. You can resume the journey at any time to start accepting new users again.

A journey in the Restricted state permanently stops the user's entry while allowing only in-progress users to continue and complete their journey flow; the journey cannot be changed to the Running state.

For more information, refer to [Journey States](doc:journey-states-edit-a-journey). 

### Once we stop a journey version, how long does it take to move the new version to *Running* state?

When you stop the previous version while publishing the new one, all users in the previous version are forced to exit the journey. The new journey version transitions to the Scheduled state on Publish and automatically moves to the Running state after two hours. For more information, refer to [Make Structural Changes](doc:edit-a-journey#option-2-make-structural-changes).
