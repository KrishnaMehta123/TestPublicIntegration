---
title: Segment Membership Validation
excerpt: >-
  Ensure your engagement targets correct audiences with segment membership
  validation option.
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

CleverTap strongly recommends ensuring that the segment is not used in any campaigns or journeys before deleting it. Because every deletion may impact other segments that depend on it. Additionally, campaigns and journeys that utilize these affected segments in their include-exclude or custom list definitions are also affected.

For example, an e-commerce business might want to send a campaign to users who have viewed a T-shirt in the last 30 days but exclude the segment of users who have made a purchase in the last 30 days. However, the users who have purchased in the last 30 days are not available because the segment for these users was deleted. In that case, it will impact the campaign run by the e-commerce business.

# Validate Segment Membership

This section provides information about ensuring that the campaigns/journeys target the correct set of audiences if the *Who* section uses an *[include/exclude](https://docs.clevertap.com/docs/segmentation-rules#:~:text=App%20Fields%20Rule-,Segments,-%3A%20Segment%20users%20based)* or *[custom list](doc:types-of-segments#custom---list-based-segments)* definition.

## For Campaigns

When you open a draft campaign or clone a campaign that uses the *include/exclude* definition, you are prompted to validate if the segment used is valid and reachable. The following are the three stages where you will be prompted to validate your target segment:

* [When opening a draft campaign or cloning an existing campaign](doc:segment-membership-validation#when-opening-a-draft-campaign-or-cloning-an-existing-campaign)
* [When defining the target segment for the campaign](doc:segment-membership-validation#when-defining-target-segments-for-campaigns)
* [When publishing a campaign](doc:segment-membership-validation#when-publishing-a-campaign)

### When Opening a Draft Campaign or Cloning an Existing Campaign

The *Segment validation* popup opens from the campaign page as follows

<Image alt="Segment Validation Popup When Opening a Draft or Cloning an Existing Campaign " align="center" width="75% " border={true} src="https://files.readme.io/b5f1a57-image.png">
  Segment Validation Popup When Opening a Draft or Cloning an Existing Campaign 
</Image>

Click **Ok** and verify from the *Segments* page of the CleverTap dashboard if the segment included in the campaign is reachable.

### When Defining Target Segments for Campaigns

A warning appears at the top of the *Who* section of the campaign. The warning also includes the steps to verify whether the segment defined in the *Who* section is valid and reachable. 

<Image align="center" className="border" border={true} src="https://files.readme.io/ace004a-Verfiy_the_Target_Segment_from_Who_section.png" />

Before you go ahead and draft a campaign, you must go to the *Segments* page from the CleverTap dashboard and verify the accuracy of segment definition and estimated reach.

### When Publishing a Campaign

The *Segment validation* popup opens when you click **Publish Campaign**. It prompts you to confirm whether you have validated all the segments used in the campaign before you publish it. Select *I confirm segments used in the campaign are validated* and click **Publish** if you have already validated. If you have not already validated, click **Cancel** and go to the *Segments* page from the dashboard and verify the accuracy of segment definition and estimated reach.

<Image align="center" className="border" width="85% " border={true} src="https://files.readme.io/79b1989-image.png" />

## For Journeys

When opening a draft journey or cloning an existing journey, you are prompted to validate if the segment used is valid and reachable. The following are the three stages where you will be prompted to validate your target segment:

* [When opening a draft journey or cloning an existing journey](doc:segment-membership-validation#when-opening-a-draft-journey-or-cloning-an-existing-journey)
* [When defining the target segment for Journeys](doc:segment-membership-validation#when-defining-target-segments-for-journeys)
* [When publishing a journey](doc:segment-membership-validation#when-publishing-a-journey)

### When Opening a Draft Journey or Cloning an Existing Journey

The *Segment validation* popup opens from the Journey page as follows

<Image alt="Segment Validation Popup When Opening a Draft Journey or Cloning an Existing Journey" align="center" border={true} src="https://files.readme.io/6bc85c7-Segment_Validation_Popup_-_Journeys_Canvas.png">
  Segment Validation Popup When Opening a Draft Journey or Cloning an Existing Journey
</Image>

Click **Ok** and verify from the *Segments* page of the CleverTap dashboard if the segment included in the campaign is reachable.

### When Defining Target Segments for Journeys

When you open the Segment—Action popup to define the target segment that qualifies for your journey, a warning appears at the top. The warning includes the steps to verify whether the segment defined in the *Who* section is valid and reachable. 

<Image align="center" className="border" border={true} src="https://files.readme.io/589255a-Segment_Validation_-_Target_Segment_of_Journey.png" />

Before you go ahead and draft a journey, you must go to the *Segments* page from the CleverTap dashboard and verify the accuracy of segment definition and estimated reach.

### When Publishing a Journey

The *Segment validation* popup opens when you click **Publish** to publish the journey. It prompts you to confirm whether you have verified all the segments used in the journey before you publish it. Select *I confirm segments used in the journey are validated* and click **Publish** if you have already validated. If you have not already validated, click **Cancel** and go to the *Segments* page from the dashboard and verify the accuracy of segment definition and estimated reach.

<Image align="center" className="border" width="85% " border={true} src="https://files.readme.io/a0ee668-Segment_Validation_When_Publishing_a_Journey.png" />

Once you have published campaigns or journeys following segment validation, subsequent cloning of these campaigns or journeys will adhere to the standard campaign or journey creation flow. You will not be prompted to validate your target audience for the newly-cloned campaigns or journeys.
