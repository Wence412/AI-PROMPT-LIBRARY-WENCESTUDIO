# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      chart-recommender.md
Category:           Data & Analytics
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used             |
|------------------|-----------------------|-------------|------------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none                   |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none                   |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | code interp (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Removed fake confidence footers/fields, dead `agentic_hooks` scaffold, and mandatory-visible chain-of-thought across all engine files. Source: Migration Audit §08.

Variables to inject before use:
  {{DATA_DESCRIPTION}}, {{VARIABLES}}, {{DATA_SAMPLE}}, {{GOAL}},
  {{MESSAGE}}, {{AUDIENCE}}, {{TOOL}}, {{FORMAT}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Output reviewed against CATALOG.md quality standard
