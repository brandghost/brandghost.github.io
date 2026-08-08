# Cluster Spec: BrandGhost Launchpad (Phase 1)

> Produced by the `hub-spoke-topic-architecture` skill. Phase 1 scope is the
> Launchpad mega hub + 6 new spokes + the audit mini-hub relocation (9 existing
> articles moved in). Vertical-application spokes (e.g., `launchpad-for-real-estate`)
> are deferred to Phase 2 — radar showed vertical keyword volume is too small
> to justify a Phase 1 slot.
>
> Architecture is **radar-informed**, not pre-locked. Keyword landscape per
> `~\.copilot\session-state\8c7dca5e-bb24-43e8-b92a-fd3840f71556\files\content-radar-launchpad-2026-06-10.md`.
> Original sketch had 6 spokes; radar added 2 (GEO tool + AI content marketing
> tool category) and deferred 1 (vertical application).

---

## Hub Definition

- **Working title:** BrandGhost Launchpad: The AI Content Marketing Tool for SEO, GEO, and Multi-Channel Discoverability
- **Folder slug:** `brandghost/launchpad/`
- **Primary intent:** Commercial investigation (secondary: informational — entity definition)
- **Target audience:** Marketers, founders, small business owners, and agency leads evaluating AI content tools. The reader has either heard of BrandGhost or is shopping the AI-content-tool category and is one click from considering BrandGhost as an answer.
- **Core problem solved:** Defines what Launchpad is, what *category* it occupies (an AI content marketing tool, not a generic AI writer), and how it integrates SEO + GEO + multi-channel publishing in one workflow. Establishes the entity for branded queries that don't yet have measurable search volume, while anchoring the cluster's non-branded spokes.
- **Canonical angle:** Launchpad is positioned at the intersection of four capabilities that competitors split across separate products: AI content generation (Jasper/Copy.ai own this), AI SEO optimization (Surfer/Frase own this), content calendar planning (CoSchedule/Hootsuite own this), and brand audit/diagnostics (Frontify/Brandfolder own this). The hub doesn't try to beat any one competitor on their head term — it owns the *integration* story.

### Validation

- Hub can rank for `BrandGhost Launchpad` (branded) and act as a category-defining page for `ai content marketing tool` queries (secondary).
- Not a listicle — synthesizes the four-capability story into a unified product narrative.
- Risk: hub-as-overview tendency. The category-definition framework requires the hub to stay at the strategic/conceptual level. The 6 spokes each cover a specific dimension.
- Branded `BrandGhost Launchpad` has 0 measurable Keyword Planner volume — hub is demand-creation, not demand-capture. It earns rank through internal links from existing high-traffic pages (`/posts/brandghost-creator-tool-2026/` has 1,792 sessions; `/posts/best-tools-multi-platform-creators/` has 21,875 impressions at position 9.29) and the new Phase 1 Discoverability and Real Estate clusters' external CTAs that currently leak to `app.brandghost.ai/launchpad`.

---

## Sub-Hub Definition (Mini-Hub, relocated)

- **Working title:** "The Complete Guide to Brand Audits" (already exists, no rewrite)
- **Folder slug:** `brandghost/launchpad/audit/`
- **Current location:** `brandghost/features/audit/` (9 articles)
- **Relocation:** `git mv` 9 files + 1 `.label` from `brandghost/features/audit/` to `brandghost/launchpad/audit/`. Filenames and slugs unchanged so URLs are preserved (Jekyll permalink is `/posts/:title/`).
- **Primary intent:** Informational (mini-hub) with established `brand audit` keyword rankings (2,900/mo LOW per radar; already-ranking pages confirmed in GSC)
- **Target audience:** Anyone evaluating their brand's discoverability and consistency. Naturally funnels into Launchpad as the execution layer that fixes what the audit diagnoses.
- **Role in cluster:** Diagnostic mini-hub. The "what's wrong" entry point before Launchpad's "here's what to do" execution.

---

## Spoke Table

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| L1 | What Is an AI Content Marketing Tool? Why It's More Than an AI Writer | Informational | Category definition; comparison of category to AI writers, AI SEO tools, content calendar tools, and brand audit tools; the integration angle that defines the category | Generic "what is AI content" content; specific tool reviews (lives in L5); Launchpad-specific product walkthrough (lives in mega hub) | Mega hub |
| L2 | Generative Engine Optimization Tools: How to Produce Content AI Engines Cite | Commercial investigation | GEO from the *tool/execution* angle — what features a GEO tool should have, what content-production capabilities matter for LLM citation, how Launchpad's structure supports GEO output | "What is GEO" theory (owned by `discoverability/geo/` mini-hub); specific competitor GEO tool reviews; AEO content | Mega hub |
| L3 | The Modern Content Creation Workflow: From URL to Multi-Channel Calendar | Informational + commercial investigation | The end-to-end workflow: URL audit → strategy → blog draft → social cascade → distribution. The 30-day-from-3-minutes claim explained as a workflow narrative | Generic content calendar templates (owned by `content-planning/content-calendar/`); per-platform scheduling mechanics; team approval workflows | Mega hub |
| L4 | Brand Voice AI: Keeping AI-Generated Content On-Brand | Informational + commercial investigation | The brand-voice problem in AI generation; how modern tools extract voice from existing content; the human-review loop; how Launchpad implements voice consistency | Generic "what is brand voice" content; brand voice exercises without AI angle; manual voice guide templates | Mega hub |
| L5 | Jasper Alternative: BrandGhost Launchpad vs Jasper for Content Marketers | Commercial investigation (BOFU) | Direct one-to-one comparison: Jasper vs Launchpad on pricing, workflow shape, output type, GEO capability, multi-channel publishing, who each is best for | Comparisons with Copy.ai, Writesonic, Writer (separate spokes if Phase 2 justifies); Jasper-only reviews without BrandGhost context | Mega hub |
| L6 | BrandGhost Launchpad Pricing: Plans, Credits, and What You Get | Transactional (BOFU) | Pricing tiers, credit system, what each plan includes, fit by user type (solo creator, small team, agency); free tier limitations | General SaaS pricing strategy content; competitor pricing comparison (lives in L5); pricing FAQ for non-Launchpad BrandGhost features | Mega hub |

**Plus:** Audit mini-hub (`brandghost/launchpad/audit/`) — 9 existing articles relocated, no new content, mini-hub article links up to mega hub.

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| Mega hub: BrandGhost Launchpad | Commercial investigation | Informational (entity definition) |
| L1: AI Content Marketing Tool category | Informational | Commercial investigation |
| L2: GEO Content Tool | Commercial investigation | Informational |
| L3: Content Creation Workflow | Informational | Commercial investigation |
| L4: Brand Voice AI | Informational | Commercial investigation |
| L5: Jasper Alternative | Commercial investigation | — |
| L6: Launchpad Pricing | Transactional | Commercial investigation |
| Audit mini-hub (existing) | Informational | — |

Funnel mix: 1 hub + 2 informational + 3 commercial investigation + 1 transactional + 1 informational (audit). No mixed-intent pages. The hub and L5 share commercial-investigation primary but at completely different scopes (entity-evaluation vs head-to-head comparison).

---

## Internal Linking Summary

### Mandatory upward links

- L1, L2, L3, L4, L5, L6 → Mega hub
- Audit mini-hub article → Mega hub (added during relocation commit)
- All 9 audit spokes already link to the audit mini-hub article — no change needed

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Mega hub → L1, L2, L3, L4, L5, L6
- Mega hub → Audit mini-hub
- Audit mini-hub → 9 audit spokes (preserved from existing)

### Justified spoke-to-spoke links

- L1 (category) ↔ L2 (GEO tool) — readers shopping the category naturally want to know about GEO capability
- L1 (category) → L5 (vs Jasper) — readers shopping the category will want a head-to-head
- L3 (workflow) → L4 (brand voice) — workflow narrative naturally raises "how does it stay on-brand?"
- L5 (vs Jasper) → L6 (pricing) — comparison readers next ask about cost
- L6 (pricing) → L5 (vs Jasper) — pricing readers next ask "is the cheaper option actually worse?"

No circular dependency chains. Each spoke is independently understandable without requiring another spoke as background.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mega hub | `_posts/discoverability/2026-06-11-brand-discoverability-complete-guide-2026.md` | Launchpad is the execution layer for the Discoverability strategy |
| Mega hub | `_posts/brandghost/why-brandghost/2026-01-21-brandghost-creator-tool-2026.md` | Existing top-traffic page; donor for funneling readers into the Launchpad entity |
| L2 (GEO tool) | `_posts/discoverability/geo/2026-06-12-generative-engine-optimization-complete-guide.md` | Tool spoke links to theory mini-hub |
| L2 (GEO tool) | `_posts/discoverability/geo/2026-06-16-how-to-get-cited-by-chatgpt-claude-perplexity.md` | Tool spoke links to tactics article |
| L3 (workflow) | `_posts/content-planning/content-calendar/2026-02-01-how-to-build-social-media-content-calendar.md` | Workflow spoke links to calendar foundation for context |
| L3 (workflow) | `_posts/artificial-intelligence/ai-content/2026-03-29-ai-for-content-creators.md` | AI content cluster as the underlying technology |
| L4 (brand voice) | `_posts/artificial-intelligence/ai-content/2026-03-29-ai-for-content-creators.md` | Brand voice connects to AI content generation theory |
| L5 (vs Jasper) | None at write time (Jasper isn't covered elsewhere in the repo) | — |
| L6 (pricing) | None at write time (no other pricing content) | — |
| Audit mini-hub | Mega hub | Relocation-time link insertion |

### Cross-cluster links (added post-publish)

- Mega hub ↔ Real Estate mega hub and other vertical clusters as they're built
- L1 (category) ↔ L1-equivalent articles in vertical clusters (e.g., when a "Launchpad for real estate" spoke exists)
- Existing high-impression page `/posts/best-tools-multi-platform-creators/` → Mega hub (donor link via blog-internal-link-pipeline)
- Existing GSC-ranking page `/posts/ai-content-calendar-claude-mcp/` → L3 (workflow) — keyword-aligned donor

### Forward-link constraints

- All Phase 1 spoke publish dates must be ≥ mega hub publish date so spokes can link up
- Audit relocation commit must happen on or before the audit mini-hub article's link-down references are added (mini-hub already exists with `hub: true`; just moves folder)
- The relocation can land in any commit, but the link pipeline run that adds Mega hub → Audit mini-hub link must happen after both exist

---

## Risk Notes

### Cannibalization risk — HIGH ATTENTION required

**Internal to the cluster:**

- **Mega hub vs L1 (AI Content Marketing Tool category):** Both touch on "what is this thing". Mitigation: Mega hub is *entity-defining* ("BrandGhost Launchpad is..."); L1 is *category-defining* ("an AI content marketing tool is..."). L1 must NOT use "Launchpad" in the title or in any of the first 3 paragraphs — Launchpad appears only as one example of the category in the second half of the article.
- **Mega hub vs L2 (GEO Tool):** Both touch on Launchpad's GEO capability. Mitigation: Mega hub mentions GEO as one of four pillars in a single section; L2 is the dedicated execution-level deep dive.
- **L3 (workflow) vs Mega hub:** Both narrate Launchpad's process. Mitigation: Mega hub describes the *product*; L3 describes the *workflow*. Mega hub: "what Launchpad is for". L3: "what the day-to-day looks like when you use it."
- **L5 (vs Jasper) vs Mega hub:** Both contain Launchpad's value prop. Mitigation: L5 is comparative; Mega hub is non-comparative. L5 doesn't reframe what Launchpad is — it assumes the reader knows and structures everything as A vs B.

**External to the cluster (existing repo content):**

- **L1 (AI Content Marketing Tool category) vs `artificial-intelligence/ai-content/`:** The AI Content cluster covers AI as a writing aid for creators. L1 is about the category of *AI content marketing tools* (a product category). Different framings, different audiences (creators vs marketers), but adjacent. Boundary: L1 stays at the *tool/product category* level; AI Content cluster stays at the *creator-using-AI* level.
- **L2 (GEO Tool) vs `discoverability/geo/` mini-hub:** Direct overlap risk on "generative engine optimization" terms. Mitigation: GEO mini-hub owns the *theory/strategy/education* ("what is GEO", "how to get cited", "how to structure content"); L2 owns the *tool/execution/product* angle ("GEO content production tools", "tool features for GEO"). The primary keyword for L2 is `generative engine optimization tool` (1,300/mo LOW); the GEO mini-hub primary is `generative engine optimization` (22,200/mo MEDIUM) — distinct queries with distinct SERP intent.
- **L3 (workflow) vs `content-planning/content-calendar/`:** Calendar cluster owns generic content calendar templates and theory. L3 owns the *AI-assisted workflow from website URL to multi-channel calendar*. Boundary: L3 must NOT use "content calendar" as primary keyword; primary is `content creation workflow` (590/mo LOW). L3 may link UP to calendar hub but does not duplicate calendar template content.
- **L5 (vs Jasper) vs `brandghost/why-brandghost/comparisons/`:** The existing comparisons cluster has 6 articles comparing BrandGhost to *social media schedulers* (Buffer, Later, Hootsuite, Sprout Social). L5 compares to an *AI content tool* (Jasper). Zero keyword overlap confirmed by repo grep (no existing article mentions Jasper, Copy.ai, Writesonic, etc.). No cannibalization risk.
- **L6 (pricing) vs `_posts/brandghost/2026-XX-brandghost-pricing-guide.md`:** A `brandghost-pricing-guide` is listed in `content-roadmap.yml` as a planned brandghost cluster article. If it's written, it covers the broader BrandGhost product pricing. L6 is Launchpad-specific. Coordinate: write L6 first under Launchpad cluster, then if the general pricing article is written later, it can link to L6 for Launchpad specifics.
- **Audit mini-hub vs nothing:** The 9 audit articles already exist and rank for their keywords (`brand audit examples`, `brand audit template`, etc.). Relocating to `brandghost/launchpad/audit/` is folder-only; URLs preserved.

### Ambiguous intent: NONE

All Phase 1 pages have unambiguous primary intent. The hub legitimately carries dual intent (commercial investigation + informational entity) because brand entity pages naturally do both. Each spoke is single-intent at the primary level.

### Pages that may need future splitting

- **L1 (AI Content Marketing Tool category)** may eventually split into "AI content marketing tool features", "AI content marketing tool comparison", "AI content marketing tool ROI" as the cluster matures. Hold as one consolidated explainer for Phase 1.
- **L5 (vs Jasper)** may extend to a comparison mini-hub (vs Copy.ai, vs Writesonic, vs Writer) if conversion data supports it. Hold as one Jasper-specific article for Phase 1.
- **L3 (workflow)** may split into separate workflow articles per vertical or per use case. Hold as one for Phase 1.

### Build-order risk

- **The audit relocation should happen in the same commit window as the Phase 1 build**, not before. Reason: the mega hub article links UP to the audit mini-hub at write time. If the audit hasn't been moved yet, the link target path is `brandghost/features/audit/...` (current location). If moved before the mega hub is written, the new path is correct from the start.
- **Recommended commit sequence:**
  1. Move audit cluster: `git mv brandghost/features/audit brandghost/launchpad/audit` (single commit, URLs preserved)
  2. Then run orchestrator for Launchpad (mega hub + 6 spokes), with the audit mini-hub link pointing at the new location
- Alternatively, run them in either order if the writer is told the destination path explicitly.

### Deferred to later phases (NOT Phase 1)

- `launchpad-for-real-estate` vertical spoke — radar showed `real estate social media ideas` is 140/mo LOW; viable but small. Defer until R6 in the real-estate cluster (`geo-for-real-estate-agents-recommended-by-chatgpt-siri`) is live and traffic-validated.
- `launchpad-vs-copyai`, `launchpad-vs-writesonic`, `launchpad-vs-writer` — defer until vs-Jasper traffic validates the comparison angle.
- `launchpad-for-coaches`, `launchpad-for-agencies`, etc. — defer to Phase 2 vertical builds.
- AI visibility / AI overview optimization spokes — defer until AEO mini-hub of Discoverability is built (currently Phase 2 of Discoverability cluster).

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Notes |
|---|---|---|---|---|---|
| brandghost-launchpad | `brandghost/launchpad/` | mofu | (mega hub) | yes | Branded primary, category secondary |
| ai-content-marketing-tool | `brandghost/launchpad/` | mofu | L1 | no | Primary: `ai content marketing tool` (1,000/mo LOW) |
| geo-content-tool | `brandghost/launchpad/` | mofu | L2 | no | Primary: `generative engine optimization tool` (1,300/mo LOW) |
| content-creation-workflow | `brandghost/launchpad/` | mofu | L3 | no | Primary: `content creation workflow` (590/mo LOW) |
| launchpad-brand-voice | `brandghost/launchpad/` | mofu | L4 | no | Primary: `brand voice ai` (110/mo LOW) |
| launchpad-vs-jasper | `brandghost/launchpad/` | bofu | L5 | no | Primary: `jasper alternative` (320/mo LOW) |
| launchpad-pricing | `brandghost/launchpad/` | bofu | L6 | no | Primary: `BrandGhost pricing` (0/mo — BOFU support, not acquisition) |

**Plus** 9 audit articles relocated from `brandghost/features/audit/` to `brandghost/launchpad/audit/` (filenames preserved, URLs preserved, no rewrites).

**Net new write work: 7 articles** (1 hub + 6 spokes).
**Plus 1 relocation: 9 audit files (folder move only).**

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 1 with no further architectural questions
- Each of the 7 new articles has an unambiguous reason to exist that doesn't duplicate an existing cluster
- The audit relocation preserves all 9 article URLs and their current `brand audit` keyword rankings
- The Launchpad cluster serves as the conversion destination for the Discoverability and Real Estate Phase 1 clusters' external CTAs
- No spoke article in this cluster reads like a thin variant of "Launchpad does X" — each occupies a distinct search-intent cell
- Cannibalization with `discoverability/geo/`, `content-planning/content-calendar/`, `artificial-intelligence/ai-content/`, and `brandghost/why-brandghost/comparisons/` is avoided by the keyword boundaries documented above
