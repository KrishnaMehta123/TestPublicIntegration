---
title: Accessibility in CleverTap Messaging
excerpt: >-
  Learn how to create accessible campaigns in CleverTap that meet global
  accessibility standards, ensuring a more inclusive experience for all users.
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

Globally, an estimated 15% of the population has some form of disability ([WHO](https://www.who.int/news-room/fact-sheets/detail/disability-and-health)). Designing accessible messaging is a legal requirement and an opportunity to drive greater engagement and inclusivity. Accessibility ensures CleverTap campaigns can be understood and interacted with by all users, including those with disabilities.

By following the [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/) (WCAG), you can remove barriers for users with visual, auditory, motor, or cognitive challenges. This is especially important with the upcoming European Accessibility Act (EAA), enforceable from June 2025, which mandates accessibility for digital products and services across the EU market ([European Commission](https://ec.europa.eu/social/main.jsp?catId=1202)).

# Why Accessibility Matters in CleverTap Campaigns

### Legal Compliance

Ensure your messaging complies with regulations such as the [EAA](https://commission.europa.eu/strategy-and-policy/policies/justice-and-fundamental-rights/disability/union-equality-strategy-rights-persons-disabilities-2021-2030/european-accessibility-act_en), reducing legal and brand-related risk.

### Enhanced User Experience

Accessible design often results in simpler, clearer messaging that benefits all users, not just those with disabilities.

### Positive Brand Image

Brands that prioritize accessibility show a strong commitment to inclusivity and social responsibility, which builds customer trust and loyalty.

### Improved Campaign Performance

Accessible campaigns often see higher engagement and improved ROI across channels.

## Industry Insights

- Organizations that embed accessibility into their culture see stronger innovation and business performance.
- Over 97% of homepages still have WCAG accessibility issues ([WebAIM Million Project](https://webaim.org/projects/million/#wcag)), presenting a chance for brands to lead with inclusive design.

# Fundamental Accessibility Principles

### Color Contrast

- Maintain a minimum contrast ratio of **4.5:1** between text and background colors (WCAG AA standard).
- Use tools such as [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) to verify.
- CleverTap In-App Custom HTML templates support these contrast levels to ensure readability.

### Content Structure

- Organize content with a logical heading structure to support screen readers.
- Use semantic elements such as`<h1>` for main titles and `<h2>`, `<h3>` for sub-sections. Use `<button>` for actions and `<a>` for links.
- Avoid using generic containers such as `<div>` for structure unless paired with proper ARIA roles and keyboard interaction support.

### Keyboard Navigation

- Ensure all interactive elements are operable using only the keyboard.
- Avoid trapping users inside components such as modals or carousels.

### Clear, Actionable Labels

- Use descriptive labels such as _Register Today_ instead of _Click Here_ to help all users, especially those using screen readers to understand the purpose of actions.

# Elements of Accessible Messaging

### Text & Typography

- Use legible fonts with a minimum size of **16px**.
- CleverTap respects device-level text scaling settings.
- Enable scrolling for long messages to ensure content is not trimmed.

### Images & Multimedia

- Add meaningful alt text (up to **150 characters**) to all non-decorative images.

### Interactive & Dynamic Content

- Clearly describe the behavior of elements such as carousels, countdowns, and progress bars.
- Ensure smooth keyboard navigation and focus visibility.
- Maintain minimum touch target sizes for mobile devices:

  - iOS: **44x44 px**
  - Android: **48x48 dp**

### Custom HTML

- Use semantic tags such as `<button>`, `<section>`, and `<article>` to aid assistive technologies.
- Apply [ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) attributes when needed.
- Test content with screen readers such as NVDA, JAWS, or VoiceOver to verify compatibility.

# Accessible Rich Internet Applications (ARIA) Features

CleverTap's built-in components use appropriate [ARIA attributes](https://www.w3.org/WAI/standards-guidelines/aria/) to improve accessibility. If you are building custom HTML messages, ensure your developers also apply these best practices to maintain compatibility with screen readers.

# Accessibility Testing Guidelines

| Testing Area                | Recommended Approach                                                                                        |
| --------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Keyboard Navigation         | Use Tab, Enter, Spacebar, and Escape keys to verify full interaction without a mouse.                       |
| Screen Reader Compatibility | Test with NVDA, VoiceOver, or TalkBack to confirm correct reading order and interaction clarity.            |
| Color Contrast              | Use the [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) to ensure WCAG compliance. |
| Font Scaling                | Test text resizing across mobile devices to confirm layout stability.                                       |

# Accessibility Best Practices

| Element              | Do’s                                                     | Don’ts                                                                  |
| -------------------- | -------------------------------------------------------- | ----------------------------------------------------------------------- |
| Text & Typography    | Use clear hierarchy, strong contrast, and legible fonts. | Do not rely solely on color or decorative fonts to convey meaning.      |
| Images & Media       | Add alt text and transcripts for meaningful content.     | Do not skip alt text or transcripts for important visuals.              |
| Interactive Elements | Ensure full keyboard access and use large touch targets. | Do not make navigation paths restrictive or touch areas too small.      |
| Custom HTML          | Use semantic tags and ARIA roles where needed.           | Do not use generic tags such as `<div>` without added semantic meaning. |

# CMS Support

The CleverTap Content Management System (CMS) supports image accessibility by allowing you to do the following:

- Add alt text during image upload, including historical content.
- Auto-fill alt text when available during campaign setup or prompt for it when missing.

# Channel-Specific Recommendations

These best practices help you build accessible campaigns across various channels.

### Push Notifications

Push notifications must be accessible across devices and assistive technologies.

- Use clear, concise messaging with sufficient contrast.
- Include descriptive alt text for all images.
- Makes CTA labels screen reader-friendly and actionable.
- Adjust font size based on device settings.
- Support for TalkBack compatibility.

> 🚧 SDK Update Required for EAA Compliance
> 
> To ensure accessibility support, including alt text and screen reader compatibility, update to the latest SDK versions:
> 
> | Platform                    | EAA Compliant SDK Version                                    |
> | --------------------------- | ------------------------------------------------------------ |
> | Android Native              | v7.4.1                                                       |
> | Android Push Templates      | v2.1.0                                                       |
> | iOS Native                  | v7.2.1                                                       |
> | iOS Rich Push Notifications | v1.1.0                                                       |
> | Web SDK                     | Update required if integrated using NPM or a package manager |

### In-App Messaging

Make your in-app messages accessible by following these guidelines:

- Include alt text for all images and captions for multimedia.
- Ensure clear labeling and support for keyboard navigation.
- Accessibility support is available for Image Interstitial and Advanced in-app message builders. Legacy builders do not support these features.
- Users can add alt text when uploading images via CMS; CleverTap auto-applies this during campaign creation.
- Supports screen readers such as VoiceOver and TalkBack for text, buttons, images, and containers.

### Emails

Ensure accessible email design by:

- Structuring content using semantic HTML (headings, paragraphs, lists).
- Including alt text for all images.
- Providing transcripts or captions for any multimedia.
- Testing compatibility across desktop and mobile clients.

### Web Messages

Web messages must be fully navigable and screen reader-compatible.

- Use ARIA labels for interactive components.
- Support Keyboard navigation across modals, carousels, and expandable elements.
- Provide Keyboard navigation in Box, Banner, and Interstitial templates.
- Add alt text to Web Pop-up and Web Push Soft Prompt templates.
- Enable screen reader support for both template types.

### WhatsApp

Ensure your WhatsApp campaigns are accessible to all users by following these key accessibility practices:

- Use descriptive labels for buttons and actions.
- Include alt text for all images and provide captions for any media.

### Native Display/Web Native Display

Design accessible Native Display and Web Native Display experiences using the proper structure and supporting assistive technologies.

- Use semantic HTML and ARIA roles for structure.
- Ensure full keyboard accessibility and focus visibility.
- Add alt text and multimedia captions where needed.

### Web/App Inbox

Ensure that inbox messages are navigable, readable, and compatible with screen readers and accessibility settings to make them inclusive.

- Use semantic HTML and clear headings to structure content.
- Support Keyboard navigation and screen reader compatibility.
- Add alt text for all images and provide multimedia captions.
- Ensure Screen Reader support for buttons, titles, messages, and tabs.
- Enable live captions for embedded videos via device accessibility settings.

# Driving Impact Through Inclusion

Incorporating accessibility best practices into CleverTap campaigns ensures compliance with global standards and creates a more inclusive user experience.

By making accessibility a priority:

- You demonstrate commitment to inclusivity.
- You reduce legal and brand risks.
- You reach a wider audience and boost engagement.
- You build lasting customer loyalty through responsible design.

Investing in accessibility is both a business imperative and a moral responsibility. This aligns with CleverTap's mission to help brands create meaningful, human-first customer experiences.