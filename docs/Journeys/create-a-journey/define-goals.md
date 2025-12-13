---
title: Define Goals
excerpt: Understand how to define journey goals on the canvas.
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

By defining a goal, you can decide when a user can exit the Journey path. It helps you to compare a Journey’s effectiveness against a Control Group. For example, your goal could be to increase user registrations on your platform or want existing users to use your platform more frequently.

To define a goal, you can drag and drop any segment from the left-hand side palette and add it as a goal for your Journey. A Journey can support up to **three** goals, and a user exits from the journey upon completing any of the goals.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d824ddb-Define_a_Journey_Goal.gif",
        "Drag and drop a segment to define a goal for Journey",
        1208
      ],
      "align": "center",
      "border": true,
      "caption": "Define a Journey Goal"
    }
  ]
}
[/block]


## Types of Goals

- Action-based goals: In this goal, users will exit your Journey as soon as they perform a goal, in real-time. For example, exit people as soon as they perform the _Charged_ event, where _item_ is _Red Nike Shoes_.
- Past behavior goals: Past behavior goals, like segments, are evaluated once every twenty-four hours, at 12:00 am. Once the goal is evaluated, users who meet this goal will not be a part of the Journey from that day onward. For example, exit people if they have spent at least $300 in the past week.