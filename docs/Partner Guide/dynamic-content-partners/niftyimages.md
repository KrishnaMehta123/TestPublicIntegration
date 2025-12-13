---
title: NiftyImages
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

[NiftyImages](https://niftyimages.com/) allows marketers to create personalized and dynamic images for Email and In-App messaging campaigns. By integrating NiftyImages with CleverTap, you can enhance your campaigns with real-time customized visuals, such as personalized images, countdown timers, and dynamic charts, creating a more engaging experience for your audience. With this integration, you can:

- **Personalize Emails with Dynamic Images**: Embed dynamic images tailored to individual users.
- **Drive Urgency with Real-Time Countdown Timers**: Add real-time countdown timers to create urgency for promotions or events.
- **Enhance In-App Messages with Personalized Visuals**: Personalize In-App messages with user-specific images.
- **Keep Visuals Fresh with Automated Image Updates**: Ensure your Emails and In-App messages reflect the most up-to-date information without manual intervention.

# Prerequisites for Integration

The following are the prerequisites for NiftyImages:

- Ensure you have access to your NiftyImages account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**, and **Region**.

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by NiftyImages. The CleverTap and NiftyImages integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [NiftyImages](https://niftyimages.com/ContactUs) for support and resolution.

# Integrate CleverTap with NiftyImages

To set up the CleverTap integration with your NiftyImages account, perform the following steps:

1. [Create Personalized Image in NiftyImages](doc:niftyimages#create-personalized-image-in-niftyimages).
2. [Configure Email Campaign in CleverTap](doc:niftyimages#configure-email-campaign).  
   OR  
   [Configure In-App Campaign in CleverTap](doc:niftyimages#configure-in-app-campaign).

## Create Personalized Image in NiftyImages

NiftyImages enables marketers to create dynamic and personalized visuals for campaigns, including countdown timers, personalized images, and data-driven charts. To do so, follow these steps:

1. Log into your [NiftyImages](https://niftyimages.com/) account.
2. Select the type of image you want to create from the available options:
   - Personalized Image (user-specific details)
   - Countdown Timer (event-based urgency)
   - Mobile Text (responsive visuals)
   - Messaging Charts (real-time data-driven graphics)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d2af368bce1054a4c79a32a38f08de9e3b5a158fc5284e5872f01dc1f5f125fe-image.png",
        null,
        "Create New Image"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create New Image"
    }
  ]
}
[/block]


For this, we have selected a **Personalized Image** (upload your own image).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06da0fa8021e2fcfe976c6a85b1be9261898e0c910e5ba1c5485cd4acf8bd0bf-image.png",
        null,
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


**Personalization Options**:

- Use merge tags like `{{Profile.name}}` to dynamically pull data and personalize elements (for example, inserting user names automatically).
- Set default values to ensure a fallback is displayed when specific data isn’t available (for example, `{{Profile.name | default: "User"}}` will display "User" if the name field is empty).
- Configure customization based on the intended purpose (for example, using a countdown timer for a sale event or dynamic charts for personalized insights).
- Customize fonts, colors, and layouts to enhance personalization.

> 📘 Note
> 
> Merge tags in NiftyImages function the same way as [Liquid tags](doc:personalize-message-all#liquid-tags) used in CleverTap. They dynamically pull user-specific data to personalize content in Emails and In-App messages.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/70db4944f85c074523132a58cf0e08ec1c7b2a1d0ebadd1e4930813ef11a669b-2025-03-18_17-59-02_1.gif",
        "",
        "Personalization Options"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Personalization Options"
    }
  ]
}
[/block]


3. Add _Design Options_ and _Advanced Options_ to enhance the image by adding:
   - **Text** – Insert user names or messages.
   - **Image** – Upload custom visuals.
   - **Shapes** – Highlight key areas.
   - **Dynamic Image** – Change visuals based on real-time data.
   - **Data Source** – Connect live data.
   - **Chart / Calendars** – Display insights or events.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f246f962553a084299297dde5edc23d6771d79148e638a3b532b00b87da245f-image.png",
        null,
        "Add Elements"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Add Elements"
    }
  ]
}
[/block]


4. Save and generate HTML code. To do so, perform the following steps:
   1. Click **Save** in the top-right corner.
   2. Provide a name for the file. NiftyImages generates an **HTML code snippet**.
   3. Preview the functionality by entering a sample name to see the dynamic image changes.
   4. Copy the generated HTML snippet.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f7c302a6dcb3c1fad1b75d6958f00b1b76370a2c613a45f1a9ea8b663c6d88e5-2025-03-18_17-59-43_1.gif",
        "",
        "Generate HTML Code"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Generate HTML Code"
    }
  ]
}
[/block]


## Configure Email Campaign

Set up and personalize your email campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   - Select a **Basic Template, Pre-used Template, or a Saved Template**.
   - Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the copied **NiftyImages HTML snippet** inside the `<body>` section in CleverTap Email editor Source.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/66c125021595a44bc2ff34a134678a79a4a84181bc4b0754a214199019a14ca6-2025-03-19_12-38-49_1.gif",
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


4. Replace the **MERGE_TAG** with the appropriate [CleverTap Liquid Tag](doc:personalize-message-all#liquid-tags) for personalization, as shown in the following example:

```html With Liquid Tag
<img src="https://img1.niftyimages.com/hqkh/ixv5/5qyp?name={{Profile.name}}" />
```

You can also use the following code to dynamically personalize images for users while setting a default fallback value for the personalized image in NiftyImage itself.

```html HTML
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body style="font-family:Arial,'Helvetica Neue',Helvetica,sans-serif;">
<p>Hello</p>
<p><img src="https://img1.niftyimages.com/hqkh/ixv5/5qyp?name={{Profile.name}}" /></p>
<p> </p>
</body>
</html>`
```

5. Send a test email to verify personalization and ensure the NiftyImages integration functions correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/40643942f6d9671d91ab2e28c426426ae6b316f784a43af5acc1b9f7e206611f-test_emal.png",
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


6. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured merge tags and settings.

## Configure In-App Campaign

Before creating an In-App campaign, ensure your app is configured with the [CleverTap SDK](https://developer.clevertap.com/docs/clevertap-sdks) and has [Push Notifications](https://docs.clevertap.com/docs/setup-push-notification) enabled. This ensures seamless delivery and functionality of In-App messages.

Set up and personalize your In-App campaigns in CleverTap to engage users effectively. To do so, follow these steps:

1. Go to **Campaigns** in the CleverTap dashboard. Click on **+ Campaign** and select **In-App Messages** from the dropdown menu.
2. Click **Go to Editor** under the _What_ section.
3. Select any template from the available options. For this example, we will use **Custom HTML Templates**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png",
        null,
        "Custom HTML Templates"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Custom HTML Templates"
    }
  ]
}
[/block]


4. Paste the **NiftyImages HTML snippet** inside the `<body>` tag of the custom HTML.

**Example HTML for an In-App Message:**

```html
<!DOCTYPE html>
<html>
<head>
<title> </title>
</head>
<body>
<img src="https://img1.niftyimages.com/hqkh/ixv5/5qyp?name= MERGE_TAG " width="300" height="300" />
</body>
</html>
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb7051795d9a67136234cacb261189643b8ffa64796169ebf67b455cece26670-Screen_Recording_2025-01-13_at_3.51.09_PM_1.gif",
        "",
        "Custom HTML Templates"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Custom HTML Templates"
    }
  ]
}
[/block]


5. Replace the **MERGE_TAG** with the appropriate [CleverTap Liquid tag](doc:personalize-message-all#liquid-tags) for personalization. For example:
   - Use `@Profile - Name | default: "Parth"` or `{{Profile.name | default: "Parth"}}`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d117ffcd644fb335fddbdb32cc82fd62448960d2c370b7faf62d9c9c4ceea81-Screen_Recording_2025-01-13_at_3.52.37_PM_1.gif",
        "",
        "Replace the MERGE_TAG"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Replace the MERGE_TAG"
    }
  ]
}
[/block]


If the user profile contains a name, it will display the user name. In this example, the default value **Parth** will be displayed if no name is available.  

You can access liquid tags and dynamic placeholders by typing `{`, or by using the `{{` or `@` option.

6. Click **Send Test** to preview and verify the In-App message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae0b8e73dd9d461905a3aab5502da0c0811cef48b892983cac3d44b791b58ec0-image.png",
        null,
        "Send Test"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Send Test"
    }
  ]
}
[/block]


7. Click **Save** and **Publish** to launch your In-App campaign.

Once published, users will receive personalized In-App messages based on the configured liquid tags, ensuring a dynamic and engaging experience.