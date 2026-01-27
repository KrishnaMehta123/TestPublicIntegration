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

This section explains how to import data into CleverTap from external sources. Depending on your requirements, you can upload data in bulk, automate ingestion from backend systems, or import historical records to ensure continuity in reporting and engagement.

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
<a href="https://docs.clevertap.com/docs/data-warehouse-import" class="integration-card">
    <div class="name">Data Warehouse</div>
  </a>
</div>
`}</HTMLBlock>
