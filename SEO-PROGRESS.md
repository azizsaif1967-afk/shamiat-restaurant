# Shamiat Restaurant — SEO/AEO/GEO Progress

## Final Audit Summary (2026-06-18)

**10-step SEO/AEO/GEO plan: COMPLETE.**

### What was built (Steps 1–10)

| Area | What was done |
|---|---|
| Schema | Restaurant + FAQPage (14 Q&As, 4 Arabic) + BreadcrumbList + Menu (3 sections, 12 items) + WebPage/Speakable — all 5 blocks valid JSON-LD |
| Local discovery | areaServed expanded to 19 towers/neighbourhoods on SZR; geo (25.22885, 55.286282); sameAs to 5 platforms |
| AEO/AI | llms.txt with nearby-buildings list and intent map; Speakable targeting #faq + hero H1 + lede |
| Image SEO | 9 image sitemap entries; OG image → dish-mansaf.jpg + alt; descriptive alts on all dish imgs |
| Content | #near-me section (4 neighbourhood cards); Arabic FAQ (dir=rtl, lang=ar); Arabic meta keywords |
| E-E-A-T | Reviews row with Talabat + Google Maps links; real sameAs URLs (no fabricated links) |
| Performance | LCP hero-poster preloaded; above-fold imgs fetchpriority=high; footer logo lazy-loaded |
| Discovery files | robots.txt (index,follow); sitemap.xml (image sitemap, lastmod 2026-06-18); llms.txt |

### Rich-result eligibility (verified 2026-06-18)
- **Restaurant**: ✅ eligible — name, address, telephone, image, aggregateRating all present
- **FAQPage**: ✅ eligible — 14 mainEntity Questions with acceptedAnswer
- **BreadcrumbList**: ✅ eligible — 2 ListItems with position/name/item
- **Menu**: ✅ valid — 3 MenuSections × 12 MenuItems with price/priceCurrency/HalalDiet
- **WebPage/Speakable**: ✅ valid

### Regression check (2026-06-18)
- H1: exactly 1 ✅
- Robots: `index,follow,max-image-preview:large` ✅
- Canonical: `https://shamiatrestaurant.com/` ✅
- OG URL: `https://shamiatrestaurant.com/` ✅

### Human TODOs (cannot be done by automation — require real data)
1. **Google Search Console**: Replace `REPLACE_WITH_YOUR_GSC_VERIFICATION_TOKEN` in `<head>` with your real GSC verification token.
2. **Google Business Profile URL**: Once you have your GBP URL (`https://g.page/r/YOUR_PLACE_ID`), add it to `sameAs` in the Restaurant schema and update the "Google reviews" link in the visit section (marked with a comment in the HTML).
3. **OG image check**: Verify `dish-mansaf.jpg` is at least 1200×630px and landscape-oriented for correct social share previews.
4. **Review schema**: Add real attributed `Review` entries to the Restaurant schema once you have verified review text from Google or Talabat. Do not fabricate.

---

## Plan

- [x] **Step 1** — Verify/strengthen LocalBusiness schema (geo, hours, areaServed towers, hasMenu, acceptsReservations, payment) + FAQPage + visible FAQ + llms.txt local facts + sitemap freshness.
  - _2026-06-12: geo ✓, hours ✓, hasMenu ✓, acceptsReservations ✓, paymentAccepted ✓, FAQPage (6 Q) ✓, visible FAQ ✓, sitemap lastmod ✓. Added 14 tower/neighbourhood entries to areaServed (19 total) and added nearby-towers section to llms.txt._

- [x] **Step 2** — Google Maps embed in the contact/visit area; NAP consistency across page+schema+llms; attributed Review entries (real text only, else TODO).
  _2026-06-13: Added dark-styled Google Maps iframe (coords 25.22885,55.286282, zoom 17) in visit section. Added missing `og:url` meta tag (NAP/URL consistency). Updated sitemap lastmod to 2026-06-13. NAP verified consistent across page, schema, llms.txt. All 3 JSON-LD blocks valid; 1 × h1; robots/canonical/OG intact._
  **Human TODO:** No real review text/URLs available — add attributed `Review` entries to Restaurant schema once you have verified Google/Talabat review text and URLs. (Do not fabricate.)

- [x] **Step 3** — Menu/MenuItem schema for top dishes + a definitional AEO first-sentence under each menu category heading.
  _2026-06-13: Added Menu JSON-LD with 3 MenuSections (Shamiat Specials ×6, Charcoal Grill ×3, Mezze & Appetizers ×3 = 12 MenuItem entries), all with price/priceCurrency/suitableForDiet:HalalDiet. Added `.cat-def` AEO definitional first-sentence under all 11 menu category headings. All 4 JSON-LD blocks parse valid; 1×h1; canonical/robots unchanged._

- [x] **Step 4** — Image SEO: descriptive alt on every img; dish-based OG/Twitter image; image sitemap entries.
  - _2026-06-13: Fixed 10 terse img alts (7 drink juice photos + 3 manakish: labneh/muhammara/spinach). Updated `og:image` and `twitter:image` from `og-shamiat.jpg` → `dish-mansaf.jpg` (mansaf is primary keyword dish). Added `og:image:alt` and `twitter:image:alt` tags. Added `xmlns:image` to sitemap.xml with 9 `<image:image>` entries (mansaf, mansaf mlahea, lamb chops, mixed grill, kunafa, oze lamb, fattoush, Shamiat spread, logo). All 4 JSON-LD blocks valid; 1 × h1; robots/canonical intact._
  **Human TODO:** Verify `dish-mansaf.jpg` renders well at 1200×630 in social share previews (OG standard ratio). If portrait/square, resize or revert to a landscape food photo for OG.

- [x] **Step 5** — Neighbourhood delivery content: short entity-rich paragraphs for Trade Centre, DIFC, Downtown Dubai, Business Bay.
  _2026-06-14: Added `#near-me` section with 4 entity-rich cards (Trade Centre & SZR towers, DIFC & Emirates Towers, Downtown Dubai & One Central, Business Bay). Each card names specific tower buildings, delivery platforms, dishes and hours — targeting "restaurant near [tower]" and "delivery to [neighbourhood]" queries. Added matching CSS (.nbh-grid/.nbh-card). All 4 JSON-LD blocks valid; 1 × h1; robots/canonical unchanged._

- [x] **Step 6** — Speakable schema + 3-4 more long-tail near-me FAQ entries (visible + schema).
  _2026-06-15: Added WebPage schema with SpeakableSpecification (cssSelector: #faq, section.hero h1, section.hero .lede). Expanded FAQPage from 6 → 10 questions with 4 new long-tail entries: "kebab near me SZR", "mansaf near me Dubai", "best restaurant near Duja Tower", "halal food open late SZR". Matching visible FAQ items added (10 total). All 5 JSON-LD blocks valid; 1 × h1; robots/canonical intact._

- [x] **Step 7** — E-E-A-T: Google Maps & Talabat review links; sameAs to Google Business Profile + Talabat store (real URLs only).
  - _2026-06-16: Expanded sameAs from 3 → 5 entries: added Talabat store URL (https://www.talabat.com/uae/restaurant/637743/...) and Deliveroo URL (https://deliveroo.ae/menu/dubai/sheikh-zayed/shamiat-restaurant) — both real verified URLs already used in the page. Added visible "Reviews & ratings · 4.5★ from 1,300+" row in visit/get-in-touch section with links to Google Maps listing and Talabat store. All 5 JSON-LD blocks valid; 1 × h1; canonical/robots intact._
  - **Human TODO:** Replace the Google Maps search URL in the "Google reviews" link with the direct Google Business Profile URL (e.g. https://g.page/r/YOUR_PLACE_ID/review) once you have it from Google Business. Also add it to sameAs. Comment in the HTML marks the exact spot.

- [x] **Step 8** — Core Web Vitals: img width/height, preload LCP image, lazy below-the-fold, defer non-critical JS.
  _2026-06-16: Added `<link rel="preload" as="image" href="images/hero-poster.jpg" fetchpriority="high">` in `<head>` (after preconnect hints) to preload the hero video poster — the LCP element on first paint. Added `fetchpriority="high"` to the intro-splash logo and nav brand-img (both above-fold). Added `loading="lazy"` to the footer logo (below-fold). No external scripts in the page — all JS is inline, so no defer/async needed. Dish `<img>` tags inside CSS `aspect-ratio:4/3` containers already have CLS controlled by the container. 1 × h1; robots/canonical intact._

- [x] **Step 9** — Arabic bilingual near-me keywords + short Arabic FAQ (مطعم سوري قريب مني، مطعم عربي شارع الشيخ زايد).
  _2026-06-17: Extended `<meta name="keywords">` with 6 Arabic near-me terms (مطعم سوري قريب مني, مطعم عربي قريب مني, مطعم حلال دبي, مشاوي قريب مني دبي, مطعم شامي دبي, مطعم لبناني شارع الشيخ زايد). Added 4 Arabic Q&As to FAQPage schema (14 questions total). Added visible Arabic FAQ subsection (dir="rtl" lang="ar") with 4 items: مطعم سوري قريب مني، مطعم عربي SZR، مشاوي DWTC، أوقات العمل. Sitemap lastmod → 2026-06-17. All 5 JSON-LD blocks valid; 1 × h1; robots/canonical/OG intact._

- [x] **Step 10** — Full re-audit: validate all JSON-LD, confirm rich-result eligibility (Restaurant, FAQ, Breadcrumb), fix regressions, write a final summary atop SEO-PROGRESS.md.
  _2026-06-18: All 5 JSON-LD blocks valid. Rich-result eligible: Restaurant ✅, FAQPage (14 Q) ✅, BreadcrumbList ✅, Menu ✅, WebPage/Speakable ✅. Fixed 1 regression: &amp; HTML entities in Restaurant makesOffer → replaced with plain &. Updated sitemap lastmod → 2026-06-18. Final summary written atop this file. 4 human TODOs logged._
