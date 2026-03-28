# BrandGhost Blog — Agent Instructions

These rules apply to ALL agents working in this repository. Read this file before taking any action on blog content.

---

## Rule 1: Always ask which skill to use before editing or creating blog content

Before making **any** changes to blog posts or creating new content, if the user has not explicitly mentioned or implied a skill to use, you **MUST** ask:

> "Which skill should I use for this, if any?"

This applies to:
- Editing or updating an existing blog post
- Creating a new standalone blog post
- Creating a hub-and-spoke cluster or any part of one
- Rewriting or restructuring existing content

Do not assume. Do not proceed based on your own judgment about which skill is appropriate. Ask first.

---

## Rule 2: Always use `brandghost-seo-orchestrator` when building a cluster from scratch

When building a hub-and-spoke content cluster from scratch (new hub + new spokes), **always** use the local `brandghost-seo-orchestrator` skill:

**Location:** `.github/skills/brandghost-seo-orchestrator/SKILL.md`

Read that file first. It delegates to:
- Shared `blog-seo-orchestrator` (Phases 1–5: research, architecture, writing, validation, editorial review)
- Local `blog-seo-writing-by-intent` override (`.github/skills/blog-seo-writing-by-intent/SKILL.md`) — writes directly to `_posts/` in Jekyll YAML format
- Phase 6: featured image generation via `tools/skills/blog-featured-image/generate-image.ps1`

**Do not embed the orchestrator's instructions inline in a prompt.** Always instruct the agent to read and follow the SKILL.md file directly so the full skill chain and all constraints are enforced.

### Correct way to invoke:
```
Read and follow .github/skills/brandghost-seo-orchestrator/SKILL.md.
Build a TOFU cluster on "[topic]" starting [date].
```

### What the orchestrator enforces (do not bypass):
- Articles written to `_posts/` directly — never `drafts/`
- Jekyll YAML frontmatter — never JSON
- No H1 in article body
- `AllowedInternalLinks` must never include same-cluster URLs dated after the article being written
- SEO score ≥75 per article before moving on
- Featured image generated, uploaded, HTTP 200 verified for every article

---

## Rule 3: Never push to the remote repository

Only commit locally. Never run `git push` under any circumstances.

---

## Rule 4: Local skill overrides take precedence over shared skills

This repo has local skill overrides in `.github/skills/`. When a local override exists for a shared skill, the local version **always** takes precedence:

| Local Override | Overrides |
|----------------|-----------|
| `.github/skills/blog-seo-writing-by-intent/SKILL.md` | Shared `blog-seo-writing-by-intent` |

Read the local override before the shared skill when both exist.

---

## Rule 5: No forward same-cluster links

Never link from one cluster article to another cluster article with a later publish date. Those URLs will 404 when the earlier article goes live.

Same-cluster hub↔spoke links are added post-publish via `blog-internal-link-pipeline`.

---

## Rule 6: [UNVERIFIED] tags are a FAILURE STATE — zero tolerance

**This rule has NO exceptions and applies to every agent, every article, every pass.**

`[UNVERIFIED]` marks a claim that has NOT been verified. It is not a valid publishing state. Before any article is committed:

**Every `[UNVERIFIED]` tag must be resolved by doing exactly one of:**
1. Find a real, working citation URL → replace the tag with a `<a href="...">` anchor in the same sentence
2. **REMOVE** the specific claim (number, stat, or assertion) entirely
3. **SOFTEN** the language to remove the specific unverifiable assertion (e.g., "$10–$50" → "rates vary by channel size")

**Never leave `[UNVERIFIED]` in committed content.** If you see one, treat it as a blocker.

**Never add an `[UNVERIFIED]` tag as a "fix."** Adding the tag just labels the problem. The fix is cite, remove, or soften.

**Never invent URLs.** If you cannot find a real working URL, remove or soften the claim.

**When in doubt: cut it out.**

---

## Rule 7: Hub placement — one hub per folder, directly in the folder

A hub article **must live directly in the folder it anchors.** The hub at `_posts/foo/hub.md` anchors the `foo/` cluster — not any parent or child folder.

**Enforcement rules:**
- A folder requires exactly **one** `hub: true` file directly in it if the folder contains **≥3 direct `.md` article files**
- Zero hubs in a folder with ≥3 articles → **violation (missing hub)**
- Two or more `hub: true` files in the same folder → **violation (duplicate hub)**
- Empty or stub folders (< 3 direct articles) → no hub required; warning only

**Examples:**
- `_posts/artificial-intelligence/ai-content/hub.md` with `hub: true` → anchors `ai-content/`
- `_posts/artificial-intelligence/hub.md` with `hub: true` → anchors `artificial-intelligence/` (the group root)
- These are different hubs at different levels — not interchangeable

**Never place a hub at the wrong folder level.** If the hub title says "AI for Content Creators" it belongs in `ai-content/`, not the parent `artificial-intelligence/` folder.

---

