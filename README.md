# Afterlight Journal — Design-System Specimen

A responsive, single-page design-system specimen for **Afterlight Journal**, an
independent culture and design publication. This is documentation for a visual
foundation — tokens, type, and reusable components — not a finished marketing
homepage. Later modules build on this: figures, forms, tables, SVG, navigation,
shapes, and effects.

**Live site:** 


## What's here

```
index.html          The full specimen page (S1–S6 + intro + documentation footer)
css/styles.css       All tokens, reset, and component rules
docs/test-record.md      Required test conditions, expected/observed results, revisions
docs/ai-disclosure.md    AI disclosure + verification record
docs/code-defense.md     Reset strategy, token hierarchy, scoped override, evidence-based revision
```

## Design system

- **Architecture:** primitive tokens → semantic tokens → component rules. Components
  never reference a primitive or raw hex value directly.
- **Themes:** Rich Editorial (default) and Midnight Editorial (alternate), toggled at
  runtime via `[data-theme]`. The alternate theme remaps eight semantic tokens
  (background, surface, text, muted text, border, action, action-hover, focus) with
  zero duplicated component CSS.
- **Type:** Libre Baskerville (display) + Inter (body), SIL Open Font License 1.1, via
  Google Fonts, with documented fallback stacks.
- **Spacing / radius / elevation:** small proportional scales (`--space-xs` through
  `--space-3xl`, three radius steps, two elevation levels) — see S2 in the specimen.

## Sections

| ID | Section |
|----|---------|
| S1 | Foundation + selective reset |
| S2 | Token inventory (color, spacing, measure, radius, elevation, typography) |
| S3 | Typography (families, hierarchy, content specimen, fallback evidence) |
| S4 | Actions + states (links, primary/secondary buttons) |
| S5 | Surfaces + content patterns (article card, featured card, callout, media placeholder) |
| S6 | Control foundations (text input, select, checkbox, radio, button) |

## Status

- [x] Design phase complete
- [x] Implementation (HTML/CSS, both themes)
- [x] Required testing (320/768/1280px, 200% zoom, keyboard, theme contrast, font
      fallback, HTML/CSS validation) — see `docs/test-record.md`
- [x] Code defense evidence-based revision — see `docs/code-defense.md`
- [x] GitHub Pages publication verified against local build

## Running locally

No build step. Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server
```

## AI disclosure

AI-Assisted with Disclosure. See `docs/ai-disclosure.md` for the full record of what
AI assistance was used for and what the author verified independently.

## License

Project code:  MIT. Fonts: SIL Open Font
License 1.1 (Libre Baskerville, Inter).
