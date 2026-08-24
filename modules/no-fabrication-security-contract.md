# Shared Module: no-fabrication-security-contract

**Purpose**: Shared instruction blocking invented ATT&CK IDs / CVE data / IoCs / attribution when evidence is thin, per [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §07/§10/§11.

**Applies to**: security-audit, threat-analyzer, vulnerability-assessment — all three explicitly cross-link each other and share one report skeleton, but none currently blocks the model from inventing specifics.

---

## Clause (mandatory, applies to every finding/classification in the report)

```
NO-FABRICATION SECURITY CONTRACT (mandatory):
For every finding, classification, or reference in this report:
- MITRE ATT&CK technique IDs, CVE/CWE identifiers, and IoCs may only be
  cited if they were supplied by the user, are a well-established mapping
  for a pattern clearly present in the supplied input, or the tool has
  search/lookup access and actually performed the lookup this turn.
- Do not invent a technique ID, CVE number, or IoC to make a finding look
  more complete. If the specific identifier is not confirmed, describe the
  finding in plain language and mark the identifier field
  "Identifier Unconfirmed — verify against [ATT&CK Navigator / NVD / vendor
  advisory] before citing."
- Do not assign attribution (threat actor, campaign name) unless it was
  supplied or is directly evidenced by IoCs in the input. Otherwise: "
  Attribution Unconfirmed."
- CVSS scores: only state a score if it was supplied or can be computed
  from CVSS vector components actually present in the input. Otherwise:
  "Severity: [Critical/High/Medium/Low] (qualitative estimate — CVSS not
  computed, insufficient vector data)."
- Do not provide working exploit code for any finding, regardless of
  severity — describe exploitability in one paragraph instead.
```

## Where this differs by prompt

| Prompt | Trigger context | Emphasis |
|---|---|---|
| security-audit | Code/config audit | CWE references for code-level findings; CVSS discipline |
| threat-analyzer | Incident/TTP analysis | MITRE ATT&CK ID discipline; attribution discipline (highest risk of over-claiming) |
| vulnerability-assessment | CVE/patch-specific | CVE/CVSS discipline; patch-availability claims must also be flagged unconfirmed if not verified |

## Governance note

Per audit §11, this cluster's outputs read as complete security audits if
presented without qualification, which is a false-negative risk (a report
that looks thorough but silently omits unconfirmed items reads as "clean").
Every report generated with this module must carry the disclaimer: "This is
not a substitute for a full penetration test or a licensed security
assessment. All findings require human security-analyst sign-off before
being treated as a complete picture of risk."
