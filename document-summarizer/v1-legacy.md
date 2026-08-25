# Document Summarizer

## Metadata
- **Category**: Analyze Text
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | 200K context for long documents |
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent summarization |
| Gemini Pro | ✅ Optimal | 1M context for massive docs |
| Perplexity | ⚡ Good | Good for web content |
| Copilot | ⚡ Good | Great for M365 documents |

---

## Use Cases

- Summarize research papers and whitepapers
- Condense meeting transcripts
- Create executive briefings from reports
- Digest legal documents and contracts
- Process lengthy email threads

---

## The Prompt

```markdown
You are an expert document analyst and professional summarizer. Your task is to create a comprehensive yet concise summary of the provided document.

## Document to Summarize
{{document_content}}

## Summary Parameters
- **Target Length**: {{summary_length}} (Brief: 100-200 words | Standard: 300-500 words | Detailed: 500-800 words)
- **Audience**: {{target_audience}} (Executive | Technical | General)
- **Focus Areas**: {{focus_areas}} (Optional: specific topics to emphasize)

## Summarization Process

Follow this systematic approach:

### Step 1: Document Overview
Identify the document type, purpose, and scope.

### Step 2: Key Information Extraction
Extract the most critical information:
- Main thesis/purpose
- Key arguments/findings
- Supporting evidence
- Conclusions/recommendations

### Step 3: Hierarchical Condensation
Organize information by importance, preserving essential context.

### Step 4: Quality Check
Ensure the summary:
- Captures all critical points
- Maintains factual accuracy
- Flows logically
- Matches target length

## Output Format

---
## 📄 Document Summary

### Document Overview
| Attribute | Value |
|-----------|-------|
| Type | [Document type] |
| Length | [Original length estimate] |
| Date/Source | [If available] |

### Executive Summary
[2-3 sentence high-level overview]

### Key Points
1. **[Topic 1]**: [Summary]
2. **[Topic 2]**: [Summary]
3. **[Topic 3]**: [Summary]

### Critical Findings/Arguments
- [Finding 1]
- [Finding 2]
- [Finding 3]

### Notable Quotes
> "[Significant quote from document]"

### Conclusions & Recommendations
[Main conclusions and any recommendations from the document]

### Action Items (if applicable)
- [ ] [Action item 1]
- [ ] [Action item 2]

### Topics for Further Review
- [Topic requiring deeper dive]
---
```

If the document content is empty, placeholder text, or too thin to summarize meaningfully, say so explicitly and ask for the missing material rather than inventing content.

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{document_content}}` | The full document text | Research paper, report, transcript |
| `{{summary_length}}` | Desired summary length | Brief, Standard, Detailed |
| `{{target_audience}}` | Who will read the summary | Executive, Technical, General |
| `{{focus_areas}}` | Specific topics to emphasize | "Budget implications, Timeline" |

---

## Example Usage

**Input:**
```
Document: [Long research report on AI adoption in enterprises]
Target Length: Standard
Audience: Executive
Focus Areas: ROI, Implementation challenges
```

**Expected Output:**
```
## 📄 Document Summary

### Document Overview
| Attribute | Value |
|-----------|-------|
| Type | Industry Research Report |
| Length | ~15,000 words (45 pages) |
| Source | TechAnalytics Research, Q4 2025 |

### Executive Summary
Enterprise AI adoption reached 67% in 2025, with average ROI of 340% for mature implementations. However, 45% of initiatives still fail due to integration challenges and talent gaps. Successful adopters prioritize incremental deployment and cross-functional alignment.

### Key Points
1. **Market Penetration**: AI adoption up 23% YoY, with manufacturing and finance leading
2. **ROI Metrics**: Median payback period of 14 months; top performers see 5x returns
3. **Failure Factors**: Data quality (34%), talent shortage (28%), change resistance (22%)

### Critical Findings
- Companies with dedicated AI governance see 2.3x higher success rates
- Cloud-native AI solutions outperform on-premise by 40% in time-to-value
- Small pilots (under $500K) have 3x higher full-deployment rates

### Notable Quotes
> "The organizations winning with AI treat it as a business transformation, not a technology project."

### Conclusions & Recommendations
Start with high-impact, low-complexity use cases. Invest in data infrastructure before scaling AI. Establish clear governance and success metrics from day one.

### Action Items
- [ ] Assess current data quality maturity
- [ ] Identify 3 pilot use cases with clear ROI potential
- [ ] Establish AI governance committee
```

---

## Pro Tips

1. **Use Claude for 100+ page documents** - Leverage full 200K context
2. **Layer summaries** - Create executive (1 page) → detailed (3 page) hierarchy
3. **Specify exclusions** - Tell it what to skip (e.g., "Ignore appendices")
4. **Request citations** - Ask for page/section references for key claims
5. **Multi-document synthesis** - Summarize multiple docs into one coherent brief

---

## Techniques Used

- [x] Role Assignment (Expert analyst)
- [x] Chain-of-Thought (Systematic process)
- [ ] Few-Shot Examples
- [x] Structured Output (Formatted report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if the document content is empty or too thin to summarize meaningfully, the prompt now says so and asks for the missing material instead of inventing content.
- **Removed** (engine files only): fake `<confidence>` footer, dead `<agentic_hooks>` block, and forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Key Insights Extractor](./key-insights-extractor.md)
- [Comparative Analysis](./comparative-analysis.md)
