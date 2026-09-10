# TEST_REPORT — sindagi-cakewala-bakery-and-sweets

- `npm install`: PASS (87 packages)
- `npm run build`: PASS — `dist/index.html` 14.08 kB (gzip 3.65 kB), CSS 11.99 kB (gzip 3.25 kB), JS 1.20 kB (gzip 0.63 kB). Total `dist/` ≈ 36K.
- Base path: `/sindagi-cakewala-bakery-and-sweets/` ✓
- No-phone compliance: `grep -ci 'tel:\|wa.me'` on `index.html` = **0** — no `tel:`/`wa.me` links, no invented number. CTAs are Directions/Maps only; "Call for hours" is plain text.
- SEO: title + meta description + OG tags ✓; JSON-LD `Bakery` (no `telephone`) ✓
- A11y/perf: skip link ✓; async Google Fonts (`media="print" onload`) + `<noscript>` fallback ✓; `prefers-reduced-motion` in CSS ✓; dark text only, no light-orange text ✓
- Contrast spot-check: body ink #1F1B16 on cream #FFFBF2; brand-700 #A63F0D on white — dark, passes.

## Flags
- `data-missing=phone` — CSV phone empty; owner must supply number before any call CTA is added.
- Street-level address missing (city + PIN only) — visit uses city-level address + Maps link.
