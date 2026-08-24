# PROMPT UPDATE MANIFEST
Library Entry: contract-reviewer.md | Category: Research & Analysis (Legal) | Updated: 2026-08-24
Status: **DEPRECATED — MERGED into `legal-document-analyzer`** (see README.md)

## Change Log

### v2.0.0 — 2026-08-24
- **[DEPRECATED]** Merged into `legal-document-analyzer` per Migration Audit
  §07. `v1-legacy.md`, `claude-4-6.md`, `gemini-3-1-pro.md`, and
  `gpt-oss-120b.md` have been removed from this folder — see
  `legal-document-analyzer/` for the live prompt (Negotiation Mode section)
  and `legal-document-analyzer/MANIFEST.md` for the full merge changelog.
- Original variables `{{CONTRACT_TYPE}}, {{PARTIES}}, {{YOUR_POSITION}},
  {{DEAL_VALUE}}, {{JURISDICTION}}, {{CONTRACT_TEXT}}, {{MUST_HAVES}},
  {{RED_LINES}}, {{NICE_TO_HAVES}}` all map onto `legal-document-analyzer`'s
  variable set (`{{document_type}}`, `{{my_role}}`, `{{document_content}}`,
  plus the same Negotiation Mode fields) — no functionality was lost.

### v1.0 — 2025-12-19 (prior)
- Initial library entry, since merged.
