---
title: Journey States
excerpt: Learn about different Journey States in CleverTap.
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

Journey States in CleverTap refer to the distinct phases a user experiences within an automated Journey. Each state is defined by unique characteristics determining how and when users enter, progress through, or exit the Journey. These states offer valuable insights into user behavior, enabling marketers to monitor engagement and optimize workflow efficiency.

The following table gives a quick overview of key aspects for each journey state:

* User Entry
* User Movement
* Possible Next Actions
* Possible Next States
* Editing Permissions

<Table>
  <thead>
    <tr>
      <th>
        State Name
      </th>

      <th>
        User Entry
      </th>

      <th>
        User Movement
      </th>

      <th>
        Possible Next Actions
      </th>

      <th>
        Possible Next States
      </th>

      <th>
        Editing Options
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Draft**
      </td>

      <td>
        Not Applicable
      </td>

      <td>
        Not Applicable
      </td>

      <td>
        Edit, Save, Publish, Clone
      </td>

      <td>
        Scheduled, Running
      </td>

      <td>
        Full editing allowed
      </td>
    </tr>

    <tr>
      <td>
        **Scheduled**
      </td>

      <td>
        Not Applicable
      </td>

      <td>
        Not Applicable
      </td>

      <td>
        Edit, Clone, Pause, Stop
      </td>

      <td>
        Running, Paused, Stopped
      </td>

      <td>
        Partial edit (What section).
      </td>
    </tr>

    <tr>
      <td>
        **Running**
      </td>

      <td>
        Users enter the journey as per the entry criteria
      </td>

      <td>
        Users progress as per the defined flow
      </td>

      <td>
        Edit, Clone, Pause, Stop
      </td>

      <td>
        Paused, Stopped, Restricted, Completed
      </td>

      <td>
        <li>Partial edit (What section).</li><li>Full edit creates a new version.</li>
      </td>
    </tr>

    <tr>
      <td>
        **Paused**
      </td>

      <td>
        No new user entry
      </td>

      <td>
        Existing users continue to move through the flow
      </td>

      <td>
        Edit, Clone, Resume, Stop
      </td>

      <td>
        Running, Stopped, Restricted, Completed
      </td>

      <td>
        <li>Partial edit (What section).</li><li>Full edit creates a new version.</li>
      </td>
    </tr>

    <tr>
      <td>
        **Completed**
      </td>

      <td>
        No new user entry
      </td>

      <td>
        Existing users progress until they exit
      </td>

      <td>
        Edit, Clone, Stop
      </td>

      <td>
        Stopped
      </td>

      <td>
        Full edit creates a new version.
      </td>
    </tr>

    <tr>
      <td>
        **Stopped**
      </td>

      <td>
        No new user entry
      </td>

      <td>
        No further progression; users are exited over 30–60 days
      </td>

      <td>
        Edit, Clone
      </td>

      <td>
        None
      </td>

      <td>
        Full edit creates a new version.
      </td>
    </tr>

    <tr>
      <td>
        **Restricted**
      </td>

      <td>
        No new entry
      </td>

      <td>
        Existing users continue the movement
      </td>

      <td>
        Edit, Stop
      </td>

      <td>
        Stopped
      </td>

      <td>
        <li>Partial edit (What section).</li><li>Full edit creates a new version.</li>
      </td>
    </tr>
  </tbody>
</Table>

# Draft

The Draft State in CleverTap refers to a Journey created but not published. Any unsaved changes in this state may be lost unless explicitly saved. If you have an existing unsaved Journey in the cache and choose to create a new Journey, CleverTap provides the option to either start a fresh Journey or restore the cached Journey for further editing.

If you restore the cached Journey, the most recent version saved in your browser cache loads, enabling you to continue editing from where you stopped. The cache is specific to each user and depends on the web browser, ensuring that only the user who created the Journey can access it while preventing accidental data loss.

The *Created By* and *Published By* columns on the Journeys List page identify the users responsible for creating and publishing a journey or its versions. The *Created By* column shows the user who initially created the journey or its latest draft version, while the *Published By* column indicates the user who published that specific version. When a draft is published, the journey transitions to the Scheduled or Running state based on its setup. Each version maintains its own creation and publishing metadata to enable accurate version tracking.

> 📘 Draft Management
>
> Only one draft is allowed per Journey entity at any time. Creating a new draft version replaces the existing one.

# Scheduled

The Scheduled state indicates that the journey is set to go live at a later time. In this state, users do not yet qualify for the journey, which becomes active when the scheduled time arrives.

The following table describes the key difference between the Past Behavior and Live Behavior Journeys in the Scheduled state:

| **Feature**                | **Past Behavior Setup**                                                                                         | **Live Behavior Setup**                                                                                      |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Qualification Criteria** | Based on **past actions** or **custom lists**.                                                                  | Based on **real-time user actions** or **inactivity**.                                                       |
| **Entry Timing**           | **At a fixed time**.                                                                                            | **At a fixed time**.                                                                                         |
| **Trigger Type**           | Static triggers based on predefined events.                                                                     | Dynamic triggers that act as soon as the criteria are met.                                                   |
| **Use Case Focus**         | Re-engagement or follow-ups based on past activities (for example, targeting users who checked out last month). | Real-time engagement or retention campaigns (for example, sending a cart abandonment reminder in real time). |

If the journey is stopped while in the Scheduled state, it will not go live, and no users will qualify for the journey.

## Editing Journey in Scheduled State

To edit a scheduled journey, click the ![](https://files.readme.io/8f45b08c7f55c17da382ee310aa5def046dab2b3d740a837ce8e39e61ea57240-Edit_icon.png) icon. In this state, you can only do limited edits to the *What* section of engagement nodes, such as message content, providers, and manual distribution percentages.

# Running

The Running state indicates that the journey is active, and the users execute actions as defined. In this state, users enter the Journey as they qualify and move ahead in the Journey as per the flow after qualifying (refer to the following GIF).

<Image alt="User Entry and Movement in Running State" align="center" border={true} src="https://files.readme.io/5aa5ea778cb2e4c2a73b283535a56b64413f776a1ca3379792ba2b4766364f3b-Running.gif">
  User Entry and Movement in Running State
</Image>

As users move through the Journey nodes (for example, receiving a message, meeting a condition, or dropping off), the stats are updated immediately in the dashboard. The date range selection in the calendar widget directly influences the Node stats. Consider an example where the Journey running from January 1 to January 10 sends push notifications to users. On January 5, you use the calendar widget to filter data for January 1–January 4. The Node stats update to reflect only the number of users who entered, dropped off, or converted during that time frame. Always ensure you are analyzing the correct time frame. For nodes with scheduled actions (for example, if a campaign is scheduled to run after two days), stats are updated only when those actions are triggered.

## Editing Journey in Running State

You can edit the *What* section of engagement nodes, such as message content, provider configuration, or manual distribution settings, without creating a new version. You must create a new version to modify other journey aspects (for example, entry criteria, goal logic, and journey structure).

Once you publish a new version, you can:

* **Stop the older version**, if you want all users to move to the new version immediately
* **Mark the old version Restricted** if you want to allow existing users to continue moving through it. The new users who meet the updated entry criteria are routed into the new version of the journey.

# Paused

The Paused state indicates that the already qualified users or the users who have entered the journey continue to advance in the journey. However, no new users qualify for the journey until it resumes (refer to the following GIF). For example, consider a Journey targeting users who abandon their cart without completing a purchase within 30 minutes. If you pause the Journey, users already qualified continue to progress and receive the notifications as per the Journey setup, such as receiving a discount after 24 hours, while new users who meet the criteria during the pause do not enter. Once the Journey resumes, new users qualify again based on the cart abandonment trigger. Existing user progress remains unaffected by the paused period.

<Image alt="User Entry and Movement in Paused State" align="center" border={true} src="https://files.readme.io/8f53f43f6d2bf593957d3fd51ab66753c3d0a36009497ab9f6a31af58422c7c9-Paused.gif">
  User Entry and Movement in Paused State
</Image>

## Editing Journey in Paused State

While updates to the What section, such as message content or provider settings, are still allowed without versioning, any structural changes require you to create a new draft version. This includes edits to nodes, paths, goals, and qualification logic.

When you publish the new version, CleverTap prompts you to choose how to handle the paused version:

* **Stop the older version**, if you want all users to move to the new version immediately
* **Mark the old version Restricted** if you want to allow existing users to continue moving through it. The new users who meet the updated entry criteria are routed into the new version of the journey. Once you move the older journey to Restricted, it cannot be resumed. 

> 📘 Note
>
> Only one version of a journey can be in the Paused/Running state at a time.

# Stopped

The Stopped state indicates that the journey has been permanently deactivated. Users currently in the journey do not progress further, and actions are halted. 

<Image alt="User Entry and Movement in Stopped State" align="center" border={true} src="https://files.readme.io/d37e56e4b883fcc1cbf6eaf85b1ba34bb3f4c462b274b7f6528058564920684b-Stopped.gif">
  User Entry and Movement in Stopped State
</Image>

## Editing Journey in Stopped State

You can make changes to a stopped journey by creating a new draft version. This allows you to modify all aspects of the journey, including nodes, paths, goals, and qualification criteria.

Once the new version is published, it becomes the active version of the journey. The stopped version remains inactive; users do not progress, and no new users qualify for it. Any users still present in the journey are exited automatically within 30 to 60 days.

# Completed

The Completed state signifies that the user entry is marked complete. The already qualified users continue to move ahead and move out of the journey once they all get timed out (refer to the following GIF).

<Image alt="User Entry and Movement in Completed State" align="center" border={true} src="https://files.readme.io/854ba478e8cd88e48cda04e1e449cbf26cf26ebb353e680b83dbebbf24a8125e-Completed.gif">
  User Entry and Movement in Completed State
</Image>

## Editing Journey in Completed State

You can make changes to a Journey in the Completed State by creating a new draft version. This includes updates to nodes, paths, goals, and entry criteria. When you publish the new version, you will be prompted to choose how the completed version should be handled:

Once you publish a new version, you can:

* **Force exit from version**, if you want all users to move to the new version immediately
* **Keep moving in version** if you want to allow existing users to continue moving through it. The new users who meet the updated entry criteria are routed into the new version of the journey.

<Image alt="Edit a Journey in Completed State" align="center" border={true} src="https://files.readme.io/b18a8d5c4aea555b1672fe3ac6404078cb7e21f819b8cd894e9dece8b2b35cf2-Edit_a_Journey_in_Completed_State.png">
  Edit a Journey in Completed State
</Image>

# Restricted

The Restricted state indicates that the journey version is no longer accepting new users, but users who have already qualified will continue to progress through the journey. This is a system-driven state that is applied when a new version of the journey is published and the previous version is not stopped, but retained to support in-progress users.

For example, consider a running journey that you edit and publish as a new version. If you choose not to stop the previous version, it enters the Restricted state. In this state, the journey flow remains active only for users already inside the journey; no new users will enter.

<Image alt="User Entry and Movement in Restricted State " align="center" width="90% " border={true} src="https://files.readme.io/6ed85c1e970478e35469e9dd240d3f26c4babbd9935d531e4d75b55f112f338c-Restricted_state_-_Static_New_Journey.png">
  User Entry and Movement in Restricted State 
</Image>

A version in the Restricted state cannot be made active again. This state exists solely to ensure continuity for users already in the journey while new users are directed to the latest active version.

## Editing Journey in Restricted State

Journey in the Restricted state supports limited edits to the *What* section. To edit the journey beyond the What section, select *Full editing* to create a new version. This initiates a new draft version. Once published, the older version remains restricted, and only the new version will remain active.
