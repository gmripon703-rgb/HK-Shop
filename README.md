# NovaDrop - Dropshipping Store with Cart, Cash on Delivery & Admin Dashboard

A high-converting, single-page dropshipping storefront featuring a fluid shopping cart, Cash on Delivery (COD), local mobile payments (bKash, Nagad, Rocket, Bank Transfer), real-time inventory synchronization, and a built-in **Admin Dashboard** for sales tracking and product management. Styled with a **Navy Blue Light Mix** theme.

---

## 🚀 How to Publish to GitHub & Deploy to Cloudflare Pages / Workers

Follow these simple steps to put your store online with worldwide CDN speed and free SSL:

### Step 1: Push to GitHub

1. Create a new repository on [GitHub](https://github.com/new) (e.g. `novadrop-store`).
2. In your local terminal or workspace root, run:
   ```bash
   git init
   git add .
   git commit -m "feat: complete dropshipping store with cart, COD, admin dashboard & navy UI"
   git branch -M main
   git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPOSITORY_NAME>.git
   git push -u origin main
   ```

---

### Step 2: Deploy to Cloudflare Pages (Recommended - 100% Free)

Cloudflare Pages automatically builds your site and distributes it across 300+ edge locations worldwide with automatic continuous deployment on every Git push.

1. Log into your [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. In the left navigation, click **Compute (Workers & Pages)** > **Create application** > **Pages** tab.
3. Click **Connect to Git** and authorize your GitHub account.
4. Select your `novadrop-store` repository.
5. In the **Build configuration** screen, enter:
   - **Project Name**: `novadrop-store` (or your choice)
   - **Framework preset**: `Vite`
   - **Build command**: `npm run build`
   - **Build output directory**: `dist`
   - **Root directory**: `/` (leave blank or default)
6. Click **Save and Deploy**.
7. In ~30-45 seconds, your storefront will be live at `https://novadrop-store.pages.dev`!

---

### Step 3: Deploy via Cloudflare Workers / Wrangler CLI (Alternative)

If you prefer deploying directly via the command line with Wrangler:

```bash
# 1. Install dependencies & build
npm install
npm run build

# 2. Deploy to Cloudflare Pages directly
npx wrangler pages deploy dist --project-name=novadrop-store
```

The configuration is already defined in `wrangler.toml` and `public/_headers`.

---

## 🛒 Key Storefront Features

- **Navy Blue Light Mix Theme**: Deep luxury navy palette (`#070D1F` to `#1E293B`) with ambient glowing sapphire and warm gold/amber accents.
- **Wonderful Shopping Cart**:
  - Slide-over drawer with itemized goods, custom quantity steppers, and free shipping progress meter.
  - Live coupon codes (e.g. `WELCOME10` for 10% off).
- **Cash on Delivery (COD) & Local Mobile Checkout**:
  - Full support for zero-advance COD: customers inspect the parcel upon courier arrival before paying.
  - Local Mobile Wallet options: bKash, Nagad, Rocket, or direct Bank Transfer with one-click copy number and Transaction ID (TrxID) input.
  - Automatic customer details verification (Full Name, Phone, Address, City/District).
  - Post-order success screen with tracking number, timeline, and direct **"Notify via WhatsApp"** button.
- **Admin Dashboard**:
  - Click **"Admin Panel"** in the top navigation bar.
  - **Sales Tracking**: Total Revenue, Total Orders, COD Pending count, and Average Order Value (AOV).
  - **Live Orders Manager**: View and manage customer orders, update dispatch status, and mark payments as received.
  - **Product Manager**: Add new products to the live store, adjust stock counts, or delete items.
  - **Payment Settings**: Update your official bKash, Nagad, and WhatsApp notification numbers anytime.
- **Mobile Sticky Action Bar**:
  - Touch-optimized bottom bar for instant cart view and 1-tap COD ordering on mobile devices.
- **Single-File Standalone Export**:
  - Click **"Export (PHP/HTML)"** to download self-contained single-page templates (`standalone-store.html` or `index.php`) ready to drop into any shared cPanel or Apache/Nginx web server.

---

## 🛠 Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview build
npm run preview
```
