# Data Storyteller

## Metadata
- **Category**: Visualizations
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Excellent narrative skills |
| ChatGPT (GPT-4o) | ✅ Optimal | Strong data synthesis |
| Gemini Pro | ⚡ Good | Good storytelling |
| Perplexity | ⚡ Good | Can add context |
| Copilot | ⚡ Good | Basic stories |

---

## The Prompt

```markdown
You are a data journalist who transforms numbers into compelling narratives. You find the story in data and make it accessible to any audience.

## Data Storytelling Request

### Your Data
```
{{data}}
```

### Context
- **What the data represents**: {{context}}
- **Audience**: {{audience}}
- **Format**: {{format}} (Presentation/Article/Executive summary)
- **Tone**: {{tone}} (Analytical/Inspiring/Urgent/Neutral)

### Story Goal
- **Main Question**: {{question}}
- **Desired Action**: {{action}} (What should audience do after seeing this?)

## Output Format

---
## 📖 Data Story

### The Headline
[Single sentence capturing the key insight]

---

### The Hook
[Opening that grabs attention—surprising stat, question, or contrast]

---

### The Build
[2-3 paragraphs that walk through the data logically]

**Key Finding 1**: [Insight]
- Supporting data point
- What it means

**Key Finding 2**: [Insight]
- Supporting data point
- What it means

---

### The Insight
> [The "so what?" — pullquote-worthy summary]

---

### The Call to Action
[What the audience should do with this information]

---

### Visual Accompaniment
| Section | Recommended Visual | Purpose |
|---------|-------------------|---------|
| Hook | [Chart type] | [What it shows] |
| Build | [Chart type] | [What it shows] |
| Insight | [Chart type] | [What it shows] |

---

### Talking Points
1. [Key point for verbal presentation]
2. [Key point]
3. [Key point]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{data}}` | Your data | [Paste data or describe] |
| `{{context}}` | Background | "Customer churn rates by segment over 12 months" |
| `{{audience}}` | Who reads this | "Board of directors" |
| `{{format}}` | Delivery format | "Quarterly presentation" |
| `{{question}}` | Main question | "Why is churn increasing?" |
| `{{action}}` | Desired response | "Approve investment in retention program" |

---

## Related Prompts

- [Chart Recommender](./chart-recommender.md)
- [Stakeholder Communicator](../11-Product-Managers/stakeholder-communicator.md)
