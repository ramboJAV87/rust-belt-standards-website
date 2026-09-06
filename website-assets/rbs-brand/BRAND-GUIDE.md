# Rust Belt Standards LLC — Brand Assets

## Color palette

| Role | Hex | Use |
| --- | --- | --- |
| Slate navy | `#1E3A4C` | Badge background, wordmark on light backgrounds |
| Steel blue | `#7FB8C9` | Code brackets, accent elements, links |
| Cream | `#F4F1EC` | The R, light backgrounds |
| Grey | `#6E7A85` | Tagline, secondary text on light |
| Light text | `#EAF1F4` | Wordmark on dark backgrounds |
| Muted light | `#9AA7B2` | Tagline on dark backgrounds |

## Typography

The logo files have all text converted to vector paths, so they render identically
everywhere with no font dependency. For the website itself, a clean grotesque
sans (Inter, Helvetica Neue, or system-ui) matches the wordmark closely.

## Taglines

- **Logo lockup:** Made on purpose, priced on purpose.
- **Website hero:** Software that respects your time and your budget.
- **Hero subhead:** Built for the person using it, not the person selling it.

## Files

### Vector (preferred for web and print)

| File | Use |
| --- | --- |
| `rbs-logo-horizontal.svg` | Primary logo. Site header, letterhead, invoices |
| `rbs-logo-horizontal-no-tagline.svg` | Tight spaces where the tagline would be unreadable |
| `rbs-logo-stacked.svg` | Square-ish spaces, social profiles, print |
| `rbs-mark.svg` | Mark alone (rounded corners). Favicon, avatars |
| `rbs-mark-square-appicon.svg` | Full-bleed square, no rounded corners — App Store source |
| `*-ondark.svg` | Variants for dark backgrounds |
| `*-mono-black.svg` / `*-mono-white.svg` | Single-color for faxes, engraving, one-color print |

### Raster (`png/`)

| File | Use |
| --- | --- |
| `rbs-appicon-1024.png` | **App Store Connect app icon.** 1024×1024, no alpha, square |
| `rbs-mark-180.png` | `apple-touch-icon` for the website |
| `rbs-mark-192.png` / `rbs-mark-512.png` | PWA / Android manifest icons |
| `rbs-mark-32.png` / `rbs-mark-16.png` | Browser favicon |
| `rbs-logo-horizontal.png` | General web/email use, 1200px wide |
| `rbs-logo-stacked.png` | Social profile images |

## Website favicon setup

```html
<link rel="icon" href="/rbs-mark-32.png" sizes="32x32">
<link rel="icon" href="/rbs-mark-192.png" sizes="192x192">
<link rel="apple-touch-icon" href="/rbs-mark-180.png">
<link rel="icon" href="/rbs-mark.svg" type="image/svg+xml">
```

## Usage rules

- Keep clear space around the logo equal to the height of the R on all sides.
- Don't recolor the badge, stretch the lockup, or rotate the mark.
- Don't place the standard logo on a busy photo — use the mono white version.
- Minimum size for the horizontal lockup with tagline: 200px wide. Below that,
  use the no-tagline version or the mark alone.

## Note on Apple's app icon

Apple applies its own rounded-corner mask, so the App Store source icon must be a
full square with no transparency and no pre-rounded corners. Use
`png/rbs-appicon-1024.png` — it is built to that spec.
