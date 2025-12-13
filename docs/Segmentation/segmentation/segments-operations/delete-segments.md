---
title: Delete Segments
excerpt: Understand how Segment Deletion works in CleverTap.
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

Segment Deletion allows you to safely remove segments without affecting ongoing engagements, such as Campaigns, Journeys, Bulletins, Product Experiences, or other types of segments. This feature prevents the deletion of currently used segments, helping to eliminate potential issues such as targeting the wrong audience, causing business disruptions, or interrupting communication with your users.

Learn how and when you can delete segments and manage dependencies.

> 📘 Deletion Dependency
>
> Before deleting a segment, it is essential to verify if it is in use in active engagements to prevent disruption. CleverTap allows segments to be deleted only when it is safe.

# Validations for Dependent Segments

When deleting a segment, CleverTap automatically checks if it is included or excluded in any other segments or engagements. CleverTap ensures segments are safely deleted by validating their dependencies:  

* **Segments in Active Engagements**: A segment cannot be deleted if it is part of an active engagement. To delete a segment used in an active engagement, you must stop the active engagement.
* **Segments with Dependent Segments**:  A segment that depends on another segment can be deleted if the related segments do not have any engagements.

This process ensures the seamless operation of all engagements and avoids errors caused by missing segments.

## Understand Deletion Rules for Engagement Types

Segments can be used in various engagement types, and their deletion depends on the engagement state. The following table shows the engagement state when segments can or cannot be deleted:

| **Engagement Type** | **States Allowing Segment Deletion**                           | **States Restricting Segment Deletion**                          |
| ------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------- |
| **Campaign**        | Draft, Stopped, Completed, Approval Pending, Expired, Archived | Scheduled, Running, Awaiting Next Run (unless stopped or paused) |
| **Journey**         | Draft, Stopped, Archived                                       | Published, Running, Paused, Completed (unless stopped or paused) |

# Handle Deleted Segments in Cloned Engagements

When cloning engagements that include deleted segments, CleverTap provides alerts. The segment builder highlights the deleted segment's name in Campaigns and Journeys.

## Deleted Segments in Campaigns

When cloning a Campaign that includes a deleted segment, the system displays an error message in the campaign's *Who* section. This validation ensures campaigns are not published with invalid or outdated segments, helping maintain the accuracy of your audience targeting.

<Image alt="Cloning a Campaign with a Deleted Segment" align="center" border={true} src="https://files.readme.io/e0bd40208b61671723e6e1410a5e1f30edfec66537db1d222281ff2f404d693f-Campaign____Cloned_7.png">
  Cloning a Campaign with a Deleted Segment
</Image>

## Deleted Segments in Journeys

Similarly, when publishing a cloned Journey that includes a deleted segment, the system highlights all the nodes in red that use one or more deleted segments.

<Image alt="Highlighted Node in Red" align="center" border={true} src="https://files.readme.io/4a3a1b49eab3c3867ec0e18ffc7495aa65268b9c9bc8729b0b994d8665581d7b-Red_Nodes_in_Journey.png">
  Highlighted Node in Red
</Image>

On opening those nodes, the system displays the error message in the node's *Who* section.

<Image alt="Publishing a Journey with a Deleted Segment" align="center" border={true} src="https://files.readme.io/de36570738cb6e4a88941e22e13fd620417ec34328ba314d24ad4b71482a2aca-Frame_790.png">
  PublishingWhen a Journey with a Deleted Segment
</Image>

## Resolve Cloned Engagements

Ensure the accuracy of your audience targeting by resolving issues with deleted segments in cloned engagements.

You will not be able to publish the cloned engagement until you either:

* Replace the deleted segments with an available segment, or
* Remove the deleted segments from the campaign's *Who* section.

If you do not remove the deleted segment from the cloned engagement, the *Who* section will remain incomplete, and the **Publish** button will be disabled, preventing the engagement from being published.

This validation ensures that all segments used in the engagement are valid and prevents issues that may arise from targeting outdated or invalid segments.

# FAQs

### Q. What happens if I delete a segment still in use?

A. If a segment is still in use, the system will prevent you from deleting it until the associated engagements are stopped.

### Q. Can I delete a segment used in a previous campaign?

A. Yes, you can delete segments from engagements that have been completed, stopped, or archived.

### Q. Why can not I publish my cloned campaign if it contains a deleted segment?

A. If your cloned campaign includes or excludes a deleted segment, the system prevents publishing until the segments are replaced or removed.
