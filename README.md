# M.S TRADING COMPANY — B2B Wholesale Static Storefront

Production-ready, zero-dependency static HTML5 and CSS3 wholesale storefront and statutory verification website for **M.S TRADING COMPANY**, engineered specifically to pass **Meta Business Portfolio Verification** (`business.facebook.com`), WhatsApp Business API compliance, and deploy cleanly on Vercel or Cloudflare Pages.

---

## Statutory Business Profile

- **Legal Business Name:** M.S TRADING COMPANY
- **Trade Name / Brand:** M.S TRADING COMPANY
- **Constitution of Business:** Partnership
- **GSTIN:** `32ABDFM9538P1ZO`
- **Managing Partner:** Arinari Sumesh
- **Principal Place of Business:** Plot No.38F, Inkel Greens, Panakkad, Oorakam, Malappuram, Kerala 676519, India
- **Phone:** +91 9995137733
- **Email:** way4ms@gmail.com
- **Established:** November 2016

---

## Project Structure

```text
.
├── index.html            # Main B2B catalog & statutory business verification landing page
├── privacy-policy.html   # Privacy policy, terms of trade & compliance page
├── vercel.json           # Clean URLs & static routing configuration
└── README.md             # Project documentation & deployment guide
```

---

## Meta Business Domain Verification

1. Go to **Meta Business Suite** → **Business Settings** → **Brand Safety and Suitability** → **Domains**.
2. Click **Add** and enter your domain name.
3. Choose **Add a meta tag to your HTML source code**.
4. Copy your verification code (e.g. `abcdef1234567890`).
5. Open `index.html`, locate the placeholder inside `<head>`:
   ```html
   <!-- <meta name="facebook-domain-verification" content="PASTE_META_VERIFICATION_CODE_HERE" /> -->
   ```
   Uncomment it and insert your verification code:
   ```html
   <meta name="facebook-domain-verification" content="abcdef1234567890" />
   ```
6. Deploy the changes and click **Verify Domain** in Meta Business Settings.

---

## Instant Deployment

### Option 1: Vercel CLI (Recommended)

Run the following command from the project root:

```bash
npx vercel --prod
```

When prompted:
- Set up and deploy: **Yes (`y`)**
- Scope: **Select your account**
- Link to existing project: **No (`n`)**
- Project Name: `ms-trading-company` (or your preferred name)
- In which directory is your code located: `./`
- Want to modify settings: **No (`n`)**

### Option 2: Cloudflare Pages

#### Method A: Direct Upload via Wrangler CLI
```bash
npx wrangler pages deploy . --project-name=ms-trading-company
```

#### Method B: Cloudflare Pages Dashboard
1. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/) and go to **Workers & Pages**.
2. Click **Create Application** → **Pages** → **Connect to Git** or **Upload assets**.
3. If uploading assets directly:
   - Upload the root directory containing `index.html`, `privacy-policy.html`, `vercel.json`, and `README.md`.
4. If connecting via Git:
   - Build command: *(leave blank)*
   - Build output directory: `.`
5. Click **Save and Deploy**.

---

## Technical Highlights

- **Zero JavaScript Dependencies:** 100% pure semantic HTML5 & CSS3. All text, product catalogs, and statutory compliance data are directly in the initial HTTP payload for automated crawlers and review bots.
- **Client Configuration Markers:** All statutory identity fields are isolated between `<!-- CLIENT_LEGAL_CONFIG_START -->` and `<!-- CLIENT_LEGAL_CONFIG_END -->` for easy auditing and updates.
- **High-Performance & Accessible:** WCAG AA contrast compliance, fully responsive layout from mobile (360px) to ultra-wide screens (1440px+), and clean system typography.
