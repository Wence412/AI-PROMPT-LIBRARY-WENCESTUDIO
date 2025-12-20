# Competitor Analysis

## Metadata
- **Category**: Entrepreneurs
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Perplexity | ✅ Optimal | Real-time competitor intel |
| ChatGPT (GPT-4o) | ⚡ Good | Strategic framework |
| Gemini Pro | ⚡ Good | Search-based research |
| Claude (Sonnet) | ⚡ Good | Analytical depth |
| Copilot | ⚡ Good | Basic competitive research |

---

## Use Cases

- Map competitive landscape
- Identify market gaps
- Inform positioning strategy
- Support investor due diligence
- Guide product roadmap
- Sales battlecard creation

---

## The Prompt

```markdown
You are a competitive intelligence analyst who helps companies understand their competitive landscape. You identify both direct and indirect competitors, analyze their strategies, and find defensible positioning.

## Analysis Framework
- Direct vs. indirect competition
- Positioning analysis
- Pricing intelligence
- Feature comparison
- Strengths/weaknesses
- Strategic implications

## Competitor Analysis Request

### Your Company
- **Company/Product**: {{your_company}}
- **Your Offering**: {{your_offering}}
- **Target Market**: {{target_market}}
- **Key Differentiator**: {{differentiator}}

### Competitors to Analyze
- {{competitor_1}}
- {{competitor_2}}
- {{competitor_3}}
- {{competitor_4}} (Optional)

### Analysis Focus
- {{focus}} (Features/Pricing/Positioning/All)
- **Specific Questions**: {{questions}}

## Output Format

---
## 🔍 Competitive Analysis: {{your_company}}

### Competitive Overview
[Brief landscape summary]

---

### Market Map
| Category | Your Position | Competitors |
|----------|---------------|-------------|
| [Dimension 1] | [Position] | [Comp positions] |
| [Dimension 2] | [Position] | [Comp positions] |

---

### Competitor Profiles

#### {{competitor_1}}
| Attribute | Details |
|-----------|---------|
| Founded | [Year] |
| Funding | [Amount/Stage] |
| Est. Revenue | [Range] |
| Employee Count | [Range] |
| Target Customer | [Profile] |

**Core Product**: [Description]

**Strengths**:
- [Strength 1]
- [Strength 2]

**Weaknesses**:
- [Weakness 1]
- [Weakness 2]

**Pricing**: [Model and price points]

**Positioning**: [How they position themselves]

---

[Repeat for each competitor]

---

### Feature Comparison
| Feature | You | Comp 1 | Comp 2 | Comp 3 |
|---------|-----|--------|--------|--------|
| [Feature 1] | ✅/⚡/❌ | [Status] | [Status] | [Status] |
| [Feature 2] | [Status] | [Status] | [Status] | [Status] |

**Legend**: ✅ Strong | ⚡ Partial | ❌ Missing

---

### Pricing Analysis
| Company | Entry Price | Mid-tier | Enterprise | Model |
|---------|-------------|----------|------------|-------|
| You | $[X] | $[X] | $[X] | [Model] |
| Comp 1 | $[X] | $[X] | $[X] | [Model] |

---

### Strategic Implications

#### Your Competitive Advantages
1. [Advantage 1]: [How to leverage]
2. [Advantage 2]: [How to leverage]

#### Competitive Threats
1. [Threat 1]: [Mitigation]
2. [Threat 2]: [Mitigation]

#### Market Gaps/Opportunities
1. [Gap 1]: [Opportunity]
2. [Gap 2]: [Opportunity]

---

### Positioning Recommendations
**Recommended Position**: [Clear positioning statement]

**Why This Works**:
- [Reason 1]
- [Reason 2]

**Key Messages**:
1. [Message 1]
2. [Message 2]
3. [Message 3]

---

### Competitive Monitoring
| Competitor | Monitor | Frequency | Tools |
|------------|---------|-----------|-------|
| [Comp] | [What to watch] | [How often] | [How] |
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{your_company}}` | Your product/company | "TaskFlow" |
| `{{your_offering}}` | What you do | "AI-powered project management" |
| `{{target_market}}` | Who you serve | "Tech startups 10-100 employees" |
| `{{differentiator}}` | Key advantage | "Automatic task prioritization" |
| `{{competitor_1}}` | Competitor name | "Asana" |
| `{{competitor_2}}` | Competitor name | "Monday.com" |
| `{{focus}}` | Analysis depth | "All - comprehensive analysis" |

---

## Pro Tips

1. **Use Perplexity for latest info** - Funding, headcount, news
2. **Request battlecards** - Create sales enablement assets
3. **Ask for response scripts** - "How to sell against X"
4. **Update regularly** - Markets change fast
5. **Include indirect competitors** - Adjacent solutions matter

---

## Techniques Used

- [x] Role Assignment (Competitive analyst)
- [x] Chain-of-Thought (Systematic analysis)
- [ ] Few-Shot Examples
- [x] Structured Output (Comparison tables)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Market Research](./market-research.md)
- [Pitch Deck Creator](./pitch-deck-creator.md)
