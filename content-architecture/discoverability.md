# Cluster Spec: Brand Discoverability (Phase 1)

> Produced by the `hub-spoke-topic-architecture` skill. Phase 1 scope is the
> Discoverability mega hub plus the GEO mini-hub. SEO, AEO, and Multi-Channel
> mini-hubs are deferred to later phases. The 5 existing articles in `_posts/seo/`
> are **excluded from this spec** — they will migrate into the appropriate
> discoverability sub-folders in a separate URL-preserving change.

---

## Hub Definition (Mega Hub)

- **Working title:** Brand Discoverability: How to Get Found in 2026
- **Folder slug:** `discoverability/`
- **Primary intent:** Informational
- **Target audience:** Marketers, founders, and content owners who already invest in SEO but are realizing that customers are searching across new surfaces (ChatGPT, Perplexity, AI Overviews, TikTok, voice assistants) and they don't show up there yet.
- **Core problem solved:** Reframes the discipline from "ranking on Google" to "being discoverable everywhere your customer searches." Establishes the SEO + GEO + AEO + Social-Discovery pillar model and signposts each sub-hub.
- **Canonical angle:** Category-creation. Owns the umbrella term "Brand Discoverability" — does not compete with generic "what is SEO" content. The hub is the entry point for readers asking "how do I get found in the AI era?"

### Validation

- Can stand alone as a flagship page targeting "brand discoverability" / "online discoverability" / "discoverability optimization" / "AI search optimization" queries.
- Not a listicle — the four-pillar framing requires synthesis, not enumeration.
- Risk: hub-as-overview tendency. Each pillar gets a paragraph; the temptation to expand each into a section must be resisted — that's what the sub-hubs are for.

---

## Sub-Hub Definition (Mini-Hub, owns its own spokes)

- **Working title:** Generative Engine Optimization (GEO): The Complete Guide
- **Folder slug:** `discoverability/geo/`
- **Primary intent:** Informational (secondary: commercial investigation — readers comparing GEO services / tools)
- **Target audience:** Marketers and content strategists who have heard of GEO or have noticed their brand isn't getting cited by ChatGPT/Claude/Perplexity and want to fix that.
- **Core problem solved:** Defines GEO as a distinct discipline from SEO. Explains how LLMs retrieve, evaluate, and cite source material. Gives a complete-guide-level overview that ranks for the broadest GEO queries and signposts each tactical spoke.
- **Canonical angle:** Greenfield category. "Generative Engine Optimization" / "GEO" is a brand-new term — the hub aims to be the definitive reference.

### Validation

- Can rank for "generative engine optimization", "GEO", "what is GEO", "AI search optimization", "how to rank in ChatGPT".
- Not redundant with the mega hub: the mega hub introduces the 4 pillars; the GEO hub is the deep dive into one of those pillars.
- Risk: the GEO hub article itself may try to answer every GEO question rather than signposting to spokes. The hub's job is breadth + framework, not depth.

---

## Spoke Table

### Spokes of the mega hub (Phase 1)

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| M1 | The 4 Pillars of Brand Discoverability: SEO, GEO, AEO, and Social Search | Informational | Pillar-by-pillar comparison; when each matters; how they reinforce each other | Tactical how-to for any pillar (that's the sub-hub's job); product CTAs | Mega hub |

> Note: The GEO mini-hub at `discoverability/geo/` is itself a spoke of the mega hub (mini-hub pattern). SEO/AEO/Multi-Channel sub-hubs follow in later phases as additional mega-hub spokes.

### Spokes of the GEO mini-hub (Phase 1)

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| G1 | GEO vs SEO: How AI Search Changes Content Strategy | Informational | Side-by-side comparison of ranking factors; what's identical; what's net-new; what's flipped | "What is SEO" basics; AEO-specific topics (voice, AI Overviews) | GEO mini-hub |
| G2 | How to Get Your Brand Cited by ChatGPT, Claude, and Perplexity | Commercial investigation | Concrete tactics for getting cited; LLM retrieval signals; what to publish where; structured data role | Generic SEO advice; tactics for Google AI Overviews (that's AEO) | GEO mini-hub |
| G3 | How to Structure Content for LLM Citation | Informational | Page structure, sentence patterns, claim-evidence pairing, citation-friendly formatting | Schema markup specifics (covered separately in AEO); brand voice / writing quality | GEO mini-hub |
| G4 | Measuring GEO: How to Track AI Citations of Your Brand | Commercial investigation | Tools and methods for tracking LLM citations; manual audit techniques; what success looks like | Google Analytics specifics; broader brand mentions outside AI surfaces | GEO mini-hub |

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| Mega hub: Brand Discoverability | Informational | — |
| M1: 4 Pillars of Brand Discoverability | Informational | — |
| GEO mini-hub: GEO Complete Guide | Informational | Commercial investigation |
| G1: GEO vs SEO | Informational | — |
| G2: How to Get Cited by ChatGPT | Commercial investigation | Informational |
| G3: How to Structure Content for LLM Citation | Informational | Commercial investigation |
| G4: Measuring GEO | Commercial investigation | Informational |

No mixed-intent pages. No pages dependent on another spoke to make sense.

---

## Internal Linking Summary

### Mandatory upward links

- M1 → Mega hub
- GEO mini-hub → Mega hub
- G1, G2, G3, G4 → GEO mini-hub
- G1, G2, G3, G4 → Mega hub (optional but recommended — the grand-parent link)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- Mega hub → M1, GEO mini-hub
- GEO mini-hub → G1, G2, G3, G4

### Justified spoke-to-spoke links

- G1 (GEO vs SEO) ↔ G3 (Structure for citation) — reader comparing disciplines naturally asks "okay so what do I actually do?"
- G2 (Get cited by ChatGPT) → G4 (Measuring GEO) — reader who has tactics next asks how to measure
- G3 → G2 — reader learning structure naturally asks for application tactics

No circular dependencies. Each spoke is independently understandable.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mega hub | `https://app.brandghost.ai/launchpad` | Product funnel handoff (until `brandghost/launchpad/` blog cluster exists) |
| GEO mini-hub | `_posts/brandghost/features/audit/2026-04-16-brandghost-brand-audit-tool.md` | Audit is the diagnostic that measures GEO readiness |
| G2 (Get cited by ChatGPT) | `_posts/brandghost/features/audit/2026-04-16-brandghost-brand-audit-tool.md` | The audit tool checks for AI-citation signals |
| Any GEO spoke | `_posts/artificial-intelligence/ai-content/2026-03-29-ai-for-content-creators.md` | AI content is the engine that produces GEO-optimized material |

### Cross-cluster links (added post-publish)

- Mega hub ↔ Vertical clusters (Real Estate first) once Real Estate is live
- G2 ↔ Vertical-specific GEO spokes ("GEO for real estate agents") when written

---

## Risk Notes

### Cannibalization risk: HIGH attention required

**Internal to the cluster:**

- **Mega hub vs M1 (4 Pillars):** Both could try to do "what is brand discoverability." Mitigation: Mega hub stays at the *category-defining* level ("here is a new way to think about being found"). M1 is structural: a side-by-side comparison of the 4 pillars. Mega hub does not enumerate pillar-by-pillar in depth.
- **Mega hub vs GEO mini-hub:** Both touch on GEO. Mitigation: Mega hub mentions GEO as one pillar in one paragraph and links to the mini-hub. Mini-hub goes deep.
- **G1 (GEO vs SEO) vs Mega hub:** Mega hub will inevitably compare SEO and GEO; G1 is the dedicated comparison. Mitigation: Mega hub frames the comparison at the *strategic* level (when to invest in each); G1 is *operational* (specific ranking factors, page structure differences).

**External to the cluster (existing articles):**

- **`_posts/seo/2026-06-13-from-seo-to-discoverability-reframing-your-marketing-strategy.md`** already covers "the shift from SEO to discoverability." The new mega hub must NOT duplicate this article — it should reference it (or assume it as background) and instead define the discoverability framework. Once that article migrates into `discoverability/`, it becomes an additional umbrella spoke.
- **`_posts/seo/2026-06-09-the-ultimate-guide-to-ai-content-generation-for-seo.md`** is GEO-adjacent. The new GEO mini-hub must not duplicate it. Differentiator: the existing article is about AI as a tool to write SEO content; the new GEO hub is about getting cited BY AI engines as a brand.
- **`_posts/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md`** overlaps with the mega hub and with G1. Differentiator: the existing article describes the AI-driven SEO shift in past tense / industry analysis; the new content focuses on actionable framework + tactics.

### Ambiguous intent: NONE

All Phase 1 pages have unambiguous single primary intent. The hub articles carry secondary commercial-investigation intent only because complete-guide content naturally answers some "should I do this" questions; this does not blur the primary informational intent.

### Pages that may need future splitting

- **G2 (Get cited by ChatGPT)** may eventually need per-LLM splits: "How to get cited by ChatGPT", "by Claude", "by Perplexity", "by Google Gemini". Hold as one consolidated article for Phase 1; promote to mini-hub when search demand for individual LLM queries is validated.
- **G4 (Measuring GEO)** may eventually split into "Tools" vs "Manual methods" vs "What metrics matter" — hold as one for Phase 1.

### Deferred to later phases (NOT Phase 1)

- SEO mini-hub at `discoverability/seo/` (folder created during build, no hub article yet)
- AEO mini-hub at `discoverability/aeo/`
- Multi-Channel mini-hub at `discoverability/multi-channel/`
- Migration of the 5 existing `seo/*` articles into the appropriate sub-folders
- Vertical-specific GEO spokes (e.g., `discoverability/geo/real-estate`)

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? |
|---|---|---|---|---|
| brand-discoverability-complete-guide-2026 | `discoverability/` | tofu | (mega hub) | yes |
| 4-pillars-brand-discoverability-seo-geo-aeo-social | `discoverability/` | tofu | M1 | no |
| generative-engine-optimization-complete-guide | `discoverability/geo/` | tofu | (mini-hub) | yes |
| geo-vs-seo-ai-search-changes-content-strategy | `discoverability/geo/` | tofu | G1 | no |
| how-to-get-cited-by-chatgpt-claude-perplexity | `discoverability/geo/` | mofu | G2 | no |
| how-to-structure-content-for-llm-citation | `discoverability/geo/` | mofu | G3 | no |
| measuring-geo-track-ai-citations | `discoverability/geo/` | mofu | G4 | no |

**Total: 7 articles** (2 hubs + 5 spokes).

Slugs are provisional — the orchestrator's Phase 0.5 keyword research may refine them based on validated search volume. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 1 with no further architectural questions
- Each of the 7 articles has an unambiguous reason to exist that does not depend on another future article
- Internal links are mapped so no Phase 1 article requires a future-dated article to make sense
- Once the 5 existing `seo/*` articles migrate in, they slot cleanly into the SEO / GEO / Multi-Channel sub-folders without conflicting with anything Phase 1 produces
