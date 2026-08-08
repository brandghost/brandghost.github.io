# Cluster Spec: Brand Discoverability — Brand Authority Mini-Hub (Phase 4)

> Produced by the `hub-spoke-topic-architecture` skill. Brand Authority is the
> FOUNDATIONAL LAYER beneath the four Discoverability pillars (SEO, GEO, AEO,
> Multi-Channel) — explicitly NOT a fifth pillar. Architecture is radar-informed;
> see `~\.copilot\session-state\8c7dca5e-bb24-43e8-b92a-fd3840f71556\files\content-radar-brand-authority-2026-06-11.md`.
>
> Companion to: `discoverability.md` (parent cluster).
> Sibling specs: `discoverability-aeo.md`,
> `discoverability-seo.md`. Knowledge Graph / Entity SEO topics
> are **deferred from Phase 1 of both clusters** per user arbitration — revisit
> in a later phase with traffic data.
>
> Note: this mini-hub is being built in PARALLEL with the SEO mini-hub; both
> publish across overlapping date ranges. Cross-cluster links to/from SEO are
> handled per the forward-link safety rules below.

---

## Hub Definition (Mini-Hub)

- **Working title:** Brand Authority in the AI Era: Why Search and AI Engines Recommend Some Brands
- **Folder slug:** `discoverability/brand-authority/`
- **Primary intent:** Informational (secondary: commercial investigation)
- **Target audience:** Marketers, founders, and brand owners who already understand SEO/GEO/AEO tactics but are wondering why some brands get recommended by AI engines, picked for featured snippets, and cited by ChatGPT while their brand doesn't. The reader needs a strategic understanding of brand-level authority signals beyond page-level optimization.
- **Core problem solved:** Defines Brand Authority as the strategic layer beneath SEO/GEO/AEO/Multi-Channel tactics. Explains why AI engines and search engines prefer certain brands — third-party consensus, entity clarity, trust signals, brand mentions, and reputation across the web. Acts as the FOUNDATION article that the tactical Discoverability pillars sit on.
- **Canonical angle:** Wedge per radar — "AI-era brand authority for small teams without enterprise tooling." Not Moz's Domain Authority (Moz owns the metric). Not generic brand strategy (HubSpot owns that). Specifically: how brands become AI-cite-able and search-recommended entities through practical signals a small team can build.

### Validation

- Can rank for `brand authority` (880/mo LOW per radar) and act as the canonical brand-authority-for-AI-search reference.
- Not a listicle — synthesizes mentions, citations, trust signals, entity clarity, and AI recommendation logic into one coherent framework.
- Risk: framework-drift tendency. The mini-hub must NOT rewrite the 4-pillar M1 article (just-shipped `4-pillars-brand-discoverability-seo-geo-aeo-social`); it positions Brand Authority as the layer BELOW those pillars, not a fifth peer.
- Demand is real but exact-match volume is modest. Hub article borrows mature `brand authority` demand while positioning around AI-era selection logic.

---

## Spoke Table

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| B1 | How to Build Brand Authority That AI Engines Recognize | Commercial investigation | Concrete authority-building tactics: third-party mentions, owned content depth, expertise demonstration, consistency across surfaces, entity clarity (high level), small-team executable steps | Generic brand-strategy advice (HubSpot owns that); entity SEO technical implementation (deferred to future SEO phase); link-building tactics (Ahrefs owns that); Domain Authority gaming (Moz owns that metric) | Brand Authority mini-hub |
| B2 | Brand Mentions vs Backlinks in the AI Era | Informational | Comparison of mentions and links as authority signals; why AI engines weight mentions differently than Google; unlinked mentions as evidence; co-citation; the shift from link economy to mention economy | Link-building tactics; link reclamation workflows (Ahrefs owns); manual outreach playbooks | Brand Authority mini-hub |
| B3 | The Trust Signals That Matter for AI Search in 2026 | Commercial investigation | Trust signals beyond E-E-A-T: authorship clarity, transparent ownership, review consistency, response to feedback, brand recency across surfaces, factual correctness; E-E-A-T mentioned as one framework | Generic "what is E-E-A-T?" article (Backlinko/Moz/Search Engine Land own that); YMYL deep dive; rater guidelines explainer | Brand Authority mini-hub |
| B4 | How AI Models Pick Brands to Recommend in Their Category | Commercial investigation | Category recommendation logic: why ChatGPT/Claude/Perplexity surface certain brands; third-party consensus mechanics; how AI training data and retrieval converge; tactical steps to influence the signals | Page-level LLM citation tactics (owned by GEO `how-to-get-cited-by-chatgpt-claude-perplexity`); voice search (owned by AEO); featured snippets (owned by AEO) | Brand Authority mini-hub |
| B5 | Measuring Brand Authority in the AI Era: Share of Voice, Mentions, and AI Presence | Commercial investigation | Measurement framework: brand share of voice across SERPs, mentions tracking, branded search volume, AI answer presence, sentiment; tool-light approach; what to measure when you can't afford Brandwatch | Tool-specific deep dives (Brandwatch, Mention.com); Moz/Ahrefs authority scores (proprietary); GEO citation tracking (owned by GEO `measuring-geo-track-ai-citations`) | Brand Authority mini-hub |

**Total Phase 1: 1 mini-hub + 5 spokes = 6 articles.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| Brand Authority mini-hub | Informational | Commercial investigation |
| B1: How to Build Brand Authority | Commercial investigation | Informational |
| B2: Brand Mentions vs Backlinks | Informational | — |
| B3: Trust Signals for AI Search | Commercial investigation | Informational |
| B4: How AI Models Pick Brands | Commercial investigation | Informational |
| B5: Measuring Brand Authority | Commercial investigation | Informational |

Mix: 1 hub + 1 informational comparison + 4 commercial-investigation tactical. Healthy mix.

---

## Internal Linking Summary

### Mandatory upward links

- B1, B2, B3, B4, B5 → Brand Authority mini-hub
- Brand Authority mini-hub → Discoverability mega hub (`brand-discoverability-complete-guide-2026`, 2026-06-11 — earlier date)
- Brand Authority mini-hub → M1 "4 Pillars" (2026-06-15 — published BEFORE Brand Authority Hub on 06-14? **NO — M1 publishes 06-15, BA Hub publishes 06-14.** Defer this link to post-publish pipeline.)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Brand Authority mini-hub → B1, B2, B3, B4, B5
- Discoverability mega hub → Brand Authority mini-hub
- M1 "4 Pillars" → Brand Authority mini-hub (M1 should be updated to reference the foundational layer)
- GEO mini-hub → Brand Authority mini-hub (sibling reference)
- AEO mini-hub → Brand Authority mini-hub (sibling reference)
- SEO mini-hub → Brand Authority mini-hub (sibling reference; SEO mini-hub mentions entity authority and links here)

### Justified spoke-to-spoke links

- B1 (How to Build) → B3 (Trust Signals) — building authority requires understanding trust signals
- B1 (How to Build) → B2 (Mentions vs Backlinks) — building authority requires the mention strategy
- B3 (Trust Signals) → B4 (How AI Picks Brands) — trust signals are inputs to AI recommendation
- B4 (How AI Picks Brands) → B2 (Mentions vs Backlinks) — mentions are a key input
- B5 (Measuring) → all other spokes — measurement reflects everything else

No circular dependency chains.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mini-hub | `_posts/discoverability/2026-06-11-brand-discoverability-complete-guide-2026.md` | Mandatory up-link to mega hub |
| Mini-hub | `_posts/discoverability/geo/2026-06-12-generative-engine-optimization-complete-guide.md` | GEO is one tactical pillar that Brand Authority underpins |
| Mini-hub | `_posts/brandghost/launchpad/audit/2026-04-02-the-complete-guide-to-brand-audits.md` | Audit cluster diagnoses what Brand Authority teaches to build |
| B1 (How to Build) | `_posts/brandghost/launchpad/audit/2026-04-16-brandghost-brand-audit-tool.md` | Audit tool measures brand readiness across the signals |
| B2 (Mentions vs Backlinks) | None at write time | Standalone comparison |
| B3 (Trust Signals) | `_posts/brandghost/launchpad/audit/2026-04-08-brand-health-check.md` | Trust signals are part of brand health |
| B4 (How AI Picks Brands) | `_posts/discoverability/geo/2026-06-16-how-to-get-cited-by-chatgpt-claude-perplexity.md` | LLM citation tactics complement brand-level recommendation |
| B5 (Measuring) | `_posts/discoverability/geo/2026-06-20-measuring-geo-track-ai-citations.md` | Measurement sibling: GEO measures citations, this measures broader brand authority |

### Forward-link constraint check

Brand Authority Hub publishes 2026-06-14. B5 publishes 2026-06-28.

Targets that publish BEFORE Brand Authority articles (safe to link at write time):
- Discoverability mega hub (06-11) ✓
- Migrated SEO article (06-11) ✓
- GEO Hub (06-12) ✓
- GEO G2 (06-16) — safe for B2-B5 (all publish after 06-16)
- GEO G4 / measuring-geo (06-20) — safe for B2, B3, B4, B5
- All audit articles (April 2026) ✓
- Launchpad cluster (06-18 to 06-30) — partial; check per-article date

Targets that publish AFTER Brand Authority articles (defer to link pipeline):
- M1 "4 Pillars" (06-15) — defer link from Hub (06-14); B1-B5 may link at write time
- SEO Hub (06-13) — actually PUBLISHES 1 DAY BEFORE BA Hub. SAFE to link from BA Hub.
- SEO spokes (06-15 to 06-23) — defer per-article based on date
- AEO Hub (06-19) and AEO spokes — defer per-article based on date

### Cross-cluster links (added post-publish)

- BA mini-hub ↔ M1 "4 Pillars" — M1 update needed to add foundational reference
- BA mini-hub ↔ SEO mini-hub — SEO Hub publishes 06-13, can link from BA Hub
- BA mini-hub ↔ AEO mini-hub — bilateral once link pipeline runs
- BA mini-hub ↔ Multi-Channel mini-hub (Phase 4 future)
- BA mini-hub ↔ Launchpad cluster — Launchpad is the execution path for brand-authority-aware content
- BA mini-hub ↔ vertical clusters

---

## Risk Notes

### Cannibalization risk — clearly bounded per radar

**Internal to the cluster:**

- **Mini-hub vs B1 (How to Build):** Both teach building authority. Mitigation: Mini-hub frames the *strategic understanding* (what is brand authority, why does it matter, what shapes it); B1 is the *tactical playbook* (concrete steps to build).
- **B3 (Trust Signals) vs B1 (How to Build):** Both touch on what makes brands trustworthy. Mitigation: B3 is signal-focused (what signals exist, what AI engines look for); B1 is action-focused (how to create those signals).
- **B4 (How AI Picks) vs Mini-hub:** Both touch on AI recommendation. Mitigation: Mini-hub names the topic at framework level (one paragraph); B4 is the dedicated explainer of category-recommendation mechanics.

**External:**

- **Vs `discoverability/geo/`:** GEO covers page/source citation tactics. Brand Authority covers brand-entity-level credibility. Boundary: GEO = "how does this page get cited?"; Brand Authority = "why does this brand get recommended?". B4 must NOT teach LLM citation page structure (link to GEO instead).
- **Vs `brandghost/launchpad/audit/`:** Audit diagnoses ("is your brand ready?"); Brand Authority teaches ("how do you become an authoritative brand?"). Boundary: B1 doesn't duplicate audit checklists; it teaches the strategic foundation.
- **Vs `discoverability/aeo/`:** AEO owns voice/AI Overviews/snippets/schema tactics. Brand Authority owns brand-level signals. Different layers.
- **Vs SEO mini-hub (parallel build):** SEO is tactical execution layer. Brand Authority is strategic foundation. Boundary per arbitration: Knowledge Graph / Entity SEO topics deferred from BOTH clusters Phase 1. Brand Authority mentions entity authority strategically; SEO mentions it tactically; neither writes a dedicated article in this phase.
- **Vs Moz / Ahrefs / Semrush / Backlinko / Search Engine Land / HubSpot:** Brand Authority is conceptually contested. Wedge: AI-era recommendation logic + small-team-executable signals. Don't compete with Moz on Domain Authority. Don't compete with Backlinko on E-E-A-T explainers. Don't compete with HubSpot on generic brand strategy. Stay narrow.
- **Vs `discoverability/2026-06-15-4-pillars-brand-discoverability-seo-geo-aeo-social.md` (M1):** M1 enumerates 4 pillars. Brand Authority is the foundational layer below. Boundary: Brand Authority mini-hub may reference M1 but does NOT enumerate pillars or position itself as a 5th pillar.

### Ambiguous intent: NONE

All pages have clear primary intent.

### Pages that may need future splitting

- **B1 (How to Build)** may split into "Building Authority Through Mentions", "Building Authority Through Content Depth", "Building Authority Through Owned Surfaces" as the cluster matures.
- **B3 (Trust Signals)** may extend with per-signal deep dives (authorship, transparency, sentiment specifically).
- **B5 (Measuring)** may split into "Measuring Mentions", "Measuring AI Presence", "Measuring Share of Voice" — radar shows `share of voice` carries most demand so consolidating around that for Phase 1.

### AI-era exact-match terms are mostly 0-volume

Per radar: `AI brand authority`, `brand authority for AI search`, `trust signals for AI search`, and most "why ChatGPT mentions brands" variants returned 0/mo in Keyword Planner. The cluster relies on mature `brand authority`, `unlinked brand mentions`, `trust signals`, `share of voice`, and `how to build brand authority` demand while angling the content toward AI-era recommendation. Articles must position around the AI-search angle in body copy without relying on AI-era exact-match keywords.

### Knowledge Graph / Entity SEO deferred

Per user arbitration, Entity SEO and Knowledge Graph topics are NOT in Phase 1 of either Brand Authority or SEO clusters. Both clusters mention entity authority briefly in body copy:
- Brand Authority: "Entity clarity is a key signal — see SEO mini-hub for technical implementation when that detail matters"
- SEO mini-hub: "Brand entity authority underpins SEO performance — see Brand Authority cluster"

Revisit Knowledge Graph / Entity SEO as a Phase 2 addition to whichever cluster generates more traffic to it.

### Build-order constraints

- Hub publishes first (06-14)
- B1..B5 publish on every-other-day even-day cadence: 06-16, 06-22, 06-24, 06-26, 06-28
- BA SKIPS 06-18 and 06-20 because those days are already at the 3-article cap (per the published schedule)
- The gap between B1 (06-16) and B2 (06-22) is 5 days — exceeds the minimum 1-day-in-between rule, which the user has explicitly allowed
- No BA article links to a sibling that publishes later than its own publish date

### Deferred to later phases (NOT Phase 1)

- Knowledge Graph / Entity SEO standalone spokes (deferred per arbitration)
- E-E-A-T deep dive (defer; Backlinko/Moz dominate)
- "What is brand authority" standalone article (mini-hub covers definition; weak exact demand 90/mo)
- "Become the recommended brand" standalone (folded into B4; weak exact demand)
- Per-platform brand authority (defer to vertical clusters)
- Tool-specific deep dives (Brandwatch/Mention/Brand24) — defer
- BrandGhost-specific brand authority spoke — defer to Launchpad cluster expansion if needed

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Primary keyword | Vol/Comp |
|---|---|---|---|---|---|---|
| brand-authority-ai-era | `discoverability/brand-authority/` | tofu | (mini-hub) | yes | brand authority | 880 / LOW |
| how-to-build-brand-authority | `discoverability/brand-authority/` | mofu | B1 | no | how to build brand authority | 20 / LOW |
| brand-mentions-vs-backlinks | `discoverability/brand-authority/` | mofu | B2 | no | unlinked brand mentions | 210 / LOW |
| trust-signals-ai-search | `discoverability/brand-authority/` | mofu | B3 | no | trust signals | 720 / LOW |
| how-ai-models-pick-brands-to-recommend | `discoverability/brand-authority/` | mofu | B4 | no | how to get ChatGPT to recommend your brand | 20 / MEDIUM |
| measuring-brand-authority-ai-era | `discoverability/brand-authority/` | mofu | B5 | no | share of voice | 5,400 / LOW |

**Total: 6 articles** (1 hub + 5 spokes).

Slugs and primary keywords are locked by user approval. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 4 of Discoverability with no further architectural questions
- Each article has an unambiguous reason to exist that does not duplicate GEO, AEO, SEO mini-hub, audit, M1 "4 Pillars", or external enterprise brand-authority content (Moz/Ahrefs/Semrush/Backlinko/HubSpot)
- The 6-article schedule fills the 2026-06-14 → 2026-06-28 even-day publishing window (skipping 06-18 and 06-20 due to cap) per user cadence approval
- Cross-cluster boundaries with GEO (page-level vs brand-level), audit (diagnose vs teach), SEO (tactical vs strategic), and Launchpad (product vs strategy) hold under review
- The wedge positioning ("AI-era brand authority for small teams without enterprise tooling") is honored — no article reads like a Moz proprietary-score piece or a Backlinko E-E-A-T explainer
- Knowledge Graph / Entity SEO is intentionally absent from Phase 1; mini-hub mentions entity authority briefly and links to SEO mini-hub when both are live
- M1 "4 Pillars" article gets an update post-publish to reference Brand Authority as the foundational layer (separate small commit after both clusters are committed)
