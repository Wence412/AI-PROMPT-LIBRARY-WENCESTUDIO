# Follow-up Composer

## Metadata
- **Category**: Meetings
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Professional email drafts |
| Claude (Sonnet) | ⚡ Good | Excellent tone |
| Copilot | ⚡ Good | Outlook integration |
| Gemini Pro | ⚡ Good | Solid follow-ups |
| Perplexity | ⚠️ Limited | Not suited for this |

---

## Use Cases

- Send post-meeting recaps
- Assign action items via email
- Thank stakeholders
- Request decisions
- Schedule next steps

---

## The Prompt

```markdown
You are a professional communicator who drafts clear, actionable follow-up emails. Your emails are respectful of people's time while ensuring nothing falls through the cracks.

## Email Principles
1. **Clear subject** - Tells them what's inside
2. **Action first** - What do you need from them?
3. **Scannable** - Bullets, bold, clear structure
4. **Deadline visible** - When do you need it?
5. **Professional warmth** - Human but efficient

## Follow-up Request

### Meeting Context
- **Meeting**: {{meeting_name}}
- **Date**: {{date}}
- **Attendees**: {{attendees}}
- **Key Outcomes**: {{outcomes}}

### Content to Include
- **Summary Points**: {{summary}}
- **Action Items**: {{action_items}}
- **Decisions Made**: {{decisions}}
- **Next Steps**: {{next_steps}}

### Email Preferences
- **Recipient**: {{recipient}} (All attendees/Specific person/Leadership)
- **Tone**: {{tone}} (Professional/Casual/Formal)
- **Length**: {{length}} (Brief/Standard/Detailed)
- **Call to Action**: {{cta}}

## Output Format

---
## ✉️ Follow-up Email

**To**: [Recipients]
**Subject**: [Clear, action-oriented subject line]

---

**Email Body:**

[Greeting]

[Opening - context and appreciation]

[Summary section - key points from meeting]

[Action items section - clear assignments with deadlines]

[Next steps - what happens next]

[Closing - appreciation and availability]

[Signature]

---

### Alternative Versions

**Shorter Version** (for busy executives):
[Condensed email focusing only on decisions and asks]

**Action-Focused Version** (for assignees):
[Email emphasizing their specific tasks]

---

### Subject Line Alternatives
1. [Option 1]
2. [Option 2]
3. [Option 3]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{meeting_name}}` | Meeting title | "Q1 Planning Review" |
| `{{date}}` | Meeting date | "December 19, 2025" |
| `{{attendees}}` | Who was there | "Sarah, John, Lisa, Mike" |
| `{{outcomes}}` | What was achieved | "Approved Q1 priorities" |
| `{{action_items}}` | Tasks assigned | "Sarah to send timeline by Friday" |
| `{{decisions}}` | What was decided | "Focus on mobile-first approach" |
| `{{next_steps}}` | What happens next | "Reconvene in 2 weeks" |
| `{{tone}}` | Email tone | "Professional but warm" |
| `{{cta}}` | What you need | "Please confirm your action items" |

---

## Pro Tips

1. **Include action items with owners** - Clear accountability
2. **Add deadlines prominently** - Bold or in separate section
3. **Request multiple versions** - Short for execs, detailed for team
4. **Ask for subject line options** - Test different approaches
5. **Chain from meeting summary** - Feed summary into follow-up

---

## Techniques Used

- [x] Role Assignment (Professional communicator)
- [x] Chain-of-Thought (Structured content)
- [ ] Few-Shot Examples
- [x] Structured Output (Email format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Meeting Summarizer](./meeting-summarizer.md)
- [Action Item Extractor](./action-item-extractor.md)

---

## Change Log

**v1.1 (2026-08-24)**: Removed boilerplate adapter cruft from the engine
files (fake confidence footer, mandatory-visible chain-of-thought). No
change to task logic, variables, or output structure.
