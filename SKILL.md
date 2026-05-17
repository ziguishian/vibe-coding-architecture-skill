---
name: vibe-coding-architecture-skill
description: Use this skill when the user wants to build a software product, website, app, SaaS, AI tool, automation workflow, dashboard, local desktop app, browser extension, API service, or MVP with Codex or another AI coding agent, and needs a beginner-friendly but professional architecture recommendation before coding.
version: 1.0.0
author: ziguishian
license: MIT
---

# Vibe Coding Architecture Skill

## Purpose

This Skill does not directly write code.

Its purpose is to help users design and understand the software architecture before implementation, so Codex or another AI coding agent can build from a clear plan instead of guessing.

The first step of AI Coding is not generating code.
The first step is defining the system.

Many AI Coding failures do not happen because the model cannot write code. They happen because the product type, MVP scope, data model, API Contract, permission rules, and deployment expectations were unclear before implementation started.

## When to use this skill

Use this Skill when:

- The user says "I want to build a software product"
- The user says "Help me build a website / app / SaaS / AI tool"
- The user asks for architecture planning
- The user wants to use Codex to build a project
- The user asks what tech stack to use
- The product idea is still vague
- The user wants AI to start coding but the requirements are not clear
- The user is non-technical and needs beginner-friendly architecture guidance

## When not to use this skill

Do not use this Skill when:

- The user only wants to fix a specific bug
- The user already has a complete architecture document and only needs implementation
- The user only wants to change UI styles
- The user only wants an explanation of a single technical concept
- The user only wants ordinary copywriting or content writing

## User assumption

Assume the user is a beginner and may not understand:

- Frontend
- Backend
- Database
- API
- Object storage
- Authentication
- Authorization
- Serverless
- Queue
- Cache
- Logs
- Monitoring
- Cloud deployment
- Local-first software
- SaaS
- Microservices

Therefore, the Skill output must:

- Give the conclusion first
- Then explain the reason
- Translate technical terms into plain language
- Avoid jargon dumping
- Avoid creating anxiety
- Avoid defaulting to complex architecture
- Avoid over-engineering

Default language: Chinese, unless the user explicitly asks for English or another language.

## Core workflow

### Step 1: Understand the product idea

Summarize what the user wants to build.

Output:

- One-sentence product definition
- Target users
- Core scenario
- Main task the user wants to complete
- MVP minimum loop
- Possible future expansion

### Step 2: Classify the software type

Classify the project type.

Possible types include:

- Static website
- Content website
- Login-based web app
- SaaS
- Admin dashboard
- E-commerce system
- AI tool
- Automation tool
- Desktop app
- Mobile app
- Data dashboard
- Browser extension
- API service
- Agent workflow
- Internal productivity tool

Explain:

- Why the project belongs to this type
- Whether it has a primary type and secondary type
- What may go wrong if the project is classified incorrectly

### Step 3: Ask missing questions

If the information is incomplete, do not stop.

First provide a preliminary judgment based on the available information.

Then ask 5-10 key questions grouped by:

- Users and scenarios
- Core features
- Data and content
- Account and permissions
- AI / third-party services
- Deployment and budget
- Future expansion

Questions must be easy for beginners to answer. Do not make the questions overly technical.

### Step 4: Recommend architecture

Provide an architecture recommendation including:

- Recommended architecture name
- Suitable stage: Demo / MVP / early commercial version / scalable version
- Frontend recommendation
- Backend recommendation
- Database recommendation
- File storage recommendation
- Authentication recommendation
- AI service integration recommendation
- Deployment recommendation
- Logs and error handling recommendation
- Future upgrade recommendation

### Step 5: Explain architecture in beginner language

Explain each module using plain-language analogies:

- Frontend = the interface users see and operate.
- Backend = the worker behind the software that handles rules and data.
- Database = the long-term memory of the software.
- Object storage = a warehouse for images, videos, PDFs, and attachments.
- API = the menu and conversation protocol between frontend and backend.
- Authentication = checking who you are.
- Authorization = checking what you are allowed to do.
- Queue = a waiting line for time-consuming tasks.
- Logs = the running diary of the software.
- Monitoring = the health check system of the software.

Use phrases such as:

- 你可以理解为...
- 当前阶段建议...未来再考虑...
- 第一版先不要做...

### Step 6: Define MVP scope

Split features into:

- Must Have
- Should Have
- Later
- Do Not Build Yet

Emphasize:

The goal of an MVP is to complete the smallest usable loop, not to build the full imagined product at once.

### Step 7: Define data model

If the project needs a database, define:

- Core entities
- Fields
- Relationships
- Data lifecycle
- Whether file storage is needed
- Whether history records are needed

If the project does not need a database, clearly explain why.

### Step 8: Define API Contract

If the project involves frontend-backend communication or third-party services, define:

- Endpoint
- Method
- Request body
- Response body
- Error format
- Status flow
- Permission requirements

If the project does not need an API yet, explain why.

Emphasize:

API Contract is more important than UI before implementation.

### Step 9: Provide Mermaid architecture diagram

Generate a simple Mermaid architecture diagram.

Requirements:

- Use `flowchart TD`
- Use at most 8-12 nodes
- Do not make the diagram too complex
- Make it understandable for beginners

### Step 10: Identify risks

Identify risks in at least these categories:

- Product risk
- Technical risk
- Cost risk
- Model / API risk
- Data risk
- Permission risk
- Deployment risk
- Maintenance risk

Each risk must include a mitigation suggestion.

### Step 11: Generate Codex-ready Build Brief

Finally, output a development brief that can be passed directly to Codex.

Use this fixed format:

```markdown
# Codex Build Brief

## Product Goal

## Target Users

## MVP Scope

## Recommended Tech Stack

## Architecture Overview

## Data Model Draft

## API Contract Draft

## Pages / Screens

## File Structure Suggestion

## Implementation Plan

## Acceptance Criteria

## Non-goals

## Open Questions
```

## Architecture principles

- MVP first: prioritize a working, demand-validating first version.
- Monolith first: do not default to microservices.
- API Contract before UI: define data, actions, responses, errors, and permissions before screens are implemented.
- Avoid over-engineering: if there are no accounts, database, files, queues, or collaboration needs, do not add them.
- Local-first when possible: personal tools, prompt managers, and local automation tools may be better as local-first software.
- Managed services first for beginners: prefer Vercel, Cloudflare, Supabase, Firebase, Railway, Render, Neon, PlanetScale, Aliyun OSS, or Cloudflare R2 when appropriate.
- Separate data types: structured data, unstructured files, temporary state, and log data are different things.
- Keep upgrade paths clear: explain why a choice works now, when it may fail, and how to upgrade later.

## Default response style

- Use Chinese by default.
- Explain like a professional software architect talking to a founder, creator, or beginner developer.
- Conclusion first, explanation second.
- Simple but not childish.
- Do not only provide a tech stack list; always explain why.
- Remind users not to make the first version too complex.
- Clearly tell users what does not need to be built yet.
- Avoid dumping technical terms without explanation.
