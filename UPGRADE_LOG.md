# 🔄 UPGRADE LOG — AI-PROMPT-LIBRARY-WENCESTUDIO

**Upgrade Date**: 2026-03-27
**Standard**: 2026 Reasoning-Aware Prompt Architecture
**Engines**: Claude Sonnet 4.6 · Gemini 3.1 Pro · GPT-OSS 120B

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

## Upgraded Prompts (70)

### Batch 1 — Analyze & Coach
api-documentation, blog-post-generator, brand-voice-analyzer, business-plan-generator, career-coach, code-reviewer, concept-explainer, content-repurposer, cover-letter-writer, creative-brainstormer

### Batch 2 — Code to Data
dashboard-designer, data-analyst, debate-partner, debug-assistant, devops-pipeline, document-summarizer, email-newsletter, email-writer, essay-improver, executive-coach

### Batch 3 — Feature to Grant
feature-prioritizer, financial-advisor, fitness-coach, game-design-consultant, github-actions, grant-writer, graph-generator, growth-hacker, business-contract-generator, competitor-analyzer

### Batch 4 — Habit to Life
habit-formation, image-prompt-generator, incident-response, infographic-planner, interview-coach, journaling-coach, key-insights-extractor, legal-brief-drafter, legal-document-analyzer, life-coach

### Batch 5 — LinkedIn to PRD
linkedin-optimizer, listing-writer, market-research, market-researcher, meeting-summarizer, mindfulness-guide, narrative-designer, pitch-deck-creator, poetry-composer, prd-generator

### Batch 6 — Property to Salary
property-analyzer, refactoring-guide, research-assistant, resume-optimizer, roadmap-planner, salary-negotiator

### Batch 7 — Security to Tutor
security-audit, seo-content-optimizer, social-media-manager, stakeholder-communicator, startup-advisor, story-writer, strategy-guide-creator, study-guide-creator, threat-analyzer, tutor

### Batch 8 — User to Vulnerability
user-story-writer, video-script-writer, vulnerability-assessment

### Catch-up
sentiment-analyzer

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
