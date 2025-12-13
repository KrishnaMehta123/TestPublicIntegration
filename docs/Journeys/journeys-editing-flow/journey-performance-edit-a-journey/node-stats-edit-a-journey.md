---
title: Node Stats
excerpt: >-
  Track user flow across journey nodes with version-specific stats to evaluate
  performance, drop-offs, and conversion impact
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

The *Node Stats* tab helps you track users' progress through each step of a journey. For every node on the canvas, you can view performance metrics such as the number of users who entered, where they dropped off, or whether they completed a goal.

Each node is labeled with a unique ID visible on the top-right corner of the node block. This makes it easier to reference and interpret stats in context.

You can select a specific date range from the calendar and view granular stats for each node type – Entry, Segment, Engage, or Force Exit.

If your journey has multiple versions, use the version dropdown on the Node Stats tab to analyze each version independently. The stats shown reflect only those users who entered and moved through the selected version's structure, logic, and timing. This ensures the insights remain accurate, especially when versions differ in entry criteria, delays, goals, or node sequences. Viewing stats version-wise, you can meaningfully compare user movement, drop-offs, and conversion outcomes for each version.

<Image alt="Node Stats" align="center" border={true} src="https://files.readme.io/6bd4e622a763638d65f35c1f7e167061aa82fad8da3fc8d62ef74f5a5ffe5797-Node_Stats.png">
  Node Stats
</Image>

# Entry Node

The *Entry* node is the starting point of every journey and defines which users are eligible to enter. Each journey version can have only one Entry node, which must always be a Segment node.

Entry criteria, such as segment conditions or trigger logic, may differ depending on the version, resulting in different sets of qualified users across versions.

When analyzing the Node Stats, the Entry node provides insight into the number of users who met the entry criteria, the number who actually entered, and the number who were included in the control group. These stats also help compare the effectiveness of entry criteria across versions and identify if changes in qualification logic impacted journey inflow.

<Image alt="Entry Node" align="center" border={true} src="https://files.readme.io/53a486bcfdb0d168359b16576f77015010e37eff2d252b2d9c8a9ccbb45dedb6-image.png">
  Entry Node Stats
</Image>

| Metric          | Description                                                                                                                                                                                      |
| :-------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qualified       | The total number of users who qualified for the journey based on entry conditions. This is shown only on the Entry node and may vary by version..                                                |
| Entered Journey | The number of users who entered the journey flow after qualifying. These users progress through node connectors, such as Yes or No.                                                              |
| Control Group   | The number of users randomly held back as part of a control group. These users do not receive journey campaigns, which allow you to measure uplift by comparing them against the treated cohort. |

# Segment Node

The *Segment* node evaluates users based on behavioral or profile conditions. It acts as a decision point that branches the journey based on whether users match defined segment criteria. Segment nodes can be used at any point in the journey, including as the entry node.

In the case of multiple journey versions, the Node Stats tab reflects segment-level performance only for the currently selected version. Segment definitions may evolve across versions, affecting the number of users who qualify at that node or proceed forward. This allows you to assess how changes in segmentation (for example, segment criteria or order in the flow) impact the user movement, conversion, and drop-offs.

<Image title="Segment node for Journeys" alt={316} align="center" border={true} src="https://files.readme.io/5a1ed63-Journeys_node_Segment.png">
  Segment node
</Image>

<Table>
  <thead>
    <tr>
      <th>
        Metric
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Entered Node
      </td>

      <td>
        The total number of users who entered the node. It includes all users from Moved Forward, Waiting, Goal Met, and Journey Timeout.
      </td>
    </tr>

    <tr>
      <td>
        Moved forward
      </td>

      <td>
        Users who have progressed via node connectors, such as Yes, No, or Node Timeout.
      </td>
    </tr>

    <tr>
      <td>
        Waiting users
      </td>

      <td>
        The users waiting at a node to qualify. The users may wait for either of two reasons: <ul><li>Delay from a previous node</li><li>Waiting to perform an action</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Goal Met
      </td>

      <td>
        These users have performed the intended goal, such as viewing a movie or purchasing a product. <ul><li>**Before Node**: Indicates that the user achieved the goal while waiting on the delay path but did not get a message from the next node.</li><li><em>At Node</em>: If the *Failed* connector is not connected, users who do not qualify for any path from the node are retained in the **At Node** state, as the next step is not defined for them.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Journey timeout exits
      </td>

      <td>
        These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.
      </td>
    </tr>
  </tbody>
</Table>

# Engagement Node

The *Engage* node represents the campaign delivery points within a journey, where users receive messages via channels such as Push, SMS, Email, or WhatsApp. These nodes are critical for driving user actions, and the stats captured here help you assess how effectively your messages are reaching and engaging users.

In the case of multiple journey versions, the Engage nodes may vary in their content, timing, or conditions across versions.

<Image title="Engage nodes for Journeys" alt={315} align="center" width="35% " border={true} src="https://files.readme.io/57fac94bf291066f54f862a5ac04c659ef9825711032e9cd8d033c8ddb5b637c-Push_Node_Stats.png">
  Engage Node
</Image>

<Table>
  <thead>
    <tr>
      <th>
        Stat
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Entered Node**
      </td>

      <td>
        The total number of users who entered the node. It includes the sum of all the users from Moved Forward, Waiting Users, Goal Met, and Journey Timeout.
      </td>
    </tr>

    <tr>
      <td>
        **Moved Forward**
      </td>

      <td>
        Users who moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable. **Unreachable** refers to profiles that lack identity (for example, email, phone, or device token is unavailable).
      </td>
    </tr>

    <tr>
      <td>
        **Waiting Users**
      </td>

      <td>
        Users who are delayed in progressing. Two possible reasons: <ul><li>**Before Node**: Delay from a previous node or users marked as Unreachable (if Unreachable path is not connected).</li><li>**At Node**: Users at this node without a defined outcome. For example, if  the *Failed* connector is not connected, users who do not qualify for any path from the node are retained in the **At Node** state, as the next step is not defined for them..</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        **Goal Met** 
      </td>

      <td>
        Users who fulfilled the journey goal condition.<ul><li>**Before Node**: Goal achieved while waiting, but did not receive the following message.</li><li>**At Node**: Users currently at the node who have met the goal. If the *Failed* connector is not connected, users who do not qualify for any path from the node are retained in the **At Node** state, as the next step is not defined for them.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        **Journey Timeout Exits**
      </td>

      <td>
        Users who exited the journey due to reaching the overall journey timeout duration. In the case of multiple journey versions, users can exit an Engage node for the following reasons: <ul><li>**Journey Timeout**: The user did not take the expected action within the defined node delay window.</li><li>**Version Change**: In the case of multiple journey versions, users may be forced to exit from older versions when a new version is published and the older version is stopped. The older journey version was stopped while the user was still in progress. These users are automatically exited when a new version is published and takes over.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

You can view the campaign-level stats for every node. Click the **Engage** node to open the campaign-level stats.

> 📘 Unique Users Converted
>
> If a user enters the journey and performs the conversation event twice, only one conversation event for that unique user is counted.

# Force Exit Node

The *Force Exit* node is used to remove users from the journey at a specific point manually. This node tracks only the number of users who were explicitly exited at that point in the journey flow.

<Image title="Force exit node for Journeys" alt={310} align="center" border={true} src="https://files.readme.io/200599b-Journeys_node_Force_exit.png">
  Force Exit Node
</Image>
