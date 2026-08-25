# PROMPT UPDATE MANIFEST
Library Entry: seo-content-optimizer.md | Category: Content Creation | Updated: 2026-03-27
Variables: {{CONTENT_IDENTIFIER}}, {{EXISTING_CONTENT}}, {{TARGET_KEYWORD}}, {{SECONDARY_KEYWORDS}}, {{CURRENT_POSITION}}, {{TARGET_POSITION}}, {{COMPETITOR_URLS}}, {{SERP_FEATURES}}, {{GOAL}}, {{CONTENT_TYPE}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search |
| GPT-OSS 120B | gpt-oss-120b.md | search |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer / "Confidence" and "Confidence &
  Caveats" trailing output fields, and the forced mandatory-visible
  chain-of-thought requirement (now internal reasoning only). Source:
  Migration Audit §08.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if existing content, target keyword, or competitor context
  is empty, placeholder, or too thin to support real analysis, the prompt
  now says so and asks for specifics instead of inventing rankings,
  competitor data, or content gaps.
- Core prompt logic, variables, and output structure unchanged.
