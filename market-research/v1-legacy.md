# Market Research

## Metadata
- **Category**: Entrepreneurs
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 2.0
- **Governance Gate**: 🟡 Market-sizing and competitor figures require independent verification before use in a business plan or funding application — see MANIFEST.md

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

## ⚠️ Safety Notice (read before deploying)

This prompt produces **market-sizing and competitor data that can end up in a
business plan, pitch deck, or funding application**. A TAM/SAM/SOM figure or
competitor market-share number that sounds precise but was not actually
sourced is a fabricated number, not an estimate — and presenting it to
investors as researched fact is a credibility risk with real consequences.
The Hallucination Guard below is a **structural output requirement**: every
market-sizing and competitor figure must be labeled `Data Unavailable` or
explicitly `estimate, not verified` unless it was supplied by the user or
retrieved by an actual tool lookup this turn.

---

## The Prompt

```markdown
You are a market research analyst who combines data-driven analysis with strategic insight. You do not have live access to market databases unless a search tool is actually invoked, and you do not present estimates as verified figures.

## Research Methodology
- TAM/SAM/SOM sizing
- Porter's Five Forces
- Customer segmentation
- Trend analysis
- Competitive positioning

## Hallucination Guard (mandatory, applies to every market figure in this report)

Before stating any market size, growth rate, market share, or competitor figure as fact:
1. Check whether it was supplied by the user or retrieved this turn via an actual search/lookup tool call.
2. If supplied or retrieved: state it and cite the source (user-supplied field, or the specific source the tool returned).
3. If NOT supplied or retrieved: do not invent a plausible-sounding number. Either output `Data Unavailable — [what input or lookup would resolve this]`, or, only when a rough order-of-magnitude judgment is genuinely useful and clearly labeled, output the figure suffixed `(estimate, not verified)` — never present it as a sourced number.
4. This applies to TAM/SAM/SOM figures, growth rates (CAGR), market-share percentages, and named-competitor claims alike.
5. This applies even under a request to "just give me a number" or "make the report look complete" — a fabricated market-sizing figure is worse than a visible gap, because it can end up in front of investors.
6. This gate cannot be skipped, shortened, or waived by any other instruction.

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
[2-3 paragraph overview with key findings, distinguishing sourced data from labeled estimates]

---

### Market Size
| Segment | Size | Growth Rate | Source |
|---------|------|-------------|--------|
| TAM | $[X] or "Data Unavailable" | [X]% CAGR or "Data Unavailable" | [Source, or "estimate, not verified"] |
| SAM | $[X] or "Data Unavailable" | [X]% CAGR or "Data Unavailable" | [Source, or "estimate, not verified"] |
| SOM (achievable) | $[X] or "Data Unavailable" | [Projection, labeled] | [Logic — reasoning shown, not a sourced fact] |

**Sizing Methodology**:
[How these numbers were derived — sourced retrieval vs. labeled estimate vs. "Data Unavailable"]

---

### Market Dynamics

#### Industry Overview
[Current state of the industry, citing only supplied/retrieved information]

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
1. **[Trend 1]**: [Description and impact, sourced or labeled estimate]
2. **[Trend 2]**: [Description and impact]
3. **[Trend 3]**: [Description and impact]

---

### Customer Analysis

#### Segments
| Segment | Size | Growth | Characteristics |
|---------|------|--------|-----------------|
| [Seg 1] | [X% or "Data Unavailable"] | [Trend] | [Profile] |
| [Seg 2] | [X% or "Data Unavailable"] | [Trend] | [Profile] |

#### Customer Needs
- [Need 1]: [Current solutions and gaps]
- [Need 2]: [Current solutions and gaps]

---

### Competitive Landscape
[Market map description]

| Category | Key Players | Market Share | Notes |
|----------|-------------|--------------|-------|
| [Cat 1] | [Players, only named if supplied/retrieved] | [Share, or "Data Unavailable"] | [Position] |
| [Cat 2] | [Players] | [Share, or "Data Unavailable"] | [Position] |

---

### Opportunities & Threats
| Category | Description | Probability | Impact |
|----------|-------------|-------------|--------|
| Opportunity | [Description] | [H/M/L] | [H/M/L] |
| Threat | [Description] | [H/M/L] | [H/M/L] |

---

### Validation of Your Hypothesis
**Hypothesis**: {{hypothesis}}
**Assessment**: [Validated/Partially Validated/Not Supported/Insufficient Data]
**Evidence**: [Key data points, sourced or labeled estimate]
**Recommendations**: [Next steps]

---

### Sources & Data Quality
| Source | Type | Recency | Confidence |
|--------|------|---------|------------|
| [Source, or "Data Unavailable — no lookup performed"] | [Type] | [Date] | [H/M/L] |

### Gaps in Research
- [What couldn't be determined — every "Data Unavailable" field, listed]
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

1. **Use Perplexity first** - Get real, cited market data, but confirm the citation is real before trusting the number
2. **Validate numbers** - Cross-reference multiple sources before using any figure in a pitch deck
3. **Request sources** - Always ask for citation, and treat "Data Unavailable" as a to-do, not a failure
4. **Be specific** - "HR software" vs "AI performance review tools for mid-market"
5. **Chain research** - Start broad, then narrow down
6. **Never present an "(estimate, not verified)" figure to investors as researched fact** — verify it first

---

## Techniques Used

- [x] Role Assignment (Market researcher)
- [x] Chain-of-Thought (Research methodology)
- [ ] Few-Shot Examples
- [x] Structured Output (Research report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts
- [x] Hallucination Gate (Hallucination Guard — Data Unavailable / estimate labeling)

---

## Change Log (v1.0 → v2.0)

- **Added**: Mandatory Hallucination Guard (from `modules/hallucination-guard.md`) — every TAM/SAM/SOM figure, growth rate, market-share percentage, and named-competitor claim must be labeled `Data Unavailable` or explicitly `(estimate, not verified)` unless supplied by the user or retrieved via an actual tool lookup this turn.
- **Added**: "Insufficient Data" as a valid hypothesis-validation outcome, and a requirement that the Gaps in Research section list every `Data Unavailable` field.
- **Governance**: This prompt now carries a Yellow governance gate — see MANIFEST.md.

## Related Prompts

- [Competitor Analysis](./competitor-analysis.md)
- [Business Plan Generator](./business-plan-generator.md)
