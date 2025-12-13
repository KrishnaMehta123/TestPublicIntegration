---
title: Zapier
excerpt: Workflow Automation
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

[Zapier](https://zapier.com/), a workflow automation platform, automates repetitive work by connecting the applications with zero coding. The following are some of the scenarios where Zapier can prove to be a very useful platform:

- Add responses from the survey conducted to the CleverTap dashboard
- Update user profile information on the CleverTap dashboard

Zapier allows you to transfer information collected in one app (the trigger) to another application (the action). Such a trigger/action combo is called a **Zap**. With this integration, you can create Zaps to do the following:

- [Create/Update user information](doc:zapier#createupdate-user-information)
- [Upload event](doc:zapier#upload-event)

# Prerequisites for Integration

The following are the prerequisites for CleverTap-Zapier integration:

- A CleverTap Account Passcode
- An active Zapier account to create the CleverTap app

# Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

# Create/Update User Information

To create/update the user information:

1. Log in to the [Zapier dashboard](https://zapier.com/app/dashboard) and click **+ Create Zap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ddbe272-Create_a_Zap.png",
        "Create a Zap on Zapier Dashboard",
        2852
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create a Zap on Zapier Dashboard"
    }
  ]
}
[/block]

Zapier can connect different applications. We will use Google Sheets for this example.

2. **Set up a Trigger**. For this example, perform the following steps:

    a. Select _Google Sheets_ from the _App event_ section. This starts the Zap when a trigger event takes place in Google Sheets.  
    b. Select _Event_ from the dropdown list. We will select _New Spreadsheet Row_ for this example and click **Continue**.  
    d. Select the _Google Sheets account_ from the dropdown list. You can also connect a new account if your account does not appear in the dropdown.  
   e. Click **Continue**.  
   f. Set up a trigger event. For this example, select the Google sheet for which you want to set up an event. Also, select the _Worksheet_ from the Google sheet for which you want to set up a trigger and click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/04e1117-Set_up_Trigger_-_CreateUpdate_User.gif",
        "Set up a trigger for Create/Update User zap",
        1262
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly. 
4. Click **Continue**.
5. **Select the _Action_  that the zap must perform after the trigger event occurs.** For this example, perform the following steps:

   a. Select _CleverTap_ from the _App event_ dropdown.  
   b. Select _Create/Update User Profile_ from the _Event_ dropdown. This implies that whenever a new row is added to the selected google sheet, a new user profile is created, or an existing user profile is updated with the new information.  
   c. Click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9aea22b-Set_up_Action_-_Create_User.gif",
        "Set up Action for Create/Update User zap",
        1262
      ],
      "align": "center",
      "border": true,
      "caption": "Select Action for Zap"
    }
  ]
}
[/block]

  d. Click **Choose account** and then click **+ Connect a new account**. _Connect an account | Zapier_ window opens. Enter all the required details for connecting the CleverTap account. Enter the same passcode that you obtained in the [Create a Passcode on CleverTap Dashboard](doc:zapier#create-a-passcode-on-clevertap-dashboard) step.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e10990-Connect_CleverTap_account.gif",
        "Select the account to connect CleverTap Account",
        1280
      ],
      "align": "center",
      "border": true,
      "caption": "Select Account to Connect the Account"
    }
  ]
}
[/block]

  e.  Click **Continue** after successfully connecting your account.  
  f. Set up an action as shown in the following figure and click **Continue**:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/10679ae-Set_up_Action_-_CreateUpdate_User.gif",
        "Set up an action for Create/Update User zap",
        1280
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up an Action"
    }
  ]
}
[/block]

6. Click **Test action** to test the zap.
7. Click **Publish Zap**.

After publishing this zap, a new user is created, or an existing user is updated on the CleverTap dashboard every time a trigger occurs. CleverTap uses the _Identity_ field to identify if it is a new user or an existing user.

# Upload Event

To upload an event:

1. Log in to the [Zapier dashboard](https://zapier.com/app/dashboard) and click **+ Create Zap**. Zapier can connect different applications. We will use Google Sheets for this example.
2. **Set up a Trigger**. For this example, perform the following steps:

    a. Select _Google Sheets_ from the _App event_ section. This starts the Zap when a trigger event takes place in Google Sheets.  
    b. Select _Event_ from the dropdown list. We will select _New Spreadsheet Row_ for this example.  
    c. Click **Continue**.  
    d. Select the _Google Sheets account_ from the dropdown list. You can also connect a new account if your account does not appear in the dropdown.  
    e. Click **Continue**.  
    f. Set up a trigger event. For this example, select the google sheet for which you want to set up an event. Also, select the _Worksheet_ from the google sheet for which you want to set up a trigger and  click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b59b2be-Setup_Trigger_-_Upload_Event_1.gif",
        "Set up trigger event for Upload Event zap",
        1254
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]

3. Click **Test Trigger**. This ensures that the right account is connected and the trigger is set up correctly. 
4. Click **Continue**.
5. **Select the _Action_  that the zap must perform after the trigger event occurs.** For this example, perform the following steps:

   a. Select _CleverTap_ from the _App event_ dropdown.  
   b. Select _Upload Event_ from the _Event_ dropdown. This implies that whenever a new row is added to the selected google sheet, a new user profile is created, or an existing user profile is updated with the new information.  
   c. Click **Continue**.  
   d. Click **Choose account** and then click **+ Connect a new account**. _Connect an account | Zapier_ window opens. Enter all the required details for connecting the CleverTap account. You can obtain this information by navigating to _Settings_ > _Project_ from the CleverTap dashboard. For more information about connecting the CleverTap account with Zapier, refer to the figure under _Step 5d_ of [Create/Update User Information](doc:zapier#createupdate-user-information).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db0607e-Set_up_Action_-_Upload_Events.gif",
        "Select account to connect CleverTap account",
        1230
      ],
      "align": "center",
      "border": true,
      "caption": "Select Account to Connect"
    }
  ]
}
[/block]

   e.  Click **Continue** after successfully connecting your account.  
   f. Set up an action as shown in the following figure and click **Continue**:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a09529-Set_up_Action_-_Upload_Event_Part_2.gif",
        "Set up an action for Upload Events zap",
        1280
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up an Action"
    }
  ]
}
[/block]

6. Click **Test action** to test the zap.
7. Click **Publish Zap**.

After publishing this zap, an event is uploaded to the CleverTap dashboard every time a trigger occurs. CleverTap uses the _Identity_ field to identify if it is a new user or an existing user.

# Supported Date-Time Formats

Supported date-time formats include:

- **UNIX Epoch**: Tracks time as a running total of seconds. For example, **1521611063**.
- **ISO 8601**: It is in the format **YYYY-MM-DDTHH:mm:ss. sssZ**. For example, 2018-03-05T15:16:0Z.
- **Short Date**: It is in the format **YYYY-MM-DD HH:mm:ss**. For example, 2018-03-5 15:16:0.
- **Long Date**: It is in the format **dddd, MMMM dd, yyyy HH:mm:ss**. For example, March 05, 2018 15:16:0.

> 📘 UTC/GMT Date-Time Format
> 
> The timezone of the timestamp must be in UTC/GMT format. It can be obtained by adding Z at the end of the timestamp string. This is done so that the correct timezone (adjusted as per the local region) displays on the dashboard.