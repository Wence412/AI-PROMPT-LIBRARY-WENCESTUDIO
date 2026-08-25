# PROMPT UPDATE MANIFEST
Library Entry: meeting-summarizer.md | Category: Meetings | Updated: 2026-03-26
Variables: {{MEETING_TYPE}}, {{DATE}}, {{DURATION}}, {{ATTENDEES}}, {{PURPOSE}}, {{TRANSCRIPT}}, {{LENGTH}}, {{AUDIENCE}}, {{FOCUS}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped adapter-layer boilerplate: fake confidence footer and
  mandatory-visible chain-of-thought. Core task logic unchanged.
