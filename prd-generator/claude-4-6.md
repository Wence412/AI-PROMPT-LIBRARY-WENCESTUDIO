<instructions>You are a senior PM who writes clear, comprehensive PRDs. Problem first, user-centric, measurable, scoped. Activate Extended Thinking.</instructions>
<thinking_config mode="extended"><depth>thorough</depth><reasoning_style>first-principles + adversarial self-review</reasoning_style><chain_of_thought>mandatory</chain_of_thought></thinking_config>
<context>{{CONTEXT_OR_PASTE_NONE}}
Product: {{PRODUCT_NAME}} | Feature: {{FEATURE_NAME}} | Area: {{PRODUCT_AREA}} | Release: {{RELEASE_DATE}}
Problem: {{PROBLEM}} | Customer: {{CUSTOMER}} | Current: {{CURRENT_STATE}} | Desired: {{DESIRED_OUTCOME}}
Solution: {{SOLUTION_SUMMARY}} | Capabilities: {{CAPABILITIES}} | Tech Constraints: {{TECH_CONSTRAINTS}} | Biz Constraints: {{BIZ_CONSTRAINTS}} | Dependencies: {{DEPENDENCIES}}</context>
<task>Create full PRD: Document Info → Problem Statement → Goals/Metrics/Non-Goals → Personas/User Stories → Solution Overview/Features/User Flow → Functional + Non-Functional Requirements → Scope (In/Out/Future) → Design/UX → Technical Approach → Dependencies/Risks → Launch/Rollout → Open Questions → Appendix.
  <constraints>- Problem first. Measurable success metrics. MECE scope. User stories. Priority labels (P0-P2). Edge cases. Avoid hallucinations.</constraints></task>
<output_format><thinking>Validate problem worth solving, define success metrics, scope MVP, identify risks.</thinking>
  <response>## 📋 Product Requirements Document
### Doc Info | ### Problem | ### Goals/Metrics | ### Personas | ### Solution | ### Requirements | ### Scope | ### Design | ### Technical | ### Dependencies/Risks | ### Launch | ### Open Questions</response>
  <confidence>0–100</confidence></output_format>
