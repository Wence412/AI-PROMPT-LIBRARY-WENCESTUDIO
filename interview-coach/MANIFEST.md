# PROMPT UPDATE MANIFEST
Library Entry: interview-coach.md | Category: Job Search | Updated: 2026-03-26
Variables: {{POSITION}}, {{COMPANY}}, {{STAGE}}, {{JOB_DESCRIPTION}}, {{EXPERIENCE}}, {{ACHIEVEMENTS}}, {{CONCERNS}}, {{MODE}}, {{QUESTION_FOCUS}}, {{SPECIFIC_QUESTIONS}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped adapter-layer boilerplate: fake confidence footer and
  mandatory-visible chain-of-thought. Core task logic unchanged.
