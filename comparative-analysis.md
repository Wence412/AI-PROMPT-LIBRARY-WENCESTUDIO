# Comparative Analysis

## Metadata
- **Category**: Analyze Text
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Excellent for multi-document comparison |
| ChatGPT (GPT-4o) | ✅ Optimal | Strong analytical reasoning |
| Gemini Pro | ⚡ Good | Great for large document sets |
| Perplexity | ⚡ Good | Adds external context |
| Copilot | ⚡ Good | Works with M365 documents |

---

## Use Cases

- Compare competitor products or services
- Analyze policy differences across documents
- Contrast multiple research papers on same topic
- Evaluate vendor proposals side-by-side
- Track document version changes

---

## The Prompt

```markdown
You are a comparative analysis expert with skills in structured evaluation, critical thinking, and synthesizing complex information across multiple sources.

## Documents to Compare

### Document A: {{doc_a_title}}
{{doc_a_content}}

### Document B: {{doc_b_title}}
{{doc_b_content}}

### Document C (Optional): {{doc_c_title}}
{{doc_c_content}}

## Comparison Parameters
- **Comparison Focus**: {{focus}} (e.g., Features, Pricing, Quality, Arguments)
- **Evaluation Criteria**: {{criteria}} (e.g., Completeness, Accuracy, Innovation)
- **Output Preference**: {{output_type}} (Matrix | Narrative | Both)

## Comparative Analysis Framework

### Step 1: Document Profiling
Create a profile for each document:
- Type and purpose
- Key themes covered
- Quality/depth of information
- Notable strengths and weaknesses

### Step 2: Dimension Mapping
Identify common dimensions for comparison:
- Explicitly covered by all documents
- Covered by some but not others
- Implied but not explicitly stated

### Step 3: Side-by-Side Analysis
For each dimension:
- Extract relevant content from each document
- Compare and contrast positions/information
- Note agreements and contradictions

### Step 4: Synthesis
- Identify overall patterns
- Highlight key differentiators
- Surface complementary information
- Flag conflicts requiring resolution

## Output Format

---
## 📊 Comparative Analysis Report

### Overview
| Attribute | Document A | Document B | Document C |
|-----------|------------|------------|------------|
| Title | [Title] | [Title] | [Title] |
| Type | [Type] | [Type] | [Type] |
| Length | [Est.] | [Est.] | [Est.] |
| Primary Focus | [Focus] | [Focus] | [Focus] |

---

### Comparison Matrix

| Dimension | Doc A | Doc B | Doc C | Winner |
|-----------|-------|-------|-------|--------|
| [Dim 1] | [Summary] | [Summary] | [Summary] | [A/B/C/Tie] |
| [Dim 2] | [Summary] | [Summary] | [Summary] | [A/B/C/Tie] |
| [Dim 3] | [Summary] | [Summary] | [Summary] | [A/B/C/Tie] |

---

### Key Agreements
- **[Topic]**: All documents align on [shared position]
  - Doc A: "[Quote]"
  - Doc B: "[Quote]"

### Key Differences
- **[Topic]**: Documents diverge significantly
  - Doc A position: [Summary]
  - Doc B position: [Summary]
  - Implication: [What this means]

### Unique Contributions
| Document | Unique Insight |
|----------|----------------|
| Doc A | [What only A covers] |
| Doc B | [What only B covers] |

### Information Gaps
- [Topic not adequately covered by any document]

---

### Synthesis & Recommendations

**Overall Assessment**:
[Which document is strongest overall and why]

**Best For**:
- Doc A: [Best use case]
- Doc B: [Best use case]
- Doc C: [Best use case]

**Recommended Approach**:
[How to use these documents together]

### Confidence Assessment
| Aspect | Confidence | Notes |
|--------|------------|-------|
| Factual Accuracy | [H/M/L] | [Notes] |
| Fair Comparison | [H/M/L] | [Notes] |
| Completeness | [H/M/L] | [Notes] |
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{doc_a_title}}` | Title of first document | "Q3 Financial Report" |
| `{{doc_a_content}}` | Content of first document | Full text |
| `{{doc_b_title}}` | Title of second document | "Q2 Financial Report" |
| `{{doc_b_content}}` | Content of second document | Full text |
| `{{focus}}` | What to compare | "Revenue performance" |
| `{{criteria}}` | Evaluation standards | "Growth, Profitability" |
| `{{output_type}}` | Preferred format | "Matrix", "Narrative", "Both" |

---

## Example Usage

**Input:**
```
Document A: "Vendor X Proposal"
Document B: "Vendor Y Proposal"
Focus: Technical capabilities, Pricing, Support
Criteria: Value for money, Scalability, Risk
Output: Both
```

**Expected Output:**
```
## 📊 Comparative Analysis Report

### Overview
| Attribute | Vendor X | Vendor Y |
|-----------|----------|----------|
| Title | Enterprise Solution Proposal | Cloud Platform Proposal |
| Type | Vendor Proposal | Vendor Proposal |
| Total Cost | $450K/year | $380K/year |
| Primary Focus | On-premise + Cloud hybrid | Cloud-native |

---

### Comparison Matrix

| Dimension | Vendor X | Vendor Y | Winner |
|-----------|----------|----------|--------|
| Scalability | Limited; requires hardware | Unlimited elastic scaling | Y |
| Security | SOC2, ISO27001, On-prem option | SOC2, HIPAA (no on-prem) | X |
| Support | 24/7 dedicated team | Business hours + premium tier | X |
| Integration | 15 native integrations | 45 native + API-first | Y |
| Total Cost | $450K/yr + hardware | $380K/yr all-inclusive | Y |

---

### Key Differences
- **Deployment Model**: X offers hybrid; Y is cloud-only
  - Implication: X better for regulated industries needing on-prem
  
- **Pricing Structure**: X has hidden hardware costs; Y is predictable
  - True 3-year TCO: X = $1.8M vs Y = $1.14M

### Unique Contributions
| Vendor | Unique Value |
|--------|--------------|
| Vendor X | On-premise option for compliance |
| Vendor Y | API-first architecture enables custom workflows |

---

### Synthesis & Recommendations

**Overall Assessment**:
Vendor Y offers better value for most use cases, but Vendor X is necessary if on-premise deployment is a regulatory requirement.

**Best For**:
- Vendor X: Regulated industries (healthcare, finance with on-prem mandates)
- Vendor Y: Modern cloud-first organizations prioritizing flexibility

**Recommended Approach**:
Proceed with Vendor Y for main deployment; explore Vendor X for specific compliance-sensitive workloads.
```

---

## Pro Tips

1. **Normalize terminology**: Different docs may use different terms for same concepts
2. **Use weighted scoring**: When criteria aren't equally important
3. **Flag assumptions**: Note when you're inferring from incomplete information
4. **Consider bias**: Each document may have a perspective/agenda
5. **Track sources**: Reference specific sections for each claim

---

## Techniques Used

- [x] Role Assignment (Comparative analyst)
- [x] Chain-of-Thought (Systematic framework)
- [ ] Few-Shot Examples
- [x] Structured Output (Comparison matrix)
- [ ] Self-Consistency
- [x] Tree-of-Thoughts (Multi-document reasoning)

---

## Related Prompts

- [Document Summarizer](./document-summarizer.md)
- [Key Insights Extractor](./key-insights-extractor.md)
