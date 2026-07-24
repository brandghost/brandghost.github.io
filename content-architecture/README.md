# BrandGhost Blog — Content Architecture Framework

> **Files in this folder:**
> - `README.md` (this file) — the master architecture framework. Cluster Groups 1–15 defined here. Strategic, durable, doesn't change with individual builds.
> - `<cluster>.md` (e.g. `discoverability.md`, `real-estate.md`, `launchpad.md`, `discoverability-aeo.md`, `discoverability-seo.md`, `discoverability-brand-authority.md`) — per-cluster build specs produced by the `hub-spoke-topic-architecture` skill. Detailed spoke tables, primary keywords, intent assignment, internal-link maps, cannibalization boundaries, deferred items. Committed when a cluster is built; updated when its architecture evolves.
>
> **Relationship:** This README defines the framework (what clusters exist and why). Sibling `<cluster>.md` files define the detailed build for each. Both are in the same folder so the architecture is colocated.

---

## Purpose of This Document

This document defines the **structural DNA** of the BrandGhost blog — how content is organized, how pages relate to each other, and how to reason about what to build next. It is intentionally free of keyword volume data, traffic metrics, or competitive analysis. Those inputs inform *which* topics to prioritize, but this framework governs *how* topics are organized regardless of when they are built.

Use this document as a reference when:
- Briefing an LLM to generate new articles within an existing cluster
- Deciding where a new article belongs in the architecture
- Planning a new cluster from scratch
- Establishing internal linking for any new or edited post

Per-cluster build details (spoke lists, primary keywords, publish schedules, cannibalization boundaries for specific phases) live in sibling `<cluster>.md` files in this same folder.

---

## Core Concept: Hub-and-Spoke with Mini-Hubs

### Hub

A **hub** is a broad, high-level page that:
- Introduces a topic category and orients the reader
- Links down to every spoke article it owns
- Receives links back up from all of its spokes
- Does not need to cover each spoke's topic in depth — it summarizes and delegates

**Hub placement rule:** A hub article must live **directly in the folder it anchors**. A hub at `_posts/foo/bar.md` anchors the `foo/` cluster — not any parent or child folder. A folder requires a hub if it contains ≥3 direct `.md` article files. One hub per folder maximum; two or more is a violation.

### Spoke

A **spoke** is a focused, specific article that:
- Covers exactly one narrow slice of its parent hub's topic
- Links up to its parent hub (mandatory)
- May cross-link to sibling spokes when contextually relevant

### Mini-Hub

A **mini-hub** is a spoke that also has its own children. It simultaneously:
- Links **up** to its parent hub (acting as a spoke)
- Links **down** to its own child spokes (acting as a hub)

Mini-hubs arise naturally when a spoke topic has a second dimension worth expanding. The rule of thumb: if a spoke can be split into 3+ distinct sub-topics that each warrant a standalone article, promote it to a mini-hub.

**Example:** "Best Time to Post on Twitter" is a spoke of the Twitter Hub — but it also owns 7 day-of-week sub-spokes. It is simultaneously a spoke and a hub.

### Mega Hub (Cluster Entry Point)

A **mega hub** is the top-level hub for an entire cluster group. It:
- Introduces the full topic area at the highest level
- Links to all L1 hubs or top-level spokes within its cluster
- Is the page that earns authority for the broadest version of the topic

Not every cluster needs a mega hub immediately. Spokes and L1 hubs can exist and interlink before a mega hub is built.

---

## Architecture Overview

The blog is organized into **independent cluster groups**. Each cluster group is a self-contained hub-and-spoke structure with its own mega hub at the top. Cluster groups are **not nested under a single root** — they sit adjacent to each other and cross-link where topics overlap.

```
TOPIC clusters                               AUDIENCE clusters                PRODUCT cluster
─────────────────────────────────────        ─────────────────────────        ────────────────
[ Platform Scheduling ]                      [ Brand Discoverability ]        [ BrandGhost ]
[ Content Calendar ]                              ↕                                ↕
[ AI Scheduling / MCP ]            ↔         [ Vertical: Real Estate ]    ↔   [ Launchpad ]
[ AI Content Creation ]                      [ Vertical: Coaches ]            [ Audit ]
[ Analytics ]                                [ Vertical: ... ]
[ Content Repurposing ]                      [ Small Business (cross-vertical) ]
[ Growth Strategy ]                          [ Personal Branding ]
[ Multi-Platform Scheduling ]                [ Content Creators ]
```

Each cluster group is an independent entry point for a reader. Three cluster *kinds* coexist:

- **Topic clusters** — organized around a tactic, mechanic, or workflow (how to do X). TOFU-heavy.
- **Audience clusters** — organized around who the reader is (vertical / industry / role). Dual-home topic spokes to make them findable by readers entering the site through audience lens.
- **Product cluster** — BrandGhost-specific surfaces (Launchpad, Audit, features). MOFU/BOFU only.

Cross-links between clusters are explicit and documented per cluster below.

---

## The Grid Model: How to Multiply Out a Cluster

Some cluster groups are one-dimensional: a hub with a flat list of spokes. Others are two-dimensional: the spokes can be organized along **two axes**, producing a grid where every cell is a potential article.

**When to use a grid:** When you have two independent dimensions where any combination of (dimension A value) × (dimension B value) produces a distinct, valid article topic.

**How to read a grid:**
- Rows = one dimension (e.g., platform)
- Columns = another dimension (e.g., topic type)
- Each cell = one spoke article
- Each row = one L1 hub page that owns all cells in that row

**How to multiply out:** Given N rows and M columns, the full grid produces up to N × M spoke articles plus N hub pages. In practice not every cell will have enough content to justify a standalone article — leave cells empty until there is enough substance to write a quality page.

**The grid does not need to be complete.** Publish high-value cells first. The hub page can list cells as "coming soon" or simply omit them until they exist.

---

## How to Use This Framework with an LLM

When briefing an LLM to generate content within this architecture, provide:

1. **Which cluster group** the article belongs to (by name and number)
2. **Its position in the hierarchy** — is it a mega hub, L1 hub, L2 spoke, mini-hub, or L3 sub-spoke?
3. **Its grid coordinates** if applicable — (Platform row, Topic Type column)
4. **Which pages it must link up to** — parent hub(s)
5. **Which pages it may link down to or across to** — sibling spokes, cross-cluster hubs

Example brief:
> "Write a spoke article for Cluster 1 (Platform Scheduling), Instagram row, 'Best Time to Post' column. This article is a mini-hub: it must link up to the Instagram Hub, and it must link down to the 7 day-of-week sub-spokes listed in the architecture doc. Follow the mini-hub pattern from the framework."

---

## Intent Stratification

Every article on this blog serves a reader at one of three funnel stages. The funnel stage is encoded in the `funnel_stage` frontmatter field and determines content tone, CTA strategy, and related-post filtering.

### The three stages

| Stage | Value | Reader state | Content tone | CTA |
|---|---|---|---|---|
| Top of Funnel | `tofu` | Discovering the topic for the first time | Educational, no sales pressure | "Learn more", "Explore our guide" |
| Middle of Funnel | `mofu` | Aware of the problem, evaluating solutions | Comparative, solution-focused | "See how BrandGhost compares", "Try free" |
| Bottom of Funnel | `bofu` | Ready to act, evaluating BrandGhost specifically | Direct, feature-focused | "Start free trial", "See pricing" |

### How intent maps to the hierarchy

**Tier position sets the default intent:**

| Tier | Default intent | Rationale |
|---|---|---|
| Mega-hub | `tofu` | Broadest entry point — reader is oriented, not yet evaluating tools |
| L1 hub | `tofu` | Complete guide for a platform — still informational |
| L2 mini-hub | `tofu` or `mofu` | Depends on topic column (see below) |
| Spoke | Inherits from its topic column | Column type is the decisive factor |
| Sub-spoke (day-of-week, content format) | `tofu` | Highly specific how-to — pure information |

**Topic column type determines intent for spokes:**

| Column type | Intent | Examples |
|---|---|---|
| How to Schedule | `tofu` | How to schedule Twitter posts, schedule Instagram Reels |
| Best Time to Post | `tofu` | Best time to post on TikTok, best day to post on Instagram |
| Content Calendar | `tofu` | Twitter content calendar template, LinkedIn content calendar |
| Analytics | `tofu` or `mofu` | Platform analytics guide = TOFU; best analytics tools = MOFU |
| Free Scheduling | `mofu` | Schedule Pinterest pins free — reader is solution-aware, price-conscious |
| Best [Scheduler] | `mofu` | Best Twitter scheduler — reader is comparing tools |
| vs / Comparison | `mofu` | Twitter vs Bluesky scheduling — reader is evaluating options |
| Automation | `mofu` | Twitter automation — reader knows they want a tool |
| For Business | `mofu` | Instagram for business scheduling — audience-qualified, higher intent |
| BrandGhost-specific | `bofu` | BrandGhost review, BrandGhost pricing, BrandGhost features |

**Rule: BOFU content never lives under a platform cluster.** BOFU articles belong exclusively in the `BrandGhost` category. A platform cluster may link to a BOFU article but never parents it.

### Encoding intent in frontmatter

Every post must include:
```yaml
funnel_stage: tofu   # tofu | mofu | bofu
cluster_id: twitter  # id from cluster-map.yml
```

If an article is dual-homed (appears as a spoke in two clusters), also add:
```yaml
secondary_cluster_id: analytics
```

---

## Cannibalization Avoidance

Two articles cannibalize each other when they **target the same primary keyword intent at the same funnel stage** and would each fully answer the same reader's query. One article should not exist.

Dual-homing is NOT cannibalization — it is one article, two inbound navigation paths.

### The cannibalization test

Before writing a new article, ask: *"If I deleted one of these two articles, would the remaining one fully cover the same search query?"*

- Yes → Cannibalization. Merge or delete, do not write a second article.
- No → Safe. The articles serve different queries, different audiences, or different funnel stages.

### The cluster registry check

The cluster-map.yml is the canonical registry of all existing and planned content. **Before generating a new article slug, search cluster-map.yml for any existing spoke with the same or equivalent slug pattern.**

Common false-duplicate patterns:
- `best-twitter-scheduler` vs `what-to-look-for-twitter-scheduler` → Different intent (MOFU evaluation vs TOFU education). Safe.
- `twitter-analytics-scheduling` vs `twitter-x-analytics-guide-creators` → Different angle (scheduling informed by analytics vs analytics as a standalone topic). Safe.
- `twitter-automation` vs `twitter-automation-tools` → Equivalent intent. Cannibalization risk. Do not write the second.

### Cross-cluster query distinction

When adding a cross-cluster hub article (e.g., `social-media-analytics-guide` as the analytics mega-hub), ensure it targets a distinct query from any L1 hub beneath it.

- Analytics mega-hub: targets "social media analytics guide" (cross-platform overview)
- Platform analytics spokes: target "Twitter analytics guide", "Instagram analytics guide" (platform-specific)
- These do NOT cannibalize — different query, different scope.

A cross-cluster hub targets the **broadest version** of the query. L1 hubs and spokes target narrower, platform-specific or audience-specific variants.

---

### Cluster Boundary Ownership

Some clusters have overlapping subject matter but different intent. The table below encodes which cluster **owns** a given query pattern. Owning a pattern means only that cluster may write articles primarily targeting it — other clusters may reference the topic but must not try to rank for it.

**The cardinal rule:** If the primary keyword contains a platform name and is tool-agnostic → `social-media-platforms/`. If the primary keyword is BrandGhost-specific (product, feature, brand name) → `brandghost/`.

| Primary keyword pattern | Owner cluster | All other clusters: FORBIDDEN |
|---|---|---|
| "how to schedule [platform] posts" | `social-media-platforms/[platform]/scheduling` | Do not write this from `brandghost/features/` |
| "best time to post on [platform]" | `social-media-platforms/[platform]/timing` | Do not write this from `brandghost/features/` |
| "[platform] automation" | `social-media-platforms/[platform]/scheduling` | Do not write this from `brandghost/features/` |
| "[platform] for business scheduling" | `social-media-platforms/[platform]/` | Do not write this from `brandghost/features/` |
| "[platform] analytics guide" | `social-media-platforms/[platform]/analytics` | Do not write this from `brandghost/features/` |
| "cross-post across platforms" (generic) | `social-media-platforms/cross-posting/` | Do not write this from `brandghost/features/` |
| "schedule posts with BrandGhost" | `brandghost/features/scheduling/` | Do not write this from `social-media-platforms/` |
| "BrandGhost for [platform]" | `brandghost/features/scheduling/` | Do not write this from `social-media-platforms/` |
| "topic streams" (any variant) | `brandghost/features/topic-streams/` | All other clusters |
| "first comment scheduling / auto first comment" | `brandghost/features/first-comments/` | All other clusters |
| "unified social media inbox/feed" | `brandghost/features/unified-feed/` | All other clusters |
| "AI remix social media posts" | `brandghost/features/ai-content/` | All other clusters |
| "[tool] alternative" / "BrandGhost vs [tool]" | `brandghost/why-brandghost/comparisons/` | Do not write in `creator-tools/` unless it is a generic roundup with no BrandGhost promotion |
| "what is BrandGhost" / "BrandGhost review" | `brandghost/` root or `brandghost/why-brandghost/` | All other clusters |
| "hootsuite alternative" / "buffer alternative" | `brandghost/why-brandghost/comparisons/` | Do not write in `creator-tools/` |
| "brand discoverability" / "online discoverability" / "discoverability optimization" | `discoverability/` mega hub | All other clusters |
| "generative engine optimization" / "GEO" / "rank in ChatGPT" / "get cited by AI" / "AI search optimization" | `discoverability/geo/` | All other clusters — including `seo/` |
| "answer engine optimization" / "AEO" / "voice search optimization" / "Google AI Overviews" | `discoverability/aeo/` | All other clusters |
| "SEO best practices" / "modern SEO" / "AI-era SEO" | `discoverability/seo/` | Do not write generic SEO content from any other cluster |
| "social search optimization" / "TikTok SEO" / "YouTube SEO" | `discoverability/multi-channel/` | All other clusters |
| "BrandGhost Launchpad" / "what is launchpad" | `brandghost/launchpad/` | All other clusters |
| "brand audit" / "brand audit tool" / "social media brand audit" | `brandghost/launchpad/audit/` (currently `brandghost/features/audit/` pending move) | All other clusters |
| "social media for real estate agents" / "real estate marketing" / "Instagram for real estate" | `real-estate/` | Do not write from `small-business/local-business/real-estate/` |
| "social media for [vertical]" where vertical has its own top-level cluster | The vertical's top-level cluster (e.g., `coaches/`, `agencies/`, `saas/`) | Do not nest under `small-business/` |

#### The funnel flow between `social-media-platforms/` and `brandghost/`

These clusters are NOT competing — they are sequential stages of the same funnel:

```
Reader searches "how to schedule Instagram posts"
  → social-media-platforms/instagram/scheduling/   [TOFU — tool-agnostic education]
      → article recommends BrandGhost, links to:
          → brandghost/features/scheduling/         [MOFU — product-specific]
              → article links to:
                  → brandghost/why-brandghost/comparisons/  [BOFU — conversion]
```

**`social-media-platforms/` articles should mention and link to BrandGhost as a recommended tool.** `brandghost/features/` articles should never try to re-answer the "how to schedule X" question — they answer "why use BrandGhost to do it."

#### Duplicate detection before writing

Before writing any `brandghost/features/scheduling/[platform]` article, confirm:
1. There is already a `social-media-platforms/[platform]/scheduling/` article covering the "how to" angle
2. The new BrandGhost article targets "BrandGhost + [platform]" as primary keyword, NOT "how to schedule [platform] posts"
3. No existing `brandghost/features/` article already covers the same platform + BrandGhost angle

---

## The Hub Relationship Model

A hub is **not an intrinsic property of an article** — it is a relationship. The same article can be:
- A **hub** to the articles that link up to it
- A **spoke** to a higher-level hub above it
- An **entry point** for readers arriving from a different cluster

The term "inverted hub" describes a hub that provides an **alternative navigation path** into articles that have another primary parent. It is a relationship property, not a content type.

### Example: the analytics cluster as an inverted hub

`twitter-x-analytics-guide-creators` has two valid parents:
1. **Primary parent:** Twitter L1 hub → it lives as a spoke of the Twitter platform cluster
2. **Secondary parent:** Social Media Analytics mega-hub → it is also a spoke of the analytics cluster

The analytics mega-hub is "inverted" relative to the platform cluster — it cuts horizontally across all platform analytics articles. Both are valid relationships. One article, two inbound paths.

### When an inverted hub generates independent content

An inverted hub is most valuable when it generates articles that **cannot live under any single platform hub** — cross-platform content serving readers who enter the site via a goal or role rather than a platform:

```
Social Media Analytics (hub)
  ├── Platform analytics guides      ← dual-homed with platform hubs
  ├── How to track social media ROI  ← UNIQUE to analytics — no platform home
  ├── Best analytics tools           ← UNIQUE to analytics — cross-platform MOFU
  └── Social media reporting templates ← UNIQUE to analytics — no platform home
```

The cross-platform articles are what justify the inverted hub's existence. Without them, the hub is just a navigation layer.

### Preventing false inversion

A cluster should not be called an "inverted hub" if it only contains dual-homed articles from another cluster. It must generate independent content worth indexing on its own. Minimum threshold: **at least 3 articles unique to the inverted hub** before it earns a standalone hub page.

---

## Content Scaling Playbook

Every new article should expand the site along one of four defined axes. Do not invent articles by brainstorming. Expand along an axis from a known gap.

### Axis 1 — Platform axis

Add a new platform row. Each new platform multiplies the full set of topic columns:
- New platform + all TOFU columns = ~8–12 articles immediately
- New platform feeds into the existing "Best Time to Post" cross-platform aggregate hub
- YouTube Shorts, Snapchat, BeReal, Reddit are next candidates

### Axis 2 — Topic-column axis

Add a new mini-hub type to every existing platform. Each new column multiplies by the number of platform rows:
- "Scheduling Tools" mini-hub per platform = 10 platforms × ~5 articles = ~50 new articles
- "For Business" mini-hub per platform = 10 × ~5 = ~50 new articles
- "Content Calendar" (already exists as a flat cluster) → promote to mini-hub per platform

### Axis 3 — Audience-segment axis

Build a cross-platform inverted hub for a specific reader role. Each new audience hub generates:
- A mega-hub article targeting the broadest version of the role's query
- Cross-platform how-to articles unique to that role
- Audience-specific versions of platform articles (dual-homed)

Current planned audience hubs: **Social Media Analytics**, **Small Business**, **Brand Discoverability** (Cluster 14), and the **Vertical Audience Clusters** under Cluster Group 15. The 10 verticals from the BrandGhost marketing site (`/use-cases`) are: Real Estate (Phase 1 build), Coaches & Consultants, Marketing Agencies, E-commerce & DTC, SaaS & Tech, Local Businesses, Professional Services, Education & Training, Nonprofits & Churches, and Monetized Creators (covered by the existing `content-creators/` cluster).

### Axis 4 — Depth axis

Promote an existing spoke to a mini-hub when it can support 3+ sub-spokes. Depth expansion does not add audience breadth but increases long-tail coverage and topical authority:
- `best-time-to-post-on-tiktok` → promoted to mini-hub with 7 day-of-week sub-spokes (done)
- `how-to-schedule-instagram-posts` → could promote with format sub-spokes: Reels, Stories, Carousels (done for some)
- `best-twitter-scheduler` → could promote with comparison sub-spokes (future)

### The content matrix

The platform cluster is a matrix of (Platform) × (Topic Column). Every cell is a potential article. Track completeness via the gap analysis script (`tools/scripts/architecture-gap-analysis.ps1`).

```
              Twitter  Instagram  LinkedIn  TikTok  Facebook  Pinterest  ...
              ──────────────────────────────────────────────────────────
How to Schedule  ●        ●          ●         ●        ●         ●
Best Time/Day   ●●●      ●          ●●●       ●●●      ●         ●●●
Free Scheduling  ●        ●          ●         ●        ●         ●
Best Scheduler   ●        ●          ●         ●        ●         ●      ← MOFU
vs/Comparison   ●●        -          ●         -        -         ●
For Business     ●        ●          ●         ●        ●         ●      ← MOFU
Analytics        ●        ●          ●         ●        -         ●      ← dual-homed
Automation       ●        ●          ●         ●        ●         -
Content Calendar ●        ●          ●         ●        ●         ●
Bulk Scheduling  ●        -          -         ●        -         ●
```

A `-` is a known gap. Fill gaps before starting new axes.

---

## Category Taxonomy

Post categories encode the cluster hierarchy for readers browsing by topic. The category path mirrors the cluster architecture.

### Category hierarchy rules

- **L1 (always required):** The cluster group name
- **L2 (required for platform posts):** The platform name
- **L3 (optional):** The mini-hub type, for sub-spoke articles where the extra specificity aids navigation

```yaml
# Non-platform post — L1 only
categories: [Content Calendar]

# Platform post — L1 + L2
categories: [Social Media Platforms, Twitter]

# Sub-spoke with L3 (optional, only if the mini-hub has its own category page)
categories: [Social Media Platforms, TikTok, Best Time to Post]
```

### L1 cluster group names

| L1 Category | Used for |
|---|---|
| `Social Media Platforms` | All platform-specific scheduling, timing, automation, for-business, and analytics posts |
| `Social Media Analytics` | Cross-platform analytics, analytics tools, ROI & reporting, analytics by audience |
| `Content Calendar` | Content planning, calendar templates, posting schedules |
| `AI & Automation` | MCP, AI-powered workflows, automation tools, Claude/ChatGPT integrations |
| `Content Strategy` | Repurposing, batching, pillars, general strategy |
| `Creator Tools` | Tool comparisons, writing utilities, screenshot generators, character counters |
| `Small Business` | SMB-focused cross-platform guides (note: platform-specific for-business posts go under `Social Media Platforms`; industry-vertical posts go under the relevant vertical L1) |
| `Growth & Engagement` | Audience growth, engagement strategy, algorithm guides |
| `Personal Branding` | Personal brand strategy, thought leadership, creator identity |
| `Brand Discoverability` | SEO, GEO, AEO, multi-channel discoverability strategy and tactics |
| `Real Estate` | Social media + content marketing for real estate agents, brokers, property managers |
| `BrandGhost` | Product announcements, release notes, BrandGhost-specific features, Launchpad, brand audit tool (BOFU only) |

### Platform names (exact capitalisation required)

`Twitter`, `Instagram`, `Pinterest`, `Facebook`, `Threads`, `Mastodon`, `Bluesky`, `TikTok`, `LinkedIn`, `Telegram`, `YouTube`, `Reddit`, `Discord`

### Category assignment rules (in priority order)

1. If slug contains `mcp`, `ai-content`, `automat`, `claude`, `chatgpt` → `AI & Automation`
2. If slug contains `geo`, `aeo`, `discoverability`, `generative-engine`, `answer-engine`, `voice-search`, `ai-search` → `Brand Discoverability`
3. If slug contains `seo` AND no platform in slug → `Brand Discoverability` (current `seo/` folder is part of the discoverability cluster; migration deferred but category routing already applies)
4. If slug contains `analytics`, `metrics`, `impressions`, `dashboard`, `roi`, `reporting` AND no platform in slug → `Social Media Analytics`
5. If slug contains `analytics`, `metrics`, `impressions` AND platform in slug → `Social Media Platforms` (+ platform L2); also add `secondary_cluster_id: analytics` in frontmatter
6. If slug contains `-vs-`, `best-.*-scheduler`, `comparison` → `Social Media Platforms` (+ platform L2) if platform-specific; `Creator Tools` if generic tool comparison
7. If slug contains `calendar`, `content-pillar`, `batching`, `repurpose`, `strategy` → `Content Strategy` or `Content Calendar`
8. If slug contains `screenshot`, `character-counter`, `thread-splitter` → `Creator Tools`
9. If slug contains `real-estate`, `realtor`, `broker`, `property-manager` → `Real Estate`
10. If slug contains `small-business` without a platform → `Small Business`
11. If slug contains `launchpad`, `brand-audit`, `audit-tool` (BrandGhost-specific framing) → `BrandGhost`
12. Default for platform-specific posts → `Social Media Platforms` (+ platform L2)

---

## Build Sequence Guidance

Build in this structural order (rationale is architectural, not traffic-based):

1. **Hub pages for clusters with existing spokes first** — spokes with no hub to link to are structurally broken
2. **Complete the grid for platforms that already have a hub** — fill empty cells before starting new platforms
3. **Mini-hub children (day-of-week, content format spokes)** — these require their mini-hub parent to exist first
4. **New cluster groups** — build the hub page first, then produce spokes in order of structural importance (complete the column before starting a new one)
5. **Column-level mega hubs** (e.g., "Best Time to Post on Social Media") — build last, after enough rows exist to justify the aggregator

---

## Cluster Group 1: Platform Scheduling

### What this cluster covers

How to schedule, automate, and manage posting on each major social media platform. This is the primary cluster group for BrandGhost.

### Structure

This cluster uses the **grid model**. The two dimensions are:

- **Rows (platforms):** Each platform is an L1 hub
- **Columns (topic types):** Each topic type is a spoke category within every platform

```
                    ← TOPIC TYPE COLUMNS →
                    Best    How-To   Auto-  For      Content   Analytics  Free   Bulk   vs/
                    Time    Sched    mation Business Calendar             Sched  Sched  Comp

↑  Twitter Hub      [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
P  Instagram Hub    [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
L  LinkedIn Hub     [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
A  Pinterest Hub    [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
T  Facebook Hub     [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
F  Threads Hub      [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
O  Mastodon Hub     [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
R  Bluesky Hub      [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
M  Telegram Hub     [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
S  TikTok Hub       [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
↓  YouTube Hub      [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
   Reddit Hub       [cell]  [cell]  [cell]  [cell]   [cell]    [cell]    [cell] [cell] [cell]
```

Each cell is a standalone spoke article. Each platform hub links to every cell in its row. Each cell links back to its platform hub.

### Platform Hub Examples

**Hub page:** "Twitter Scheduling: The Complete Guide"
- Links to: How to schedule Twitter posts, Best time on Twitter, Twitter automation, Twitter for business, Twitter content calendar, Twitter analytics, Twitter thread scheduling, Twitter character counter, Bulk scheduling on Twitter, Best Twitter scheduler, Free Twitter scheduling, Twitter vs Bluesky scheduling, Twitter posting strategy

**Hub page:** "Instagram Scheduling: The Complete Guide"
- Links to: How to schedule Instagram posts, Best time on Instagram, Instagram automation, Instagram for business, Instagram content calendar, Best time to post on Instagram (mini-hub), How to schedule Reels (mini-hub), How to schedule Stories, How to schedule Carousels, Free Instagram scheduling, Schedule Instagram on desktop, Instagram engagement guide

**Hub page:** "LinkedIn Scheduling: The Complete Guide"
- Links to: How to schedule LinkedIn posts, Best time on LinkedIn (mini-hub), LinkedIn automation, LinkedIn for business, LinkedIn content calendar, LinkedIn analytics, Best LinkedIn scheduler, Free LinkedIn scheduling, LinkedIn carousels, LinkedIn vs Twitter scheduling, LinkedIn for personal profiles vs company pages, LinkedIn newsletters

### Optional Cross-Platform Hub (Column-Level Hub)

Because every platform has a "Best Time to Post" spoke, an optional cross-platform hub can aggregate all of them:

**Optional mega hub:** "Best Time to Post on Social Media"
- Links to: Best time on Twitter, Best time on Instagram, Best time on LinkedIn, Best time on Pinterest, Best time on Facebook, Best time on Threads, Best time on Mastodon, Best time on Bluesky, Best time on Telegram, Best time on TikTok, Best time on YouTube, Best time on Reddit

This pattern applies to any topic type column that justifies its own aggregate hub — Automation, Analytics, and Content Calendar are other natural candidates. These column-level hubs are **optional enhancements**, not structural requirements.

### Mini-Hub Pattern 1: Best Time to Post on [Platform]

Every "Best Time to Post on [Platform]" spoke is also a mini-hub. It owns 7 day-of-week sub-spokes:

```
Twitter Hub  (L1 platform hub)
└── Best Time to Post on Twitter  (L2: spoke of Twitter Hub AND mini-hub for day spokes)
    ├── Best time to post on Twitter on Mondays
    ├── Best time to post on Twitter on Tuesdays
    ├── Best time to post on Twitter on Wednesdays
    ├── Best time to post on Twitter on Thursdays
    ├── Best time to post on Twitter on Fridays
    ├── Best time to post on Twitter on Saturdays
    └── Best time to post on Twitter on Sundays
```

This pattern applies to every platform row. Each platform's "Best Time" cell is a mini-hub for 7 day-of-week spokes.

**Why this is a mini-hub and not just more spokes of the platform hub:** The day-of-week articles are subordinate to the "Best Time" summary — a reader who lands on Monday's article needs to understand how it relates to the broader best-time picture before drilling up to the platform hub. The mini-hub is the natural intermediate step.

### Mini-Hub Pattern 2: How to Schedule [Content Format] on [Platform]

The "How to Schedule" spoke for platforms with distinct content formats also becomes a mini-hub. Each native content format on that platform gets its own sub-spoke:

```
Instagram Hub  (L1 platform hub)
└── How to Schedule Instagram Posts  (L2: spoke of Instagram Hub AND mini-hub for formats)
    ├── How to Schedule Instagram Reels
    ├── How to Schedule Instagram Stories
    └── How to Schedule Instagram Carousels

Facebook Hub  (L1 platform hub)
└── How to Schedule Facebook Posts  (L2: spoke of Facebook Hub AND mini-hub for formats)
    ├── How to Schedule Facebook Reels
    ├── How to Schedule Facebook Stories
    └── How to Schedule Facebook Groups

LinkedIn Hub  (L1 platform hub)
└── How to Schedule LinkedIn Posts  (L2: spoke of LinkedIn Hub AND mini-hub for formats)
    ├── How to Schedule LinkedIn Carousels
    ├── How to Schedule LinkedIn Articles
    ├── How to Schedule LinkedIn Newsletters
    └── How to Schedule LinkedIn Polls
```

Apply this pattern to any platform that has 3+ distinct native content formats worth separate articles. Platforms with a single uniform post type (Mastodon, Bluesky, Reddit) do not need this mini-hub.

---

## Cluster Group 2: Content Calendar & Planning

### What this cluster covers

How to plan, organize, and manage a content schedule — separate from the mechanics of scheduling on any specific platform.

### Structure

Single-level hub-and-spoke. The mega hub links to a flat list of spokes. Platform-specific calendar articles are dual-homed: they live as spokes here AND cross-link to the relevant platform hub in Cluster 1.

```
Content Calendar Hub  (mega hub)
├── How to build a social media content calendar
├── Social media content calendar templates (roundup)
├── Best content calendar tools
├── Content pillars for social media
├── Content batching for creators
├── How to plan a month of social media content
├── Build a content calendar that works
└── Platform-specific calendar templates (dual-homed with Cluster 1):
    ├── Instagram content calendar template
    ├── Twitter content calendar template
    ├── Facebook content calendar template
    ├── Threads content calendar template
    ├── Pinterest content calendar
    ├── Bluesky content calendar
    └── LinkedIn content calendar
```

---

## Cluster Group 3: MCP & AI-Powered Scheduling

### What this cluster covers

Using the Model Context Protocol (MCP) to automate social media scheduling via AI agents. This is a high-differentiation topic — it uniquely bridges BrandGhost's API capabilities with the LLM tooling ecosystem.

### Structure

Single-level hub-and-spoke. The mega hub introduces MCP as a concept for social media; spokes cover setup, use cases, comparisons, and platform-specific integrations.

```
MCP Hub  (mega hub)
├── MCP social media automation: complete guide
├── MCP for beginners: your first automated social post
├── MCP server setup with Claude Desktop
├── MCP security for social media
├── AI content calendar with Claude MCP
├── MCP vs Zapier for social media automation
├── MCP for social media agencies
└── MCP: ChatGPT vs Claude for social scheduling
```

**Cross-cluster links:** MCP Hub ↔ AI Content Creation Hub (Cluster 4), MCP Hub ↔ Multi-Platform Scheduling Hub (Cluster 8)

---

## Cluster Group 4: AI Content Creation & Brand Voice

### What this cluster covers

Using AI tools to write, ideate, and maintain an authentic brand voice for social media — separate from scheduling mechanics.

### Structure

Single-level hub-and-spoke. The mega hub introduces AI as a writing aid; spokes cover specific use cases, prompt techniques, and philosophical takes on authenticity.

```
AI Content Creation Hub  (mega hub)
├── AI ghostwriter for authentic social media content
├── How to use AI for social media without sounding like a bot
├── AI tools for brand voice and caption writing
├── AI content generation and the virtual influencer problem
├── The future of AI in social content creation
├── How to write AI prompts for social media
├── How to maintain brand voice when using AI
├── AI caption generators: how to choose one
├── When to use AI vs write from scratch
└── AI content ideas when you're stuck
```

**Cross-cluster links:** AI Content Hub ↔ MCP Hub (Cluster 3)

---

## Cluster Group 5: BrandGhost Product

### What this cluster covers

BrandGhost-specific content: product features, platform support, getting started guides, comparisons against competing tools, and creator success stories. This is the only cluster that contains BOFU content. Every article in this cluster is product-first — it assumes the reader is either already using BrandGhost or actively evaluating it.

**Intent boundary:** `social-media-platforms/` owns tool-agnostic education. `brandghost/` owns product-specific content. An article about "how to schedule Instagram posts" belongs in `social-media-platforms/`. An article about "how BrandGhost handles Instagram scheduling" belongs in `brandghost/features/`.

### Sub-cluster architecture

```
brandghost/  (root)
├── hub: "What Is BrandGhost? The Complete Guide"   ← not yet written
├── 10-tips-to-save-time                             ← general, stays at root
├── ai-philosophy                                    ← brand mission, stays at root
│
├── launchpad/  (L1 hub: "BrandGhost Launchpad: How It Works")
│   │   ← hub not yet written. Launchpad is the primary product surface
│   │     framed by the marketing site (app.brandghost.ai/launchpad).
│   │
│   ├── (planned) what is launchpad
│   ├── (planned) launchpad workflow walkthrough
│   ├── (planned) launchpad pricing and plans
│   ├── (planned) launchpad vs traditional content tools
│   │
│   └── audit/   (L2 mini-hub — current home: brandghost/features/audit/)
│         hub: "The Complete Guide to Brand Audits" (already live)
│         spokes: brand audit checklist, brand health check, personal brand audit,
│                 brand audit template, social media brand audit,
│                 brand audit examples, brandghost brand audit tool, how to do brand audit
│         PLANNED MOVE: relocate from brandghost/features/audit/ to
│                       brandghost/launchpad/audit/ once the Launchpad mega hub exists.
│                       Coordinate URL-preserving redirects at move time.
│
├── features/  (L1 hub: "BrandGhost Features: Everything You Can Do")
│   │   ← hub not yet written
│   │
│   ├── topic-streams/   ← UNIQUE FEATURE — no keyword overlap with social-media-platforms/
│   │     hub: "What Are Topic Streams? BrandGhost's Evergreen Content Rotation"
│   │     spokes: use cases by niche, best practices, content rotation strategy
│   │
│   ├── first-comments/  ← UNIQUE FEATURE — no keyword overlap
│   │     hub: "BrandGhost First Comments: Auto-Post the First Reply"
│   │     spokes: why first comments matter, platform support, examples
│   │
│   ├── unified-feed/    ← UNIQUE FEATURE — no keyword overlap
│   │     hub: "BrandGhost Unified Feed: Manage All Comments in One Place"
│   │     spokes: engagement workflows, reply strategy, inbox zero for social
│   │
│   ├── ai-content/      ← UNIQUE FEATURE — no keyword overlap
│   │     hub: "BrandGhost AI Content Tools: Generate, Remix, and Reuse"
│   │     spokes: AI post generation, content remix, templates by niche
│   │
│   ├── content-library/ ← UNIQUE FEATURE — no keyword overlap
│   │     hub: "BrandGhost Content Library: Save and Reuse Your Best Posts"
│   │     spokes: organizing content, reusing posts, template strategy
│   │
│   └── scheduling/      ← SHARED DOMAIN — strict keyword rules apply (see below)
│         hub: "Scheduling Posts with BrandGhost: All Platforms"
│         spokes: one per supported platform, always branded keyword
│         RULE: every spoke must target "BrandGhost + [platform]" as primary keyword.
│               Never target "how to schedule [platform] posts" — that is owned by
│               social-media-platforms/[platform]/scheduling/.
│
├── getting-started/  (L1 hub — not yet written)
│   hub: "Getting Started with BrandGhost: Setup Guide"
│   spokes: account connection per platform, first post walkthrough, onboarding tips
│
├── why-brandghost/  (L1 hub — existing article: brandghost-creator-tool-2026)
│   hub: "Why BrandGhost? The Case for a Creator-First Scheduling Tool"
│   │
│   └── comparisons/  (L2 mini-hub — not yet written)
│         hub: "Best Hootsuite Alternatives in 2026" or "BrandGhost vs [Top Tools]"
│         spokes: BrandGhost vs Hootsuite (exists), vs Buffer, vs Later, vs Sprout Social,
│                 vs Publer, vs native platform schedulers
│
└── success-stories/  (L1 hub — not yet written)
      │
      └── content-creators/  (L2 mini-hub — not yet written)
            hub: "How Content Creators Use BrandGhost"
            spokes: Thimo case study (exists), Monte case study (exists),
                    future creator stories (real only, no fabrication)
```

### Keyword ownership per sub-cluster

| Sub-cluster | Target keyword pattern | Example primary keywords |
|---|---|---|
| `launchpad/` | "BrandGhost Launchpad", "what is launchpad", "launchpad workflow" | Always branded — never compete with generic content marketing terms |
| `launchpad/audit/` | "brand audit", "brand audit tool", "brand audit checklist", "social media brand audit" | Owns the brand-audit keyword space (currently living at `features/audit/`). |
| `features/topic-streams/` | "topic streams", "evergreen post rotation", "content rotation scheduling" | No platform cluster overlap possible |
| `features/first-comments/` | "auto first comment", "schedule first comment social media" | No platform cluster overlap possible |
| `features/unified-feed/` | "unified social media inbox", "manage comments all platforms one place" | No platform cluster overlap possible |
| `features/ai-content/` | "AI remix posts", "AI social media content generator BrandGhost" | No platform cluster overlap possible |
| `features/content-library/` | "social media content library", "save reuse social posts" | No platform cluster overlap possible |
| `features/scheduling/[platform]` | **MUST include "BrandGhost"** — e.g., "BrandGhost for Instagram", "schedule Instagram posts with BrandGhost" | Never: "how to schedule Instagram posts" (that is social-media-platforms/) |
| `why-brandghost/comparisons/` | "[tool] alternative", "BrandGhost vs [tool]" | "hootsuite alternative", "BrandGhost vs Buffer" |
| `getting-started/` | "BrandGhost setup", "connect [platform] to BrandGhost", "BrandGhost tutorial" | Always branded |
| `success-stories/` | "BrandGhost case study", creator names | Always branded |

### Supported platforms (as of Mar 2026)

Analytics supported: Twitter/X, Instagram, Facebook, YouTube.
Posting supported: all of the above plus LinkedIn, TikTok, Pinterest, Mastodon, Bluesky, Threads, Reddit, Tumblr, Telegram.
LinkedIn/TikTok/Pinterest: **do NOT claim analytics support** — it is not yet live.

### Funnel stage rules for BrandGhost cluster

- `launchpad/` hub → `mofu` (reader is evaluating Launchpad)
- `launchpad/audit/` → `tofu` for educational audit content, `mofu`/`bofu` for product-specific audit tool content
- `features/` sub-clusters with unique features → `mofu` (reader is evaluating BrandGhost)
- `features/scheduling/[platform]` spokes → `bofu` (reader is deciding to use BrandGhost for a specific platform)
- `why-brandghost/comparisons/` → `bofu` (reader is at decision point)
- `getting-started/` → `mofu` (reader is onboarding)
- `success-stories/` → `mofu` (social proof for evaluating readers)
- Root hub ("what is BrandGhost") → `tofu` (brand discovery)

**BOFU content never lives under `social-media-platforms/`.** If a platform cluster article mentions BrandGhost pricing or conversion CTAs, it is misclassified — move it to `brandghost/`.

---

## Cluster Group 6: Creator Tools & Workflow

### What this cluster covers

Third-party tools used alongside BrandGhost — design, video editing, planning, and social media management. This cluster positions BrandGhost within a broader creator stack.

### Structure

Single-level hub-and-spoke. The roundup article at the top functions as a natural hub. Individual tool deep-dives and comparisons are spokes.

```
Creator Tools Hub  (mega hub)
├── Top tools for content creators (roundup)
├── Canva for content creators
├── CapCut for video editing
├── Descript for video and podcasting
├── Notion as a planning system for creators
├── Best social media management tools for teams
├── Best multi-platform tools for solo creators
├── BrandGhost vs Hootsuite
└── Why all-in-one tools fail creators
```

---

## Cluster Group 6: Social Media Writing Utilities

### What this cluster covers

BrandGhost's free utility tools — character counters, post screenshot generators, and thread splitters. These are high-intent, tool-specific pages with immediate utility value.

### Structure

Single-level hub-and-spoke. The mega hub is a landing page for all free tools; spokes cover each tool individually or by use case.

```
Writing Utilities Hub  (mega hub)
├── Free social media writing tools: overview
├── Best online character counter for social media
├── Twitter/X character counter and thread splitter
├── Bluesky character counter
├── Threads character counter
├── Auto-split long posts by character count
├── Tweet screenshot generator: complete guide
├── How to turn a tweet into a shareable screenshot
├── Tweet screenshot generator ideas and use cases
└── Screenshot generator vs taking screenshots manually
```

---

## Cluster Group 7: Social Media Consistency & Strategy

### What this cluster covers

The mindset, workflow, and habits side of showing up consistently on social media. Not platform-specific. Closer to creator psychology and sustainable content production than to scheduling tactics.

### Structure

Single-level hub-and-spoke. May be merged with a broader "Social Media Strategy" hub if the cluster stays thin. Keep separate as long as the consistency angle remains distinct from pure scheduling strategy.

```
Consistency Hub  (mega hub)
├── How to stay consistent on social media: ultimate guide
├── Social media consistency fundamentals
├── How to prevent content creator burnout
├── 10 tips to save time on social media
├── Social media for founders
└── Why social media platforms fail creators (opinion/thought leadership)
```

**Potential merge candidate:** If Cluster 7 (Consistency) and Cluster 8 (Strategy) both stay thin, consider consolidating them into a single "Social Media Strategy" cluster with a shared hub.

---

## Cluster Group 8: Multi-Platform Scheduling (General)

### What this cluster covers

Cross-platform and general scheduling strategy — not tied to a specific platform. Covers questions about how to manage a multi-channel presence efficiently.

### Structure

Single-level hub-and-spoke. Overlaps intentionally with Cluster 1 (Platform Scheduling) at the edges — spokes here cross-link to the relevant platform hubs.

```
Multi-Platform Scheduling Hub  (mega hub)
├── How to schedule posts across multiple social media platforms
├── How to post to all social media at once
├── How to schedule a full week of social media content
├── How far ahead should you schedule social media posts
├── Best practices for multi-platform scheduling
├── Social media posting schedule guide
├── How to automate social media posting
├── Automate posting across multiple channels
└── Schedule social media posts with Claude
```

**Cross-cluster links:** Multi-Platform Hub ↔ MCP Hub (Cluster 3), Multi-Platform Hub ↔ individual platform hubs in Cluster 1

---

## Cluster Group 9: Social Media Analytics

### What this cluster covers

How to read, interpret, and act on social media analytics data. This cluster bridges the scheduling/planning world (Clusters 1–8) with performance measurement.

### Structure

Grid-optional. Can be built as a flat hub initially, then expanded into a grid (Platform × Analytics Topic Type) as the cluster grows.

```
Analytics Hub  (mega hub)
├── Social media analytics: what metrics actually matter
├── How to read your social media analytics dashboard
├── Social media analytics for small businesses
├── Best social media analytics tools
├── How to use analytics to improve your posting schedule
└── Platform-specific analytics guides (dual-homed with Cluster 1):
    ├── Twitter analytics guide
    ├── Instagram analytics guide
    ├── LinkedIn analytics guide
    ├── Pinterest analytics guide
    └── TikTok analytics guide
```

**Cross-cluster links:** Analytics Hub ↔ Platform hubs in Cluster 1 (analytics spokes already exist there), Analytics Hub ↔ Small Business Hub (Cluster 10)

---

## Cluster Group 10: Social Media for Small Business

### What this cluster covers

Social media strategy, scheduling, and tools specifically for small businesses and solopreneurs — audience-segment lens rather than a platform or tactic lens.

**Relationship to vertical clusters (Cluster Group 15):** Small Business is the *cross-vertical* SMB hub — it covers content that applies to any small business regardless of industry (how to manage social with a small team, scheduling for solopreneurs, time-saving workflows). When a specific vertical (e.g., Real Estate, Coaches, Local Restaurants) has enough demand to warrant its own cluster, that vertical is **promoted to a top-level cluster under Cluster Group 15** rather than living as a subfolder here. Small Business links across to those vertical clusters; vertical clusters link back to Small Business for cross-vertical educational content.

### Structure

Grid-optional. Can expand into a (Platform × Small Business Topic) grid, but starts as a flat hub with platform-specific small business guides as dual-homed spokes.

```
Small Business Hub  (mega hub)
├── Social media for small business: where to start
├── Best social media platforms for small businesses
├── How to manage social media with a small team
├── Social media scheduling for solopreneurs
├── Time-saving social media workflows for small business
└── Platform-specific small business guides (dual-homed with Cluster 1):
    ├── Instagram for small business
    ├── Facebook for small business
    ├── LinkedIn for small business
    └── Pinterest for small business
```

**Cross-cluster links:** Small Business Hub ↔ platform "for business" spokes in Cluster 1, Small Business Hub ↔ Analytics Hub (Cluster 9), Small Business Hub ↔ Vertical Audience Clusters (Cluster Group 15) for industry-specific deep dives.

**Note on existing folder scaffold:** `_posts/small-business/` contains a deep pre-scaffolded folder tree (`local-business/restaurants/`, `local-business/real-estate/`, `startups/saas/`, etc.). That scaffold predates Cluster Group 15 and overlaps with the vertical-cluster model. When a vertical has its own top-level cluster under Cluster Group 15, the corresponding small-business subfolder should be left empty (no new articles written there) — content lives in the vertical cluster.

---

## Cluster Group 11: Social Media Growth Strategy

### What this cluster covers

How to grow an audience on social media — distinct from scheduling (how to post) and consistency (how to keep posting). Covers follower growth, engagement, and algorithmic dynamics.

### Structure

Grid-optional. Can expand into a (Platform × Growth Tactic) grid as content volume increases.

```
Growth Hub  (mega hub)
├── Social media growth strategy: complete guide
├── How to grow your social media following from zero
├── Social media growth for creators vs businesses
├── Organic growth vs paid growth on social media
└── Platform-specific growth guides (dual-homed with Cluster 1):
    ├── How to grow on Instagram
    ├── How to grow on LinkedIn
    ├── How to grow on TikTok
    ├── How to grow on Bluesky
    └── How to grow on Pinterest
```

---

## Cluster Group 12: Content Repurposing

### What this cluster covers

How to adapt existing content for different platforms and formats — a natural BrandGhost use case given its multi-platform scheduling capabilities.

### Structure

Grid-optional. The natural second dimension is "platform pair" (source → destination), which could expand into a grid of (source platform × destination platform) for repurposing workflow guides.

```
Repurposing Hub  (mega hub)
├── Content repurposing for social media: complete guide
├── How to repurpose a blog post for social media
├── How to repurpose a YouTube video across platforms
├── Cross-posting vs repurposing: what's the difference
├── How to repurpose long-form content into short posts
└── Platform-pair repurposing guides:
    ├── Repurpose Twitter threads for LinkedIn
    ├── Repurpose YouTube content for Instagram Reels
    └── Repurpose LinkedIn articles for Twitter/X
```

---

## Cluster Group 13: Personal Branding on Social Media

### What this cluster covers

How individuals build and manage a personal brand across social media platforms — distinct from brand/business social media management.

### Structure

Single-level hub-and-spoke initially. Can expand with platform-specific personal branding guides as dual-homed spokes.

```
Personal Brand Hub  (mega hub)
├── How to build a personal brand on social media
├── Personal branding vs company page: when to use which
├── How to define your personal brand voice
├── Content batching for personal brand builders
├── How to show up authentically as a personal brand
└── Platform-specific personal branding guides:
    ├── Personal branding on LinkedIn
    ├── Personal branding on Twitter/X
    └── Personal branding on Instagram
```

---

## Cluster Group 14: Brand Discoverability

### What this cluster covers

How brands get found across every modern surface where customers search — Google (SEO), AI chatbots like ChatGPT and Perplexity (GEO), voice assistants and answer engines like Siri/Alexa/Google AI Overviews (AEO), and social discovery on TikTok/YouTube/Instagram (Multi-Channel). This is the editorial cluster that anchors BrandGhost's "SEO, GEO & Social Discovery" positioning from the marketing site.

**Editorial framing — "Brand Discoverability":** The mega hub and sub-hub copy uses the phrase *Brand Discoverability* to mirror the BrandGhost brand language and signal category-creation. The folder slug stays `discoverability/` (short, brand-neutral URL, future-proof if naming evolves).

**Relationship to existing `seo/` folder:** The 5 articles currently in `_posts/seo/` (published 2026-06-09 through 2026-06-13) are thematically *discoverability* articles wearing an SEO folder label. They are slated to migrate to `discoverability/` (and the appropriate sub-hub) **with URL-preserving redirects**. Migration is deferred to a coordinated window; until then, those articles stay where they are and the discoverability cluster is built around them.

### Structure

Mega hub with 4 sub-hubs, each owning a clean keyword space. Sub-hubs are mini-hubs in the sense of the framework: they link up to the discoverability mega hub and down to their own spokes.

```
discoverability/   (mega hub)
├── hub: "Brand Discoverability: How to Get Found in 2026" — TOFU
├── from-seo-to-discoverability               ← exists at seo/, slated to migrate
├── multi-channel-discoverability             ← exists at seo/, slated to migrate (dual-homed)
│
├── seo/   (mini-hub: "SEO in 2026: What Still Matters")
│   ├── ai-influence-on-seo                   ← exists at seo/, slated to migrate
│   ├── (planned) modern SEO fundamentals
│   ├── (planned) technical SEO in the AI search era
│   └── (planned) on-page SEO checklist
│
├── geo/   (mini-hub: "Generative Engine Optimization (GEO): Get Cited by ChatGPT")
│   ├── (planned) what is GEO
│   ├── (planned) how to get cited by ChatGPT
│   ├── (planned) GEO vs SEO
│   ├── (planned) structuring content for LLM citation
│   ├── (planned) measuring GEO performance
│   ├── ai-content-generation-for-seo         ← exists at seo/, slated to migrate (rescope)
│   └── (planned) GEO for [vertical] — dual-homed with vertical clusters
│
├── aeo/   (mini-hub: "Answer Engine Optimization (AEO): Show Up in Voice and AI Answers")
│   ├── (planned) what is AEO
│   ├── (planned) AEO vs SEO
│   ├── (planned) AEO for voice search (Siri, Alexa, Google Assistant)
│   ├── (planned) AEO for Google AI Overviews
│   ├── (planned) featured snippets and AI answers
│   └── (planned) schema markup for AEO
│
└── multi-channel/   (mini-hub: "Multi-Channel Discoverability: Beyond Google")
    ├── discoverability-optimization-future-of-seo-beyond-websites ← exists at seo/, slated to migrate
    ├── (planned) social search optimization (TikTok and YouTube as search engines)
    ├── (planned) visual search discoverability
    └── (planned) community discoverability (Reddit, forums)
```

### Why sub-hubs and not sibling clusters

SEO, GEO, AEO, and Multi-Channel Discoverability all overlap significantly. Articles like "how AI is changing SEO" cross all four — they cannot pick a single sibling parent without forcing the choice. Under one mega hub, the umbrella article lives at `discoverability/` and each sub-hub owns its narrower keyword space without competing for the broader query.

### Keyword ownership per sub-hub

| Sub-hub | Target keyword pattern | Example primary keywords |
|---|---|---|
| `discoverability/` (mega) | "brand discoverability", "online discoverability", "discoverability optimization", "get found online" | Owns the umbrella term — never compete with this from sub-hubs |
| `discoverability/seo/` | Modern SEO in the AI era: "SEO best practices 2026", "AI-era SEO", "SEO fundamentals" | Avoid generic "what is SEO" — too saturated |
| `discoverability/geo/` | "generative engine optimization", "GEO", "rank in ChatGPT", "get cited by AI", "AI search optimization", "LLM SEO" | **Greenfield keyword space — own the category** |
| `discoverability/aeo/` | "answer engine optimization", "AEO", "voice search optimization", "Google AI Overviews", "featured snippets" | Established but underserved |
| `discoverability/multi-channel/` | "multi-channel discoverability", "social search", "TikTok SEO", "YouTube SEO", "visual search" | Pairs with content-repurposing/ cluster |

### Cross-cluster links

- `discoverability/*` ↔ `brandghost/launchpad/audit/*` — every discoverability theory article links to the relevant audit (the diagnostic); audit articles link up to the discoverability sub-hub they measure.
- `discoverability/*` ↔ `brandghost/launchpad/*` — every discoverability article funnels to the product as the execution path.
- `discoverability/geo/[vertical]`, `discoverability/aeo/[vertical]` ↔ vertical clusters (Cluster Group 15) — vertical-specific spokes dual-home with the relevant vertical hub.
- `discoverability/multi-channel/*` ↔ `content-repurposing/` (Cluster 12) — repurposing is a key tactic for multi-channel discoverability.
- `discoverability/*` ↔ `artificial-intelligence/ai-content/` (Cluster 4) — AI content is the engine that produces discoverable content at scale.
- `discoverability/*` ↔ `analytics/` (Cluster 9) — measurement of GEO/AEO performance gets dual-homed spokes in the analytics cluster.

### Funnel stage rules for discoverability cluster

- Mega hub → `tofu` (category education)
- Sub-hub L1 articles ("what is GEO", "what is AEO", etc.) → `tofu`
- Tactical spokes ("how to get cited by ChatGPT", "schema markup for AEO") → `mofu`
- "Launchpad does this for you" oriented spokes → `bofu` and live in `brandghost/launchpad/`, not here

### Build priority

Phase 1 build: mega hub + GEO mini-hub. Rationale — GEO has the largest greenfield keyword space (the term is brand-new in search behaviour) and is BrandGhost's most differentiated angle vs scheduling competitors. SEO/AEO/Multi-Channel sub-hubs follow in subsequent phases as the existing 5 `seo/` articles migrate in.

---

## Cluster Group 15: Vertical Audience Clusters

### What this cluster group covers

One top-level cluster per audience vertical listed on the BrandGhost marketing site at `/use-cases`. Each vertical is its own self-contained hub-and-spoke cluster. This is a *cluster pattern*, not a single cluster — Cluster Group 15 documents the rules; each individual vertical (Cluster 15a, 15b, 15c, …) follows them.

The 10 verticals identified on the marketing site:

| Vertical | Folder slug | Status |
|---|---|---|
| Real Estate Agents | `real-estate/` | **Phase 1 build — primary** |
| Coaches & Consultants | `coaches/` | Planned |
| Marketing Agencies | `agencies/` | Planned |
| E-commerce & DTC Brands | `ecommerce/` | Planned |
| SaaS & Tech Companies | `saas/` | Planned (note: existing `_posts/small-business/startups/saas/` scaffold to be retired in favour of top-level cluster) |
| Local Businesses | `local-businesses/` | Planned (broad cross-industry — distinct from individual local-vertical clusters like restaurants/) |
| Professional Services | `professional-services/` | Planned |
| Education & Training | `education/` | Planned |
| Nonprofits & Churches | `nonprofits/` | Planned |
| Monetized Creators | (covered by existing `content-creators/`) | Existing cluster — reframe and link as a vertical |

### Why top-level and not nested

The marketing site treats each vertical as a *peer audience*, not a sub-type of another. Real Estate sits next to Local Businesses on the use-cases page as an equal entry point. Nesting verticals under `small-business/` (the existing scaffold) would orphan them behind a parent hub that does not yet exist and would tie each vertical's URL to a hierarchy that the brand does not actually use.

Top-level placement also creates clean, brand-aligned URLs (`/posts/real-estate-content-calendar/` vs `/posts/small-business/local-business/real-estate/...`).

### Standard vertical cluster shape

Every vertical cluster follows the same template. Each vertical produces ~6–10 spokes for a minimum-viable cluster, can expand to 20+ over time as long-tail variations emerge.

```
[vertical]/   (mega hub: "Social Media Marketing for [Vertical]: Complete Guide")
├── Local SEO / industry SEO guide for [vertical]
├── Best social platforms for [vertical]
├── [Primary platform for vertical] marketing guide for [vertical]
├── Content ideas for [vertical]
├── AI tools and Launchpad for [vertical]
├── GEO for [vertical] — dual-homed with discoverability/geo/
├── Content calendar template for [vertical] — dual-homed with content-planning/content-calendar/
└── (optional) Sub-vertical spokes (e.g., real-estate/{commercial,residential,mortgage})
```

### Cross-cluster links per vertical

Every vertical cluster owes the following outbound links from its mega hub:

| Link target | Reason |
|---|---|
| `discoverability/` mega hub | Discoverability is the strategy each vertical pursues |
| `discoverability/geo/[vertical]` | Vertical-specific GEO spoke (dual-homed) |
| `discoverability/aeo/[vertical]` | Vertical-specific AEO spoke when written (dual-homed) |
| Relevant `social-media-platforms/[platform]/` hubs | Whichever platforms dominate for that vertical (e.g., real-estate → Instagram, Facebook, YouTube) |
| `brandghost/launchpad/` (when live) | Product conversion CTA |
| `analytics/` mega hub | Performance measurement entry point |
| `content-planning/content-calendar/` | Calendar template dual-home |

### Keyword ownership per vertical cluster

| Vertical | Primary keyword patterns |
|---|---|
| `real-estate/` | "social media for real estate agents", "real estate marketing", "[city] realtor marketing", "Instagram for real estate", "real estate content ideas", "GEO for real estate agents" |
| `coaches/` | "social media for coaches", "marketing for consultants", "thought leadership content", "coaching content strategy" |
| `agencies/` | "social media agency tools", "white-label content tools", "client content management", "agency workflow" |
| `ecommerce/` | "social media for ecommerce", "DTC content marketing", "Shopify social", "product content strategy" |
| `saas/` | "social media for SaaS", "B2B content marketing", "developer marketing", "SaaS thought leadership" |
| `local-businesses/` | "social media for local business", "local SEO + social", "near me marketing" |
| `professional-services/` | "social media for [accountants/lawyers/etc]", "professional services content marketing" |
| `education/` | "social media for course creators", "education marketing", "training program promotion" |
| `nonprofits/` | "social media for nonprofits", "church social media", "cause-related marketing" |

### Funnel stage rules for vertical clusters

- Vertical mega hub → `tofu` (broad audience-aware education)
- "Best platforms for [vertical]" → `tofu`
- "Content ideas for [vertical]" → `tofu`
- "AI tools for [vertical]" and "Launchpad for [vertical]" → `mofu` (product-aware reader)
- "How [Vertical Company] uses BrandGhost" success stories → `mofu` (lives under `brandghost/success-stories/[vertical]/` not the vertical cluster itself)

### Vertical Cluster 15a: Real Estate (first concrete instance)

**Status:** Phase 1 build alongside the Brand Discoverability cluster.

**Folder slug:** `real-estate/`

**Mega hub:** "Social Media Marketing for Real Estate Agents: Complete Guide"

**Initial spoke set (~6–7 spokes for MVP):**

```
real-estate/
├── (planned) Local SEO for real estate agents — rank for "[city] realtor"
├── (planned) Best social platforms for real estate agents (Instagram, Facebook, YouTube)
├── (planned) Real estate Instagram marketing guide
├── (planned) Content ideas for real estate agents (just-listed, neighborhood, market updates)
├── (planned) AI tools for real estate marketing
├── (planned) GEO for real estate agents — dual-homed with discoverability/geo/
└── (planned) Real estate content calendar template — dual-homed with content-planning/content-calendar/
```

**Sub-vertical spokes (deferred to later phases):** commercial real estate, residential, mortgage agents, property managers, luxury real estate.

**Cross-cluster links (mandatory at write time):**
- ↔ `discoverability/` mega hub
- ↔ `social-media-platforms/instagram/`, `social-media-platforms/facebook/`, `social-media-platforms/youtube/` hubs
- ↔ `content-planning/content-calendar/` hub (for the calendar template spoke)

**Cross-cluster links (added post-publish):**
- ↔ `discoverability/geo/` and the GEO-for-real-estate spoke once both are live
- ↔ `brandghost/launchpad/` mega hub when it exists

**Existing scaffold cleanup:** `_posts/small-business/local-business/real-estate/` (empty folder + empty `mortgage/` subfolder) is left in place but **must not receive new articles**. Content goes to `_posts/real-estate/` instead. The empty scaffold can be removed in a later cleanup pass.

---

## Internal Linking Rules

### Spoke → hub (mandatory)

Every spoke must link up to its immediate parent hub. Mini-hubs link to both their parent hub and their grandparent hub if one exists.

```
sub-spoke links to → mini-hub (mandatory)
sub-spoke links to → L1 hub (optional but recommended)
spoke links to → L1 hub (mandatory)
L1 hub links to → mega-hub (mandatory)
```

### Hub → spoke (expected)

Hub articles must link down to all published spokes. Because hubs are written before their spokes (by build sequence), hub → spoke links for future-dated spokes are **added post-publish** via the `blog-internal-link-pipeline` skill. Never add a hub → spoke link at write time for a spoke that hasn't been published yet.

### Cross-cluster linking patterns

**Platform hub ↔ Analytics hub:**
- Platform analytics spoke (e.g., `twitter-x-analytics-guide-creators`) links up to **both** its platform hub AND the analytics mega-hub
- Analytics mega-hub links to each platform analytics spoke
- Platform hub optionally links to the analytics mega-hub as a "go deeper" reference

**Platform hub ↔ Content Calendar hub:**
- Platform calendar template spoke (e.g., `twitter-content-calendar-template`) links up to **both** its platform hub AND the content calendar hub
- Content calendar hub links to each platform calendar spoke

**Platform hub ↔ Small Business hub:**
- Platform for-business spoke (e.g., `twitter-for-business-scheduling`) links up to its platform hub as primary parent
- Small Business hub links to each platform for-business spoke as secondary navigation

**Analytics hub ↔ Small Business hub:**
- `social-media-analytics-for-small-businesses` is a spoke of both clusters
- Both hub pages link to it; the article links up to both

**Discoverability hub ↔ Audit cluster:**
- Every `discoverability/[sub-hub]/*` article links to the relevant audit article in `brandghost/launchpad/audit/*` as the diagnostic counterpart (e.g., a "how to optimize for GEO" spoke links to a "brand audit for GEO" article).
- Audit articles link up to the corresponding discoverability sub-hub for the strategy context they measure.

**Discoverability hub ↔ Launchpad hub:**
- Every discoverability article includes one outbound link to `brandghost/launchpad/` as the product execution path. This is the funnel handoff from strategy (discoverability) to product (launchpad).

**Discoverability hub ↔ Vertical cluster (Cluster Group 15):**
- Each vertical cluster's mega hub links up to `discoverability/` as the cross-vertical strategy hub.
- When a vertical-specific GEO or AEO spoke is written (e.g., "GEO for real estate agents"), it is dual-homed: it lives under both `discoverability/geo/` and the vertical cluster.
- Vertical clusters never duplicate discoverability content — they link to it.

**Discoverability hub ↔ AI Content / Content Repurposing / Analytics:**
- `discoverability/multi-channel/` ↔ `content-repurposing/` (Cluster 12) — repurposing is a primary tactic for multi-channel discoverability.
- `discoverability/*` ↔ `artificial-intelligence/ai-content/` (Cluster 4) — AI content production is the engine behind scalable discoverability.
- `discoverability/*` ↔ `analytics/` (Cluster 9) — measurement of SEO/GEO/AEO performance gets dual-homed spokes in the analytics cluster.

**Vertical cluster ↔ Platform hub (Cluster 1):**
- A vertical cluster's mega hub links to the 2–4 social platform hubs most relevant to that vertical (e.g., real-estate → Instagram, Facebook, YouTube).
- The vertical's platform-specific marketing guide spoke (e.g., "Real estate Instagram marketing guide") may be dual-homed with the platform hub when the topic is strong enough to dual-rank.

**Vertical cluster ↔ Small Business hub (Cluster 10):**
- Small Business hub links to each vertical mega hub as a "go deeper for your specific industry" reference.
- Vertical mega hubs may link up to Small Business for cross-vertical foundational content.

### Sibling cross-links (spoke → spoke)

Sibling cross-links (spoke to spoke within the same cluster) are allowed when contextually relevant but must not be forced. Guidelines:
- Link to a sibling when the current article would logically prompt the reader's next question
- Do not link to a sibling just because it's in the same cluster
- Maximum 1–2 sibling cross-links per article to avoid circular density

### No forward links in same cluster

**Never link to an article in the same cluster with a publish date later than the current article.** That URL will return 404 to every reader who visits before the linked article goes live. Same-cluster forward links are added post-publish via `blog-internal-link-pipeline`.

### Link density guidelines

| Article length | Internal links target range |
|---|---|
| Short (<800 words) | 1–3 |
| Medium (800–2000 words) | 3–6 |
| Long-form (2000+ words) | 5–10 |

These are soft targets. Links must serve the reader — do not pad to hit a number.

### Cross-cluster link eligibility

Before adding a cross-cluster link, verify:
1. The target article is already published (date ≤ today)
2. The anchor text reads naturally in context
3. The link serves the reader's likely next question — not just passes PageRank

If a cross-cluster link would require rewriting a sentence to feel natural, omit it. Forced links harm trust and readability.

