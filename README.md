# INNI website: deployment

This folder is the complete website. Upload **everything inside it** to your web host's root folder (often called `public_html` or `www`).

## What's here
- `index.html`: the site. Opening your domain loads it.
- `support.js`: required. It must sit next to `index.html`.
- `content/`: the editable master lists (see *HOW TO ADD CONTENT.md*).
- `images/`: all images, split into site / artists / releases / merch / management.

## Hosting
- It works on any static host: Netlify, Vercel, GitHub Pages, Cloudflare Pages, or ordinary shared hosting (cPanel, FTP). No database or server code is needed.
- It must be served over **http/https**. Double-clicking `index.html` on your computer will show an empty site, because browsers block reading the content files from disk. To preview locally, run `npx serve` in this folder, or drag the folder onto app.netlify.com/drop.
- Page links use `#`, e.g. `innimusic.com/#/release/years`, so no redirect or rewrite rules are needed.
- The site loads React from unpkg.com, and the buy buttons load from Shopify. The visitor's browser needs internet access to both.

## Updating content
Edit the files in `content/` and add images to `images/`, then re-upload the changed files. Changes appear on the next page load; the content files are never cached.

## Shopify
Your store domain and public Storefront token are in `content/shop.json`. This token is designed to be public. In Shopify, make sure the Buy Button sales channel lists your live domain.
