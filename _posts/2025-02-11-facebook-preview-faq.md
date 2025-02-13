---
title: Troubleshooting Facebook Link Previews - FAQ for BrandGhost Users
description: Facebook’s API has some quirks when handling links, and we’re here to help you resolve them
author: BrandGhost
date: 2025-02-13 00:00:00 +0800
categories: [Content Strategy, Social Media]
tags:
  [social media, brand, content, content strategy, evergreen, posting topics]
pin: true
math: true
mermaid: true
image: ""
---

# Troubleshooting Facebook Link Previews - FAQ for BrandGhost Users

Are your Facebook posts missing link previews when posting via BrandGhost? You’re not alone! Facebook’s API has some quirks when handling links, and we’re here to help you resolve them. Below are the most common questions and solutions.

---

## Why isn't my Facebook post showing a link preview?

When posting a link to Facebook via the API, Facebook needs to scrape the URL to generate a preview. If the preview isn’t appearing, it could be due to:

- Missing or incorrect Open Graph meta tags on your website.

- Facebook not scraping the URL before posting.

- Issues with your Facebook Page’s settings or permissions.

- A caching issue on Facebook’s side.

---

## How can I check if my link has the right Open Graph meta tags?

Facebook relies on Open Graph (OG) meta tags to generate previews. To ensure your page is properly set up:

1. Open the Facebook [Sharing Debugger](https://developers.facebook.com/tools/debug/)

2. Enter your URL and click Debug.

3. If you see errors or missing tags, update your website’s <head> section with the following tags:

```
<meta property="og:title" content="Your Page Title" />
<meta property="og:description" content="A brief description of your page." />
<meta property="og:image" content="https://yourdomain.com/image.jpg" />
<meta property="og:url" content="https://yourdomain.com" />
```

4. After updating, click Scrape Again in the Sharing Debugger to refresh Facebook’s cache.

---

## Keep Posting!

By following these troubleshooting steps, you can ensure your Facebook posts look great and drive engagement. Keep creating and sharing with confidence using BrandGhost!
