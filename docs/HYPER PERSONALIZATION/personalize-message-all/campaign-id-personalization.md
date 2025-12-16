---
title: Campaign ID Personalization
excerpt: ''
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

Campaign ID personalization is a feature that associates distinct campaign IDs with various marketing assets like links, image URLs, and so on; By doing so, you can track the origin of incoming traffic. When users interact with these customized links, the specific campaign ID associated with each interaction is recorded. This information is invaluable for attribution tracking, as it allows businesses to attribute user actions and conversions to the exact marketing campaign or source that prompted the engagement. This precision in tracking ensures that you have a clear understanding of which campaigns are most effective in driving traffic and conversions.

# Video Tutorial

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/wTbOgZSba1IG0ytWWixKyw/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

<br />

# Use Cases

The following are some of the use cases that this feature solves:

* **When Campaign ID is associated with Deep Links**  
  Associate campaign IDs with deep links to enable precise tracking of traffic sources when users click on these links. For instance, if you are running a campaign, you might have the following deep link: [https://demo.app.link/click?ctmessage=123456](https://demo.app.link/click?ctmessage=123456), where 123456 represents the campaign ID.

  Now, when users click on the link and open it, you can track the traffic source with the help of the campaign ID parameter. This helps you determine which campaign drives the most engagement or conversions for your business.
* **When Campaign ID is associated with Image URL**  
  Consider an e-commerce company running multiple email marketing campaigns simultaneously. They use unique campaign IDs in the image URLs of the products featured in these campaigns. When a customer clicks on a product image in the campaign and makes a purchase, the campaign ID embedded in the image URL is captured. They can attribute each sale to the specific campaign and product that led to it, providing accurate data on which campaigns are most effective in driving conversions.

# Create Campaigns Using Campaign ID Personalization

You can personalize your campaigns using campaign ID. You can do so by using CleverTap's Liquid Tags feature in the Image URL or Deep link/Open URL fields under the _What_ section of the campaign creation page.

* **Using Deep link/Open URL Field**  
  Consider the example where you want to track the traffic source within the attribution partner and analyze the behavior of the customers who interacted with the campaign. You can track the source of the traffic by adding Campaign ID to the _Deep link/Open URL_ field, as shown in the above image.

<Image align="center" alt="Campaign ID Personalization Using Deep link/Open URL Field" border={true} caption="Campaign ID Personalization Using Deep link/Open URL Field" src="https://files.readme.io/f2b3dda-Campaign_ID_Personalization_-_Deep_link_URL_field.gif" />

* **Using Image URL Field**  
  Consider an example where XYZ Styles is launching their new spring fashion collection. They want to track and personalize their marketing efforts to drive traffic and sales, while also learning more about customer preferences. XYZ Styles assigns a unique campaign ID, say `SPR2023`, to the Spring Collection Launch campaign. For each product featured in their campaigns, they embed the campaign ID in the image URLs. When users click on these personalized image links, the XYZ Styles system records the campaign ID associated with each click, linking it back to the Spring Collection Launch campaign.

<Image align="center" alt="Campaign ID Personalization Using Image URL" border={true} caption="Campaign ID Personalization Using Image URL" src="https://files.readme.io/2e2eaa4-Campaign_ID_Personalization_-_Image_URL_field.gif" />
