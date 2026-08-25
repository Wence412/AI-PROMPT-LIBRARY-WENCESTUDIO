# PROMPT UPDATE MANIFEST
Library Entry: video-script-writer.md | Category: Content Creation | Updated: 2026-03-27
Variables: {{VIDEO_TYPE}}, {{TARGET_LENGTH}}, {{PLATFORM}}, {{TOPIC}}, {{TARGET_VIEWER}}, {{KNOWLEDGE_LEVEL}}, {{TONE}}, {{PRESENTER_STYLE}}, {{CTA}}, {{VISUALS}}, {{MUSIC}}, {{BRAND_NOTES}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer / "Confidence" and "Confidence &
  Caveats" trailing output fields, and the forced mandatory-visible
  chain-of-thought requirement (now internal reasoning only). Source:
  Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the topic, target viewer, or video type is empty,
  placeholder, or too thin to script from, the prompt now says so and asks
  for specifics instead of inventing a topic or audience.
- Core prompt logic, variables, and output structure unchanged.
