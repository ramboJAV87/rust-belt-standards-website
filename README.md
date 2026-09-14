# rustbeltstandards.com

Marketing site for **Rust Belt Standards LLC** (Medina, Ohio) and its
two products, Coastward and ChuckEd.

Plain static HTML and CSS — no build step, no framework, no backend.

## Structure

```
index.html          Homepage: hero, products, philosophy, contact
coastward/          Coastward landing page (/coastward), with its own stylesheet
privacy.html        Privacy policy
styles.css          Homepage + privacy page styles
site.webmanifest    PWA/manifest icons
robots.txt          / sitemap.xml
assets/brand/       RBS logo kit files actually used by the site
assets/coastward/   Coastward app icon, favicon sizes, and screenshots/
assets/chucked/     ChuckEd logo
website-assets/     Source-of-truth brand kits, brand guides, and the design brief
```

`assets/` holds only the files the site references. `website-assets/` is the full
delivered brand kit (including the RBS brand guide, the Coastward and ChuckEd
product references, and the original design brief) and is kept in the repo as the
source of truth.

## Local preview

No build step. Open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000. Serving over HTTP (rather than opening the file
directly) is preferable because the site uses root-relative paths like
`/styles.css`.

## Deploying to Vercel

Import the GitHub repo in Vercel and deploy with framework preset **Other** —
no build command, output directory is the repo root. `vercel.json` sets
`cleanUrls` so `/privacy` also resolves.

## Coastward screenshots

The Coastward page has clearly marked placeholder frames for eight screenshots
(hero + one per feature). Each is a `<div class="shot" data-screenshot="NAME">`
in `coastward/index.html` containing a `.shot-placeholder`. To swap one in, drop
the image into `assets/coastward/screenshots/` and replace the placeholder div
with `<img src="/assets/coastward/screenshots/NAME.png" alt="...">`. The frame
is sized for a portrait phone screenshot (1179 × 2556); other portrait sizes
are cropped to fit. See `assets/coastward/screenshots/README.md` for filenames.

## Design notes

- The RBS palette (slate navy, steel blue, warm steel white) is used for the site
  shell only: header, hero, philosophy section, footer.
- Coastward and ChuckEd each keep their own palette, scoped to their own product
  card — two labeled instruments mounted on the same panel.
- Monospace (IBM Plex Mono) is used only for small factual labels: the hero spec
  plate, product status lines, principle numbers. Never for headlines.
- The ChuckEd mark is half Akron Blue, so on the dark ChuckEd card it sits on a
  light plate rather than directly on the blue.

## Brand asset rules

See `website-assets/rbs-brand/BRAND-GUIDE.md`. In short: don't recolor the badge,
don't stretch the lockup, and keep clear space around the logo equal to the
height of the R.
