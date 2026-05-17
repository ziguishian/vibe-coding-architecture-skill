# Tech Stack Guide

The exact choice depends on region, budget, access speed, and maintenance ability.

## 1. Personal website / portfolio

Recommended tech stack: Astro or Next.js static export, Markdown/MDX, Vercel or Cloudflare Pages.

Why it fits: content is mostly public and rarely needs a backend.

What not to use: database, authentication, complex CMS, microservices.

MVP version: static pages for profile, works, articles, and contact.

Future upgrade version: add headless CMS, newsletter, analytics, or search.

## 2. Xiaohongshu content tool / carousel generation tool

Recommended tech stack: Next.js, serverless API routes, PostgreSQL/Supabase for history, object storage for generated images, LLM API.

Why it fits: users need input forms, generated outputs, history, and possibly image export.

What not to use: microservices or complex workflow engines in the first version.

MVP version: topic input, title generation, carousel copy, tag suggestions, export text.

Future upgrade version: image rendering, templates, team workspace, subscription quotas.

## 3. AI SaaS

Recommended tech stack: Next.js, PostgreSQL, managed auth, server-side AI calls, Stripe or equivalent billing later.

Why it fits: SaaS needs login, user data, usage records, and model cost control.

What not to use: frontend-only API key calls, untracked model usage, complex microservices.

MVP version: login, generation form, quota counter, history.

Future upgrade version: billing, team accounts, model routing, queue, monitoring.

## 4. Admin dashboard

Recommended tech stack: React/Next.js, backend API, PostgreSQL, role-based authorization.

Why it fits: dashboards manage structured business data and require permissions.

What not to use: static site only, no audit records, unclear roles.

MVP version: CRUD for core entities, filters, admin login.

Future upgrade version: audit logs, advanced reporting, exports, workflow approval.

## 5. E-commerce MVP

Recommended tech stack: Next.js, PostgreSQL, managed payment provider, object storage for product images.

Why it fits: orders, products, users, payments, and inventory are structured data.

What not to use: custom payment system or marketplace architecture too early.

MVP version: product list, checkout, order records, admin order view.

Future upgrade version: coupons, refunds, inventory sync, shipping integrations.

## 6. Data dashboard

Recommended tech stack: React/Next.js, PostgreSQL or data warehouse connection, chart library, scheduled import when needed.

Why it fits: dashboards need reliable data sources, filters, and visual summaries.

What not to use: real-time streaming unless truly required.

MVP version: upload/import data, key charts, filters, CSV export.

Future upgrade version: scheduled sync, alerts, permissions, cached metrics.

## 7. Automation workflow tool

Recommended tech stack: web UI or CLI, backend worker, queue only if tasks are long, file storage for inputs/outputs.

Why it fits: automation often has batch tasks and generated reports.

What not to use: visual workflow builder in the first version.

MVP version: upload spreadsheet, process rows, generate report, download result.

Future upgrade version: task queue, progress tracking, scheduling, webhooks.

## 8. Desktop app

Recommended tech stack: Tauri or Electron, SQLite, local file storage.

Why it fits: local-first tools benefit from offline access and user-owned data.

What not to use: cloud SaaS architecture unless sharing and sync are core.

MVP version: local CRUD, search, import/export.

Future upgrade version: optional sync, encryption, plugin system.

## 9. Mobile app

Recommended tech stack: React Native or Flutter, BaaS for auth/database when online sync is needed.

Why it fits: cross-platform development reduces first-version cost.

What not to use: separate native apps unless platform-specific behavior is critical.

MVP version: core mobile flow, login if needed, local cache.

Future upgrade version: push notifications, offline sync, native integrations.

## 10. Browser extension

Recommended tech stack: TypeScript, Manifest V3, lightweight backend only if sync or AI calls are needed.

Why it fits: extensions live inside the browser and interact with pages.

What not to use: full SaaS backend for a simple local extension.

MVP version: content script, popup, local settings.

Future upgrade version: account sync, cloud rules, AI assistant, analytics.

## 11. API service

Recommended tech stack: FastAPI, Express, Hono, or similar, PostgreSQL if persistent data is needed, OpenAPI docs.

Why it fits: API products need clear contracts, validation, and authentication.

What not to use: UI-first planning before defining endpoints.

MVP version: core endpoints, request validation, error format, docs.

Future upgrade version: rate limits, API keys, billing, monitoring.

## 12. Agent workflow

Recommended tech stack: orchestration layer, tool adapters, state store, logs, human approval steps.

Why it fits: agent systems need clear task state, tool permissions, and recovery behavior.

What not to use: fully autonomous multi-agent complexity before proving one workflow.

MVP version: one agent flow, explicit inputs, tool calls, final report.

Future upgrade version: queues, approvals, memory, evaluation, multi-provider routing.
