---
title: Using Teams in Engagements
excerpt: >-
  Learn how to use Teams feature to create, manage, and access Campaigns and
  Journeys.
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

The [Teams](https://docs.clevertap.com/docs/teams-setup) feature in CleverTap introduces scoped access for both engagements (campaigns and journeys), ensuring that users only view, create, manage, and publish items that belong to their assigned teams. This enforces cleaner ownership and stricter governance and prevents cross-team content visibility.

This document explains how Teams affects the creation, editing, and approval workflows, segment usage, and visibility of campaigns and journeys.

> 📘 **Private Beta**
>
> This feature is released in Private Beta and is enabled for select customers only. To enable this feature, contact your Customer Success Manager or raise a support ticket.

# Access and Roles

Teams work alongside Roles to define both **what users can do** (permissions) and **what they can access** (team-scoped entities). For more information, refer to [User Roles and Access](https://docs.clevertap.com/docs/teams-setup#user-roles-and-access).

# View Assigned Team for Engagements

The Campaigns and Journeys listing pages display a Team column that shows the team associated with each engagement. This helps maintain clarity of ownership and restricts access based on team membership.

* Non-admin users see only campaigns and journeys from the team they are currently logged into.
* Admins can view all engagements, but must use the team switcher to view and manage campaigns for a different team.
* If you access a campaign or journey via a shared link and are not part of the associated team, a *Permission Denied* error is displayed.

<Image alt="View Assigned Team for Engagements" align="center" border={true} src="https://files.readme.io/2a50adbf2833e1460d04d2e919522062048ccc4e8d2706ba8ef0daa5449104e5-screen.png">
  View Assigned Team for Engagements
</Image>

The filter only displays the current logged-in team, as each session is scoped to a single team. Users must switch teams using the team switcher in the top navigation bar to view engagements from another team.

<Image alt="Engagements Filtered Basis Current Logged In Team" align="center" border={true} src="https://files.readme.io/f62e226cbc3431dda9b9d9d302fa502565ab4c7016135e731228e52d2c723880-Filter_Engagements_Basis_Current_Logged_In_Team.gif">
  Engagements Filtered Basis Current Logged In Team
</Image>

The campaign and journey listing pages display a **Team** column to indicate the team to which the engagement is associated.

* You can view only the campaigns or journeys that belong to your assigned teams.
* Admins can view campaigns and journeys across all teams.
* If you try to access a campaign or journey via a shared link belonging to a different team, the *Permission Denied* error displays. 

This view ensures that entity visibility aligns with the access rules defined through Teams.

<Image alt="Teams in Campaign Listing" align="center" border={true} src="https://files.readme.io/85c7d4a2d63eb0af415f725054200340ab2f662123298c247903c6c52196849d-Teams_in_Campaign.png">
  View Assigned Team for Campaign
</Image>

# Engagement Creation within Team

When a user creates a new campaign or journey, the team assignment step determines where that item will reside and who will be able to access it:

* If the user is assigned to only one team, that team is automatically selected and locked. The user cannot change it.
* Admins can create campaigns and journeys under any team, as they are implicitly part of all teams.
* While they are implicitly part of all teams, they must still create each item from within a specific team context. This means the campaign will belong to the team they are currently logged into. 
* Admins can switch teams using the team switcher to create an engagement for the required team.

This behavior ensures that all entities are always created within a valid team scope.

<Image alt="Team Selection" align="center" border={true} src="https://files.readme.io/9959c03feb2b9fb9918dc6ca1ceb5503cd6c0129f62a3e1710e33cc2a6d5dfb0-Engagement_Creation_Within_Team.png">
  Team Selection for Campaigns
</Image>

<Image alt="Assign Journey to a Team" align="center" border={true} src="https://files.readme.io/207976183656c4ab029e8950db82f0e2710967bc757dbe174907e83e3143d6bc-Team_Selection_for_Journeys.png">
  Team Selection for Journeys
</Image>

This selection ensures the engagement is created with the correct access rights.

> 📘 **Default Team Behavior**
>
> * When Teams is enabled, all existing campaigns and journeys created before teams are automatically assigned to the Default Team. Any new entity created without a selected team will also default to this team.
> * The Default Team cannot be deleted or renamed, and its campaigns and journeys are visible only to users who belong to it or Admins.

# Segmentation in Engagements

During campaign or journey creation, only segments from the same team are available in the *Who* section, and when configuring any segment-based node, such as Goals, Conditional Split, or IntelliNODE for journeys. This also applies to Include/Exclude segments.

> 🚧 **Sharing Segments Across Teams**
>
> If you change the team in draft state, previously selected segments from a different team become invalid and must be replaced.

# Event Access in Campaigns

CleverTap enforces team-scoped event visibility to ensure users only interact with event data relevant to their assigned team. This enables cleaner governance and safeguards cross-team access. 

> 📘 **Note**
>
> Filtered event access applies only to custom events. System events are always visible to all users and cannot be restricted.

When a team is assigned to a user, the events accessible in campaigns are scoped to that team’s configuration. For more information on setting up Events in Teams, refer to [Event Visibility in Teams](https://docs.clevertap.com/docs/teams-setup#event-visibility-in-teams).

During campaign creation, editing, or cloning, event-based configurations will behave as follows:

| **Section**              | **What You See**                                           | **If Events Are Restricted**                                                                                    |
| ------------------------ | ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Conversion Tracking**  | The event dropdown only shows events from your team.       | If cloning a campaign with a restricted event, an error occurs. Remove or replace the event to continue.        |
| **Target Segment**       | Only segments using accessible events are allowed.         | The campaign throws an error until the segment is updated to remove restricted events.                          |
| **Delivery Preferences** | Best Time configurations show only team-accessible events. | The campaign cannot be published if the selected configuration uses restricted events.                          |
| **Publish Campaign**     | A validation check runs before publishing.                 | If any section contains restricted events, publishing is blocked until all such events are replaced or removed. |

# Event Access in Journeys

Journeys also enforce team-scoped event access. Any triggers, goals, or personalization used in the journey builder must be based on events accessible to the assigned team.

| Journey Area                        | What You See                                                       | If Events Are Restricted                                                                       |
| ----------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| **Trigger Node**                    | The event dropdown shows only team-accessible events.              | If you select a restricted event, an error prevents you from saving or publishing the journey. |
| **Goal Node**                       | You can define conversion events only from your team’s event list. | Journeys cloned from another team must replace restricted goals before activation.             |
| **IntelliNODE / Conditional Split** | Event-based splits show only team-scoped events.                   | If a restricted event is referenced, the node becomes invalid and must be edited.              |
| **Publish Journey**                 | A full validation check is performed before publishing.            | Journeys using events outside your team’s scope cannot be published until corrected.           |

# Events Access During Personalization

CleverTap’s personalization features, including Liquid Tags, Linked Content, and Recommendations, respect team-based event access. 

| Feature                                         | What You See                                                         | If Events Are Restricted                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Liquid Tags**                                 | Only event properties from accessible events appear in the dropdown. | When cloning, if an event used in a Liquid Tag is restricted, the event property dropdown appears empty, and you must reselect properties from accessible events. If personalization is added to a running campaign, the **What** section becomes restricted due to a team change. The user cannot go back and edit it. To make changes, they must clone the campaign and update the tag with an accessible event. |
| **Linked Content / Recommendations / Catalogs** | Only accessible events are allowed for triggers or logic.            | Users must reconfigure the personalization block to continue if restricted events are detected (for example, during cloning).                                                                                                                                                                                                                                                                                      |

# How Campaign Approval Works with Teams

When Teams is enabled, campaign approval requests are routed based on the team assigned to the engagement. The approval logic is as follows:

* Admins receive all approval requests, regardless of the team under which the campaign or journey was created.
* Approvers receive approval requests only for campaigns created within teams to which they are assigned.

The following table outlines how approval requests are routed based on the user’s role, team assignment, and the team under which the campaign was created:

| User Type      | User’s Team | Campaign Team | Receives Request? | Notes                                                           |
| :------------- | :---------- | :------------ | :---------------- | :-------------------------------------------------------------- |
| Admin          | All Teams   | Any Team      | Yes               | Admins are global and always receive requests                   |
| Approver       | Team A      | Team A        | Yes               | Same team and therefore has approval permission                 |
|                | Team A      | Team B        | No                | Different team, and therefore does not have approval permission |
| Member/Creator | Team A      | Team A        | No                | No approval permission                                          |

# FAQs

Here are answers to common questions about using Teams with Campaigns and Journeys.

### Can a campaign or journey be moved to another team after publishing?

No. The team reassignment is allowed only in the *Draft* state.

### What happens if a user is removed from a team?

If a user is removed from a team, they lose access to all engagements belonging to that team. Any entities the user created while they were part of a team remain associated with that original team, even if the user later joins or moves to a different team.

### Can segments from one team be used in another team’s campaign or journey?

No. Segment usage is restricted to the team selected during campaign and journey creation. 

For setup details, refer to [Teams Setup](https://docs.clevertap.com/docs/teams-setup) and for segment-specific rules, refer to [Teams in Segmentation](https://docs.clevertap.com/docs/using-teams-in-segmentation). 

### What happens if a campaign or journey uses an event that your team does not have access to?

If your team cannot access a previously used event (for example, when editing or cloning an engagement), the event will appear as read-only. Replace or remove it before saving or publishing the campaign.
