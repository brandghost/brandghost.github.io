# BrandGhost Blog — Content Architecture Framework

---

## Purpose of This Document

This document defines the **structural DNA** of the BrandGhost blog — how content is organized, how pages relate to each other, and how to reason about what to build next. It is intentionally free of keyword volume data, traffic metrics, or competitive analysis. Those inputs inform *which* topics to prioritize, but this framework governs *how* topics are organized regardless of when they are built.

Use this document as a reference when:
- Briefing an LLM to generate new articles within an existing cluster
- Deciding where a new article belongs in the architecture
- Planning a new cluster from scratch
- Establishing internal linking for any new or edited post

---

## Core Concept: Hub-and-Spoke with Mini-Hubs

### Hub

A **hub** is a broad, high-level page that:
- Introduces a topic category and orients the reader
- Links down to every spoke article it owns
- Receives links back up from all of its spokes
- Does not need to cover each spoke's topic in depth — it summarizes and delegates

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
[ Cluster: Platform Scheduling ]    [ Cluster: Content Calendar ]    [ Cluster: AI Scheduling ]
           ↕ cross-links                      ↕ cross-links                  ↕ cross-links
[ Cluster: Small Business ]         [ Cluster: Analytics ]           [ Cluster: Growth Strategy ]
```

Each cluster group is an independent entry point for a reader. Cross-links between clusters are explicit and documented per cluster below.

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

Current planned audience hubs: **Social Media Analytics**, **Small Business**
Future audience hub candidates: E-Commerce, Nonprofits, Agencies, Creators, B2B

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
| `Small Business` | SMB-focused cross-platform guides (note: platform-specific for-business posts go under `Social Media Platforms`) |
| `Growth & Engagement` | Audience growth, engagement strategy, algorithm guides |
| `Personal Branding` | Personal brand strategy, thought leadership, creator identity |
| `BrandGhost` | Product announcements, release notes, BrandGhost-specific features (BOFU only) |

### Platform names (exact capitalisation required)

`Twitter`, `Instagram`, `Pinterest`, `Facebook`, `Threads`, `Mastodon`, `Bluesky`, `TikTok`, `LinkedIn`, `Telegram`, `YouTube`, `Reddit`, `Discord`

### Category assignment rules (in priority order)

1. If slug contains `mcp`, `ai-content`, `automat`, `claude`, `chatgpt` → `AI & Automation`
2. If slug contains `analytics`, `metrics`, `impressions`, `dashboard`, `roi`, `reporting` AND no platform in slug → `Social Media Analytics`
3. If slug contains `analytics`, `metrics`, `impressions` AND platform in slug → `Social Media Platforms` (+ platform L2); also add `secondary_cluster_id: analytics` in frontmatter
4. If slug contains `-vs-`, `best-.*-scheduler`, `comparison` → `Social Media Platforms` (+ platform L2) if platform-specific; `Creator Tools` if generic tool comparison
5. If slug contains `calendar`, `content-pillar`, `batching`, `repurpose`, `strategy` → `Content Strategy` or `Content Calendar`
6. If slug contains `screenshot`, `character-counter`, `thread-splitter` → `Creator Tools`
7. If slug contains `small-business` without a platform → `Small Business`
8. Default for platform-specific posts → `Social Media Platforms` (+ platform L2)

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

## Cluster Group 5: Creator Tools & Workflow

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

**Cross-cluster links:** Small Business Hub ↔ platform "for business" spokes in Cluster 1, Small Business Hub ↔ Analytics Hub (Cluster 9)

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

