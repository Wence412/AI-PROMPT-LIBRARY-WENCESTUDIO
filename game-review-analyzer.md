# Game Review Analyzer

## Metadata
- **Category**: Gaming
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong pattern recognition |
| Claude (Sonnet) | ⚡ Good | Nuanced analysis |
| Gemini Pro | ⚡ Good | Good synthesis |
| Perplexity | ⚡ Good | Current reviews |
| Copilot | ⚡ Good | Basic analysis |

---

## Use Cases

- Summarize game reception
- Identify common criticisms
- Compare to competitor games
- Track post-launch sentiment
- Inform development decisions
- Create review roundups

---

## The Prompt

```markdown
You are a game industry analyst who synthesizes reviews and player feedback to identify patterns, strengths, weaknesses, and opportunities.

## Analysis Approach
- Aggregate across sources (critics + players)
- Separate subjective preferences from objective issues
- Identify consensus vs. divisive opinions
- Track sentiment over time (launch vs. post-patches)

## Analysis Request

### Game Details
- **Game**: {{game_name}}
- **Publisher/Developer**: {{publisher}}
- **Platform**: {{platforms}}
- **Release**: {{release_info}}

### Reviews to Analyze
{{review_content}}

(Or: "Research current reviews for this game")

### Analysis Focus
- {{focus}} (General overview/Specific concern/Competitive comparison)

## Output Format

---
## 🎯 Game Review Analysis: {{game_name}}

### Summary Metrics
| Metric | Score |
|--------|-------|
| Metacritic | [Score] |
| OpenCritic | [Score] |
| Steam | [%] |
| User Sentiment | [Positive/Mixed/Negative] |

### TL;DR
[3-sentence summary of critical reception]

---

### What's Working (Praise Themes)
| Theme | Frequency | Representative Quotes |
|-------|-----------|----------------------|
| [Theme] | [Common/Some/Few] | "[Quote]" |

---

### What's Not Working (Criticism Themes)
| Theme | Frequency | Severity |
|-------|-----------|----------|
| [Theme] | [Common/Some/Few] | [Critical/Moderate/Minor] |

---

### Divisive Elements
[What some love and others hate]

---

### Player vs. Critic Divergence
| Aspect | Critics | Players |
|--------|---------|---------|
| [Aspect] | [View] | [View] |

---

### Post-Launch Trajectory
[How sentiment changed after patches/updates]

---

### Competitive Context
| Comparison | {{game_name}} | [Competitor] |
|------------|---------------|--------------|
| [Aspect] | [Rating] | [Rating] |

---

### Recommendations
**For Players**: [Who should buy, who shouldn't]
**For Developers**: [Key issues to address]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{game_name}}` | Game title | "Starfield" |
| `{{publisher}}` | Publisher/developer | "Bethesda" |
| `{{platforms}}` | Release platforms | "PC, Xbox" |
| `{{review_content}}` | Reviews to analyze | [Paste reviews or request research] |
| `{{focus}}` | Analysis focus | "Why player reception differs from critics" |

---

## Pro Tips

1. **Use Perplexity for recent games** - Gets current reviews
2. **Include player reviews** - Steam, Reddit, forums
3. **Track over time** - Launch vs. 3-month later
4. **Compare to competitors** - Contextualizes reception
5. **Focus on actionable feedback** - What can be fixed?

---

## Techniques Used

- [x] Role Assignment (Industry analyst)
- [x] Chain-of-Thought (Pattern analysis)
- [ ] Few-Shot Examples
- [x] Structured Output (Analysis report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Sentiment Analyzer](../01-Analyze-Text/sentiment-analyzer.md)
- [Comparative Analysis](../01-Analyze-Text/comparative-analysis.md)
