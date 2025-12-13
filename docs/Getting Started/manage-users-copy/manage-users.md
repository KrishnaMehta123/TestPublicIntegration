---
title: Manage Users
excerpt: Understand how you can invite and manage users on the CleverTap dashboard
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

To access the CleverTap dashboard, the user needs an invitation and an appropriate access level. The account admin can perform different operations, such as adding a new user, deleting an existing user, assigning a role to a user, editing the user's current role, and so on from the *Settings* > *Users* page.

<Image title="Users Page Navigation" alt="A dashboard image of User Settings page which gives an overview of added users and their access type" align="center" width="800px" border={true} src="https://files.readme.io/4ad9c66d5e3b370dda07c60a04d21f65404a0b1537a1734be355262577f07520-Users_Navigation.png">
  User Settings
</Image>

After the new user is added, the dashboard allows an admin to view the following information about all the users added to the project:

* Name
* Role
* Email
* User Status
* Last Login
* Passcode-Status.

## Invite Users

To invite a new user to the CleverTap dashboard:

1. Click **+ User** from the *Users* page.
2. Enter the email address and assign the role. For more information about different roles in the CleverTap dashboard, refer to [Role-Based Access Control](doc:role-based-access-control).

<Image alt="Invite Users" align="center" border={true} src="https://files.readme.io/a6364c54837b4a8886a9cd91ed670bbec7fdde0fdd81788150f3238bdca6a5f6-Invite_Users.png">
  Invite Users
</Image>

> 📘 Assign Multiple Roles to a User
>
> You can assign multiple roles to a user if needed. If you assign two system roles to the user, the role with higher precedence is assigned to the user.

> 📘 Invite Multiple Users at Once
>
> You can invite multiple users (up to 50) at once by clicking **+ User** from the *Invite User* window.

<Image title="Invite Multiple Users to Dashboard" alt="A dashboard image showing how to invite multiple users at once to the project" align="center" border={true} src="https://files.readme.io/a3d7e754fc9ea124cd7499303470731f3ee4b122d2c6923674690969d665cb4a-Bulk_User_Invite.png">
  Invite Multiple Users at Once
</Image>

3. Click **Invite** to extend invitations to the email IDs added.

## Download User List

You can download the list of all users by clicking **Download as CSV** from the *Users* page.

<Image title="Download User List" alt="A dashboard image showing the option to download user list as CSV" align="center" border={true} src="https://files.readme.io/316aa4d70b8dee9178b2750c5da9e112bfb220dad76aad65039264f2d7eabccb-Download_as_CSV.png">
  Download User List as CSV
</Image>

# Operations

The account admin can perform different user management operations from the CleverTap dashboard. Each of these operations is described briefly in the following sections:

## Revoke Access

Revoking user access implies that the user can no longer access the dashboard. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Revoke User Access* from the list.

<Image title="Revoke Access" alt="A dashboard image showing the option to Revoke User Access of a user" align="center" border={true} src="https://files.readme.io/ff67eeef82dc136192a51b15330abd0c3faca9a83408a8db520bc8c90908e6ae-Revoke_User_Access.png">
  Revoke User Access
</Image>

## Edit Role

You can also edit the role of the user in the future. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Edit Role* from the list.

<Image title="Edit a Role" alt="A dashboard image showing the option to Edit Role of a user" align="center" border={true} src="https://files.readme.io/5963e7810ba35dd527a2ebc534de18bafe97c7098db5aaf0d544d4f6ddb2e611-Edit_Role.png">
  Edit Role
</Image>

For more information about role management, refer to [Role-Based Access Control](doc:role-based-access-control).

### Bulk Action For Managing Multiple User Roles

You can assign or unassign roles for multiple users at once. To do so: 

1. Select the set of users for whom you want to assign or unassign the roles
2. Click the ![](https://files.readme.io/22ed0b8-image.png) icon.

<Image alt="Manager Multiple User Roles in Bulk" align="center" border={true} src="https://files.readme.io/087f4f6460583409f2bb3c502af0f621050b6c9bb459f35b1eece01c0741e6dd-Bulk_Action_for_Managing_Multiple_Roles.png">
  Manage Multiple User Roles in Bulk
</Image>

4. After the *Edit Roles* window opens, enter the roles you wish to assign to your users in the *Assign roles* field.    Similarly, enter the roles you wish to unassign for your users in the *Unassign roles* field. 
5. After making the required changes, click **Continue**.

<Image alt="Save Bulk Actions" align="center" border={true} src="https://files.readme.io/416bca13c62d3aff8dd86308a4fc8ddb4d749f31039404aceeec81a129da0828-Multiple_Roles_Assignment.png">
  Save Bulk Actions
</Image>

6. Review the bulk changes in user roles and click **Save**.

## Delete User

Admins can delete users from a project to ensure unauthorized users, such as former employees, can no longer access the CleverTap dashboard. This eliminates manual interventions, making user offboarding secure and seamless. Once deleted, the user loses access, and all deletions are recorded in audit logs for security and compliance. However, admins cannot delete themselves from a project; other admins can.

To delete a user:

1. Click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select **Delete User**.
2. Click **Delete** to confirm the action to permanently remove the user from the project.

<Image alt="Delete a User" align="center" border={true} src="https://files.readme.io/0de3e86a9df1cde55bbd98b4d9715fd63b9ac8e416de1a7bab9b1bdf4d3873b5-Delete_User.png">
  Delete a User
</Image>

## Reset Passcode

Reset Passcode generates a fresh new passcode for the user. Post resetting, the user must incorporate this passcode for the APIs. To reset the passcode, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Reset Passcode* from the list.

<Image title="Reset Passcode" alt="A dashboard image showing the option to Reset the Passcode of a user" align="center" border={true} src="https://files.readme.io/7ceab210ba5ce562e78dab2ce792ecfadf757b8f427b87af8acfd017f8492218-Reset_Passcode.png">
  Reset Passcode
</Image>

## Grant User Passcode

Every CleverTap API call requires a passcode to authenticate the API calls. Granting a user passcode helps authenticate the user when making API calls. To grant a passcode, click the ![Ellipsis](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Grant Passcode* from the list.

<Image title="Grant Passcode" alt="A dashboard image showing the option to Grant Passcode to a user" align="center" border={true} src="https://files.readme.io/5a749c9ba96244de87cf366e7dab3a8ffe64205f873b4e7c53b614424e040055-Grant_Passcode.png">
  Grant Passcode
</Image>

Select the tenure for which you want to grant the passcode and then click **Grant** to confirm your action.

<Image title="Grant Passcode" alt="A pop-up asking to select the Passcode Time for the user" align="center" width="80%" border={true} src="https://files.readme.io/f537e123c5519a313c110175d55e4e24211d2d5c5bf0ba9881943aa4e381bcc8-Grant_Passcode_Popup.png">
  Select Passcode Time
</Image>

For more information about API authentication in CleverTap, refer to [Authentication](https://developer.clevertap.com/docs/authentication).

# FAQ

### Q. How to recover Admin access and assign it to a new user if the original Admin account is deactivated?

A. If your organization’s sole admin account has been deactivated and you no longer have access to it, you can still recover admin access and assign new admin privileges by following these steps:

1. Contact your organization’s IT administrator or domain owner to temporarily reactivate and grant access to the email account of the Project's admin.

2. Once the account is reactivated, use the *Forgot Password* option on the CleverTap login page to reset the password for that admin user account.

3. After resetting the password, log in to the account and assign admin access to an existing user within your Project or invite a new user with Admin access. This new admin will then have access to the CleverTap dashboard for that project.

4. (Optional) [Revoke](doc:manage-users#revoke-access) the former admin's access from the dashboard project.

To prevent similar issues in the future, CleverTap recommends assigning admin roles to at least two users. This ensures that if one admin leaves or becomes unavailable, the other can still manage the project and perform necessary administrative tasks.
