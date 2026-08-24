# PROMPT UPDATE MANIFEST
Library Entry: legal-brief-drafter.md | Category: Legal | Updated: 2026-08-24
Upgraded By: WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version: 2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate: 🔴 HUMAN REVIEW REQUIRED (licensed counsel)
  This prompt drafts court-facing documents. No output may be filed, sent, or
  relied upon until a licensed attorney has independently verified every
  citation flagged "AUTHORITY NEEDED — NOT VERIFIED" (and spot-checked the
  USER-SUPPLIED ones) in the Citation Audit table. A fabricated citation
  filed with a court carries direct sanctions/malpractice exposure.

Variables: {{CASE_NAME}}, {{COURT}}, {{DOC_TYPE}}, {{POSITION}}, {{FACTS}}, {{PRIMARY_ARGUMENT}}, {{SUPPORTING_POINTS}}, {{KEY_AUTHORITY}}, {{OPPOSITION}}, {{ADVERSE_CASES}}, {{LIMIT}}, {{CITATION_FORMAT}}

| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional — retrieved citations still require verification) |

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory, structural Citation Verification
  Gate in every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b). The model may cite only authority the user actually
  supplied (`{{key_authority}}` / `{{adverse_cases}}`); anything else must
  be tagged `AUTHORITY NEEDED — NOT VERIFIED` rather than invented. This
  replaces the prior advisory-only disclaimer language.
  Source: Migration Audit §04/§05, P0 finding "Court-facing document
  generator with no citation-verification gate."
- **[ADDED]** Structural Citation Audit table appended to every brief,
  auditing every citation used against USER-SUPPLIED / NOT VERIFIED status
  — present even when the audit is all "NOT VERIFIED," so the reviewer
  knows nothing has been confirmed.
- **[ADDED]** v1-legacy.md now carries an explicit hard disclaimer; it
  previously had none at all.
- **[GOVERNANCE]** Flagged HUMAN REVIEW (licensed counsel) required — see
  gate above; this prompt was previously deployed with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. v1-legacy.md had zero hallucination guard or
  disclaimer. claude-4-6.md added an advisory disclaimer line only —
  no structural mechanism prevented the model from inventing citations.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Citation Verification Gate present and evaluated before drafting, in every variant
  ☑ Citation Audit table required in output, in every variant
  ☑ Disclaimer present in every variant, including v1-legacy.md
  ☐ Every "NOT VERIFIED" citation confirmed by licensed counsel against a primary source
  ☐ Licensed-counsel sign-off obtained before filing or sending any output
