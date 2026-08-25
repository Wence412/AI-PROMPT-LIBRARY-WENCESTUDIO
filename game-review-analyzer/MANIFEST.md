# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      game-review-analyzer.md
Category:           Gaming
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-integrity change)

| Engine           | File                  | Tools               |
|------------------|-----------------------|----------------------|
| Claude Sonnet 4.6| claude-4-6.md         | none                 |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | search (optional)    |
| GPT-OSS 120B     | gpt-oss-120b.md       | search (optional)    |

Variables to inject before use:
  {{GAME_NAME}}, {{PUBLISHER}}, {{PLATFORMS}}, {{RELEASE_INFO}}, {{REVIEW_CONTENT}}, {{FOCUS}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Score Integrity Guardrail to every
  variant (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b). The
  Summary Metrics table (Metacritic/OpenCritic/Steam) now states a specific
  score **only** if it was supplied in `{{review_content}}` or retrieved
  this turn via an actual search/tool call — otherwise it renders "Score
  Unavailable — no review data provided" instead of a plausible-sounding
  number. Representative quotes in the Praise/Criticism tables must
  likewise come from supplied or retrieved review text, not be invented.
  Source: Migration Audit P1 finding "game-review-analyzer's format demands
  specific Metacritic/Steam scores even when no review content or search
  tool is supplied." Module: `modules/hallucination-guard.md`.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer (claude-4-6.md)
  and the `### Confidence` / `**Confidence & Caveats**` fields (gemini-3-1-pro.md,
  gpt-oss-120b.md) — a numeric confidence score does not fix an invented
  review score; the guardrail above does.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md.
- **[FIX]** Removed `<chain_of_thought>mandatory</chain_of_thought>` from
  `<thinking_config>` and converted the `<thinking>` output node into brief
  internal-reasoning guidance (including a step to check what review data
  was actually supplied/retrieved) rather than a mandatory visible block.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. Output format demanded a specific Metacritic/
  OpenCritic/Steam score row even when no review content or search tool was
  supplied, incentivizing an invented number; claude-4-6.md also carried a
  bare `<confidence>` footer.

Deployment checklist:
  ☑ Variables populated
  ☑ Score Integrity Guardrail present in every variant
  ☑ No numeric confidence score anywhere in the output
  ☑ Verified "Score Unavailable" renders correctly when {{REVIEW_CONTENT}}
    is empty and no search tool is enabled
