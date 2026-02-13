---
title: Copywriter Agent
excerpt: 'Learn how to generate Push Notification message copies with AI. '
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

Copywriter Agent helps you instantly create, edit, or refine message copy for your Push Notifications campaigns directly within CleverTap. It goes beyond standard AI copy generation by combining your Brand Kit with insights from your past high-performing campaigns. This ensures that every message aligns with your brand voice and is inspired by what has already driven results for your audience.

Copywriter Agent reduces manual effort, speeds up campaign creation, and helps you produce consistent, on-brand copy that is aligned with your engagement goals.

> 📘 **Private Beta**
>
> This feature is currently available in Private Beta and enabled for select customers. To get access, contact your Customer Success Manager.

# Maximize Efficiency with Copywriter Agent

With Copywriter Agent, you can:

* Save time during campaign creation by generating copy where you build campaigns, without switching tools or re-entering context.
* Maintain brand consistency at scale by applying your Brand Kit automatically, so all messages follow approved tone and style, even across teams.
* Create more effective copy by drawing inspiration from your past high-performing campaigns, rather than relying on generic AI suggestions.
* Explore multiple message variations quickly for the same intent, helping you test and choose the best-performing approach.
* Improve speed and consistency across teams by reducing manual rewrites and copy reviews.

# Learn How Copywriter Agent Works

The Copywriter Agent is embedded within the Push Notification Message Editor. The agent helps you generate copy based on the:

* Campaign intent: The prompt you provide describes what you are trying to achieve in this campaign. For example, _Re-engage users who abandoned their cart with items still available_ or _Bring back dormant users who haven’t opened the app in 14 days_.
* Brand Kit: The agent applies your brand tone and style to keep the generated content aligned with your brand's messaging guidelines. If your account has multiple Brand Kits, you can select the appropriate one before generating copy to match the brand or campaign you are working on. For more information about configuring Brand Kits, refer to [Brand Kit](https://docs.clevertap.com/docs/brand-kit).
* Past campaign lookback: Your past campaign lookback is set in Brand Kit. Based on the intent you provide, the agent automatically identifies relevant past campaigns with similar intent that have performed well and uses them as inspiration. For example, if you create a holiday campaign, the agent references high-performing past messages and applies a similar tone or structure. This helps ensure the copy feels more relevant, contextual, and closer to what has already worked for your audience.

# Generate Copy Using a Prompt

To guide tone, style, and language, make sure the correct [Brand Kits](https://staging.docs.user.clevertap.net/update/docs/copywriter-agent?isFramePreview=true#brand-kits) and [Content Settings](https://staging.docs.user.clevertap.net/update/docs/copywriter-agent?isFramePreview=true#content-settings) are selected.

To generate copy using Copywriter Agent:

1. Open your **Campaign Editor**.
2. Click **Ask AI** to generate both Title and Message. You can also click the ![](https://files.readme.io/935fb6454c1119d8ecbbcb60baaa21dd7d7fbd62688f5c4fc3a5590b17a9c46e-Clever_AI_icon.png) icon in the Title or Message field to generate content specifically for that field.

<Image align="center" border={true} caption="Ask AI in Campaign Editor" src="https://files.readme.io/ea80a513e9d48c0014db45b9b310ae855e3ac1d5eea24b189c2b7155b6a67605-image.png" />

3. In the new copywriter window, describe the intent of the campaign, or what you want the message to do. For example, _Bring back dormant users who haven’t opened the app in 14 days_ or _Promote the Friday sale for premium plans_. The AskAI window also displays some example prompts to help you get started.

<Image align="center" border={true} caption="Copywriter Agent Prompt Window" src="https://files.readme.io/84e693985286d24e7df8b4656e293952ea7aad8855d1bf111fc2d0c5031cfe58-2026-01-21_13-06-52.png" />

4. Select the Brand Kit and configure Content Settings (such as tone, emotion, or personalization) based on your campaign needs.
5. Add Click the ![](https://files.readme.io/764e6202e87af763be5fe1711eb756251036bcdc9064d72195a8c915a53bef5b-2026-01-21_14-16-28.png) icon to generate the copy. You can preview how the copy looks in real time within the device preview.
6. The Copywriter Agent creates multiple variations based on your prompt and settings. It also refers to past campaigns for reference and provides the list of campaign templates.

<Image align="center" border={true} caption="Generated copy variations" src="https://files.readme.io/0c9ea05ffa0f0012ea9dd45a0bbc75cac6e204b18337b729d7bac115e97a8c16-2026-01-21_13-14-46_1.gif" />

7. To refine the generated copy, select the output you want and click **Improve**. You are navigated to the prompt pane to rewrite the copy (for example, you can prompt it to make the copy shorter, friendlier, more urgent, and so on).

<Image align="center" border={true} src="https://files.readme.io/fcdef699d9fd84361ee1b2bf7230eda931b6f744dd39bf91ec67f1ead5073c4f-2026-01-21_14-32-05_1.gif" className="border" />

8. Click **Use Content** to insert the selected copy into your campaign.

> 📘 Optimize Output with Detailed Prompts
>
> The Copywriter Agent relies on the clarity of your prompt to generate accurate, high-quality copies. The more specific you are about goal, audience, tone, and so on, the better the output will align with your campaign goals.

# Brand Kit and Content Settings

The Copywriter Agent provides controls to guide the style and tone of the generated copy, using [Brand Kits](https://staging.docs.user.clevertap.net/update/docs/copywriter-agent?isFramePreview=true#brand-kits) and [Content Settings](https://staging.docs.user.clevertap.net/update/docs/copywriter-agent?isFramePreview=true#content-settings).

<Image align="center" border={true} caption="Core Brand and Content Settings" src="https://files.readme.io/e9ed262d61bf5bd0306ece9643bc83d334764bd900810dbd0be24885be32ffe9-2025-12-29_15-54-14.png" />

## Brand Kits

Click on **Brand Kits** to view your brand’s tone, campaign reference period, creativity, and so on for your content. If you have configured multiple brand kits, select the appropriate one before generating content. Click **Apply to this Thread**.

You can also configure a custom kit for the current thread. This helps align generated copy with your brand’s preferred tone and instructions.

<Image align="center" border={true} caption="Brand Kits" src="https://files.readme.io/bc9c2aecf542c8a8a2dd1572ed3dd1194dc108625051a7733719b3fd8b3d508a-2026-01-21_15-41-55.png" />

<Callout icon="📘" theme="info">
  **Note**

  * Locked Brand Kits can’t be edited in the campaign flow because they are meant to enforce brand consistency across teams. Locking a kit ensures that campaign-level users cannot override approved brand styles.
  * Any changes made to a Brand Kit from the campaign flow apply only to the current thread. This allows you to experiment with copy variations without permanently changing your account-level Brand Kit.
  * If a prompt conflicts with Brand Kit settings, the agent automatically follows the Brand Kit settings to maintain consistency.
  * For more information on setting up and using brand kits, refer to [Brand Kit](https://docs.clevertap.com/docs/brand-kit).
</Callout>

## Content Settings

You can customize how the content must be written using **Content Settings**.

1. Click the Content Settings icon in the Ask AI window to configure the following options:

* **Language**: Choose the language for the generated copy.
* **Script**: Select the writing system used for the selected language (for example, if your selected language is Hindi, choose Devanagari script for `नमस्ते` or Latin script for `Namaste`.)
* **Emotions**: Define the emotional tone, such as Neutral, FOMO, Trust, Joy, Surprise, and Anticipation.
* **Content Type**: Select the writing style, such as Catchphrase, Punchy, Throwback, and so on.
* **Personalization**: Enable this to include personalization placeholders (for example, `Name` or `City`) where relevant.
* **Emojis**: Enable this to allow emojis when they fit the message tone and channel.

2. Click **Apply** to save your settings before generating content.

<Image align="center" border={true} caption="Content Settings for Copywriter Agent" src="https://files.readme.io/20f94fc39ebe47585e2d2730d72cf968d121b345df48288ddbe84067100af65d-2026-01-21_14-01-50.png" />

# Threads

Once you start generating copy, CleverTap automatically saves your sessions under the Threads ![](https://files.readme.io/a973e47e78d9cb32bf7c2372bc46d90fdb6f8eb16dd6ebaa77a63c2b385438c8-Threads_icon.png) tab. Each session is stored as a thread, which preserves your prompts, refinements, and generated outputs, helping you resume from where you left off without losing context.

<Image align="center" caption="All Threads" src="https://files.readme.io/7cbea7cbf4e0d258a535a8feeb9c1ef2c4e4a0dc6f4298a9a89f4f1f97000205-2026-01-21_16-00-17.png" />

### How Threads Work

Threads are scoped to your **Account**, **Agent**, and **User**, ensuring that your history remains personalized and relevant. All threads for your account appear in the **All Threads** popup. A thread becomes the context for your next generation, allowing Clever.AI to remember your prior brand preferences or edits. They are not tied to specific campaigns; they persist across multiple campaigns for seamless continuity.

If multiple users from the same account use AI tools:

* Each user sees only their own threads and the latest image generation session that they have participated in.
* Threads are separate for Segmentation, Analytics, Designer Agent, and Copywriter Agent, even under the same account.

### Manage Threads

From the **All Threads** view, you can:

* Revisit previously generated copy to review or compare variations.
* Continue refining copy within the same context without starting over.
* Reuse effective messages across campaigns with similar goals.

# Best Practices for Writing Prompts

The Copywriter Agent relies heavily on the clarity of your prompt. Follow these best practices to get better results:

* Clearly state the goal of the message
  _Example: “Re-engage users who haven’t opened the app in 14 days.”_
* Mention the audience
  _Example: “Users who abandoned cart.”_
* Define the tone or emotion
  _Example: friendly, urgent, reassuring._
* Avoid vague prompts that lack context, such as _write a notification_ or _marketing copy_.
* All generated copies should be reviewed by your internal brand and legal teams before use in public campaigns.
* Avoid including any personal or confidential information in AI prompts. Keep descriptions focused on creative intent.

You can refine the output by adjusting the prompt, changing Content Settings (emotion, tone, personalization), or regenerating content multiple times. Each variation helps you explore different angles until the copy matches your intent. Refer to the below table for difference between vague and effective prompts:

<Table>
  <thead>
    <tr>
      <th>
        Vague Prompt
      </th>

      <th>
        Effective Prompt
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Write a push notification
      </td>

      <td>
        You are a lifecycle marketing copywriter for a consumer app.  
        Create high-converting copy to re-engage users who haven’t opened the app in 14 days.  
        Deliver:

        * A concise title
        * A clear, benefit-led message  
          Keep the tone friendly and trustworthy, and include a gentle CTA.
      </td>
    </tr>

    <tr>
      <td>
        Create marketing copy
      </td>

      <td>
        Create high-converting copy to promote the Friday sale to existing users. Add a title with 3 words, and a clear message highlighting the main offer or benefit.  
        Use a sense of urgency, keep the tone modern and trustworthy, and include a gentle CTA.
      </td>
    </tr>

    <tr>
      <td>
        Notify users about an offer
      </td>

      <td>
        Create high-converting message to notify existing users about a limited-time offer.  
        Deliver a title and a clear message explaining the value of the offer  
        Keep the tone helpful and persuasive, and include a gentle CTA.
      </td>
    </tr>

    <tr>
      <td>
        Notify users about items left in cart
      </td>

      <td>
        Create high-converting push message to remind cart abandoners about items left behind. Add a clear message nudging users to complete their purchase  
        Keep the tone fun, casual, and action-oriented, and include a gentle CTA.
      </td>
    </tr>

    <tr>
      <td>
        Announce a feature
      </td>

      <td>
        You are a marketing copywriter for a consumer app.  
        Create high-converting copy to encourage existing users to try a new feature. It should include a clear message highlighting the primary benefit of the feature  
        Keep the tone informative and trustworthy, and include a CTA.
      </td>
    </tr>
  </tbody>
</Table>

# FAQs

### Is the generated copy reused or shared across accounts?

No. All generated copy is unique to your prompt and campaign context. CleverTap does not reuse or share generated content across accounts.

### Who owns the generated content?

You retain full ownership of all content generated using the Copywriter Agent. CleverTap does not claim any intellectual property rights over the generated output.

### Is my data used to train AI models?

No. Your prompts and generated content are not used to train AI models. Only the minimum required input is sent securely to generate the response.

### What if I don't want any user to override my brand guidelines?

Brand guidelines are automatically applied to every generated copy, whether your Brand Kit is locked or not. However, users with appropriate permissions can customize settings for individual threads. If you want to prevent overrides, you can lock the Brand Kit from the BrandKit section. When locked, users cannot modify tone, style, or other brand settings during campaign creation. The agent automatically applies the locked kit's guidelines. For more information, refer to [Brand Kit](https://docs.clevertap.com/docs/brand-kit).
