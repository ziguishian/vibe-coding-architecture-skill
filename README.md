# Vibe Coding Architecture Skill

A reusable AI Skill for choosing product architecture before coding.

## What is this?

This repository provides a reusable Skill and supporting documentation that guides AI assistants to make architecture decisions before implementation.

It is a documentation-first resource for AI coding workflows, not a codebase, npm package, or framework template.

## Why architecture comes first in Vibe Coding

Many AI coding failures happen not because the model cannot write code, but because the product direction was unclear at the start.

When product type, system boundaries, data flow, API contract, and MVP scope are vague, code quality declines and iteration cost increases.

Vibe Coding should begin with architectural clarity:

- Define the product category.
- Choose an appropriate architecture direction.
- Reduce MVP scope.
- Define data and API boundaries.
- Then generate implementation prompts.

## The problem this skill solves

Without a structured pre-coding phase, AI assistants often jump into implementation too early. This skill prevents that by forcing architecture decisions first.

It helps answer critical pre-coding questions:

- What kind of product is this?
- Is this a landing page, SaaS, dashboard, local app, automation workflow, browser extension, API service, or AI tool?
- Does it need frontend only, full-stack, local-first, cloud-first, or hybrid architecture?
- Does it need auth, database, storage, queue, cron, API, background jobs, or model routing?
- What should be included in the MVP?
- What should not be built yet?
- What data model is needed?
- What API contract is needed?
- What are the main technical risks?
- What final coding prompt should be given to Codex, Claude Code, Cursor, or another AI coding agent?

## When to use this skill

Use this skill when:

- A user wants to build a new product and requirements are still high-level.
- A user asks for stack selection before architecture is clarified.
- A user asks for a coding prompt but architecture decisions are incomplete.
- A team wants a repeatable method to reduce premature coding.

## What this skill helps AI decide

The skill guides AI to decide:

- Product type
- Architecture direction
- MVP boundaries
- Data model requirements
- API contract requirements
- Key technical and delivery risks
- Final implementation prompt for coding agents

## How to use it

1. Start with `SKILL.md` as the primary instruction file.
2. Follow the 9-step workflow from product understanding to final coding prompt.
3. Use `references/architecture-checklist.md` for fast pre-flight checks.
4. Review examples in `examples/` for product-type-specific patterns.

## Example use cases

- AI SaaS MVP with generation workflow and user accounts
- Local-first desktop tool with local data and API key management
- Static landing page with minimal frontend-only stack
- Automation workflow with task state and staged execution

## Core principle

**Before coding, clarify architecture.**

Vibe Coding is not skipping engineering; it is moving engineering decisions into a structured AI conversation.

## Repository structure

```text
.
├── README.md
├── SKILL.md
├── LICENSE
├── .gitignore
├── examples/
│   ├── README.md
│   ├── ai-saas-mvp.md
│   ├── local-desktop-app.md
│   ├── landing-page.md
│   └── automation-workflow.md
└── references/
    └── architecture-checklist.md
```
