---
title: Cloud Storage
excerpt: ''
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

This section introduces the export methods that deliver CleverTap data directly to your cloud storage locations. This page provides an overview of the supported storage partners and export types so you can choose the correct approach for receiving profile or event data in your preferred cloud environment.

This section outlines the storage platforms supported for file-based exports.

[block:html]
{
  "html": "<style>\n  .grid {\n    display: grid;\n    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));\n    gap: 1rem;\n    padding: 0 1rem;\n    max-width: 100%;\n    margin: 0 auto;\n  }\n\n  .integration-card {\n  display: flex;\n  align-items: center;\n  justify-content: flex-start;\n  padding: 1.5rem 1rem; /* add top & bottom padding */\n  min-height: 64px; /* ensures consistent tile height */\n  background: #fff;\n  border-radius: 12px;\n  border: 1px solid rgba(0, 0, 0, 0.08);\n  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);\n  transition: box-shadow 0.2s ease-in-out;\n  text-decoration: none;\n}\n\n  .integration-card:hover {\n    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);\n  }\n\n  .icon {\n    width: 24px;\n    height: 24px;\n    stroke: #2b2e33;\n    flex-shrink: 0;\n  }\n\n  .name {\n    font-size: 1rem;\n    font-weight: 600;\n    color: #2b2e33;\n  }\n</style>\n\n<div class=\"grid\">\n  <a href=\"https://docs.clevertap.com/docs/data-export-to-aws-s3\" class=\"integration-card\">\n   <div class=\"name\">Amazon S3</div>\n  </a>  \n  <a href=\"https://docs.clevertap.com/docs/bigquery\" class=\"integration-card\">\n  <div class=\"name\">BigQuery</div>\n  </a>\n\t<a href=\"https://docs.clevertap.com/docs/data-export-to-gcp\" class=\"integration-card\">\n  <div class=\"name\">Google Cloud Platform (GCP)</div>\n  </a>\n\t<a href=\"https://docs.clevertap.com/docs/microsoft-azure\" class=\"integration-card\">\n  <div class=\"name\">Microsoft Azure</div>\n  </a>\n</div>"
}
[/block]


> 📘 Profile and User Exports (Legacy) vs. Profile Exports
> 
> CleverTap supports two distinct export flows, depending on your data requirements and integration needs:
> 
> - [**Profile and User Exports (Legacy)**](doc:event-and-profile-exports): Supports exporting both events and user profiles.
> - [**Profile Exports**](doc:profile-exports): The newer, enhanced export flow that supports exporting user profiles only with improved flexibility and structure.