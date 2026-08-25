# PROMPT UPDATE MANIFEST
Library Entry: story-writer.md | Category: Creative Arts | Updated: 2026-03-27
Variables: {{GENRE}}, {{TONE}}, {{LENGTH}}, {{POV}}, {{TENSE}}, {{PREMISE}}, {{SETTING}}, {{PROTAGONIST}}, {{CONFLICT}}, {{THEME}}, {{STYLE}}, {{INFLUENCES}}, {{AVOID}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Removed the forced mandatory-visible chain-of-thought
  requirement from claude-4-6.md's `<thinking_config>` (now internal
  reasoning only). Source: Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the premise, protagonist, or conflict is empty,
  placeholder, or too thin to build a real story from, the prompt now says
  so and asks for specifics instead of inventing a generic placeholder
  story.
- Core prompt logic, variables, and output structure unchanged.
