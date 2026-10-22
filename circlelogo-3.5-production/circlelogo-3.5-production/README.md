# CircleLogo 3.5 — Delta Digitech Enterprise Bulk Circular Logo Utility
### Individual Background & Shape Composer | Delta Digitech Corporate Branding | Bulk Logo Processing | Free Cloudflare Pages Ready

CircleLogo 3.5 is an internal company utility engineered for Delta Digitech team members. It allows employees to upload dozens of store and brand logos (PNG, JPG, WebP, SVG), adjust each logo's circular framing, customize individual background colors and gradients, add decorative shape accents behind artwork, and export high-resolution circular PNG files with true alpha-transparent corners individually or packaged in a bulk ZIP archive.

---

## 🌟 What's New in Version 3.5

### 1. Individual Background & Shape Composer
- **Direct Workspace Integration**: Located strictly inside the **Edit** modal of each individual logo. The global dashboard remains clean and familiar.
- **Three Dedicated Editing Tabs**:
  - **LOGO**: Zoom slider (10%–400%), Contain / Cover fit modes, horizontal and vertical positioning offset, 360° rotation, horizontal flip, and auto-centering.
  - **BACKGROUND**: 12 preset fills (Transparent, Solid White, Solid Black, Light Grey, Dark Grey, Light Blue, Navy Blue, Beige, Soft Pink, Light Green, Custom Color, Gradient), HEX color input, and opacity slider (0%–100%).
  - **SHAPES**: 8 decorative shape types (Circle, Ellipse, Square, Rectangle, Rounded Rectangle, Pill, Abstract Blob, Ring/Geometric Accent) with independent color, dimensions (width/height), horizontal/vertical offsets, rotation, opacity, layer reordering (move forward/backward), duplication, visibility toggle, and locking.
- **True 3-Layer Composition Engine**:
  - **Layer 1 (Bottom)**: Background (contained strictly within the circular boundary).
  - **Layer 2 (Middle)**: Decorative Shape layers (behind original artwork).
  - **Layer 3 (Top)**: Original uploaded logo (unmodified, non-destructive, with its transforms applied).

### 2. Official Delta Digitech Corporate Branding
- Header displays both the **CircleLogo 3.5** product badge and the **official Delta Digitech company logo** (crisp, high-DPI RGBA asset preserving original colors and proportions).
- Dedicated footer attribution: `CircleLogo | An internal utility by Delta Digitech`.
- **Zero Contamination**: Corporate branding is strictly confined to the application UI and is never rendered onto customer logos, exported PNGs, or ZIP archives.

### 3. Preserved Production Features
- **Bulk Uploading**: Multi-file drag-and-drop or file browser selection for 10, 50, 100+ files.
- **Independent State Management**: Each logo retains its own unique background, shape layers, and transformations. Editing Logo 1 never impacts Logo 2 or Logo 3.
- **Batch Export with Individual Settings**: Export All generates a ZIP where every file accurately reflects its own custom background, shapes, and zoom/position adjustments.
- **Real Circular Masking**: Genuine Canvas 2D circular clipping path (`ctx.arc` + `ctx.clip()`) guaranteeing that all pixels outside the circle have `alpha = 0`.
- **Resolution Options**: 256×256, 512×512 (default), 1024×1024, and 2048×2048.
- **Zero-Latency In-Browser Processing**: Pure HTML5 Canvas, JSZip, and modern Web APIs with no external server transmission or data retention.

---

## 🚀 Cloudflare Pages Free Deployment Guide

CircleLogo 3.5 is 100% static and optimized for free deployment on Cloudflare Pages.

### Quick Deployment via Cloudflare Dashboard (Drag & Drop)
1. Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. Navigate to **Compute (Workers) > Workers & Pages > Create application**.
3. Select the **Pages** tab and click **Upload assets**.
4. Set Project name: `circlelogo` (your free URL will be `https://circlelogo.pages.dev`).
5. Drag and drop the `circlelogo-3.5-production` folder or select its files.
6. Click **Deploy site**. Your tool is instantly live with free global CDN and HTTPS!

### Deploy via Wrangler CLI
```bash
npx wrangler pages deploy ./circlelogo-3.5-production --project-name=circlelogo
```

---

## 🔒 Optional Employee Access Restrictions (Cloudflare Zero Trust)
To restrict access exclusively to Delta Digitech staff members using their `@deltadigitech.com` email addresses:
1. In the Cloudflare Dashboard, open **Zero Trust** (free for up to 50 users).
2. Go to **Access > Applications > Add an application**.
3. Select **Self-hosted**.
4. Application name: `CircleLogo Internal Utility`.
5. Application domain: `circlelogo.pages.dev` (or your custom subdomain).
6. Under **Policies**, create an Access Policy:
   - Action: `Allow`.
   - Rule type: `Include > Emails ending in > @deltadigitech.com` (or Google Workspace SSO).
7. Save. Employees accessing the link will be prompted for a one-time PIN sent to their company email.

---

© 2026 Delta Digitech Pvt Ltd. All rights reserved.
