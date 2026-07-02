# Cluster Spec: Real Estate Vertical (Phase 1)

> Produced by the `hub-spoke-topic-architecture` skill. Phase 1 build of the first
> vertical cluster under Cluster Group 15 (Vertical Audience Clusters). Lives at
> top-level folder `_posts/real-estate/`, not under `small-business/`.
>
> Build sequencing: this cluster's articles must be **published on dates AFTER the
> Discoverability cluster's GEO articles** so that the cross-cluster GEO-for-real-estate
> dual-home link target exists at write time. The publish-scheduler will handle slot
> allocation accordingly.

---

## Hub Definition

- **Working title:** Social Media Marketing for Real Estate Agents: The Complete Guide for 2026
- **Folder slug:** `real-estate/`
- **Primary intent:** Informational (secondary: commercial investigation — agents evaluating tools and tactics)
- **Target audience:** Independent real estate agents, brokers, and small brokerage owners (1–10 agents) who handle their own marketing. Less applicable to mega-brokerage marketing departments.
- **Core problem solved:** A single authoritative resource for real estate agents trying to figure out *the entire social-media-and-discoverability picture* — which platforms matter, what content works, how to be found by buyers searching "best realtor in [city]" on Google AND on AI assistants, and how to do it without burning a day a week.
- **Canonical angle:** Agent-focused, not brokerage-focused. Practical, not aspirational. Acknowledges that agents have 15 minutes a day, not 4 hours, and frames every tactic around that constraint.

### Validation

- Can stand alone as a flagship page targeting "social media for real estate agents", "real estate marketing", "real estate content strategy", "Instagram for realtors".
- Not a listicle — synthesizes platform choice + content strategy + discoverability + workflow into a single coherent narrative.
- Risk: pressure to enumerate platforms or content ideas inside the hub. Hub must signpost to spokes, not duplicate them.

---

## Spoke Table

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| R1 | Local SEO for Real Estate Agents: How to Rank for "Best Realtor in [Your City]" | Commercial investigation | Google Business Profile setup; local citations; review strategy; neighborhood landing pages; competing with big brokerages on local search | National-level SEO; GEO / AI-search tactics (R6); platform-specific marketing | Real Estate Hub |
| R2 | Best Social Media Platforms for Real Estate Agents (Ranked by ROI) | Commercial investigation | Platform-by-platform breakdown for agents: Instagram, Facebook, YouTube, TikTok, LinkedIn. Time investment, audience fit, content type fit | Deep platform tactics (separate spokes per platform exist or are deferred); content ideas (R4); local SEO (R1) | Real Estate Hub |
| R3 | Real Estate Instagram Marketing: The Agent's Playbook | Informational | Profile setup, content pillars (just-listed, just-sold, neighborhood, market, education, personal), Reels strategy, hashtag strategy for real estate | Other platforms (separate spokes); Instagram general scheduling (lives in `social-media-platforms/instagram/`); paid ads | Real Estate Hub + (cross) `social-media-platforms/instagram/` hub |
| R4 | 50 Content Ideas for Real Estate Agents (With Examples) | Informational | Idea bank organized by content pillar: market updates, neighborhood spotlights, just-listed/just-sold, buyer education, seller education, personal-brand, behind-the-scenes | Platform-specific format guidance (R3 for IG, future spokes for others); content calendar mechanics (R7) | Real Estate Hub |
| R5 | AI Marketing Tools for Real Estate Agents: What Actually Works | Commercial investigation | AI use cases specific to agents: listing description generation, market report drafting, content batching, social-post variants. Tool categories rather than tool brand-by-brand reviews. Mentions Launchpad as a category fit | Generic AI marketing content (covered in `artificial-intelligence/ai-content/`); deep tool reviews | Real Estate Hub |
| R6 | GEO for Real Estate Agents: How to Get Recommended by ChatGPT and Siri | Commercial investigation | Why buyers/sellers now ask AI assistants for agent recommendations; what AI assistants look at; structured content tactics for agent discoverability in LLMs; review signals; schema for real-estate professionals | General GEO content (lives in `discoverability/geo/`); local SEO basics (R1) | Real Estate Hub + (cross) `discoverability/geo/` mini-hub |
| R7 | The Real Estate Agent's Content Calendar: A 30-Day Template | Informational | Day-by-day 30-day template; how to batch a month in 90 minutes; what to post on which days; how to repurpose listings across platforms | Generic content calendar theory (lives in `content-planning/content-calendar/`); platform mechanics | Real Estate Hub + (cross) `content-planning/content-calendar/` hub |

**Total Phase 1: 1 mega hub + 7 spokes = 8 articles.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| Real Estate mega hub | Informational | Commercial investigation |
| R1: Local SEO for Real Estate | Commercial investigation | Informational |
| R2: Best Platforms (ROI ranking) | Commercial investigation | Informational |
| R3: Instagram Playbook | Informational | Commercial investigation |
| R4: 50 Content Ideas | Informational | — |
| R5: AI Marketing Tools | Commercial investigation | Informational |
| R6: GEO for Real Estate | Commercial investigation | Informational |
| R7: 30-Day Content Calendar | Informational | — |

Skew: 4 commercial-investigation (R1, R2, R5, R6) + 3 pure informational (R3, R4, R7) + 1 mixed hub. Healthy mix — the cluster funnels naturally from informational discovery (R4, R7) into tool/platform evaluation (R2, R5) into product CTA (R5 mentions Launchpad; R6 ties to BrandGhost's GEO capability).

---

## Internal Linking Summary

### Mandatory upward links

- R1, R2, R3, R4, R5, R6, R7 → Real Estate mega hub
- R3 → also up to `social-media-platforms/instagram/` hub (dual-homed)
- R6 → also up to `discoverability/geo/` mini-hub (dual-homed; requires GEO mini-hub published first)
- R7 → also up to `content-planning/content-calendar/` hub (dual-homed)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Mega hub → R1, R2, R3, R4, R5, R6, R7

### Justified spoke-to-spoke links

- R2 (Best Platforms) → R3 (Instagram Playbook) — natural drilldown when Instagram is named as top platform
- R1 (Local SEO) → R6 (GEO for Real Estate) — discoverability complement (different surfaces)
- R6 → R1 — same complement in the other direction
- R4 (Content Ideas) → R7 (Content Calendar) — reader with ideas next asks how to schedule them
- R7 → R4 — calendar reader needs idea fuel

No circular dependencies. Each spoke is independently understandable.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mega hub | `_posts/social-media-platforms/instagram/2026-03-20-instagram-for-content-creators.md` | Instagram is a primary platform for real estate |
| Mega hub | `_posts/social-media-platforms/facebook/2026-03-21-facebook-for-content-creators.md` | Facebook (Pages + Groups + Marketplace) is critical for real estate |
| Mega hub | `_posts/social-media-platforms/youtube/2026-04-04-how-to-schedule-youtube-videos.md` | Video tours and market updates make YouTube important |
| Mega hub | `https://app.brandghost.ai/launchpad` | Product funnel handoff |
| R1 (Local SEO) | `_posts/brandghost/features/audit/2026-04-16-brandghost-brand-audit-tool.md` | Audit tool helps measure local-search readiness |
| R3 (Instagram Playbook) | `_posts/social-media-platforms/instagram/scheduling/2026-02-02-how-to-schedule-instagram-posts.md` | How-to-schedule is the platform mechanics dual-link |
| R3 (Instagram Playbook) | `_posts/social-media-platforms/instagram/timing/2026-02-03-best-time-to-post-on-instagram.md` | Timing is the natural follow-on to scheduling for agents |
| R5 (AI Tools) | `_posts/artificial-intelligence/ai-content/2026-03-29-ai-for-content-creators.md` | AI content cluster is the underlying technology |
| R6 (GEO for Real Estate) | **`_posts/discoverability/geo/[geo-mini-hub-slug].md`** | Dual-home parent — **must exist before R6 publishes** |
| R6 (GEO for Real Estate) | **`_posts/discoverability/geo/how-to-get-cited-by-chatgpt-claude-perplexity.md`** | Sibling GEO tactic article from Discoverability cluster |
| R7 (Content Calendar) | `_posts/content-planning/content-calendar/2026-02-01-how-to-build-social-media-content-calendar.md` | Dual-home parent |

### Cross-cluster links (added post-publish)

- Real Estate mega hub ↔ Small Business mega hub (Cluster 10)
- All Real Estate spokes ↔ `brandghost/launchpad/` mega hub when that exists

### Forward-link constraints

- R6 **must not** publish before the GEO mini-hub and `how-to-get-cited-by-chatgpt-claude-perplexity` from the Discoverability cluster. The publish-scheduler must enforce this ordering.
- All other Real Estate articles can publish in any internal order as long as the mega hub publishes first or simultaneously (mega-hub→spoke links are added post-publish via the link pipeline).

---

## Risk Notes

### Cannibalization risk: LOW within cluster, MEDIUM cross-cluster

**Internal to the cluster:**

- **R1 (Local SEO) vs R6 (GEO):** Both are discoverability topics. Mitigation: R1 is strictly Google + Maps + traditional local SEO. R6 is strictly AI-assistant citation. Their intro paragraphs must explicitly distinguish the two surfaces.
- **R2 (Best Platforms) vs R3 (Instagram Playbook):** R2 includes Instagram as one of N platforms; R3 is Instagram-only depth. R2 must stop at "Instagram is X out of 10 for agents because Y" and link to R3 — no playbook-level content in R2.
- **R4 (Content Ideas) vs R7 (Content Calendar):** R4 is *what to post*; R7 is *when and how to schedule it*. Separable intents.

**Cross-cluster:**

- **R3 (Instagram Playbook for Real Estate) vs `social-media-platforms/instagram/` hub:** The platform hub is platform-general. R3 is real-estate-specific. As long as R3 stays focused on the real-estate angle (content pillars unique to listings, neighborhood, market) and links *to* the platform hub for general mechanics, no overlap.
- **R6 (GEO for Real Estate) vs `discoverability/geo/` mini-hub and spokes:** The Discoverability cluster's GEO content is industry-agnostic. R6 is real-estate-specific application. Mitigation: R6 cites the GEO mini-hub for theory, then immediately pivots to "for real estate specifically, here's what matters."
- **R5 (AI Tools for Real Estate) vs `artificial-intelligence/ai-content/`:** AI-Content cluster is creator-and-marketer-agnostic. R5 names tool categories with real-estate use cases. Boundary: R5 does NOT teach how AI content generation works — it assumes that knowledge and applies it.
- **R7 (Content Calendar for Real Estate) vs `content-planning/content-calendar/`:** Content Calendar cluster owns the generic template / theory. R7 owns the real-estate-specific 30-day template. Different scope, no competition.

**External — existing scaffold:**

- `_posts/small-business/local-business/real-estate/` (empty folder) overlaps semantically with the new top-level `real-estate/`. The arch doc commit already documents this; the small-business subfolder must remain empty. Reinforced here: if any future contributor adds content to that path, it is a misroute and should be relocated to `_posts/real-estate/`.

### Ambiguous intent: NONE

All Phase 1 pages have unambiguous primary intent. The hub legitimately carries dual intent (informational + commercial investigation) because complete-guide content for a vertical naturally answers both "what should I do" and "what tools should I use" — explicitly documented.

### Pages that may need future splitting

- **R2 (Best Platforms)** may need promotion to mini-hub once per-platform real-estate spokes exist (Facebook for Real Estate, YouTube for Real Estate, TikTok for Real Estate). Hold as one consolidated comparison for Phase 1.
- **R4 (50 Content Ideas)** may eventually split into "Ideas for buyer's agents", "Ideas for listing agents", "Ideas for property managers". Hold as one for Phase 1.
- **R6 (GEO for Real Estate)** may split when there is enough demand for sub-vertical GEO articles ("GEO for commercial real estate", "GEO for property management"). Hold for Phase 1.

### Deferred to later phases (NOT Phase 1)

- Per-platform real-estate spokes (Facebook for Real Estate, YouTube for Real Estate, TikTok for Real Estate, LinkedIn for Real Estate)
- Sub-vertical clusters (commercial real estate, residential, mortgage agents, property managers, luxury real estate)
- AEO for Real Estate (after Discoverability AEO mini-hub is built)
- City-specific or region-specific spokes (geographic long-tail expansion)
- Real-estate success-story content under `brandghost/success-stories/real-estate/` (when verifiable case studies exist — no fabrication per the repo rules)

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Dual-home? |
|---|---|---|---|---|---|
| social-media-marketing-real-estate-agents-complete-guide | `real-estate/` | tofu | (mega hub) | yes | — |
| local-seo-real-estate-agents-rank-for-best-realtor-city | `real-estate/` | mofu | R1 | no | — |
| best-social-media-platforms-real-estate-agents-ranked | `real-estate/` | mofu | R2 | no | — |
| real-estate-instagram-marketing-agent-playbook | `real-estate/` | tofu | R3 | no | dual-home: `social-media-platforms/instagram/` |
| 50-content-ideas-real-estate-agents | `real-estate/` | tofu | R4 | no | — |
| ai-marketing-tools-real-estate-agents | `real-estate/` | mofu | R5 | no | — |
| geo-for-real-estate-agents-recommended-by-chatgpt-siri | `real-estate/` | mofu | R6 | no | dual-home: `discoverability/geo/` |
| real-estate-agent-content-calendar-30-day-template | `real-estate/` | tofu | R7 | no | dual-home: `content-planning/content-calendar/` |

**Total: 8 articles** (1 hub + 7 spokes, 3 of them dual-homed).

Slugs are provisional — the orchestrator's Phase 0.5 keyword research may refine them. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 1 with no further architectural questions
- Each of the 8 articles has an unambiguous reason to exist that does not depend on a future Phase article
- Dual-homed articles (R3, R6, R7) link cleanly into their secondary parent clusters without forcing keyword competition
- R6 publish date is enforced to follow the Discoverability GEO articles so the dual-home link is valid at write time
- No article appears in the small-business/local-business/real-estate scaffold path
