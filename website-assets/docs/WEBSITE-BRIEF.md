# Rust Belt Standards LLC — Website Brief

Give this whole file to Claude Code as context when starting the build.

## Goal

A single-page website at rustbeltstandards.com that establishes RBS as a
legitimate, real software company — this is required for Apple Developer and
Google Play organization verification, so it needs to read as credible and
deliberately built, not like a generic template or a placeholder.

Keep it to one page. No heavy animation, no stock-photo hero, no filler
sections (testimonials, stats, blog) since none of that is real yet.

## Creative direction

Think "spec plate riveted onto well-made machinery" — precise, unpretentious,
confident. Not generic corporate SaaS, not a cutesy startup site. RBS's own
identity (code brackets, slate/steel palette) reads as engineered. Both
products under it also replace messy improvisation with a proper system —
Coastward replaces spreadsheet/group-text chaos, ChuckEd replaces whiteboard
chaos on a shop floor.

**Avoid:** warm-cream-serif-terracotta "generic AI landing page" look,
icon-in-rounded-card grids, ALL-CAPS eyebrow labels above every section,
scroll-triggered fade-up animation on everything, centered hero text.

**Do:** one quiet technical detail behind the hero (subtle grid or corner
registration marks), asymmetric/left-aligned hero, small monospace factual
labels used sparingly (e.g. "EST. · MEDINA, OH") the way a stamped spec plate
uses real numbers.

## Color

RBS shell (header, footer, hero background):
- Slate Navy `#1E3A4C`
- Steel Blue `#7FB8C9`
- Warm Steel White `#F4F1EC`

Coastward and ChuckEd each keep their OWN palette inside their own card/section
— like two labeled instruments mounted on the same panel, not blended into one
site-wide palette:

Coastward: Ink Navy `#1C2B39`, Rust `#BB4A2E`, Tide Teal `#3E6E68`,
Gold `#C89B3C`, Warm Paper `#EDE7DA` (see coastward/coastward-brand-reference.md)

ChuckEd: Akron Blue `#041E42`, Akron Gold `#A89968`

## Type

Clean grotesque sans for headlines/body (Inter or similar system-ui stack).
Monospace used sparingly for small factual labels only, not for headlines.

## Layout (single page)

1. **Header** — RBS mark (rbs-brand/rbs-mark.svg) + wordmark, simple nav:
   Coastward / ChuckEd / Contact
2. **Hero** — left-aligned, asymmetric. Headline: "Software that respects
   your time and your budget." Subhead: "Built for the person using it, not
   the person selling it." Small monospace detail line.
3. **Products section** — "Two products, two problems solved." Two cards
   side-by-side on desktop, stacked on mobile:
   - Coastward card: coastward/coastward-icon.png, short description from
     coastward-brand-reference.md, own palette
   - ChuckEd card: chucked/chucked_logo.svg, short description from
     RustBeltStandards_ChuckEd_Reference.docx, own palette
4. **Philosophy section** — back to RBS navy shell. State the six principles
   plainly as a tight line/list, not six icon-cards:
   Easy · Functionality · Affordable · Built for the user · Intentional · Clean
   Tagline: "Made on purpose, priced on purpose."
5. **Footer** — support@rustbeltstandards.com · link to privacy policy
   (docs/privacy-policy.md content) · © Rust Belt Standards LLC

## Assets in this folder

- `rbs-brand/` — full RBS logo kit (SVG + PNG), see rbs-brand/BRAND-GUIDE.md
  for exact file-by-file usage guidance and favicon/app-icon setup
- `coastward/` — Coastward app icon (coastward-icon.png, full color on navy),
  Android adaptive foreground layer, and full brand reference doc
- `chucked/` — ChuckEd logo (PNG + SVG) and full product reference doc
- `docs/privacy-policy.md` — full privacy policy text, needs its own page or
  anchor linked from the footer

## Technical notes

- Static site (plain HTML/CSS, or a lightweight framework if preferred) —
  no backend needed for this initial version
- Should deploy cleanly to Vercel from a GitHub repo
- Use rbs-brand/png/rbs-mark-32.png, rbs-mark-180.png, rbs-mark-192.png for
  favicon / apple-touch-icon / PWA icons per the BRAND-GUIDE.md instructions
- Mobile-responsive — this will be viewed on phones, and the site itself
  needs to look credible on both desktop and mobile for app store reviewers
