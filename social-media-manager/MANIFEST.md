# PROMPT UPDATE MANIFEST
Library Entry: social-media-manager.md | Category: Content Creation | Updated: 2026-03-27
Variables: {{CORE_MESSAGE}}, {{CONTENT_TYPE}}, {{PLATFORMS}}, {{BRAND_VOICE}}, {{AUDIENCE}}, {{GOAL}}, {{ASSETS}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer / "Confidence" and "Confidence &
  Caveats" trailing output fields, dead `<agentic_hooks>` scaffold, and the
  forced mandatory-visible chain-of-thought requirement (now internal
  reasoning only). Source: Migration Audit §08.
- **[FIX]** Platform character limits, hashtag counts, and "best posting
  time" claims were hardcoded as 2025-era fact; now labeled "Platform Spec
  Unconfirmed — verify current limits before publishing" across all 4 engine
  files and v1-legacy.md.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if a required field is empty, placeholder, or too thin to
  act on, the prompt now says so instead of inventing content.
- Core prompt logic, variables, and output structure unchanged.
