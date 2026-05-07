# Vibe Coding Architecture Skill

![技能类型](https://img.shields.io/badge/类型-AI%20Skill-4f46e5)
![核心理念](https://img.shields.io/badge/核心-先架构后编码-0ea5e9)
![许可证](https://img.shields.io/badge/许可证-MIT-22c55e)
![仓库定位](https://img.shields.io/badge/仓库-文档优先-f59e0b)

一个可复用的 AI Skill，用于在写代码前先选择产品架构。

> English version: [`README.md`](./README.md)

---

## 这是什么？

这个仓库提供了一个可复用 Skill 与文档化工作流，帮助 AI 助手在进入实现前先做架构决策。

它是一个 **Skill/文档仓库**，不是代码工程、npm 包或脚手架模板。

---

## 为什么 Vibe Coding 要先做架构

很多 AI 编程失败，并不是 AI 不会写代码，而是起点阶段产品定义不清晰。

如果产品类型、系统边界、数据流、API Contract 和 MVP 范围不明确，后续实现往往不稳定且迭代成本高。

**核心原则：写代码前，先明确架构。**

---

## 这个 Skill 解决什么问题

没有架构前置阶段时，AI 往往会过早进入编码。

这个 Skill 强制 AI 先回答关键问题：

- 这是什么产品类型？
- 它是落地页、SaaS、仪表盘、本地应用、自动化工作流、浏览器插件、API 服务还是 AI 工具？
- 它需要前端单体、全栈、本地优先、云优先还是混合架构？
- 是否需要鉴权、数据库、存储、队列、定时任务、API、后台任务或模型路由？
- MVP 应该包含什么？
- 哪些功能暂时不该做？
- 需要怎样的数据模型？
- 需要怎样的 API Contract？
- 关键技术风险是什么？
- 最终该给 Codex、Claude Code、Cursor 等工具什么 coding prompt？

---

## 什么时候使用

当需求仍然模糊、但有人准备让 AI “直接开始写”时，就应该使用它。

典型场景：

- “帮我做一个……”
- “我该用什么技术栈？”
- “给我一个 Codex 提示词。”
- “我想做 Vibe Coding。”

---

## 这个 Skill 帮 AI 决策什么

- 产品类型
- 架构方向
- MVP 边界
- 数据模型需求
- API Contract 需求
- 关键风险与缓解方案
- 最终实现提示词

---

## 如何使用

1. 打开 `SKILL.md`，按 9 步流程执行。
2. 用 `references/architecture-checklist.md` 做编码前检查。
3. 参考 `examples/` 中的产品类型示例。
4. 只有架构结论完成后再生成最终 coding prompt。

---

## 请求示例

- “我想做一个本地优先的 Prompt 管理工具。请先用 Vibe Coding Architecture Skill 做架构决策输出。”
- “写代码前请先判断产品类型，并按 must/should/later/do-not-build-yet 定义 MVP。”
- “请按此仓库 Skill 格式，在 API Contract 明确后再给我 Cursor 的最终 coding prompt。”

---

## 使用示例

### 输入示例

> 我想做一个自动化工具：输入主题，生成初稿，审核，然后保存到文档。

### 期望行为

AI 不应直接开始写代码，而应先输出：

1. 产品摘要
2. 产品类型
3. 推荐架构
4. 推荐技术栈
5. MVP 范围（Must/Should/Later/Do not build yet）
6. 数据模型
7. API Contract
8. 关键风险与缓解
9. 最终 coding prompt

完整输出可参考 `examples/automation-workflow.md`。

---

## 仓库结构

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
