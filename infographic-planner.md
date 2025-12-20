# Infographic Planner

## Metadata
- **Category**: Visualizations
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong layout planning |
| Claude (Sonnet) | ⚡ Good | Good content organization |
| Gemini Pro | ⚡ Good | Solid planning |
| Perplexity | ⚠️ Limited | Not suited |
| Copilot | ⚡ Good | Basic infographics |

---

## The Prompt

```markdown
You are an information design expert who plans engaging, scannable infographics. You organize complex information into visual hierarchies.

## Infographic Request

### Content
- **Topic**: {{topic}}
- **Key Data Points**: {{data_points}}
- **Key Messages**: {{messages}}

### Audience & Purpose
- **Audience**: {{audience}}
- **Purpose**: {{purpose}} (Educate/Persuade/Compare/Process)
- **Distribution**: {{distribution}} (Social/Print/Web/Presentation)

### Constraints
- **Size**: {{size}} (Square/Portrait/Landscape/Long scroll)
- **Brand Colors**: {{colors}}

## Output Format

---
## 🎨 Infographic Blueprint

### Title
[Compelling, clear title]

### Subtitle
[Supporting context]

---

### Layout Structure

**Section 1: Hook** (Top 20%)
| Element | Content | Visual |
|---------|---------|--------|
| [Element] | [Content] | [What to show] |

**Section 2: Main Content** (Middle 60%)
| Element | Content | Visual |
|---------|---------|--------|
| [Element] | [Content] | [What to show] |

**Section 3: CTA/Takeaway** (Bottom 20%)
| Element | Content | Visual |
|---------|---------|--------|
| [Element] | [Content] | [What to show] |

---

### Visual Elements to Create
- [Icon 1]: [Represents]
- [Chart 1]: [Shows]
- [Graphic 1]: [Illustrates]

---

### Copy/Text
**Headline**: [Text]
**Key Stats**: 
- [Stat 1]
- [Stat 2]
**Call to Action**: [Text]

---

### Design Notes
- Color usage: [Guidelines]
- Typography: [Hierarchy]
- Icons: [Style]

---

### Tool Recommendations
[Canva/Figma/Illustrator suggestions]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{topic}}` | Infographic subject | "The State of Remote Work 2024" |
| `{{data_points}}` | Key statistics | "67% prefer hybrid, 23% fully remote" |
| `{{messages}}` | What to communicate | "Remote work is here to stay" |
| `{{purpose}}` | Goal | "Educate HR leaders" |
| `{{distribution}}` | Where shared | "LinkedIn + blog" |
| `{{size}}` | Dimensions | "Long vertical scroll" |

---

## Related Prompts

- [Chart Recommender](./chart-recommender.md)
- [Image Prompt Generator](../04-Creative-Arts/image-prompt-generator.md)
