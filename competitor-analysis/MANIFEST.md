# PROMPT UPDATE MANIFEST
Library Entry: competitor-analysis.md | Category: Business, Strategy & Planning | Updated: 2026-03-26
Variables: {{YOUR_COMPANY}}, {{YOUR_OFFERING}}, {{TARGET_MARKET}}, {{DIFFERENTIATOR}}, {{COMPETITOR_1-4}}, {{FOCUS}}, {{QUESTIONS}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Moderate | search (optional) |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Moderate | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | Moderate | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if your company's offering, target market, or the competitor
  list are empty, placeholder, or too thin to analyze meaningfully, the prompt
  now says so and asks for specifics instead of inventing competitor data.
- Core prompt logic, variables, and output structure unchanged.
