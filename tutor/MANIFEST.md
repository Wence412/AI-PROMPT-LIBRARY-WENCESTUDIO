# PROMPT UPDATE MANIFEST
Library Entry: tutor.md | Category: Students & School | Updated: 2026-03-27
Variables: {{SUBJECT}}, {{TOPIC}}, {{LEVEL}}, {{STUCK}}, {{GOAL}}
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
- **[FIX]** Made explicit across all 4 engine files and v1-legacy.md that
  tutoring is a multi-turn Socratic dialogue, not a single-shot
  complete-answer format — the prompt now instructs pacing one guiding
  question at a time and pausing for the student's reply, per Migration
  Audit finding (light touch, pedagogy unchanged).
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if subject, topic, or where-you're-stuck is empty,
  placeholder, or too thin to tutor on, the prompt now says so instead of
  inventing a topic.
- Core prompt logic, variables, and output structure unchanged.
