# Cluster Spec: Brand Discoverability — Multi-Channel Mini-Hub (Phase 5)

> Produced by the `hub-spoke-topic-architecture` skill. Multi-Channel is the
> fifth mini-hub under the `discoverability/` cluster (after GEO Phase 1,
> AEO Phase 2, SEO Phase 3, Brand Authority Phase 4). Completes the
> 4-pillar Discoverability framework named in the M1 "4 Pillars" article
> (Social Search is the 4th pillar; this mini-hub anchors it).
> Architecture is radar-informed; see
> `~\.copilot\session-state\8c7dca5e-bb24-43e8-b92a-fd3840f71556\files\content-radar-multi-channel-2026-06-11.md`.
>
> Companion to: `README.md` (master) and sibling specs `discoverability.md`,
> `discoverability-aeo.md`, `discoverability-seo.md`,
> `discoverability-brand-authority.md` — all colocated in `content-architecture/`.
>
> Note: 2 migrated articles already exist in `_posts/discoverability/multi-channel/`
> from the earlier `seo/*` migration. This phase adds the hub + 4 new spokes
> that BIND those existing articles plus add tactical depth on specific surfaces
> (TikTok, YouTube, Reddit/community, visual search).

---

## Hub Definition (Mini-Hub)

- **Working title:** Multi-Channel Discoverability: Beyond Google Search
- **Folder slug:** `discoverability/multi-channel/`
- **Primary intent:** Informational (secondary: commercial investigation)
- **Target audience:** Marketers, founders, and content owners who already know SEO/GEO/AEO matters but are losing customers to discovery on TikTok, YouTube, Reddit, Pinterest, and other in-platform search experiences. The reader has been treating these as "social media marketing" and hasn't realized they're now *search* surfaces.
- **Core problem solved:** Defines Social Discovery as the fourth pillar of Brand Discoverability — the SEO-equivalent layer that operates inside TikTok, YouTube, Reddit, Pinterest, and other platforms where users now search instead of (or before) Google. Frames each major surface, explains why in-platform search behaves differently than Google search, and signposts tactical spokes.
- **Canonical angle:** Wedge per radar — "Social Discovery for small teams beyond Google." Not "social media marketing" (the social-media-platforms/ clusters cover that). Not enterprise multi-channel analytics (Brandwatch, Sprinklr own that). Specifically: in-platform *search* optimization across TikTok, YouTube, Reddit, Pinterest for teams without enterprise tooling.

### Validation

- Can rank for `social media SEO` (3,600/mo LOW per radar) and act as the canonical Social Discovery framework reference.
- Not a listicle — synthesizes in-platform search across multiple surfaces into one coherent discipline.
- Risk: confusion with the `social-media-platforms/*` clusters, which cover *how to post and schedule*. Mini-hub must explicitly frame "discoverability ON the platform" as distinct from "posting TO the platform."

---

## Existing Migrated Articles (already in folder)

| File | Topic | Role in cluster |
|---|---|---|
| `_posts/discoverability/multi-channel/2026-06-10-discoverability-optimization-the-future-of-seo-beyond-websites.md` | The shift from website-only SEO to multi-channel discoverability | Existing spoke — broad framework piece, predates this hub |
| `_posts/discoverability/multi-channel/2026-06-12-multi-channel-discoverability-your-guide-to-online-presence.md` | Cross-platform online presence guide | Existing spoke — practical "where to show up" piece |

Both are TOFU, broad-scope. The new hub binds them and adds surface-specific tactical depth. New spokes must NOT duplicate the broad-framing scope these two cover.

---

## Spoke Table (new spokes for this build — Phase 5)

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| MC1 | TikTok SEO: How to Get Found in TikTok's Search Engine | Commercial investigation | TikTok's in-platform search behavior; how TikTok ranks results; caption + hashtag + cover text optimization; the "TikTok as Gen Z's Google" shift; content patterns that surface in search vs feed | TikTok scheduling / posting mechanics (lives in `social-media-platforms/tiktok/scheduling/`); TikTok analytics; TikTok algorithm theory for organic feed reach | Multi-Channel mini-hub |
| MC2 | YouTube SEO for Small Teams (Without Spending on TubeBuddy) | Commercial investigation | YouTube's in-platform search; title + description + tags + thumbnail optimization for search vs suggested; chapter timestamps for snippet eligibility; small-team workflow without enterprise tooling | YouTube creator monetization; enterprise YouTube SEO platforms (TubeBuddy, vidIQ deep dives); how to schedule YouTube videos (lives in `social-media-platforms/youtube/`); subscriber-growth tactics unrelated to search | Multi-Channel mini-hub |
| MC3 | Community Discoverability: How to Be Found on Reddit, Quora, and Niche Forums | Commercial investigation | Reddit search behavior; Quora answer discoverability; niche forum visibility; ethical community participation as a discoverability play; what gets flagged as spam vs welcome contribution | Reddit advertising / paid Reddit; pure SEO link-building from Reddit (link economy plays); spam tactics | Multi-Channel mini-hub |
| MC4 | Visual Search Optimization: Pinterest, Google Lens, and Image Discoverability | Commercial investigation | Pinterest search + visual recognition; Google Lens behavior; image alt + filename + EXIF; Pinterest pin structure for in-platform search; how visual search differs from text search | Pinterest scheduling (lives in `social-media-platforms/pinterest/`); pure SEO image optimization for Google (overlaps with SEO mini-hub on-page checklist — link, don't duplicate); enterprise visual analytics platforms | Multi-Channel mini-hub |

**Total Phase 5 build: 1 mini-hub + 4 new spokes = 5 new articles. Combined with 2 existing migrated articles, the cluster will have 7 articles total.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| Mini-hub | Informational | Commercial investigation |
| MC1: TikTok SEO | Commercial investigation | Informational |
| MC2: YouTube SEO | Commercial investigation | Informational |
| MC3: Community Discoverability | Commercial investigation | Informational |
| MC4: Visual Search Optimization | Commercial investigation | Informational |
| Migrated: Discoverability Beyond Websites | Informational | — |
| Migrated: Multi-Channel Online Presence Guide | Informational | — |

Mix: 1 hub + 4 commercial-investigation tactical + 2 existing informational. Healthy split — the migrated articles cover framework; new spokes are surface-specific tactics.

---

## Internal Linking Summary

### Mandatory upward links

- MC1, MC2, MC3, MC4 → Multi-Channel mini-hub
- Mini-hub → Discoverability mega hub (`brand-discoverability-complete-guide-2026`, 2026-06-11)
- Mini-hub → migrated existing articles in same folder (binds them)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Mini-hub → MC1, MC2, MC3, MC4
- Discoverability mega hub → Multi-Channel mini-hub
- M1 "4 Pillars" → Multi-Channel mini-hub
- GEO, AEO, SEO, Brand Authority mini-hubs → Multi-Channel mini-hub (sibling references)

### Justified spoke-to-spoke links

- MC1 (TikTok) ↔ MC2 (YouTube) — both video-first surfaces; readers often want both
- MC3 (Community) → MC1, MC2 — community visibility benefits from video content existing elsewhere
- MC4 (Visual Search) → MC1, MC2 — visual platforms intersect (Pinterest <-> YouTube thumbnails <-> TikTok covers)

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mini-hub | `_posts/discoverability/2026-06-11-brand-discoverability-complete-guide-2026.md` | Mandatory up-link |
| Mini-hub | Both migrated articles in same folder | Hub binds existing spokes |
| Mini-hub | `_posts/discoverability/geo/2026-06-12-generative-engine-optimization-complete-guide.md` | Sibling mini-hub reference |
| Mini-hub | `_posts/discoverability/seo/2026-06-13-seo-best-practices.md` | Sibling mini-hub reference |
| Mini-hub | `_posts/discoverability/aeo/2026-06-19-answer-engine-optimization-complete-guide.md` | Sibling mini-hub reference |
| Mini-hub | `_posts/discoverability/brand-authority/2026-06-14-brand-authority-ai-era.md` | Sibling foundational layer reference |
| MC1 (TikTok) | `_posts/social-media-platforms/tiktok/2026-03-25-tiktok-for-content-creators.md` | Platform hub for reader who wants TikTok generally |
| MC1 (TikTok) | `_posts/social-media-platforms/tiktok/scheduling/2026-03-18-how-to-schedule-tiktok-posts.md` | "How to post" complement to "how to be found" |
| MC2 (YouTube) | `_posts/social-media-platforms/youtube/2026-04-04-how-to-schedule-youtube-videos.md` | YouTube scheduling complement |
| MC2 (YouTube) | `_posts/social-media-platforms/youtube/timing/2026-05-27-youtube-upload-schedule-day-of-week.md` | Timing complement |
| MC3 (Community) | None at write time (no Reddit deep-content elsewhere in repo) | — |
| MC4 (Visual Search) | `_posts/social-media-platforms/pinterest/2026-03-23-pinterest-for-content-creators.md` | Pinterest platform hub |
| MC4 (Visual Search) | `_posts/social-media-platforms/pinterest/scheduling/2026-02-06-how-to-schedule-pinterest-pins.md` | Pinterest scheduling complement |

### Cross-cluster links (added post-publish)

- Multi-Channel ↔ Launchpad cluster (Launchpad's `content-creation-workflow` spoke touches multi-channel output)
- Multi-Channel ↔ `content-repurposing/` cluster (repurposing is the production tactic that enables multi-channel presence)
- Multi-Channel ↔ vertical clusters (vertical-specific "social discovery for [vertical]" spokes eventually)
- Multi-Channel ↔ AEO mini-hub voice search article (voice and social-platform search both bypass Google)

### Forward-link constraint check

All cross-cluster targets above are published BEFORE the Multi-Channel hub's publish date (06-25). Verified:
- Discoverability mega hub 2026-06-11 ✓
- Both migrated articles 2026-06-10/12 ✓
- GEO mini-hub 2026-06-12 ✓
- SEO mini-hub 2026-06-13 ✓
- AEO mini-hub 2026-06-19 ✓
- Brand Authority mini-hub 2026-06-14 ✓
- All social-media-platforms targets (March/April/May 2026) ✓

No forward-link risk at write time.

---

## Risk Notes

### Cannibalization risk — clearly bounded

**Internal to the cluster:**

- **Mini-hub vs the 2 migrated articles:** Mitigation: Mini-hub frames the *4-pillar position* (Social Discovery as a discipline, why it matters, what surfaces it covers, signpost to spokes). The migrated articles cover the broader *shift narrative* (SEO → multi-channel). Mini-hub references them as context; doesn't restate their argument.
- **MC1 vs MC2 vs MC3 vs MC4:** All four are surface-specific. Boundaries are obvious: TikTok ≠ YouTube ≠ Reddit ≠ Pinterest/visual. Each must explicitly name its surface(s) in title and opening paragraph.

**External:**

- **Vs `social-media-platforms/*` clusters (HIGH attention required):** Those clusters own "how to schedule / post / time" tactics per platform. Multi-Channel mini-hub owns "how to be DISCOVERED on the platform via in-platform search." Strict boundary:
  - `social-media-platforms/tiktok/scheduling/` = how to post on TikTok
  - `discoverability/multi-channel/MC1` = how TikTok search ranks content
  - Different reader intent, different keyword target. MC1's primary keyword is `TikTok SEO` (3,600/mo LOW); platform scheduling cluster targets `how to schedule TikTok posts`.
- **Vs `content-repurposing/` cluster:** Repurposing is the production TACTIC that enables multi-channel presence. Multi-Channel mini-hub explains WHERE/HOW to be discovered. Different layer. Boundary: Multi-Channel articles don't teach repurposing workflow; they assume content exists and explain discoverability optimization.
- **Vs `discoverability/seo/`:** SEO mini-hub covers Google search. Multi-Channel covers everything-but-Google. The `on-page-seo-checklist` spoke covers image alt text for Google SEO; MC4 covers image optimization for Pinterest/visual search. Different SERPs.
- **Vs `discoverability/aeo/voice-search-optimization`:** Voice search is its own surface. Multi-Channel doesn't cover Siri/Alexa. Boundary: voice = AEO; in-platform social search = Multi-Channel.
- **Vs Backlinko / Brian Dean (YouTube SEO content):** Backlinko owns generic YouTube SEO. MC2's wedge is "small teams without TubeBuddy/vidIQ" — practical execution focus, not encyclopedic depth.
- **Vs Hootsuite / Sprout Social / Buffer (multi-channel social management):** Those tools sell scheduling/management. Multi-Channel mini-hub covers in-platform search discoverability. Different value prop.

### Ambiguous intent: NONE

All pages have unambiguous primary intent.

### Pages that may need future splitting

- **MC1 (TikTok SEO)** may eventually split into "TikTok search algorithm explained" + "TikTok hashtag strategy for search" + "TikTok cover text optimization." Hold as one consolidated guide for Phase 1.
- **MC2 (YouTube SEO)** may split into "title/description optimization" + "thumbnail/chapter optimization" + "playlist SEO." Hold as one for Phase 1.
- **MC3 (Community Discoverability)** may split into Reddit-only + Quora-only + niche forums. Hold consolidated for Phase 1.
- **MC4 (Visual Search)** may split into Pinterest-specific + Google Lens-specific. Hold consolidated for Phase 1.

### Surface-specific scope is intentional

Each MC spoke covers ONE surface (or a tightly related pair) so the article can go deep without becoming a 10,000-word everything-explainer. This is the same pattern AEO uses (A2 voice, A3 AI Overviews, A4 snippets, A5 schema — surface per article).

### Build-order constraints

- Hub publishes first (06-25)
- MC1..MC4 publish odd days 06-27 → 07-03
- All cross-cluster targets are past dates relative to MC publish dates
- No same-day-but-later same-cluster article links (each MC publishes on a distinct day)

### Deferred to later phases (NOT Phase 1)

- LinkedIn search optimization (LinkedIn's in-platform search behavior — niche, defer)
- Snapchat / Threads / Bluesky search-specific articles
- Vertical-specific multi-channel spokes (e.g., "Multi-Channel Discoverability for Restaurants")
- Per-platform deep dives (TikTok hashtag deep dive, YouTube thumbnail deep dive) — split only when traffic justifies
- Multi-channel measurement / analytics article (cross-platform analytics; defer)

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Primary keyword | Vol/Comp |
|---|---|---|---|---|---|---|
| multi-channel-discoverability-beyond-google | `discoverability/multi-channel/` | tofu | (mini-hub) | yes | social media SEO | 3,600 / LOW |
| tiktok-seo-social-search | `discoverability/multi-channel/` | mofu | MC1 | no | TikTok SEO | 3,600 / LOW |
| youtube-seo-for-small-teams | `discoverability/multi-channel/` | mofu | MC2 | no | YouTube SEO for beginners | 390 / LOW |
| community-discoverability-reddit-quora-forums | `discoverability/multi-channel/` | mofu | MC3 | no | Reddit SEO | 2,400 / LOW |
| visual-search-optimization-pinterest-google-lens | `discoverability/multi-channel/` | mofu | MC4 | no | Pinterest visual search | 1,300 / LOW |

**Total: 5 new articles** (1 hub + 4 spokes). Combined with 2 existing migrated articles, cluster has 7 articles total.

Slugs and primary keywords are locked by user approval. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 5 of Discoverability with no further architectural questions
- Each new article has an unambiguous reason to exist that doesn't duplicate the 2 migrated articles, the GEO/AEO/SEO/Brand Authority sibling mini-hubs, the `social-media-platforms/*` clusters, or the `content-repurposing/` cluster
- The 5-article schedule (06-25 → 07-03 odd days) fills slack days and dry-zone days per user cadence approval
- The mini-hub completes the 4-pillar Discoverability framework named in M1 "4 Pillars" — after this build, M1's enumeration of SEO + GEO + AEO + Social Search all map to live mini-hub articles
- Cross-cluster boundaries with platform clusters (post-mechanics vs discoverability) hold under review
- The wedge positioning ("Social Discovery for small teams beyond Google") is honored — no article reads like a Hootsuite enterprise multi-channel management piece or a Backlinko encyclopedia entry
