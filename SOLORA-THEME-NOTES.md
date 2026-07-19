# Solora / Tierly demo store — theme rebuild notes

Working notes for the `solora-tierly` demo store theme (Dawn base → premium custom).
Purpose: a Solora/Tierly-branded showcase storefront (like shopvid.app markets Shopvid) that
demos Tierly volume pricing + provides App Store screenshots + reviewer demo. Last updated 2026-07-19.

## Direction (locked)
- **Aesthetic:** Warm Editorial — cream/peach gradients, serif display + clean sans, aurora glow,
  pill buttons, warm espresso ink (`#2E1D12`), accent gradient orange→rose (`#FF7A2F` → `#FF4D6D`).
- **Content:** Solora / **Tierly** (the app) — volume-pricing marketing, NOT a product brand.
- **Reference:** shopvid.app (Shopify store on the "Concept" theme marketing the Shopvid app).

## Files created / edited (in this downloaded theme folder)
- `sections/solora-hero.liquid` — hero (aurora bg, serif gradient headline, pill CTAs). Editable in theme editor.
- `sections/solora-marquee.liquid` — scrolling editorial band.
- `sections/solora-volume.liquid` — "Buy more, save more" tier cards (3+/6+/12+ → 10/18/25%) — the Tierly demo centerpiece.
- `sections/solora-value-props.liquid` — 4 Tierly features (Applied at checkout · No code · Target anything · See the lift).
- `assets/solora-premium.css` — global reskin: fonts, pill/gradient buttons, cards, radii, **warm header override** (killed the black bar), announcement bar.
- `layout/theme.liquid` — added Google Fonts <link> + `solora-premium.css`.
- `templates/index.json` — homepage composed: hero → marquee → Featured products → volume → value props.

## Fonts
- Currently **Fraunces** (display/serif) + **Inter** (body/sans), loaded via Google Fonts in `theme.liquid`.
- **TODO:** switch to match shopvid.app's fonts (detecting the exact families). Update the `<link>` in
  `theme.liquid` + the `font-family` refs in `solora-premium.css` and the section CSS.

## Apply / preview
```
cd "C:/Users/ACER/Downloads/shopify__solora-tierly"
shopify theme dev --store solora-tierly.myshopify.com   # live preview, hot reload
shopify theme push --store solora-tierly.myshopify.com  # when happy
```

## Done
- Homepage rebuilt (hero, marquee, featured collection, volume, value props).
- Header warm/translucent (was black); hero heading espresso (was cold black).
- Content pivoted coffee → Solora/Tierly.

## Next (tomorrow)
1. **Match shopvid font** (item above).
2. **Product page** — spotlight the Tierly price-table block + premium layout. ← most important for screenshots.
3. **Header/footer** polish; set store name to "Solora" (Settings → Store details) or upload a Solora logo (Header section).
4. Add **Story + Reviews + Newsletter** sections to round out the homepage; wire the "See how it works" button.
5. Optional: swap the snowboard sample products for cleaner demo products.
6. Then: capture the 6 App Store screenshots (see `Tierly/docs/app-listing.md`).

## Reminders
- This is the **demo store** for the Tierly App Store submission (see `Tierly/docs/app-store-submission.md`).
- Don't push/publish anything until Hank says so.
- Built on Dawn; Dawn's cart/checkout/search/account/JS left intact — only the visible surfaces are custom.
