# PROMPT UPDATE MANIFEST
Library Entry: incident-response.md | Category: Cybersecurity | Updated: 2026-08-24
Upgraded By: WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version: 2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate: 🔴 HUMAN REVIEW REQUIRED
  This prompt produces regulatory breach-notification guidance and forensic
  triage during active incidents. No output may be treated as a fixed
  regulatory deadline or confirmed root cause without legal/compliance and
  forensic sign-off — see the Jurisdiction & Data-Availability Hedge in every
  variant.

Variables: {{INCIDENT_TYPE}}, {{INCIDENT_SUMMARY}}, {{DETECTION_TIME}}, {{CURRENT_STATE}}, {{AFFECTED_SYSTEMS}}, {{DATA_AT_RISK}}, {{USERS_AFFECTED}}, {{INDUSTRY}}, {{REGULATIONS}}, {{RESOURCES}}, {{SPECIFIC_QUESTION}}

| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | search (optional — regulatory results still require the hedge) |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional — regulatory results still require the hedge) |

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Jurisdiction & Data-Availability
  Hedge in every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b). Regulatory deadlines/requirements are now stated only when
  `{{regulations}}` actually names a framework/jurisdiction (otherwise the
  prompt outputs "Regulatory Guidance Unavailable" and escalates to
  legal/compliance instead of guessing). Unconfirmed forensic claims (root
  cause, entry point, scope) must be labeled `HYPOTHESIS — UNCONFIRMED`
  rather than asserted as fact. Severity is now explicitly framed as a
  working triage estimate, not a certified assessment.
  Source: Migration Audit §04/§05, P0 finding "Regulatory breach-
  notification guidance with no disclaimer in v1" / "still no explicit
  'state unavailable' fallback for missing forensic data" (claude-4-6).
- **[ADDED]** v1-legacy.md now carries an explicit hard disclaimer; it
  previously had none at all.
- **[GOVERNANCE]** Flagged HUMAN REVIEW required before any automated/
  autonomous use — see gate above; this prompt was previously deployed
  with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. v1-legacy.md stated severity, regulatory deadlines,
  and forensic conclusions definitively with no jurisdiction hedge or
  missing-data fallback. claude-4-6.md added a disclaimer line but still no
  explicit "state unavailable" fallback for missing forensic/regulatory data.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Jurisdiction & Data-Availability Hedge present and applied to every section, in every variant
  ☑ "Regulatory Guidance Unavailable" fallback fires when {{regulations}} is empty/ambiguous
  ☑ Unconfirmed forensic claims labeled HYPOTHESIS — UNCONFIRMED, not asserted as fact
  ☑ Disclaimer present in every variant, including v1-legacy.md
  ☐ Legal/compliance sign-off obtained before any regulatory deadline is treated as fixed
  ☐ Forensic sign-off obtained before any HYPOTHESIS item is treated as confirmed
