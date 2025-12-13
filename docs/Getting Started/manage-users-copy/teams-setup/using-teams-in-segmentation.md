---
title: Using Teams in Segmentation
excerpt: >-
  Learn how to use the Teams feature in Segmentation to manage and access
  team-specific segments.
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

The [Teams](doc:teams-setup) feature helps organizations streamline access to CleverTap entities such as Segments, Campaigns, and Journeys by assigning users to specific teams. With Teams enabled, users work within their designated team context, ensuring they view and manage only the segments created by their own team.

Whether operating across geographies or verticals, Teams ensures:

* Users work with segments that align with their goals and responsibilities
* Cross-team access to audiences is prevented by default.
* Segment ownership remains clear and auditable
* Collaboration across brands, regions, or pods is streamlined and secure

Teams work alongside Roles to define both **what users can do** (permissions) and **what they can access** (team-scoped entities). For more information, refer to [User Roles and Access](doc:teams-setup#user-roles-and-access).

> 📘 Private Beta
>
> This feature is released in Private Beta and enabled only for select customers. To enable this feature, contact your Customer Success Manager or raise a support ticket.

# View and Filter Segments by Team

The Segments listing page includes a **Teams** column that displays the associated team for each segment.

* **Admins** can view segments for the team they are currently logged in with. They must switch to that team to view segments from another team.
* **Non-admin users** can view and manage only the segments from your current (logged-in) team. If you are part of multiple teams, you must switch to a different team to view segments from that team.

<Image alt="View Assigned Team for Segment" align="center" border={true} src="https://files.readme.io/29e173e2455ec570314e37515bd1e9fac1781162be8c61c797ec54ec3ad0d386-image.png">
  View Assigned Team for Segment
</Image>

# Segment Creation within Team

When you create a segment, it is automatically associated with the team you are currently logged into. Also, if you create a segment using Include or Exclude conditions, you can only select data (events, properties, or other segments) that belong to your current team.

The selected team appears at the top of the segment builder. 

You cannot manually change or assign a team during segment creation. If you are part of multiple teams, switch to the relevant one before starting segment creation.

<Image alt="Teams in Create Segment" align="center" border={true} src="https://files.readme.io/7cc115e77a856cded61c51c032505e7676f1b464322051e6188f3c66a3f3530b-image.png">
  Teams in Create Segment
</Image>

# Team Access for System Segments

CleverTap includes a set of predefined segments, such as **All Users** and **Test Users**, which follow preset rules and are automatically assigned to the Default Team.

* [Default team](doc:teams-setup#handle-existing-users-and-entities) includes these system segments by default.
* Only Admins and users in the Default Team have access to these system segments.

# Event Access in Segmentation

With Teams enabled, users can access only the events scoped to their current team when creating or editing segments. This ensures every team works with its own data, reinforces governance rules, and avoids accidental cross-team targeting.

The following table outlines how CleverTap enforces event-level visibility during segmentation:

| User Action                                    | What You See                                                                        | Why It Happens                                      | Example                                                                                                                                                                                             |
| ---------------------------------------------- | ----------------------------------------------------------------------------------- | --------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Create a new segment                           | The **Event** dropdown shows only events your current team can access               | Enforces team-level data boundaries.                | Team A user sees only "Install Completed", "Signup Form Viewed", and not events from any other team.                                                                                                |
| Edit or clone a segment with restricted events | Events appear as read-only                                                          | These events are no longer accessible to your team. | You clone a segment that includes the event **"Gold Tier Upgrade"** (created by another team). In the segment builder, the event appears as read-only. You must remove or replace it before saving. |
| Save a segment without an active team session  | System blocks save and prompts re-login                                             | A valid team ID is required for all segments.       | After a session timeout, clicking **Save Segment** throws an error.                                                                                                                                 |
| View the Segments page                         | Only segments from your assigned teams are shown; **Team filter** is auto-selected. | Ensures a focused, team-specific view of segments.  | A user in Team B sees only 12 segments, while an admin sees all the segments.                                                                                                                       |

> 📘 **Team Visibility on Legacy Feature Versions**
>
> On legacy versions of CleverTap features, segments from teams you are not part of are completely hidden, both on the dashboard and API responses. This ensures that segmentation data always reflects your active team context and prevents unintended data exposure.

# Segments in Engagements

When Teams is enabled, each engagement automatically aligns with the user’s active team. This framework ensures clarity, governance, and consistency across all Campaigns and Journeys.

While creating a Campaign or Journey:

* The Who section shows only segments linked to your current team, helping you target relevant audiences without cross-team overlap.
* You continue working under the same team context until you log out and log in with another team.
* Campaigns can only use segments from the assigned team. The validation ensures correct team alignment at publish time.

For more information, refer to [Teams in Engagements](doc:using-teams-in-engagements).

> 🚧 **Sharing Segments Across Teams**
>
> If you change the selected team while a campaign is in draft, any segments linked to a different team become invalid and must be replaced.

# FAQs

The following are the answers to the common questions about using Teams with Segments:

### What happens to existing segments when we enable Teams?

When Teams is enabled, all existing segments are automatically assigned to the Default Team created by CleverTap. This ensures that no segments are hidden or lost.

### Can I access my old segments if my team is changed?

No. You lose access to segments from your previous team unless you are part of the Default Team or have Admin access.

### Can I migrate a segment to another team?

No. Once you create a segment, you cannot change the assigned team.

### Can I share a segment across teams?

No. Segments belong to a single team and are visible only to members of that team.

### What happens if someone is removed from a team while setting up a Campaign or Journey?

If a user is removed from a team during setup, they immediately lose access to that team's segments. The Campaign or Journey becomes invalid, and they must either replace the segments or be reassigned to the team to proceed
