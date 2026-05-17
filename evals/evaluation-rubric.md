# Evaluation Rubric

Score each dimension from 1 to 5.

1 = poor or missing. 3 = acceptable but incomplete. 5 = strong, clear, beginner-friendly, and implementation-ready.

## 1. Understands the software the user wants to build

- 1: Misunderstands the product.
- 3: Captures basic intent but misses important context.
- 5: Summarizes product, users, scenario, MVP loop, and future direction clearly.

## 2. Correctly classifies the product type

- 1: Wrong type.
- 3: Partially correct but vague.
- 5: Identifies primary and secondary type and explains why.

## 3. Avoids over-engineering

- 1: Adds complex services without need.
- 3: Mostly simple but includes some unnecessary parts.
- 5: Keeps MVP lean and names what not to build yet.

## 4. Gives a clear tech stack

- 1: No concrete stack.
- 3: Stack is present but generic.
- 5: Stack matches product type, stage, and user ability.

## 5. Explains the reason behind each technical choice

- 1: Only lists technologies.
- 3: Gives limited reasoning.
- 5: Explains why choices fit now and when to upgrade.

## 6. Is beginner-friendly

- 1: Jargon-heavy and intimidating.
- 3: Understandable but still technical.
- 5: Conclusion first, plain explanations, no jargon dumping.

## 7. Asks key follow-up questions

- 1: No questions.
- 3: Some questions but not prioritized.
- 5: 5-10 relevant, beginner-friendly questions grouped by topic.

## 8. Includes a Mermaid architecture diagram

- 1: No diagram.
- 3: Diagram exists but too complex or unclear.
- 5: Uses `flowchart TD`, 8-12 nodes at most, beginner-friendly.

## 9. Generates a Codex-ready Build Brief

- 1: No Build Brief.
- 3: Brief exists but misses sections.
- 5: Uses the fixed Build Brief format and can be passed directly to Codex.

## 10. Distinguishes current stage from future expansion

- 1: Mixes MVP and future features.
- 3: Some distinction.
- 5: Clearly separates Demo/MVP/early commercial/scalable choices.

## 11. Identifies risks and non-goals

- 1: No risks or non-goals.
- 3: Mentions risks generally.
- 5: Covers product, technical, cost, model/API, data, permission, deployment, maintenance risks with mitigations.

## 12. Defines a data model and API Contract

- 1: Missing.
- 3: Present but vague.
- 5: Includes entities, fields, relationships, lifecycle, endpoints, methods, request/response, errors, status flow, and permissions when applicable.

## Suggested interpretation

- 55-60: Excellent Skill output.
- 45-54: Good, minor improvements needed.
- 35-44: Usable but incomplete.
- Below 35: Needs major revision before implementation.
