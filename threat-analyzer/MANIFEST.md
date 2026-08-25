# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      threat-analyzer.md
Category:           Cybersecurity
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate:    🟠 NOT A SUBSTITUTE FOR A FULL PENETRATION TEST
  This prompt produces a threat analysis report that can drive incident
  response decisions. Every finding — especially anything marked "Identifier
  Unconfirmed" or "Attribution Unconfirmed" — requires human security-analyst
  sign-off before being treated as a complete picture of risk.

| Engine           | File                  | Complexity  | Tools Used  |
|------------------|-----------------------|-------------|-------------|
| Claude Sonnet 4.6| claude-4-6.md         | Advanced    | none        |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Advanced    | search      |
| GPT-OSS 120B     | gpt-oss-120b.md       | Advanced    | search      |

Variables to inject before use:
  {{THREAT_TYPE}}, {{THREAT_DESCRIPTION}}, {{ARTIFACTS}}, {{CONTEXT}},
  {{INDUSTRY}}, {{MATURITY}}, {{ASSETS}}, {{DEPTH}}, {{FOCUS}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory No-Fabrication Security Contract
  (from `modules/no-fabrication-security-contract.md`) to every variant
  (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b). MITRE ATT&CK
  technique IDs, CVE/CWE identifiers, IoCs, threat-actor attribution, and
  CVSS scores may now only be cited if supplied by the user, a well-
  established mapping for a pattern clearly present in the input, or the
  result of an actual tool lookup this turn. Unconfirmed items must be
  marked "Identifier Unconfirmed" / "Attribution Unconfirmed" / qualitative
  severity instead of stated as fact. Working exploit code is blocked
  outright. Source: Migration Audit §07/§10/§11, finding "Threat-analysis
  cluster has no fabrication gate on ATT&CK IDs / CVE data / IoCs /
  attribution despite outputs reading as confirmed intelligence."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md. A numeric or
  bare confidence label on a security report is false precision that
  invites treating an unconfirmed finding as verified.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>` and converted the `<thinking>` node under
  `<output_format>` from a mandatory visible block into internal-reasoning
  guidance that is not rendered in the report.
- **[FIX]** Removed persona credential-stacking ("15+ years of experience,"
  "CISSP, OSCP, and GCIH certifications") across all three model variants —
  trimmed to role-relevant expertise; the model cannot actually hold
  certifications and the claim added no analytical value.
- **[GOVERNANCE]** Added explicit disclaimer to every variant's output: not
  a substitute for a full penetration test or licensed security assessment;
  all findings require human security-analyst sign-off. Flagged Amber
  governance gate (see above); this prompt was previously deployed with no
  such gate.

### v1.0 — 2026-03-27 (prior)
- Initial library entry. No fabrication gate on ATT&CK IDs, CVE data, IoCs,
  or attribution. claude-4-6.md carried a bare `<confidence>` footer and
  mandatory chain-of-thought; gemini/gpt-oss variants carried bare
  confidence fields. All three variants opened with unearned credential-
  stacking ("15+ years," CISSP/OSCP/GCIH).

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ No-Fabrication Security Contract present and evaluated for every finding
  ☑ Unconfirmed identifiers/attribution rendered literally, not omitted
  ☑ No numeric confidence score anywhere in the output
  ☑ Disclaimer present: not a substitute for a full penetration test
  ☐ Human security-analyst sign-off obtained before acting on findings
