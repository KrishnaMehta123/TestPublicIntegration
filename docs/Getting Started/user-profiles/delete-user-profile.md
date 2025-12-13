---
title: Delete User Profile
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

This section covers how an admin can delete a user profile.

> ❗️ Permanent Deletion
> 
> Once an admin deletes a profile, the profile is permanently deleted and cannot be retrieved.

# Delete a User Profile

To delete a user profile, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Find People_.
2. Click on the appropriate profile once you have identified it.
3. Click **Delete Profile**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8d9fbf-1_Delete_Profile.png",
        "Click Delete Profile",
        1415
      ],
      "align": "center",
      "border": true,
      "caption": "Delete Profile"
    }
  ]
}
[/block]

4. On the window popup, select the checkbox to agree to delete profile data.
5. Click **Delete**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/462245d-2_Confirm_Delete_Profile.png",
        "Click Cancel or Delete Button",
        412
      ],
      "align": "center",
      "border": true,
      "caption": "Confirm Delete Profile"
    }
  ]
}
[/block]

## Deletion Timeline

Once a profile is marked for deletion, the actual deletion happens in the next 48 hours. Every day from 2 AM to 4 AM (local time), our system fetches the profiles which are marked for deletion, then deletes them in batches.

> 📘 Note
> 
> For each user profile deleted, the events will be saved with CleverTap as per the data retention policy

> 📘 Bulk Delete Profiles
> 
> You can bulk delete profiles using the API. For more information, refer to the [delete user profile API](https://developer.clevertap.com/docs/delete-user-profile-api).