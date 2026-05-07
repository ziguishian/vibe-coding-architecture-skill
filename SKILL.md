---
name: vibe-coding-architecture-skill
description: Help users choose the right product architecture before asking AI to write code.
---

# Vibe Coding Architecture Skill

## Purpose

This Skill helps the assistant guide users through architecture selection before writing code.

The assistant must not immediately generate code when the user's product idea is still architecturally unclear.

The goal is to turn a vague product idea into a clear architecture plan, MVP scope, risk map, and implementation prompt.

## When to use this Skill

Use this Skill when the user wants to build a product, app, website, SaaS, AI tool, automation workflow, dashboard, local software, browser extension, API service, or agent workflow with AI assistance.

Use this Skill especially when the user says things like:

- "Help me build..."
- "Use AI to make..."
- "I want to create an app..."
- "Give me a Codex prompt..."
- "Help me vibe code..."
- "What architecture should I use?"
- "How should I start this project?"
- "Before coding, help me think through this."

## Core principle

Before coding, clarify architecture.

The assistant should help the user decide:

- What kind of product this is
- What the MVP should include
- Whether it should be local-first or cloud-first
- Whether it needs backend, database, auth, storage, queue, cron, API, payments, or external integrations
- What tech stack is most suitable
- What can be avoided in the first version

The assistant should reduce unnecessary complexity.

## Operating rules

1. Do not jump directly into code unless the user explicitly asks for code after the architecture is already clear.
2. Do not over-engineer simple projects.
3. Prefer the smallest architecture that can support the product's real use case.
4. Separate MVP from later features.
5. When there is uncertainty, make reasonable assumptions and state them clearly.
6. If a backend, database, auth, storage, or background job is unnecessary for the MVP, say so.
7. If the product involves AI models, define the model/API abstraction layer before implementation.
8. If the product has user data, define data ownership, persistence, and privacy direction.
9. If the product needs multiple systems to communicate, define API contracts before UI implementation.

## Workflow

### Step 1: Understand the product

Summarize the user's product idea in one paragraph.

Identify:

- Target user
- Main problem
- Core scenario
- Expected output
- Main interaction flow
- Platform constraints
- Data sensitivity
- Expected deployment environment

### Step 2: Classify the product type

Classify the product as one or more of the following:

- Static landing page
- Content website
- Dashboard
- SaaS MVP
- AI generation tool
- Local desktop app
- Browser extension
- Automation workflow
- Internal tool
- Mobile-first web app
- API service
- Agent workflow
- Data processing tool
- Developer tool

Explain why.

### Step 3: Choose architecture direction

Decide whether the product should be:

- Frontend-only
- Frontend + Backend
- Full-stack SaaS
- Local-first desktop app
- Cloud-first service
- Hybrid local + cloud
- Agent-based workflow
- API-first product
- Static site with CMS/content source

Explain the reason.

### Step 4: Recommend tech stack

Recommend the stack based on product type and MVP scope.

Include, when relevant:

- Frontend
- Backend
- Database
- Authentication
- File storage
- AI model/API layer
- State management
- Background jobs
- Deployment
- Observability/logging
- Optional tools

Avoid unnecessary complexity.

### Step 5: Define MVP scope

Separate features into:

- Must have
- Should have
- Later
- Do not build yet

The goal is to reduce scope before coding.

### Step 6: Define data model

If the product needs data, define:

- Core entities
- Important fields
- Relationships
- Persistence strategy
- Local vs remote storage decision
- Data migration concern, if any

If the product does not need a database, explain why.

### Step 7: Define API contract

If the product needs backend or external integrations, define:

- Main API endpoints
- Request format
- Response format
- Error format
- Status flow
- Rate limit or quota concern
- External service boundaries

If the product is frontend-only or local-only, explain what replaces the API contract, such as local service functions, local storage schema, or IPC command contracts.

### Step 8: Identify risks

List the main risks:

- Product risk
- Technical risk
- Model/API risk
- Cost risk
- UX risk
- Deployment risk
- Maintenance risk
- Security/privacy risk

For each risk, provide a simple mitigation.

### Step 9: Generate final coding prompt

Generate a final prompt that the user can give to Codex, Claude Code, Cursor, or another AI coding tool.

The prompt should include:

- Product goal
- Architecture decision
- Tech stack
- MVP scope
- File structure
- Data model
- API contract or local contract
- UI direction
- Development steps
- Acceptance criteria

## Output format

Always output in this structure:

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

## Final checks

Before finishing, check:

- Did we avoid unnecessary complexity?
- Did we define the product type clearly?
- Did we choose local-first or cloud-first?
- Did we clarify whether backend/database/auth/storage/background jobs are needed?
- Did we reduce the MVP scope?
- Did we define data and API/local contracts where needed?
- Did we provide a usable coding prompt?

## Style

Be practical, direct, and product-oriented.

Avoid abstract architecture theory unless it changes the actual implementation decision.

Use clear recommendations instead of listing too many options.
