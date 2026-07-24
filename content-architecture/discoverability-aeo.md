# Cluster Spec: Brand Discoverability — AEO Mini-Hub (Phase 2)

> Produced by the `hub-spoke-topic-architecture` skill. AEO is the second
> mini-hub under the existing `discoverability/` cluster (after GEO, which
> was Phase 1). Architecture is radar-informed; see
> `~\.copilot\session-state\8c7dca5e-bb24-43e8-b92a-fd3840f71556\files\content-radar-aeo-2026-06-11.md`
> for the keyword and competitor data that grounds this spec.
>
> Companion to: `discoverability.md` (parent cluster). This
> spec lives standalone so the AEO sub-architecture can be reviewed and
> built independently without re-opening the broader discoverability spec.

---

## Hub Definition (Mini-Hub)

- **Working title:** Answer Engine Optimization (AEO): Show Up in Voice Search, AI Overviews, and Featured Snippets
- **Folder slug:** `discoverability/aeo/`
- **Primary intent:** Informational (secondary: commercial investigation — readers evaluating AEO services or tools)
- **Target audience:** Small teams, creators, founders, and in-house marketers who need their content to surface as answers across voice assistants, Google AI Overviews, and featured snippets — without buying an enterprise SEO/answer-engine platform.
- **Core problem solved:** Defines AEO as a discipline distinct from SEO and from GEO. Explains the answer-surface landscape (voice assistants, AI Overviews, featured snippets, structured answers) and the content patterns that make a brand answer-eligible. Signposts each tactical spoke.
- **Canonical angle:** The wedge per the radar is "AEO readiness without an enterprise SEO platform." Don't try to out-Schema-App Schema App or out-Yext Yext on enterprise tooling. The mini-hub positions AEO as something a small team or creator can execute with their existing content workflow + careful structure + minimal schema.

### Validation

- Can rank for `answer engine optimization` (8,100/mo MEDIUM per radar) and act as the canonical AEO reference for `voice search optimization`, `Google AI Overviews`, and `featured snippet optimization` adjacent queries.
- Not a listicle — the answer-surface framework requires synthesis across voice/AI Overviews/snippets/schema, not just enumeration.
- Risk: hub-as-overview tendency. Each answer surface gets a paragraph in the mini-hub; depth lives in spokes.
- Bare acronym `AEO` is **not** a usable primary keyword (165,000/mo LOW but polluted by American Eagle Outfitters retail intent per radar). Always use the full phrase `answer engine optimization` as primary, with `AEO` as a body-text synonym.

---

## Spoke Table

| Spoke # | Working title | Primary intent | Scope: includes | Scope: excludes | Rolls up to |
|---|---|---|---|---|---|
| A1 | AEO vs SEO: How They Overlap, Where They Diverge, and Why You Need Both | Informational | Side-by-side AEO vs SEO comparison; ranking-factor differences; query types each serves; when to invest in which; how they reinforce each other | GEO comparison (covered by `geo-vs-seo-ai-search-changes-content-strategy` in GEO cluster); SEO history (owned by migrated `why-ai-is-changing-the-rules-of-seo`); AEO-only tactics (A2..A5) | AEO mini-hub |
| A2 | Voice Search Optimization: How to Get Found by Siri, Alexa, and Google Assistant | Commercial investigation | How voice assistants select answers; conversational/long-tail query patterns; voice-specific content structure; on-page optimization for voice; FAQ structure; the brand-mention/listing layer | Specific competitor voice platforms (Yext, BrightLocal); deep voice-tech architecture; AI Overviews specifically (A3); featured snippets specifically (A4) | AEO mini-hub |
| A3 | How to Rank in Google AI Overviews: A Practical Optimization Guide | Commercial investigation | How Google AI Overviews work; what triggers them in SERPs; content patterns that get selected; measuring AI Overview presence; evergreen tactics (NOT news of latest AIO launches) | News/product-feature recaps; voice search (A2); schema deep-dive (A5); how to get cited by ChatGPT (GEO cluster); featured snippets (A4) | AEO mini-hub |
| A4 | Featured Snippet Optimization for AI Answers and Position Zero | Commercial investigation | Featured snippet mechanics; paragraph/list/table snippet patterns; question-and-answer formatting; how snippets relate to AI Overviews and voice answers; on-page structure for snippet capture | AI Overviews specifics (A3); voice search specifics (A2); deep schema (A5); general SEO ranking factors | AEO mini-hub |
| A5 | Schema Markup for AEO: FAQ, How-To, and Structured Data That Helps Answer Engines | Commercial investigation | FAQ schema, HowTo schema, Article schema, Q&A schema, Speakable schema; how schema helps answer engines parse and surface content; common implementation patterns; what schema does and does NOT do; validating with Google's tools | Full Schema.org reference; local business schema (defer to future local-business clusters); programmatic schema for ecommerce; generic structured-data-for-SEO content beyond AEO use | AEO mini-hub |

**Total Phase 1: 1 mini-hub + 5 spokes = 6 articles.**

---

## Intent Assignment Summary

| Page | Primary intent | Secondary intent |
|---|---|---|
| AEO mini-hub | Informational | Commercial investigation |
| A1: AEO vs SEO | Informational | — |
| A2: Voice Search Optimization | Commercial investigation | Informational |
| A3: How to Rank in AI Overviews | Commercial investigation | Informational |
| A4: Featured Snippet Optimization | Commercial investigation | Informational |
| A5: Schema Markup for AEO | Commercial investigation | Informational |

Mix: 1 hub + 1 informational comparison + 4 commercial-investigation tactical. Healthy mix — the cluster funnels from "what is this" (hub + A1) into "how do I actually do it" (A2..A5). No mixed-intent pages.

---

## Internal Linking Summary

### Mandatory upward links

- A1, A2, A3, A4, A5 → AEO mini-hub
- AEO mini-hub → Discoverability mega hub (`brand-discoverability-complete-guide-2026`, 2026-06-11 — published before mini-hub)

### Mandatory downward links (added post-publish via `blog-internal-link-pipeline`)

- AEO mini-hub → A1, A2, A3, A4, A5
- Discoverability mega hub → AEO mini-hub
- M1 ("4 Pillars of Brand Discoverability") → AEO mini-hub
- GEO mini-hub → AEO mini-hub (sibling cross-reference)

### Justified spoke-to-spoke links

Per natural reading flow:

- A1 (AEO vs SEO) → A2 (voice search) — comparison readers next want tactical entry point
- A1 (AEO vs SEO) → A3 (AI Overviews) — comparison readers want the highest-volume answer surface
- A3 (AI Overviews) ↔ A4 (featured snippets) — closely related answer surfaces; many readers conflate them
- A5 (schema) → A2 (voice) — voice optimization depends partly on structured data
- A5 (schema) → A4 (snippets) — snippet eligibility benefits from schema

No circular dependency chains. Each spoke is independently understandable.

### Cross-cluster links (mandatory at write time)

| From | To | Reason |
|---|---|---|
| Mini-hub | `_posts/discoverability/2026-06-11-brand-discoverability-complete-guide-2026.md` | Mandatory up-link to mega hub |
| Mini-hub | `_posts/discoverability/2026-06-15-4-pillars-brand-discoverability-seo-geo-aeo-social.md` | M1 names AEO as one pillar; mini-hub is the deep dive |
| Mini-hub | `_posts/discoverability/geo/2026-06-12-generative-engine-optimization-complete-guide.md` | Sibling mini-hub reference — AEO and GEO are sibling disciplines |
| A1 (AEO vs SEO) | `_posts/discoverability/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md` | Differentiator: A1 is AEO-vs-SEO specific; the migrated SEO article is broad AI/SEO history |
| A1 (AEO vs SEO) | `_posts/discoverability/geo/2026-06-14-geo-vs-seo-ai-search-changes-content-strategy.md` | Sibling comparison article — readers comparing should know AEO≠GEO |
| A2 (Voice) | `_posts/brandghost/launchpad/audit/2026-04-16-brandghost-brand-audit-tool.md` | Audit checks voice-readiness signals; AEO teaches strategy |
| A3 (AI Overviews) | `_posts/discoverability/geo/2026-06-16-how-to-get-cited-by-chatgpt-claude-perplexity.md` | Reader naturally asks "and what about ChatGPT?" — link to GEO cluster |
| A5 (schema) | `_posts/brandghost/launchpad/audit/2026-04-16-brandghost-brand-audit-tool.md` | Audit tool checks schema implementation |

### Cross-cluster links (added post-publish)

- AEO mini-hub ↔ Launchpad mega hub (`brandghost-launchpad`, 2026-06-18) — Launchpad is the execution layer that produces AEO-ready content
- AEO mini-hub ↔ Launchpad GEO/AEO product spoke (`geo-content-tool`, 2026-06-22) — both touch on AI search execution
- A3 ↔ vertical clusters when AEO-for-[vertical] spokes are written (e.g., "AEO for real estate agents" in a later phase)

### Forward-link constraints

All cross-cluster targets above are published BEFORE the AEO mini-hub's earliest spoke (06-19). Verified:
- Discoverability mega hub: 2026-06-11 ✓
- 4 Pillars: 2026-06-15 ✓
- GEO mini-hub: 2026-06-12 ✓
- Migrated SEO article: 2026-06-11 ✓
- GEO vs SEO: 2026-06-14 ✓
- How to Get Cited by ChatGPT: 2026-06-16 ✓
- Audit tool article: 2026-04-16 ✓
- Launchpad mega hub: 2026-06-18 (publishes 1 day before AEO mini-hub — safe but tight; mini-hub publishes 06-19)
- Launchpad GEO/AEO product spoke `geo-content-tool`: 2026-06-22 — **AFTER** A1 (06-21) and would be a forward link from A1. Defer to post-publish link pipeline.

---

## Risk Notes

### Cannibalization risk — clearly bounded per radar

**Internal to the cluster:**

- **Mini-hub vs A1 (AEO vs SEO):** Both touch on the relationship between AEO and SEO. Mitigation: Mini-hub frames the *category* (AEO is a discipline that handles voice + AI Overviews + snippets); A1 is the *comparison piece* (specific ranking-factor differences, when to invest in which). Mini-hub spends one paragraph on the AEO vs SEO question; A1 is the dedicated article.
- **Mini-hub vs A2/A3/A4/A5:** Mini-hub mentions each answer surface in one paragraph; spokes are the tactical depth. Mini-hub must not include "how to optimize for voice search" tactics inline — only signpost to A2.
- **A3 (AI Overviews) vs A4 (Featured Snippets):** Closely related. Mitigation: A3 is Google's AI Overviews specifically (the new answer block above the SERP); A4 is the long-running featured snippet feature. Both contribute to "position zero" but mechanically differ. A3's opening paragraph must explicitly distinguish from A4 and vice versa.

**External to the cluster:**

- **Vs `discoverability/geo/` mini-hub:** AEO ≠ GEO. **Strict boundary per radar:**
  - AEO owns: voice assistants (Siri, Alexa, Google Assistant), Google AI Overviews, featured snippets, position zero, FAQ/Schema for answer eligibility
  - GEO owns: ChatGPT, Claude, Perplexity, LLM citation behavior, source-page structure for LLM retrieval
  - AEO articles may mention ChatGPT/Claude/Perplexity only in *comparison paragraphs*. Any tactical instruction for getting cited by those systems must link to the GEO mini-hub instead of being duplicated.
- **Vs `discoverability/seo/2026-06-11-why-ai-is-changing-the-rules-of-seo.md`:** The migrated SEO article covers broad AI/SEO history (RankBrain, BERT, semantic search). AEO articles should not rehash that history. **Boundary:** AEO articles start from "answer engines now surface direct answers" and move quickly into answer formats, voice, AI Overviews, snippets, schema. One short context section may reference the SEO article for AI/SEO history; no rehashing.
- **Vs `brandghost/launchpad/audit/`:** Audit cluster diagnoses; AEO cluster teaches strategy/tactics. **Strict rule per radar: do NOT write "AEO audit checklist" in Phase 1.** AEO articles link to existing audit articles as the diagnostic counterpart; they don't replace the audit content.
- **Vs `brandghost/launchpad/geo-content-tool` (Launchpad cluster's GEO product spoke):** That spoke covers GEO from the *tool/product* angle. The AEO mini-hub and spokes cover AEO from the *strategy/education* angle. No keyword overlap (`generative engine optimization tool` vs `answer engine optimization`).
- **Vs Schema.org / Schema App / Yext / Conductor / BrightLocal (external competitors):** Don't try to be a comprehensive schema reference, a voice search local-business platform, or an enterprise AI visibility tool. Stay at the *small-team / creator practical guidance* level. A5 (schema) must be practical, not exhaustive — link to Google's schema reference docs and Schema.org for full vocabularies.
- **Vs `artificial-intelligence/ai-content/`:** AI Content cluster covers AI as a writing/ideation aid for creators. AEO cluster covers what to publish so answer engines surface it. Different framings, adjacent topics. Boundary: AEO doesn't cover AI content production; AI Content cluster doesn't cover answer-engine targeting.

### Ambiguous intent: NONE

All Phase 1 pages have unambiguous primary intent. The mini-hub legitimately carries dual intent (informational + commercial investigation) because complete-guide pages naturally answer both "what is this discipline" and "should I invest in this" questions.

### Pages that may need future splitting

- **A2 (Voice Search Optimization)** may eventually split into per-assistant articles (Siri-specific, Alexa-specific, Google Assistant-specific) if search demand emerges. Currently `how to optimize for Siri` shows 0/mo per Planner — don't split yet.
- **A3 (AI Overviews)** may split into news/feature-update recaps separate from evergreen optimization guidance. Hold as one evergreen article for Phase 1.
- **A4 (Featured Snippets)** may eventually split into per-snippet-type articles (paragraph vs list vs table snippets) at higher long-tail volume.
- **A5 (Schema)** may extend with per-schema-type spokes (HowTo schema deep dive, Article schema deep dive) when long-tail demand justifies.

### Local voice search deliberately deferred

Per radar: `local voice search` (20/mo MEDIUM) and `voice search for local business` (0/mo) are too small for Phase 1 and the SERP is dominated by BrightLocal and Yext. A2 covers voice search broadly. Local-voice-search content belongs in a future local-business vertical cluster (Cluster Group 15) where the vertical context justifies the depth, not in the AEO mini-hub.

### Build-order constraint

- Mini-hub must be the FIRST article in the cluster (per user cadence rule + per architecture rule that hub publishes first).
- All 5 spokes' allowedInternalLinks include the mini-hub — so the mini-hub must exist at the time spokes are written.
- A1 (06-21) → forward-links to Launchpad's `geo-content-tool` spoke (06-22) are NOT allowed at write time. Cross-cluster link to Launchpad GEO spoke deferred to post-publish link pipeline.

### Deferred to later phases (NOT Phase 2)

- AEO-for-[vertical] spokes (e.g., AEO for real estate agents, AEO for restaurants) — defer until vertical clusters have enough demand validation
- Local voice search deep dive — defer to local-business vertical cluster
- Per-assistant optimization (Siri-only, Alexa-only) — defer until long-tail demand emerges
- Per-snippet-type articles — defer
- Per-schema-type deep dives — defer
- AEO measurement / tracking — could justify a future spoke once Phase 1 traffic emerges

---

## Phase 1 Deliverable Summary

| Slug (provisional) | Folder | Funnel | Spoke # | hub: true? | Primary keyword | Vol/Comp |
|---|---|---|---|---|---|---|
| answer-engine-optimization-complete-guide | `discoverability/aeo/` | tofu | (mini-hub) | yes | answer engine optimization | 8,100 / MEDIUM |
| aeo-vs-seo | `discoverability/aeo/` | tofu | A1 | no | AEO SEO | 4,400 / MEDIUM |
| voice-search-optimization | `discoverability/aeo/` | mofu | A2 | no | voice search optimization | 2,900 / LOW |
| how-to-rank-in-ai-overviews | `discoverability/aeo/` | mofu | A3 | no | how to rank in AI overviews | 880 / LOW |
| featured-snippet-optimization-ai-answers | `discoverability/aeo/` | mofu | A4 | no | featured snippet optimization | 260 / LOW |
| schema-markup-for-aeo | `discoverability/aeo/` | mofu | A5 | no | FAQ schema | 6,600 / LOW |

**Total: 6 articles** (1 hub + 5 spokes).

Slugs and primary keywords are locked by user approval. Folder paths and intent assignments are locked.

---

## Success Criteria for This Spec

This spec is successful if:
- A writer can begin Phase 2 of Discoverability with no further architectural questions
- Each of the 6 articles has an unambiguous reason to exist that does not duplicate the GEO mini-hub, the audit cluster, the migrated SEO article, the Launchpad cluster, or external enterprise tooling content
- The 6-article schedule fills the 2026-06-19 → 2026-06-29 odd-day publishing window exactly (06-29 is the gap the user wants filled)
- Cross-cluster boundaries with GEO, audit, SEO migrated article, and Launchpad GEO product spoke hold under review
- The wedge positioning ("AEO for small teams without enterprise tooling") is honored in every article — no article reads like a Conductor or Yext enterprise-tier explainer
