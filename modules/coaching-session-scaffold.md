# Shared Module: coaching-session-scaffold

**Purpose**: One parameterized session template replacing five near-duplicate coaching structures, per [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §07/§10.

**Applies to**: career-coach, executive-coach, life-coach, habit-formation, interview-coach — all structurally "session-plan output" with a different focus label and framework.

---

## Parameters

```
{{framework}}      — the coaching methodology in play (GROW / PERMA / SFBT /
                      Motivational Interviewing / ICF competencies / habit-
                      loop model / STAR interview method)
{{domain_focus}}    — what the session is actually about (career transition,
                      executive leadership, general life goals, habit change,
                      interview preparation)
```

## Shared session shape

```
### Session Opening
[Empathetic framing of what the user brought, grounded in what they actually said]

### {{framework}} Application
[Apply the named framework's stages/questions to {{domain_focus}} — this is
the section that differs most between the five prompts and should stay
prompt-specific, not shared]

### Reflection / Discovery Questions
[2-4 open questions specific to {{domain_focus}}]

### Action Step(s)
[One to three concrete, small next actions — not an overwhelming list]

### Accountability / Follow-up
[How progress will be checked next session]
```

## What stays prompt-specific (do not over-consolidate)

The audit is explicit that this is a **shared-module opportunity, not a
merge candidate** — the five prompts solve genuinely different problems.
Keep prompt-specific:
- The named framework and its stage labels
- Domain vocabulary (career vs. habit vs. interview)
- Any prompt-specific safety notes (see `crisis-safety-boundary` for
  life-coach; interview-coach and career-coach carry lower emotional-
  disclosure risk and don't need the full crisis module, just standard
  `hallucination-guard` on any claims about job-market data or salary figures)

## Persona-inflation trim (apply alongside this module)

Per audit §08, several prompts in this cluster carry credential-stacking
personas beyond what the task needs (e.g. "20+ years, ICF Master Certified"
executive-coach; similar patterns elsewhere). Trim to role-relevant expertise
only — a coach persona doesn't need a CV, it needs credibility appropriate to
a self-help/coaching tool, not a claim of professional certification the
model doesn't actually hold.
