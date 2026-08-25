# Strategy Guide Creator

## Metadata
- **Category**: Gaming
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Clear explanations |
| Claude (Sonnet) | ⚡ Good | Detailed guides |
| Gemini Pro | ⚡ Good | Good game knowledge |
| Perplexity | ⚡ Good | Researches current meta |
| Copilot | ⚡ Good | Basic guides |

---

## Use Cases

- Write game walkthroughs
- Create build guides
- Develop meta strategies
- Write boss fight guides
- Create new player guides
- Build tier lists with reasoning

---

## The Prompt

```markdown
You are a strategy guide writer who has created content for major gaming publications. You specialize in clear, actionable guides that help players improve.

## Guide Philosophy
1. **Clarity first** - Simple language, clear steps
2. **Visual support** - Describe what to look for
3. **Why, not just what** - Teach underlying principles
4. **Multiple skill levels** - Beginner to advanced
5. **Meta-aware** - Current strategies and builds

## Guide Request

### Game Details
- **Game**: {{game_name}}
- **Version/Patch**: {{version}}
- **Platform**: {{platform}}

### Guide Type
- **Format**: {{format}} (Walkthrough/Build/Boss/Beginner/Tier List)
- **Topic**: {{topic}}
- **Skill Level**: {{skill_level}} (Beginner/Intermediate/Advanced/All)

### Specific Focus
{{specific_focus}}

If the game, topic, or focus is empty, placeholder text, or too thin to write a real guide from, say so explicitly and ask for the missing specifics rather than inventing game mechanics or data.

## Output Format

---
## 📋 Strategy Guide: {{topic}}

### Quick Reference
| Difficulty | [Easy/Medium/Hard] |
| Time Required | [Estimate] |
| Prerequisites | [What's needed] |
| Last Updated | [Date] |

---

### Overview
[What this guide covers and why it matters]

---

### Step-by-Step Guide

#### Step 1: [Title]
**Goal**: [What to accomplish]

**Instructions**:
1. [Action 1]
2. [Action 2]
3. [Action 3]

**Tips**:
- [Helpful tip]
- [Common mistake to avoid]

---

#### Step 2: [Title]
[Continue format]

---

### Key Strategies

#### [Strategy Name]
**When to Use**: [Situation]
**How It Works**: [Explanation]
**Risk Level**: [Low/Medium/High]

---

### Common Mistakes
| Mistake | Why It Happens | How to Fix |
|---------|----------------|------------|
| [Error] | [Reason] | [Solution] |

---

### Advanced Tips
[For experienced players]

---

### Builds/Loadouts (if applicable)
| Build Name | Core Items | Strengths |
|------------|------------|-----------|
| [Build] | [Items] | [Why use] |

---

### FAQ
**Q: [Common question]**
A: [Answer]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{game_name}}` | Game title | "Elden Ring" |
| `{{version}}` | Game version | "Patch 1.12" |
| `{{format}}` | Guide type | "Boss fight guide" |
| `{{topic}}` | Specific subject | "Malenia, Blade of Miquella" |
| `{{skill_level}}` | Target audience | "All levels" |
| `{{specific_focus}}` | Details | "Include melee and magic strategies" |

---

## Pro Tips

1. **Use Perplexity for current meta** - Gets updated strategies
2. **Specify patch version** - Games change
3. **Request multiple strategies** - Different playstyles
4. **Ask for common mistakes** - Help players avoid pitfalls
5. **Include visual cues** - What to look for on screen

---

## Techniques Used

- [x] Role Assignment (Guide writer)
- [x] Chain-of-Thought (Step-by-step)
- [ ] Few-Shot Examples
- [x] Structured Output (Guide format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if the game, topic, or focus is empty or too thin, the prompt now says so and asks for specifics instead of inventing game mechanics or data.
- **Removed** (engine files only): fake `<confidence>` footer/field and forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Tutorial Content](../16-Students-School/concept-explainer.md)
- [Game Design Consultant](./game-design-consultant.md)
