# Market Research

## Metadata
- **Category**: Entrepreneurs
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Perplexity | ✅ Optimal | Real-time market data |
| ChatGPT (GPT-4o) | ⚡ Good | Strong analysis framework |
| Gemini Pro | ⚡ Good | Google research integration |
| Claude (Sonnet) | ⚡ Good | Thorough insights |
| Copilot | ⚡ Good | Good for general research |

---

## Use Cases

- Size markets for business plans
- Validate startup ideas
- Identify customer segments
- Research industry trends
- Inform product decisions
- Support funding applications

---

## The Prompt

```markdown
You are a market research analyst with experience in venture capital due diligence and strategic consulting. You combine data-driven analysis with strategic insight.

## Research Methodology
- TAM/SAM/SOM sizing
- Porter's Five Forces
- Customer segmentation
- Trend analysis
- Competitive positioning

## Research Request

### Focus Area
- **Market/Industry**: {{market}}
- **Geographic Scope**: {{geography}}
- **Time Horizon**: {{timeframe}} (Current/1-year/5-year)

### Specific Questions
- {{question_1}}
- {{question_2}}
- {{question_3}}

### Business Context
- **My Product/Service**: {{product}}
- **Target Customer**: {{customer}}
- **Hypothesis to Validate**: {{hypothesis}}

### Output Preferences
- **Depth**: {{depth}} (Quick overview/Standard/Deep dive)
- **Data Priority**: {{data_priority}} (Quantitative/Qualitative/Both)

## Output Format

---
## 📊 Market Research Report: {{market}}

### Executive Summary
[2-3 paragraph overview with key findings]

---

### Market Size
| Segment | Size | Growth Rate | Source |
|---------|------|-------------|--------|
| TAM | $[X] | [X]% CAGR | [Source] |
| SAM | $[X] | [X]% CAGR | [Source] |
| SOM (achievable) | $[X] | [Projection] | [Logic] |

**Sizing Methodology**:
[How these numbers were derived]

---

### Market Dynamics

#### Industry Overview
[Current state of the industry]

#### Porter's Five Forces
| Force | Intensity | Implications |
|-------|-----------|--------------|
| Buyer Power | [H/M/L] | [Impact] |
| Supplier Power | [H/M/L] | [Impact] |
| Competitive Rivalry | [H/M/L] | [Impact] |
| Threat of Substitutes | [H/M/L] | [Impact] |
| Threat of New Entrants | [H/M/L] | [Impact] |

---

### Key Trends
1. **[Trend 1]**: [Description and impact]
2. **[Trend 2]**: [Description and impact]
3. **[Trend 3]**: [Description and impact]

---

### Customer Analysis

#### Segments
| Segment | Size | Growth | Characteristics |
|---------|------|--------|-----------------|
| [Seg 1] | [X%] | [Trend] | [Profile] |
| [Seg 2] | [X%] | [Trend] | [Profile] |

#### Customer Needs
- [Need 1]: [Current solutions and gaps]
- [Need 2]: [Current solutions and gaps]

---

### Competitive Landscape
[Market map description]

| Category | Key Players | Market Share | Notes |
|----------|-------------|--------------|-------|
| [Cat 1] | [Players] | [Share] | [Position] |
| [Cat 2] | [Players] | [Share] | [Position] |

---

### Opportunities & Threats
| Category | Description | Probability | Impact |
|----------|-------------|-------------|--------|
| Opportunity | [Description] | [H/M/L] | [H/M/L] |
| Threat | [Description] | [H/M/L] | [H/M/L] |

---

### Validation of Your Hypothesis
**Hypothesis**: {{hypothesis}}
**Assessment**: [Validated/Partially Validated/Not Supported]
**Evidence**: [Key data points]
**Recommendations**: [Next steps]

---

### Sources & Data Quality
| Source | Type | Recency | Confidence |
|--------|------|---------|------------|
| [Source] | [Type] | [Date] | [H/M/L] |

### Gaps in Research
- [What couldn't be determined]
- [Recommended follow-up research]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{market}}` | Industry/market | "Enterprise HR software" |
| `{{geography}}` | Region scope | "North America" |
| `{{timeframe}}` | Analysis period | "Current + 3-year outlook" |
| `{{product}}` | What you offer | "AI-powered performance review platform" |
| `{{customer}}` | Target buyer | "HR directors at mid-market companies" |
| `{{hypothesis}}` | What to validate | "Mid-market HR teams are underserved by current solutions" |
| `{{depth}}` | Level of detail | "Deep dive" |

---

## Pro Tips

1. **Use Perplexity first** - Get real, cited market data
2. **Validate numbers** - Cross-reference multiple sources
3. **Request sources** - Always ask for citation
4. **Be specific** - "HR software" vs "AI performance review tools for mid-market"
5. **Chain research** - Start broad, then narrow down

---

## Techniques Used

- [x] Role Assignment (Market researcher)
- [x] Chain-of-Thought (Research methodology)
- [ ] Few-Shot Examples
- [x] Structured Output (Research report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Competitor Analysis](./competitor-analysis.md)
- [Business Plan Generator](./business-plan-generator.md)
