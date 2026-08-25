# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      career-coach.md
Category:           Personal Development & Coaching
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | search (optional) |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | search (optional) |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | search (optional) |

Variables to inject before use:
  {{CLIENT_NAME}}, {{CURRENT_ROLE}}, {{INDUSTRY}}, {{EXPERIENCE_YEARS}},
  {{CAREER_GOAL}}, {{CHALLENGE}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the current role, career goal, or challenge are empty,
  placeholder, or too thin to coach against, the prompt now says so and asks
  for specifics instead of inventing a client profile.
- Core prompt logic, variables, and output structure unchanged.
