# PROMPT UPDATE MANIFEST
Library Entry: linkedin-optimizer.md | Category: Job Search | Updated: 2026-03-26
Variables: {{CURRENT_HEADLINE}}, {{CURRENT_ABOUT}}, {{TARGET_ROLES}}, {{INDUSTRY}}, {{STAGE}}, {{SKILLS}}, {{UNIQUE_VALUE}}, {{FOCUS}}
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
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the current headline/About and target roles are all
  empty, placeholder, or too thin to work from, the prompt now says so and
  asks for the missing specifics instead of inventing a profile or
  achievements.
- Core prompt logic, variables, and output structure unchanged.
