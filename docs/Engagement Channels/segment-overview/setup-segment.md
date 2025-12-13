---
title: Setup
excerpt: >-
  Understand how to set up Segment for sending event data to the Segment
  dashboard
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To export event data to the [segment.io](https://segment.io/) dashboard via the _Campaigns_ page, we need to connect the segment.io account to the CleverTap dashboard. To do so:

1. Log in to your CleverTap account.
2. Navigate to _Settings_ > _Partners_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/deb5cd8-Navigate_to_Partners_page.png",
        "Navigate to Partners Page",
        2854
      ],
      "align": "center",
      "border": true,
      "caption": "View Segment on Partners Page"
    }
  ]
}
[/block]



3. Hover on the _Segment_ icon and click **Integrate**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c775761-Click_Integrate.png",
        "Click Integrate in Partner List Tab",
        2396
      ],
      "align": "center",
      "border": true,
      "caption": "Click Integrate in Partner List Tab"
    }
  ]
}
[/block]



On clicking, _Integrate raw data partner - Segment_ popup opens on the right side of the screen.

4. Enter the following details and click **Integrate**:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Partner Nickname",
    "0-1": "Enter the nickname for the partnership.",
    "1-0": "Write Key",
    "1-1": "A unique identifier for each source. It helps Segment identify which source is sending the data and which destinations should receive that data.  \nFor more information, refer to [Locate your Write Key](https://segment.com/docs/connections/find-writekey/)."
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "left",
    "left"
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8dc099d-Integrate_raw_data_partner_-_Segment.png",
        "Configure Segment Details",
        2402
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Segment Details"
    }
  ]
}
[/block]



After the integration is successful, the _Integrated_ tag displays against Segment on the _Partner List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbc5d0f-Integrated_tag.png",
        "View Integrated Tag",
        2396
      ],
      "align": "center",
      "border": true,
      "caption": "View Integrated Tag"
    }
  ]
}
[/block]