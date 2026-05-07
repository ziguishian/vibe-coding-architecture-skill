# Vibe Coding Architecture Skill

![Skill](https://img.shields.io/badge/Type-AI%20Skill-4f46e5)
![Focus](https://img.shields.io/badge/Focus-Architecture%20Before%20Code-0ea5e9)
![License](https://img.shields.io/badge/License-MIT-22c55e)
![Docs](https://img.shields.io/badge/Repo-Documentation%20First-f59e0b)

A reusable AI Skill for choosing product architecture before coding.

> 中文文档请看：[`README.zh-CN.md`](./README.zh-CN.md)

---
<img width="1233" height="404" alt="image" src="https://github.com/user-attachments/assets/8d949ae0-62af-4836-a32a-7f34239cf3b9" />
<img width="3840" height="2159" alt="image" src="https://github.com/user-attachments/assets/7ebc74f6-96ac-430b-a036-a42c60888dad" />


## What is this?

This repository provides a reusable Skill and documentation workflow that helps AI assistants make architecture decisions before implementation.

It is a **Skill/documentation repository**, not a code project, npm package, or framework starter.

---

## Why architecture comes first in Vibe Coding

Many AI coding failures are not caused by weak coding ability, but by unclear product definition at the beginning.

If product type, system boundary, data flow, API contract, and MVP scope are ambiguous, implementation usually becomes unstable and expensive to iterate.

**Core principle: Before coding, clarify architecture.**

---

## The problem this skill solves

Without a pre-coding architecture phase, AI often starts coding too early.

This skill forces AI to answer key questions first:

- What kind of product is this?
- Is it landing page, SaaS, dashboard, local app, automation workflow, browser extension, API service, or AI tool?
- Does it need frontend-only, full-stack, local-first, cloud-first, or hybrid architecture?
- Does it need auth, database, storage, queue, cron, API, background jobs, or model routing?
- What should be included in MVP?
- What should not be built yet?
- What data model is needed?
- What API contract is needed?
- What are the key technical risks?
- What final coding prompt should be passed to Codex, Claude Code, Cursor, or other agents?

---

## When to use this skill

Use this when requirements are still fuzzy and someone is about to ask AI to “start building.”

Typical situations:

- “Help me build ...”
- “What stack should I use?”
- “Give me a Codex prompt.”
- “I want to vibe code.”

---

## What this skill helps AI decide

- Product type
- Architecture direction
- MVP scope boundary
- Data model requirement
- API contract requirement
- Key risks and mitigations
- Final implementation prompt

---

## How to use it

1. Open `SKILL.md` and follow the 9-step workflow.
2. Use `references/architecture-checklist.md` as a pre-coding checklist.
3. Review examples in `examples/` for specific product patterns.
4. Generate the final coding prompt only after architecture is complete.

---

## Request examples

- “I want to build a local-first prompt manager app. Use the Vibe Coding Architecture Skill first, then give me architecture decision output.”
- “Before coding, classify my product type and define MVP scope with must/should/later/do-not-build-yet.”
- “Use this repository’s skill format and generate a final coding prompt for Cursor only after API contract is defined.”

---

## Usage example

### Example input

> I want to build an automation tool that takes a topic, generates a draft, reviews it, and saves it to a document.

### Expected behavior

The assistant should not directly generate code. It should output:

1. Product summary
2. Product type
3. Recommended architecture
4. Recommended tech stack
5. MVP scope (Must/Should/Later/Do not build yet)
6. Data model
7. API contract
8. Key risks + mitigation
9. Final coding prompt

See concrete outputs in `examples/automation-workflow.md`.

---

## Repository structure

```text
.
├── README.md
├── README.zh-CN.md
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
