---
title: Role-Based Access Control (COPY)
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

As a part of our commitment to account security, CleverTap offers Role-Based Access Control (RBAC) for account administrators to enable different levels of access for dashboard users.

> 📘 RBAC for Product Experiences
> 
> Role-based access control (RBAC) is now supported for _Product Experiences_. For more information, refer to [Product Experiences](doc:product-experiences).

## Invite Users

The user needs an invitation and an appropriate access level to access the CleverTap dashboard. For more information about inviting users to the dashboard, refer to [Manage Users](doc:manage-users#invite-users).

# Types of Roles

Roles in CleverTap can be broadly categorized as System Roles and Custom Roles. Each of these roles has been discussed in detail in the following sections.

## System Roles

CleverTap provides four standard system roles for every account. These roles cannot be cloned, deleted, or edited.

- **Admin**: Full and unlimited access to the account.

  - Assign new users as Admin, Creator, Member, or custom roles.
  - Revoke access of an existing user.
  - Create campaigns.
  - Stop and archive campaigns.
  - Approve or reject campaigns created by users in the Creator role.
  - View analytics.
  - Download user profiles.
  - Download reports.
  - Add and update billing details.
  - Read and modify the Schema of Event and profile Properties
  - Manage Security Features viz. IP Whitelisting, 2FA & Campaign Approval Workflow

- **Creator**: Create, edit, schedule, and stop any type of engagement such as campaigns, journeys, and product experiences.

  - Create engagements.
  - Stop and delete engagements.
  - View analytics.
  - Download reports.
  - A Creator cannot perform user-setting or role-setting actions. Additionally, they cannot view billing information.

- **Member**: View analytics and reports in the account.

  - Read-only access.
  - View analytics, including campaign performance.

- **Approver**: Approve campaigns created by users in the creator role.
  > 📘 Note
  > 
  > The Approver role can only be accessed when the [Campaign Approval Workflow](https://docs.clevertap.com/docs/campaign-approval-workflow) feature is turned on.
  - Create campaign.
  - Stop and archive campaigns.
  - Approve or reject campaigns created by users in the Creator role.
  - View analytics.
  - Download user profiles.
  - Download reports.
  - An Approver cannot perform user-setting or role-setting actions.

## Custom Roles

To create a custom role, perform the following steps:

1. Navigate to _Settings_ > _Roles_ from the dashboard.  
2. Click **+ Role**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4c349d-2020-05-13_16-12-18_Create_Role.png",
        "Click +Role to Create a New Role",
        1235
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Role"
    }
  ]
}
[/block]


3. Select the required permissions for _Component access_ and click **Save & Continue**.
4. Select the suitable role for _Data access_ and click **Save & Continue**. You can see the overview of the permissions that you assign for the new role.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e94d77-Overview_section.png",
        "Select the Required Permissions for Component access",
        2384
      ],
      "align": "center",
      "border": true,
      "caption": "Assign Permissions to Users by Selecting Components"
    }
  ]
}
[/block]


5. Click **Create Role** and enter the _Role name_ to identify the new role uniquely.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0192c27-Enter_Role_name.png",
        "Enter Role name",
        554
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Enter Role Name"
    }
  ]
}
[/block]


# Define Access for Custom Roles

## Define Access for Basic Custom Roles

When inviting a new user, the administrators can assign a custom role to the user. Administrators can also create a new custom role or clone an existing custom role.

Set up a role by defining two things:

1. Component - Select the component for which you want to grant access.
2. Access levels:

- Read Access - Only allowed to view the feature (e.g., view campaign stats). Suppose a particular entity is accessible to you with Read Access. You can open it and see what is present, but you can not modify anything in the entity or download any data.
- Write Access - Allowed to read and write the feature (e.g., create campaigns). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26c2f69-2020-05-13_16-21-33_Custom_Role.png",
        "Assign Access Permissions",
        1210
      ],
      "align": "center",
      "border": true,
      "caption": "Assign Access Permissions"
    }
  ]
}
[/block]


## Define Access for Advanced Custom Roles

Custom roles can be mapped to user groups for advanced role-based access control. You can give access to different datasets to various users and restrict access to the data you don't want them to view on the CleverTap dashboard. Administrators can also restrict data access to new custom roles based on selected user properties such as geographies. Users assigned to these roles are limited to only read/write data available to the particular role. 

> 👍 Advanced Custom Role Example
> 
> You can grant access to a role _US Campaign Manager_ where the role has write access to campaigns for only users in the United States. You cannot create campaigns for users in other geographies.

1. Assign permissions for component access and define which feature components are available to the user role. 
2. (Optional) Mask [personally identifiable information](role-based-access-control#mask-personally-identifiable-information) or [events](role-based-access-control#mask-events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22c915f-Mask_Events_and_PII.png",
        "You can mask personally identifiable information and events",
        "Assign Permissions and Configure Roles for Privacy"
      ],
      "align": "center",
      "border": true,
      "caption": "Assign Permissions and Configure Roles for Privacy"
    }
  ]
}
[/block]


3. Assign permissions for data access and define the user property data accessible by the user role.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f0507e1-Mapping_User_Properties.png",
        "Mapping User Properties",
        1369
      ],
      "align": "center",
      "border": true,
      "caption": "Map User Properties"
    }
  ]
}
[/block]


# Segment Access

Segment access management in roles allows you to better manage your security, compliance, and data management. If you have dashboard users who are responsible for all marketing activities in specific sub-regions, you can grant access to only that segment of users who are from the sub-region.

> 👍 Segment Access Example
> 
> You have operations in Spain, Germany, England, Greece, and Italy and each region is managed by a regional manager. You can create a role for each of these regions where access to end-user data is restricted by their geography. In this way, each regional manager will have access to only end-users only from their region.

> 📘 Note
> 
> By picking the user property that the role is granted access to, you are restricting access to all data on CleverTap. Even if the role is viewing 'All Users' data, it is default limited to the access restriction for that role. You cannot assign more than one segment role per user.

# Operations on Custom Roles

You can edit, clone, or delete custom roles. To do so, click the ![Ellipsis](https://files.readme.io/2717d2a-ellipses_icon.png) icon and select the respective action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29d8c80-2020-05-13_16-33-51_Edit-Clone.png",
        "View Role Operations",
        1219
      ],
      "align": "center",
      "border": true,
      "caption": "Role Operations"
    }
  ]
}
[/block]


## Access Rules and Handling Clashes

Permissions and access can be set while creating a custom role. The following order of preference applies.

- A user can only be assigned a system role and custom role(s).
- **Permission Clash on System Roles**: When a user is assigned multiple system roles, there is a permission clash, and only the role with the higher access level is assigned. For example, if a user is assigned both Admin and Creator roles, the Admin role is assigned. Thus, a user cannot have multiple system roles assigned at the same time.
- **Component Clash on System Role & Custom Role**: When a user is assigned a System role and a Custom role, there can be situations where one role has access to a component, and another role does not allow access to the same component. In this case, the permissions assigned for that component will be the least access level of all the assigned roles.  
  For example, a user has the following two roles: 

  - **Creator**: has write access to Campaigns.
  - **Custom Role A**: does not have access to the Campaigns component. 

  In this scenario, the user will have write access to the Campaigns. 

  Let us take one more example: A user has the following two roles:

  - **Creator**: has write access to Campaigns.
  - **Custom Role B**: has read access to the Campaigns component. 

  In this scenario, the user will have read access to the Campaigns.
- **Component Clash on Custom Roles**: When a user is assigned multiple Custom roles, there can be situations where one role has access to a component, and another role does not allow access to the same component. In this case, the permissions assigned for that component will be the least access level of all the assigned roles.  
  For example, a user has two custom roles: 
  - **Custom Role C**: has write access to Campaigns.
  - **Custom Role D**: does not have access to the Campaigns component.  
    In this scenario, the user will have write access to the Campaigns.  
    Let us take one more example: a user has the following two custom roles:
  - **Custom Role C**: has write access to Campaigns
  - **Custom Role D**: has read access to the Campaigns component.  
    In this scenario, the user will have read access to the Campaigns.

## General rules of access

- Any write access automatically gives read access to the user.
- All users can have multiple custom roles; however, a user cannot have multiple system roles. 
- A user can have access to both system and custom roles at the same time. They can have one system role and unlimited custom roles. 
- System roles cannot be edited.

## Components of Access

Only the users with Admin roles can alter and assign access to custom roles. 

| Component   | Subcomponents                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| :---------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Boards      | <ul> <li>Daily Boards</li> <li>Custom Boards</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Segments    | <ul> <li><strong>Manual segmentation</strong>: Segments, Find People</li> <li><strong>Automated segmentation</strong>: Goals, IBM, RFM</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Analytics   | <ul> <li><strong>Core Analytics</strong>: Events, Funnels, Cohorts, Trends, Attribution, Device Crossovers</li> <li><strong>Advanced Analytics</strong>: Pivots, Flows</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Engagement  | <ul> <li><strong> Campaigns</strong>: Campaigns, Clever Campaigns</li> <li><strong>Journeys</strong></li> <li><strong>Recommendation</strong></li> <li><strong>Catalogs</strong></li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Real Impact | <ul> <li><strong>Control groups</strong>: Custom Control Group, System Control Group</li> <li><strong>Real Impact dashboard</strong></li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Settings    | <ul> <li><strong>Billing</strong>: Billing, app usage, plans, invoices</li> <li><strong>Account Settings</strong>: Add new app, change account, timezone, privacy settings, uninstall</li> <li><strong>User Settings</strong>: Invite user, revoke access, account settings</li> <li><strong>Role Settings</strong>: Role Based Access Control</li><li><strong>Event and User Properties</strong>	</li> <li><strong>CSV Uploads</strong>: Profile uploads and external user list	</li> <li><strong>My Profile And Password	</strong></li> <li><strong>Exports</strong>: Events and profile exports to amazon S3</li> <li><strong>Downloads</strong>: Download profiles</li> <li><strong>Email Reports</strong>: Campaign and Journey reports	</li> <li><strong>Campaign Integration and Settings</strong>: Push, Email, SMS, Web Push, FB, Google AdWords</li> <li><strong>Campaign Settings</strong>: Campaign limits, Best Time settings</li> </ul> |

## Mask Personally Identifiable Information and Events

There are two options available for masking data on user profiles:

### Mask Personally Identifiable Information

   This option allows you to mask the data that describes personal information such as Email, Phone number, Location, Gender, User properties, as well as other sensitive data.

  When the _Mask Personally Identifiable Information_ is enabled, the user Profile page appears as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dda9129-mask_PII.png",
        null,
        "Masking Personally Identifiable Information "
      ],
      "align": "center",
      "border": true,
      "caption": "Masking Personally Identifiable Information "
    }
  ]
}
[/block]


### Mask Events

This option masks the data that shows the event activity of a user profile.

   When _Mask Events_ is enabled, the user Profile page appears as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81c5045-Mask_Events.png",
        null,
        "Masking User Profile Events"
      ],
      "align": "center",
      "border": true,
      "caption": "Masking User Profile Events"
    }
  ]
}
[/block]