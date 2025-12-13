---
title: Litmus
excerpt: Dynamic Content
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

[Litmus](https://www.litmus.com/) is a powerful personalization platform that helps marketers create dynamic, real-time content for emails, In-app messages, and push notifications. With Litmus, you can generate personalized visuals such as countdown timers, sentiment trackers, and user-specific images that render upon message open, driving deeper engagement and urgency.

CleverTap and Litmus integration enables you to deliver high-impact, personalized messaging experiences that drive conversions. With this integration, marketers can:

- Create dynamic content in Litmus using real-time personalization.
- Embed personalized images into CleverTap campaigns using HTML or image URLs.
- Tailor content at send time with CleverTap Liquid tags for user-specific personalization.

# Prerequisites for Integration

The following are the prerequisites for Litmus:

- Ensure you have access to your Litmus account with access to the Personalize module.
- Ensure you have a CleverTap account.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Litmus. The CleverTap and Litmus integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Litmus](https://help.litmus.com/) for support and resolution.

# Integrate Litmus with CleverTap

Using content created with Litmus, you can deliver real-time personalized visuals in your CleverTap campaigns. For example, you can use Litmus to generate a dynamic countdown timer or personalized image and embed it directly into your Email, In-App, or Push Notification campaign.

Consider a small example where you want to create an email campaign promoting a 48-hour flash sale. You can achieve this by adding a countdown timer to the campaign. The timer creates urgency by showing exactly how much time is left before the offer expires, encouraging users to take immediate action.

To implement this, perform the following two major steps:

1. [Create Personalized Content in Litmus](doc:litmus#create-personalized-content-in-litmus).
2. [Configure Litmus in CleverTap campaigns](doc:litmus#configure-litmus-in-clevertap-campaigns).

## Create Personalized Content in Litmus

1. Click **Create New**  and select _Personalized Content_  from the  [Litmus](https://litmus.com/sessions/new) dashboard to create dynamic content.
2. Select an image type such as:
   - **Countdown Timer**: Select this option to include a live countdown to create urgency for events or offers. For example, use it in a flash sale email showing _“Only 2 hours left!"_
   - **Personalized Image**: Select this option to include user-specific details such as name, location, or plan type within an image. For example, in a subscription renewal campaign, show an image that reads:  
     “John, your Pro Plan benefits in New York expire in 3 days!”  
     The personalized details—John, Pro Plan, and New York—are rendered directly in the image, making the message feel tailor-made and more likely to catch the user's eye in a crowded inbox.
   - **Sentiment Tracker**: Select this option to show real-time emotional feedback (such as a smiley-to-sad scale) based on campaign engagement. For example, add it to post-purchase emails to gather satisfaction ratings.
   - **Scratch-off**: Select this option to create an interactive reveal experience, ideal for surprise discounts or offers. For example, use it in a festive campaign where users scratch to reveal a 20% coupon.  
     For this example, we are selecting the _Personalized Image_ option.
3. Upload your own image or select from existing image templates. For our example, we are selecting an already existing template for customization.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec0275f98cf5c73a2dba86dbba292f4a51138e45215a8bac281d79157bc31c32-Screen_Recording_2025-04-11_at_12.49.26_PM_1.gif",
        "",
        "Personalized Image"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Personalized Image"
    }
  ]
}
[/block]


4. Design your image by using the following customization options:
   - **Add Text**: To place custom text on the image.
   - **Add Dynamic Text**: To assign a label (for example, first name).
5. Adjust styling and alignment as needed.
6. Save and generate HTML code. To do so, perform the following steps:
   1. Click **Next: Preview your personalized image** to test the content with sample values.
   2. Provide a _First Name_ and an _Email_ where the saved file details will be sent.
   3. Click **Next: Save and Get HTML**
   4. Click **Copy HTML** to copy the HTML and use it in CleverTap campaigns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e536fc243cca766c1c946b6d404d5dcaa30e123b9c62517a0e4b9c7efc49671b-Screen_Recording_2025-04-08_at_12.16.03_PM_1.gif",
        "",
        "Save and generate HTML code"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Save and generate HTML code"
    }
  ]
}
[/block]


## Configure Litmus in CleverTap campaigns

The [personalized content configured in Litmus](doc:litmus#create-personalized-content-in-litmus) can be used in any CleverTap campaign that supports HTML or image URLs. While this guide includes an example for an [email campaign](doc:litmus#configure-personalized-email-campaign-in-clevertap), you can also use Litmus content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-in-app), and other CleverTap messaging channels that support dynamic visuals.

## Configure Personalized Email Campaign in CleverTap

Set up and personalize your email campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to the _Campaigns_, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Configure the campaign as per your requirements and click **Go to Editor** under the _What_ section.
3. Select a _Basic Template_, _Pre-used Template_, or a _Saved Template_.
4. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
5. Paste the copied **Litmus HTML snippet** inside the `<body>` section in CleverTap Email editor Source.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a82d182e3a034f05bd88b203763165279bf1cd110701e6453540ddee75f199b1-Screen_Recording_2025-04-08_at_2.56.53_PM_1.gif",
        "",
        "Insert the HTML Code Snippet"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Insert the HTML Code Snippet"
    }
  ]
}
[/block]


6. Replace the `MERGE_TAG` with the appropriate [CleverTap Liquid Tag](doc:personalize-message-all#liquid-tags) for personalization.  
   Set default values to ensure a fallback is displayed when specific data is not available (for example, `{{Profile.name | default: "NULL"}}` will display "NULL" if the name field is empty). Refer to [Litmus Merge Tags](https://help.litmus.com/article/136-using-merge-tags) for more details.
7. Send a test email to verify personalization and ensure the Litmus integration functions correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f7cf90d5ed0d2c60a1d160ab12535d30d66a7565af57ad3145c17bb752a8ca1-image.png",
        null,
        "Test Email"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Test Email"
    }
  ]
}
[/block]


8. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured Liquid Tags and settings.

By combining Litmus's dynamic content capabilities with CleverTap’s advanced segmentation and messaging, you can create timely, relevant interactions that resonate with every user. For more information on using personalization in CleverTap, refer to [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags).