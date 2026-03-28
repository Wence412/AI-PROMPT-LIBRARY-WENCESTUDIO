# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      business-plan-generator.md
Category:           Business, Strategy & Planning
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used          |
|------------------|-----------------------|-------------|---------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Complex     | search (optional)   |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Complex     | search (optional)   |
| GPT-OSS 120B     | gpt-oss-120b.md       | Complex     | search, code interp |

Variables to inject before use:
  {{BUSINESS_NAME}}, {{INDUSTRY}}, {{BUSINESS_MODEL}}, {{ONE_LINER}},
  {{STAGE}}, {{PRODUCT_DESCRIPTION}}, {{PROBLEM}}, {{TARGET_CUSTOMER}},
  {{UNIQUE_VALUE}}, {{PURPOSE}}, {{FUNDING_AMOUNT}}, {{TIMEFRAME}},
  {{TEAM_INFO}}, {{TRACTION}}, {{ASSETS}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard
