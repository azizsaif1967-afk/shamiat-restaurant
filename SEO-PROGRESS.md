# Shamiat Restaurant — SEO/AEO/GEO Progress

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

- [ ] **Step 5** — Neighbourhood delivery content: short entity-rich paragraphs for Trade Centre, DIFC, Downtown Dubai, Business Bay.

- [ ] **Step 6** — Speakable schema + 3-4 more long-tail near-me FAQ entries (visible + schema).

- [ ] **Step 7** — E-E-A-T: Google Maps & Talabat review links; sameAs to Google Business Profile + Talabat store (real URLs only).
  - _TODO (human): Find and supply the real Google Business Profile URL for Shamiat Restaurant to add as a sameAs entry._

- [ ] **Step 8** — Core Web Vitals: img width/height, preload LCP image, lazy below-the-fold, defer non-critical JS.

- [ ] **Step 9** — Arabic bilingual near-me keywords + short Arabic FAQ (مطعم سوري قريب مني، مطعم عربي شارع الشيخ زايد).

- [ ] **Step 10** — Full re-audit: validate all JSON-LD, confirm rich-result eligibility (Restaurant, FAQ, Breadcrumb), fix regressions, write a final summary atop SEO-PROGRESS.md.
