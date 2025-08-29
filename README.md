# Lucrose-Pharma-WhatsApp-Store-
# Lucrose Pharma – WhatsApp Store

Single-file, mobile-first micro-store for Lucrose Pharma built with Tailwind (CDN) + vanilla JS. Customers can browse medicines by category, add to cart, and place orders via WhatsApp Click‑to‑Chat with fully itemized order summary. [Guided by WhatsApp click-to-chat formats and Tailwind responsive patterns.]

[![made-with-tailwind](https://img.shields.io/badge/Made%20with-TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![license-MIT](https://img.shields.io/badge/License-MIT-green.svg)](#license)
[![deploy-static](https://img.shields.io/badge/Deploy-Static%20Hosting-blue)](#deployment)
[![whatsapp-order](https://img.shields.io/badge/Order-WhatsApp-success?logo=whatsapp)](#how-order-works)

## Features
- Single HTML file using Tailwind via CDN (no build step) for quick deploys.  
- Category-wise product listing, search and filter, and a cart drawer with overlay.  
- WhatsApp Click‑to‑Chat: prefilled, URL‑encoded multiline order message (name, address, items, totals).  
- Free Delivery rule: Shipping ₹0 for orders ≥ ₹1,000; else ₹49.  
- Mobile-first UI, sticky header, floating WhatsApp button, and responsive layout.

## Demo
- Live: Add your deployed URL (e.g., GitHub Pages, Netlify, Vercel).
- Screenshot: Add a screenshot of the homepage/cart.

## Tech Stack
- HTML + Tailwind CSS (CDN utilities)  
- Vanilla JavaScript (no frameworks)  
- WhatsApp Click‑to‑Chat for order workflow

## Getting Started
1. Clone the repo:
   git clone https://github.com/your-username/Lucrose-Pharma-WhatsApp-Store.git
   cd Lucrose-Pharma-WhatsApp-Store
2. Open index.html in a browser (double-click or serve with any static server).
3. Update business details:
   - WhatsApp number in JS: const WA_NUMBER = "918546095691"
   - Logo: replace LOGO_URL_HERE in header <img> (or put assets/logo.png and point to it).
   - Products/MRP: edit catalogData in index.html.
4. Optional: Host on GitHub Pages (Settings → Pages → Deploy from main /root).

## How Order Works
- Click “Add” to collect items in the cart → Open cart drawer → Fill name, address, payment → “Order on WhatsApp”.  
- The site opens WhatsApp chat to the configured number with an itemized, URL‑encoded message including subtotal, shipping, tax (0 placeholder), and total.  

## Configuration
- Free delivery threshold: change subtotal >= 1000 in calcTotals().  
- Shipping charge (below threshold): change 49 in calcTotals().  
- Tax: currently 0; integrate as needed.  
- Categories & Products: edit in the catalogData array.

## Customize Look & Feel
- Colors: adjust CSS vars in <style> or Tailwind utility classes inline.  
- Logo: use transparent PNG/SVG for best results.  
- Cards/spacing: tweak utility classes in renderCatalog().

## Accessibility
- Logo has alt text “Lucrose Pharma”.  
- Buttons have clear labels; consider adding aria-labels if needed.

## Security/Privacy
- No backend or data storage.  
- All checkout occurs in WhatsApp chat initiated by the customer.

## Known Limitations
- No inventory/stock validation.  
- Taxes/discounts not auto‑computed.  
- No persistent cart across refresh (in-memory only).

## Roadmap
- LocalStorage cart persistence  
- Coupon/discount logic  
- Category images and product thumbnails  
- Multi-language support (EN/HI)

## Contributing
Pull requests welcome. For major changes, open an issue to discuss what you’d like to change.

## License
MIT © Your Name
See the LICENSE file for details.
