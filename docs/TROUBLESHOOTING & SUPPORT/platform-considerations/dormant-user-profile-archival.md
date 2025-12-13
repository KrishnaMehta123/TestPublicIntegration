---
title: Dormant User Profile
excerpt: >-
  Understand the concepts of dormant profiles and their archival process in
  CleverTap.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

A dormant user is a user profile that was active in your app in the past but is not active anymore. The criteria for considering a profile dormant may vary based on the business platform and its use case. For example, a banking app might consider some user profiles as dormant users if they:

- Have not performed any activity for some time in the past.
- Have not received any message for some time in the past.
- Are not reachable via any messaging channel.

# Dormancy Criteria in CleverTap

The [anonymous profiles](doc:user-profiles#user-profile-types) are considered as dormant if:

- They have not performed any event in the last six months (180 days), and,
- They are not reachable across any channel, such as Email, Phone, Push, etc.

# Archive Dormant User Profiles

The CleverTap system runs the dormant profile archival process every 15 days and continuously monitors user activities based on the archival criteria. After a profile is identified as dormant, the system archives it.

## Key Benefits

The following are the key benefits of archiving dormant user profiles:

- **Improved Data Quality:** Ensures that your data integrity is maintained and relevant to your business requirements.
- **Enhanced Data Analysis:** Provides precise analytics and reachable user base details. This empowers you to make informed and business-critical decisions based on accurate real-time data.
- **Streamlined Active User Base:** Declutters your active user base and ensures that your engagement efforts are focused on the most relevant and actively participating users.
- **System Performance Optimization:** Archiving enhances system performance by decluttering the user base. This optimization allows for smoother operations and improved response times.