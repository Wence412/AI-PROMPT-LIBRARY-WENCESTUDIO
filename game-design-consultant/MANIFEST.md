# PROMPT UPDATE MANIFEST
Library Entry: game-design-consultant.md | Category: Gaming | Updated: 2026-03-26
Variables: {{GAME_NAME}}, {{GENRE}}, {{PLATFORM}}, {{AUDIENCE}}, {{CORE_FANTASY}}, {{REFERENCES}}, {{DESIGN_FOCUS}}, {{CHALLENGE}}, {{CONSTRAINTS}}, {{STAGE}}, {{EXISTING_DESIGN}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | search, code interp (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer, dead `<agentic_hooks>` scaffold
  (where present), and the forced mandatory-visible chain-of-thought
  requirement (now an internal reasoning instruction only). Source: Migration
  Audit §08.
- **[FIX]** Addressed forced-precision numeric output with no data grounding
  (Migration Audit §08): tunable balance parameters must now be labeled
  explicitly as illustrative playtesting starting points, not measured or
  balanced data.
- **[FIX]** Trimmed persona-inflation credential-stacking ("shipped 15+
  titles") named in Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if the game concept or design focus is empty, placeholder, or
  too thin to design against, the prompt now says so and asks for the
  missing specifics instead of inventing a concept.
- Core prompt logic, variables, and output structure unchanged.
