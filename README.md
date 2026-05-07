# Vibe Coding Architecture Skill

A reusable AI Skill for choosing product architecture before coding.  
一个可复用的 AI Skill，用于在写代码前先选择产品架构。

---

## What is this? / 这是什么？

This repository provides a reusable Skill and documentation workflow that helps AI assistants make architecture decisions before implementation.  
这个仓库提供了一个可复用 Skill 与文档化工作流，帮助 AI 助手在进入实现前先做架构决策。

It is a **Skill/documentation repository**, not a code project, npm package, or framework starter.  
它是一个**Skill/文档仓库**，不是代码工程、npm 包或脚手架模板。

---

## Why architecture comes first in Vibe Coding / 为什么 Vibe Coding 要先做架构

Many AI coding failures are not caused by weak coding ability, but by unclear product definition at the beginning.  
很多 AI 编程失败，并不是 AI 不会写代码，而是起点阶段产品定义不清晰。

If product type, system boundary, data flow, API contract, and MVP scope are ambiguous, implementation usually becomes unstable and expensive to iterate.  
如果产品类型、系统边界、数据流、API Contract 和 MVP 范围不明确，后续实现往往不稳定且迭代成本高。

**Core principle / 核心原则：Before coding, clarify architecture. / 写代码前，先明确架构。**

---

## The problem this skill solves / 这个 Skill 解决什么问题

Without a pre-coding architecture phase, AI often starts coding too early.  
没有架构前置阶段时，AI 往往会过早进入编码。

This skill forces AI to answer key questions first:  
这个 Skill 强制 AI 先回答关键问题：

- What kind of product is this? / 这是什么产品类型？
- Is it landing page, SaaS, dashboard, local app, automation workflow, browser extension, API service, or AI tool? / 它是落地页、SaaS、仪表盘、本地应用、自动化工作流、浏览器插件、API 服务还是 AI 工具？
- Does it need frontend-only, full-stack, local-first, cloud-first, or hybrid architecture? / 它需要前端单体、全栈、本地优先、云优先还是混合架构？
- Does it need auth, database, storage, queue, cron, API, background jobs, or model routing? / 是否需要鉴权、数据库、存储、队列、定时任务、API、后台任务或模型路由？
- What should be included in MVP? / MVP 应该包含什么？
- What should not be built yet? / 哪些功能暂时不该做？
- What data model is needed? / 需要怎样的数据模型？
- What API contract is needed? / 需要怎样的 API Contract？
- What are the key technical risks? / 关键技术风险是什么？
- What final coding prompt should be passed to Codex, Claude Code, Cursor, or other agents? / 最终该给 Codex、Claude Code、Cursor 等工具什么 coding prompt？

---

## When to use this skill / 什么时候使用

Use this when requirements are still fuzzy and someone is about to ask AI to “start building.”  
当需求仍然模糊、但有人准备让 AI “直接开始写”时，就应该使用它。

Typical situations / 典型场景：

- “Help me build ...” / “帮我做一个……”
- “What stack should I use?” / “我该用什么技术栈？”
- “Give me a Codex prompt.” / “给我一个 Codex 提示词。”
- “I want to vibe code.” / “我想做 Vibe Coding。”

---

## What this skill helps AI decide / 这个 Skill 帮 AI 决策什么

- Product type / 产品类型
- Architecture direction / 架构方向
- MVP scope boundary / MVP 边界
- Data model requirement / 数据模型需求
- API contract requirement / API Contract 需求
- Key risks and mitigations / 关键风险与缓解方案
- Final implementation prompt / 最终实现提示词

---

## How to use it / 如何使用

1. Open `SKILL.md` and follow the 9-step workflow.  
   打开 `SKILL.md`，按 9 步流程执行。
2. Use `references/architecture-checklist.md` as a pre-coding checklist.  
   用 `references/architecture-checklist.md` 做编码前检查。
3. Review examples in `examples/` for specific product patterns.  
   参考 `examples/` 中的产品类型示例。
4. Generate the final coding prompt only after architecture is complete.  
   只有架构结论完成后再生成最终 coding prompt。

---


## Quick start request template / 快速请求模板

Copy and fill this template when you ask an AI coding assistant:  
当你向 AI 编程助手提问时，可直接复制以下模板：

```text
I want to build: <product goal>
Target users: <who>
Core scenario: <main workflow>
Constraints: <time/budget/platform>

Use the Vibe Coding Architecture Skill first.
Do not write code yet.
Please output the Architecture Decision format with:
1) Product Summary
2) Product Type
3) Recommended Architecture
4) Recommended Tech Stack
5) MVP Scope
6) Data Model
7) API Contract
8) Key Risks
9) Final Coding Prompt
```

## Request examples / 请求示例

You can ask the assistant like this:  
你可以这样向 AI 发起请求：

- “I want to build a local-first prompt manager app. Use the Vibe Coding Architecture Skill first, then give me architecture decision output.”  
  “我想做一个本地优先的 Prompt 管理工具。请先用 Vibe Coding Architecture Skill 做架构决策输出。”
- “Before coding, classify my product type and define MVP scope with must/should/later/do-not-build-yet.”  
  “写代码前请先判断产品类型，并按 must/should/later/do-not-build-yet 定义 MVP。”
- “Use this repository’s skill format and generate a final coding prompt for Cursor only after API contract is defined.”  
  “请按此仓库 Skill 格式，在 API Contract 明确后再给我 Cursor 的最终 coding prompt。”

---

## Usage example / 使用示例

### Example input / 输入示例

> I want to build an automation tool that takes a topic, generates a draft, reviews it, and saves it to a document.  
> 我想做一个自动化工具：输入主题，生成初稿，审核，然后保存到文档。

### Expected behavior / 期望行为

The assistant should not directly generate code. It should output:  
AI 不应直接开始写代码，而应先输出：

1. Product summary / 产品摘要
2. Product type / 产品类型
3. Recommended architecture / 推荐架构
4. Recommended tech stack / 推荐技术栈
5. MVP scope (Must/Should/Later/Do not build yet) / MVP 范围分层
6. Data model / 数据模型
7. API contract / API Contract
8. Key risks + mitigation / 关键风险与缓解
9. Final coding prompt / 最终 coding prompt

See concrete outputs in `examples/automation-workflow.md`.  
可在 `examples/automation-workflow.md` 查看完整示例。

---

## Example use cases / 用例类型

- AI SaaS MVP with generation flow / AI 生成型 SaaS MVP
- Local-first desktop productivity app / 本地优先桌面效率工具
- Static startup landing page / 创业落地页
- Workflow/agent automation tool / 工作流或 Agent 自动化工具

---

## Repository structure / 仓库结构

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
