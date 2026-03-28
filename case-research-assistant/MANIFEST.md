# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      case-research-assistant.md
Category:           Research & Analysis (Legal)
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Complex     | search (optional) |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Complex     | search (optional) |
| GPT-OSS 120B     | gpt-oss-120b.md       | Complex     | search (optional) |

Variables to inject before use:
  {{LEGAL_QUESTION}}, {{JURISDICTION}}, {{AREA_OF_LAW}}, {{FACTS}},
  {{POSITION}}, {{OPPOSING_ARGUMENT}}, {{FOCUS}}, {{SPECIFIC_CASE}},
  {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard
