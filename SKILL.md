---
name: vibe-coding-architecture-skill
description: Help users choose the right product architecture before asking AI to write code.
---

# Vibe Coding Architecture Skill

## Purpose

This skill helps the assistant guide users through architecture selection before writing code.

When the user's product idea is still architecturally unclear, the assistant should not immediately generate code.

Instead, the assistant should first help the user clarify:

- Product type
- Architecture direction
- MVP scope
- Data model
- API contract
- Technical risks
- Final coding prompt

## When to Use This Skill

Use this skill when:

- The user wants to build a product, website, app, SaaS, AI tool, automation tool, local desktop app, browser extension, admin panel, or API service.
- The user says “help me build...”.
- The user says “give me a Codex prompt...”.
- The user says “what stack should I use...”.
- The user says “I want to vibe code...”.
- The requirements are still vague.
- The user wants to start with Codex, Claude Code, Cursor, or another AI coding tool.

## Core Principle

Before coding, clarify architecture.

Vibe Coding is not about skipping engineering.
It is about moving engineering decisions into a structured conversation with AI.

The assistant should not rush into implementation.
The assistant should first help the user make the right architectural decisions.

## Workflow

### Step 1: Understand the Product

Summarize:

- Target user
- Main problem
- Core scenario
- Expected output
- Main interaction flow
- Constraints

### Step 2: Classify the Product Type

Choose one primary type (and one secondary type if necessary):

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

Explain why the classification fits.

### Step 3: Choose Architecture Direction

Select the architecture direction:

- Frontend-only
- Frontend + Backend
- Full-stack SaaS
- Local-first desktop app
- Cloud-first service
- Hybrid local + cloud
- Agent-based workflow
- API-first product

Explain trade-offs and why this direction is appropriate.

### Step 4: Recommend Tech Stack

Recommend:

- Frontend
- Backend
- Database
- Authentication
- File storage
- AI model/API layer
- Deployment
- Optional tools

Rules:

- Avoid unnecessary complexity.
- Do not choose a backend unless it is needed.
- Do not choose a database unless persistent data is needed.
- Do not choose authentication unless user accounts are needed.
- Do not choose cloud infrastructure if the product can be local-first.
- Do not design a large system before validating the MVP.

### Step 5: Define MVP Scope

Split scope into:

- Must have
- Should have
- Later
- Do not build yet

Focus on reducing scope, not expanding it.

### Step 6: Define Data Model

If data persistence is needed, define:

- Core entities
- Main fields
- Relationships
- Storage strategy

If no database is needed, explicitly explain why.

### Step 7: Define API Contract

If frontend-backend communication or external integration is needed, define:

- Endpoint
- Method
- Request body
- Response body
- Error format
- Status flow

If no API is needed, explicitly explain why.

### Step 8: Identify Risks

List key risks and one mitigation for each:

- Product risk
- Technical risk
- Model/API risk
- Cost risk
- UX risk
- Deployment risk
- Maintenance risk

### Step 9: Generate Final Coding Prompt

Generate a final prompt that can be directly used with Codex, Claude Code, Cursor, or other AI coding agents.

The prompt must include:

- Product goal
- Architecture decision
- Tech stack
- MVP scope
- Data model
- API contract
- UI direction
- File structure
- Development steps
- Acceptance criteria

## Output Format

Use this exact output structure:

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

## Final Checks

- Did we avoid unnecessary complexity?
- Did we identify the product type clearly?
- Did we decide local-first or cloud-first?
- Did we clarify whether backend/database/auth/storage are needed?
- Did we reduce MVP scope?
- Did we define the data model if needed?
- Did we define the API contract if needed?
- Did we identify key risks?
- Did we provide a usable coding prompt?
