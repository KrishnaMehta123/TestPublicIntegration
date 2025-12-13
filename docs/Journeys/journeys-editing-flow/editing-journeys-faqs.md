---
title: 'Editing Journeys: FAQs'
excerpt: Find answers to frequently asked questions.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# FAQs

Find answers to the following common questions about editing a Journey.

### What can I edit in a journey?

There are two ways to make edits:

- **Partial Edit**: Using this option, you can make non-structural changes directly to the current version of a _Running_ journey. This includes modifying message content, user distribution in the IntelliNODE journey, and the service provider. 
- **Full Editing**: Using this option, you can make structural or behavioral changes requiring the creation of a new journey version. Selecting this option allows you to change all the journey components. This allows you to evolve the journey logic while preserving continuity for in-progress users and maintaining a record of changes across versions.

For more information about editing, refer to [Edit a Journey](doc:edit-a-journey). 

### What happens to the old version and users in it when I publish a new one?

The previous version either moves to the Restricted or Stopped state. If you choose to move the older journey version to the Restricted state:

- The users who had entered the journey continue progressing in the older journey version. No new users enter the restricted journey version, and user entry to this version is stopped.
- New users who meet the updated entry criteria are routed into the new journey version.

If you choose to move the older to the Stopped state:

- All users in the previous version are forced to exit the journey version.
- The new journey version transitions to the Scheduled state on Publish and automatically moves to the Running state after two hours.
- The users who exited the older version could qualify for the new version.

 Journey versioning ensures that older versions, including their design and performance data, remain accessible for reference. Only one version can be in the _Running_ state at any given time. For more information, refer to [Journey States](doc:journey-states-edit-a-journey). 

### What happens to user entry and movement in the journey with the creation of a new version?

In a journey entity with multiple versions:

- Users entry is stopped in all the older versions in the Restricted or Paused state.
- Users are allowed to enter only the latest running version per the entry criteria.

For more information, refer to [Journey States](doc:journey-states-edit-a-journey).

### How can I view Stats for a particular version?

Each journey version has its own set of stats. Use the Version dropdown in the journey stats view to toggle between versions and analyze performance metrics independently. You can compare outcomes across versions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a2c0b26710978fb399659fac7678116e176ebb9ff05daa580232f022bb808d22-Select_Version_from_Dropdown.png",
        "",
        "Select Version to View Stats "
      ],
      "align": "center",
      "border": true,
      "caption": "Select Version to View Stats "
    }
  ]
}
[/block]


### Will creating a version consume journey limits, and how many versions can be created for a journey?

Version creation consumes the journey limits. Journeys in _Paused_, _Running_, and _Restricted_ state consume the journey limit. You can create up to **10 versions** of a single journey entity. If you want to edit this journey entity after reaching this limit, you can clone the desired journey version. 

### What would be the impact on reporting?

Each journey version maintains its own set of reports and stats. You can choose to generate reports for: _All versions of the journey_, or _Selected versions only_. This flexibility ensures that you get precise, contextual insights, whether you analyze individual journey versions or compare performance across versions. For more information, refer to [View Journey Reports](doc:viewing-journey-reports-edit-a-journey). 

### What happens to user movement between versions?

The user would remain in one version in a journey entity. The user would move between versions only when the user exits the previous version and qualifies for the new version entry criteria. For more information, refer to [Edit a Journey](doc:edit-a-journey).

### What is the difference between Paused and Restricted journeys?

A journey in the Paused state is temporarily halted manually. It does not allow new user entries, but users who have already entered continue to progress through the journey as configured. You can resume the journey at any time to start accepting new users again.

A journey in the Restricted state permanently stops the user's entry while allowing only in-progress users to continue and complete their journey flow; the journey cannot be changed to the Running state.

For more information, refer to [Journey States](doc:journey-states-edit-a-journey). 

### Once we stop a journey version, how long does it take to move the new version to _Running_ state?

When you stop the previous version while publishing the new one, all users in the previous version are forced to exit the journey. The new journey version transitions to the Scheduled state on Publish and automatically moves to the Running state after two hours. For more information, refer to [Make Structural Changes](doc:edit-a-journey#option-2-make-structural-changes).