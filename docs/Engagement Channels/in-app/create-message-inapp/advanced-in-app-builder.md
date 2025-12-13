---
title: Advanced In-App Builder
excerpt: Learn how to edit and design In-App campaigns from the CleverTap dashboard.
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

CleverTap's Advanced In-App Builder enables the creation of visually appealing and engaging mobile In-App messages that align with your brand's aesthetics. This document walks you through the main features of the In-App Editor and its usage to help you maximize this feature's potential. 

<Image alt="Sample In-App with Advanced Builder" align="center" width="40% " src="https://files.readme.io/70dd7cd5e206879de2a4edbe492e11ab7d733e3879aedc4cae3a553d6121405b-Starting-image-1.png">
  Sample In-App Message with Advanced Editor
</Image>

The Advanced In-App Builder offers remarkable flexibility and ease of use. Here are the key features:

* **Automatic Scaling**: Content automatically adjusts to fit any device size, ensuring consistent presentation across all platforms.
* **Custom Layout**: Arrange elements in the container to create any desired layout.
* **Stacking Elements**: Overlay images or other elements for more complex and visually engaging designs.
* **Styling Options**: Access a wide range of styling options for every element, giving you precise control over the appearance.
* **Dismiss Button Controls**: Customize the appearance and behavior of the dismiss button, including its style and placement. 
* **Animation**: Enhance user interaction with dynamic effects such as slide or fade-in animations. 

# Advanced In-App Builder Template

To use the Advanced In-app Builder template:

1. From the *What* section in the In-App builder, select the *Message Type* and click **Go to Editor**. The In-App templates are displayed. 

<Image alt="Advanced In-App Builder" align="center" border={true} src="https://files.readme.io/886bdbb6e9513fa588e41a43d85f09af9c4b0d7431a0b81cdbe25d1e69f858bc-Screenshot_2024-10-11_at_11.53.15.png">
  Advanced In-App Builder
</Image>

2. From *Basic Templates*, select *Advanced In-app Builder*. The Advanced In-App Builder displays. 

<Image alt="Advanced In-App Builder" align="center" border={true} src="https://files.readme.io/b71a90dc51c963fa8eb012090cb6794a5b06fda319cf5132001f75264bb43fa8-Controls.png">
  Advanced In-App Builder
</Image>

The Advanced In-App Builder has a *What You See Is What You Get (WYSIWYG)* interface, which allows you to make modifications in real-time.

It is divided into two main sections:

* **Canvas (Left Side)**: The canvas is where you design your In-App message. It is fully interactive, allowing you to drag and drop elements and adjust their position and size with ease.
* **Controls & Styling Menu (Right Side)**: This menu contains controls and styling options for the elements on the canvas. Any changes made here instantly reflect on the canvas in real time.

> 📘 Test and Preview
>
> The *Preview and Test* feature is currently unavailable for the Builder. To test your In-App message on a real device:
>
> 1. **Send the Campaign**: Exclusively send the campaign to a specific user for testing.
> 2. **Recreate and Send**: After you are done testing, recreate the campaign and send it to your intended audience.

## Builder Elements

In the Advanced In-App Builder, *Elements* are the core components used to construct your message. Upon opening the builder, three default elements are available, as shown in the following image: 

<Image alt="Default Elements" align="center" width="40% " border={true} src="https://files.readme.io/c70df865f05856c2a53bc137e131fe0ab60fb9bf2ebb9f6439fba501513819cb-image.png">
  Default Elements
</Image>

### Overlay

The overlay provides a background for your In-App message, ensuring a seamless, integrated look.

<Image alt="Design Overlay" align="center" border={true} src="https://files.readme.io/59d4503d9c0cbbc300f4e5d245189b55d4b065e499d310f33724c110f8d82b84-Overlay_slider.gif">
  Design Overlay
</Image>

The overlay allows you to modify the following:

* **Transparency level**: Control the transparency level of the Overlay.
* **Color Background**: Add a color background.
* **Image Background**: Add an image as a background. Click **Upload** to add an image.

### Container

The container holds all the content, such as text, images, and buttons, representing your In-App message.

<Image alt="Design Container" align="center" border={true} src="https://files.readme.io/5533cc57850f22fb837390faed0082612df60c482e4be8d08cad2a526a0bcb6d-image.png">
  Design Container
</Image>

The container allows you to modify the following:

* **Background**: Apply a background color or image to your design.
* **Aspect Ratio**: Select the Aspect ratio that best fits your use case.
* **Margin**: Adjust the margin percentage to create a buffer between your popup and the device edges.
* **Border Radius**: Control the roundness of the container's edges. A higher value results in a rounder appearance.

### Dismiss Button

The *Dismiss Button* allows users to close the In-App message.

<Image alt="Hide/Display Dismiss Button" align="center" border={true} src="https://files.readme.io/889f6fa799897269c2d9e9e3fe4ddc331f73720c8cffc3eb5cfdf946e48c8132-screenshot-1.png">
  Hide/Display Dismiss Button
</Image>

## Add New Elements Inside Container

Click **Add** on the canvas to add *Text*, *Image*, or *Button*.

<Image alt="Add Elements in Container" align="center" border={true} src="https://files.readme.io/c1950ae9cf14eb15e517649ad93edc2319c50b83ef422e708c1b27c40e54e851-screenrecording-2.gif">
  Add Elements in Container
</Image>

You can enhance your In-App message by adding the following elements inside the container:

* **Text**: Add text to convey your message. Use the available styling options to ensure it fits your brand's style.
* **Image**: Incorporate visuals or branding images to create an engaging experience.
  * The builder supports multiple image elements, which you can stack on top of each other.
  * Image elements can also function as buttons, enabling call-to-actions directly from the image.
* **Button**: Create call-to-action buttons, such as *Shop Now* or *Learn More*, with precise control over the design and positioning.

### Display Element Over or Behind an Element

When working with stacked elements such as images, text boxes, or buttons, the *Bring Forward* and *Send Backward* buttons manage their visibility on the user's screen. If one element overlaps another, clicking **Bring Forward** brings the selected element to the front, ensuring it is fully visible.

<Image alt="Bring Forward and Send Backward Buttons" align="center" border={true} src="https://files.readme.io/296be8c99677e1a5a42d5b3070322bdf13c6bfbb8bb9ef33a4ef829fbe0ff4f8-screenrecording-3.gif">
  Position Elements
</Image>

## Add Animations

The builder provides built-in animation options to improve the flow of the user experience. Animations are configured from the Container element.

<Image alt="Animation" align="center" border={true} src="https://files.readme.io/e3e774a3fdb678a01416ff17dbfd20226ab3fa857e7359e2551ae55449bd0a40-scheenrecording-1.gif">
   Design Animation
</Image>

You can enhance user interaction with the help of various animation options as follows:

* **Animation types**: Choose from Instant (default), Dissolve, or Move In animations.\
  The Duration is set in milliseconds, allowing you to experiment with different values and observe the effect in the canvas.
* The **Duration** value can be set in milliseconds, and you can try different settings and see how they behave in the Canvas
* The **Repeat** button replays the animation in the Canvas. 

# Banners

Mobile Banner ads are a type of in-app message designed to subtly engage users without interrupting their app experience. They appear as small, rectangular strips anchored to either the top or bottom of the screen and can be static or animated using rich media.

Unlike Interstitial messages or full-screen Covers, Banners are *nonintrusive*. They do not block app interactions or obscure the rest of the screen. They allow seamless user activity while still effectively delivering your message.

<Image alt="Create in-app banner" align="center" border={true} src="https://files.readme.io/9405d9f1a56e914769b2147a3627b4e57d6592202ff5bfafe8a099c71ac95d6d-image.png">
  In-App Banner
</Image>

## Create Banners

You can customize Mobile Banners using the Container Element, which gives you complete control over the banner’s design, content, and behavior. 

To create a Banner, follow these steps:

1. Go to *Advanced In-App Builder* from the *Builders* tab when creating an in-app message campaign.
2. Select the *Container* element and apply the Top or Bottom position to create a Banner. 
3. Customize your Banner by adding text or images. 
4. Configure optional behaviors such as animations, tap actions, or dismiss rules.

Your Banner is ready to be used in an in-app campaign.

# Custom Fonts

The Advanced In-app Builder supports **Custom Fonts** for use across all of the Text content in your Mobile In-app Campaign. 

To use custom fonts, follow these steps:

1. When creating an in-app message campaign, select *Advanced In-App Builder* from the *Builders* tab. 
2. Select the *Container* element to manage custom fonts.

<Image alt="Font Settings in Container" align="center" width="50% " border={true} src="https://files.readme.io/154da0d64ddecb9d44d104b8e2d7e46e54f3e7e83244f6d98d0ffe263f67c420-image.png">
  Font Settings in Container
</Image>

2. From the *Font* list, you can select any available *System Fonts* or your *Custom Fonts*, which will be applied to all elements with Text in your Campaign. 

<Image alt="Select Font " align="center" width="80% " border={true} src="https://files.readme.io/99b50bebbb4e609093789b37b8d8907402b5d6639541bd57f7c628c98373d10a-Screenshot_2025-01-09_at_16.32.57.png">
  Select Font 
</Image>

3. Click the **Add** button to add your new Custom Font. You can either upload a **CSS file** containing your Custom Font or use the **URL** of an already hosted file. 

<Image alt="Add New Custom Font" align="center" width="70% " border={true} src="https://files.readme.io/015cb3f946f84d8d6a1b64e8604f11a0959caeceb8e8a6f3d5f21b1e11bfdc64-image.png">
  Add New Custom Font
</Image>

4. Enter the following details to create your Custom Font:

   <br />

   <Table>
     <thead>
       <tr>
         <th>
           **Field Name**
         </th>

         <th>
           **Description**
         </th>
       </tr>
     </thead>

     <tbody>
       <tr>
         <td>
           **Font Name**
         </td>

         <td>
           Uniquely identifies the font. This field has a limit of up to 50 characters.
         </td>
       </tr>

       <tr>
         <td>
           **Font Family**
         </td>

         <td>
           Defines the style applied to the font. This field has a limit of up to 50 characters. The custom font family must match the name of the font face in the CSS file.
         </td>
       </tr>

       <tr>
         <td>
           **Fallback to**
         </td>

         <td>
           If the Custom Font fails to load on the device, we will use one of the FallBack Fonts to render the In-app Campaign.
         </td>
       </tr>

       <tr>
         <td>
           **Font URL**
         </td>

         <td>
           If the font is not on your local system, you can select this option to add the URL for the required font. The URL must point to a CSS file.<br />- If your custom font is a public font available on the web, you can add the URL for the font.<br />- If you upload the font to your private server, check that CORS is enabled on the server to provide the custom font file.<br /><br />The custom font file must have the following header: `Access-Control-Allow-Origin: *`. When defining font URLs in the `src` attribute, utilizing the `https` protocol is important. Refer to the sample CSS code.
         </td>
       </tr>

       <tr>
         <td>
           **Upload Font**
         </td>

         <td>
           If you already have a font file available on your local system, choose **Upload Font**, and click **Upload** to upload the CSS file for your custom font. The file size should be a maximum of 1 MB.
         </td>
       </tr>
     </tbody>
   </Table>

   ## Sample CSS code

   <br />

   ```css CSS
   @font-face {
     font-family: 'Dancing Script';
     font-style: normal;
     font-weight: 400;
     font-display: swap;
     src: url(https://fonts.gstatic.com/s/dancingscript/v25/If2RXTr6YS-zF4S-kcSWSVi_szLgiuEHiC4W.woff2) format('woff2');
     unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
   }
   ```

   <br />

# FAQs

### How do I add new elements other than the default ones?

To add new elements, use the controls on the right side of the builder to drag and drop images, text, and buttons directly into the container.

### Can I preview my In-App message before sending it out?

Currently, the Preview and Test feature is limited in the advanced In-App editor. You can test it by first sending the message to a single device.

### Are there limitations on device sizes or layouts

No, the content automatically scales to fit any device size, ensuring consistency across platforms.

### What aspect ratio should I pick for landscape orientation?

Aspect Ratios of 1:1 and 16:9 are ideal for creating In-App content in landscape orientation.
