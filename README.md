# Vibe Coding Architecture Skill

> A reusable AI Skill for choosing product architecture before coding.

很多人理解 Vibe Coding，是「我说需求，AI 写代码」。

但真正稳定的 Vibe Coding 应该是：

> 我说目标，AI 先拆架构，再写代码。

This repository contains a lightweight Skill that helps AI assistants pause before coding and first make architecture decisions: product type, MVP scope, tech stack, data model, API contract, risks, and final coding prompt.

## Why this exists

In AI-assisted coding, the fastest failure mode is not that AI cannot write code.

It is that AI writes too much code before the architecture is clear.

If you ask AI to directly build a product, it may quickly generate pages, components, and folders. But if the product type is unclear, the project can become messy very quickly:

- A landing page becomes a pseudo-SaaS.
- A local tool gets an unnecessary backend.
- A simple MVP gets over-engineered with auth, queues, and storage.
- A real SaaS misses API contracts, database design, and error handling.
- An AI tool has no model abstraction, usage control, or failure strategy.

This Skill is designed to make AI ask and answer the architecture questions first.

## Core belief

> Good Vibe Coding starts before coding.

Before asking AI to implement, first make it decide:

- What kind of product is this?
- Is it local-first or cloud-first?
- Does it need frontend only, full-stack, or a desktop app?
- Does it need auth, database, storage, cron, queue, payments, or background jobs?
- What is the smallest MVP?
- What should not be built yet?
- What API contract should the system follow?
- What risks should be avoided before writing code?

## What this Skill does

Given a product idea, this Skill makes the AI output:

1. Product summary
2. Product type classification
3. Recommended architecture
4. Recommended tech stack
5. MVP scope
6. Data model direction
7. API contract direction
8. Key risks and mitigations
9. Final coding prompt for Codex, Claude Code, Cursor, or similar AI coding tools

## When to use

Use this Skill before starting an AI-assisted coding project, especially when building:

- AI tools
- SaaS MVPs
- Landing pages
- Content websites
- Local desktop apps
- Automation workflows
- Dashboard products
- Internal tools
- Browser extensions
- Agent workflows

## How to use

Copy the content of [`SKILL.md`](./SKILL.md) into your AI coding assistant as a reusable instruction, or place this repository in your Skill-compatible environment.

Then give it a product idea like:

```txt
I want to build a local-first Xiaohongshu content automation desktop app.
It should generate titles, captions, hashtags, image prompts, preview posts, and publish through local MCP.
Before coding, help me choose the architecture.
```

The AI should not directly code. It should first output an architecture decision document.

## Repository structure

```txt
vibe-coding-architecture-skill/
├── README.md
├── SKILL.md
├── LICENSE
├── .gitignore
├── examples/
│   ├── ai-landing-page.md
│   ├── saas-mvp.md
│   └── xiaohongshu-automation.md
├── references/
│   └── architecture-checklist.md
└── xiaohongshu/
    └── content-plan.md
```

## Example output structure

The Skill asks AI to always output:

```md
# Architecture Decision

## 1. Product Summary

## 2. Product Type

## 3. Recommended Architecture

## 4. Recommended Tech Stack

## 5. MVP Scope

### Must Have

### Should Have

### Later

### Do Not Build Yet

## 6. Data Model

## 7. API Contract

## 8. Key Risks

## 9. Final Coding Prompt
```

## Philosophy

Vibe Coding is not skipping engineering.

It is turning engineering decisions into structured conversation.

## License

MIT
