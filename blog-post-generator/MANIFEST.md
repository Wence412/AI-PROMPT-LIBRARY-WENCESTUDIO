# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      blog-post-generator.md
Category:           Creative Writing & Content
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | search (optional) |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | search (optional) |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | search (optional) |

Variables to inject before use:
  {{TOPIC}}, {{ANGLE}}, {{PRIMARY_KEYWORD}}, {{SECONDARY_KEYWORDS}},
  {{TARGET_AUDIENCE}}, {{READER_PROBLEM}}, {{BRAND_VOICE}}, {{WORD_COUNT}},
  {{CONTENT_TYPE}}, {{CTA_GOAL}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  □ Output reviewed against CATALOG.md quality standard

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>`/`Confidence & Caveats` footer, dead
  `<agentic_hooks>` scaffold, and the forced mandatory-visible chain-of-thought
  requirement (now an internal reasoning instruction only). Source: Migration
  Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if topic, target keyword, or audience are empty, placeholder,
  or too thin, the prompt now states "Insufficient input for [X]" instead of
  inventing generic filler content.
- Core prompt logic, variables, and output structure unchanged.
