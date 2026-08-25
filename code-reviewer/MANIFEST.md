# PROMPT UPDATE MANIFEST
Library Entry: code-reviewer.md | Category: Software Development | Updated: 2026-03-26
Upgraded By: WenceStudio Prompt Modernization Agent (Antigravity)

| Engine | File | Complexity | Tools Used |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Complex | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Complex | none |
| GPT-OSS 120B | gpt-oss-120b.md | Complex | code interp (optional) |

Variables: {{CODE}}, {{LANGUAGE}}, {{PURPOSE}}, {{CONCERNS}}, {{DEPTH}}, {{CONTEXT_OR_NONE}}

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the code block is empty, placeholder, or too thin to review
  meaningfully, the prompt now says so and asks for the missing code instead
  of inventing a review.
- Core prompt logic, variables, and output structure unchanged.
