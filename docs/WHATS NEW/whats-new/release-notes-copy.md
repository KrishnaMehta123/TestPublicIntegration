---
title: Release Notes 2024 (New)
excerpt: >-
  Explore CleverTap’s newest capabilities, designed to optimize engagement and
  retention at scale.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Stay updated with CleverTap's latest feature releases, cutting-edge feature enhancements, and performance enhancements to help you optimize your experience.

View previous updates in [What's New: 2024](https://docs.clevertap.com/docs/release-notes-2024). 

<ClickableTilesForWhatsNew />

# Release Type Legend

<TypesOfRelease />

<HTMLBlock>{`
<style>
  .filters {
    margin-top: 40px;
  }

  .filters h1 {
    font-size: 24px;
    font-weight: 600;
    margin-bottom: 16px;
  }

  .filter-box {
    background-color: #f8f9fc;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 24px 32px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.04);
  }

  .filter-options {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px 32px;
  }

  .filter-option {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 14px;
    font-weight: 500;
  }

  .filter-option img {
    width: 20px;
    height: 20px;
  }
</style>

<div class="filters">
  <h1>Filter By Feature</h1>
  <div class="filter-box">
    <div class="filter-options">
      <label class="filter-option">
        <input type="checkbox" id="filter-security-project-settings" />
        <span class="security-project-settings">
          <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
          Security & Project Settings
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-data-and-integrations" />
        <span class="data-and-integrations">
          <img src="https://files.readme.io/bf86621cc6be2995b3a9323ccfcaae0e172d6da76b2bfedc7983c5be75eb179d-Partners_Icon_Outlined.svg" alt="Data & Integrations" />
          Data & Integrations
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-analytics" />
        <span class="analytics">
          <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" />
          Analytics
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-segments" />
        <span class="segments">
          <img src="https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg" alt="Segments" />
          Segments
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-campaigns" />
        <span class="campaigns">
          <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
          Campaigns
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-journeys" />
        <span class="journeys">
          <img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" />
          Journeys
        </span>
      </label>

			<label class="filter-option">
        <input type="checkbox" id="filter-promotions" />
        <span class="promotions">
          <img src="https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg" alt="Promotions" />
          Promotions
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-conversations" />
        <span class="conversations">
          <img src="https://files.readme.io/ae95d26dd8714ac2522e7a2b39166d95ace62433496df35d5dcc4d90414527bd-Conversations.svg" alt="Conversations" />
          Conversations
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-product-experiences" />
        <span class="product-experiences">
          <img src="https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg" alt="Product Experiences" />
          Product Experiences
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-content-manager" />
        <span class="content-manager">
          <img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" />
          Content Manager
        </span>
      </label>
    </div>
  </div>
</div>
`}</HTMLBlock>

# 2024

## December

<HTMLBlock>{`
<div class="release-note article" data-category="content-manager" id="Reusable-Content-Blocks">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Reusable-Content-Blocks"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" /></div>
    <div><h3>Introducing Reusable Content Blocks for Greater Efficiency</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce Content Blocks in CleverTap’s Content Manager. Content Blocks are reusable snippets for standardized elements, such as footers, logos, or disclaimers.</p>
  <div style="text-align: center;">
  <img src="https://files.readme.io/686373549b6ac569fd3abb3ab7bafddabdd0b37236d60ce08b551e2a559309e1-image.png" alt="Footer Standardization with Content Blocks" />
  <p class="caption" style="margin-top: 8px;"><em>Footer Standardization with Content Blocks</em></p>
</div>
    <p>These blocks are designed to simplify the reuse of content across email campaigns, saving you valuable time. They help you maintain consistent messaging and standardize your brand communication.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/content-blocks" target="_blank">Content Blocks</a> and <a href="https://developer.clevertap.com/docs/content-blocks-api" target="_blank">Content Block APIs</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Store-Messages-Archiving">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Store-Messages-Archiving"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Store Outgoing Messages Using Message Archiving</h3></div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>Message Archiving now supports Google Cloud Platform (GCP), allowing customers to store copies of outgoing messages across different channels in real-time directly in their GCP bucket. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets, Azure Blob, and GCP buckets.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/message-archiving" target="_blank">Message Archiving</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Customizable-URL-Schema-SMS">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Customizable-URL-Schema-SMS"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Introducing Customizable URL Schema for SMS Campaigns</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce a new enhancement that allows you to shorten and customize the links in your SMS messages. This means you can create links that match your brand, comply with TRAI regulations, and ensure smooth delivery to customers, all while improving campaign performance.</p>
    <p>With this enhancement, you can include sender IDs in SMS URLs for seamless DLT whitelisting and create personalized URL structures that align with your branding. This ensures uninterrupted delivery and enhances customer engagement.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/sms-regulations#url-whitelisting-for-sms-marketing-campaigns" target="_blank">URL Whitelisting for SMS Marketing Campaigns</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Enhanced-Delivery-Triggers-Web-Popups">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Delivery-Triggers-Web-Popups"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Enhanced Delivery Triggers for Web Pop-ups</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to unveil our new and improved web pop-up triggers that enable timely and relevant messaging. The new triggers are based on various user interactions, such as scrolling behavior, inactivity, encountering a timed delay, or attempting to exit the webpage on a desktop.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-web-popup#triggers-for-campaign-delivery" target="_blank">Triggers for Campaign Delivery</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Analyze-Notifications-Journey-Labels">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Analyze-Notifications-Journey-Labels"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Analyze Notifications Sent Using Journeys Labels</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>You can now use Journey labels in the <em>Analytics</em> section to analyze the <em>Notifications Sent</em> event. You can now easily track and derive insights from notifications sent through Journeys tagged with specific labels.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/7f26df255f646c42fcdfbb0a6760afa7be9495d671c751f7d2d28431e2000008-Analyze_Journey_Performance_Using_Journey_Label.png" alt="Analyze Journey Performance Using Journey Labels" />
  <p class="caption" style="margin-top: 8px;"><em>Analyze Journey Performance Using Journey Labels</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/journeys-list#assign-label-to-journeys" target="_blank">Assign Label to Journeys</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Enhanced-Entry-Timelines-Journey-Setup">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Entry-Timelines-Journey-Setup"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Enhanced Entry Timelines in Journey Setup</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap has redesigned <em>Journey Entry Timelines</em> to remove redundancies and improve usability. Also, the error handling has been improved to manage scenarios such as incorrect date or day of recurrence inputs.</p>
    <p>These enhancements ensure a smoother, more intuitive Journey setup process for all CleverTap users.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-journey#define-the-journey-entry-timelines" target="_blank">Define Journey Entry Timelines</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Custom-Headers-Message-Extras">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Custom-Headers-Message-Extras"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Custom Headers and Message Extras for Enhanced Email Analytics</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now enhance your email tracking and analytics capabilities with Custom Headers and Message Extras. This feature enables you to add key-value pairs to email headers and bodies, offering seamless integration with third-party tools and internal systems. It is available for users with Sendgrid, Amazon SES, Generic SMTP, and Infobip (Advanced Email Add-on).</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-email-custom-kv#custom-headers" target="_blank">Custom Headers</a> and <a href="https://docs.clevertap.com/docs/create-message-email-custom-kv#custom-extras" target="_blank">Message Extras</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

## November

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="AppsFlyer-OneLink-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#AppsFlyer-OneLink-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>AppsFlyer OneLink Integration for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Introducing the updated AppsFlyer OneLink integration for Email. This new version makes it easier for users to set up and track clicks by managing everything from the AppsFlyer dashboard. You no longer need to configure anything on the CleverTap dashboard. The setup is now fully managed from the AppsFlyer dashboard itself, removing the need for configuration on CleverTap.</p>
    <p>The older integration is no longer available, so you must switch to the new setup to keep using it. Currently, this integration supports Sendgrid ESP only. To enable it, contact <a href="https://www.appsflyer.com/company/contact/" target="_blank">AppsFlyer support</a>.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/appsflyer-onelink#set-up-appsflyer-onelinks" target="_blank">AppsFlyer OneLink Integration</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Campaign-ID-Personalization-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Campaign-ID-Personalization-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Campaign ID Personalization for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Campaign ID Personalization is now available in both the <em>Email HTML (Rich Media) Editor</em> and <em>Drag & Drop Editor</em>, giving you more flexibility when personalizing email campaigns. You can create unique links and track engagements more accurately.</p>
    <ul>
      <li>Personalize URLs with campaign IDs for better attribution and tracking.</li>
      <li>Integrate easily with external tools to analyze engagement and meet custom analytics needs.</li>
      <li>Automate workflows using campaign IDs as payloads for custom key-value pairs.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/personalize-message-email#campaign-id-personalization" target="_blank">Campaign ID Personalization</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Event-Personalization-Email-24hrs">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Event-Personalization-Email-24hrs"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Event Personalization Beyond 24 Hours for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now apply Event Personalization to <em>Live Action</em> and <em>Date Time</em> campaigns with a delay of more than 24 hours. Create highly personalized Email campaigns based on event properties broadening the window for event-triggered communications to create custom-tailored notifications, driving better targeting and relevance.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/personalize-message-email" target="_blank">Personalize Message</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="OAuth-2.0-Webhook-Campaigns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#OAuth-2.0-Webhook-Campaigns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>OAuth 2.0 for Webhook Campaigns</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to offer a more secure and streamlined way to connect to your webhook endpoints. By adopting OAuth 2.0 authentication, we align with industry-standard security protocols to safeguard your interactions with external APIs while improving efficiency and ease of use.</p>
    <p>Enhance your Webhook security and efficiency with:</p>
    <ul>
      <li><strong>OAuth 2.0 Authentication:</strong> Robust security for webhook connections.</li>
      <li><strong>Flexible Grant Types:</strong> Support for <em>Password Credentials</em> and <em>Client Credentials</em>.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-webhooks#oauth-20" target="_blank">OAuth 2.0</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Amazon-SES-Email-HTTP">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Amazon-SES-Email-HTTP"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Amazon SES Email Delivery via HTTP Protocol</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap’s email delivery system now supports the HTTP protocol with Amazon Simple Email Service (SES), enabling faster and more efficient email delivery compared to the traditional SMTP protocol.</p>
    <p>Existing Amazon SES integrations that are using SMTP can now switch to HTTP by updating the provider setup with the required additional details.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/amazon-simple-email-service" target="_blank">Amazon Simple Email Service (SES)</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Azure-Blob-Support-Archiving">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Azure-Blob-Support-Archiving"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Support for Azure Blob in Message Archiving</h3></div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>Message Archiving now supports Azure Blob. It allows customers to store copies of outgoing messages across different channels in real-time. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets and Azure Blob.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/message-archiving" target="_blank">Message Archiving</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

## October

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="WhatsApp-Carousel-Gupshup">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#WhatsApp-Carousel-Gupshup"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>WhatsApp Carousel Templates Now Available for Gupshup</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce that carousel templates are now available for CleverTap using Gupshup with CleverTap. You can now create interactive WhatsApp campaigns with up to 10 dynamic carousel cards, allowing recipients to scroll through engaging content.</p>
    <p>With Carousel Templates on CleverTap Gupshup, you can now:</p>
    <ul>
      <li><strong>Message Bubble:</strong> Offers up to 1024 characters for detailed context.</li>
      <li><strong>Carousel Cards:</strong> Each card includes:
        <ul>
          <li><strong>Card Header:</strong> Add a media type which can be either Image or Video.</li>
          <li><strong>Card Body:</strong> Add up to 160 characters for concise messaging.</li>
          <li><strong>Card Buttons:</strong> Add up to two action buttons per card.</li>
        </ul>
      </li>
    </ul>
    <p><strong>Use Cases:</strong></p>
    <ul>
      <li><strong>E-commerce:</strong> Showcase products or promote flash sales to drive purchases.</li>
      <li><strong>Fintech:</strong> Highlight investment options or provide financial education.</li>
      <li><strong>Food Delivery:</strong> Display menu highlights or specialty dishes to entice users.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/gupshup" target="_blank">Gupshup</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Live-Behavior-Event-Personalization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Live-Behavior-Event-Personalization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Introducing Event Personalization Beyond 24 Hours for Live Behavior Campaigns</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now apply Event Personalization to Live Action and Date time campaigns with a delay of more than 24 hours. You can create highly personalized push campaigns based on event properties to create custom-tailored notifications, driving better targeting and relevance. It also extends the reach of event-triggered communications hours to increase engagement rates and conversions.</p>
    <p>For example, streaming applications can now engage users with personalized messages, even days after their last session, ensuring continued engagement.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-advanced-personalization#push-editor" target="_blank">Create Push Notification</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" id="Compare-Trends-Across-Time">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Compare-Trends-Across-Time"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" /></div>
    <div><h3>Compare Trends Across Time</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now compare an event across different time periods. For example, a user can display the count of users for the <em>Charged</em> event for Week 1 and Week 2 in the same chart. The trend line for Week 2 will be displayed as a dotted line so that it is easy to distinguish it from the Week 1 trend line. It helps create a visual comparison to quickly spot trends and differences across time frames.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/a105d0d551ff34f815b22214179e27afbc372155fd0719d07a83baf0bca32217-trends_compare.gif" alt="Compare Trends Between Different Time Periods" />
  <p class="caption" style="margin-top: 8px;"><em>Compare Trends Between Different Time Periods</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/trends-v2#compare-trends-between-time-periods" target="_blank">Compare Trends Between Time Periods</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Notification-Failed-Event">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Notification-Failed-Event"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Notification Failed Event for Email Analytics</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Announcing a significant enhancement to our Email Analytics: the <strong>Notification Failed</strong> event that gives you more deeper insights into campaign errors. With this update, CleverTap captures a <em>Notification Failed</em> event, along with the reason for failure, enabling better targeting and resolution.</p>
    <ul>
      <li><strong>Improved Targeting:</strong> Target users through alternate channels when errors occur. For example, if users encounter soft bounce errors, you can re-target them via other channels.</li>
      <li><strong>Cleaner Email List:</strong> Unsubscribe users with persistent errors to maintain an accurate and engaged subscriber base.</li>
      <li><strong>Error Analysis:</strong> Analyze the root causes of errors to resolve issues and optimize future engagements.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/events#:~:text=Notification%20Failed,in%20the%20campaign" target="_blank">Notification Failed Event</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Subscription-Group-Insights-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Subscription-Group-Insights-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Subscription Group Insights in Email Campaign Analytics</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>The new Subscription Group Insights in Email Campaign Analytics will allow you to have a more granular view of unsubscribes by subscription group providing detailed insights, including:</p>
    <ul>
      <li><strong>Group-Level Unsubscribes and Resubscribes:</strong> Track the number of unsubscribes and resubscribes for each targeted subscription group from your campaign stats.</li>
      <li><strong>Comprehensive Subscription View:</strong> View the activities of the targeted subscription groups. Additionally, you can track any changes made through the Email Preference Center for other subscription groups.</li>
      <li><strong>Enhanced Analytics:</strong> Understand user behavior better by analyzing how different subscription groups engage with your campaigns.</li>
    </ul>
    <p>For more information, refer to the documentation links below:</p>
    <ul>
      <li><a href="https://docs.clevertap.com/docs/email-campaign-stats-cc-bcc-group-unsubscribe" target="_blank">Campaign Stats (for customers with cc/bcc Beta)</a></li>
      <li><a href="https://docs.clevertap.com/docs/email-stats" target="_blank">Campaign Stats (all other customers)</a></li>
    </ul>
  </div>
</div>
`}</HTMLBlock>

w

<HTMLBlock>{`
<style>
  nav#hub-sidebar { display: none; }
  
  #content-head h1 {
    font-weight: 500 !important;
    font-size: 35px !important;
  }
  
   .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  
  .release-heading-container {
    display: flex;
    align-items: center;
    gap: 5px;
  }
  
  .release-note-heading{
  }
  
  .release-note-body img{
    border: 1px solid rgb(0,0,0,0.2)
  }
  
  .filters h3 {
  margin-bottom: 12px;
  font-size: 20px;
}

.filter-options {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  align-items: center;
}

.filter-option {
  flex: 0 0 calc(33.33% - 14px);
  color: #4A4C4C;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 16px;
  white-space: nowrap;
}

  .filter-option:hover{
  	cursor:pointer;
    color:#191919;
  }

.filter-option img {
  width: 16px;
  height: 16px;
  color:#4A4C4C;
}

 .filter-option img:hover {
  fill:red;
}

.content-manager {
	display: flex;
  align-items: center;
  gap: 8px;
}

.badges {
  display: flex;
  gap: 4px;
  flex-wrap: wrap;
  align-items: center;
}
  
.badge {
    font-size: 12px;
    font-weight: 700;
    color: white;
  	padding:0px 4px;
    border-radius: 5px;
    display: inline-block;
		min-width: max-content
}
  
  .anchor-link-icon {
  margin-left: -23px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

/* Show the anchor icon on hover */
.release-note-header:hover .anchor-link-icon {
  opacity: 1;
}
 
 .anchor-link-icon{
  	margin-left:-23px;
  }
.anchor-link-icon-inline {
  display: flex;
  align-items: center;
  font-size: 1.2em;
}
  
.release-note-header{
  display:flex;
  gap:8px;
  align-items: center;
 }
  
.private-beta {
    background-color: #B0B0B0;
}
  
.beta {
    background-color: #9E9E9E;
}
  
.new-feature {
    background-color: #4CAF50;
}
  
.enhancement {
    background-color: #2962FF;
}
  
.update {
    background-color: #673AB7;
}
  
/* Hide all articles by default */
.article {
  display: none;
}

/* Show all articles if no filters are checked */
body:not(:has(.filters input:checked)) .article {
  display: block;
}
  
* .rm-Guides a.suggestEdits {
    display: none;
  }

/* Show matching articles */
  body:has(#filter-campaigns:checked) .article[data-category="campaigns"],
	body:has(#filter-promotions:checked) .article[data-category="promotions"],
	body:has(#filter-conversations:checked) .article[data-category="conversations"],
	body:has(#filter-analytics:checked) .article[data-category="analytics"],
	body:has(#filter-segments:checked) .article[data-category="segments"],
	body:has(#filter-journeys:checked) .article[data-category="journeys"],
	body:has(#filter-data-and-integrations:checked) .article[data-category="data-and-integrations"],
	body:has(#filter-product-experiences:checked) .article[data-category="product-experiences"],
	body:has(#filter-content-manager:checked) .article[data-category="content-manager"],
	body:has(#filter-security-project-settings:checked) .article[data-category="security-project-settings"]{
  display: block;
}
  
</style>
`}</HTMLBlock>
