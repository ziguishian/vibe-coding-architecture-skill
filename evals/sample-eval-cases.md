# Sample Evaluation Cases

## 1. Very vague project idea

Input: "I want to build an app that helps people work better."

Expected output focus: preliminary judgment, 5-10 beginner-friendly questions, avoid choosing a heavy stack too early.

Common mistakes: pretending requirements are clear, recommending SaaS architecture immediately.

Recommended scoring focus: understanding, questions, avoiding over-engineering.

## 2. Personal website

Input: "I want a personal website with projects, articles, and contact info."

Expected output focus: static/content website, no backend/database for MVP, clear pages.

Common mistakes: adding login, CMS, database too early.

Recommended scoring focus: classification, MVP scope, tech stack reasoning.

## 3. AI SaaS

Input: "I want an AI writing SaaS with login, quota, and generation history."

Expected output focus: full-stack AI SaaS, managed auth, database, server-side AI calls, quota.

Common mistakes: exposing API keys on frontend, ignoring cost and usage tracking.

Recommended scoring focus: API Contract, data model, cost and model risk.

## 4. E-commerce tool

Input: "I want to build a small online store for digital products."

Expected output focus: products, orders, checkout, payment provider, file delivery, admin view.

Common mistakes: custom payment implementation, marketplace features too early.

Recommended scoring focus: data model, permissions, payment risk.

## 5. Mobile app

Input: "I want a habit tracking mobile app with reminders."

Expected output focus: mobile-first app, local data or BaaS, notifications later, simple MVP loop.

Common mistakes: building web dashboard first, overcomplicated social features.

Recommended scoring focus: product type, MVP scope, future expansion.

## 6. Desktop app

Input: "I want a local desktop app to manage my prompts."

Expected output focus: local-first desktop architecture, SQLite, no cloud auth for MVP.

Common mistakes: SaaS architecture, unnecessary backend.

Recommended scoring focus: local-first principle, data model, non-goals.

## 7. Enterprise admin dashboard

Input: "We need an internal dashboard for customers, orders, employees, and reports."

Expected output focus: admin dashboard, roles, CRUD, reports, operation logs.

Common mistakes: no permission model, no audit thinking, too many report features.

Recommended scoring focus: permissions, risks, API Contract.

## 8. Automation tool

Input: "I want to upload spreadsheets and automatically generate reports."

Expected output focus: upload, validation, processing, generated output, task status.

Common mistakes: no file handling plan, no failure states, adding visual workflow builder too early.

Recommended scoring focus: file storage, background tasks, error handling.

## 9. Browser extension

Input: "I want a Chrome extension that summarizes the current page with AI."

Expected output focus: Manifest V3 extension, content script, popup, backend for AI API key protection.

Common mistakes: putting model API key in extension frontend, requesting too many permissions.

Recommended scoring focus: product type, permissions, model/API risk.

## 10. Xiaohongshu content tool

Input: "I want a Xiaohongshu topic-to-carousel-copy generator."

Expected output focus: AI content tool, prompt templates, structured output, optional history.

Common mistakes: building image editor first, ignoring output quality and cost.

Recommended scoring focus: MVP scope, AI integration, upgrade path.
