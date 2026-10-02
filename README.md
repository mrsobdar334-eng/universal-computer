# ⚡ Universal Computer - Next-Gen 3D E-Commerce Store & Supabase Admin Hub

A modern, high-performance, futuristic 3D e-commerce store and complete Shopify theme built for **Universal Computer**, a professional international computer and electronics brand.

---

## 🌟 Key Highlights & Features

### 1. 🪐 3D Interactive WebGL Experience (Three.js)
* **Interactive 3D Hero Showcase:** Live interactive Three.js 3D viewport featuring procedural high-detail models:
  * **Laptops:** Open OLED display, backlit keyboard, glass touchpad, and illuminated brand emblem.
  * **Graphics Cards (GPUs):** Triple-fan cooling shroud with spinning axial fans, aluminum fin stacks, glowing RGB logo bar, and PCIe 5.0 gold fingers.
  * **Desktop Computers:** Tempered glass side panel, AIO CPU liquid cooler with glowing infinity mirror, dual RGB RAM modules, and front intake rings.
  * **Monitors:** Panoramic curved OLED screen with rear ambient halo ring and heavy metal stand.
  * **Peripherals:** 65% mechanical Hall-Effect magnetic keyboards, 38-gram carbon 8K gaming mice, planar magnetic audiophile headsets, and Thunderbolt 4 docks.
  * **Printers:** Precision 3D resin printer with touchscreen and illuminated vat.
* **Full Orbit & Parallax Controls:** Left-click drag to rotate in 3D space, mouse-wheel to zoom, subtle mouse parallax.
* **Aura RGB Lighting Switcher:** Live color changes (Cyan `#00f0ff`, Magenta `#ff007f`, Violet `#8b5cf6`, Emerald `#00ff88`, Amber `#ffaa00`).
* **Holographic Wireframe & Auto-Rotate Modes:** Toggle wireframe analysis mode and smooth continuous orbit.

### 2. 💻 Comprehensive Product Catalog (10 Categories & 24 Models)
* **Laptops & Portables:** CyberBlade Pro 18 (RTX 5090), Stealth Titan 16, AeroCraft UltraBook 14.
* **Desktop Gaming PCs:** Universal Quantum Apex 9000 (Liquid Custom Loop), Horizon Valkyrie Workstation, Nova Cube ITX.
* **Graphics Cards (GPUs):** ROG Matrix GeForce RTX 5090 24GB Platinum OC, MSI RTX 4080 SUPER Suprim X, Radeon RX 7900 XTX Aqua.
* **PC Components:** Intel Core i9-14900KS 6.2GHz, Corsair Dominator Titanium 64GB DDR5-7200, Samsung 990 PRO 4TB Heatsink.
* **Gaming & OLED Monitors:** Samsung Odyssey OLED G9 49" 240Hz, ASUS ROG Swift OLED 32" 4K, Alienware 34" Curved QD-OLED.
* **Keyboards & Mice:** CyberBlade 65 Rapid Trigger (0.1mm actuation), Phantom 8K Carbon Wireless (38g), Logitech G915 X.
* **Headphones & Speakers:** Quantum Planar Magnetic Hi-Res Headset, SteelSeries Arena 9 5.1 Surround.
* **Smart & 3D Printers:** Form3D 14K Resin Precision Printer, HP LaserJet Pro Ultra Duplex.
* **Wi-Fi 7 & Networking:** NETGEAR Nighthawk RS700S Tri-Band Wi-Fi 7 (19 Gbps), Ubiquiti UniFi Pro Max 16 PoE Switch.
* **Docks & Accessories:** Thunderbolt 4 Apex Titan Dual-8K Studio Dock.

### 3. 🛒 Advanced E-Commerce Capabilities
* **Live Instant Search:** Dropdown autocomplete with product thumbnails and live pricing.
* **Multi-Facet Filters:** Real-time filter by Category, Manufacturer/Brand, Price Range ($100 - $7,000), and Stock Availability.
* **Category Pills & Tabs:** Instant switching between All Hardware, Featured, Best Sellers, New Arrivals, and Gaming Rigs.
* **Slide-Out Cart Drawer:** Real-time quantity adjustment, free shipping progress bar ($500 threshold), and discount coupons (`UNIVERSAL10`, `TECH50`, `CYBERVIP`).
* **Interactive 3D Quick-View Modal:** Direct 3D inspection inside modal with full technical specifications sheet.
* **Side-by-Side Comparison Dock:** Compare up to 4 hardware models with a comprehensive specs matrix table.
* **Simulated Checkout Flow:** Real-time pricing, address capture, payment method selection, and order confirmation.
* **Live Order Tracking:** Telemetry stages from Hardware Assembly -> Cleanroom Burn-In Testing -> Air Cargo Dispatch.
* **Multi-Currency Converter:** Instant currency switching (USD, EUR, GBP, CAD, AUD, INR, JPY).
* **Audio Synthesis SFX:** Built-in Web Audio API synthesizer for tactile sci-fi sound effects and success chimes.

---

## 🛡️ Supabase Admin Panel (`admin.html`)

The admin console connects directly to your Supabase cloud backend with **100% error-free local fallback protection**:

### Features
1. **Executive Telemetry:** Real-time KPI cards for Total Revenue, Total Orders, Active Hardware Models, and Average Order Value.
2. **Catalog Inventory CRUD:** View, filter, adjust stock (+/-), delete items, or launch the **Add New Product** modal (with 3D model tag support).
3. **Orders & Fulfillment Management:** Live order tracking table with dynamic status dropdowns (`Processing`, `Shipped`, `Delivered`).
4. **Customer Directory:** Track VIP clients and purchase history.
5. **Discount Matrix:** Manage promo codes (`UNIVERSAL10`, `TECH50`, `CYBERVIP`) and track redemption numbers.
6. **Supabase Cloud Database Hub:**
   * **Masked API Credentials:** Your Supabase keys are safely masked (`sb_pub••••••••••••yEhm`, `eyJhbG••••••••••••0IU`) with an on-demand Reveal/Hide toggle.
   * **Connection Health Test:** Live latency and status check against your Supabase instance.
   * **1-Click SQL Schema Copy:** Copy the complete migration script to initialize `products`, `orders`, and `customers` tables in Supabase.
   * **Sync to Supabase:** 1-click button to push all 24 hardware catalog products directly into your Supabase database.

---

## 📂 Project Architecture

```
universal-computer/
├── index.html                           # Master 3D Storefront (Standalone web preview)
├── admin.html                           # Supabase Admin Panel
├── universal-computer-shopify-theme.zip # Ready-to-upload Shopify Theme ZIP
│
├── css/
│   ├── theme.css                        # Futuristic Dark Glassmorphism Master Design System
│   └── admin.css                        # Admin Dashboard Design System
│
├── js/
│   ├── products-data.js                 # Complete Hardware Catalog & Seed Data
│   ├── supabase-config.js               # Supabase Adapter with Masked Keys & Safe Fallback
│   ├── three-model-viewer.js            # Three.js 3D WebGL Multi-Product Engine
│   ├── theme.js                         # Storefront State, Cart, Filters & Audio Engine
│   └── admin.js                         # Admin Panel Controller
│
└── shopify-theme/                       # Complete Shopify Theme Package
    ├── layout/
    │   └── theme.liquid
    ├── sections/
    │   ├── header.liquid
    │   ├── hero-3d.liquid
    │   ├── categories-banner.liquid
    │   ├── featured-products.liquid
    │   ├── special-deals.liquid
    │   ├── customer-reviews.liquid
    │   ├── newsletter.liquid
    │   └── footer.liquid
    ├── snippets/
    │   ├── cart-drawer.liquid
    │   ├── quick-view-modal.liquid
    │   ├── compare-dock.liquid
    │   └── product-card.liquid
    ├── templates/
    │   ├── index.json
    │   ├── product.json
    │   ├── collection.json
    │   └── cart.json
    ├── config/
    │   ├── settings_schema.json
    │   └── settings_data.json
    └── assets/
        ├── theme.css
        ├── theme.js
        ├── three-model-viewer.js
        ├── products-data.js
        └── supabase-config.js
```

---

## 🚀 How to Run & Preview

### Option A: Immediate Browser Preview
Double-click `index.html` or open it in any web browser (Chrome, Edge, Firefox, Safari) to experience the full store. Open `admin.html` to access the Supabase Admin Console.

### Option B: Install on Shopify
1. In your Shopify Store Admin, navigate to **Online Store > Themes**.
2. Click **Add Theme > Upload zip file**.
3. Select `universal-computer-shopify-theme.zip`.
4. Click **Publish** to launch your futuristic 3D store!

---

## 💾 Database Architecture & Setup

The store runs out-of-the-box on a **pure local database engine** with zero API keys required.
If you ever want to connect a custom remote PostgreSQL/cloud database:
1. Open your cloud database dashboard.
2. Go to **SQL Editor > New Query**.
3. Copy the SQL schema from `admin.html` (under the **Database Manager** tab) or run:

```sql
CREATE TABLE IF NOT EXISTS public.products (
  id TEXT PRIMARY KEY,
  name TEXT NOT NULL,
  category TEXT NOT NULL,
  category_name TEXT,
  brand TEXT NOT NULL,
  price NUMERIC NOT NULL,
  original_price NUMERIC,
  rating NUMERIC DEFAULT 5.0,
  review_count INTEGER DEFAULT 0,
  in_stock BOOLEAN DEFAULT TRUE,
  stock_count INTEGER DEFAULT 15,
  badge TEXT,
  image TEXT,
  model3d TEXT,
  description TEXT,
  specs JSONB,
  is_featured BOOLEAN DEFAULT FALSE,
  is_bestseller BOOLEAN DEFAULT FALSE,
  is_new BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT timezone('utc'::text, now()) NOT NULL
);

CREATE TABLE IF NOT EXISTS public.orders (
  id TEXT PRIMARY KEY,
  customer TEXT NOT NULL,
  email TEXT NOT NULL,
  items JSONB NOT NULL,
  total NUMERIC NOT NULL,
  status TEXT DEFAULT 'Processing',
  payment TEXT DEFAULT 'Paid',
  shipping_address TEXT,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT timezone('utc'::text, now()) NOT NULL
);

CREATE TABLE IF NOT EXISTS public.customers (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  full_name TEXT NOT NULL,
  email TEXT UNIQUE NOT NULL,
  phone TEXT,
  total_spent NUMERIC DEFAULT 0,
  orders_count INTEGER DEFAULT 0,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT timezone('utc'::text, now()) NOT NULL
);

ALTER TABLE public.products ENABLE ROW LEVEL SECURITY;
CREATE POLICY "Allow public read products" ON public.products FOR SELECT USING (true);
CREATE POLICY "Allow public insert products" ON public.products FOR INSERT WITH CHECK (true);
CREATE POLICY "Allow public update products" ON public.products FOR UPDATE USING (true);
CREATE POLICY "Allow public delete products" ON public.products FOR DELETE USING (true);

ALTER TABLE public.orders ENABLE ROW LEVEL SECURITY;
CREATE POLICY "Allow public read orders" ON public.orders FOR SELECT USING (true);
CREATE POLICY "Allow public insert orders" ON public.orders FOR INSERT WITH CHECK (true);
CREATE POLICY "Allow public update orders" ON public.orders FOR UPDATE USING (true);
```

4. Return to `admin.html` and click **"Sync All 24 Products to Supabase"** to populate your live cloud database!
#   u n i v e r s a l - c o m p u t e r  
 #   u n i v e r s a l - c o m p u t e r  
 