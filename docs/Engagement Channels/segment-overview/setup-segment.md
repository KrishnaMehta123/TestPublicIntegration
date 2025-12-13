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
To export event data to the [segment.io](https://segment.io/) dashboard via the *Campaigns* page, we need to connect the segment.io account to the CleverTap dashboard. To do so:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners*.

<Image title="Navigate to Partners Page" alt={2854} align="center" border={true} src="https://files.readme.io/deb5cd8-Navigate_to_Partners_page.png">
  View Segment on Partners Page
</Image>

3. Hover on the *Segment* icon and click **Integrate**.

<Image title="Click Integrate in Partner List Tab" alt={2396} align="center" border={true} src="https://files.readme.io/c775761-Click_Integrate.png">
  Click Integrate in Partner List Tab
</Image>

On clicking, *Integrate raw data partner - Segment* popup opens on the right side of the screen.

4. Enter the following details and click **Integrate**:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Partner Nickname
      </td>

      <td>
        Enter the nickname for the partnership.
      </td>
    </tr>

    <tr>
      <td>
        Write Key
      </td>

      <td>
        A unique identifier for each source. It helps Segment identify which source is sending the data and which destinations should receive that data.\
        For more information, refer to [Locate your Write Key](https://segment.com/docs/connections/find-writekey/).
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Configure Segment Details" alt={2402} align="center" border={true} src="https://files.readme.io/8dc099d-Integrate_raw_data_partner_-_Segment.png">
  Configure Segment Details
</Image>

After the integration is successful, the *Integrated* tag displays against Segment on the *Partner List* page.

<Image title="View Integrated Tag" alt={2396} align="center" border={true} src="https://files.readme.io/cbc5d0f-Integrated_tag.png">
  View Integrated Tag
</Image>
