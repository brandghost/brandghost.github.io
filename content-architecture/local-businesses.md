# Cluster Spec: Local Businesses Vertical (Phase 1 — LOCKED)

> Produced by the `hub-spoke-topic-architecture` skill. Phase 1 build of the
> Local Businesses vertical under Cluster Group 15 (Vertical Audience Clusters).
> Lives at top-level folder `_posts/local-businesses/`, not under
> `small-business/` or `_posts/small-business/local-business/`.
>
> Build sequencing: this cluster's articles publish on even days from
> 2026-07-04 through 2026-07-18 at 06:00 UTC. The hub publishes first. Same-cluster
> forward links are prohibited: an article may link only to same-cluster spokes
> with past or same-day publish dates. Hub-to-spoke links are added only after the
> target spoke exists via `blog-internal-link-pipeline`.

---

## Hub Definition

- **Working title:** Social Media and Local SEO for Small Local Businesses: Complete Guide
- **Folder slug:** `local-businesses/`
- **Primary keyword:** `local business social media marketing` (480/mo, LOW)
- **Primary intent:** Informational (secondary: commercial investigation — owner/operators deciding which local discoverability actions are worth their limited time)
- **Target audience:** Solo operators and small teams running single-location or small-service-area businesses that customers visit or hire nearby: restaurants, salons, contractors, retail shops, fitness studios, clinics, repair shops, and other local service providers. Excludes real estate agents/brokers because `real-estate/` is its own top-level vertical.
- **Hub mission:** Give local businesses a complete, practical operating model for getting found by nearby customers without an enterprise local-SEO stack: Google Business Profile + Maps/local SEO + reviews/citations + local social/community + voice/AI answer readiness + repeatable content workflows.
- **Audience proof points:**
  - Restaurants/cafes: menu updates, Google Maps photos, reviews, specials, event posts.
  - Salons/spas: service photos, before/after examples, stylist availability, local reviews.
  - Contractors/home services: project photos, service-area language, seasonal tips, trust signals.
  - Retail/boutiques: local inventory, product arrivals, visual search/Pinterest, in-store events.
  - Fitness studios/gyms: class schedules, instructor highlights, member-community prompts, local partnerships.
  - Clinics/wellness/service providers: location clarity, appointment/service FAQs, practitioner credentials, review hygiene.
- **Opening framing:** The hub should define "local businesses" as businesses customers visit or hire nearby, then make the wedge explicit: this is an integrated small-team local discoverability guide, not a BrightLocal/Yext/Moz/SOCi-style listings-management buyer guide.
- **Locked L1 opening boundary sentence:** "This guide is local SEO for businesses customers visit or hire nearby (restaurants, salons, contractors, retail, fitness studios). For general SEO basics, see the SEO mini-hub at `discoverability/seo/seo-for-small-business`."
- **Canonical angle:** Local-discoverability operating system for owner/operators with no dedicated SEO team, no enterprise tooling budget, and no time for a 40-step local SEO checklist. The hub uses social media as the differentiating lens while borrowing demand from GBP/local SEO, AI tools, community, and visual/voice discoverability spokes.

### Validation

- Can stand alone as a flagship page targeting `local business social media marketing`, `social media for local business`, `online presence for small business`, and adjacent `local SEO for small business` support.
- Not a listicle — synthesizes local search, social/community, voice/AI readiness, and recurring content workflows into one coherent operating model.
- Risk: pressure to make the hub a local SEO encyclopedia. Hub must signpost L1 for GBP/local SEO depth and `discoverability/seo/seo-for-small-business` for general SEO basics.

---

## Spoke Table

| # | Slug | Title | Primary keyword | Vol / Comp | Funnel | Locked publish date | Dual-home | Summary |
|---:|---|---|---|---:|---|---|---|---|
| Hub | `local-business-social-media-marketing-complete-guide` | Social Media and Local SEO for Small Local Businesses: Complete Guide | `local business social media marketing` | 480 / LOW | TOFU | 2026-07-04 06:00 UTC | — | Mega hub for the integrated local discoverability model: GBP/local SEO, reviews, local social, voice/AI, visual/community, and content workflow. |
| L1 | `local-seo-google-business-profile-small-local-businesses` | Local SEO and Google Business Profile Optimization for Local Businesses | `Google Business Profile optimization` | 9,900 / LOW | MOFU | 2026-07-06 06:00 UTC | — | Google Business Profile, Maps, citations/NAP, reviews, GBP posts/photos, and "near me" local pack basics; explicitly excludes general SEO basics. |
| L2 | `voice-search-for-local-businesses` | Voice Search for Local Businesses: How to Show Up for “Near Me” Queries | `voice search local` | 720 / LOW | MOFU | 2026-07-08 06:00 UTC | `discoverability/aeo/` | Local voice-search application: "best [service] near me," review/entity signals, service-area phrasing, local FAQs, and LocalBusiness schema basics; excludes generic voice mechanics. |
| L3 | `best-social-media-platforms-local-businesses` | Best Social Media Platforms for Local Businesses | `best social media for small businesses` | 90 / MED | TOFU | 2026-07-10 06:00 UTC | — | Platform-choice guide for Instagram, Facebook, TikTok, Nextdoor, Pinterest, YouTube, and GBP posts; excludes deep platform playbooks. |
| L4 | `local-business-content-calendar-ideas` | 30-Day Local Business Content Calendar and Post Ideas | `small business social media ideas` | 170 / MED | TOFU | 2026-07-12 06:00 UTC | — | Combines local post ideas and a 30-day calendar because exact local calendar/content terms are tiny; broad examples only, no sub-vertical mini-spokes yet. |
| L5 | `ai-marketing-tools-local-businesses` | AI Marketing Tools for Local Businesses: What Helps Small Teams Save Time | `ai marketing tools for small business` | 3,600 / MED | MOFU | 2026-07-14 06:00 UTC | — | AI tool categories for small local teams: content drafting, repurposing, review-response support, calendar generation, and Launchpad funnel; excludes generic AI-writing tutorials. |
| L6 | `local-community-marketing-reddit-nextdoor-facebook-groups` | Local Community Marketing: Reddit, Nextdoor, Facebook Groups, and Neighborhood Forums | `nextdoor marketing` | 170 / MED | MOFU | 2026-07-16 06:00 UTC | `discoverability/multi-channel/MC3` | Neighborhood/community discoverability for Nextdoor, local subreddits, Facebook Groups, forums, chambers, and associations; excludes spam/link-building tactics. |
| L7 | `local-visual-search-pinterest-google-maps-photos` | Local Visual Search: Pinterest, Google Lens, and Google Maps Photos for Local Businesses | `Pinterest visual search` | 1,300 / LOW | MOFU | 2026-07-18 06:00 UTC | `discoverability/multi-channel/MC4` | Local visual trust and discovery: storefront photos, service photos, before/after examples, menus/products, GBP photo hygiene, Google Lens, and Pinterest local boards. |

**Total Phase 1: 1 mega hub + 7 spokes = 8 articles.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent | Funnel |
|---|---|---|---|
| Local Businesses mega hub | Informational | Commercial investigation | TOFU |
| L1: Local SEO + GBP | Commercial investigation | Informational | MOFU |
| L2: Local voice search | Commercial investigation | Informational | MOFU |
| L3: Best social platforms | Informational | Commercial investigation | TOFU |
| L4: Content calendar + ideas | Informational | — | TOFU |
| L5: AI marketing tools | Commercial investigation | Informational | MOFU |
| L6: Local community marketing | Commercial investigation | Informational | MOFU |
| L7: Local visual search | Commercial investigation | Informational | MOFU |

Funnel mix: 3 TOFU pages (hub, L3, L4) + 5 MOFU pages (L1, L2, L5, L6, L7) + 0 BOFU pages. No BOFU article is planned in this vertical; product-heavy conversion belongs in `brandghost/launchpad/`, with L5 and the hub providing the funnel handoff.

---

## Internal Linking Summary

### Mandatory upward links

- L1, L2, L3, L4, L5, L6, L7 → Local Businesses mega hub.
- Local Businesses mega hub → Discoverability mega hub (`brand-discoverability-complete-guide-2026`) as the cross-vertical strategy parent.
- Local Businesses mega hub → `brandghost/launchpad/` as the product execution destination.
- L1 → `discoverability/seo/seo-for-small-business` using the locked boundary framing sentence.
- L2 → `discoverability/aeo/` mini-hub as secondary parent context. The file still lives only in `_posts/local-businesses/`.
- L6 → `discoverability/multi-channel/` mini-hub and MC3 community-discoverability context. The file still lives only in `_posts/local-businesses/`.
- L7 → `discoverability/multi-channel/` mini-hub and MC4 visual-search context. The file still lives only in `_posts/local-businesses/`.

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Local Businesses mega hub → L1, L2, L3, L4, L5, L6, L7, but only after each target article exists. The hub publishes on 2026-07-04, so it must not include same-cluster spoke URLs at initial write time.
- Discoverability AEO hub → L2 after L2 publishes on 2026-07-08.
- Discoverability Multi-Channel hub / MC3 → L6 after L6 publishes on 2026-07-16.
- Discoverability Multi-Channel hub / MC4 → L7 after L7 publishes on 2026-07-18.
- Small Business hub → Local Businesses mega hub after the Local Businesses hub is live.

### Same-cluster sibling link matrix (NO forward-date links)

Only past or same-day same-cluster spokes are eligible. Use these only when contextually justified; do not force links just because the date permits them.

| Article | Publish date | Same-cluster spokes it may link to at write time | Same-cluster spokes it must NOT link to |
|---|---|---|---|
| Hub | 2026-07-04 | None at initial write time | L1, L2, L3, L4, L5, L6, L7 until each target is live and the link pipeline adds downlinks |
| L1 | 2026-07-06 | None | L2, L3, L4, L5, L6, L7 |
| L2 | 2026-07-08 | L1 | L3, L4, L5, L6, L7 |
| L3 | 2026-07-10 | L1, L2 | L4, L5, L6, L7 |
| L4 | 2026-07-12 | L1, L2, L3 | L5, L6, L7 |
| L5 | 2026-07-14 | L1, L2, L3, L4 | L6, L7 |
| L6 | 2026-07-16 | L1, L2, L3, L4, L5 | L7 |
| L7 | 2026-07-18 | L1, L2, L3, L4, L5, L6 | None |

### Justified spoke-to-spoke links

- L2 (local voice search) → L1 (GBP/local SEO) — voice "near me" eligibility depends on local entity, review, and GBP signals.
- L3 (best social platforms) → L1 (GBP/local SEO) — GBP posts/photos are a local discovery surface, not just an SEO task.
- L4 (content calendar) → L1 and L3 — calendar readers need GBP posting context and platform-choice context.
- L5 (AI tools) → L1, L3, and L4 — AI workflows support GBP/social assets and recurring local calendars.
- L6 (local community) → L1, L3, and L4 — community mentions and local groups reinforce local trust, platform choice, and calendar planning.
- L7 (local visual search) → L1, L3, L4, and L6 — visual proof supports GBP/Maps, platform selection, calendar execution, and community trust.

No circular sibling dependencies: all same-cluster sibling links flow from later-dated articles to earlier-dated articles.

### Cross-cluster links (mandatory at write time when target exists)

| From | To | Reason |
|---|---|---|
| Mega hub | `discoverability/` mega hub | Discoverability is the strategy umbrella this vertical applies locally. |
| Mega hub | `brandghost/launchpad/` mega hub | Product funnel handoff; Launchpad is the execution destination. |
| Mega hub | Relevant platform hubs: `social-media-platforms/instagram/`, `social-media-platforms/facebook/`, `social-media-platforms/tiktok/`, `social-media-platforms/pinterest/`, `social-media-platforms/youtube/` | Local social execution depends on the platform hubs for general platform mechanics. |
| Mega hub | `small-business/` hub if live | Cross-vertical SMB foundation; defer if the hub is still only a stub. |
| L1 | `discoverability/seo/seo-for-small-business` | Boundary link: generic SMB SEO belongs to SEO mini-hub; L1 owns local SEO/GBP. |
| L2 | `discoverability/aeo/` and existing voice-search optimization article | AEO owns generic voice-search mechanics; L2 owns local application. |
| L4 | `content-planning/content-calendar/` hub | Generic calendar theory lives outside the vertical; L4 applies it locally. |
| L5 | `brandghost/launchpad/` mega hub | Launchpad is the execution surface for AI-assisted local content workflows. |
| L6 | `discoverability/multi-channel/MC3` community-discoverability context | MC3 owns generic Reddit/Quora/forum discoverability; L6 owns local/community application. |
| L7 | `discoverability/multi-channel/MC4` visual-search context | MC4 owns generic visual search; L7 owns local visual trust and GBP/Maps/photo application. |

### Cross-cluster links (added post-publish)

- `discoverability/aeo/` hub and voice-search article → L2.
- `discoverability/multi-channel/` hub and MC3 → L6.
- `discoverability/multi-channel/` hub and MC4 → L7.
- `discoverability/seo/seo-for-small-business` → L1 as the local SEO application link.
- `brandghost/launchpad/` hub → Local Businesses mega hub and L5.
- Small Business hub ↔ Local Businesses mega hub.

### Forward-link constraints

- Hub publishes first on 2026-07-04. It may not link to L1-L7 at initial write time because all seven spokes are future-dated.
- L1 (2026-07-06) must not link to L2-L7.
- L2 (2026-07-08) must not link to L3-L7.
- L3 (2026-07-10) must not link to L4-L7.
- L4 (2026-07-12) must not link to L5-L7.
- L5 (2026-07-14) must not link to L6-L7.
- L6 (2026-07-16) must not link to L7.
- L7 (2026-07-18) has no future same-cluster spoke targets.
- If any cross-cluster dual-home target is not live at write time, defer that link to post-publish pipeline rather than inserting a future URL.

---

## Risk Notes

### Cannibalization risk: MEDIUM cross-cluster, LOW internal if boundaries hold

**Internal to the cluster:**

- **Hub vs L1 (Local SEO + GBP):** Hub must not become a full local SEO guide. Mitigation: hub frames local SEO as one pillar and points to L1 for GBP/Maps/citations/reviews depth.
- **L3 (Best Platforms) vs L4 (Content Calendar):** L3 is where to show up; L4 is what/when to post. L3 should not include a 30-day calendar, and L4 should not re-rank platforms.
- **L3 (Best Platforms) vs L6 (Community Marketing):** L3 may mention Nextdoor/Facebook Groups as channels; L6 owns participation, neighborhood trust, and community-specific workflows.
- **L3/L4 vs L7 (Visual Search):** Platform/calendar articles may mention photos; L7 owns search/discovery through Google Maps photos, Google Lens, Pinterest visual search, storefront images, and local proof.

**Cross-cluster:**

- **Boundary risk vs `discoverability/seo/seo-for-small-business`:** The SEO mini-hub owns general small-business SEO: technical basics, on-page SEO, content structure, and search fundamentals. L1 owns local customer discovery: GBP, Maps/local pack, reviews, citations/NAP, location/service-area pages, and "near me" behavior. Mitigation is the locked L1 opening sentence: "This guide is local SEO for businesses customers visit or hire nearby (restaurants, salons, contractors, retail, fitness studios). For general SEO basics, see the SEO mini-hub at `discoverability/seo/seo-for-small-business`."
- **Boundary risk vs `small-business/` legacy and `_posts/small-business/local-business/` scaffold:** Small Business is cross-vertical SMB education. Local Businesses is a top-level Cluster Group 15 vertical. Do not write into `_posts/small-business/local-business/` or its subfolders; the scaffold stays empty unless a future cleanup removes it.
- **Real estate exclusion:** Real estate agents are local businesses in the real world, but `real-estate/` already owns realtor/broker-specific keywords, examples, and content. Local Businesses should exclude realtor/broker-specific examples except brief contrast language.
- **Dual-home risk vs `discoverability/aeo/`:** AEO owns generic voice mechanics; L2 owns local voice queries, local entity/review signals, service-area phrasing, local FAQs, and LocalBusiness schema basics.
- **Dual-home risk vs `discoverability/multi-channel/MC3`:** MC3 owns generic community discoverability; L6 owns neighborhood/community application for Nextdoor, local subreddits, Facebook Groups, chambers, associations, and local forums.
- **Dual-home risk vs `discoverability/multi-channel/MC4`:** MC4 owns generic visual search; L7 owns local visual trust and discovery through storefront/service/product images, GBP/Maps photo hygiene, Google Lens, and local Pinterest use cases.
- **Wedge discipline vs BrightLocal/Yext/Moz/SOCi:** Do not compete as an enterprise local-SEO platform, listings-sync platform, citation-management buyer guide, franchise local-marketing suite, or Moz-style SEO encyclopedia. Wedge is small-team / single-location / no-budget local discoverability with practical weekly workflows.
- **Boundary risk vs `brandghost/launchpad/`:** Launchpad owns product/category pages. Local Businesses remains audience/problem-led. Only L5 should be overtly product-adjacent; the hub can include a restrained conversion handoff.

### Ambiguous intent: NONE

All Phase 1 pages have a single primary intent. The hub legitimately carries secondary commercial-investigation intent because complete-guide content naturally answers "what should I do" and "what tools might help" without becoming a product page.

### Pages that may need future splitting

- **L1 (Local SEO + GBP)** may split into `google-maps-seo-local-businesses`, `local-citations-for-small-businesses`, and `multi-location-seo-small-business` if those subsections earn impressions.
- **L3 (Best Platforms)** may split into local-business platform playbooks for Instagram, Facebook, TikTok, Nextdoor, Pinterest, or YouTube if traffic validates demand.
- **L4 (Content Calendar + Ideas)** may split into separate "content ideas" and "content calendar" spokes if exact local terms grow.
- **L6 (Local Community Marketing)** may split into Nextdoor-only, Reddit-only, Facebook Groups-only, or chamber/association visibility articles.
- **L7 (Local Visual Search)** may split into Pinterest-specific, Google Lens-specific, and Google Maps/GBP photo optimization articles.

### Deferred to later phases (NOT Phase 1)

- Sub-vertical mini-spokes: restaurants, salons, contractors, retail, fitness.
- Additional sub-verticals only after validation: clinics, repair shops, events/hospitality, and other local service providers.
- Dedicated Google Maps SEO spoke.
- Dedicated local citations spoke.
- Dedicated multi-location SEO spoke.
- City-specific/local-geo landing-page content.
- Success stories or testimonials unless verifiably published; do not fabricate examples or metrics.

### Build-order constraints

- The 8-article schedule is locked: 2026-07-04, 07-06, 07-08, 07-10, 07-12, 07-14, 07-16, 07-18 at 06:00 UTC.
- Hub publishes first.
- Same-cluster sibling links must follow chronological order only.
- Dual-home files are not duplicated. All articles live as single files under `_posts/local-businesses/`; secondary clusters cross-link via the internal-link pipeline after publish.

---

## Phase 1 Deliverable Summary

| Slug (locked) | Folder | Funnel | Spoke # | hub: true? | Primary keyword | Vol / Comp | Locked publish date | Dual-home? |
|---|---|---|---|---|---|---:|---|---|
| `local-business-social-media-marketing-complete-guide` | `local-businesses/` | tofu | (mega hub) | yes | `local business social media marketing` | 480 / LOW | 2026-07-04 06:00 UTC | — |
| `local-seo-google-business-profile-small-local-businesses` | `local-businesses/` | mofu | L1 | no | `Google Business Profile optimization` | 9,900 / LOW | 2026-07-06 06:00 UTC | — |
| `voice-search-for-local-businesses` | `local-businesses/` | mofu | L2 | no | `voice search local` | 720 / LOW | 2026-07-08 06:00 UTC | `discoverability/aeo/` |
| `best-social-media-platforms-local-businesses` | `local-businesses/` | tofu | L3 | no | `best social media for small businesses` | 90 / MED | 2026-07-10 06:00 UTC | — |
| `local-business-content-calendar-ideas` | `local-businesses/` | tofu | L4 | no | `small business social media ideas` | 170 / MED | 2026-07-12 06:00 UTC | — |
| `ai-marketing-tools-local-businesses` | `local-businesses/` | mofu | L5 | no | `ai marketing tools for small business` | 3,600 / MED | 2026-07-14 06:00 UTC | — |
| `local-community-marketing-reddit-nextdoor-facebook-groups` | `local-businesses/` | mofu | L6 | no | `nextdoor marketing` | 170 / MED | 2026-07-16 06:00 UTC | `discoverability/multi-channel/MC3` |
| `local-visual-search-pinterest-google-maps-photos` | `local-businesses/` | mofu | L7 | no | `Pinterest visual search` | 1,300 / LOW | 2026-07-18 06:00 UTC | `discoverability/multi-channel/MC4` |

**Total: 8 articles** (1 hub + 7 spokes, 3 of them dual-homed by cross-link only).

Slugs, primary keywords, dates, folder path, and dual-home targets are locked by the radar and user inputs. No article content is produced by this spec. No duplicate files are created outside `_posts/local-businesses/`.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 1 with no further architectural questions.
- Each of the 8 articles has an unambiguous reason to exist and a single primary intent.
- The 8-article schedule exactly fills the 2026-07-04 → 2026-07-18 even-day window at 06:00 UTC.
- L1 opens with the locked SEO-boundary framing sentence and does not cannibalize `discoverability/seo/seo-for-small-business`.
- L2, L6, and L7 dual-home by cross-link only; no duplicate files are created in Discoverability folders.
- No article is written to `_posts/small-business/local-business/` or any scaffolded subfolder.
- Real estate examples and realtor/broker keywords are excluded because `real-estate/` owns that vertical.
- Wedge positioning remains small-team / single-location / no-budget, not enterprise local SEO tooling.
- No same-cluster article contains a forward-dated sibling link.
