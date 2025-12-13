---
title: Global Campaign and Throttle Limits Permissions
excerpt: Learn more about granular Channel-Level Access Control.
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

CleverTap supports granular permissions for Global Campaign Limit and Global Throttle Limit settings. These permissions allow campaign creators to view or override default campaign limits. This enforcement applies at key stages of campaign workflows such as creating, editing, cloning, stopping, archiving, and publishing campaigns.

# Global Campaign and Throttle Limits Behaviour

By default, Global Campaign Limits are applied globally across campaigns, while Throttle Limits are defined at a campaign level. When Global Campaign Limits are not applied, the default dashboard behavior is as follows:

- Global Campaign Limits checkbox: enabled
- Global Throttle Limits checkbox: disabled

> 📘 Throttle Limits for User Timezone and Best Time
> 
> Throttle limits are enforced based on a uniform send time, which is only possible while using Account Timezone. Therefore:
> 
> - Global Throttle Limits cannot be applied when **User Timezone** is selected in the _When_ section > _Date and Time_ > _Timezone_ list while setting up the campaign.
> - Global Throttle Limits cannot be applied when **Best Time for every user** is selected in the _When_ section > _Date and Time_ > _Schedule for Later_ or _Set as Recurring_ sections while setting up the campaign.

If the Global Campaign Limits are applied, then the configured limits are enforced at the campaign level. Granular control includes:

- If Global Campaign Limits must be applied, based on the user’s role.
- Read access is always enabled. Write access to override limits is based on role and cannot be changed by the user.

> 📘 Note
> 
> Roles define each user’s default behavior and whether they have permission to override the Global Campaign or Throttle Limits at the campaign level. These permissions cannot be changed by users and are defined by an Admin via _Settings > Roles_. 
> 
> For more information, contact your Admin or refer to [Role-Based Access Control](https://docs.clevertap.com/docs/role-based-access-control).

# Settings and User Role

The behavior of Global Campaign Limit and Global Throttle Limit checkboxes options is based on two factors:

- Limits at the Settings level.
- User's role permissions (Admin or Read + Write access or User with Read access).

Below are the different cases:

- [Limit Added in Settings](https://docs.clevertap.com/docs/global-campaign-and-throttle-limits-permissions#limit-added-in-settings)
- [Limit Not Added in Settings](https://docs.clevertap.com/docs/global-campaign-and-throttle-limits-permissions#limit-not-added-in-settings)

### Limit Added in Settings

When Global Campaign and Throttle Limits are already configured in Settings, the following cases are possible:

- **Admin**: The checkbox is always enabled irrespective of the Settings configuration. Admins can modify the limit settings at any time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9285b6063fb2e6a65ad9c685375b9b1e5441269a031d3807d4c2b2364427e39-Limit_Added_in_Settings-Admin.png",
        "",
        "Admin View"
      ],
      "align": "center",
      "border": true,
      "caption": "Admin View when Limits are configured in Settings"
    }
  ]
}
[/block]


- **User - Read Only**: The checkbox is visible but greyed out, and users cannot edit it. The checkbox is enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18490e5d6274b751957108350a2052f9ade429ba0aa44de7a4901335934ee7d6-Limit_added_User_-_Read_Only.png",
        "",
        "Read Only Access when Limits are configured in Settings"
      ],
      "align": "center",
      "border": true,
      "caption": "User View with Read Only Access when Limits are configured in Settings"
    }
  ]
}
[/block]


- **User - Read and Write**: The checkbox is editable. Users can choose to enable or disable this option. The initial state of the checkbox is enabled since the limit is configured. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9285b6063fb2e6a65ad9c685375b9b1e5441269a031d3807d4c2b2364427e39-Limit_Added_in_Settings-Admin.png",
        "",
        "Admin View"
      ],
      "align": "center",
      "border": true,
      "caption": "User View with Read and Write Access when Limits are configured in Settings"
    }
  ]
}
[/block]


### Limit Not Added in Settings

- **User - Read Only**: The checkbox is visible but greyed out, and users cannot modify the checkbox. It is disabled because the limit is not added in Settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5b10156134add14687fd8df94a193133cf67e9a1aa9d88266752281b890b9ed-User_-_Read_Only.png",
        "",
        "Read Only Access when Limits are not configured in Settings"
      ],
      "align": "center",
      "border": true,
      "caption": "User View with Read Only Access when Limits are not configured in Settings"
    }
  ]
}
[/block]


- **User - Read and Write**: The checkbox is editable. Users can choose to enable or disable this option. It is disabled because the limit is not added in Settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/105078da443d65ac0f1b08fa36a31073ee8abc7d8a28b7dc9dab3e52c959f8f1-Limits_not_added_-_Read_Write.png",
        "",
        "User View with Read and Write Access when Limits are not configured in Settings"
      ],
      "align": "center",
      "border": true,
      "caption": "User View with Read and Write Access when Limits are not configured in Settings"
    }
  ]
}
[/block]


# Use Cases

## Use Case 1: Modification in Role Permissions

A user’s role is changed while he is in the process of creating a campaign. In this case:

- If the user is an Approver and the role is changed to a Creator, a popup appears when the user tries to access the campaign.
- If the user is a Creator and the role is changed to an Approver, no popup is displayed. 

This alerts the users about their updated permissions and prevents unauthorized overrides.

## Use Case 2: Creator vs. Approver Role Permissions

A user is assigned both roles, Creator and Approver. These two roles behave differently during campaign creation. In this case:

- The page defaults to the Creator's configuration if both roles are assigned, and initially loads with Creator settings.
- Approver override permissions apply only if he opens the campaign and clicks **Edit Limits**. in _Setup_

| Role     | Global Campaign Limits Default | Override Option    | Handling                                |
| -------- | ------------------------------ | ------------------ | --------------------------------------- |
| Creator  | Enabled                        | No (read-only)     | Page loads with Creator settings        |
| Approver | Disabled                       | Yes (can override) | Override is possible only after editing |

This ensures that only authorized users can modify global limit settings.

## Use Case 3: Draft Campaigns and Updated Permissions

A campaign has default Global Campaign Limits settings and override permissions. This campaign is saved as draft. After this, changes are made to the Global Campaign or Throttle Limits permissions in the draft campaign. In this case:

- Upon clicking **Save**, **Publish**, or **Schedule**, the system checks if Global Campaign or Throttle Limits permissions have changed for the user’s role. 
- If the permissions are updated, a popup notifies the users that their access has been updated.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/88139289e3cb01e7b531ac93c9ee255c667c6a631600cf11dad5f4f0eb618bc6-Role_change.png",
        "",
        "Global Campaign Limits Modified"
      ],
      "align": "center",
      "border": true,
      "caption": "Global Campaign Limits Modified"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de55004ac83f508da98cbb8ed598d991cbee5447ca3c146c78e1be71d6ecb783-Throttle_Mismatch.png",
        "",
        "Global Throttle Limits Modified"
      ],
      "align": "center",
      "border": true,
      "caption": "Global Throttle Limits Modified"
    }
  ]
}
[/block]


This ensures the campaign adheres to the latest permission rules and cannot bypass newly enforced global limits.

## Use Case 4: Edit Icon Accessibility

A user lacks write access to override Global Campaign or Throttle Limits. In this case:

- The Edit icon for campaign limits is always visible.
- Clicking the **Edit icon** opens the _Setup_ page, but the Global Campaign and Throttle Limits options are disabled.
- So, the user will not be able to interact with the checkboxes without write access. 

This allows consistent navigation while enforcing permission restrictions on actual changes.

## FAQs

### Can I remove the Edit icon if a user lacks permissions?

No. The edit icon for Campaign Limits is always shown. Global Campaign and Throttle Limits override permission only controls the checkbox editability, not access to the edit icon.

### A user's permissions are modified to read-only, how can the user publish that campaign?

If a user's permissions are changed to Read-Only while creating a campaign (or working on a draft), the user cannot publish the campaign. In this case:

- The user can create a new campaign with their current permissions.
- The user can connect with the admin to restore their permissions, and the campaign can be published.
- Any other user with the necessary permissions can publish the campaign.