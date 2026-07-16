# Virtuous Cycle — Website Implementation Brief
**For Replit · Brand edition VC-BRAND-2026-02 (Verdant) · paste this wholesale**

This briefs the visual + messaging rekey of **virtuouscycle.dev** onto the canonical Virtuous Cycle brand. Two files in the design project are the source of truth — if anything here is ambiguous, they govern: `brand/tokens.json` (machine-readable) and `brand/BRAND.md`.

The firm: a mission-driven development & advisory firm — strategy, development, and PPP structuring for land, policy, and the communities around it. **Restraint is the brand. Authority comes from economy, not volume.**

---

## 1 · Messaging — what line goes where

Use these exact lines. Do not paraphrase.

| Slot | Line | Where it lands |
|---|---|---|
| **Tagline** (hero, tone-setter) | **People-powered. Place-rooted. Purpose-driven.** | Hero `<h1>` or the line directly below the hero heading; social banners & bios |
| **Capability line** (what we do) | **PPP + Development Advisory for financeable, durable projects.** | Directly under the tagline; nav/footer; LinkedIn headline |
| **Signature / essence line** (quiet, recurring) | **Land, livelihood & the common good.** | Footer one-liner; About lead; section dividers; the line that recurs on all print collateral |
| **Motto** (story framing) | **Development that compounds.** | Section intros, About, value/ROI framing |
| **One-liner** (meta description) | A mission-driven development and advisory firm — helping communities grow with integrity by aligning design, investment, and strategy. | `<meta name="description">`, About paragraph |

**Hero pattern** (tagline first, capability second — so tone *and* "what is this firm" both land immediately):

> # People-powered. Place-rooted. Purpose-driven.
> ### PPP + Development Advisory for financeable, durable projects.

**`<title>` / Open Graph:** `Virtuous Cycle | People-powered. Place-rooted. Purpose-driven.`
**OG description:** the one-liner above.

**Retire everywhere (find & remove):**
- "Development advisory for the common good."
- "Real estate with purpose" / "Strategy with soul."
- "Place-strengthening."
- Any older "PPP + …" capability wording → use only **"PPP + Development Advisory for financeable, durable projects."** everywhere.

---

## 2 · Type — two families, no others

Load from Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Spectral:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

- **Spectral** (serif) — *speaks & reflects*: hero, headings, big numbers, and the one reflective **italic** line that can close a section. Weights 500/600; italic 500.
- **Inter** (sans) — *explains*: body @ line-height 1.6, labels, captions, buttons, data. SemiBold (600) only for tracked-caps labels or the first words of a paragraph — never mid-sentence emphasis.

```css
--serif: 'Spectral', Georgia, 'Times New Roman', serif;
--sans:  'Inter', system-ui, Arial, sans-serif;
```

Scale (web): hero 56–72px Spectral 600 · section title 36–40px Spectral 600 · lede 18–20px Spectral 500 (Pine) · body 16–17px Inter 400 / 1.6 · kicker/label 11–12px Inter 600 tracked caps, color Moss. Body never below 16px.

---

## 3 · Color — one verdant hue, a family of tones

**No off-family color.** Warmth comes from imagery (watercolor + photography), never a second swatch. Paste this token block:

```css
:root{
  /* green family — light → deep */
  --vc-mist:  #EEF3E0;  /* tints, quiet panels, table fills */
  --vc-sage:  #CFE0A8;  /* rules, soft dividers */
  --vc-leaf:  #9DC65A;  /* secondary fills, charts, hero accents on dark */
  --vc-green: #6E9E10;  /* ANCHOR — identity, accents, buttons, lead bars */
  --vc-moss:  #4F7510;  /* green TEXT on white (legible), link/hover */
  --vc-pine:  #2F4A0C;  /* panels, depth, lede text */
  --vc-field: #16230A;  /* dark grounds, reversed type, footer */
  /* warm neutrals (green-cast, never blue-grey) */
  --ink:    #1A2230;    /* display & body text */
  --grey:   #555555;    /* captions, metadata */
  --grey-l: #8A9384;    /* faint labels */
  --fill:   #F4F6F1;    /* warm house off-white */
  --hair:   #E3E7DE;    /* hairline borders */
  --paper:  #FFFFFF;
}
```

Rules:
- Buttons / primary actions: **Verdant `#6E9E10`**; hover **Moss `#4F7510`**.
- Small green text on white: use **Moss `#4F7510`**, not Verdant (contrast).
- Never green text on a green field. Reversed white type only on **Pine** or **Field** grounds (e.g. footer, hero overlays).
- Dark sections (hero band, footer): gradient `linear-gradient(157deg,#5A8A12,#16230A)`.

---

## 4 · Logo

- **Primary (stacked)** knot + wordmark · **Mark only** (the woven knot) for favicon, social avatar, nav at small sizes.
- Verdant on light grounds; **white on Pine/Field** (`filter: brightness(0) invert(1)` on the verdant mark, or a white asset).
- **Clear space** ≥ the height of one loop of the knot on all sides. **Min size** 32px on screen.
- **Never** recolor, stretch, rotate, add gradients/shadows, or put it in a containing box.

Assets are in the design project under `assets/` — export and host: `logo-verdant.png` (stacked), `icon-verdant.png` (mark), `favicon.png`.

---

## 5 · Layout & feel

- Generous whitespace; **one signature visual element per section** — a verdant band, a single watercolor, or the ribbon motif, never two at once.
- The **ribbon motif** (layered green bands) only on hero / section dividers — never behind body text, never on data.
- Imagery: original **watercolor** (Pensacola-Bay hand) for hero moments + restrained **real photography** elsewhere. Palette stays green; the image supplies the warmth.
- Findings/claims in **ranges, never point estimates** ("worth $6–17M," not "$11M").
- Sections separate by **weight and rule, not by adding hues**.

---

## 6 · Social profiles (align these too)

Same messaging, applied to each surface:

- **LinkedIn / Facebook headline (tagline):** People-powered. Place-rooted. Purpose-driven.
- **Sub-headline / "what we do":** PPP + Development Advisory for financeable, durable projects.
- **Bio / About:** the one-liner, then "Development that compounds." as a close.
- **Profile image:** the knot **mark** (verdant on white, or white on Field).
- **Banner / cover:** Field/Pine gradient or a watercolor, with the tagline reversed in Spectral; keep the wordmark small.

---

## 7 · Do-not list

Jargon, corporate clichés, exclamation marks, second person in formal copy, "place-strengthening," soul/purpose *softness* (the approved triad is the one sanctioned use of "purpose"), off-family color, gradients on the logo, point estimates, stock-photo gloss, more than one signature element per section.

---

## 8 · Suggested build order

1. **Token + font rekey** — drop in the `:root` block and Google Fonts; map existing styles to Spectral/Inter + the green family. *(This underpins everything — do it first.)*
2. **Hero** — tagline + capability line, the knot mark, a watercolor or Field-gradient ground.
3. **Footer + meta** — signature line, capability line, `<title>`/OG.
4. **Section-by-section** — apply type scale, ranges, one-element rule.
5. **Imagery pass** — watercolor hero, real photography, all within the green palette.
