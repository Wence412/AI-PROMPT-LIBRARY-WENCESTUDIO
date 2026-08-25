# PROMPT UPDATE MANIFEST
Library Entry: comparative-analysis.md | Category: Research & Analysis | Updated: 2026-03-26
Upgraded By: WenceStudio Prompt Modernization Agent (Antigravity)

| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Complex | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Complex | none |
| GPT-OSS 120B | gpt-oss-120b.md | Complex | none |

Variables: {{DOC_A_TITLE}}, {{DOC_A_CONTENT}}, {{DOC_B_TITLE}}, {{DOC_B_CONTENT}}, {{DOC_C_TITLE}}, {{DOC_C_CONTENT}}, {{FOCUS}}, {{CRITERIA}}, {{OUTPUT_TYPE}}, {{CONTEXT_OR_NONE}}

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Forced-singular-verdict framing (Migration Audit §08): the prompt
  required a per-dimension "winner" even when documents were genuinely
  comparable or under-specified. "Tie" and "Ambiguous / no clear winner" are
  now explicit, legitimate outcomes at both the dimension and overall-synthesis
  level, across all 4 engine files and v1-legacy.md.
- **[FIX]** Added a missing-data fallback: if a document is empty, placeholder,
  or too thin to compare meaningfully, the prompt now says so and asks for the
  missing content instead of inventing comparisons.
- Core prompt logic, variables, and output structure otherwise unchanged.
