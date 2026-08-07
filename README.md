# beautifi.io

The BeautiFi marketing site — a single static page, no build step, no dependencies
beyond a Google Fonts link.

| File | Purpose |
|---|---|
| `index.html` | The whole site. Styles and scripts are inline. |
| `og-image.png` | 1200×630 social card for link previews. |
| `favicon.svg` | Browser tab icon. |
| `apple-touch-icon.png` | 180×180 home-screen icon. |

## Editing

Open `index.html` in a browser — it works straight from disk. There is nothing to
compile and no package manager involved.

Design tokens live in the `:root` block at the top of the `<style>`. The palette and
the product-card markup mirror the BeautiFi/DUSN protocol UI so the site and the
product read as one system.

## Notes

- The public-feed section is an **illustrative preview**. Entries are representative,
  not live network data, and the page says so.
- Verification wording follows decision **D-003**: work is described as
  *Verified Mitigation Hours*, never as "verified clean air".
- Motion is opt-out aware — `prefers-reduced-motion` disables travel, drift and
  autonomous animation while keeping fades and the scroll indicator.

## Deployment

Served by GitHub Pages from `main` / root. The apex and `www` records are managed
in IONOS DNS. Email records (MX, SPF, DKIM, DMARC) live in the same zone and must
not be touched when changing hosting.
