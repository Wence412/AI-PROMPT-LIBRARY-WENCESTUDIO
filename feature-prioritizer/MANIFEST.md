# PROMPT UPDATE MANIFEST
Library Entry: feature-prioritizer.md | Category: Product Management | Updated: 2026-03-26
Variables: {{FEATURE_1-5}}, {{DESC_1-5}}, {{COMPANY_GOALS}}, {{RESOURCES}}, {{TIMEFRAME}}, {{CONSTRAINTS}}, {{PRIMARY_CRITERIA}}, {{SECONDARY_CRITERIA}}, {{FRAMEWORK}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | code interp (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Source: Migration Audit §08.
- **[FIX]** Addressed forced-precision numeric output with no data grounding
  (Migration Audit §08): RICE/ICE/Weighted scores must now be labeled
  explicitly as illustrative estimates, not measured data, and any dimension
  lacking supporting rationale in the input is flagged rather than scored
  with fabricated precision.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if fewer than two features or no business context is
  provided, the prompt now says so and asks for the missing inputs instead
  of inventing features or goals.
- Core prompt logic, variables, and output structure unchanged.
