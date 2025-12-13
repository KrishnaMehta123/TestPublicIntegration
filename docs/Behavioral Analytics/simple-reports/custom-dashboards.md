---
title: Custom Dashboards
excerpt: Understand what are custom dashboards in CleverTap
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

The *Custom Dashboards* is a feature in CleverTap that allows you to create and customize your board. CleverTap provides a set of default dashboards, such as the [Today View](doc:today-view), which you can use to analyze user activity in your application. 

Each custom dashboard you create is composed of cards, which are widgets you can pin to the board to track the metrics of your interest. You can pin cards and track the metrics using one of the following features: [events](doc:events), [funnels](doc:funnels), [segments](doc:segments), [trends](doc:trends),  [cohorts](doc:cohorts), and [pivots](doc:pivots).

For example, if you want to track the following metrics for the last 30 days:

* Number of users who performed App Launched and Charged events
* Number of users who performed the Charged event

You can create a custom dashboard and add cards to track the above metrics, as shown in the following figure. You can also pin those cards to the dashboard. 

<Image title="Overview of the Custom Dashboard" alt={2370} align="center" border={true} src="https://files.readme.io/330f13a-Custom_Dashboard_-_Overview.png">
  Custom Dashboard Overview
</Image>

After you build your custom dashboard, you can also share the board with others in your organization.

Custom dashboards can have the following features:

* [Boards](doc:custom-dashboards#boards)
* [Cards](doc:custom-dashboards#cards)

# Boards

The board's section provides information about different boards created for the project and the operations that can be performed on these boards. On this page, users can view a list of all boards:

* Created by them,
* Shared with them, and 
* Public boards that are available for users in their organization. 

To access boards on the CleveTap dashboard, navigate to *Boards* > *All Boards*. The *All boards* page opens.

<Image title="List of Boards and Cards" alt={2380} align="center" border={true} src="https://files.readme.io/5733378-All_Boards.png">
  List of Boards and Cards
</Image>

## Create a Custom Dashboard

This section covers how to create a custom dashboard. To create a board:

1. Navigate to **Boards** from the left navigation menu.
2. Click **+ Board**.
3. Enter your board name and click **Create**.

<Image alt="Creating a Board" align="center" border={true} src="https://files.readme.io/a009618-Create_a_Board.gif">
  Creating a Board
</Image>

## Operations

You can perform the following actions on a particular board:

### Sort

You can sort the boards by the date on which the board was created and the person who created the board. To sort the boards, click the ![Arrow](https://files.readme.io/ea0d68c-Arrow_icon.png) icon under *Created by* and *Created on* columns.

<Image title="Sort boards based on date and user who created it" alt={2378} align="center" border={true} src="https://files.readme.io/f99cf25-Sort_Boards.png">
  Sort Boards
</Image>

### Search

You can search the boards by board name or creator's email ID. To search boards, enter the search criteria under the Search text box

<Image title="Search boards using board names or creator email" alt={2378} align="center" border={true} src="https://files.readme.io/7a31a9a-Search_boards.png">
  Search Boards
</Image>

### Mark As Favorite

You can mark a board as a favorite by performing the following steps:

1. Select the board from the *Boards* > *All boards* page.
2. Click **Mark As Favorite** from the top of the page. 

<Image title="Mark a board as favorite" alt={2370} align="center" border={true} src="https://files.readme.io/e061901-Mark_As_Favorite.png">
  Mark a Board as Favorite
</Image>

The message *Board marked as favorite successfully!* displays at the top of the board page, and the board gets added to the *Favorites* section on the left navigation.

<Image title="View boards marked as favorite" alt={2724} align="center" border={true} src="https://files.readme.io/6ed3ad1-Mark_as_Favorite.png">
  Favorite Boards
</Image>

### Change Date Range

You can view the data for the different periods by changing the date range of all cards on the board, as shown below:

<Image title="View cards based on specified date range" alt={1188} align="center" border={true} src="https://files.readme.io/19635f0-Change_Date_Range.gif">
  View Cards based on Date Range
</Image>

### Refresh

You can refresh the dashboard to view the most recent information by clicking **Refresh** from the top of the page.

<Image title="Refresh the dashboard to view recent information" alt={2370} align="center" border={true} src="https://files.readme.io/9ee1da4-Refresh.png">
  Refresh the Dashboard
</Image>

### Share

CleverTap provides restricted dashboard access so that the dashboard owner can control the members who can view and contribute to the insights captured on the dashboard. The dashboard owner can add or remove members from the access list and can control access levels.

  To share a dashboard, perform the following steps:

1. Create your custom dashboard.
2. Click **Share**. The *Share Board* popup displays with restricted permissions by default. Use the search box to view and add users to this board.

> 🚧 Share Board
>
> The *Share* option is only visible to the board's creator.

3. Select a user and click **Send**. An email is sent to the user with a link to the board.\
   Select as many users as needed before clicking **Send** to add multiple users.

<Image title="Share the board with the selected user" alt={560} align="center" border={true} src="https://files.readme.io/98a8931-Share_Board_-_Select_User.png">
  Share the Board
</Image>

> 📘 Change Default Board Permissions
>
> You can change the default permissions by clicking the *Change* link on the Share Board and selecting the appropriate permission.
>
> <Image title="Change default user permission to access the boards" alt={561} align="center" border={true} src="https://files.readme.io/8f0e9f4-Share_Board_-_Change_Default_Permission.png">
>   User Permissions to Access Boards
> </Image>

### Clone

This option is used when you want to track the same metrics with minor changes. Anyone who has access to your project can clone the board by clicking **More** and then selecting **Clone** from the list.

<Image title="Clone a board" alt={1186} align="center" border={true} src="https://files.readme.io/b5a34d1-Clone_Board.gif">
  Clone a Board
</Image>

### Edit

You can rename the board by clicking **More** and then selecting **Edit** from the list.

<Image title="Edit a board" alt={1188} align="center" border={true} src="https://files.readme.io/b0170ce-Edit_Board.gif">
  Edit a Board
</Image>

### Delete

You can delete the boards you created by clicking **More** and then selecting **Delete** from the list.

<Image title="Delete a board" alt={1186} align="center" border={true} src="https://files.readme.io/8faea74-Delete_Board.gif">
  Delete a Board
</Image>

### Edit User Permissions

You can also edit the user's permissions to either Viewer (view-only access), Editor (view and edit access), or remove the user completely. To do so:

1. Click **Share** and select the permission from the list next to the user name.
2. Select *Viewer* or *Editor*. You can remove the user access by selecting *Remove*.
3. Click **Save**.

<Image title="Edit user permissions to access boards" alt={1194} align="center" border={true} src="https://files.readme.io/e9a9c2d-Edit_User_Permission.gif">
  Edit User Permissions
</Image>

## Board Limits

The following table describes a list of board limits:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Plan Type</p>
      </th>

      <th>
        <p>Limits</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Paid Plans (Enterprise/Business)</p>
      </td>

      <td>
        <ul><li>Each user can create up to 100 boards.</li><li>Users can pin up to 20 cards per board.</li><li>Users can share the board within the organization.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

# Cards

This section provides information about different operations that can be performed on the card. Select the board to view all the included cards.

## Operations

You can perform the following actions on a particular card:

### Pin a Card

When you create your new board, you start with an empty board. CleverTap allows you to pin Event details, Segments, Funnels, Cohorts, Trends, or Pivots to a particular card.

You can pin a card on a board in the following two ways:

* [Pin a Card from Board](doc:custom-dashboards#pin-a-card-from-board)
* [Pin a Card from Analytics](doc:custom-dashboards#pin-a-card-from-analytics)

#### Pin a Card from the Board

Consider the example where you want the number of users who performed *Charged* event in the last 30 days. To pin the card for these metrics to the Board:

1. Click **Events** from the empty board.
2. Select *Charged* event and select the required *Date Range* from the *Events* page.
3. Click the ![Pin](https://files.readme.io/32ed498-Pin_icon.png) icon. 
4. Enter the *Card name* and select an existing board or create a new board by selecting *Pin to a new board*. 
5. Click **Pin** to view the metrics on the custom dashboard whenever required.

<Image alt="Pin Event to a Custom Board" align="center" border={true} src="https://files.readme.io/895eebe-Pin_a_Card_from_Board.gif">
  Pin Event to a Custom Board
</Image>

The pinned card is visible on the board:

<Image alt="View Card on a Custom Board" align="center" border={true} src="https://files.readme.io/5fb4513-View_Card_on_Board.png">
  View Card on a Custom Board
</Image>

#### Pin a Card from Analytics

Users can pin Event details, Segments, Funnels, Cohorts, Trends, or Pivots to a particular card. Consider the example of pinning a card that shows information about a particular segment.

> 📘 Note
>
> The steps listed below can also be followed to pin any chart that provides the *Pin to board(s)* option.

To pin a card of the example metrics:

1. Navigate to *Segment* > *Segments*, from the dashboard.
2. Select a segment.
3. Click the ![Pin](https://files.readme.io/32ed498-Pin_icon.png) icon to pin the report to an existing or new board.

<Image title="Pin a card on the board" alt={693} align="center" border={true} src="https://files.readme.io/80633fb-Cards_1_-_pin_a_card.png">
  Pin a Card on the Board
</Image>

4. Enter the *Card name* and select the board where you want to pin this card.

<Image title="Pin a segment to custom board" alt={2236} align="center" width="smart" border={true} src="https://files.readme.io/64f62cf-Pin_a_segment_to_Custom_Board.png">
  Pin a Segment to Custom Board 
</Image>

> 📘 Other Analytics Features
>
> The following steps can also be performed for *Events*, *Funnels*, *Segments*, *Find People*, and *Trends*.

### Rename a Card

You can change the card's name when you hover over any card on a board. To do so:

1. Click the ![Edit](https://files.readme.io/2ac4bf2-Edit_icon.png) icon and enter the new name.
2. Click the ![Checkmark](https://files.readme.io/34d30a8-Checkmark_icon.png) icon to save the changes.

<Image title="Rename a card" alt={1186} align="center" border={true} src="https://files.readme.io/89651f5-Rename_a_card.gif">
  Rename a Card
</Image>

### Customize a Card

This is **applicable only to the Funnels card**. You can customize a Funnel card and rename the following:

* Funnel Steps
* Legends

To do so:

1. Click the ![Ellipsis Icon](https://files.readme.io/7e2f596-Ellipsis_for_Renaming_of_Funnels.png) icon from the funnel card.
2. Click **Customize Card**.
3. Rename the required *Funnel Steps* or *Legends*.
4. Click **Customize**.

<Image alt="Ellipsis Icon" align="center" border={true} src="https://files.readme.io/eebe5af-Customize_a_Funnel_Card.gif">
  Customize a Funnel Card
</Image>

### Refresh

You can view the most recent data for a card by clicking the ![Refresh](https://files.readme.io/b76c705-Refresh_icon.png) icon.

<Image title="Refresh the card to view most recent data" alt={1186} align="center" border={true} src="https://files.readme.io/d8dd771-Refresh_a_card.gif">
  Refresh the Card to View Recent Data
</Image>

### Delete

You can delete the card by clicking the ![Trash](https://files.readme.io/7b0992e-Trash_icon.png) icon.

<Image title="Delete a card" alt={1186} align="center" border={true} src="https://files.readme.io/b1ad24f-Delete_a_card.gif">
  Delete a Card
</Image>

> 📘 Delete Cards Access
>
> Only the creator of the board or the administrators can delete cards on public boards.

### Resize

You can resize the card by clicking the ![Resize](https://files.readme.io/ad1e01b-Resize_icon.png) icon.

<Image title="Resize a card" alt={1186} align="center" border={true} src="https://files.readme.io/d9ad652-Resize_a_card.gif">
  Resize a Card
</Image>

### Move

You can reorder the sequence of cards by clicking the ![Move](https://files.readme.io/9d21ac7-Move_icon.png) icon.

<Image title="Move a card on the board" alt={1186} align="center" border={true} src="https://files.readme.io/763c6ef-Move_a_card.gif">
  Move a Card on the Board
</Image>

# Access Control

The action that a user can perform on the dashboard may vary depending on the type of access, as shown in the following table:

| Action                                         | Administrator | Creator/Approver | Members                         |
| :--------------------------------------------- | :------------ | :--------------- | :------------------------------ |
| Create a board                                 | Yes           | Yes              | Yes, can create a private board |
| Delete their board                             | Yes           | Yes              | Yes                             |
| Pin a card to their board                      | Yes           | Yes              | Yes                             |
| Pin a card to any public board                 | Yes           | Yes              | No                              |
| Delete a pinned card from their board          | Yes           | No               | No                              |
| Delete any pinned cards from any public boards | Yes           | No               | No                              |
