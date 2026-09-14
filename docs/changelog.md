# Release Notes

## 1.0.0 — Initial release

Yen Theme for BigCommerce, built on Cornerstone 6.19.0.

### Variations

Three, and switching between them changes appearance only — never structure, never
features.

- **Light** — the theme's own defaults
- **Bold** — high-contrast palette, heavier type, opens in dark mode
- **Warm** — earth-toned palette applied throughout

### Shopping experience

- Dark/light mode toggle, with both modes designed rather than inverted
- Mega navigation with featured images and multi-column layouts
- Product cards with quick view, wishlist, compare and hover detail
- Grid and list view on category, brand and search pages
- Faceted search with a sidebar on desktop and a drawer on mobile
- Cart page with a summary sidebar, shipping estimator and gift certificates

### The Lookbook

Shoppable images: place hotspots on a photograph as percentage coordinates and map each one
to a product ID. 41 settings, and a page template of its own.

### Custom page templates

Four, each chosen from the template dropdown when creating a web page: **Lookbook**,
**About**, **FAQ** and **Track Order**. All four render their own content — the page body
you type is not what appears. See [The other page templates](usage/page-templates.md) for
what that means in practice.

### Homepage

Hero banner, trust badges, brand showcase, flash sale, reviews, press mentions and
newsletter, each with its own on/off switch in the Theme Editor.

### Under the hood

- Full Page Builder and Theme Editor integration — 367 settings across 9 sections
- Lazy loading with low-quality image placeholders, so images resolve in rather than jump
- Responsive from phone to desktop, with the desktop layout starting at 1261px
- Accessibility: ARIA attributes throughout, focus trapping in overlays, keyboard
  navigation, named landmarks, and a single main landmark per page
- 20 storefront locales covering 13 distinct translations

### What the theme does not do

- **No external services and no API keys.** Everything rendered comes from your own catalog
  and settings.
- **No order-lookup form on Track Order.** BigCommerce provides no storefront endpoint a
  theme can query for a guest's order, so the page offers what does work: order history for
  signed-in shoppers, and the emailed tracking link for guests.
