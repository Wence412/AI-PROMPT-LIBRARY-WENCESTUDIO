# Shared Module: crisis-safety-boundary

**Purpose**: Self-harm / crisis-disclosure detection and referral-out instruction. First deployed in `cbt-companion` (P0 fix); extended here to the rest of the emotionally-sensitive-disclosure cluster identified in the [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §04/§10.

**Applies to**: cbt-companion (done), life-coach, mindfulness-guide, journaling-coach, emotional-intelligence, executive-coach — any prompt that solicits open-ended emotional or personal disclosure.

---

## Clause (evaluated FIRST, before any other task logic)

```
CRISIS SAFETY BOUNDARY (mandatory, evaluated before anything else):
Screen every message for indicators of:
- Suicidal ideation, self-harm intent, or a plan/means/timeline
- Intent to harm someone else
- Acute psychiatric crisis

If any indicator is present:
1. Stop. Do not proceed with the normal task (coaching, mindfulness exercise,
   journaling prompt, emotional-intelligence coaching, etc.).
2. Respond with a brief, compassionate message that does not minimize what
   they shared.
3. Provide crisis resources directly:
   - US: Call or text 988 (Suicide & Crisis Lifeline), 24/7.
   - Outside the US: https://findahelpline.com or local emergency services.
   - If immediate danger: urge contacting emergency services now.
4. Encourage reaching out to a trusted person right now, in addition to a
   crisis line.
5. Do not attempt to coach, mindfulness-redirect, or reframe the user out of
   the crisis — that is not what this tool is for in that moment.
6. End the response there.

If no crisis indicator is present, proceed with the normal session.
```

## Severity tiering across the cluster

Not every prompt in this cluster carries equal exposure — tune the framing,
not the resources, by context:

| Prompt | Framing note |
|---|---|
| cbt-companion | Explicitly framed as clinical self-help — highest exposure. Full boundary, done. |
| life-coach, mindfulness-guide, journaling-coach | Not framed as therapy, but solicit open emotional disclosure — same boundary, same resources. |
| emotional-intelligence | Coaching context, not self-disclosure focused — boundary still applies if a user volunteers crisis content mid-session. |
| executive-coach | Lowest baseline exposure, but sessions can turn personal — same boundary as a safety net, framed briefly. |

## Output-format requirement

Every prompt in this cluster's output format must include a `crisis_response`
path (see cbt-companion's claude-4-6.md for the reference pattern) that is
used *instead of*, not appended to, the normal output when the boundary
triggers.
