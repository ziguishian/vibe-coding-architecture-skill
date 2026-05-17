# Architecture Principles

## MVP first

For a first version, prioritize a product that can run, validate demand, and iterate quickly.

Do not try to build the full imagined product at once. The MVP should complete the smallest usable loop.

## Monolith first

Start with one clear application when the team is small and the business rules are still changing.

Microservices are usually unnecessary for beginners because they add deployment, communication, debugging, and monitoring complexity.

## When frontend-backend separation is suitable

Use frontend-backend separation when:

- The frontend has many interactive pages
- The backend owns business rules and data
- Multiple clients may use the same backend
- API Contract clarity matters

Avoid it for simple static websites and landing pages.

## When Serverless is suitable

Serverless is suitable for:

- Small APIs
- Form submissions
- Webhooks
- Scheduled jobs
- AI tool MVPs with moderate traffic

Be careful with cold starts, runtime limits, vendor lock-in, and background jobs that run for a long time.

## When local-first is suitable

Local-first works well for:

- Personal productivity tools
- Prompt managers
- Notes and knowledge bases
- Desktop utilities
- Privacy-sensitive workflows

It is less suitable when real-time team collaboration, centralized permissions, or payment systems are core requirements.

## When BaaS is suitable

BaaS products such as Supabase and Firebase are suitable when beginners need authentication, database, storage, and simple APIs quickly.

They reduce maintenance burden but require understanding their permission model and pricing.

## Database selection principles

- Use no database for static landing pages.
- Use SQLite for local-first or small single-user tools.
- Use PostgreSQL for most SaaS, dashboards, and business apps.
- Use document databases only when data shape is highly flexible.
- Do not add Redis or search engines unless the use case truly needs them.

## File storage selection principles

Structured data goes in a database. Files such as images, videos, PDFs, and attachments go in object storage.

Use object storage when files are large, user-uploaded, or need public/private access rules.

## Authentication selection principles

If there are no accounts, do not add authentication.

If users need private data, quota, subscriptions, or roles, add authentication early and keep authorization rules simple.

## API Contract thinking

Before UI implementation, define:

- What data each page needs
- What actions users can trigger
- What request format the frontend sends
- What response format the backend returns
- How errors are represented
- How permissions are checked

API Contract is more important than UI before implementation.

## Avoiding over-engineering

Do not introduce complexity just to look professional.

If there are no long-running tasks, do not add a queue. If there are no files, do not add object storage. If there is no team collaboration, do not add complex permissions.
