# Karo — Landing Page

Karo is a small AI tool for small businesses that writes product
descriptions and sales copy in Persian and English, sold by monthly
subscription.

کارو یک ابزار کوچک هوش مصنوعی برای کسب‌وکارهای کوچک است که توضیح محصول
و متن فروش را به فارسی و انگلیسی می‌نویسد و با اشتراک ماهانه فروخته
می‌شود.

## What is on the page

- Hero with a live preview of Karo's output
- 6 features, 3-step "how it works"
- 3 before/after product-description examples (Persian + English)
- Pricing: 3 tiers — Starter $12/mo, Growth $29/mo (recommended),
  Business $59/mo; annual plan = two months free
- FAQ, waitlist form, footer with a crypto-payment note
- Full Persian/English toggle (RTL/LTR switch)
- SEO: title, meta description, Open Graph, JSON-LD
  (SoftwareApplication)

## Design

Design system in `../design-extract-output/DESIGN-SYSTEM.md`, extracted
from the live CSS of stripe.com and linear.app: Stripe's type scale
(tight letter-spacing, 1.07–1.25 heading line-heights), 8px radii,
pill buttons, soft layered shadows, 72px sticky nav, generous section
spacing, hairline borders. Karo keeps its own teal brand so it does not
look like a Stripe clone.

## How to run

No build step, no backend, no API keys. Just open the file, or serve it:

```bash
cd landing
python3 -m http.server 8001
# open http://localhost:8001/
```

## Waitlist — how signups are stored

This is a static page with no backend, so signups are stored in the
browser's `localStorage` (key `karo_waitlist`). The
"Download signups (JSON)" button under the form exports them as
`signups.json`. `signups.json` in this folder starts as an empty array
and is the same shape the export produces. On a real deployment, point
the form at a small backend endpoint instead.

## What it demonstrates for a client

A complete, bilingual, conversion-focused landing page: clear value
proposition, proof (before/after), pricing, objection handling (FAQ),
and a working waitlist capture — the exact page a small business needs
to start selling a product.
