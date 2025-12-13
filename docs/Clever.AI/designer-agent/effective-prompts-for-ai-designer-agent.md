---
title: Effective Prompts for AI Designer Agent
excerpt: >-
  Learn how to write clear, structured prompts to generate high-quality,
  on-brand campaign images using the AI Designer Agent.
deprecated: false
hidden: true
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

The AI Designer Agent creates brand-aligned images directly from your text descriptions. Writing a clear, structured prompt ensures that the generated image accurately reflects your intent, whether it is for a sales banner, event promotion, or seasonal creative. The model interprets your text as visual intent; it does not render exact words unless space is reserved for text. For example, a prompt such as "Add a banner area for 'Shop Now' in the bottom-right corner" results in a layout with a visual placeholder, not the words themselves.

This document helps you write prompts that get precise, visually accurate, and on-brand results.

> 📘 Private Beta
>
> Currently, this feature is released in Private Beta. If you want to access this feature, contact your Customer Success Manager.

# Writing Effective Prompts

Writing a clear, focused prompt helps the AI Designer Agent understand what you want to create and where it will be used. A good prompt explains the intent, the visual feel, and the layout composition, so the generated image matches your campaign purpose and brand identity.

You can follow this simple structure to describe your image idea in a way the Designer Agent understands easily:

### Define the Purpose (What You Want to Show)

Start by defining the intent of the image. This gives the AI the foundation for your creative direction, whether it is a product launch, a discount banner, or a festive greeting. The agent uses this initial instruction to determine the type of image to create (for example, product-focused, event-driven, or brand-awareness).

**Example prompts:**

* "Design a launch banner for a new credit card rewards program."
* "Generate a push notification image announcing a new mobile app feature."

### Describe the Look and Feel (How It Should Feel)

Add details that capture your brand's look and feel, mood, colors, and overall tone. Use adjectives that guide the image's lighting, energy, or emotional resonance. This helps the AI interpret the creative style accurately.

**Example prompts:**

* "Use warm, festive lighting with red and gold accents for a celebratory feel."
* "Apply cool blue gradients and clean white space for a professional, modern tone."
* "Add natural green and white tones for a healthy, fresh look."

### Add Layout and Composition (Where Elements Should Appear)

Specify the structure of your image; where to place text, logos, or visual emphasis. This gives the AI guidance on framing and visual hierarchy, improving clarity and usability across campaign channels.

**Example prompts:**

* "Add clear space at the bottom for headline text."
* "Place the brand logo in the top-right corner."
* "Leave room in the center for a CTA button or offer area."

### **Prompt Tips**

The following are some useful tips when adding visual and emotional details to your prompts:

* Describe mood or emotion (for example, warm, premium, playful, trustworthy).
* Mention lighting or visual treatment (for example, soft light, gradient glow, high contrast).
* Avoid mixing contradictory styles ("vibrant and minimal").
* Do not paste links or external URLs; attach or upload reference images instead.
* Include your brand or campaign colors for consistency.
* Add audience or product type for fine-tuning.

**Combine All Three Parts for Best Results**:

* "Create an image for a push notification promoting a Diwali sale on home décor items at HomeStay.\
  Use warm red and gold tones with soft festive lighting for a celebratory, premium feel.\
  Add a 'Shop Now' CTA at the bottom and place the HomeStay brand logo in the top-right corner."

<Image alt="Sample Prompt and Banner" align="center" border={true} src="https://files.readme.io/d0c16757fa8cfa3690a9b8d748b084630a14785b453d2d85f94d68913663477f-image.png">Sample Prompt and Banner</Image>

# Sample Prompts

The following sample prompts show how detailed prompts improve image quality, tone, and brand consistency. You can experiment with more prompts to find a suitable message tone and style for your brand. Browse the sample prompts by industry:

<style>{'* { margin: 0; padding: 0; box-sizing: border-box; } .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin: 20px 0; } .integration-card { text-decoration: none; border: 1px solid #e0e6ed; border-radius: 8px; padding: 16px; display: flex; align-items: center; gap: 12px; background: white; transition: all 0.2s ease; cursor: pointer; } .integration-card:hover { border-color: #4f46e5; background: #f8fafc; transform: translateY(-1px); box-shadow: 0 4px 12px rgba(0,0,0,0.1); } .logo-container { flex-shrink: 0; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; } .logo { width: 100%; height: 100%; object-fit: contain; } .content { flex: 1; } .name { font-weight: 600; font-size: 16px; color: #1f2937; margin-bottom: 4px; } .category { font-size: 14px; color: #6b7280; }'}</style>

<div className="grid">
  <a href="#e-commerce" className="integration-card">
    <div className="logo-container">
      <img src="https://img.icons8.com/fluency/48/shopping-cart-loaded.png" className="logo" alt="E-Commerce" />
    </div>
    <div className="content">
      <div className="name">E-Commerce</div>
      <div className="category">Personalization & Offers</div>
    </div>
  </a>

  <a href="#ott" className="integration-card">
    <div className="logo-container">
      <img src="https://img.icons8.com/color/48/tv.png" className="logo" alt="OTT" />
    </div>
    <div className="content">
      <div className="name">OTT</div>
      <div className="category">Content & Engagement</div>
    </div>
  </a>

  <a href="#fintech" className="integration-card">
    <div className="logo-container">
      <img src="https://img.icons8.com/color/48/money-bag.png" className="logo" alt="Fintech" />
    </div>
    <div className="content">
      <div className="name">Fintech</div>
      <div className="category">Finance & Portfolios</div>
    </div>
  </a>

  <a href="#food-delivery" className="integration-card">
    <div className="logo-container">
      <img src="https://img.icons8.com/color/48/meal.png" className="logo" alt="Food Delivery" />
    </div>
    <div className="content">
      <div className="name">Food Delivery</div>
      <div className="category">Menu & Recommendations</div>
    </div>
  </a>

  <a href="#gaming" className="integration-card">
    <div className="logo-container">
      <img src="https://img.icons8.com/color/48/controller.png" className="logo" alt="Gaming" />
    </div>
    <div className="content">
      <div className="name">Gaming</div>
      <div className="category">Rewards & Items</div>
    </div>
  </a>
</div>

## E-Commerce

**Prompt:**

> "Create a 16:9 banner for an online fashion sale offering 40% off on summer wear.\
> Use bright, airy tones with soft beige and teal accents from the brand kit.\
> Show models wearing summer outfits in a clean, minimal layout.\
> Add a bold 'Shop Now' CTA at the bottom."

**Result:**

<Image alt="E-Commerce" align="center" border={true} src="https://files.readme.io/c3ac25a634b3f8931f616ea6ed0a6394a9fb686a845960e9e3a3bbd397a1d6ed-image.png" />

## OTT

**Prompt:**
> Create a cinematic, symmetrical push banner for an OTT platform promoting an upcoming Premier League match. 
>
> Show two football players at the center one in a red kit (Liverpool) and the other in a blue kit (Chelsea) facing off under bright floodlights in a packed stadium at night. Add soft haze, motion light streaks, and a subtle red–blue glow split for depth and energy.
>
> Place text at the top centre:\
> Headline: "Premier League Live – Sat, 8:30 PM"\
> Subheadline: "Liverpool vs Chelsea • Your Favourite Teams. One Epic Battle."
>
> Keep it clean, cinematic, and broadcast-grade, like a real sports promo on OTT platform.

**Result:**

<Image alt="OTT" align="center" border={true} src="https://files.readme.io/5487678107d20a434f829934aad00b24aaec558175883a0dd85ddf146623022c-image.png" />

## Fintech

**Prompt:**

> "Design a 1:1 push banner for a personal loan offer campaign.\
> Use a calm, trustworthy color palette with blues and neutrals.\
> Include visuals of a family or homeowner looking confident and secure.\
> Add a headline 'Your Dream Home Awaits' and a subtext 'Apply for low-interest home loans today."

**Result:**

<Image alt="Fintech" align="center" border={true} src="https://files.readme.io/78b1dcdcf9450bdb46a96331b94e86c0bec6680a8c4d7e158b87abd9db078357-image.png" />

## Food Delivery

**Prompt:**

> "Design a 16:9 weekend offer banner for a food delivery app offering 25% off on pizza orders.\
> Use warm, appetizing tones with real pizza imagery and subtle glow lighting.\
> Add a bold 'Order Now' CTA in brand color #A8FBD3 with readable, rounded text."

**Result:**

<Image alt="Food Delivery" align="center" border={true} src="https://files.readme.io/0e19fd7adf3bc9afd9597b11670b66eca505322f9093163023dc389b6cd400de-image.png" />

## Gaming

**Prompt:**

> "Create a 16:9 promotional banner for a gaming app's weekly reward challenge.\
> Use dark neon backgrounds with glowing effects to emphasize excitement.\
> Add bold typography for the text 'Unlock Weekly Rewards!' and include a gold button with 'Play Now."

**Result:**

<Image alt="Gaming" align="center" border={true} src="https://files.readme.io/0f483a76343bfe4511565d2759c6a924af39eb5ee4ee425faad7f890f1689621-image.png" />

# Ways to Generate Images with AI
You can generate on-brand images in multiple ways depending on your campaign needs. The AI Image Generator supports creating new images, editing existing ones, or using a reference image to guide visual consistency.

For more information on generating and editing images, along with step-by-step instructions, refer to [Designer Agent](https://staging.docs.user.clevertap.net/docs/ai-image-generator).

> 📘 **How Brand Kit and Prompts Work Together**
>
> If your prompt conflicts with your Brand Kit, the Brand Kit always takes priority to maintain brand consistency. The system applies settings in this order: **Brand Kit → Prompt → Filters**
>
> This ensures every generated image stays brand-compliant and visually consistent with your defined design standards.

# Common Prompt Issues

Refer to the following table for common prompt related issues, and how to fix them for best results:

| Common Prompt Issue                 | Why It Causes Issues                                                                                                                                                                                            | How to Fix                                                                                                                                                               |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Vague Prompt**                    | The AI Designer Agent lacks clear direction for layout, tone, or subject. Short, generic inputs like "banner" or "sale" don't provide enough detail for a meaningful image.                                     | Be specific about what you want to show. Example: "Create a festive banner for Diwali with red and gold tones and decorative lamps."                                     |
| **Conflicting Brand or Tone**       | Opposite visual or emotional cues (for example, "vibrant yet minimal") or color requests that differ from your Brand Kit confuse the AI and result in mismatched visuals.                                       | Keep tone and brand cues consistent. Choose one style, for example, either "bold and expressive" or "clean and minimal." Ensure color choices align with your Brand Kit. |
| **Using URLs**                      | The AI cannot interpret external links or embedded design references from tools like Figma.                                                                                                                     | Upload or attach the reference image directly within the generator instead of pasting URLs.                                                                              |
| **Misunderstanding Text in Images** | The AI interprets your text as layout guidance, not literal copy. Only the text you explicitly include in your prompt will appear. If no text is given, the AI may auto-generate its own creative placeholders. | Specify exact words if you want them visible. Example: "Add the text 'Shop Now' at the bottom in a bold white font."                                                     |