# PROMPT UPDATE MANIFEST
Library Entry: debug-assistant.md | Category: Software Development | Updated: 2026-03-26
Variables: {{SYMPTOMS}}, {{EXPECTED}}, {{WHEN_STARTED}}, {{LANGUAGE}}, {{CODE}}, {{ERROR}}, {{ATTEMPTS}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Moderate | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Moderate | none |
| GPT-OSS 120B | gpt-oss-120b.md | Moderate | search, code interp (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Forced-singular-verdict framing (Migration Audit §08): "Root Cause"
  implied a single diagnosis was always available. Renamed to "Likely Cause(s)"
  across all 4 engine files and v1-legacy.md — multiple plausible causes are
  now ranked by likelihood, and "insufficient information" is an explicit,
  legitimate output state when the evidence doesn't support a diagnosis.
- **[FIX]** Added a missing-data fallback: if the code, error, and symptoms
  are empty, placeholder, or too thin to isolate a cause, the prompt now says
  so and states what additional information would narrow it down.
- Core prompt logic, variables, and output structure otherwise unchanged.
