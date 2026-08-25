# PROMPT UPDATE MANIFEST
Library Entry: document-summarizer.md | Category: Research & Analysis | Updated: 2026-03-26
Variables: {{DOCUMENT_CONTENT}}, {{SUMMARY_LENGTH}}, {{TARGET_AUDIENCE}}, {{FOCUS_AREAS}}
| Engine | File | Complexity | Tools |
|---|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | Moderate | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | Moderate | none |
| GPT-OSS 120B | gpt-oss-120b.md | Moderate | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold, and
  the forced mandatory-visible chain-of-thought requirement (now an internal
  reasoning instruction only). Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the document content is empty, placeholder, or too thin to
  summarize meaningfully, the prompt now says so and asks for the missing
  material instead of inventing content.
- Core prompt logic, variables, and output structure unchanged.
