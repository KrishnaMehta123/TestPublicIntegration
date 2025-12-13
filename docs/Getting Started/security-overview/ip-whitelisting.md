---
title: IP Whitelisting
excerpt: >-
  Understand how to leverage the IP Whitelisting feature to restrict dashboard
  access.
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

CleverTap's *IP Whitelisting* feature makes the IP restriction process more intuitive and self-serve for the customers.

The CleverTap dashboard showcases business-sensitive information such as revenue, application installs, conversions, etc. Therefore, organizations might need to restrict dashboard access to certain administrative users after integrating CleverTap SDK for different business reasons.

## Whitelist IP Addresses

To whitelist an IP address, the admin needs to perform the following steps:

1. Navigate to *Settings* > *Security* > *IP Whitelisting* . Ensure that the *Use IP whitelisting to restrict access* toggle is turned on.
2. From the *IP Whitelisting* page, click **+IP Address** to add a new IP address.

> 🚧 IP Whitelisting Toggle
>
> Only admins can turn on/off the *Use IP whitelisting to restrict access* toggle on the IP whitelisting page.

<Image title="Ip whitelisting dashboard" alt="Click +IP Address to add addresses to Whitelist" align="center" border={true} src="https://files.readme.io/299f6ad-Ip_whitelisting_dashboard.png">
  IP Whitelisting
</Image>

3. Enter the IP address you wish to whitelist in the *IP Address* field. CleverTap supports both IPV4 and IPV6 addresses.

   You can add up to 20 IP addresses at once. If you are adding multiple IP addresses, use commas to separate them. After you enter all the IPs, click *Whitelist IP Address*.

<Image title="Whitelist IP addresses" alt="Add the IP addresses to Whitelist" align="center" width="80%" border={true} src="https://files.readme.io/65f6cea-Whitelist_IP_addresses.png">
  Whitelist IP Address View
</Image>

> 📘 Note
>
> If you are whitelisting IPs for the first time, you need to ensure that you whitelist your own IP, as it avoids locking your own account.

## Remove Whitelisted IP Addresses

To remove a particular IP address:

1. Click the ![Delete icon](https://files.readme.io/27fabff-delete_icon.png)icon adjacent to the particular IP from the *IP Whitelisting* page. 
2. Click **Remove**. 

To delete multiple IP addresses together, select all the IP addresses from the whitelisted list and click the delete ![Delete icon](https://files.readme.io/27fabff-delete_icon.png) icon, as highlighted below:

<Image title="Delete multiple IP addresses." alt="Select multiple IPs you want to delete from the list of IPs" align="center" border={true} src="https://files.readme.io/e07d32f-Delete_multiple_IP_addresses.png">
  Delete Multiple IP Addresses
</Image>

> 📘 Note
>
> Turn off the *Use IP whitelisting to restrict access* toggle button to pause the IP whitelisting configuration.
