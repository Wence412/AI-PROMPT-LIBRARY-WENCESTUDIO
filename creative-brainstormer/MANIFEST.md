# PROMPT UPDATE MANIFEST
Library Entry: creative-brainstormer.md | Category: Creative Writing & Content | Updated: 2026-03-26
Variables: {{CHALLENGE}}, {{CONTEXT_INFO}}, {{CONSTRAINTS}}, {{AUDIENCE}}, {{MOOD}}, {{RANGE}}, {{QUANTITY}}, {{SUCCESS_CRITERIA}}, {{AVOID}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Moderate | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Moderate | none |
| GPT-OSS 120B | gpt-oss-120b.md | Moderate | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Removed fake confidence footers/fields (meaningless on a subjective/creative task per audit), dead `agentic_hooks` scaffold, and mandatory-visible chain-of-thought across all engine files. Source: Migration Audit §08.
