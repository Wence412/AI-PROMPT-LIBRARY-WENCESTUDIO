# PROMPT UPDATE MANIFEST
Library Entry: refactoring-guide.md | Category: Software Engineering | Updated: 2026-03-27
Variables: {{CODE}}, {{LANGUAGE}}, {{PURPOSE}}, {{PAIN_POINTS}}, {{CONSTRAINTS}}, {{GOALS}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | code interpreter (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer and the forced mandatory-visible
  chain-of-thought requirement (now an internal reasoning instruction only).
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the code to refactor is empty, placeholder, or too thin to
  refactor meaningfully, the prompt now says so and asks for the missing code
  instead of inventing a refactor.
- Core prompt logic, variables, and output structure unchanged.
