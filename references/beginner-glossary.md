# Beginner Glossary

## Frontend

The interface users see and operate.

You can understand it as: the shop window and control panel of the software.

When you need it: almost every website, app, dashboard, or tool needs a frontend.

When you do not need it: pure backend APIs or invisible automation jobs may not need one.

## Backend

The part behind the software that handles rules, data, and external services.

You can understand it as: the worker behind the counter.

When you need it: login, database writes, payments, AI calls, permissions, or business rules.

When you do not need it: simple static pages without forms or dynamic data.

## Database

The long-term memory of the software.

You can understand it as: a structured notebook that remembers users, orders, articles, tasks, and settings.

When you need it: data must be saved and queried later.

When you do not need it: a landing page or static portfolio.

## API

The conversation protocol between frontend and backend.

You can understand it as: a menu that says what the frontend can ask for and what the backend will return.

When you need it: frontend and backend exchange data.

When you do not need it: static websites with no dynamic backend.

## REST API

An API style based on URLs and HTTP methods such as GET, POST, PATCH, and DELETE.

You can understand it as: using different service windows for different actions.

When you need it: most MVP web apps and SaaS products.

When you do not need it: very simple local-only tools.

## GraphQL

An API style where the frontend asks for exactly the fields it wants.

You can understand it as: ordering a custom meal instead of choosing a fixed menu.

When you need it: complex clients with many flexible data needs.

When you do not need it: most beginner MVPs, because REST is simpler.

## Authentication

Checking who you are.

You can understand it as: showing your ID before entering.

When you need it: private accounts, user history, subscriptions, or dashboards.

When you do not need it: public landing pages.

## Authorization

Checking what you are allowed to do.

You can understand it as: having different keys for different rooms.

When you need it: admins, team members, paid users, or private resources.

When you do not need it: single-user tools with no roles.

## Object storage

A warehouse for images, videos, PDFs, and attachments.

You can understand it as: a file warehouse separate from the database.

When you need it: users upload or generate files.

When you do not need it: the product only stores text and structured records.

## CDN

A network that delivers static assets from locations closer to users.

You can understand it as: many nearby pickup points for website files.

When you need it: public sites, images, downloads, and global audiences.

When you do not need it: small internal tools with few users.

## Serverless

A deployment model where you run functions without managing servers directly.

You can understand it as: renting a kitchen only when you need to cook.

When you need it: small APIs, webhooks, and event-driven tasks.

When you do not need it: long-running jobs or complex server state.

## Edge Function

A serverless function running close to users geographically.

You can understand it as: a small service desk near each user.

When you need it: low-latency requests and lightweight logic.

When you do not need it: heavy backend processing.

## Queue

A waiting line for time-consuming tasks.

You can understand it as: putting jobs in order so workers process them calmly.

When you need it: batch processing, AI generation, video processing, or retries.

When you do not need it: quick requests that finish immediately.

## Cron

A scheduled task that runs at fixed times.

You can understand it as: an alarm clock for software.

When you need it: daily reports, cleanup jobs, or periodic sync.

When you do not need it: products with only user-triggered actions.

## Webhook

A notification sent automatically from one service to another.

You can understand it as: one system ringing another system's doorbell when something happens.

When you need it: payments, form tools, GitHub events, or third-party callbacks.

When you do not need it: fully self-contained apps.

## Logs

The running diary of the software.

You can understand it as: records of what happened and what went wrong.

When you need it: every production app.

When you do not need it: throwaway demos, though even demos benefit from basic errors.

## Monitoring

The health check system of the software.

You can understand it as: a dashboard that warns you when the product is sick.

When you need it: public products and paid services.

When you do not need it: very early local prototypes.

## Cache

Temporary memory used to make repeated access faster.

You can understand it as: keeping frequently used items on the desk instead of in the archive room.

When you need it: repeated expensive queries or slow API calls.

When you do not need it: simple MVPs with low traffic.

## SaaS

Software sold or delivered as an online service.

You can understand it as: users log in and use the product through the web, often with plans or subscriptions.

When you need it: multi-user online products.

When you do not need it: personal local tools.

## MVP

The minimum version that completes the core user value loop.

You can understand it as: the smallest product that proves whether the idea works.

When you need it: almost every new product.

When you do not need it: mature products with confirmed scope.

## Local-first

Software that stores and works with data primarily on the user's device.

You can understand it as: the user's computer is the main home of the data.

When you need it: privacy, offline use, or personal tools.

When you do not need it: team collaboration and centralized business systems.

## Cloud-first

Software that stores and runs mainly in cloud services.

You can understand it as: the product lives online so users can access it anywhere.

When you need it: SaaS, shared dashboards, and web apps.

When you do not need it: private single-user desktop utilities.

## API Contract

A written agreement about request data, response data, errors, and permissions.

You can understand it as: the rulebook for frontend-backend communication.

When you need it: any app with frontend-backend communication or third-party services.

When you do not need it: static pages without backend interaction.
