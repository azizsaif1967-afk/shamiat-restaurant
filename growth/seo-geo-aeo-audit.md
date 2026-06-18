# Shamiat Restaurant — SEO / GEO / AEO Audit

**Site:** https://shamiatrestaurant.com · **Audited:** 2026-06-18
**Pages reviewed:** Home (`index.html`), `llms.txt`, `robots.txt`,
`sitemap.xml`, menu PDF. Single-page GitHub Pages site (CNAME live).

| Dimension | Score | Status |
|---|---|---|
| **SEO** | 9/10 | Strong |
| **GEO** (AI search) | 9/10 | Strong |
| **AEO** (answers/voice) | 9/10 | Strong |
| **Combined** | **27/30** | Strong |

This is an unusually well-optimized restaurant site. The work below is about
**extending reach into the hotel/concierge audience within ~2 km**, not fixing a
broken foundation.

---

## What's already strong
- **Rich, valid schema:** `Restaurant` (address, geo, hours, `aggregateRating`
  4.5★/1,300, `makesOffer`, `sameAs`, `areaServed`), `FAQPage`, `BreadcrumbList`.
- **Local signals:** geo meta (`geo.position`, `ICBM`), exact coordinates,
  Trade Centre First / DWTC / DIFC named throughout.
- **GEO-ready:** an `llms.txt` with quotable facts (most restaurants have none),
  clean crawlability, HTTPS, social `sameAs`.
- **AEO-ready:** question-phrased FAQ headings answered concisely; opening hours,
  delivery and location all extractable.
- **On-page hygiene:** single H1, descriptive title/meta, OG + Twitter cards,
  canonical, **every image (108) has alt text**, WhatsApp + `tel:` CTAs,
  six delivery platforms linked.

## Gaps addressed in this change (the "make noise" layer)
1. **Hotels were never named.** Added a `#hotels` section naming 16 SZR / Trade
   Centre hotels (Sheraton Grand, Fairmont, voco, Novotel/Ibis WTC, Four Points,
   Towers Rotana, Crowne Plaza, …) with a concierge + room-delivery hook.
2. **No "restaurant near [hotel]" / "deliver to my hotel room" answers.** Added
   3 FAQ entries (visible + `FAQPage` schema) targeting exactly those queries.
3. **`areaServed` broadened** to include the flagship hotels and Museum of the
   Future, strengthening the local entity graph for AI engines.

## Priority recommendations (next)

| Priority | Action | Why |
|---|---|---|
| 🔴 Critical | Replace `REPLACE_WITH_YOUR_GSC_VERIFICATION_TOKEN` with the real Google Search Console token | Can't track/track impressions or submit sitemap without it |
| 🟠 High | Keep **Google Business Profile** active — weekly post, photos, reply to every review | The local pack drives most "near me" calls; biggest lever for phone volume |
| 🟠 High | Run the **concierge outreach** in `hotel-outreach-kit.md` (cards on desks) | Turns proximity into referrals — the offline half of "guests ringing" |
| 🟡 Medium | Build local citations (Zomato, TripAdvisor, Yelp, delivery apps) with identical NAP | Consistency boosts local ranking + entity confidence |
| 🟡 Medium | Add `Menu`/`hasMenu` as structured `Menu` items (beyond the PDF link) | Lets AI engines answer dish-level questions |
| 🟢 Quick win | Confirm `images/og-shamiat.jpg` renders well in link previews | Social/WhatsApp share CTR |

## Can't assess from HTML (use a tool)
- **Core Web Vitals / speed** → run pagespeed.web.dev (note: 12.7 MB menu PDF
  and several large JPGs — compress for mobile).
- **Actual rankings / local pack position** → track weekly via the Friday routine.
- **Backlinks / domain authority** → external tool.

---

*Re-run after changes via the `shamiat-friday` skill; it re-checks visibility
and logs progress weekly.*
