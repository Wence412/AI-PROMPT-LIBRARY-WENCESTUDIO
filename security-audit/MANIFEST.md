# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      security-audit.md
Category:           Cybersecurity
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate:    🟠 NOT A SUBSTITUTE FOR A FULL PENETRATION TEST
  This prompt produces a security audit report that can drive remediation
  priorities. Every finding — especially anything marked "Identifier
  Unconfirmed" — requires human security-analyst sign-off before being
  treated as a complete picture of risk.

| Engine           | File                  | Complexity  | Tools Used                                |
|------------------|-----------------------|-------------|--------------------------------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Advanced    | none                                       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Advanced    | none                                       |
| GPT-OSS 120B     | gpt-oss-120b.md       | Advanced    | search (optional), code interpreter (optional) |

Variables to inject before use:
  {{AUDIT_TYPE}}, {{PLATFORM}}, {{CONTEXT}}, {{CODE_OR_CONFIG}},
  {{FOCUS_AREAS}}, {{EXPOSURE}}, {{SENSITIVITY}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory No-Fabrication Security Contract
  (from `modules/no-fabrication-security-contract.md`) to every variant
  (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b). CWE identifiers,
  OWASP category numbers, and CVE numbers (for flagged dependencies) may
  now only be cited if supplied by the user, a well-established mapping for
  a pattern clearly present in the code/config, or the result of an actual
  tool lookup this turn. Unconfirmed items must be marked "Identifier
  Unconfirmed" instead of stated as fact, and severity ratings are now
  explicitly qualitative unless computed CVSS vector data is present.
  Clarified that "Vulnerable Code" quotes the flawed snippet verbatim and
  must never be extended into a runnable proof-of-concept exploit. Source:
  Migration Audit §07/§10/§11, finding "Security-audit cluster's outputs
  read as complete audits if presented without qualification — a report
  that looks thorough but silently omits unconfirmed items reads as
  'clean' (false-negative risk)."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md. A numeric or
  bare confidence label on a security audit is false precision that
  invites treating an unconfirmed finding as verified.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>` and converted the `<thinking>` node under
  `<output_format>` from a mandatory visible block into internal-reasoning
  guidance that is not rendered in the report.
- **[GOVERNANCE]** Added explicit disclaimer to every variant's output: not
  a substitute for a full penetration test or licensed security assessment;
  all findings require human security-analyst sign-off. Added an Amber
  governance gate (see above); this prompt was previously deployed with no
  such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No fabrication gate on CWE/OWASP/CVE identifiers
  or CVSS scores. claude-4-6.md carried a bare `<confidence>` footer and
  mandatory chain-of-thought; gemini/gpt-oss variants carried bare
  confidence fields. No disclaimer about penetration-test scope or
  sign-off requirement.

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ No-Fabrication Security Contract present and evaluated for every finding
  ☑ Unconfirmed identifiers rendered literally, not omitted
  ☑ No numeric confidence score anywhere in the output
  ☑ Disclaimer present: not a substitute for a full penetration test
  ☐ Human security-analyst sign-off obtained before acting on findings
