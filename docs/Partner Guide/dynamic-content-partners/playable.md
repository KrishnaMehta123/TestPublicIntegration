---
title: Playable
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

[Playable](https://playable.video/) enables marketers to embed short, auto-playable videos inside emails, boosting user engagement, click-through rates, and conversions.

Integrating CleverTap with Playable enables you to insert high-quality, auto-play videos seamlessly into your Email Campaigns. 

With this integration, you can:

- Launch product teaser videos directly in emails to drive anticipation before a launch.
- Embed limited-time promotional videos to increase urgency and drive conversions.
- Deliver personalized onboarding clips to educate users right inside their inbox.

# Prerequisites for Integration

The following are the prerequisites for CleverTap and Playable integration:

- Ensure you have a valid Playable account.
- Ensure you have access to the CleverTap dashboard.

# Integrate Playable with CleverTap

The integration process involves the following three major steps:

1. [Upload Video to Playable](doc:playable#upload-video-to-playable)
2. [Generate the Embed Code](doc:playable#generate-the-embed-code)
3. [Create a Personalized Email Campaign](doc:playable#configure-personalized-email-campaign-in-clevertap)

## Upload Video to Playable

Upload a video to Playable to create an optimized, interactive format suitable for use in CleverTap campaigns.

1. Go to the Playable dashboard and click **+ Add a Video**.

2. From the Upload screen, perform the following steps:

   1. Enter a Video Title that describes the content or campaign purpose.
   2. Select Output Settings such as format, size, and playback behavior.
   3. Upload a video using one of the following options:
      - Upload a video file from your device.
      - Choose a stock video from Playable’s library.
      - Provide a video URL (for example, from YouTube, TikTok, or Instagram).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/86ea7e4b3f0be1483f78c6c8be5f4c0934d5d3e09c439fe78abb000628b72d84-image.png",
        null,
        "Upload Video to Playable"
      ],
      "align": "center",
      "border": true,
      "caption": "Upload Video to Playable"
    }
  ]
}
[/block]


3. (Optional) Follow the on-screen steps to trim or edit your video.

> 📘 Note
> 
> Playable supports videos up to **10 seconds**. You can trim or edit the video during the upload process.

4. Click **Next** to complete the step.

## Generate Embed Code

After uploading the video, Playable provides the embed code required to insert the video into your CleverTap campaign.

To generate and copy the embed code, perform the following steps:

1. Click **Embed Video** on the Playable dashboard.

2. Select _Other_ from the _Who do you use to send email campaigns?_ dropdown.

3. Enter the following merge tag under the _What’s the merge tag for your provider?_ field:
   ```liquid
   {{Profile.name | default}}
   ```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c43e033fd9e73c9fd40889ea1767c9af9051c58f9d005b38e930b4e282616cf-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true
    }
  ]
}
[/block]


4. Copy the generated **HTML embed code**. This will be used in the CleverTap campaign editor.

For more details, refer to Playable's [Embed Guide](https://playable.video/docs/embed-guide).

## Configure Personalized Email Campaign in CleverTap

Set up and personalize your email campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to the _Campaigns_, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Configure the campaign per your requirements and click **Go to Editor** under the _What_ section.
3. Select from the available templates.
4. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
5. Paste the copied Playable HTML embed code copied in _step 4_ of [Generate the Embed Code](doc:playable#generate-the-embed-code) inside the `<body>` section in the CleverTap Email editor.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c6d38c21b2e13a8d71647f0cc2795a92b96dbd299db32588e1961a074a0415f-Screen_Recording_2025-01-30_at_1.48.58_PM_1.gif",
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


6. Send a test email to verify personalization and ensure the Playable integration functions correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed3179feedb583f160a9465e0ec58fad4e6422afed42c2bfaa36093596fefb9c-Screen_Recording_2025-01-30_at_1.58.56_PM_1.gif",
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


7. Publish the email campaign once verification is complete. 

By combining Playable video content with CleverTap’s advanced segmentation and messaging capabilities, you can deliver timely and relevant interactions that resonate with each user.