# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      agenda-generator.md
Category:           Meetings
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Simple      | none              |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Simple      | none              |
| GPT-OSS 120B     | gpt-oss-120b.md       | Simple      | none              |

Variables to inject before use:
  {{MEETING_TYPE}}, {{PURPOSE}}, {{OUTCOMES}}, {{DURATION}}, {{ATTENDEES}},
  {{TOPIC_1}}, {{TOPIC_2}}, {{TOPIC_3}}, {{DECISIONS}}, {{AVOID}},
  {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard
