---
title: Assigning Identities - WIP <@saby to review the whole pageeee>
excerpt: Understand how CleverTap assigns identities to users.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
When a user lands on a web page,  CleverTap creates a [user profile](https://docs.clevertap.com/docs/user-profiles) with a CleverTap ID for the user. After the CleverTap ID is assigned, other identities can be added per your implementation to identify unique users. CleverTap supports [multiple types of identifiers](https://docs.clevertap.com/docs/identity-management-overview#types-of-identifiers) to uniquely identify a user profile. Let us explore various scenarios for identifying unique users.

## Anonymous Users

Anonymous users do not have any other identity apart from the CleverTap ID on their profiles. Following are some scenarios of how different Device IDs, User IDs, and CleverTap IDs are mapped:

| Device        | CleverTap ID | User ID |
| :------------ | :----------- | :------ |
| iPhone        | 1            | null    |
| Desktop       | 2            | null    |
| Desktop       | 2            | null    |
| Android phone | 3            | null    |
| iPhone        | 1            | null    |
| Android phone | 3            | null    |

There are three unique users in this table.

Here, the first event was performed on _iPhone_. Because there was no previous record of this device, CleverTap assigned it a new CleverTap ID of 1.

The second event came from _Desktop_. Because there was no previous record of this device,  CleverTap assigned it a new CleverTap ID of 2.

The third event also came from _Desktop_, and because CleverTap already had a record of this device, it was assigned a CleverTap ID of 2. Similarly, an _Android phone_ is assigned a CleverTap ID of 3.  

## Identified User After Anonymous Log In

CleverTap assigns all the events performed on a device previously by anonymous users to the identified user. 

| Device | CleverTap ID | User ID                                  |
| :----- | :----------- | :--------------------------------------- |
| iPhone | 4            | null                                     |
| iPhone | 4            | null                                     |
| iPhone | 4            | [smith@email.com](mailto:jane@email.com) |

The first two events are logged anonymously on the device and are assigned to the profile with CleverTap ID 4. 

After a user logs in, this profile with the CleverTap ID 4 is updated with the User ID [smith@email.com.](mailto:jane@email.com.) The user Mr. Smith is now an identified user.  All future events on this device will be mapped to our identified user, Mr. Smith, with the user ID  [smith@email.com.](mailto:jane@email.com.) 

<br />

## Common User ID on Multiple Devices

| Devices     | CleverTap ID | User ID                                   |
| :---------- | :----------- | :---------------------------------------- |
| iPhone      | 8            | [smith@email.com](mailto:smith@email.com) |
| iPad        | 9            | null                                      |
| iPad+iPhone | 8+9          | [smith@email.com](mailto:smith@email.com) |

A user installs the app on the iPhone. Clevertap creates a CleverTap profile and assigns a CleverTap ID of 8. The User ID is null. After the user logs in, a CleverTap ID is assigned to the user. For example, [smith@email.com.](mailto:smith@email.com.) This profile is now identified.  

Assume a scenario where Mr. Smith installs the app on an iPad. Again, Clevertap creates a CleverTap profile and assigns a CleverTap ID of 9. The User ID is null. This is a new user profile. After Mr. Smith logs in to the iPad with his email ID [smith@email.com.](mailto:smith@email.com.), CleverTap determines that this is the same identified user, that is, CleverTap ID 8 Both the profiles are now merged. The user profile will have one User ID, that is, [smith@email.com](mailto:smith@email.com), and two CleverTap IDs, 8 and 9.

## Multiple Users on the Same Device

When multiple users log in to the same device, CleverTap creates separate CleverTap IDs for these users. Let us understand it.

| Device | CleverTap ID | User ID                                  |
| :----- | :----------- | :--------------------------------------- |
| iPad   | 6            | [bob@email.com](mailto:bob@email.com)    |
| iPad   | 6            | null                                     |
| iPad   | 7            | [smith@email.com](mailto:adam@email.com) |

Bob and Mr. Smith are friends using the same iPad. For CleverTap, these are two unique users. 

Bob performed the first event on the device, and CleverTap assigned him a CleverTap ID of 6, then Bob logged out from the device. Somebody performed another event anonymously from the same device. We don't know if it was Bob, Mr. Smith, or someone else.  However, the event would be assigned to Bob because he was the last known user.

Now, Mr. Smith logs into the device and performs an event. As soon as Mr. Smith logs in, the [OnUserLogin](https://developer.clevertap.com/docs/user-profiles-ios#create-a-user-profile-when-user-logs-in-on-user-login-method) method in CleverTap SDK checks if any pre-existing ID is associated with Mr. Smith. If there is already a pre-existing identity present for Mr. Smith, then he is assigned the ID, that is, 7. 

Now, Mr. Smith logs out. There are two more events performed on the iPad anonymously. Because Mr.Smith was the last identified user on the device, these events are attributed to Mr. Smith.