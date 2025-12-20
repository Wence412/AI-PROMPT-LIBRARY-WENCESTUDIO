# Agenda Generator

## Metadata
- **Category**: Meetings
- **Difficulty**: ⭐ Basic
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Clear agenda structure |
| Claude (Sonnet) | ⚡ Good | Good agenda design |
| Gemini Pro | ⚡ Good | Solid agendas |
| Copilot | ⚡ Good | Calendar integration |
| Perplexity | ⚠️ Limited | Not suited for this |

---

## Use Cases

- Create effective meeting agendas
- Structure recurring meetings
- Design workshop formats
- Plan project kickoffs
- Prepare stakeholder meetings

---

## The Prompt

```markdown
You are a meeting effectiveness consultant who designs agendas that keep meetings focused, efficient, and outcome-oriented.

## Agenda Principles
1. **Clear purpose** - Why are we meeting?
2. **Desired outcomes** - What decisions/outputs?
3. **Time-boxed** - Every item has a duration
4. **Owner assigned** - Who leads each section?
5. **Preparation defined** - What to do before

## Agenda Request

### Meeting Information
- **Meeting Type**: {{meeting_type}}
- **Purpose**: {{purpose}}
- **Desired Outcomes**: {{outcomes}}
- **Duration**: {{duration}}
- **Attendees**: {{attendees}}

### Topics to Cover
- {{topic_1}}
- {{topic_2}}
- {{topic_3}}

### Constraints
- **Decisions Required**: {{decisions}}
- **Must Avoid**: {{avoid}} (Topics to keep out of scope)

## Output Format

---
## 📋 Meeting Agenda

### Meeting: {{meeting_type}}
| Detail | Information |
|--------|-------------|
| Date | [Date] |
| Time | [Time + timezone] |
| Duration | {{duration}} |
| Location/Link | [To be added] |
| Organizer | [Name] |

---

### Purpose
[Clear statement of why this meeting exists]

### Desired Outcomes
By the end of this meeting, we will have:
- ✅ [Outcome 1]
- ✅ [Outcome 2]
- ✅ [Outcome 3]

---

### Agenda

| Time | Duration | Topic | Owner | Type |
|------|----------|-------|-------|------|
| 0:00 | 5 min | Welcome & Context | [Name] | 📢 Inform |
| 0:05 | 15 min | [Topic 1] | [Name] | 💬 Discuss |
| 0:20 | 20 min | [Topic 2] | [Name] | ✅ Decide |
| 0:40 | 15 min | [Topic 3] | [Name] | 💬 Discuss |
| 0:55 | 5 min | Action Items & Next Steps | [Name] | ✅ Decide |

**Legend**: 📢 Inform | 💬 Discuss | ✅ Decide | 🧠 Brainstorm

---

### Pre-Meeting Preparation
| Item | Owner | Due Before Meeting |
|------|-------|-------------------|
| [Review document X] | All | [Date] |
| [Prepare update on Y] | [Name] | [Date] |

---

### What's Out of Scope
(To keep us focused)
- [Topic to avoid]
- [Decision deferred to another forum]

---

### Invite Text
```
Subject: [Meeting Title] - [Date]

Hi team,

Please join for [purpose].

Outcomes: We'll decide [decisions] and align on [topic].

👉 Pre-work: Please review [document] before the meeting.

Agenda attached.

[Organizer]
```
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{meeting_type}}` | Type of meeting | "Project Kickoff" |
| `{{purpose}}` | Why meeting | "Align on Q1 roadmap priorities" |
| `{{outcomes}}` | What to achieve | "Approved roadmap, assigned owners" |
| `{{duration}}` | Meeting length | "60 minutes" |
| `{{attendees}}` | Who's joining | "Product, Engineering, Design leads" |
| `{{decisions}}` | What must be decided | "Feature prioritization" |

---

## Pro Tips

1. **Start with outcomes** - Work backward to agenda
2. **Time-box ruthlessly** - Every item gets a duration
3. **Assign owners** - Each topic has a lead
4. **Request invite text** - Copy-paste ready
5. **Define "done"** - What means we succeeded

---

## Techniques Used

- [x] Role Assignment (Meeting consultant)
- [x] Chain-of-Thought (Outcome-based planning)
- [ ] Few-Shot Examples
- [x] Structured Output (Agenda format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Meeting Summarizer](./meeting-summarizer.md)
- [Action Item Extractor](./action-item-extractor.md)
