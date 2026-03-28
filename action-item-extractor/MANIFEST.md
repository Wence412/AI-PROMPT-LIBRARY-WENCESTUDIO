# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      action-item-extractor.md
Category:           Meetings
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none              |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none              |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none              |

Variables to inject before use:
  {{MEETING_NAME}}, {{DATE}}, {{ATTENDEES}}, {{PROJECT_CONTEXT}},
  {{TRANSCRIPT}}, {{FORMAT}}, {{INCLUDE}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard
