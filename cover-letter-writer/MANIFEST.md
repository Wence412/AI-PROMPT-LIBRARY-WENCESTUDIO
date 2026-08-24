# PROMPT UPDATE MANIFEST
Library Entry: cover-letter-writer.md | Category: Job Search | Updated: 2026-03-26
Variables: {{EXPERIENCE_SUMMARY}}, {{JOB_TITLE}}, {{COMPANY}}, {{JOB_DESCRIPTION}}, {{WHY_COMPANY}}, {{WHY_ROLE}}, {{UNIQUE_VALUE}}, {{KEY_STORY}}, {{TONE}}, {{LENGTH}}, {{CONCERNS}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Moderate | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Moderate | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | Moderate | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if experience, JD, or personal-connection inputs are empty,
  placeholder, or too thin to build a genuine story from, the prompt now says
  so and asks for specifics instead of inventing achievements or company
  details.
- Core prompt logic, variables, and output structure unchanged.
