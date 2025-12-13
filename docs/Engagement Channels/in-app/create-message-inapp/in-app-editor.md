---
title: In-App Editor
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

 The In-App editor enables you to add content to pre-built templates or customize and build them. You can select the ready-to-use template of your choice or create a custom HTML template as per your requirements. From the *What* section in the In-App builder, select the *Message Type* and click **Go to Editor.**

The In-App Editor tool displays.

<Image align="center" className="border" border={true} src="https://files.readme.io/0d4cd27-image_interstitial.png" />

# In-App Templates

The following are the four main types of In-App templates for creating engaging and personalized In-App campaigns:

* [*Basic Templates*](doc:in-app-editor#basic-templates)
* [*Ratings Templates* ](doc:in-app-editor#ratings-template)
* [*Lead Generation Templates*](doc:in-app-editor#lead-generation-template)
* [*Custom HTML Templates*](doc:in-app-editor#custom-templates)

## Basic Templates:

Basic Templates are ready-to-use templates that enable you to send tailored and personalized In-App engagements to your mobile users. You can use both text and images with CTAs to send personalized In-App messages basis your business use case.

Using basic templates, you can create the following two types of In-App messages:

* [Content with Image notifications](doc:in-app-editor#content-with-image-notifications)
* [Image-only notifications](doc:in-app-editor#image-only-notifications)

### Content with Image notifications

These templates allow you to use images in combination with text for effective messaging. You can choose from a range of templates such as *Cover*, *Half Interstitial*, *Interstitial*, *Header*, *Footer*, and *Alert*  based on your use case.

### Image-only notifications

These templates allow you to send visually engaging images that can quickly capture users' attention and encourage them to engage with the message when they launch the app. When selecting an *image only* template, you can send a message containing only an image (without CTAs, title, or message).

You can choose from the following four types of Image only notifications:

#### Cover

It is a full-screen notification template that is valuable when the intention is to direct the user's focus toward essential actions, such as requiring them to install a necessary app update.

#### Half Interstitial

It is a center-aligned image notification template for driving better engagements. You can use this template when you want to gain the user's attention towards a sale or discount.

#### Interstitial

 It is a center-aligned image notification template you can use for driving better engagements on app launch.

#### Image Interstitial

> 📘 Availability
>
> The **Image Interstitial** template is available only with CleverTap Advanced and Cutting Edge plans.

This template helps craft personalized In-App messages that seamlessly match your app's aesthetics. You upload an image and elevate the experience by incorporating up to 10 interactive hotspots, each with its own unique actions. For example, you can use this template to create a rewarding offer for your gaming app users. The following image represents a sample In-App campaign for rewarding users using the Image Interstitial template:

<Image alt="Sample In-App Campaign using Image Interstitial Template" align="center" border={true} src="https://files.readme.io/7da5c6a-Image_Interstitial_full.png">
  Sample In-App Campaign using Image Interstitial Template
</Image>

The Image Interstitial template primarily comprises the following three elements:

* Overlay: This element is a middle layer between your In-App message and your app in the background. By default, it is transparent; however, you can select a color of your choice or upload an image to it. Using the Overlay configuration, you can:
  * Opt for a semi-transparent color to softly mask the app in the background, drawing more attention to the in-app message in the foreground.
  * Upload a patterned image to create a captivating, full-screen, layered in-app message experience.
* Content: It is the core element of the template. Click in the center of a blank device or select the **Content** option from the *Element* dropdown to activate it. Further, upload an image (JPG, PNG, or GIF) consisting of all In-App mes
* sage elements such as background, text, and buttons.\
  The editor fits the image within the Content container while preserving its aspect ratio without any cropping. By default, a 10% margin is applied to the Content container. However, you can change that from the *Margin* field.
* Buttons:  The Image Interstitial buttons are transparent regions that you can place over a Content layer. You can easily move and adjust their size to align with the button elements on the image. 

The selection area within the Content Container automatically adapts to various device screen sizes, eliminating the need to create multiple versions for different devices. To see how the image and buttons scale across different aspect ratios, use the dropdown menu with different device viewport sizes located at the top for a preview.

> 📘 Preview & Test
>
> * The *Preview & Test* feature for sending tests on the device is not available for iOS or Android SDK versions lower than **6.0.0** and Unity **3.0.0.** If you need to test on a device with a lower SDK version, send the campaign exclusively to the user first, and then recreate and send it to the intended audience.

### Guidelines for Template Aspect Ratio and File Size

The following tables include the guidelines that you must keep in mind when creating In-App messages:

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Canvas Type
      </th>

      <th>
        Canvas Aspect Ratio
      </th>

      <th>
        Sample Image Sizes
      </th>

      <th>
        Image Type Supported
      </th>

      <th>
        Image Sample
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Cover
      </td>

      <td>
        Full Screen
      </td>

      <td>
        Screen Resolution
      </td>

      <td>
        Image
      </td>

      <td>
        <ul>
        <li><a href="https://files.readme.io/c78e632fe9b547010a424ec3e302ef6e223f21fef9a05ba568a88d9d551d435b-image.png" target="_blank">Cover iPad</a></li>
        <li><a href="https://files.readme.io/83df2ce6164cf5661c328a7af509f264a22d622fff0548b5248bb15c39a829ab-image.png" target="_blank">Cover </a></li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Interstitial
      </td>

      <td>
        1.78:1
      </td>

      <td>
        16:9
      </td>

      <td>
        Image, gif, audio
      </td>

      <td>
        <ul>
        <li><a href="https://files.readme.io/ce2ad1abe590ace8a15544f43edde68db3dc776e4a515da77954404c31e652c6-image.png" target="\_blank">Interstitial iPad Pro</a></li>
        <li><a href="https://files.readme.io/67dfb63f7ede49e0fe4bd6a76d8c7485c9bedeaf2225ea050fc1776d89af6d7d-image.png" target="\_blank">Interstitial iPad</a></li>
        <li><a href="https://files.readme.io/7b16ea12877ce0e84db0c04adcfab015a4958ff016dfae0e38f12872c8464e9e-image.png" target="\_blank">Interstitial</a> </li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Half Interstitial
      </td>

      <td>
        1.30:1
      </td>

      <td>
        3:4
      </td>

      <td>
        Image
      </td>

      <td>
        <ul>
        <li><a href="https://files.readme.io/bf9fa3515ee90cbc1b3a54a95ce4dd6b71914387159ac8edd6a3bca313ead010-image.png" target="\_blank">Half Interstitial iPad Pro</a></li>
        <li><a href="https://files.readme.io/cc9b66978e7f24d593e640323c52cd0955f8a265ebc0f0cd7770628d9fe68659-image.png" target="\_blank">Half Interstitial iPad</a></li>
        <li><a href="https://files.readme.io/521962b5be7903641d38f13b21cedadba796c6e5142d3fce7ee1f4d7c1eb8ac2-image.png" target="\_blank">Half Interstitial</a> </li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Header
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>
        Title :parameters]\
        \{\
        , Message \{\
            "h-0": "C\* Title e",\
            "h-1": , Message pect Ratio",\
           Title : "Sample Image, Message \[75 Characters
      </td>
    </tr>

    <tr>
      <td>
        Footer
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Alert
      </td>

      <td>
        Native
      </td>

      <td>
        N/A
      </td>

      <td>
        N/A
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Cover
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Half Interstitial
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Interstitial
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

#### File Size Guidelines

* **Image**: Less than 500 kb.
* **Audio**: Less than 5 Mb.
* **Video**: Less than 50 Mb.

#### Message Character Limit

| Language | Title           | Message          |
| :------- | :-------------- | :--------------- |
| English  | 30              | 128              |
| Chinese  | 9 (Approximate) | 38 (Approximate) |

> 🚧 Image Cropping
>
> Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.\
> We scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then center-aligned.
>
> **Image Cropping does not apply for Image Interstitial template.**

> 🚧 Video Messages
>
> When adding video messages to In-App, ensure an audio track is always present.\
> If required, insert a blank audio track to the video.

## Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the *Ratings Template.*\
They can now create two types of rating templates for gaining feedback from their customers:

* User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
* NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance by navigating to the [NPS board](doc:nps-board) available under the *Boards* section.

The following images represent a sample *User Rating Popup* and *NPS popup* in a mobile app.

<Image title="Capture User Rating" alt={568} align="center" width="40% " border={true} src="https://files.readme.io/cc3f275-inapp.png">
  User Ratings Popup
</Image>

<Image title="Capture NPS" alt={542} align="center" width="40% " border={true} src="https://files.readme.io/3d18243-in-app_nps.png">
  NPS Popup
</Image>

Marketers get the complete flexibility to explicitly define the rating scale, style, shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments.

<Image title="Style Rating Template Elements" alt={2044} align="center" border={true} src="https://files.readme.io/d76e790-in_app_styles.png">
  In-App Editor Style
</Image>

Besides, additional styling, such as configuring the color for the message, question, background, and rating scale is also possible from the editor, as shown in the image above. The In-App notification text fields shown below can be personalized for every user based on specific user property or event property values. To learn more about tracking and monitoring user rating data, refer to [Analysing User Rating](doc:user-ratings).

<Image title="Compose In-App Message for Ratings Template" alt={1694} align="center" border={true} src="https://files.readme.io/ae7f02c-rate.png">
  Compose In-App Message
</Image>

### Follow-up Question Templates

A follow-up question to your ratings can provide more insights about the user experience. CleverTap provides the following Follow-up Question templates:

* NPS with Follow-up Question
* User Ratings with Follow-up Question

For example, after a user has submitted a rating on your app, you can ask follow-up questions such as *What did you like most about us?* and provide reply choices such as Variety, Prices, Quality, Customer Service, Delivery Process, and Website Usability. This can help you get more specific feedback to improve your product and services. Following is an image from the in-app editor: 

<Image alt="Short Keyword Choices" align="center" width="50% " border={true} src="https://files.readme.io/4766cd8-inapp_followup_nps.jpg">
  Short Keyword-Based Choices
</Image>

You can also list descriptive choices such as, *I like the available options and variety*, *I like the quality and durability of the products*, and so on. Following is an image from the in-app editor:

<Image alt="Long Sentence Choices" align="center" width="50% " border={true} src="https://files.readme.io/0decade-inapp_followup_qs_list.jpg">
  Descriptive Choices
</Image>

You can configure the follow-up question from the Web Popup editor with a short keyword-based grid (up to six choices) or a longer sentence-based list (up to four choices).

The label will be the text you want to display to your users. If you want to allow the user to select multiple choices, select *Allow multiple selections*.

<Image alt="Configure Follow-up Popup" align="center" width="80% " border={true} src="https://files.readme.io/fd33f9a-image_18.png">
  Configure Follow-up Popup
</Image>

> 📘 Note
>
> In the case of the User Ratings template, the *Notification Clicked* event is raised that records the user's clicks on the CTA buttons and the Close button

## Lead Generation Template

We know that a significant number of App users may remain anonymous. This poses a challenge to continue engaging with potential customers after they leave your App. A lead generation template can solve this issue.

Integrating a lead generation form into your App lets you get important customer details such as name, email address, phone number, etc. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication helps stay connected with your audience and opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with your App's CleverTap Lead Generation Template.

<Image alt="Sample Lead Generation Template" align="center" width="40% " border={true} src="https://files.readme.io/3658161-InApp_Lead_Gen_sample_window.png">
  Sample Lead Generation Template
</Image>

### Post Submit Actions

When a user submits information on your Lead Generation template:

* A *Notification Clicked* event is raised that records the click on the CTA. 

* A custom event named *Lead Submitted* records the details submitted by the user as of event properties. Following is a sample form image:

<Image alt="Form Submit Actions" align="center" width="50% " src="https://files.readme.io/0cae15f-Lead_Gen_Template_preview_with_fields.png">
  Form Submit Actions
</Image>

Following is a table that records the relevant properties for the fields displayed on the form:

| Submitted Event Properties | Sample Property Value               |
| :------------------------- | :---------------------------------- |
| First Name                 | John                                |
| Last Name                  | Smith                               |
| Email ID                   | [john@abc.com](mailto:john@abc.com) |
| Phone Number               | \+11234567890                       |
| Campaign ID                | 121110987654                        |
| Variant                    | wzrk\_default                       |

* The user profile is automatically updated with the submitted event properties. For example, the lead generation template can ask for additional details from an anonymous user, such as first name, last name, email, and phone number. His profile will be updated with these details, and now you can identify the user as *John Smith*.

### Lead Generation Template Variants

The following are the two types of Lead Generation templates:

* **Text**: You can create a text-only lead generation template to record user information. 
* **Image on Top**: You can add an image on the top to the lead generation template. 

Create the content to record information from your users. The following image displays a preview of the form:

<Image alt="Create Lead Generation Template" align="center" border={true} src="https://files.readme.io/035a137-lead_gen.png">
  Create Lead Generation Template
</Image>

Select the button style and card positions from the *Style* tab.

<Image alt="Style Lead Generation Elements" align="center" border={true} src="https://files.readme.io/06cbbe4-In-App_Template_Lead_Gen_Content_Editor.png">
  Style Lead Generation Elements
</Image>

Enter all the required information. 

* *Text*: Personalize the Title and Description. 
* *Media*: Add the image URL or upload an image. 
* *Input Fields*: You can add up to four input fields. Select input fields such as Name, Phone Number, Birthday, or Email Address for the template. 

<Image title="Lead Gen Template Input Fields.png" alt={1304} align="center" width="60% " border={true} src="https://files.readme.io/6a87857-Lead_Gen_Template_Input_Fields.png">
  Upto Four Input Fields 
</Image>

* *Buttons*: The *Close* button is selected by default. Add a button name such as *Submit* or *Upload*. 
* *Subtext*: Add subtext such as *privacy policy* to your lead generation template.

<Image title="Lead Gen Template SubText preview.png" alt="Add Subtext" align="center" width="55% " border={true} src="https://files.readme.io/bb6e1f2-Lead_Gen_Template_SubText_preview.png">
  Add Subtext
</Image>

The hyperlinked part must be closed between two asterisks. Add the URL where the user will be directed. You can also add a checkbox for your subtext.

<Image title="Lead Gen Template SubText.png" alt="Subtext and redirect URL" align="center" width="55% " border={true} src="https://files.readme.io/d740b86-Lead_Gen_Template_SubText.png">
  Subtext and redirect URL
</Image>

* *Acknowledgement*: You can show appreciation to your user by adding an Acknowledgement popup. Select the auto-close timer for the popup.

Select the button style and card positions from the *Style* tab.

<Image alt="Card Orientation" align="center" border={true} src="https://files.readme.io/92ac44f-In-App_Template_Types_Lead_Gen_Style.png">
  Card Orientation
</Image>

## Custom Templates

You can use the Custom HTML templates in the In-App editor to add more customization to the In-App messages with Javascript.\
Ensure that you select the *Include Javascript* box to add your custom Javascript. 

<Image title="Custom Template with HTML and Javascript" alt={1108} align="center" border={true} src="https://files.readme.io/5638bd2-in-app_journey_custom_HTML.png">
  Custom HTML and Actions
</Image>

> 📘 Create Interactive In-App Messages
>
> You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.
>
> Using the *Custom HTML* option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. 
>
> JavaScript-based campaigns are available for versions 3.5.0 and above.

### In-App Gamification Templates

Use CleverTap's out-of-the-box (OOTB) **Scratch the Card** and **Spin the Wheel** In-App message templates to engage users through interactive rewards, and can be easily customized using editable HTML settings.

> 📘 Private Beta
>
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

Gamification templates let you create interactive in-app experiences with minimal effort. With CleverTap, you can:

* Increase engagement and conversions through game-like interfaces
* Offer personalized rewards dynamically
* Fully customize the look and feel using the *Custom HTML Templates* tab

These templates include configurable variables for visuals, copy, animation, rewards, and behavior.

**Using the Templates**

1. Go to *Create In-App Message > Single Message*.
2. Select the **Custom HTML Templates** tab.
3. Select either:

   * [Spin the Wheel](doc:in-app-editor#spin-the-wheel-template)
   * [Scratch the Card](doc:in-app-editor#scratch-the-card-template)
4. Edit the settings and the Custom HTML to publish.

### Spin the Wheel Template

This template adds a fun, gamified interaction to your In-App by letting users spin a virtual wheel to unlock a discount, reward, or surprise offer directly within it. This interactive format helps boost engagement and click-through rates while creating a sense of excitement and urgency.

#### Interactive Elements

* Wheel animation with easing
* Pointer interaction + spin trigger
* Shimmer effect on reveal

<Image alt="Spin " align="center" width="25% " src="https://files.readme.io/bdfae57effccaa9fa2e956e102045ef43faf8762bbd7cced7826bd60c406f820-image.png">
  Spin the Wheel Template
</Image>

<details>

<summary><b>Expand to know more about the template.</b></summary>

### Use Case Examples

* Drive conversions during sales events or festivals with spin-to-win deals.
* Run promotional campaigns that reward users with random offers.
* Re-engage dormant users with a playful incentive.
* Launch loyalty or referral-based programs with interactive rewards.

### Template Customization Variables

This template allows you to tweak the appearance, messaging, and reward logic without the need to understand or modify the full code. Each setting explained here lets you control how the in-app experience looks and behaves, so you can launch high-converting, on-brand campaigns effortlessly. The following are the settings:

* `includeDmissButton`: Show or hide the close (X) button.
* `background`: Set the modal background color or gradient.
* `enableConfettiOnWin `: Toggle confetti animation after a win.
* `spinDurationSeconds`: Set how long the wheel spins (in seconds).
* `spinButton`: Customize the spin button’s text, color, background, and visibility.
* `claimButton`: Configure the claim button after spinning, text, color, background, and link (URL).
* `mainTitle`: Set the main headline text, font size, and color.
* `subtitle`: Set the subheading or description under the title, text, font size, and color.
* `copyInstruction`: Define the message color before and after users copy a reward code.
* `centerCircle`: Style the center hub of the wheel — color, border, and size.
* `rewards`: Define each reward option with the following:
  * `title`: Message shown on winning
  * `text`: Reward label (shown on wheel)
  * `value`: Copyable code
  * `subtitle`: Description/details
  * `probability`: Win chance
  * `colour`: Slice background color

### Configurable Settings in Template Explained

The following is a description of the customizable variables in CleverTap's Spin the Wheel gamification template.

#### includeDismissButton

Shows or hides the close (X) button on the modal. Set this to `false` if you want users to stay on the message until they take action.

```js
includeDismissButton: true,
```

#### background

Defines the background style of the spin screen. You can use a flat color or a gradient to match your campaign theme.

```js
background: "linear-gradient(180deg, #FF3672 0%, #8332F9 46.63%, #6708BC 84.62%, #4E15DD 100%)",
```

#### enableConfettiOnWin

Adds celebratory confetti after the wheel stops to boost delight. Use it to make wins feel exciting.

```js
enableConfettiOnWin: true,
```

#### spinDurationSeconds

Sets the number of seconds the wheel spins before revealing the reward. A longer duration adds suspense.

```js
spinDurationSeconds: 5,
```

#### spinButton

Customize the call-to-action (CTA) that users click to start the spin. Update the text to match your promotion (for example, "Try Your Luck", "Spin to Save").

```js
spinButton: {
  enabled: true,
  text: "Spin Now",
  background: "#ffffff",
  color: "#1d1d1d",
},
```

#### claimButton

Configure the button that appears after a spin. You can drive users to a landing page or apply a reward using a custom link.

```js
claimButton: {
  enabled: true,
  text: "Collect Now",
  background: "#F4357D",
  color: "#ffffff",
  url: "wzkr://thisleadstonowhere",
},
```

#### mainTitle

Control the headline at the top of the spin modal. Use this to grab attention with bold and fun messaging.

```js
mainTitle: {
  text: "🎉 Spin the Wheel <br>& Win Big!",
  fontSize: "24px",
  color: "#ffffff",
},
```

#### subtitle

Add supportive messaging under the title. This is where you reinforce the benefit (for example, savings, gifts, exclusives).

```js
subtitle: {
  text: "Your chance to score discounts, free gifts, and exclusive perks is just a spin away.",
  fontSize: "14px",
  color: "#e8f5ff",
},
```

#### copyInstruction

Set the message and color when users copy a reward code. You can highlight that the code was successfully copied.

```js
copyInstruction: {
  color: "#606060",
  copiedColor: "#F4357D",
},
```

#### centerCircle

Adjust the style of the central hub of the wheel (the spinner core). You can tweak the color, border, and size to match your brand.

```js
centerCircle: {
  color: "#914DFF",
  borderColor: "#2B2B2B33",
  borderWidth: 2,
  radius: 15,
},
```

#### rewards

It is the core of the experience. Each entry defines a reward slice on the wheel: what it says, the code it provides, a description, color, and the chance it gets selected. Check that the probabilities add up reasonably (they don’t need to equal 1).

```js
rewards: [
  {
    title: "Congrats! You just won a Promo Code!",
    text: "10% OFF",
    value: "DISCOUNT10",
    subtitle: "Use DISCOUNT10 at checkout to get 10% off your order. Valid through April 30.",
    probability: 0.15,
    colour: "#ffffff",
  },
  {
    title: "Congrats! You just won a Free Shipping!",
    text: "Free Shipping",
    value: "FREESHIP",
    subtitle: "Use FREESHIP at checkout to enjoy free shipping on your order. Valid through April 30.",
    probability: 0.15,
    colour: "#fc2b46",
  },
  // Add more rewards as needed
],
```

</details>

### Scratch the Card Template

This interactive template is designed to gamify the user experience by letting users "scratch" to reveal a reward, such as a coupon, discount, or points. The surprise element boosts engagement and reactivation rates while offering a delightful experience.

<Image alt="Scratch the Card Template" align="center" width="25% " src="https://files.readme.io/18e7bedad81f6ebb2df2ed18065f64f4e12e11a0c151fb59338b1b7fa60e19b3-image.png">
  Scratch the Card Template
</Image>

### Interactive Elements

* Scratch-to-reveal animation
* Shimmer effect on reward
* Confetti animation post-reveal
* Claim button redirect
* Copy reward to clipboard

<details>

<summary><b>Expand to know more about the template.</b></summary>

### Use Case Examples

* Engage users during festive or seasonal campaigns with surprise offers.
* Reactivate dormant users by giving them a chance to win a reward.
* Reward loyal customers with a fun, interactive coupon reveal.
* Launch a limited-time “scratch-to-win” contest to drive urgency and clicks.

### Template Customization Variables

This template allows you to tweak the appearance, messaging, and reward logic without the need to understand or modify the full code. Each setting explained here lets you control how the in-app experience looks and behaves, so you can launch high-converting, on-brand campaigns effortlessly. The following are the settings:

* `imageUrl`: URL of the image displayed above the scratch card (e.g., treasure chest).
* `includeDismissButton`: Toggle visibility of the close (X) button.
* `background`: Initial background color or gradient.
* `revealedBackground`: Background after scratching completes.
* `enableConfettiOnReveal`: Show celebratory confetti after reveal.
* `revealButton`: CTA before scratching. Customize text, color, and background.
* `claimButton`: CTA after reveal. Customize text, color, background, and destination URL.
* `mainTitle`: Controls headline text, color, font size, and optional text shadow.
* `subtitle`: Supports descriptive text below the title. Customize color and size.
* `rewards` – Define each potential reward with:
  * `title`: Message shown after reveal
  * `value`: Copyable code
  * `subtext`: Description or redemption details
  * `probability`: Chance of appearing

#### Config Snippets Explained

The following is a description of the customizable variables in CleverTap's *Scratch the Card* gamification template.

#### imageUrl

Sets the image shown above the scratch card.

```js
imageUrl: "https://.../scratch-the-card-chest.png",
```

#### includeDismissButton

Set to `false` if you want the user to complete the interaction.

```js
includeDismissButton: true,
```

#### background

Defines the initial background of the scratch card.

```js
background: "linear-gradient(180deg, #41F4BC 0%, #35ABFF 37.98%, #0060A5 100%)",
```

#### revealedBackground

Changes the background after the reward is revealed.

```js
revealedBackground: "linear-gradient(180deg, #41F4BC 0%, #35ABFF 100%)",
```

#### enableConfettiOnReveal

Celebratory animation to increase visual delight.

```js
enableConfettiOnReveal: true,
```

#### revealButton

Customize the call-to-action before the reward is shown.

```js
revealButton: {
  enabled: true,
  text: "Reveal My Prize",
  background: "#ffffff",
  color: "#1d1d1d",
},
```

#### claimButton

Configure how users can claim or use the reward.

```js
claimButton: {
  enabled: true,
  text: "Claim",
  background: "linear-gradient(180deg, #A4FFE4 -0.8%, #41F2BE 99.2%)",
  color: "#000000",
  url: "wzkr://thisleadstonowhere"
},
```

#### mainTitle

Control the primary heading inside the card.

```js
mainTitle: {
  text: "Scratch & Win: <br>A Surprise Awaits!",
  fontSize: "24px",
  color: "#ffffff",
  textShadow: "0 2px 4px rgba(0, 0, 0, 0.3)",
},
```

#### subtitle

Supplementary text below the title.

```js
subtitle: {
  text: "Feeling lucky? Scratch the card to reveal your reward...",
  fontSize: "14px",
  color: "#e8f5ff",
},
```

#### rewards

Each reward entry has:

```js
rewards: [
  {
    title: "Congrats! You just won a Promo Code!",
    value: "DISCOUNT10",
    subtext: "Use DISCOUNT10 at checkout...",
    probability: 0.45,
  },
  // Add more reward options here
],
```

</details>

## Best Practices

* Keep reward probabilities realistic; the total does **not** need to equal 1.
* Use high-contrast text over bright gradients for readability.
* Add expiration dates in reward subtext to create urgency.
* Use consistent reward identifiers across campaigns for tracking.

# Time to Live (TTL)

You can configure the number of days (or hours) to keep the message on the user's device by setting the *time to live*.

<Image title="Configure Time to Live for In-App Message" alt={630} align="center" border={true} src="https://files.readme.io/35148df-in-app_time_to_live.png">
  Time to Live for a Message
</Image>

The TTL can range from 1 day to 365 days. The default value for TTL is two days. The message on the user's device stays there for the specified TTL, after which it is automatically removed.

> 🚧 Choosing the Right TTL
>
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

# In-App Editor

Use the In-App editor to craft your In-app campaign with the desired messaging and styling best suited for your business. You can choose from a range of In-App templates. Alternatively, you can also use the Custom HTML option to build your own campaign.

The elements of the editor vary based on the type of template you select for creating your In-App campaign.

The following image represents the *Content with image notifications* template editor. 

<Image title="Basic Editor" alt={1206} align="center" width="80%" border={true} src="https://files.readme.io/6b590c3-in-app_editor.png">
  In-App Editor for Content with Image notifications
</Image>

At a high level, the In-App editor has the following two primary sections: *Content* and *Style*.

### Content

The Content section allows you to define your In-App message's overall text and visual content. Use this section to create engaging, and personalized In-App messages by entering enticing Title and Message. To [personalize](https://docs.clevertap.com/docs/personalize-message-inapp) the message, click the **Personalization (@)**  icon in the *Title* and *Description* fields.

Using the *Insert image* option, you can upload the desired image to make your In-App campaign visually appealing when the app is in Portrait or Landscape mode.

You can choose to add the same image with different form factors or completely different images to give a unique experience on portrait and landscape.

Additionally, you can add up to two CTAs and configure their On Click Action as per your requirement. You can use the following three types of action buttons:

* Close notification: It closes the notification after a tap. 
* Open URL: A special type of CTA that enables the user to open a deep link for Android or iOS.
* Custom key-value pairs: The key-value pairs send back custom data when a user clicks the in-app button

You can also configure the number of days (or hours) to keep the In-App message on the user's device by setting the Message Time to Live field as per your use case. 

> 📘 Image Interstitial Template Exception
>
> The elements of the In-App editor for the *Image only notifications* templates are similar to those of the  *Content with Image notifications* templates except for the *Title* and *Message* fields.

### Style

The Style section enables you to customize the appearance of your In-App message elements, such as title color, background color, message color, button text color, and so on. 

Customize the overall In-App message elements as per your brand style guidelines to make them visually appealing.

<Image title="Define Elements Style" alt={963} align="center" border={true} src="https://files.readme.io/c9edbb1-In-App_Message.png">
  Style Elements from Editor
</Image>

> 🚧 Typeform and Character Limit
>
> We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.
>
> The character limit for a message in English is 30 for the title and 128 for the message.\
> The character limit for a message in Chinese is 9 for the title and 38 for the message.
