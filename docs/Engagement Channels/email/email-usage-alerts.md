---
title: Email Usage Alerts
excerpt: >-
  Track email add-on usage, monitor overages, and analyze organization-level
  trends.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

The Email Usage Alerts feature gives you complete visibility into your organization’s email add-on consumption. It helps you stay on top of your plan limits, understand usage patterns, and proactively manage overages.

With intuitive visualizations and detailed usage tables, you can:

- View your current plan and how much of it you’ve consumed
- Track email volume requests and IP allocations across all projects
- Monitor daily and monthly usage trends across all projects combined
- Access overage summaries and take action before limits are exceeded
- Download CSV reports for billing, audits, or offline analysis

# Access Add-On Details

The following two sections on the CleverTap dashboard display email add-on limits and usage aggregated across organization projects:

- From _Organisation_ > _Projects_

  [block:image]{"images":[{"image":["https://files.readme.io/3f110179d19b526697bb1045731e3a6fc9fe0de37790a2a967730ba85ce36b3a-Email_Add-On_Usage_Information_from_Projects_Section_-_Advanced_Add-On.png","","Email Add-On Usage Information from Projects Section "],"align":"center","border":true,"caption":"Email Add-On Usage Information from Projects Section "}]}[/block]
- From _Billing_ > _My Plan_

  [block:image]{"images":[{"image":["https://files.readme.io/92ed8063f59c07154a614a9fc37b188efcc9ae94fed795c8425dc29a5d2ed5f9-Email_Add-On_Usage_Information_from_My_Plans_Section_-_Advanced_Add-On.png","","Email Add-On Usage Information from My Plans Section"],"align":"center","border":true,"caption":"Email Add-On Usage Information from My Plans Section"}]}[/block]

  <br />

# Billing Calculations & Usage

This section provides a real-time summary of your email consumption for the selected month. The **Billing calculations** section shows how your email add-on usage is measured against your subscribed limits. It outlines the following information:

- Plan Limit: The maximum allowable email usage and IP allocations, based on your subscribed plan
- Actual Usage: Email messages sent by CleverTap to the configured email service providers (such as SendGrid or Infobip) during the selected time period.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d2e1ec03cf6a85bcd643473df05d05ac93e58fd8036cfa4c8348b9662a69ec0-image.png",
        null,
        "Monthly Billing Calculations and Usage "
      ],
      "align": "center",
      "border": true,
      "caption": "Monthly Billing Calculations and Usage "
    }
  ]
}
[/block]


When your email usage exceeds the limit defined in your add-on plan, the additional volume is considered overage and charged accordingly. For example, 

| **Item**       | **Email Requests** | **IPs** |
| -------------- | ------------------ | ------- |
| **Plan Limit** | 10,000,000         | 2       |
| **Usage**      | 12,000,000         | 2       |
| **Overage**    | 2,000,000          | –       |

# Email Usage Trend

This section provides daily or monthly usage trends based on the selected _Usage_ cycle, helping you analyze consumption patterns and monitor usage effectively.

The _Email Usage Trend_ chart plots daily email sent counts across all organization projects combined. You need to hover over data points to view exact values. The tabular view, just below the usage trend, displays a breakdown of daily volumes across all your projects combined. You can also download it as CSV for offline analysis or internal reporting. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db0aeeefc5ccad94df2be36b8b6993c461063bfb4fdfc184aca75384b0a76702-Email_Usage_Trend.png",
        "",
        "Email Usage Trend"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Daily Email Usage Trend"
    }
  ]
}
[/block]


The _IPs Usage Trend_ chart shows the number of IPs assigned to your organization during the selected _Usage_ cycle, displayed daily or monthly, depending on the time range.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8670c7285394bf480b58c04a3296e271a8209e5f35302f8e0d4f94c414ce2a27-image.png",
        null,
        "Daily IPs Usage Trend "
      ],
      "align": "center",
      "border": true,
      "caption": "Daily IPs Usage Trend "
    }
  ]
}
[/block]


# Usage Alerts via Email

CleverTap automatically sends threshold-based alert emails when your email add-on consumption crosses 70%, 90%, or 100% of your plan limit. These alerts are triggered at the organization level and are sent to the designated billing contacts, who are added as primary and secondary billing contacts. You can access this information from the Billing > Billing details section of the dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dce26d34c24d5b1b7d840246ee5992fa7164ee19b11c17fd75bf766ac1cb1f3e-BIlling_Contacts.png",
        null,
        "Access Billing Contacts"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Access Billing Contacts"
    }
  ]
}
[/block]


Each email includes a clear usage warning with the percentage of consumption (for example, "You’ve used over 90% of your email add-on limit"), the exact number of emails used vs. your plan limit, and a reminder that overage charges will apply if the limit is exceeded within the billing cycle (refer to the following image). Usage alerts emails are sent when the usage exceeds 70%, 90%, and 100%. A link to Contact Sales is also provided in case you need to upgrade your limit.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbf6ad1312060b087151ea46ab43095e0d2e7656058481ae4557b87c93716ae7-Email_Notificaton_for_Usage.png",
        "",
        "Email Warning"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Email Warning"
    }
  ]
}
[/block]


You can also see a nag bar notification displayed at the top of the dashboard when your usage crosses key thresholds.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ce9b14abd6c5ba5b61ca152e6880afc1443a2022994cf8b379cd528a91a75057-Nagbar_Notification_on_the_Dashboard.png",
        "",
        "Nagbar Warning on Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Nagbar Warning on Dashboard"
    }
  ]
}
[/block]


# Historical Trend

The _Historical Trend_ tab offers a flexible view of your past email add-on usage, allowing you to analyze trends across any custom date range. You can use this tab to:

- Understand long-term email volume patterns
- Analyze usage across custom date ranges using the calendar filter
- Export historical usage data to support audits, reviews, or custom reporting needs outside standard billing cycles.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6889f68e8dc0c3e79d6e3b755c359ef4dafa7a7e439dd634c943216e75999faf-Historical_Trend_-_Usage_Alert.png",
        "",
        "Historical Trend"
      ],
      "align": "center",
      "border": true,
      "caption": "Historical Trend"
    }
  ]
}
[/block]