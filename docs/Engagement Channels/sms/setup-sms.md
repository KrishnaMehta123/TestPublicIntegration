---
title: Setup
excerpt: Understand how to set up SMS as a channel for your marketing campaigns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Add a New Provider

To add a new SMS provider, perform the following steps:

1. From the dashboard, navigate to *Settings* > *Channels* > *SMS*.
2. Click **Add Provider**.

<Image title="Click +Add Provider to Add an SMS Provider" alt={1074} align="center" border={true} src="https://files.readme.io/ea1f1a5-1_Add_Provider_dashbboard.png">
  Add Provider
</Image>

3. Enter all the required information.
4. Click **Save**. 

Once the phone number is validated by the SMS service provider, you can send a test SMS to test the integration before you start creating SMS campaigns and journeys.

<Image title="Enter SMS Provider Details and Click Save" alt={1088} align="center" border={true} src="https://files.readme.io/30118cb-sms_provider.png">
  Provider Details
</Image>

To learn more about integrating specific SMS service providers with CleverTap, refer to this [document](https://docs.clevertap.com/docs/sms-partners). 

# Edit Provider Details

To edit a *Provider*, perform the following steps:

1. Click the ellipsis next to the required provider from the *Providers* tab. 
2. Click **Edit settings** to update the provider details. 

You can also mark a provider as default by selecting *Mark as Default* option available in the ellipsis next to a particular provider.

# Add a Provider Group

The failure of an SMS provider may affect your SMS campaigns, so it is always better to have another SMS provider. By grouping providers, you can provide your users with a seamless experience.

You can assign a preferred provider to send a message. A provider group is used based on its assigned priority for each message. If provider 1 is unavailable, then we attempt the message with provider 2, and so on. In the end, this ensures higher message deliverability for your campaigns.

> 📘 Provider Group Maximum
>
> Each provider group can have a maximum of 10 providers.

To create a provider group, perform the following steps:

1. From the dashboard, navigate to *Settings* > *SMS* > *Provider Groups* tab. 
2. Click **+Provider Group**.

<Image title="Click +Provider Group to Create a Provider Group" alt={1064} align="center" border={true} src="https://files.readme.io/a9f0479-3_Provider_Group_dashboard.png">
  Provider Group
</Image>

3. Enter a *Group Name*.
4. Select the providers by priority.
5. Click **Save Provider Group**.

<Image title="Click Save Provider Group to Save" alt={576} align="center" border={true} src="https://files.readme.io/663186b-SMS_provider_group_create.png">
  Create Provider Group
</Image>

## Edit a Provider Group

To edit a provider group, perform the following steps:

1. Click the ellipsis next to the required provider from the *Provider Groups* tab. 
2. Click **Edit settings** to add or remove providers or change the priority for any providers. 

You can also mark a provider group as default by selecting the *Mark as Default* option available in the ellipsis next to a particular provider group.

<Image title="Click Edit Settings to Edit a Provider Group" alt={1062} align="center" border={true} src="https://files.readme.io/72b25cf-4_Edit_Provider_Group.png">
  Edit Provider Group
</Image>
