---
title: Import
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

The _Imports_ section explains how to bring external user data into CleverTap, including user profiles, past events, and historical records. It highlights the different import options available, such as bulk uploads, API-based imports, and partner integrations, giving you flexibility in how you sync data from other systems into your CleverTap account.

<HTMLBlock>{`
<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1rem;
    padding: 0 1rem;
    max-width: 100%;
    margin: 0 auto;
  }

  .integration-card {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding: 1.5rem 1rem; /* add top & bottom padding */
  min-height: 64px; /* ensures consistent tile height */
  background: #fff;
  border-radius: 12px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

  .integration-card:hover {
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  }

  .icon {
    width: 24px;
    height: 24px;
    stroke: #2b2e33;
    flex-shrink: 0;
  }

  .name {
    font-size: 1rem;
    font-weight: 600;
    color: #2b2e33;
  }
</style>

<div class="grid">
  <a href="https://docs.clevertap.com/docs/imports-via-api" class="integration-card">
    <div class="name">API</div>
  </a>
  <a href="https://docs.clevertap.com/docs/csv-upload" class="integration-card">
    <div class="name">CSV Upload</div>
  </a>
<a href="https://docs.clevertap.com/docs/imports-via-sftp" class="integration-card">
    <div class="name">SFTP</div>
  </a>
<a href="https://staging.docs.user.clevertap.net/docs/data-warehouse-imports" class="integration-card">
    <div class="name">Data Warehouse Import</div>
  </a>
</div>
`}</HTMLBlock>
