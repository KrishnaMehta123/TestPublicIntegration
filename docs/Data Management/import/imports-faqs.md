---
title: 'Imports: FAQs'
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
This document answers common questions about importing user data into CleverTap through APIs or SFTP, covering sequencing, data preparation, and best practices to ensure data integrity during historical imports.

### What is Historical Data Import in CleverTap?

Historical Data Import allows you to bring user profiles and past events from older systems into CleverTap using the [Upload User Profiles API](doc:upload-user-profiles), [Upload Events API](doc:upload-events), or [SFTP Import](doc:sftp-import).

### Can I import historical data for both profiles and events using SFTP?

Yes. SFTP Import supports uploading, User Profile files, and Event files. Refer to [SFTP Import](doc:sftp-import).

### Do I need to upload user profiles before events?

Yes. CleverTap requires that user profiles be uploaded first, followed by historical events.  
This ensures correct identity stitching during ingestion. Refer to, [Upload User Profiles](doc:upload-user-profiles)

### What information should be included in user profile uploads?

User profile uploads should include: Name, Age, Email ID, Phone number, Custom tags, Additional profile attributes

You can upload these using:

- [Upload User Profiles API](doc:upload-user-profiles)
- [SFTP Import](doc:sftp-import-profiles)

### How should I upload historical events?

Once profiles are uploaded, you can send historical events—such as purchases or lifecycle actions—using:

- [Upload Events API](doc:upload-events)
- [Events SFTP Import](doc:sftp-import-events)

### In what order should I upload historical event data?

Always upload events **chronologically**, beginning with the **oldest data first** and progressing to the most recent.  
This ensures proper sequencing and accurate behavioral timelines. Learn more: [Upload User Events](doc:upload-events)

### Can I test historical uploads before sending them to Production?

Yes. CleverTap recommends testing with a **sample dataset** in your **Test Account** first.  
Your Test Account can be reset, while Production cannot delete or modify imported data. Refer to [Test Account Guidelines](doc:accounts-and-environments)

### How does CleverTap handle timestamps on historical events?

Events that contain timestamps will appear in the CleverTap Dashboard based on the provided event time.  
Import eligibility depends on your account’s **Data Retention Policy (DRP)**. Refer to [Data Retention Policy](doc:data-retention)