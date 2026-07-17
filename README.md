# Virtuous Cycle — Brand Kit

Canonical brand system, collateral prototypes, and application materials for
Virtuous Cycle LLC. Imported from a Claude Design handoff bundle (see
[`HANDOFF.md`](HANDOFF.md) for the original export note).

**Brand edition:** VC-BRAND-2026-02 ("Verdant") — the current system.
The source-of-truth for messaging and design tokens is
[`brand/Website Brief (Replit).md`](brand/Website%20Brief%20\(Replit\).md).

## Layout

| Path | Contents |
|---|---|
| `*.html` (root) | Standalone document prototypes (collateral + guides). Each expects the sibling `vc-*.css` files and the shared `assets/` folder. |
| `vc-brand.css` · `vc-collateral.css` · `vc-guide.css` · `vc-templates.css` | Shared stylesheets the prototypes link to. |
| `assets/` | Shared binary assets: logo/knot PNGs (6 colorways), `icon`/`logo` variants, `favicon`, `hero-watercolor`, `ribbon.svg`/`ribbon-v2.svg`, `mockup-*.png`, and `fonts/` (Inter + Spectral woff2 subsets). |
| `brand/` | Source-of-truth references — `tokens.json` (machine-readable design tokens), `BRAND.md` (canonical brand doc), and the Replit website brief. |
| `brand-guide/` | The 14-page **rendered** Visual Identity Guide (`p01`–`p14.png`), edition 2026-02. |
| `mockups/` | Collateral preview renders (banners, business cards, apparel, etc.). |
| `application/` | GDCI job-application source documents (`.docx`). |
| `docpage.js` · `tweaks-panel.jsx` | Claude Design editor scaffolding referenced by some exported pages. |

## Documents

Renders verified locally (fonts load from Google Fonts, so open with a
network connection or self-host the fonts):

- **Collateral** — `Letterhead`, `Memo`, `Invoice`, `Proposal`, `Apparel`,
  `Stickers`, `Pull-up Banner`, `Advisory Report`, `Business Cards`,
  `Postcard`, `Stationery`, `Conference Flyer`, `Conference Kit`,
  `Email Signature`, `Capabilities`
- **Guides** — `Brand Guide.html` (current VC-BRAND-2026-02 guidelines),
  `Brand Guide (print)`, `Brand Guide (Express export)`, `Brand Decisions`
  (direction memo)
- **Primary** — `Brand Kit.html` (project catalog), `GDCI Application Preview.html`

### Superseded

- **`Brand Guide v1 (olive).html`** — the earlier **VC-BRAND-2026-01** edition
  (Gelasio/Poppins type, amber+navy palette, "place-strengthening"). Kept for
  reference only; the current guide is the 2026-02 set in `brand-guide/`.

## Completeness

The import is complete: all 22 HTML documents, both ribbon SVGs, the full
`assets/` binary set, `tokens.json`, and `BRAND.md` are present, and every
`href`/`src`/`url()` reference across the HTML and CSS resolves locally
(verified programmatically). Inter-page navigation between collateral pages
works end-to-end.

## Previewing locally

Because the prototypes reference the shared `assets/` folder and `vc-*.css` by
relative path, serve the repo root rather than opening files directly:

```sh
python3 -m http.server 8000
# then open http://localhost:8000/Letterhead.html
```
