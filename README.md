# Apni Kirana — Free Direct-Order E-Commerce Website

A mobile-first grocery e-commerce front end built with HTML, CSS and vanilla JavaScript.

## Features

- Responsive home page and product catalogue
- Search + category filters
- Product details and related products
- LocalStorage shopping cart
- Checkout form
- Cash on Delivery + configurable UPI
- Order ID generation
- WhatsApp order message generation
- Local order tracking
- Hindi browser SpeechSynthesis feedback
- LocalStorage product/order admin demo
- No paid backend required for the demo
- GitHub Pages / Netlify / Cloudflare Pages compatible

## 1. Configure your shop

Open `script.js` and change:

```js
const SHOP_WHATSAPP = "91XXXXXXXXXX";
const SHOP_PHONE = "91XXXXXXXXXX";
const SHOP_UPI_ID = "yourupi@upi";
const SHOP_NAME = "Apni Kirana";
const DELIVERY_CHARGE = 30;
const FREE_DELIVERY_ABOVE = 499;
```

For WhatsApp and phone, use country code without `+` or spaces.

Example:

```js
const SHOP_WHATSAPP = "919876543210";
```

## 2. Run on your phone/computer

You can simply open `index.html` in a modern browser.

For the best development experience, use VS Code + Live Server, or any simple local web server.

## 3. Free hosting — GitHub Pages

1. Create/sign in to a GitHub account.
2. Create a new repository, for example `apni-kirana`.
3. Upload:
   - `index.html`
   - `style.css`
   - `script.js`
   - `README.md`
4. Open repository Settings → Pages.
5. Select **Deploy from a branch**.
6. Select the `main` branch and `/root`.
7. Save.
8. GitHub will provide your public website address.

## 4. Free hosting — Netlify

1. Create/sign in to Netlify.
2. Choose **Add new site** → **Deploy manually** (wording may vary).
3. Drag the project folder containing `index.html`, `style.css`, and `script.js` into the upload area.
4. Netlify will give you a free `netlify.app` address.
5. You can later connect a custom domain.

## 5. Cloudflare Pages

Upload the same project to a Git repository and create a Pages project from that repository. No server-side code is required for this front end.

## Important production warning

The admin panel in this project uses browser `localStorage`. That means products/orders are stored only in the browser that is using the website. It is NOT a secure shared admin system.

For a real business with multiple customers and a shop owner dashboard, use a real backend/database/authentication system (for example Supabase, Firebase, or a custom server). Do not store sensitive customer information in an unsecured client-only admin panel.

## Payment warning

The UPI section creates a UPI payment intent and QR when a valid UPI ID is configured. It does not automatically verify payment. For automatic payment verification, integrate a legitimate payment gateway/backend.

## Product images

The demo products use remote Unsplash image URLs. Replace them with your own product images for production. If you want fully self-contained hosting, download your own images into an `images/` folder and change the `image` fields in `script.js`.

## Main customer flow

Browse → Search → Product → Add to Cart → Checkout → Place Order → Order Confirmation → Send Order to WhatsApp

