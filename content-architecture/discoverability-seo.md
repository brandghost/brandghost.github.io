# Cluster Spec: Brand Discoverability — SEO Mini-Hub (Phase 3)

> Produced by the `hub-spoke-topic-architecture` skill. SEO is the third
> mini-hub under the existing `discoverability/` cluster (after GEO Phase 1
> and AEO Phase 2). Architecture is radar-informed; see
> `~\.copilot\session-state\8c7dca5e-bb24-43e8-b92a-fd3840f71556\files\content-radar-seo-2026-06-11.md`
> for keyword and competitor data.
>
> Companion to: `discoverability.md` (parent cluster).
> Sibling: `discoverability-aeo.md`. Knowledge Graph /
> Entity SEO topics are **deferred from Phase 1 of both clusters** per
> user arbitration — revisit in a later phase with traffic data.

---

## Hub Definition (Mini-Hub)

- **Working title:** SEO Best Practices in 2026: Modern Search Fundamentals for Small Teams
- **Folder slug:** `discoverability/seo/`
- **Primary intent:** Informational (secondary: commercial investigation)
- **Target audience:** Marketers, founders, and small in-house teams who need a current-state SEO framework without an enterprise SEO platform (Moz/Ahrefs/Semrush). The reader knows SEO matters but is confused about what still works in the AI search era.
- **Core problem solved:** Defines what modern SEO actually means in 2026 — what Google still rewards, what changed in the AI era, what to keep doing, what to stop doing, and how SEO sits alongside GEO and AEO. Acts as the practical-current-state framework that the migrated `why-ai-is-changing-the-rules-of-seo` article points to.
- **Canonical angle:** Wedge per radar — "modern SEO for small teams in the AI search era." Don't try to out-Moz Moz on the head term `SEO` (823,000/mo, too contested for BrandGhost). Don't try to be an SEO encyclopedia. Be the practical framework for teams without an enterprise SEO stack who still need to rank.

### Validation

- Can rank for `SEO best practices` (4,400/mo LOW per radar) and act as the canonical small-team SEO framework reference.
- Not a listicle — synthesizes "what still matters" across multiple SEO disciplines into one coherent framework.
- Risk: hub-as-overview tendency. Each tactical area gets a paragraph; depth lives in spokes.
- Bare `SEO` is NOT a usable primary keyword (823,000/mo LOW but incumbent-owned). Use `SEO best practices` as primary, with `SEO` / `modern SEO` / `SEO best practices 2026` as body-text synonyms.

---

## Spoke Table

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| S1 | Modern SEO Fundamentals: What Still Matters in 2026 | Informational | Core ranking signals that survived the AI era; intent matching; content quality; site fundamentals; how to think about SEO without chasing every algorithm change | AI-search-specific tactics (GEO/AEO own those); enterprise/Schema-App-level technical depth; historical AI/SEO algorithm changes (owned by migrated `why-ai-is-changing-the-rules-of-seo`) | SEO mini-hub |
| S2 | Technical SEO Basics for Small Teams | Commercial investigation | Crawlability, indexability, site speed, mobile, basic schema, sitemaps, robots.txt — small-team-scoped without enterprise tooling | Enterprise technical audits requiring Screaming Frog Pro or similar; deep schema implementation (AEO owns answer-schema; Brand Authority will own entity schema later); ongoing technical SEO ops | SEO mini-hub |
| S3 | The On-Page SEO Checklist (for People Who Don't Want to Read a 5,000-Word Guide) | Commercial investigation | Practical checklist: title tags, meta descriptions, headings, internal links, image alt, URL structure, content structure | Technical SEO basics (S2); content strategy / topic research; AI-era voice/AEO-specific tactics | SEO mini-hub |
| S4 | SEO for Small Businesses: A Practical Framework | Commercial investigation | Audience-specific SEO framework for SMBs without an in-house SEO; prioritization for resource-constrained teams; what to outsource vs DIY | Generic small-business marketing advice; Local SEO specifics (defer to Local Businesses vertical cluster); enterprise SEO ops | SEO mini-hub |
| S5 | Competitor SEO Analysis for Small Teams (Without Ahrefs) | Commercial investigation | Manual SERP review workflow; lightweight content gap analysis; reverse-engineering competitor content strategy; using free/low-cost tools; AI-assisted competitor analysis | Tool-led competitor analysis (Moz/Ahrefs/Semrush own that); enterprise backlink analysis; PR competitor tracking | SEO mini-hub |

**Total Phase 1: 1 mini-hub + 5 spokes = 6 articles.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| SEO mini-hub | Informational | Commercial investigation |
| S1: Modern SEO Fundamentals | Informational | — |
| S2: Technical SEO Basics | Commercial investigation | Informational |
| S3: On-Page SEO Checklist | Commercial investigation | Informational |
| S4: SEO for Small Businesses | Commercial investigation | Informational |
| S5: Competitor SEO Analysis | Commercial investigation | Informational |

Mix: 1 hub + 1 informational fundamentals + 4 commercial-investigation tactical. Healthy mix.

---

## Internal Linking Summary

### Mandatory upward links

- S1, S2, S3, S4, S5 → SEO mini-hub
- SEO mini-hub → Discoverability mega hub (`brand-discoverability-complete-guide-2026`, 2026-06-11 — earlier date)
- SEO mini-hub → migrated `why-ai-is-changing-the-rules-of-seo` (positioned as the historical/context article that the mini-hub builds on)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- SEO mini-hub → S1, S2, S3, S4, S5
- Discoverability mega hub → SEO mini-hub
- M1 "4 Pillars" → SEO mini-hub
- Migrated `why-ai-is-changing-the-rules-of-seo` → SEO mini-hub (the migrated article is the AI/SEO history; the mini-hub is the current-state framework)

### Justified spoke-to-spoke links

- S1 (Fundamentals) → S2 (Technical), S3 (On-Page) — fundamentals reader naturally wants tactical entry points
- S2 (Technical) ↔ S3 (On-Page) — closely related; tactical readers move between them
- S4 (SMB) → S2 (Technical), S3 (On-Page) — small-team reader wants the practical tactics
- S5 (Competitor Analysis) → S4 (SMB) — readers competing in their category often have small-team context

No circular dependency chains.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mini-hub | `_posts/discoverability/2026-06-11-brand-discoverability-complete-guide-2026.md` | Mandatory up-link |
| Mini-hub | `_posts/discoverability/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md` | Historical context article |
| Mini-hub | `_posts/discoverability/geo/2026-06-12-generative-engine-optimization-complete-guide.md` | Sibling mini-hub (GEO) |
| Mini-hub | `_posts/discoverability/aeo/2026-06-19-answer-engine-optimization-complete-guide.md` | Sibling mini-hub (AEO) — publishes BEFORE SEO Hub (06-13)? **NO — AEO Hub publishes 06-19, SEO Hub publishes 06-13.** Cross-link AEO→SEO at write time; SEO→AEO via post-publish link pipeline |
| S1 (Fundamentals) | `_posts/discoverability/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md` | Historical context |
| S2 (Technical) | `_posts/discoverability/aeo/[future date]-schema-markup-for-aeo.md` | Schema overlap, defer to post-publish link pipeline (AEO A5 publishes 06-29, AFTER S2 on 06-15) |
| S3 (On-Page) | None at write time | Content focused on practical checklist |
| S4 (SMB) | None at write time (would link to Local Businesses vertical when it exists) | — |
| S5 (Competitor Analysis) | None at write time | — |

### Forward-link constraint check

SEO Hub publishes 2026-06-13, S5 publishes 2026-06-23. All cross-cluster targets above (Discoverability mega hub 06-11, migrated SEO 06-11, GEO Hub 06-12) publish BEFORE the SEO Hub. ✓ Safe.

**AEO Hub (06-19) publishes AFTER SEO Hub (06-13) and AFTER S1 (06-15) and AFTER S2 (06-17).** SEO→AEO cross-links from articles published before 06-19 must NOT be added at write time. Link pipeline will add them post-publish.

### Cross-cluster links (added post-publish)

- SEO mini-hub ↔ AEO mini-hub (06-19) — once both live
- SEO mini-hub ↔ Multi-Channel mini-hub (Phase 4, future) — once Multi-Channel exists
- SEO mini-hub ↔ Brand Authority mini-hub (publishing 06-14 → 06-28 in parallel) — BA Hub on 06-14, AFTER SEO Hub on 06-13. SEO Hub may NOT link to BA Hub at write time. BA articles MAY link to SEO articles published before them.
- SEO mini-hub ↔ Launchpad mega hub (06-18) — once Launchpad live
- SEO mini-hub ↔ vertical clusters (Real Estate exists; future Coaches, Local Businesses)

---

## Risk Notes

### Cannibalization risk — clearly bounded per radar

**Internal to the cluster:**

- **Mini-hub vs S1 (Modern SEO Fundamentals):** Both touch on "what is modern SEO." Mitigation: Mini-hub frames the *current-state framework* (here's what SEO looks like in 2026, here are the four/five disciplines that matter); S1 is the deep dive on *ranking fundamentals* (intent matching, content quality, link signals, site fundamentals). Mini-hub introduces; S1 explains.
- **S2 (Technical) vs S3 (On-Page):** Both tactical. Mitigation: S2 is *infrastructure* (crawlability, speed, mobile, sitemaps); S3 is *page content* (titles, meta, headings, internal links). Clear functional boundary.
- **S4 (SMB) vs S1 (Fundamentals):** S4 is the audience-specific framework. Mitigation: S4 prioritizes for SMB constraints (limited time, no SEO team, budget). S1 is audience-agnostic foundational knowledge.

**External:**

- **Vs `discoverability/geo/` and `discoverability/aeo/`:** GEO and AEO own AI-specific search surfaces. SEO mini-hub stays on traditional Google search with AI-era awareness. Boundary: SEO mini-hub may mention AI/GEO/AEO in context but tactical instructions for those surfaces link out, not duplicated.
- **Vs `discoverability/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md` (migrated):** That article is AI/SEO history (RankBrain, BERT, semantic search evolution). SEO mini-hub is current-state framework. Migrated article = historical context. Mini-hub = present-day execution. Reference each other but don't duplicate.
- **Vs `brandghost/launchpad/`:** Launchpad is product positioning. SEO mini-hub is education/strategy. Launchpad's `ai-content-marketing-tool` spoke compares the category; SEO mini-hub doesn't compete on tool positioning.
- **Vs Brand Authority cluster (parallel build):** Brand Authority covers strategic-level authority signals. SEO mini-hub covers tactical execution. Entity SEO / Knowledge Graph topics deferred from both per user arbitration. SEO mini-hub may mention "entity authority matters" in body and link to Brand Authority when both are live (post-publish).
- **Vs Moz / Ahrefs / Semrush / Backlinko / Search Engine Land:** Don't try to be a comprehensive SEO encyclopedia. Stay small-team-focused. S5 explicitly frames competitor analysis "without Ahrefs" — that's the wedge.

### Ambiguous intent: NONE

All pages have clear primary intent.

### Pages that may need future splitting

- **S2 (Technical SEO Basics)** may eventually split into Core Web Vitals, Schema, Mobile, Sitemaps individual articles. Hold consolidated for Phase 1.
- **S5 (Competitor Analysis)** may extend with `content gap analysis`, `keyword gap analysis`, `competitor backlink analysis` as separate spokes. Hold as one Phase 1.
- **Knowledge Graph / Entity SEO / E-E-A-T** intentionally deferred per arbitration. Revisit Phase 2 of SEO mini-hub OR Phase 2 of Brand Authority based on traffic data.

### AI-era SEO framing

The mini-hub MUST mention AI's impact on SEO without becoming an "AI SEO" article. The migrated `why-ai-is-changing-the-rules-of-seo` covers AI/SEO history; the mini-hub covers what to actually DO in 2026 given that history. Avoid `AI SEO` as primary keyword (60,500/mo MEDIUM, semantically messy per radar).

### Build-order constraints

- Hub publishes first (06-13)
- S1..S5 publish on every-other-day odd-day cadence: 06-15, 06-17, 06-19, 06-21, 06-23
- No SEO article links to a sibling that publishes later than its own publish date
- AEO sibling cluster publishes in OVERLAPPING dates (AEO Hub 06-19); SEO→AEO links via post-publish link pipeline only
- Brand Authority cluster publishes in OVERLAPPING dates (BA Hub 06-14); SEO→BA links via post-publish link pipeline only

### Deferred to later phases (NOT Phase 1)

- Knowledge Graph / Entity SEO spokes
- E-E-A-T deep dive (defer; Backlinko/Moz dominate)
- AI SEO standalone article (cannibalization with migrated article and GEO/AEO)
- Content SEO / owned media workflow (defer; overlap with Launchpad workflow spoke)
- Per-platform SEO (defer to vertical clusters)
- Local SEO depth (defer to Local Businesses vertical cluster)
- Backlink building / link strategy (defer; Ahrefs dominates)

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Primary keyword | Vol/Comp |
|---|---|---|---|---|---|---|
| seo-best-practices | `discoverability/seo/` | tofu | (mini-hub) | yes | SEO best practices | 4,400 / LOW |
| modern-seo-fundamentals | `discoverability/seo/` | tofu | S1 | no | SEO fundamentals | 1,300 / LOW |
| technical-seo-basics-small-teams | `discoverability/seo/` | mofu | S2 | no | technical SEO | 14,800 / LOW |
| on-page-seo-checklist | `discoverability/seo/` | mofu | S3 | no | on page SEO checklist | 2,400 / LOW |
| seo-for-small-business | `discoverability/seo/` | mofu | S4 | no | SEO for small businesses | 8,100 / LOW |
| competitor-seo-analysis-small-teams | `discoverability/seo/` | mofu | S5 | no | competitor SEO analysis | 5,400 / LOW |

**Total: 6 articles** (1 hub + 5 spokes).

Slugs and primary keywords are locked by user approval. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 3 of Discoverability with no further architectural questions
- Each article has an unambiguous reason to exist that does not duplicate GEO, AEO, Launchpad, audit, the migrated AI/SEO history article, or external enterprise SEO content
- The 6-article schedule fills the 2026-06-13 → 2026-06-23 odd-day publishing window per user cadence approval
- Cross-cluster boundaries with GEO, AEO, Brand Authority, Launchpad hold under review
- The wedge positioning ("modern SEO for small teams without enterprise tooling") is honored — no article reads like a Moz/Ahrefs/Semrush enterprise-tier piece
- Knowledge Graph / Entity SEO is intentionally absent from Phase 1; mini-hub mentions entity authority briefly and links to Brand Authority cluster when both are live
