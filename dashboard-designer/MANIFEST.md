# PROMPT UPDATE MANIFEST
Library Entry: dashboard-designer.md | Category: Data & Analytics | Updated: 2026-03-26
Variables: {{NAME}}, {{USER}}, {{DECISIONS}}, {{REFRESH}}, {{DATA_SOURCES}}, {{QUESTIONS}}, {{TOOL}}, {{DEVICE}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Complex | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Complex | none |
| GPT-OSS 120B | gpt-oss-120b.md | Complex | code interp (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold,
  the forced mandatory-visible chain-of-thought requirement (now internal
  reasoning only), and "world-class" persona inflation in claude-4-6.md.
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if data sources or key questions are empty, placeholder, or
  too thin to support real design decisions, the prompt now says so and asks
  for specifics instead of inventing data fields or metrics.
- Core prompt logic, variables, and output structure unchanged.
