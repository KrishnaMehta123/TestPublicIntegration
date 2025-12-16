---
title: Designer Agent
excerpt: Learn how to generate Push Notification images with the Designer Agent.
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

**Designer Agent** helps you instantly create, edit, or refine images for your Push Notification campaign, all within CleverTap, without the need for external design tools. It combines advanced AI capabilities with your Brand Kit to generate on-brand, campaign-ready visuals quickly and efficiently. This makes it easier for teams to design creative images directly in the campaign editor, reducing dependency on design teams and accelerating go-to-market time.

> 📘 Private Beta
>
> This feature is released in Private Beta and is enabled for select customers only. To enable this feature, contact your Customer Success Manager.
>
> Designer Agent is available in Push Notifications, for accounts where push templates are enabled. This feature will soon be expanded to other messaging channels.

# How Designer Agent Works

The feature is embedded within the Push Notification editor, next to image upload fields, such as **Expanded Image** or **Large Icon**. You can use it to:

* Create new images from scratch using descriptive prompts.
* Edit or refine existing visuals with prompts.

The Designer Agent automatically applies your Brand Kit to ensure every generated image aligns with your brand colors, styles, and tone.

<Image align="center" alt="AI Image Generator for Push Notification" border={true} caption="Designer Agent for Push Notification" src="https://files.readme.io/74795935df940693c38e96dff8d6cb0cd01e89ed293312891efb74866c2cdd25-AI_Image_Generator_for_Push_Campaign.png" />

<Callout icon="📘" theme="info">
  **Brand Kit Application**

  The latest created Brand Kit is automatically selected and applied to your image, even if you don’t manually choose one.

  If only one Brand Kit exists, it is applied by default. If multiple kits are available, the most recently created one is auto-selected.
</Callout>

## Generate Image Using Prompt

The Designer Agent utilizes your prompt and Brand Kit settings to create visuals that align with your campaign’s theme. By providing clear and detailed descriptions of what you need, you can quickly create on-brand images tailored to your requirements.

To generate an image using prompts:

1. Open your **Push Notification** campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png)Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png)Generate with AI**  for the _Rich media_ field.
3. Click **Generate Image**. The _Generate Image_ window opens.
4. Describe the image you want in the prompt field at the bottom. For example, refer to the below sample image for an OTT platform to promote an upcoming Premier League football match:

<Image align="center" border={true} caption="Image Generated using Text to Image Option" src="https://files.readme.io/3686d1c1d24a170e204e82e473e7a1cc1fc4e5a4ce2cfdf4d8df292c81af7e1e-image.png" />

5. Click ![](https://files.readme.io/bdbfd957c9ccc6dff7284d71450e4414281705ac5d8337c238198a6d7cc896ee-Image_Settings_Icon.png) to select the _File format_ (JPEG or PNG). The Ratio/Size (that is, 1:1) is auto-selected and non-editable. The aspect ratio and size are automatically aligned with Push OS specifications (for example, 1:1 for Large Icon and 3:2 for Expanded Image) to ensure compatibility.

<Image align="center" border={true} caption="Image Settings" src="https://files.readme.io/de22a44d0c1d4fe360efac8ee163fa4677f6dd663e01ab39bdf324a6fc30a98d-image.png" />

6. Click **Primary Kit** to view your brand’s style, button colors, brand colors, and so on, for your image. Click **Apply**. Click **Secondary Kit** to configure a custom kit for the current image. For more information on setting it up, refer to [Brand Kits](https://docs.clevertap.com/docs/brand-kit) .

<Image align="center" border={true} caption="Brand Kits" src="https://files.readme.io/a5b3f89da995732024b828934b34a14f56a8567b828d1fd984541e3834a71ff3-image.png" />

<Callout icon="📘" theme="info">
  **Brand Kits**

  * Brand Kit names reflect the Brand Kits configured in your account.
  * If a brand kit is locked, it cannot be edited within the campaign flow.
  * Any changes made to BrandKit through campaign flow only apply to **that thread**.
  * If a prompt conflicts with your Brand Kit’s defined elements, such as brand colors, button styles, or tone, the AI will prioritize the Brand Kit settings. For example, If your Brand Kit specifies yellow and green as primary brand colors and the prompt requests purple, the generated image will use purple, with yellow and green as the dominant colors.

  This ensures consistent, on-brand visuals across all AI-generated assets, regardless of the prompt details. For more information on setting up and using brand kits, refer to <Anchor label="Brand Kit" target="_blank" href="https://docs.clevertap.com/docs/brand-kit">Brand Kit</Anchor>.
</Callout>

7. Click **Generate**. Review the generated image and click **Insert** to add the image to your campaign.
8. After inserting the image, you can edit or refine the image directly within the editor:
   * Enter follow-up prompts in the same chat thread to refine the image.
   * To edit an existing image, go to the Message Editor, click **Upload**, and select the image. Click ![](https://files.readme.io/3dd08bfdc757b30950b16c701f01b8970b5ddec566c161e93cb3c1081ee73e60-Edit_icon.png) and describe the change you want to make (for example, Change CTA text from "Watch Live" to “Watch Now”). Each refinement creates a new version saved in your Threads history, allowing you to revisit or reuse past iterations.

<Image align="center" border={true} caption="Edit Generated Image" src="https://files.readme.io/56e6f65f6ee6b65114011d2bd974fc24f168fc111754f3e6141a771a6a0773d1-2025-12-15_17-34-36_2.gif" />

> 📘 Why detailed prompts matter?
>
> The Designer Agent relies on the clarity of your description to produce accurate, high-quality visuals. The more specific you are about theme, colors, layout, or mood, the better the output will align with your campaign goals. Include contextual details (like event name, offer type, or brand tone) for best results. For more information, refer [Generate On-Brand Images with Effective Prompts](https://docs.clevertap.com/docs/effective-prompts-for-ai-designer-agent).

## Generate Using Reference Image

To generate an image using a reference image, perform the following steps:

1. Open your Push Notification campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png)Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png)Generate with AI**  for the _Rich media_ field.
3. Click **Generate Image**. The Generate Image window opens.
4. Click ![](https://files.readme.io/7c39b5787600b7ac069bc4f2f78a6f3f0304bd3c3cc04eef082aa945c714fdf8-Plus_Icon.png) to select an existing banner from CMS.

<Image align="center" alt="Generate Image Using Reference Image" border={true} caption="Generate Image Using Reference Image" src="https://files.readme.io/e321224127b1de1ff8feae54767ad33433f1ef8bf704571e3418a72d4f777fc2-2025-11-28_14-49-17_1.gif" />

5. You can also browse and select an image from your AI-generated images folder in the CMS. Click **Upload** and **Edit**.

<Image align="center" alt="Edit Image" border={true} caption="Edit Image" src="https://files.readme.io/feba778dbafdf0bb11dd24ae8038992f84b7b7f97547fff534d2152026ac4d7c-image.png" />

6. In the prompt field, describe the updates or new campaign details you want to apply.  Once you select an image, you can:
   * **Change text**: For example, update offer amounts, taglines, or call-to-action text.
   * **Change background**: Modify colors, replace backgrounds, or adjust contrast for seasonal themes.
   * **Replace visual elements**: Swap product photos, icons, or logos.
   * **Adjust layout**: Realign elements, add or remove visual sections, or reposition branding.
   * **Add highlights or effects**: Emphasize key offers or add simple visual effects, such as a glow or drop shadows. For example, if you want to use 30% Off banner as a reference and update it for Holi with bright color accents and festive treats.
7. Click **Brand Kit** to view or switch to another kit if needed.
8. Click **Generate**. It analyzes your reference image and applies the prompt instructions you provide. A new image is generated that maintains the layout and design consistency of your requirements.
9. Review the generated image and click **Insert** to add it to your campaign.

## Use Secondary Image to Update Primary Image

Upload an existing image as a reference. Clever.AI uses its layout, style, and color palette to create a fresh visual. You can use this method when you want to: refresh a past campaign creative, maintain a consistent look and feel across offers, and make quick adaptations for regional or seasonal variations.

This helps with the following:

* Retains brand tone and design balance.
* Reduces turnaround for variant creation.

To generate an image using this method, perform the following steps:

1. Open your Push Notification campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png)Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png)Generate with AI**  for the _Rich media_ field.
3. Click **Generate Image**. The Generate Image window opens.
4. Click ![](https://files.readme.io/7c39b5787600b7ac069bc4f2f78a6f3f0304bd3c3cc04eef082aa945c714fdf8-Plus_Icon.png) to upload the following.
   * Primary Image: The creative you want to update.
   * Secondary Image: The visual reference that defines your desired color tone, layout, or design.
5. In the prompt field, describe how you want to adapt or align the primary image to match the secondary one.

<Image align="center" alt="Use Secondary Image to Update Primary Image" border={true} caption="Use Secondary Image to Update Primary Image" src="https://files.readme.io/879aae0c5629396861b0d7d09d4684d616f8ca0ab45eac0938ddc2a6d5ab87b1-2025-11-23_17-21-52_1.gif" />

Refer to the following example prompt:

> Use the Christmas Sale banner as the primary image and the Diwali Sale banner as the secondary reference.  
> Match the Christmas image’s composition, color palette, and text placement to the Diwali banner’s warm, festive layout.  
> Replace the background gradient with rich gold tones, add warm lighting, and include subtle decorative elements like stars or ribbons.  
> Headline: “Celebrate the Season with Style”  
> Subheadline: “Up to 50% Off on Fashion & Accessories.”  
> CTA: “Shop Now” in a red or gold rounded button.

6. Click **Brand Kit** to apply your brand’s predefined colors, tones, and layout.
7. Click **Generate**. It analyzes both images and adjusts the primary to match the secondary in tone, layout, and design style.
8. Review the generated image in the preview panel and click **Insert** to add it to your campaign. To make refinements, use follow-up prompts.

# Manage Generated Images

All AI Generated images can be accessed via [Threads](https://docs.clevertap.com/docs/designer-agent#threads)  and [AI Generated Images Folder](https://docs.clevertap.com/docs/designer-agent#ai-generated-images-folder).

## Threads

Once you start generating images, it automatically saves your sessions under the ![](https://files.readme.io/a973e47e78d9cb32bf7c2372bc46d90fdb6f8eb16dd6ebaa77a63c2b385438c8-Threads_icon.png) tab. Each session is stored as a **thread**, which captures your prompts, refinements, and generated outputs, helping you resume from where you left off without losing context.

<Image align="center" border={false} caption="All Threads" src="https://files.readme.io/82ae5a722aeb6d03bf7f543afdbab7666281ece777de4920eb08b689e9ac7987-image.png" />

### How Threads Work

Threads are scoped to your **Account**, **Agent**, and **User**, ensuring that your history remains personalized and relevant. All threads for your account appear in the **All Threads** popup. A thread becomes the context for your next generation, allowing Clever.AI to remember your prior visual style, brand preferences, or edits. They are not tied to specific campaigns; they persist across multiple campaigns for seamless continuity.

If multiple users from the same account use AI tools:

* Each user sees only their own threads and the latest image generation session that they have participated in.
* Threads are separate for Segmentation, Analytics, Designer Agent, and Copywriter Agent, even under the same account.

### Manage Threads

From the **All Threads** view, you can:

* Reopen an older thread to continue generating or editing images using the same context.
* Review and compare multiple image versions created during that session.
* Restore or reuse previously generated images without regenerating them.

<Callout icon="💡" theme="default">
  ### **Tip**

  For subsequent edits, you need not restart a session. You can type your next instruction directly in the chat. For example: _“Make the background blue and add a 50% OFF badge in the corner.”_ The AI will update the existing image while maintaining your brand styling and earlier visual tone.
</Callout>

## AI Generated Images Folder

All AI-generated images are automatically stored in your _CMS_, under the **AI Generated Images** folder for your account. This allows you to reuse, manage, or download previously created visuals without needing to regenerate them.

<Image align="center" alt="AI Generated Images Folder" border={true} caption="AI Generated Images Folder" src="https://files.readme.io/c7bd10e224147810623d972c5b4c9854c17e9d267de86e3a17db5fa22d64eeaa-brand.png" />

# Best Practices for Writing Prompts

The following best practices will help you with writing more detailed prompts:

* Be **specific** and include theme, tone, and visual intent.  
  _Example: “Create a modern app promo banner with minimalist icons.”_
* Add **context**; specify what the image is for (offer, product launch, festival).
* Use your **brand kit** for visual alignment.
* Don’t write one-liners. A prompt like “banner” or “sale” gives the AI too little to work with — resulting in generic, off-brand images.
* Describe the scene, emotion, and layout you want to see.  
  _Example: “Create a 1:1 Push Notification image for a festive Diwali campaign with maroon and gold tones, decorative lamps, and a bold ‘Shop Now’ button in brand colors.”_
* Review and refine your prompt if the output doesn’t match your intent.

The Designer Agent relies on the clarity of your description to produce accurate, high-quality visuals. The more specific you are about theme, colors, layout, and mood, the better the output aligns with your campaign goals.

For more information, refer to [Generate On-Brand Images with Effective Prompts](https://docs.clevertap.com/docs/effective-prompts-for-ai-designer-agent).

# FAQs

### Does CleverTap store or reuse the images I generate?

Yes, the images you generate are stored securely within your account’s CMS so you can access them later. However, CleverTap does not reuse, resell, or redistribute your images in any way. The generated output remains unique to your prompt and campaign inputs. Images are stored only for your reuse and are never shared across accounts.

### Who owns the images I generate?

You retain full ownership of all images generated using the Designer Agent. CleverTap does not claim any intellectual property rights over generated content.

### How is my data used and shared with Nano Banana AI?

CleverTap’s Designer Agent uses Nano Banana AI to create images. Your input data is transmitted securely to Nano Banana’s API for generation and returned to CleverTap for display in your campaign. Your data is never used to train Nano Banana AI models. Nano Banana deletes all input data within 30 days, in accordance with their Terms of Use. CleverTap sends only the necessary input to generate your requested image, including your text prompt, and, if applicable, metadata such as brand kit colors or style selections. No personally identifiable information (PII) about you or your users is shared unless you explicitly include it in your prompt. The generated image and related metadata are stored securely within your CleverTap account.

<Callout icon="💡" theme="default">
  **Best Practice**

  All generated materials should be reviewed by your internal brand and legal teams before use in public campaigns.

  Avoid including any personal or confidential information in AI prompts. Keep descriptions focused on creative intent.
</Callout>

### Can I paste links or URLs (for example, Figma or design file links) in the prompt?

No. The Designer Agent does not support links or URLs pasted in the prompt, as it does not fetch or render content from external URLs.

### What aspect ratios are supported?

Aspect ratios are pre-selected and non-editable based on your campaign channel (for example, 3:2 for Expanded image and 1:1 for Large icon).

### Can I edit the generated image after inserting it?

Yes. You can prompt it to “change background,” “update offer text,” “replace image”, and so on. These edits happen directly in the chat interface.

### What image formats are supported?

The generator currently supports **JPEG** and **PNG** formats.

### What if I don't want any user to override my brand guidelines?

You can lock your Brand Kit from the BrandKit section.

### What if I want to make sure no one overrides my brand guidelines?

Brand guidelines are automatically applied to every generated image, whether your Brand Kit is locked or not. However, if you want to prevent anyone from changing or overriding these settings during image generation, you can lock the Brand Kit from the BrandKit section. When locked, the selected kit’s styles (colors, buttons, etc.) are automatically applied to every generated image, and cannot be overridden in the campaign flow. For more information, refer to [Brand Kit](https://docs.clevertap.com/docs/brand-kit).

# Additional Resources

For more information, refer to the following resources:

* [Generate On-Brand Images with Effective Prompts](https://docs.clevertap.com/docs/effective-prompts-for-ai-designer-agent)
* [Brand Kit](https://docs.clevertap.com/docs/brand-kit)
