# PROMPT UPDATE MANIFEST
Library Entry: academic-research-assistant.md (renamed from research-assistant.md on 2026-08-24) | Category: Students & School | Updated: 2026-08-24
Variables: {{TOPIC}}, {{QUESTION}}, {{FIELD}}, {{ASSIGNMENT}}, {{SOURCE_TYPES}}, {{COUNT}}, {{CITATION_STYLE}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search + scholar |
| GPT-OSS 120B | gpt-oss-120b.md | search |

## Change Log

### v1.1 — 2026-08-24
- **[RENAME]** `research-assistant` → `academic-research-assistant`, per
  Migration Audit §07: the generic name collided on catalog search with
  `market-research`, `case-research-assistant`, and `competitor-analysis`,
  despite this prompt being functionally distinct (academic/citation
  research helper using the CRAAP framework). No content or variable
  changes; disambiguation only.
