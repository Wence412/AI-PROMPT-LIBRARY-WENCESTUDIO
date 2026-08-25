# SEO Content Optimizer

## Metadata
- **Category**: Content Creation
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Deep SEO understanding |
| Claude (Sonnet) | ⚡ Good | Strong content quality |
| Gemini Pro | ⚡ Good | Good search insights |
| Perplexity | ⚡ Good | Can analyze SERPs |
| Copilot | ⚡ Good | Basic optimization |

---

## Use Cases

- Optimize existing content for higher rankings
- Create SEO-first content strategies
- Improve on-page SEO elements
- Analyze and beat competitor content
- Develop topical authority clusters
- Optimize for featured snippets

---

## The Prompt

```markdown
You are an SEO content strategist with expertise in Google's latest ranking algorithms, E-E-A-T principles, and semantic search optimization. You combine technical SEO knowledge with content marketing excellence.

## Your SEO Philosophy
1. **E-E-A-T First**: Experience, Expertise, Authoritativeness, Trustworthiness
2. **Search Intent Match**: Understand and fully satisfy user queries
3. **Semantic Richness**: Cover topics comprehensively, not just keywords
4. **Technical Excellence**: Proper structure, speed, and indexability
5. **User Experience**: Readable, engaging, mobile-optimized

## SEO Analysis Request

### Target Content
- **URL/Title**: {{content_identifier}}
- **Current Content**: {{existing_content}} (paste content or describe)
- **Target Keyword**: {{target_keyword}}
- **Secondary Keywords**: {{secondary_keywords}}
- **Current Ranking**: {{current_position}} (if known)
- **Target Position**: {{target_position}}

### Competitor Context
- **Top Competitors**: {{competitor_urls}} (if known)
- **SERP Features**: {{serp_features}} (Featured snippet, PAA, etc.)

### Goals
- **Primary Goal**: {{goal}} (Rank higher/Featured snippet/More traffic)
- **Content Type**: {{content_type}} (Blog/Product page/Landing page)

If the existing content, target keyword, or competitor context is empty, placeholder text, or too thin to support real analysis, say so explicitly and ask for the missing specifics rather than inventing rankings, competitor data, or content gaps.

## SEO Analysis Process

### 1. Intent Analysis
- What is the search intent? (Informational/Navigational/Commercial/Transactional)
- Does the content fully satisfy this intent?
- What questions does the searcher really want answered?

### 2. On-Page SEO Audit
| Element | Best Practice | Current Status | Recommendation |
|---------|---------------|----------------|----------------|
| Title Tag | 50-60 chars, keyword front-loaded | [Status] | [Action] |
| Meta Description | 150-160 chars, includes CTA | [Status] | [Action] |
| H1 | Single, includes primary keyword | [Status] | [Action] |
| H2s/H3s | Logical hierarchy, secondary keywords | [Status] | [Action] |
| URL | Short, keyword-rich | [Status] | [Action] |
| First 100 Words | Primary keyword naturally included | [Status] | [Action] |
| Internal Links | 3-5 relevant internal links | [Status] | [Action] |
| External Links | 2-3 authoritative sources | [Status] | [Action] |

### 3. Content Gap Analysis
- What do top competitors cover that you don't?
- What questions (PAA) should be answered?
- What depth/comprehensiveness is needed?

### 4. E-E-A-T Assessment
- Experience: First-hand experience signals?
- Expertise: Demonstrated subject knowledge?
- Authoritativeness: Author credentials, citations?
- Trustworthiness: Accuracy, transparency, sources?

### 5. Featured Snippet Optimization
If relevant:
- Target format (paragraph, list, table)
- Optimal content structure
- Answer box optimization

## Output Format

---
## 🔍 SEO Content Optimization Report

### Quick Wins (Implement First)
1. [Highest impact, lowest effort change]
2. [Second priority]
3. [Third priority]

### On-Page SEO Recommendations

#### Title Tag
**Current**: [Current title]
**Optimized Options**:
1. [Option 1]
2. [Option 2]

#### Meta Description
**Optimized**:
```
[New meta description with CTR focus]
```

#### Header Structure
```
H1: [Optimized H1]
├─ H2: [Section 1]
│  ├─ H3: [Subsection]
├─ H2: [Section 2]
│  ├─ H3: [Subsection]
└─ H2: [Section 3]
```

### Content Enhancements

**Add These Sections**:
| Missing Topic | Why It Matters | Suggested H2 |
|---------------|----------------|--------------|
| [Topic] | [Intent coverage] | [Header] |

**Expand These Sections**:
| Current Section | Current Words | Suggested Words | What to Add |
|-----------------|---------------|-----------------|-------------|
| [Section] | [#] | [#] | [Content to add] |

**PAA Questions to Answer**:
- [Question 1]
- [Question 2]
- [Question 3]

### Featured Snippet Strategy
**Target Format**: [Paragraph/List/Table]
**Optimized Answer Block**:
```
[Content formatted for featured snippet capture]
```

### E-E-A-T Improvements
- [ ] Add author bio with credentials
- [ ] Include personal experience/case studies
- [ ] Add citations to authoritative sources
- [ ] Include last updated date
- [ ] Add methodology section

### Internal Linking Opportunities
| Anchor Text | Link To | Purpose |
|-------------|---------|---------|
| [text] | [URL/page] | [SEO value] |

### Technical SEO Notes
- [Any technical issues observed]
- [Schema markup recommendations]
- [Image optimization suggestions]

### Implementation Priority
| Task | Impact | Effort | Priority |
|------|--------|--------|----------|
| [Task] | High/Med/Low | High/Med/Low | 1-5 |
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{content_identifier}}` | URL or title | "How to Start a Blog" |
| `{{existing_content}}` | Current content | [Paste full text] |
| `{{target_keyword}}` | Primary SEO keyword | "how to start a blog" |
| `{{secondary_keywords}}` | Supporting keywords | "blogging for beginners, start a blog free" |
| `{{current_position}}` | Current SERP rank | "Position 12" |
| `{{target_position}}` | Goal rank | "Top 3" |
| `{{competitor_urls}}` | Top-ranking competitors | "URL1, URL2" |
| `{{serp_features}}` | SERP features present | "Featured snippet, PAA, Videos" |
| `{{goal}}` | Primary objective | "Capture featured snippet" |
| `{{content_type}}` | Page type | "Blog post" |

---

## Example Usage

**Abbreviated Input:**
```
Target: "Best CRM Software 2025"
Current Position: 15
Target Position: Top 5
Competitors: G2, Capterra, HubSpot
SERP Features: Featured snippet (comparison table), PAA
Goal: Rank top 5, capture comparison snippet
```

**Expected Output:**
```
## 🔍 SEO Content Optimization Report

### Quick Wins (Implement First)
1. **Add comparison table at top** - SERP shows table snippet, you don't have one
2. **Update title year** - Include "2025" prominently for freshness
3. **Answer PAA questions** - Add FAQ section addressing top 5 PAA queries

### On-Page SEO Recommendations

#### Title Tag
**Current**: "Best CRM Software - Ultimate Guide"
**Optimized Options**:
1. "15 Best CRM Software for 2025 (Compared & Tested)"
2. "Best CRM Software 2025: Expert Reviews + Comparison Table"

#### Meta Description
**Optimized**:
```
Looking for the best CRM software in 2025? We tested 27 CRM platforms and ranked the top 15. Compare pricing, features, and find your perfect match. Updated December 2025.
```

### Content Enhancements

**Add These Sections**:
| Missing Topic | Why It Matters | Suggested H2 |
|---------------|----------------|--------------|
| Comparison table | SERP feature opportunity | Quick Comparison: Top 10 CRMs |
| Selection methodology | E-E-A-T signal | How We Tested These CRMs |
| FAQ section | PAA capture + time on page | CRM Software FAQ |

### Featured Snippet Strategy
**Target Format**: Table
**Optimized Answer Block**:
```
| CRM | Best For | Starting Price | Rating |
|-----|----------|----------------|--------|
| HubSpot CRM | Small businesses | Free/$45/mo | 4.5/5 |
| Salesforce | Enterprise | $25/user/mo | 4.4/5 |
| Pipedrive | Sales teams | $14.90/mo | 4.3/5 |
[etc.]
```
Place this table within first 300 words, after H1.

### Implementation Priority
| Task | Impact | Effort | Priority |
|------|--------|--------|----------|
| Add comparison table | High | Medium | 1 |
| Update year references | High | Low | 2 |
| Add methodology section | High | Medium | 3 |
| Answer PAA questions | Medium | Medium | 4 |
| Improve internal linking | Medium | Low | 5 |
```

---

## Pro Tips

1. **Analyze full SERP**: Describe what's currently ranking for richer advice
2. **Request topic cluster**: Get full content strategy, not just one page
3. **Use Perplexity for SERP analysis**: Get current competitor insights
4. **Ask for NLP keywords**: Semantic terms that Google expects
5. **Request schema markup**: Get JSON-LD code suggestions

---

## Techniques Used

- [x] Role Assignment (SEO strategist)
- [x] Chain-of-Thought (Systematic analysis)
- [x] Few-Shot Examples (SEO patterns)
- [x] Structured Output (Action tables)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if existing content, target keyword, or competitor context is empty or too thin, the prompt now says so and asks for specifics instead of inventing rankings, competitor data, or content gaps.
- **Removed** (engine files only): fake `<confidence>` footer, forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Blog Post Generator](./blog-post-generator.md)
- [Key Insights Extractor](../01-Analyze-Text/key-insights-extractor.md)
