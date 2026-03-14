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
