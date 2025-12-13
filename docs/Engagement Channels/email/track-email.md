---
title: Track Email
excerpt: Learn how to track your email clients and user agents.
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

CleverTap allows you to track emails and analyze data such as links and open rates of emails. You can boost your user engagement by tracking your emails.

# Track Client Names

Get insights for your email campaign such as the _Client name (\_such as Gmail) and \_User Agent_ (such as Mozilla Firefox). If some clients cannot be identified, they are saved as _Unidentified_ clients. 

## Analyze Client Names

You can analyze the client names to check the efficiency of your campaign and if the message is received correctly by the target audience. 

Clients are tracked with the Notification Viewed event. You can use the event properties _Client Name_ and \_User Agent \_to analyze your campaign.  
Follow the steps to analyze the client information:

1. Click Analytics > Events from the dashboard.
2. Select the event _Notification Viewed_.
3. Filter by the _Campaign Type_ as _Email_ event property. 
4. Click View Details. 
5. Click the Trend & Properties tab to view the event trend.
6. Scroll down to \_Event property \_section.  
7. Select the _Client Name _ property from the list to view the clients. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/43d4f02-Email_client_name_property.png",
        "Analyze Client Name Event Property",
        1160
      ],
      "align": "center",
      "caption": "Analyze Client Name Event Property"
    }
  ]
}
[/block]

8. Select the event _User Agent_ to view the client by the user agent.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6d35e3f-Email_user_agent_property.png",
        "Analyze User Agent Event Property",
        1165
      ],
      "align": "center",
      "border": true,
      "caption": "Analyze User Agent Event Property"
    }
  ]
}
[/block]

9. Toggle between the views by clicking the ![event property view](https://files.readme.io/2d94b48-Analytics_Event_Property_view_toolbar.png) toolbar.
10. Scroll down to see a Frequency histogram.