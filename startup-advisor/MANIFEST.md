# PROMPT UPDATE MANIFEST
Library Entry: startup-advisor.md | Category: Entrepreneurs | Updated: 2026-03-27
Variables: {{COMPANY_NAME}}, {{STAGE}}, {{INDUSTRY}}, {{PRODUCT}}, {{MODEL}}, {{REVENUE}}, {{GROWTH}}, {{TEAM}}, {{RUNWAY}}, {{TRACTION}}, {{CHALLENGE}}, {{OPTIONS}}, {{QUESTION_1}}, {{QUESTION_2}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search (optional) |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional) |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all engine files: fake
  `<confidence>0–100</confidence>` footer and the forced mandatory-visible
  chain-of-thought requirement (now internal reasoning only). Source:
  Migration Audit §08.
- **[FIX]** Trimmed the credential-stacking persona ("2 exits, 50+
  investments, 100+ startups") named explicitly in Migration Audit §08, in
  favor of a plainer founder/angel investor/advisor framing.
- **[FIX]** Added a missing-data fallback across all 4 engine files and
  v1-legacy.md: if company metrics, challenge, or options are empty,
  placeholder, or too thin to advise on credibly, the prompt now says so
  and asks for specifics instead of inventing metrics or context.
- Core prompt logic, variables, and output structure unchanged.
