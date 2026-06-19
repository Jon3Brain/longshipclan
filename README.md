# Longship Clan

Static storefront for the Longship Clan, published at **https://longshipclan.com**.
Single self-contained `index.html` (no build step, no backend) plus product images.

## Structure
- `index.html` — the entire site (HTML + CSS + JS in one file)
- `images/` — product photos referenced by the store
- `CNAME` — custom domain for GitHub Pages

## Editing the store
All products, prices, and payment handles live in one block near the bottom of
`index.html`, marked `EDIT THIS BLOCK`. Each product supports:
- `img` — front photo; `imgBack` — optional back photo (adds a "View Back" flip)
- `colors` — optional list `[{name, img}]` (adds a color picker that swaps the photo)
- `sizes` — optional list for apparel
- `cat` — `swag` | `wear` | `gear` (groups items into sections)

To swap a placeholder/processed image for a real photo, drop the file in `images/`
and point the product's `img` at it.

## Checkout
No live payments. Checkout gathers buyer details, opens a pre-filled order email to
the club, and shows Square / PayPal / Venmo / Cash App options to pay manually.

## Hosting
GitHub Pages, served from the `main` branch root. Custom domain set via `CNAME`.
