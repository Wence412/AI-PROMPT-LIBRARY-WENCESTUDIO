# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      client-communicator.md
Category:           Real Estate
Updated:            2026-03-26
Upgraded By:        WenceStudio Prompt Modernization Agent (Antigravity)

| Engine           | File                  | Complexity  | Tools Used |
|------------------|-----------------------|-------------|------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none       |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none       |

Variables to inject before use:
  {{CLIENT_TYPE}}, {{STAGE}}, {{COMM_TYPE}}, {{SITUATION}},
  {{TONE}}, {{CONTEXT_OR_NONE}}

Deployment checklist:
  □ Variables populated
  □ Thinking Mode set to Extended in model panel
  □ Output reviewed against CATALOG.md quality standard

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Trimmed persona inflation ("world-class ...").
  Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the situation is empty, placeholder, or too thin to draft a
  genuine message from, the prompt now says so and asks for specifics instead
  of inventing client or deal details.
- Core prompt logic, variables, and output structure unchanged.
