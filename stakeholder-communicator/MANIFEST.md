# PROMPT UPDATE MANIFEST
Library Entry: stakeholder-communicator.md | Category: Product Management | Updated: 2026-03-27
Variables: {{AUDIENCE}}, {{TYPE}}, {{TOPIC}}, {{FORMAT}}, {{KEY_MESSAGE}}, {{DATA}}, {{BACKGROUND}}, {{ASK}}, {{RELATIONSHIP}}, {{SENSITIVITY}}
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
  v1-legacy.md: if the key message, supporting data, or background is
  empty, placeholder, or too thin to communicate credibly, the prompt now
  says so and asks for specifics instead of inventing data, context, or
  outcomes.
- Core prompt logic, variables, and output structure unchanged.
