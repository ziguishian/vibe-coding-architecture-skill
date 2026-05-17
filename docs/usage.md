# Usage

The typical workflow is:

1. User describes the software idea.
2. Skill classifies the product type.
3. Skill asks key missing questions.
4. Skill recommends architecture.
5. Skill outputs a Codex Build Brief.
6. User confirms or adjusts the plan.
7. Codex starts coding after the architecture is clear.

## Recommended prompt shape

```text
I want to build [product]. Please use vibe-coding-architecture-skill to plan the architecture before coding.
```

Chinese:

```text
我想做一个 [产品]，请先用 vibe-coding-architecture-skill 帮我做架构规划，不要直接写代码。
```

## What to expect

The Skill should provide:

- A clear product summary
- Product type classification
- Beginner-friendly questions
- Architecture recommendation
- MVP scope
- Data model
- API Contract
- Mermaid diagram
- Risk assessment
- Codex Build Brief

## How to use the Build Brief

After the Skill generates the Build Brief, pass it to Codex as the implementation context.

Do not ask Codex to build the full dream version at once. Ask it to build the MVP loop first.
