# New Horizon Precision — Brand Palette Standard

This repository now includes a refreshed color system and an updated HTML entry (`index.v2.html`) that implements the palette as CSS variables and Clarendon typography. This palette and typography are the new standard for digital, print, and embroidery usage across New Horizon Precision.

## Color Palette

Primary Palette (Core Identity)
- Dark Green: `#1E3D2F` — Main brand color; text, drone silhouette, crop fields (growth, reliability, nature)
- Golden Yellow: `#E4A936` — Accent; sunrise, highlights, secondary details (harvest, optimism, precision)
- Off-White: `#F6F2EA` — Background for clean contrast; hats/shirts, website backgrounds

Secondary Palette (Support + Flexibility)
- Sky Blue: `#4E9CBF` — Optional accent; digital branding, social graphics, tech feel
- Charcoal Gray: `#2D2D2D` — Neutral text/background alternative; sleek apparel option
- Bright Green: `#6BAF5B` — Light accent for fields or design variations

## Typography

**Primary Font:** Clarendon (serif)
- Used for headings, logo, and key brand elements
- Fallback: Georgia, serif
- Provides a professional, established, and trustworthy appearance

## Implementation

In `index.v2.html`, the palette is defined via CSS variables under `:root`:

```css
:root {
  --color-dark-green: #1E3D2F;
  --color-golden-yellow: #E4A936;
  --color-off-white: #F6F2EA;
  --color-sky-blue: #4E9CBF;
  --color-charcoal-gray: #2D2D2D;
  --color-bright-green: #6BAF5B;
}
```

Use these variables for backgrounds, text, and accents to ensure consistency. The layout mirrors the previous site structure while applying the updated palette and Clarendon typography to header, CTA, section headings, certification section, and footer.

## Apparel & Embroidery Guidance
- 2-Color Version: Dark Green + Golden Yellow (great for hats and polos)
- Monochrome Version: Dark Green only, for one-color printing/stitching
- Reversed Version: Off-White logo on Dark Green or black background

## Files
- `index.v2.html` — Updated site variant using the new palette
- `index.html` — Previous version (reference)

## Standard
This palette and Clarendon typography are the official standard for all New Horizon Precision assets going forward. New pages and assets should reference these variables, color values, and font choices.

## Next Steps (optional)
If desired, we can produce a one-page Brand Guidelines PDF with exact colors, typography, spacing, and usage examples suitable for web handoff and print shops.

