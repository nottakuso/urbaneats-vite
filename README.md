# Urbaneats (Static HTML/CSS/JS)

A simple, responsive food ordering MVP built with plain HTML, CSS, and JavaScript. Uses localStorage for cart and submits orders via email (mailto) or WhatsApp. Ready to host on Netlify/Vercel/GitHub Pages.

## Structure
- `index.html` – Landing
- `menu.html` – Browse products (from `data/products.json`)
- `product.html` – Product details (variants / add-ons)
- `cart.html` – Cart management
- `checkout.html` – Order summary and submission
- `order-success.html` – Confirmation
- `assets/css/styles.css` – Styles
- `assets/js/app.js` – Settings and helpers
- `assets/js/cart.js` – Cart logic
- `data/products.json` – Catalog data

## Settings
Update currency, tax, delivery fee, and contact in `assets/js/app.js` (SETTINGS):
```js
export const SETTINGS = {
  currency: 'GBP',
  symbol: '£',
  taxRate: 0.07,
  deliveryFee: 2.5,
  ordersEmail: 'orders@example.com',
  businessPhone: ''
};
```

## Running
For local testing with module imports and fetch, use a static server (recommended):
- VS Code Live Server, or
- `npx serve` in the project folder, or
- Host on Netlify/Vercel/GitHub Pages

## Customize
- Replace images in `assets/img/`
- Edit products and categories in `data/products.json`
- Adjust colors in `assets/css/styles.css` (`--brand`)

## Notes
- Email (mailto) opens the user's default mail client. For production email/webhook, add a backend or Formspree.
- WhatsApp uses `SETTINGS.businessPhone` (international format).
