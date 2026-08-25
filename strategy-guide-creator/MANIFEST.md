# PROMPT UPDATE MANIFEST
Library Entry: strategy-guide-creator.md | Category: Gaming | Updated: 2026-03-27
Variables: {{GAME_NAME}}, {{VERSION}}, {{PLATFORM}}, {{FORMAT}}, {{TOPIC}}, {{SKILL_LEVEL}}, {{SPECIFIC_FOCUS}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>` footer/field and the forced mandatory-visible
  chain-of-thought requirement (now internal reasoning only). Source:
  Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the game, topic, or focus is empty, placeholder, or too
  thin to write a real guide from, the prompt now says so and asks for
  specifics instead of inventing game mechanics or data.
- Core prompt logic, variables, and output structure unchanged.
