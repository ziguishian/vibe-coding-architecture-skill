# Common Architecture Patterns

## Static Site

Suitable for: landing pages, portfolios, documentation.

Not suitable for: login, user data, dashboards.

Core modules: pages, content files, assets, hosting.

Recommended tech stack: Astro, Next.js static export, Vercel, Cloudflare Pages.

Common pitfalls: adding a backend before there is dynamic data.

Upgrade direction: add CMS, forms, analytics, search.

## Full-stack Web App

Suitable for: login-based products with pages, API, and database.

Not suitable for: simple static sites.

Core modules: frontend, backend routes, database, auth.

Recommended tech stack: Next.js, PostgreSQL, managed auth.

Common pitfalls: unclear API Contract and mixed permission rules.

Upgrade direction: extract services only after clear scaling pressure.

## BaaS-backed App

Suitable for: beginner MVPs needing auth, database, and storage quickly.

Not suitable for: highly customized backend rules.

Core modules: frontend, BaaS auth, database, storage, server functions.

Recommended tech stack: Supabase or Firebase.

Common pitfalls: weak row-level security and unclear pricing.

Upgrade direction: add custom backend for complex business rules.

## Serverless App

Suitable for: lightweight APIs, forms, webhooks, AI calls.

Not suitable for: long-running jobs.

Core modules: frontend, functions, managed database, logs.

Recommended tech stack: Vercel Functions, Cloudflare Workers, Supabase.

Common pitfalls: timeout limits and hidden usage costs.

Upgrade direction: add workers, queues, or container backend.

## AI Wrapper App

Suitable for: products wrapping LLM APIs with a specific workflow.

Not suitable for: vague "chat with everything" products.

Core modules: prompt templates, backend model calls, usage tracking, history.

Recommended tech stack: Next.js, PostgreSQL, server-side AI SDK/API calls.

Common pitfalls: exposing API keys, ignoring cost, not saving inputs/outputs.

Upgrade direction: add model routing, evaluation, quotas, and queues.

## Admin Dashboard

Suitable for: internal management of customers, orders, reports.

Not suitable for: public marketing pages.

Core modules: auth, roles, CRUD, filters, reports.

Recommended tech stack: React/Next.js, backend API, PostgreSQL.

Common pitfalls: no audit trail and unclear admin permissions.

Upgrade direction: workflow approvals, exports, analytics.

## Content Management Tool

Suitable for: writing, editing, scheduling, and publishing content.

Not suitable for: pure static pages without editors.

Core modules: editor, content database, media storage, publishing workflow.

Recommended tech stack: Next.js, PostgreSQL, object storage.

Common pitfalls: building complex collaboration too early.

Upgrade direction: roles, review flow, publishing integrations.

## Automation Workflow

Suitable for: batch processing, reporting, scheduled tasks.

Not suitable for: immediate interactive-only pages.

Core modules: input, processing logic, task status, output files.

Recommended tech stack: backend worker, queue when needed, object storage.

Common pitfalls: no retry strategy and no progress visibility.

Upgrade direction: queue, scheduler, webhook triggers.

## Local-first Desktop App

Suitable for: prompt managers, notes, personal tools.

Not suitable for: team SaaS from day one.

Core modules: desktop shell, local database, local files, export/import.

Recommended tech stack: Tauri/Electron, SQLite.

Common pitfalls: adding cloud auth before local value is proven.

Upgrade direction: optional sync and encryption.

## Mobile App

Suitable for: camera, notifications, location, mobile-first use.

Not suitable for: desktop-heavy admin work.

Core modules: mobile UI, local state, API/BaaS, push notifications later.

Recommended tech stack: React Native or Flutter.

Common pitfalls: building native iOS and Android separately too early.

Upgrade direction: offline sync and native integrations.

## Browser Extension

Suitable for: augmenting web pages and browser workflows.

Not suitable for: products that do not need browser context.

Core modules: manifest, popup, content script, storage.

Recommended tech stack: TypeScript, Manifest V3.

Common pitfalls: unclear permission requests and fragile page scraping.

Upgrade direction: sync backend and AI assistant.

## Internal Tool

Suitable for: team operations, manual workflows, approvals.

Not suitable for: consumer products with polished onboarding needs.

Core modules: auth, roles, forms, tables, reports.

Recommended tech stack: Retool-like tools, Next.js, PostgreSQL.

Common pitfalls: ignoring permission boundaries.

Upgrade direction: audit logs and workflow automation.

## API-first Product

Suitable for: developer-facing services.

Not suitable for: products whose main value is visual UI.

Core modules: API, docs, keys, rate limits, logs.

Recommended tech stack: FastAPI/Express/Hono, OpenAPI, PostgreSQL.

Common pitfalls: weak error format and no usage tracking.

Upgrade direction: billing, dashboard, SDKs.

## Agent Workflow

Suitable for: repeatable AI-assisted task execution.

Not suitable for: unclear autonomous systems with no acceptance criteria.

Core modules: planner, tools, state, logs, approval points.

Recommended tech stack: agent SDK or orchestration layer, state store, logs.

Common pitfalls: too much autonomy and no recovery path.

Upgrade direction: evaluations, queues, human review, multi-agent coordination.
