# Apoorvi Healthcare — Website

**Production-ready marketing website for Apoorvi Healthcare**, a home healthcare service provider in Delhi-NCR.

---

## 🚀 Deployment Guide

### Option A — Drag & Drop (Fastest)
1. Open [app.netlify.com](https://app.netlify.com) and log in.
2. Click **"Add new site" → "Deploy manually"**.
3. Drag and drop the **entire project folder** (`poorvi-healthcare/`) into the upload area.
4. Netlify deploys in ~10 seconds and gives you a URL like `https://amazing-name.netlify.app`.
5. Go to **Site Settings → Domain Management** to connect your custom domain.

### Option B — Git Repository (Recommended for ongoing updates)
1. Push this folder to a GitHub/GitLab repo.
2. On Netlify → **"Add new site" → "Import an existing project"** → connect your repo.
3. Build settings:
   - **Build command:** *(leave empty — no build step needed)*
   - **Publish directory:** `.` (the root)
4. Netlify auto-deploys on every `git push`.

---

## ✏️ Placeholders to Replace

Search for these strings in `index.html`, `robots.txt`, `sitemap.xml`, and `netlify.toml` and replace with real values:

| Placeholder | What to replace with | Files |
|---|---|---|
| `[PHONE_NUMBER]` | Actual phone number, e.g. `+91 98765 43210` | `index.html` |
| `[EMAIL]` | Contact email, e.g. `care@apoorvihealthcare.in` | `index.html` |
| `[DOMAIN]` | Your domain, e.g. `apoorvihealthcare.in` | `index.html`, `robots.txt`, `sitemap.xml`, `netlify.toml` |
| `[CITY/LOCALITY]` | Your primary locality, e.g. `Kalkaji, South Delhi` | `index.html` |
| `[CLOUDFLARE_ANALYTICS_TOKEN]` | Cloudflare Analytics token (see below) | `index.html` |

> **Tip:** Use Find & Replace (`Ctrl+H`) in any code editor to update all at once.

---

## 📊 Cloudflare Web Analytics Setup

Cloudflare Analytics is **privacy-friendly, cookieless, and GDPR-compliant** — no consent banner needed.

### How to get your token:
1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) and log in (free account works).
2. In the left sidebar, click **"Web Analytics"**.
3. Click **"Add a site"** → enter your domain → click **"Done"**.
4. Cloudflare gives you a script snippet. **Copy the token** from inside `data-cf-beacon='{"token": "YOUR_TOKEN_HERE"}'`.
5. Replace `[CLOUDFLARE_ANALYTICS_TOKEN]` in `index.html` with your token.
6. Deploy. Analytics data appears in your Cloudflare dashboard within minutes.

> **No DNS change required** — this works on Netlify-hosted sites without proxying through Cloudflare.

### What you'll see in Cloudflare:
- Page views, unique visitors, top pages, referring sites, country breakdown.
- **All data is private** — never shown on the website itself.

---

## 📋 Netlify Forms — Receiving Submissions

The contact form uses **Netlify Forms** (free tier: 100 submissions/month).

### How it works:
- Form submissions are captured automatically by Netlify.
- No backend or server code needed.

### To view submissions:
1. Go to your site in the Netlify dashboard.
2. Click **"Forms"** in the top nav.
3. Click the **"contact"** form to see all submissions.

### To enable email notifications:
1. In Netlify → **Forms → contact → Form notifications**.
2. Click **"Add notification" → "Email notification"**.
3. Enter the email address to receive alerts on each submission.

### To forward to Google Sheets / Airtable:
- Use **Zapier** or **Make (Integromat)**:
  1. Create a Zap: Trigger = "Netlify → New Form Submission" → Action = "Google Sheets: Create Row".
  2. Map the form fields (name, phone, email, service, message) to sheet columns.
- Or use **Netlify's native integrations** (paid plans).

---

## 📁 Project Structure

```
poorvi-healthcare/
├── index.html          # Single-page website (all sections)
├── css/
│   └── style.css       # Complete stylesheet (design system)
├── js/
│   └── main.js         # Vanilla JS (nav, FAQ, form, animations)
├── robots.txt          # SEO: crawler instructions
├── sitemap.xml         # SEO: sitemap (submit to Google Search Console)
├── netlify.toml        # Netlify deployment & headers config
└── README.md           # This file
```

---

## 🔍 SEO Checklist (Post-Deployment)

- [ ] Replace all `[PLACEHOLDER]` values in `index.html`
- [ ] Update `sitemap.xml` with your real domain
- [ ] Submit `sitemap.xml` to [Google Search Console](https://search.google.com/search-console)
- [ ] Submit `sitemap.xml` to [Bing Webmaster Tools](https://www.bing.com/webmasters)
- [ ] Add an OG image at `https://[DOMAIN]/og-image.png` (1200×630 px, your brand design)
- [ ] Set up Cloudflare Analytics (see above)
- [ ] Enable Netlify form email notifications
- [ ] Add real phone number, email, and social media links
- [ ] Test mobile responsiveness on real devices
- [ ] Run [PageSpeed Insights](https://pagespeed.web.dev/) to verify performance score

---

## 🎨 Brand Reference

| Element | Value |
|---|---|
| Primary Color | `#7A2E7A` (Purple) |
| Dark Variant  | `#5C1F5C` |
| Light Variant | `#9B4A9B` |
| Font | Inter (Google Fonts) |
| Tagline | "Trusted Critical Care Specialist" |
| Sub-tagline | "Safe care in the comfort of your home" |

---

## 📞 Support

For technical changes, content updates, or additional pages, edit `index.html` and `css/style.css` directly.

The site is built with plain HTML + CSS + vanilla JS — no frameworks, no build tools, no dependencies. Any web developer can maintain it.

---

*Built for Apoorvi Healthcare — Delhi-NCR*
