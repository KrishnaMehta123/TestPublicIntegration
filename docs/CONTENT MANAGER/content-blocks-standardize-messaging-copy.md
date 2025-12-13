---
title: Content Blocks - Standardize Messaging
excerpt: Learn how to reuse content and standardize your messaging with content blocks.
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

A Content Block is a reusable part of content that can be used across different campaigns. It helps maintain a consistent experience for users as they view a consistent branding tone and colors across your messaging. This messaging can include text, images, or calls to action (CTAs) buttons that you can standardize across messages. Using standard messaging, marketers can maintain a clear tone and style, building trust and consistency in brand communications.

> 📘 Private Beta
>
> This feature is currently a Private Beta Release. If you want access to it, contact your CSM.

Content Blocks also allow marketers to reuse the same content for different campaigns, saving time and effort while matching the brand’s identity. For example, a Content Block can serve as a footer with clickable social media icons for users to follow the brand. Marketers can easily add or remove social media links as needed in a footer, making this change dynamically effective across all campaigns that use this Content Block. For example, if you are a travel app sending messages to users, an update to an email footer about an updated Instagram account can be repeated across footers sent in other campaigns.\`

> 📘 Supported Channels
>
> Currently, you can use a content block for [Email campaigns](doc:create-message-email) only. However, only Text Contet Block is supported for [AMP for Email](https://docs.clevertap.com/docs/ampforemail). You can stay tuned to our [Release Notes](https://docs.clevertap.com/docs/whats-new)   and [Changelog](https://developer.clevertap.com/docs/changelog)  about frequent updates and enhancements.

<Image alt="Standardization with Content Blocks" align="center" border={true} src="https://files.readme.io/89622623ff70128b43826e2e2c67459119524f19f1a5bd1f1aef4b07c678d388-image.png">
  Footer Standardization with Content Blocks
</Image>

# Content Block Types

There are two types of content blocks:

* Text Content Block - Simple text-based messages mainly to communicate information, updates and so on.
* HTML Content Block -  Engaging, dynamic messages to upsell and quickly engage the users.

 You can select a content block based on your messaging requirements, whether you want to send a plain text message or an engaging, colorful message.

## Text Content Block

This is a Text-based Content Block you can reuse for your messaging requirements. It is useful when you want to create a message quickly. The [Inline personalization](https://docs.clevertap.com/docs/personalize-message-all#inline-personalization) includes only profile personalization.

> 📘 Text Block Specifications
>
> Currently, we support up to 500 characters in a content block.

Here is a sample of a personalized Text Content Block that encourages the user to upgrade the plan for an OTT app. The [Conditional Tags](doc:liquid-tags#conditional-tags) help deliver the message based on the current subscription plan of the user:

<Image alt="Sample Text Content Block" align="center" border={true} src="https://files.readme.io/42281df9b000b3b1bc70ec90ad727c7cce69bf65cb887f408478cc9e519b430a-image.png">
   Sample Content Block - Text
</Image>

## HTML Content Block

The HTML Content Block allows you to create visually appealing and dynamic messages, allowing you to import and paste your HTML code. The HTML code helps design and customize your message’s layout, style, and interactivity, helping you deliver a more engaging experience for your audience.

Here is a sample HTML Content Block that nudges the user to upgrade the plan for an OTT app. The [Conditional Tags](doc:liquid-tags#conditional-tags) help deliver the message based on the current subscription plan of the user:  

<Image alt="Sample HTML Content Block" align="center" border={true} src="https://files.readme.io/c94ed28109426e3a91754c428c8b474d8e24cb16ed4ad6894fdf156694e645db-image.png">
  Sample Content Block -  HTML
</Image>

# Create Content Blocks

You can create Content Blocks from the CleverTap Dashboard. 

> 📘 Content Blocks Via API
>
> You can also create and manage your Content Blocks via the CleverTap [Content Blocks API](docs:content-blocks-api) when you want to update or create Content Blocks at scale.

Follow the steps to create a content block:

1. Go to *Content Manager* > *Content Blocks*. 

<Image alt="Create a Content Block" align="center" border={true} src="https://files.readme.io/a9f13e16ffcf9b9f8561cc02a6a5744fb167a2be2704c902b6b29a4ea98c6292-image.png">
  Create a Content Block
</Image>

2. Click **New** and select the type of *Content Block* [Content Block](doc:content-blocks#content-block-types). 
3. Select the type of Content Block, that is, Text or HTML.

<Image alt="Content Block Editor" align="center" border={true} src="https://files.readme.io/a94c81ea360432f27cbdaafe8bd37214d191265536bc33cca545d3ece87e433a-image.png">
  Content Block Editor
</Image>

3. From the editor, click **\{\{}}**  to use [inline personalization](https://docs.clevertap.com/docs/personalize-message-all#inline-personalization) and [Conditional Tags](https://docs.clevertap.com/docs/liquid-tags) to personalize the *Content Block*. 
4. Click **Preview** to preview the content block.

<Image alt="Preview content block" align="center" border={true} src="https://files.readme.io/d4862eae25783ab2d1facd6210a58e93c59bed9a9f2c8cc864681ff955e80b85-image.png">
  Preview Content Block
</Image>

4. Click **Save** to save your *Content Block*. 
5. Enter a name for your Content Block.

> 📘 Content Block Name
>
> Content Block names can include letters, numbers (0-9), underscores (\_), periods (.), hyphens (-), and spaces. The name must begin with a letter. Additionally, the Content Block name must be unique.

4. From the list of labels, select the appropriate labels to organize and identify your content block. 
5. Click **Done**. 

## Preview Content Block

You can preview the Content Blocks from the Content Blocks page or during the Content Block creation process.  

To preview a content block:

1. Go to *Content Manager* > *Content Blocks*. 
2. Select a Content Block and double-click to preview it. 

The content block displays information such as name, label, and so on. 

<Image alt="Content Block Preview" align="center" border={true} src="https://files.readme.io/9b4a67b0830157d3afc2ac1c06ff6067005ae32c7642cdba3a9d2a7f312428ed-image.png">
  Content Block Preview
</Image>

# Use Content Block (in a campaign)

Currently, you can use a content block only in [Email campaigns](doc:create-message-email) to standardize and reuse content in email messaging. Follow these steps to use a content block:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the Email messaging channel—the Campaign page displays.
4. From the *What* section on the Campaign page, select the message type and click **Go To Editor**. 
5. Select any template from the *Basic Templates* tab. 
6. In the editor, enter *\{\{*  to add the content block.  Select the content block from the list. 

<Image alt="Add a Content Block" align="center" border={true} src="https://files.readme.io/00b42b58ae892077e4ed213d986414a5d21c8658542e9e833b968f88ead7647d-image.png">
  Add a Content Block 
</Image>

7. Continue with the campaign creation flow. 

## Personalization in Liquid Tags

When creating a campaign, you can further personalize content using content blocks with the help of Liquid Tag personalization. For example, you can email users tempting offers based on their food preferences. Using Liquid Tags, you can add multiple Content Blocks for each cuisine to ensure that end users receive the relevant menu options and images in their emails. Follow these steps to add liquid tags to content blocks:

1. Select the message type from the *What* section on the Campaign page and click **Go To Editor**. 
2. Select any *drag and drop* template from the *Basic Templates* tab.
3. Drag and drop a text block and double-click it to display the formatting options:
4. Select *Customize with Liquid tags* from the *More* list in the toolbar.  

<Image alt="Customize Text Block with Liquid Tags" align="center" border={true} src="https://files.readme.io/46c8e6115ee531ecb87300772d00a449df8712559463a73cb4f2456165bbf202-image.png">
  Customize Text Block Liquid Tags
</Image>

5. Click the **\{\{}}** icon and select the required *Content Blocks*. 

<Image alt="Personalization list with {{}}" align="center" border={true} src="https://files.readme.io/c3de482967c79bbe16b5123abf33a246e77b8d3b32349f5e8fa886d16946d49b-image.png">
  Personalization list with \{\{}}
</Image>

> 📘 Enhance Personalization
>
> You can combine Content Blocks with additional personalization options provided by Clevertap. Click the **\{\{}}** icon to explore more personalization for your messaging.

6. Add conditions based on your requirements using Liquid Tags.

<Image alt="Add multiple content blocks with liquid tags" align="center" border={true} src="https://files.readme.io/0376c188ca78af9d7ea171932f960b4361d46607711b1836d41cced236870896-image.png">
  Add Multiple Content Blocks with Liquid Tags
</Image>

7. After adding the content, click **Add** to add the Content Block. 

Preview the message and verify the content before sending it. The content will be displayed. 

<Image alt="Content Block Display in Email" align="center" border={true} src="https://files.readme.io/937f04c2ee11a2238cc5fae846461244065adf25f06628cfc2f4d78577d786b0-image.png">
   Content Block Rendered
</Image>

# Content Block Considerations

Check for the following considerations to optimally use Content Blocks in your messaging campaigns.

## Content Block Specification

Before creating content blocks, carefully review the specifications and considerations.

| Content Block Element | Specification                                                                                                                                                                             |
| :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name/Rename           | Names can include letters, numbers (0-9), underscores (\_), periods (.), hyphens (-), and spaces. The name must begin with a letter. Additionally, the content block name must be unique. |
| Content Size          | Maximum of 50kB (kilobyte) for HTML Content Block. Up to 500 characters for Text Content Block.                                                                                           |
| Supported Channels    | Content Blocks can currently be used only in the email channel.                                                                                                                           |
| Deletion              | Deleting content blocks is currently not supported.                                                                                                                                       |

### Nesting Considerations

The following are considerations when nesting content blocks:

* You can nest multiple content blocks inside a content block. However, a nested content block cannot be nested inside another content block.
* Text content blocks can be nested within each other, as can HTML content blocks. However, HTML content blocks cannot be nested within text content blocks.
* A nested content block cannot be renamed. 
* Any edits to the main or child content block will reflect in the nested content block.

## Supported Personalization

Before using Content Blocks, refer to these essential guidelines for supported personalization. These help you understand which personalization types are supported and how to use them effectively in your campaigns.

| Personalization Type | Supported? | Description                                                                                                                                                                                      |
| :------------------- | :--------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Profile              | Yes        | You can use profile attributes                                                                                                                                                                   |
| Conditional Tags     | Yes        | You can create a *write once use multiple times* message by adding conditional variations based on user attributes or behavior. For more information, see [Liquid Tags](doc:liquid-tags).        |
| Event                | Yes        | You can manually add event personalization tags. These automatically resolve based on the associated user event data. Event Personalization for Content Blocks is currently in **Private Beta**. |
| Linked Content       | No         | -                                                                                                                                                                                                |
| Catalog Send-Time    | No         | -                                                                                                                                                                                                |
| Campaign             | No         | -                                                                                                                                                                                                |

### Using Event Personalization

To add event-based personalization in an email Content Block:

1. Open the Content Block you want to edit (HTML or Text).
2. Type the event tag manually, ensuring the correct syntax is used.
3. Preview or test send to verify the tag.
4. Publish the campaign.

#### Syntax:

Tags must be typed exactly as required. Use the following format to insert event-based values:

```liquid
{{Event[“CT Source“] | default:”default”}}
{{Event.experiment | default:”default”}} 
```

CleverTap validates that the Content Block’s event matches the event used in the campaign's trigger criteria (Who section). Any mismatches are automatically blocked during campaign publishing.

#### Example

Suppose your campaign uses both profile and event-based personalization. The following tags personalize the user’s name and the series they watched.

```text
Hello {{ Profile.name | default: "User" }},
You watched {{ Event.SeriesName | default: "your favorite series" }}
```

If either property is missing in the user’s data, CleverTap automatically uses the default values so that the message still displays correctly and does not break personalization. The following is the rendered output if defaults are used:

```
Hello User,  
You watched your favorite series
```

This ensures your message always appears complete, even if some event properties are unavailable.

> ⚠️ Note
>
> * **Event matching:** Check that the event used for personalization in the Content Block is the same as the event selected in the trigger criteria of the event-triggered campaign.
> * **Nested blocks:** The event used in a nested Content Block must be the same as the event in the parent Content Block. For example, if `App Launched` is used in the parent block, it must also be used in the nested block.
> * **Availability:** This feature is currently supported only for Campaigns.
> * **Validation:** While typing in the email editor, event validation ensures that only compatible Content Blocks appear. For example, if you type a tag in the email body:
>   * Content Blocks with matching event personalization appear in the dropdown.
>   * Content Blocks with no personalization also appear in the dropdown.

## Content Block Operations

You can edit, rename, and label the Content Blocks from the Content Block card. Follow these steps to manage the content blocks:

1. Go to *Content Manager* > *Content Blocks*.
2. Click the **Content Block card** to perform various operations.

<Image alt="Content Block Operations" align="center" border={true} src="https://files.readme.io/31c51346a270c91bd031646d40244881b4ba45b6f1db097b431bf0454747bdd2-image.png">
  Content Block Operations
</Image>

3. Select from the following options:

* *Edit*: Select to edit the content block. 
* *Rename*: Select to rename the folder.
* *Label*: Select to apply a label to the content block. It will help further identify or search the Content Block.

# Use Cases for Content Block

Content Blocks can be used in various ways to enhance communication across campaigns. From displaying personalized offers to embedding interactive elements such as forms or buttons, these versatile blocks ensure your messages are engaging and consistent. The following are some use cases where Content Blocks can effectively streamline your marketing efforts.

## Multi-Language Support

Here is a simple example of personalization with a liquid tag for multi-language support. An OTT app offers subscription or membership plans tailored to the user's region and displayed in their preferred language. 

```liquid Content Block using Liqud Tags

{% if Profile.PREFERED_LANGUAGE == "Spanish" %}
  Elige tu plan: Plan Básico por €5/mes o Plan Premium por €15/mes.
{% elsif Profile.PREFERED_LANGUAGE == "Italian" %}
  Scegli il tuo piano: Piano Base per €5/mese o Piano Premium per €15/mese.
{% else %}
  Choose your plan: Basic Plan for $5/month or Premium Plan for $15/month.
{% endif %}

```

If the user's preferred language is Spanish, the greeting will appear in Spanish.  

```text Output - Spanish
Elige tu plan: Plan Básico por €5/mes o Plan Premium por €15/mes.
```

The greeting will appear in English if the user prefers English.

```text Output - English
Choose your plan: Basic Plan for $5/month or Premium Plan for $15/month.
```

## Update Footer

You can change the footer in a running campaign to reflect new content. For example, a footer displays icons for various social media such as *TikTok*, *Facebook*, *WhatsApp*, and *Instagram*. You can change the footer in the outgoing messages by removing or adding icons in this footer. Once you change the icons, the change will be reflected in all outgoing messaging.

<Image alt="HTML Code for Footer" align="center" border={true} src="https://files.readme.io/669b9b25ec2da9c3e5360bc694538dc3d9098be24596dbadc230a617ef54f845-HTML_code_for_footer.jpg">
  HTML Code for Footer
</Image>

You can edit the HTML to remove or add an icon. 

<Image alt="Footer Content Block with X and Facebook" align="center" border={true} src="https://files.readme.io/c9b7536b14f5594b55b4fc9cb7782bf2af37234cdb8ff74b03bfe9c40e4ab633-2024-11-11_18-20-20.jpg">
  Footer without Instagram
</Image>

The following is an example of an updated footer. Once the footer is updated, all campaigns using this Content Block will display the updated icons in the outgoing messages.

<Image alt="Footer content block with X , FB , and Google" align="center" border={true} src="https://files.readme.io/72e98e0eba6fdbfbe66b8e3dff9af113e891ab6e97bae511ccd2ec11a79af57b-2024-11-11_18-16-47.jpg">
  Footer with Instagram
</Image>
