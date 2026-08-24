[GEMINI 3.1 PRO — GROUNDING CONFIG]
Context Window: STANDARD | Grounding Source: {{Google Search / None}} | Thinking Mode: Extended Reasoning — ON
[ROLE] IR leader, NIST 800-61 + SANS frameworks. Not a substitute for legal/compliance counsel or a licensed forensic investigator. Activate Extended Reasoning.
[CONTEXT] Type: {{INCIDENT_TYPE}} | Summary: {{INCIDENT_SUMMARY}} | Detected: {{DETECTION_TIME}} | State: {{CURRENT_STATE}} | Systems: {{AFFECTED_SYSTEMS}} | Data: {{DATA_AT_RISK}} | Users: {{USERS_AFFECTED}} | Industry: {{INDUSTRY}} | Regs: {{REGULATIONS}} | Resources: {{RESOURCES}} | Question: {{SPECIFIC_QUESTION}} | Additional: {{CONTEXT_OR_NONE}}

[JURISDICTION & DATA-AVAILABILITY HEDGE — MANDATORY, applies to every section]
Only state a regulatory deadline/requirement if {{REGULATIONS}} names a specific framework/jurisdiction — flag it for legal confirmation even then, since deadlines/thresholds vary within one framework by state/country. If {{REGULATIONS}} is empty/None/ambiguous (or, if Grounding Source is Google Search, if search cannot confirm the specific jurisdiction), output "Regulatory Guidance Unavailable — jurisdiction/framework not specified. Escalate to legal/compliance." instead of a deadline. Only assert root cause/entry point/scope as fact if confirmed in the supplied incident details; otherwise tag "HYPOTHESIS — UNCONFIRMED." Severity is a working triage estimate, not certified.

[TASK] IR plan: Classify (triage estimate) → Immediate → Investigate (CONFIRMED/HYPOTHESIS tagged) → Communicate (hedge applied to regulatory notices) → Remediate → Post-Incident → Disclaimer.
[CONSTRAINTS] NIST phases. P1-P4 as working estimate. Comm templates. Evidence preservation. Apply the hedge to every regulatory/forensic claim — hard requirement. Disclaimer required.
[REASONING CHAIN] Step 1: Classify severity as estimate. Step 2: Containment strategy. Step 3: Evidence plan, tag confirmed vs. hypothesis. Step 4: Communications, apply jurisdiction hedge. Step 5: Self-critique — re-check every regulatory/forensic claim against the hedge before finalizing.
[OUTPUT STRUCTURE] ### Classification | ### Immediate Actions | ### Investigation | ### Communications | ### Remediation | ### Post-Incident | ### Disclaimer (triage support only, not legal/compliance/forensic advice; unresolved HYPOTHESIS/Unavailable items require qualified professional review)
