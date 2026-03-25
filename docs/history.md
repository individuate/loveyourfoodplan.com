# loveyourfoodplan.com — History

## 2026-03-25

### Button contrast and WebP image optimization
- Separated button background into `--color-btn-bg` token so dark mode button stays #B94D32 (5.03:1 with white text) while text accent uses lighter #E07A5C
- Button version text changed from 0.85-opacity to full white (5.03:1, passes AA)
- Converted all 10 screenshots from PNG to WebP: 3.3MB → 1.1MB (67% reduction)

### Accessibility, contrast, dark mode, and performance audit fixes
- Extracted all hard-coded colors to CSS custom properties (`:root` variables)
- Added dark mode via `prefers-color-scheme: dark` with full inverted palette
- Fixed WCAG AA contrast failures: secondary text (#9C9590 → #78716C), accent (#C45D3E → #B94D32 for text, #E07A5C for dark mode), button version text opacity (0.6 → 0.85)
- Added skip-to-content link, `<main>` landmark, `aria-label` on nav
- Made screenshot images keyboard-accessible: `tabindex="0"`, `role="button"`, Enter/Space handlers
- Lightbox now has `role="dialog"`, `aria-modal`, visible close button, focus trap, and focus restoration
- Added `:focus-visible` outlines site-wide
- Added `loading="lazy"` and `width`/`height` attributes to all below-fold images
- Added `defer` to TelemetryDeck script
- Added 480px small-phone breakpoint with tighter padding and smaller headings
- Added SVG emoji favicon and `meta theme-color` (light + dark)

## 2026-03-24

### Add app screenshots and polish copy
- Added 7 app screenshots: dietary approaches, restrictions, food preferences, new meal plan, generating spinner, meal plan grid, recipe, and API key setup
- Cropped approaches and restrictions to tight chip-only views; preferences onward show full app with sidebar
- Screenshot containers use auto-height with subtle box-shadow for definition
- Copy tweaks: "NO CLUTTER" caps, "filled with ads" addition, medium-weight emphasis, "Currently fully free! No demo mode, no ads."
- Download CTA heading bumped to h2 for more presence

### Expand to full marketing page
- Replaced minimal hero-only landing page with full scrolling marketing page
- Added sections: intro hook ("Love your food plan!"), 4 step-by-step feature sections with alternating text/screenshot layout, full-width meal plan showcase, recipe section, API key explanation, download CTA
- Screenshot placeholders ready for app screenshots to be dropped in
- Terracotta accent used for step labels, hook paragraph, and strikethrough detail
- Medium-weight (500) emphasis on key phrase in intro
- Improved footer contrast and added TelemetryDeck privacy note
- Mobile responsive: feature sections stack vertically under 640px

## 2026-03-23

### Initial setup
- Created public repo for marketing site, DMG downloads, and Sparkle update hosting
- Enabled GitHub Pages with custom domain (loveyourfoodplan.com)
- Added placeholder index.html and CNAME
- Configured Cloudflare DNS with CNAME records pointing to individuate.github.io

### Build marketing page from Paper design
- Converted Paper design to production HTML with Google Fonts (Instrument Serif, Inter)
- Download button links to GitHub Releases DMG (`loveyourfoodplan.com/releases/latest/download/LoveYourFoodPlan.dmg`)
- Added mobile responsive breakpoint (640px) and button hover state
- Copyright footer for Individuate LLC

### Marketing page design exploration
- Designed one-page landing page in Paper with warm editorial aesthetic
- Instrument Serif display headline, Inter body text, terracotta (#C45D3E) accent
- Centered hero layout: headline, subtitle, download button, macOS requirement note
- Privacy-forward footer noting local-first architecture with Claude AI caveat
