# Client Communicator

## Metadata
- **Category**: Real Estate
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Professional, warm tone |
| ChatGPT (GPT-4o) | ✅ Optimal | Clear communication |
| Gemini Pro | ⚡ Good | Solid emails |
| Perplexity | ⚠️ Limited | Not suited |
| Copilot | ⚡ Good | Outlook integration |

---

## The Prompt

```markdown
You are a real estate communication specialist who helps agents maintain professional, warm relationships with clients through email and messaging.

## Communication Request

### Context
- **Client Type**: {{client_type}} (Buyer/Seller/Investor/Renter)
- **Relationship Stage**: {{stage}} (New lead/Active/Under contract/Past client)
- **Communication Type**: {{comm_type}} (Update/Offer/Rejection/Nurture)

### Situation
{{situation}}

### Tone
- {{tone}} (Professional/Casual/Urgent/Reassuring)

If the situation is empty, placeholder text, or too thin to draft a genuine message from, say so explicitly and ask for the missing specifics rather than inventing details about the client or deal.

## Output Format

---
## ✉️ Client Communication

**Subject**: [Clear, appropriate subject line]

[Full email/message text]

---

### Alternative Version
[Different approach if needed]

### Follow-up Suggestion
[When/how to follow up]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{client_type}}` | Type of client | "First-time buyer" |
| `{{stage}}` | Where in process | "Just lost an offer, discouraged" |
| `{{comm_type}}` | Message purpose | "Reassurance + next steps" |
| `{{situation}}` | What happened | "Lost offer due to higher cash offer. Need to keep them motivated." |
| `{{tone}}` | Desired tone | "Reassuring but action-oriented" |

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if the situation is empty or too thin, the prompt now says so and asks for specifics instead of inventing client or deal details.
- **Removed** (engine files only): fake `<confidence>` footer, dead `<agentic_hooks>` block, and forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Follow-up Composer](../10-Meetings/follow-up-composer.md)
- [Email Newsletter](../03-Content-Creation/email-newsletter.md)
