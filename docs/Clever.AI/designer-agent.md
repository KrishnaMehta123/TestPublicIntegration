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

**Designer Agent** helps you instantly create, edit, or refine images for your Push Notification campaign, all within CleverTap, without the need for external design tools. It combines advanced AI capabilities with your Brand Kit to generate on-brand, campaign-ready visuals quickly and efficiently. This makes it easier for teams to design creative, personalized images directly in the campaign editor, reducing dependency on design teams and accelerating go-to-market time.

> 📘 Private Beta
> 
> This feature is released in Private Beta and is enabled for select customers only. To enable this feature, contact your Customer Success Manager.
> 
> Designer Agent is available in Push Notifications, for accounts where push templates are enabled. This feature will soon be expanded to other messaging channels.

# How Designer Agent Works

The feature is embedded within the Push Notification editor, next to image upload fields, such as **Expanded Image** or **Large Icon**. You can use it to:

- Create new images from scratch using descriptive prompts.
- Edit or refine existing visuals with prompts.

The Designer Agent automatically applies your Brand Kit to ensure every generated image aligns with your brand colors, styles, and tone.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/74795935df940693c38e96dff8d6cb0cd01e89ed293312891efb74866c2cdd25-AI_Image_Generator_for_Push_Campaign.png",
        "",
        "AI Image Generator for Push Notification"
      ],
      "align": "center",
      "border": true,
      "caption": "Designer Agent for Push Notification"
    }
  ]
}
[/block]


## Generate Image Using Prompt

The Designer Agent utilizes your prompt and Brand Kit settings to create visuals that align with your campaign’s theme. By providing clear and detailed descriptions of what you need, you can quickly create on-brand images tailored to your requirements. To do so:

The AI Image Generator uses your prompts along with Brand Kit settings to produce visuals that match your campaign's theme. 

The AI Image Generator combines your prompt and Brand Kit settings to produce campaign-ready images that align with your brand and message.

1. Open your **Push Notification** campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png) Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png) Generate with AI**  for the _Rich media_ field. 
3. Click **Generate Image**. The _Generate Image_ window opens.
4. Describe the image you want in the prompt field at the bottom. For example, if you are going to generate a sample image for an OTT platform to promote an upcoming Premier League football match, refer to the following image: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d536d43634a56cea46994435aa5db5450774744f0e6b8e05e2470d4c11ed7a9c-OTT_Platform_Example.png",
        "",
        "Generate Image"
      ],
      "align": "center",
      "border": true,
      "caption": "Image Generated Using Text to Image Option"
    }
  ]
}
[/block]


5. Click ![](https://files.readme.io/bdbfd957c9ccc6dff7284d71450e4414281705ac5d8337c238198a6d7cc896ee-Image_Settings_Icon.png) to select the _File format_ (JPEG or PNG). The Ratio/Size (that is, 1:1) is auto-selected and non-editable. The aspect ratio and size are automatically aligned with Push OS specifications (for example, 1:1 for Large Icon and 16:9 for Expanded Image) to ensure compatibility.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a7f815daca070109b5ff17f4f78a54aa308f9847b073dc4a391f738344ff8e02-image.png",
        null,
        "Image Studio"
      ],
      "align": "center",
      "border": true,
      "caption": "Image Studio"
    }
  ]
}
[/block]


6. Click **Primary Kit** to view your brand’s style, button colors, brand colors, and so on, for your image. Click **Apply**. Click **Secondary Kit** to configure a custom kit for the current image. For more information on setting it up, refer to [Brand Kits](https://docs.clevertap.com/docs/brand-kit).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/664001348ea7da1a08f8185bb381e98c5c06a2d0afcf98268593042681c1a0d3-image.png",
        null,
        "Brand Kit"
      ],
      "align": "center",
      "caption": "Brand Kit"
    }
  ]
}
[/block]


> 📘 **Brand Kits**
> 
> - Brand kit names reflect what you set up in your account.
> - You can set up a maximum of 10 brand kits per account. You can select from the available kits.
> - If a brand kit is locked, it cannot be edited within the campaign flow.
> - Any changes you make here apply only to the current campaign. They do not update the original brand kit saved in your account.
> - When generating or editing images, the **selected Brand Kit** always takes precedence over text prompts. If a prompt conflicts with your brand kit’s defined elements, for example, color codes, borders, or typography, the AI prioritizes the brand kit settings.  
>   **Example**  
>   If your brand kit specifies a _red border (0.5 cm)_ and the prompt requests a _blue border_,  
>   the generated image will use **red**, following your brand kit guidelines.  
>   This ensures visual consistency and keeps all campaign creatives on-brand, regardless of the prompt details.
> 
> For more information on setting up and using brand kits, refer to [Brand Kit](https://docs.clevertap.com/docs/brand-kit). 

7. Click **Generate**. Review the generated image and click **Insert** to add the image to your campaign.
8. After inserting the image, you can edit or refine the image directly within the editor:

- Enter follow-up prompts in the same chat thread to refine the image.
- To edit an existing image, go to the Message Editor, click **Upload**, and select the image. Click ![](https://files.readme.io/3dd08bfdc757b30950b16c701f01b8970b5ddec566c161e93cb3c1081ee73e60-Edit_icon.png) and describe the change you want to make (for example, Change CTA text from "Watch Live" to “Watch Now”). Each refinement creates a new version saved in your Threads history, allowing you to revisit or reuse past iterations.

  [block:image]{"images":[{"image":["https://files.readme.io/01e7233196e05a2a68213836230306770b3d994a7555e64bdfbfb041c577dde2-Edit_Generated_Image.gif","","Edit Generated Image"],"align":"center","border":true,"caption":"Edit Generated Image"}]}[/block]

## Generate Using Reference Image

To generate an image using a reference image, perform the following steps:

1. Open your Push Notification campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png) Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png) Generate with AI**  for the _Rich media_ field.
3. Click **Generate Image**. The Generate Image window opens.
4. Click ![](https://files.readme.io/7c39b5787600b7ac069bc4f2f78a6f3f0304bd3c3cc04eef082aa945c714fdf8-Plus_Icon.png) to select an existing banner from CMS. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e321224127b1de1ff8feae54767ad33433f1ef8bf704571e3418a72d4f777fc2-2025-11-28_14-49-17_1.gif",
        "",
        "Generate Image Using Reference Image"
      ],
      "align": "center",
      "border": true,
      "caption": "Generate Image Using Reference Image"
    }
  ]
}
[/block]


5. You can also browse and select an image from your AI-generated images folder in the CMS. Click **Upload** and **Edit**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/feba778dbafdf0bb11dd24ae8038992f84b7b7f97547fff534d2152026ac4d7c-image.png",
        null,
        "Edit Image"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Image"
    }
  ]
}
[/block]


6. In the prompt field, describe the updates or new campaign details you want to apply.  Once you select an image, you can:

- **Change text**: For example, update offer amounts, taglines, or call-to-action text.
- **Change background**: Modify colors, replace backgrounds, or adjust contrast for seasonal themes.
- **Replace visual elements**: Swap product photos, icons, or logos.
- **Adjust layout**: Realign elements, add or remove visual sections, or reposition branding.
- **Add highlights or effects**: Emphasize key offers or add simple visual effects, such as a glow or drop shadows.  
  For example, if you want to use 30% Off banner as a reference and update it for Holi with bright color accents and festive treats.

7. Click **Brand Kit** to view or switch to another kit if needed.
8. Click **Generate**. It analyzes your reference image and applies the prompt instructions you provide. A new image is generated that maintains the layout and design consistency of your requirements.
9. Review the generated image and click **Insert** to add it to your campaign.

> 📘 Brand Kit Application
> 
> The latest created Brand Kit is automatically selected and applied to your image, even if you don’t manually choose one.
> 
> If only one Brand Kit exists, it’s applied by default.
> 
> If multiple kits are available, the most recently created one is auto-selected.

## Use Secondary Image to Update Primary Image

Upload an existing image as a reference. Clever.AI uses its layout, style, and color palette to create a fresh visual. You can use this method when you want to: refresh a past campaign creative, maintain a consistent look and feel across offers, and make quick adaptations for regional or seasonal variations.

This helps with the following:

- Retains brand tone and design balance.
- Reduces turnaround for variant creation.

To generate an image using this method, perform the following steps:

1. Open your Push Notification campaign editor.
2. For Android, click **![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png) Generate with AI** for the _Expanded image_ or _Large icon_ fields. For iOS, click **![](https://files.readme.io/de594698e41f816505d7fb2148204b4ce6f2f581d952289e89b9d9022fe5015d-Clever_AI_icon.png) Generate with AI**  for the _Rich media_ field.
3. Click **Generate Image**. The Generate Image window opens.
4. Click ![](https://files.readme.io/7c39b5787600b7ac069bc4f2f78a6f3f0304bd3c3cc04eef082aa945c714fdf8-Plus_Icon.png) to upload the following.
   - Primary Image: The creative you want to update.
   - Secondary Image: The visual reference that defines your desired color tone, layout, or design.
5. In the prompt field, describe how you want to adapt or align the primary image to match the secondary one.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/879aae0c5629396861b0d7d09d4684d616f8ca0ab45eac0938ddc2a6d5ab87b1-2025-11-23_17-21-52_1.gif",
        "",
        "Use Secondary Image to Update Primary Image"
      ],
      "align": "center",
      "border": true,
      "caption": "Use Secondary Image to Update Primary Image"
    }
  ]
}
[/block]


Refer to the following example prompt:

6. ```Text Example Prompt
   Use the Christmas Sale banner as the primary image and the Diwali Sale banner as the secondary reference.  

   Match the Christmas image’s composition, color palette, and text placement to the Diwali banner’s warm, festive layout.  
   Replace the background gradient with rich gold tones, add warm lighting, and include subtle decorative elements like stars or ribbons.  
   Headline: “Celebrate the Season with Style”  
   Subheadline: “Up to 50% Off on Fashion & Accessories.”  
   CTA: “Shop Now” in a red or gold rounded button.
   ```

7. Click **Brand Kit** to apply your brand’s predefined colors, tones, and layout.

8. Click **Generate**. It analyzes both images and adjusts the primary to match the secondary in tone, layout, and design style.

9. Review the generated image in the preview panel and click **Insert** to add it to your campaign. To make refinements, use follow-up prompts. 

> 📘 Why detailed prompts matter?
> 
> The Designer Agent relies on the clarity of your description to produce accurate, high-quality visuals. The more specific you are about theme, colors, layout, or mood, the better the output will align with your campaign goals. Include contextual details (like event name, offer type, or brand tone) for best results. For more information, refer AI Image Prompts. (link to be added)

# Manage Generated Images

All AI Generated images can be accessed via [Threads](https://docs.clevertap.com/docs/designer-agent#threads)  and [AI Generated Images Folder](https://docs.clevertap.com/docs/designer-agent#ai-generated-images-folder).

## Threads

Once you start generating images, it automatically saves your sessions under the ![](https://files.readme.io/a973e47e78d9cb32bf7c2372bc46d90fdb6f8eb16dd6ebaa77a63c2b385438c8-Threads_icon.png) tab. Each session is stored as a **thread**, which captures your prompts, refinements, and generated outputs, helping you resume from where you left off without losing context. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e709fdea4b216257df9129d2d2e28f798ed53f1ec2caaf0bf946eba64d51bf18-image.png",
        null,
        "All Threads"
      ],
      "align": "center",
      "border": true,
      "caption": "All Threads"
    }
  ]
}
[/block]


### How Threads Work

Threads are scoped to your **Account**, **Agent**, and **User**, ensuring that your history remains personalized and relevant. All threads for your account appear in the **All Threads** popup. A thread becomes the context for your next generation, allowing Clever.AI to remember your prior visual style, brand preferences, or edits. They are not tied to specific campaigns; they persist across multiple campaigns for seamless continuity.

If multiple users from the same account use AI tools:

- Each user sees only their own threads and the latest image generation session that they have participated in.  
- Threads are separate for **Designer Agent** and **AI Content Generator**, even under the same account.

### Manage Threads

From the **All Threads** view, you can:

- Reopen an older thread to continue generating or editing images using the same context.
- Review and compare multiple image versions created during that session.
- Restore or reuse previously generated images without regenerating them.

> 💡 **Tip**
> 
> For subsequent edits, you need not restart a session. You can type your next instruction directly in the chat. For example: _“Make the background blue and add a 50% OFF badge in the corner.”_ The AI will update the existing image while maintaining your brand styling and earlier visual tone.

## AI Generated Images Folder

All AI-generated images are automatically stored in your _CMS_, under the **AI Generated Images** folder for your account. This allows you to reuse, manage, or download previously created visuals without needing to regenerate them.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7bd10e224147810623d972c5b4c9854c17e9d267de86e3a17db5fa22d64eeaa-brand.png",
        null,
        "AI Generated Images Folder"
      ],
      "align": "center",
      "border": true,
      "caption": "AI Generated Images Folder"
    }
  ]
}
[/block]


# Best Practices for Writing Prompts

The following best practices will help you with writing more detailed prompts:

- Be **specific** and include theme, tone, and visual intent.  
  _Example: “Create a modern app promo banner with minimalist icons.”_
- Add **context**; specify what the image is for (offer, product launch, festival).
- Use your **brand kit** for visual alignment.
- Don’t write one-liners. A prompt like “banner” or “sale” gives the AI too little to work with — resulting in generic, off-brand images.
- Describe the scene, emotion, and layout you want to see.  
  _Example: “Create a 1:1 Push Notification image for a festive Diwali campaign with maroon and gold tones, decorative lamps, and a bold ‘Shop Now’ button in brand colors.”_
- Review and refine your prompt if the output doesn’t match your intent.

The Designer Agent relies on the clarity of your description to produce accurate, high-quality visuals. The more specific you are about theme, colors, layout, and mood, the better the output aligns with your campaign goals.

| Prompt Type         | Example                                                                                                                                               | Output Description                                                |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **Short Prompt**    | “Create a sale banner.”                                                                                                                               | Produces a generic image with limited relevance or branding.      |
| **Detailed Prompt** | “Design a 1:1 Push Notification image for a Diwali sale using maroon and gold tones, soft festive lighting, and a ‘Shop Now’ button in brand colors.” | Produces a vibrant, on-brand image matching the campaign context. |

For more information, refer to [Effective Prompts for AI Designer Agent](https://docs.clevertap.com/docs/effective-prompts-for-ai-designer-agent).

# FAQs

### Can I edit the generated image after inserting it?

Yes. You can prompt it to “change background,” “update offer text,” “replace image”, and so on. These edits happen directly in the chat interface.

### What image formats are supported?

The generator currently supports **JPEG** and **PNG** formats.

### What if I want my brand guidelines applied every time I generate an image?

You can lock your Brand Kit from the BrandKit section. When locked, the selected kit’s styles (colors, buttons, etc.) are automatically applied to every generated image, and cannot be overridden in the campaign flow. For more information, refer to Brand Kit. (link) 

### Does CleverTap store or reuse the images I generate?

Yes, the images you generate are stored securely within your account’s CMS so you can access them later. However, CleverTap does not reuse, resell, or redistribute your images in any way. The generated output remains unique to your prompt and campaign inputs.

> 📘 Note
> 
> Images are stored only for your reuse and are never shared across accounts.

### Who owns the images I generate?

You retain full ownership of all images generated using the Designer Agent. CleverTap does not claim any intellectual property rights over generated content. 

### How is my data used and shared with Nano Banana AI?

CleverTap’s Designer Agent uses Nano Banana AI to create images. Your input data is transmitted securely to Nano Banana’s API for generation and returned to CleverTap for display in your campaign. Your data is never used to train Nano Banana AI models. Nano Banana deletes all input data within 30 days, in accordance with their Terms of Use. CleverTap sends only the necessary input to generate your requested image, including your text prompt, and, if applicable, metadata such as brand kit colors or style selections. No personally identifiable information (PII) about you or your users is shared unless you explicitly include it in your prompt. The generated image and related metadata are stored securely within your CleverTap account. 

> 💡 **Best Practice**
> 
> All generated materials should be reviewed by your internal brand and legal teams before use in public campaigns.
> 
> Avoid including any personal or confidential information in AI prompts. Keep descriptions focused on creative intent.

### Can I paste links or URLs (for example, Figma or design file links) into the AI chat?

No. The Designer Agent does not support links or URLs pasted into the chat or prompt field, as it does not fetch or render content from external URLs.

### Do filters affect prompts?

Filters (such as “Cinematic,” “Minimalistic,” or “3D Render”) refine image tone and texture. If there is a conflict, your Brand Kit and prompt take priority.

### What aspect ratios are supported?

Aspect ratios are pre-selected and non-editable based on your campaign channel (for example, 1:1 for Large Icon, 16:9 for Expanded Image).

# Additional Resources

For more information, refer to the following resources:

- [Effective Prompts for AI Designer Agent](https://docs.clevertap.com/docs/effective-prompts-for-ai-designer-agent)
- [Brand Kit](https://docs.clevertap.com/docs/brand-kit)