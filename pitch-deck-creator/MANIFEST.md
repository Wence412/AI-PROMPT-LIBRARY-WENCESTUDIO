# PROMPT UPDATE MANIFEST
Library Entry: pitch-deck-creator.md | Category: Entrepreneurs | Updated: 2026-03-26
Variables: {{COMPANY_NAME}}, {{ONE_LINER}}, {{STAGE}}, {{RAISE_AMOUNT}}, {{STYLE}}, {{PROBLEM}}, {{SOLUTION}}, {{CUSTOMER}}, {{BUSINESS_MODEL}}, {{TRACTION}}, {{MARKET_SIZE}}, {{COMPETITORS}}, {{DIFFERENTIATOR}}, {{FOUNDERS}}, {{WHY_YOU}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer and the forced mandatory-visible
  chain-of-thought requirement (now an internal reasoning instruction only).
  Source: Migration Audit §08.
- **[FIX]** Trimmed persona-inflation credential-stacking ("helped raise
  $500M+ in aggregate funding") named in Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the company name, problem, and solution are all empty,
  placeholder, or too thin to build a deck from, the prompt now says so and
  asks for the missing specifics instead of inventing a startup, traction, or
  market data.
- Core prompt logic, variables, and output structure unchanged.
