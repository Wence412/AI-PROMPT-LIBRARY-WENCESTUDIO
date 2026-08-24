# 🔄 UPGRADE LOG — AI-PROMPT-LIBRARY-WENCESTUDIO

**Upgrade Date**: 2026-03-27
**Reconciled**: 2026-08-24 (see Reconciliation Note below)
**Standard**: 2026 Reasoning-Aware Prompt Architecture
**Engines**: Claude Sonnet 4.6 · Gemini 3.1 Pro · GPT-OSS 120B

---

## ⚠️ Reconciliation Note (2026-08-24)

The original "Upgraded Prompts (70)" batch list below named roughly 15
prompts that do not exist as folders in this repository (`api-documentation`,
`brand-voice-analyzer`, `content-repurposer`, `data-analyst`,
`debate-partner`, `devops-pipeline`, `email-writer`, `financial-advisor`,
`fitness-coach`, `github-actions`, `grant-writer`, `graph-generator`,
`growth-hacker`, `business-contract-generator`, `competitor-analyzer`) while
omitting roughly 15 folders that do exist (`action-item-extractor`,
`agenda-generator`, `architecture-designer`, `case-research-assistant`,
`cbt-companion`, `chart-recommender`, `client-communicator`,
`comparative-analysis`, `competitor-analysis`, `contract-reviewer`,
`data-storyteller`, `documentation-writer`, `emotional-intelligence`,
`follow-up-composer`, `game-review-analyzer`). This was caught by the
[migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c)
§04 via direct comparison against the cloned repository's actual folder
list, independent of any model-verification question. The batch list below
has been regenerated from the real 70-folder list (confirmed 2026-08-24) so
this log can be trusted as an audit trail going forward.

---

## Summary

| Metric | Value |
|---|---|
| Prompts upgraded | **70** |
| Meta-prompts excluded | **4** |
| Files created | **350** (5 per prompt) |
| Subfolders | **70** |
| Batches | **8** |

---

## Per-Prompt Structure

Each upgraded prompt folder contains:

| File | Purpose |
|---|---|
| `v1-legacy.md` | Original prompt preserved |
| `claude-4-6.md` | XML structural isolation + `<thinking_config>` |
| `gemini-3-1-pro.md` | `[GROUNDING CONFIG]` + `[REASONING CHAIN]` |
| `gpt-oss-120b.md` | `[THINKING CONFIG]` + `[TOOL AUGMENTATION]` |
| `MANIFEST.md` | Variables, engine map, tool requirements |

---

## Upgraded Prompts (70) — regenerated 2026-08-24 from the actual folder list

### Batch 1 — Action to Chart
action-item-extractor, agenda-generator, architecture-designer, blog-post-generator, business-plan-generator, career-coach, case-research-assistant, cbt-companion, chart-recommender

### Batch 2 — Client to Dashboard
client-communicator, code-reviewer, comparative-analysis, competitor-analysis, concept-explainer, cover-letter-writer, creative-brainstormer, dashboard-designer

*(`contract-reviewer` was merged into `legal-document-analyzer` on 2026-08-24 — see Batch 5 and `contract-reviewer/README.md`. It remains on disk only as a deprecated redirect stub, not a live prompt.)*

### Batch 3 — Data to Feature
data-storyteller, debug-assistant, document-summarizer, documentation-writer, email-newsletter, emotional-intelligence, essay-improver, executive-coach, feature-prioritizer

### Batch 4 — Follow-up to Journaling
follow-up-composer, game-design-consultant, game-review-analyzer, habit-formation, image-prompt-generator, incident-response, infographic-planner, interview-coach, journaling-coach

### Batch 5 — Key Insights to Meeting
key-insights-extractor, legal-brief-drafter, legal-document-analyzer, life-coach, linkedin-optimizer, listing-writer, market-research, real-estate-market-researcher, meeting-summarizer

### Batch 6 — Mindfulness to Resume
mindfulness-guide, narrative-designer, pitch-deck-creator, poetry-composer, prd-generator, property-analyzer, refactoring-guide, academic-research-assistant, resume-optimizer

### Batch 7 — Roadmap to Story
roadmap-planner, salary-negotiator, security-audit, sentiment-analyzer, seo-content-optimizer, social-media-manager, stakeholder-communicator, startup-advisor, story-writer

### Batch 8 — Strategy to Vulnerability
strategy-guide-creator, study-guide-creator, threat-analyzer, tutor, user-story-writer, video-script-writer, vulnerability-assessment

---

## Excluded (Meta-Prompts)

These 4 meta-prompts remain as root-level `.md` files (not upgraded):

- `prompt-debugger.md`
- `prompt-evaluator.md`
- `prompt-optimizer.md`
- `prompt-versioner.md`

---

## Engine Architecture

### Claude Sonnet 4.6
- XML tags: `<instructions>`, `<thinking_config>`, `<context>`, `<task>`, `<output_format>`
- Extended Thinking with `mode="extended"`, `depth`, `reasoning_style`
- Confidence score 0–100

### Gemini 3.1 Pro
- `[GROUNDING CONFIG]` with context window + search source
- `[REASONING CHAIN]` with explicit steps
- Extended Reasoning — ON
- Context window declarations (STANDARD / MAXIMUM 2M)

### GPT-OSS 120B
- `[THINKING CONFIG]` with effort level + self-critique
- `[TOOL AUGMENTATION]` with search/code interpreter/Drive flags
- `[AGENT MODE: STANDALONE]`

---

## Infrastructure Files (Unchanged)

- `CATALOG.md` — Category index
- `README.md` — Repository overview
- `PLATFORM_GUIDE.md` — Platform comparison
- `PROMPT_TEMPLATE.md` — Template reference
