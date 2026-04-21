# Saddam Burger - Cloudflare Pages eCommerce Website

A modern, mobile-friendly, high-speed eCommerce website for Saddam Burger, optimized for Cloudflare Pages.

## Features

- 🍔 Modern food delivery UI inspired by Foodpanda/McDonald's/KFC
- 📱 Fully responsive mobile-first design
- 🛒 AJAX cart system without page reloads
- 📱 Direct WhatsApp ordering (+92 301 1118099)
- 🔢 Auto-generated Order IDs with date/time
- 🎫 Coupon code support
- ⚡ Super fast loading speed
- 📊 SEO optimized

## Deployment to Cloudflare Pages

### Option 1: Using Wrangler CLI (Recommended)

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Create a Cloudflare API Token:**
   - Go to https://dash.cloudflare.com/profile/api-tokens
   - Create a new token with "Cloudflare Pages: Edit" permissions

3. **Set your API token:**
   ```bash
   export CLOUDFLARE_API_TOKEN="your_api_token_here"
   ```

4. **Deploy:**
   ```bash
   npm run deploy
   ```
   
   Or directly:
   ```bash
   npx wrangler pages deploy ./public --project-name=saddamburger
   ```

### Option 2: Using Cloudflare Dashboard (No CLI required)

1. Go to https://dash.cloudflare.com/
2. Navigate to **Workers & Pages** → **Create Application** → **Pages**
3. Click **Connect to Git** and select your repository
4. Configure build settings:
   - **Build command**: Leave empty (no build needed)
   - **Build output directory**: `public`
5. Click **Save and Deploy**

### Option 3: Manual Upload via Dashboard

1. Go to https://dash.cloudflare.com/
2. Navigate to **Workers & Pages** → **Create Application** → **Pages**
3. Click **Upload assets**
4. Create a project named `saddamburger`
5. Drag and drop the `public` folder or upload `index.html`
6. Click **Deploy**

## Local Development

Run a local development server:

```bash
npm run dev
```

Or directly:

```bash
npx wrangler pages dev ./public
```

Then open http://localhost:8788 in your browser.

## Project Structure

```
/workspace
├── public/
│   └── index.html          # Main application (single file)
├── index.html              # Copy of main application
├── package.json            # NPM configuration
├── wrangler.toml           # Wrangler configuration
└── README.md               # This file
```

## Configuration

You can customize the following in `public/index.html`:

- **WhatsApp Number**: Search for `+92 301 1118099` and replace with your number
- **Products**: Edit the `products` array in the JavaScript section
- **Categories**: Modify the `categories` array
- **Delivery Charges**: Update the `deliveryCharge` variable
- **Coupons**: Edit the `coupons` object

## Features Overview

### Homepage
- Hero banner with deals and offers
- 8 menu categories (Burgers, Zinger Burgers, Fries, Pizza, Wraps, Drinks, Deals, Combos)
- Featured products and best sellers sections
- Customer reviews
- Google Maps integration
- Sticky mobile order button

### Cart System
- Add/remove items without page reload
- Quantity controls
- Real-time subtotal, delivery, and grand total calculation
- Coupon code support

### Checkout Process
- Simple form: Name, Phone, Address, City, Notes
- Auto-generated Order ID (e.g., SB-48291)
- Automatic date and time stamp
- Professional WhatsApp invoice format

### WhatsApp Order Format
```
🍔 Saddamburger Order Confirmed

Order ID: SB-48291
Date: 21 April 2026
Time: 08:45 PM

Customer Name: Ali Raza
Phone: 03XXXXXXXXX
Address: Johar Town Lahore

Items:
1x Zinger Burger - Rs 550
2x Fries - Rs 400
1x Pepsi - Rs 120

Subtotal: Rs 1070
Delivery: Rs 150
Total: Rs 1220

Notes: No onion please

Thank you for ordering from Saddamburger 🍔
```

## Support

For issues or questions, contact via WhatsApp: +92 301 1118099

---

Built with ❤️ for Saddam Burger
