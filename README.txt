KST3D — STATIC HTML WEBSITE
Version 2.2.0 | Exported 3 October 2026

READY TO DEPLOY
This folder contains the built website: HTML, CSS, JavaScript, product photos,
favicon, 3D rendering code, licences and Vercel configuration.
No npm install, build command, API key or environment variable is required.
Keep all folders together and deploy this directory as the website root.

GITHUB + VERCEL
1. Push the contents of this KST3D folder to your GitHub repository.
2. Import that repository into Vercel.
3. Use Framework Preset: Other; Root Directory: repository root.
4. Leave Build Command and Install Command empty; Output Directory: .
The included vercel.json already supplies these settings and static asset caching.
If your repository contains the outer KST3D folder, use KST3D as Root Directory.
Then deploy. This export has been checked locally; it has not been published.
Official reference: https://vercel.com/docs/builds/configure-a-build

LOCAL PREVIEW
Open Terminal in this folder and run:
  python3 -m http.server 8000
Open http://localhost:8000 in your browser.
Use a local web server, rather than double-clicking index.html, so module loading
and product URLs work correctly.

CONTENTS
index.html                  Home page
collections/all/index.html  Collection page
products/*/index.html       Eight individual product pages
products/*.webp             Product photography
assets/                     Built JavaScript and CSS, including Three.js
favicon.svg                 Site icon
licenses/                   Third-party licence notices
vercel.json                 Static hosting and cache settings

PERFORMANCE
The 3D renderer pauses offscreen, in background tabs and while dialogs are open.
Model geometry is reused. Identical details are drawn together; their visual
resolution is unchanged. Scroll progress uses cached measurements and transforms.
3D loads separately from shopping and help. Versioned asset names allow reliable
browser caching without keeping stale JavaScript after updates.

PROTOTYPE FEATURES
The catalogue, product pages, interactive models, print-scroll animation, local
shopping bag, print guide and WhatsApp links are included. The bag is saved in the
visitor's browser. Orders are enquiries sent through WhatsApp; this static export
does not process payments or connect to Shopify checkout. The print guide answers
locally and does not access orders or an AI service. Video areas remain empty for
your footage. Quote files are not uploaded; customers attach them in WhatsApp.
Product data matches the approved prototype and does not automatically update
from a Shopify store.

FONTS
Switzer loads from Fontshare's CDN; Helvetica/Arial are fallback fonts.
Its licence permits website use but restricts redistributing the font binaries in
repositories, so those binaries are not included in this GitHub export.
All application code and product images are included locally.

EDITING
These are production files. For larger edits, use the accompanying editable
KST3D-Website-Source.zip, run npm install and npm run build, then:
  npm run export:static -- /path/to/KST3D
Replace the deployed export with that newly generated folder.
