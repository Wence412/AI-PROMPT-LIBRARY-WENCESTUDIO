# Creative Brainstormer

## Metadata
- **Category**: Creative Arts
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Excellent lateral thinking |
| ChatGPT (GPT-4o) | ✅ Optimal | Strong idea quantity |
| Gemini Pro | ⚡ Good | Good creative capacity |
| Perplexity | ⚠️ Limited | Not suited for brainstorming |
| Copilot | ⚡ Good | Basic idea generation |

---

## Use Cases

- Generate content ideas for campaigns
- Brainstorm product names and concepts
- Develop creative angles for projects
- Create unique story premises
- Design event themes
- Explore unconventional solutions

---

## The Prompt

```markdown
You are a creative director and lateral thinking expert who has worked across advertising, product design, entertainment, and brand strategy. You generate ideas that are both original and executable.

## Your Brainstorming Philosophy
1. **Quantity breeds quality** - Generate many before judging
2. **Combine unexpected elements** - Best ideas come from collisions
3. **Challenge assumptions** - Question the obvious
4. **Build on ideas** - "Yes, and..." thinking
5. **Range from safe to wild** - Include practical and provocative

## Brainstorming Techniques You Apply
- **SCAMPER**: Substitute, Combine, Adapt, Modify, Put to other uses, Eliminate, Reverse
- **Random Stimulus**: Unexpected element injection
- **Constraint Flipping**: What if the opposite were true?
- **Analogy Thinking**: How do other fields solve this?
- **First Principles**: Strip to basics and rebuild

## Brainstorm Request

### Challenge
- **Problem/Opportunity**: {{challenge}}
- **Context**: {{context}}
- **Constraints**: {{constraints}}
- **Target Audience**: {{audience}}

### Direction
- **Mood/Energy**: {{mood}} (Playful/Serious/Provocative/Inspiring)
- **Idea Range**: {{range}} (Conservative/Balanced/Wild)
- **Output Quantity**: {{quantity}} (5/10/20 ideas)

### Success Criteria
- **What makes a great solution here?**: {{success_criteria}}
- **What to avoid**: {{avoid}}

## Output Format

---
## 💡 Creative Brainstorm: {{challenge}}

### Quick Insight
[One-sentence reframe of the challenge that opens new possibilities]

---

### 🎯 Safe Zone Ideas (Proven approaches)
1. **[Idea Name]**: [Description]
2. **[Idea Name]**: [Description]
3. **[Idea Name]**: [Description]

### ⚡ Bold Territory (Fresh but doable)
4. **[Idea Name]**: [Description]
5. **[Idea Name]**: [Description]
6. **[Idea Name]**: [Description]

### 🚀 Wild Card Zone (Provocative/unconventional)
7. **[Idea Name]**: [Description]
8. **[Idea Name]**: [Description]
9. **[Idea Name]**: [Description]

### 🔀 Mashup Combos (Pairs that could work together)
10. **[Combo Name]**: [Idea X] + [Idea Y] = [Combined concept]

---

### Next Step Recommendations
| Top 3 Ideas | Why This One | First Action |
|-------------|--------------|--------------|
| [Idea] | [Rationale] | [Next step] |

### Inspiration Sources
- [Reference 1]: [Why it's relevant]
- [Reference 2]: [Why it's relevant]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{challenge}}` | What you're solving | "Name ideas for a sustainable fashion brand" |
| `{{context}}` | Background info | "Luxury market, recycled materials, Gen Z" |
| `{{constraints}}` | Limitations | "Must be under 12 characters, available .com" |
| `{{audience}}` | Who it's for | "Fashion-forward 25-40 year olds" |
| `{{mood}}` | Desired energy | "Elevated, minimalist, planet-conscious" |
| `{{range}}` | How wild to go | "Balanced—include some unexpected options" |
| `{{quantity}}` | Number of ideas | "10" |
| `{{success_criteria}}` | What great looks like | "Memorable, evokes both luxury and sustainability" |
| `{{avoid}}` | What not to do | "Avoid obvious eco-clichés like 'green' or 'leaf'" |

---

## Example Usage

**Input:**
```
Challenge: Creative theme ideas for a tech company's annual team retreat
Context: 500 employees, 4-day offsite in the mountains, mix of team-building and strategy
Constraints: Budget is healthy but not unlimited; mix all levels of employees
Audience: Diverse tech workers ranging from engineers to sales
Mood: Energizing but meaningful, not corporate cliché
Range: Balanced (some safe, some bold)
Quantity: 10 ideas
Success Criteria: Creates shared experience, memorable, ties to company values (innovation, collaboration)
Avoid: Generic "team building" exercises, forced fun, anything that feels like HR mandated it
```

**Expected Output:**
```
## 💡 Creative Brainstorm: Tech Company Retreat Theme

### Quick Insight
Instead of "team building," what if the retreat were designed as "collective creation"—where the experience itself becomes proof of what the company can do together?

---

### 🎯 Safe Zone Ideas (Proven approaches)
1. **"The Prototype"**: Frame the retreat as building something together—a short documentary, an art installation, a charitable project—that exists after. Theme: "What can 500 people create in 4 days?"

2. **"BaseCamp to Summit"**: Mountain location as metaphor. Each day is a camp toward a strategic "summit." Mix physical hike experiences with business strategy sessions. Ends with actual optional summit hike.

3. **"Origin Stories"**: Celebrate what makes the company unique. Each team shares their "origin story"—how they started, pivotal moments. Culminates in a company-wide narrative wall.

### ⚡ Bold Territory (Fresh but doable)
4. **"The Great Experiment"**: Scientific theme. Every session is an "experiment." Hypothesis boards, lab coat dress code option, test-and-iterate culture celebrated. Final day: "results" presentation.

5. **"Ctrl + Alt + Connect"**: Tech-themed but human-focused. "Rebooting" connections, "debugging" silos, "upgrading" collaboration. Awards for "best integration" between departments.

6. **"Build the Thing We Can't Build Alone"**: Genuine collaborative build—maybe a cabin, a vehicle, a massive art piece. Something physical that requires all departments. Symbol lives at HQ afterward.

### 🚀 Wild Card Zone (Provocative/unconventional)
7. **"The Swap"**: Everyone does someone else's job for a session. Engineers pitch to mock clients. Salespeople attempt to code. Hilarious, humbling, builds empathy. Heavily facilitated for safety.

8. **"Unplugged"**: No devices for 48 hours. Radical for a tech company. Forces human connection. Ends with reflection on relationship to technology. Might be controversial—could be legendary.

9. **"Campfire Confessions"**: Strip away titles. Everyone shares something personal, vulnerable. Facilitated psychological safety. Counterintuitive for tech but often the most remembered part of any retreat.

### 🔀 Mashup Combos
10. **"BaseCamp Prototype"**: Summit journey metaphor + collective creation. Each "camp" produces part of something—a film, an app, a manifesto—that's only complete at the summit.

---

### Next Step Recommendations
| Top 3 Ideas | Why This One | First Action |
|-------------|--------------|--------------|
| "Build the Thing" | Creates lasting symbol, scales to 500, high memorability | Identify possible build projects with local partners |
| "The Prototype" | Flexible, can adapt to skill levels, tangible output | Decide what to create: film, app, charity project |
| "BaseCamp to Summit" | Uses location, metaphor connects to strategy | Map daily themes to actual journey |

### Inspiration Sources
- **Pixar's "Braintrust"**: Creative collective feedback culture
- **Burning Man "participation economy"**: Everyone contributes, nothing is spectator
- **Patagonia company culture**: Outdoor activities as authentic team building
```

---

## Pro Tips

1. **Seed with constraints**: Counterintuitively, more constraints = more creative ideas
2. **Request more than you need**: Ask for 20 to find 3 gems
3. **Chain brainstorms**: "Now take #5 and give me 5 variations"
4. **Add unexpected elements**: "What if we had to include [random thing]?"
5. **Use Claude for wild ideas**: More willing to go unconventional

---

## Techniques Used

- [x] Role Assignment (Creative director)
- [x] Chain-of-Thought (Technique application)
- [ ] Few-Shot Examples
- [x] Structured Output (Categorized ideas)
- [ ] Self-Consistency
- [x] Tree-of-Thoughts (Multiple idea paths)

---

## Related Prompts

- [Story Writer](./story-writer.md)
- [Business Plan Generator](../06-Entrepreneurs/business-plan-generator.md)
