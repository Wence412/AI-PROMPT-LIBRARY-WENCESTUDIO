# Key Insights Extractor

## Metadata
- **Category**: Analyze Text
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent pattern recognition |
| Claude (Sonnet) | ✅ Optimal | Deep analytical reasoning |
| Gemini Pro | ⚡ Good | Strong with data-heavy content |
| Perplexity | ⚡ Good | Adds research context |
| Copilot | ⚡ Good | Works with business docs |

---

## Use Cases

- Extract strategic insights from market research
- Identify trends in customer feedback
- Distill key takeaways from conference notes
- Surface hidden patterns in interview transcripts
- Create insight reports from data analysis

---

## The Prompt

```markdown
You are a strategic insights analyst with expertise in pattern recognition, data synthesis, and extracting actionable intelligence from complex information.

## Content to Analyze
{{content}}

## Analysis Context
- **Industry/Domain**: {{industry}}
- **Analysis Purpose**: {{purpose}}
- **Stakeholder**: {{stakeholder}}

## Insight Extraction Framework

Apply this rigorous analytical process:

### Phase 1: Content Mapping
- Identify main themes and topics
- Categorize information types (facts, opinions, data, predictions)
- Note information gaps or contradictions

### Phase 2: Pattern Recognition
- Surface recurring themes
- Identify correlations between topics
- Spot outliers and anomalies
- Detect underlying assumptions

### Phase 3: Insight Generation
For each insight, apply the SPARK framework:
- **S**pecific: What exactly is the insight?
- **P**rovable: What evidence supports it?
- **A**ctionable: What can be done with it?
- **R**elevant: Why does it matter to stakeholders?
- **K**ey: Is this critical or nice-to-know?

### Phase 4: Prioritization
Rank insights by:
1. Strategic importance (1-10)
2. Confidence level (Low/Medium/High)
3. Urgency (Immediate/Short-term/Long-term)

## Output Format

---
## 🔍 Key Insights Report

### Analysis Overview
| Parameter | Value |
|-----------|-------|
| Content Type | [Type] |
| Total Insights | [Number] |
| Critical Insights | [Number] |
| Analysis Date | [Date] |

---

### 🔴 Critical Insights (Act Now)

#### Insight #1: [Title]
| Dimension | Assessment |
|-----------|------------|
| Finding | [Specific insight] |
| Evidence | [Supporting data/quotes] |
| Impact | [High/Medium/Low] |
| Confidence | [High/Medium/Low] |
| Action Required | [Specific action] |
| Urgency | [Immediate/Short-term/Long-term] |

---

### 🟡 Important Insights (Monitor)

#### Insight #2: [Title]
[Same structure as above]

---

### 🟢 Emerging Insights (Track)

#### Insight #3: [Title]
[Same structure as above]

---

### Pattern Summary
| Theme | Frequency | Implications |
|-------|-----------|--------------|
| [Theme 1] | [Count/Prevalence] | [What it means] |

### Information Gaps
- [What's missing from the analysis]
- [Questions that remain unanswered]

### Recommended Next Steps
1. **Immediate**: [Action within 1 week]
2. **Short-term**: [Action within 1 month]
3. **Long-term**: [Strategic initiative]

### Methodology Notes
[Brief note on analytical approach and any caveats]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{content}}` | Text to analyze for insights | Report, transcript, feedback |
| `{{industry}}` | Relevant industry context | SaaS, Healthcare, Retail |
| `{{purpose}}` | Why you need insights | Strategic planning, Product roadmap |
| `{{stakeholder}}` | Who will use insights | CEO, Product team, Board |

---

## Example Usage

**Input:**
```
Content: [Customer interview transcripts from 20 users]
Industry: B2B SaaS
Purpose: Product roadmap prioritization
Stakeholder: Product leadership
```

**Expected Output:**
```
## 🔍 Key Insights Report

### Analysis Overview
| Parameter | Value |
|-----------|-------|
| Content Type | Customer Interview Transcripts |
| Total Insights | 12 |
| Critical Insights | 3 |
| Analysis Date | 2025-12-19 |

---

### 🔴 Critical Insights (Act Now)

#### Insight #1: Onboarding Friction Causing Early Churn
| Dimension | Assessment |
|-----------|------------|
| Finding | 65% of users (13/20) cited confusion during first-week setup |
| Evidence | "I almost gave up on day 2" (User 7); "Setup wizard missed key steps" (User 12) |
| Impact | High |
| Confidence | High |
| Action Required | Redesign onboarding flow with guided walkthrough |
| Urgency | Immediate |

---

### 🟡 Important Insights (Monitor)

#### Insight #2: Integration Ecosystem is Key Differentiator
| Dimension | Assessment |
|-----------|------------|
| Finding | Users with 3+ integrations show 4x higher retention |
| Evidence | Power users consistently mentioned Slack, Salesforce, and Zapier |
| Impact | High |
| Confidence | Medium |
| Action Required | Prioritize top 5 requested integrations |
| Urgency | Short-term |

---

### Pattern Summary
| Theme | Frequency | Implications |
|-------|-----------|--------------|
| Onboarding issues | 65% | Immediate UX investment needed |
| Integration requests | 55% | Ecosystem strategy critical |
| Pricing concerns | 40% | Consider tier restructuring |

### Information Gaps
- No data from churned customers (survivor bias)
- Limited enterprise segment representation

### Recommended Next Steps
1. **Immediate**: Launch onboarding audit and A/B test new flow
2. **Short-term**: Build Salesforce native integration
3. **Long-term**: Develop integration marketplace strategy
```

---

## Pro Tips

1. **MECE Framework**: Ensure insights are Mutually Exclusive, Collectively Exhaustive
2. **Quantify when possible**: "Most users" → "14 of 20 users (70%)"
3. **Separate signal from noise**: Focus on patterns, not one-off comments
4. **Challenge assumptions**: Ask AI to identify hidden biases in the data
5. **Cross-reference**: Feed multiple sources for triangulated insights

---

## Techniques Used

- [x] Role Assignment (Strategic analyst)
- [x] Chain-of-Thought (Multi-phase analysis)
- [ ] Few-Shot Examples
- [x] Structured Output (SPARK framework)
- [ ] Self-Consistency
- [x] Tree-of-Thoughts (Pattern exploration)

---

## Related Prompts

- [Sentiment Analyzer](./sentiment-analyzer.md)
- [Comparative Analysis](./comparative-analysis.md)

---

## Change Log

**v1.1 — 2026-08-24**: Removed the batch-applied confidence-score footer and mandatory-visible chain-of-thought requirement from claude-4-6.md, per migration audit §08 (library-wide mechanical fix, no change to this prompt's core logic).
