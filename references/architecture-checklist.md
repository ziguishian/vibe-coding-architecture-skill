# Architecture Checklist for Vibe Coding

Use this checklist before asking AI to generate code.

## Product Type

- [ ] I can clearly classify the product type.
- [ ] I can explain why this type fits better than alternatives.
- [ ] I identified whether it is single-mode or mixed-mode (primary + secondary type).

## Architecture Direction

- [ ] I chose one architecture direction (frontend-only, full-stack, local-first, cloud-first, hybrid, etc.).
- [ ] I documented why this direction is the simplest valid choice for MVP.
- [ ] I confirmed the architecture matches user workflow and constraints.

## Frontend

- [ ] I know whether a frontend UI is required.
- [ ] I defined the core user interaction flow.
- [ ] I limited UI scope to MVP-critical screens/components.

## Backend

- [ ] I verified whether backend logic is truly necessary.
- [ ] I identified required backend responsibilities.
- [ ] I avoided creating backend services without clear MVP need.

## Database

- [ ] I verified whether persistent data storage is needed.
- [ ] I listed core entities and required fields.
- [ ] I avoided adding a database when files/local state are enough.

## Authentication

- [ ] I verified whether user accounts are required in MVP.
- [ ] I selected auth only if identity/permissions are needed.
- [ ] I avoided premature multi-role auth design.

## Storage

- [ ] I identified whether file/object storage is required.
- [ ] I clarified storage type (local, object storage, provider-managed).
- [ ] I defined retention and access needs for MVP.

## AI Model Layer

- [ ] I identified which model capabilities are needed (text, vision, tool use, etc.).
- [ ] I defined model call boundaries and fallback behavior.
- [ ] I estimated basic cost/latency constraints.

## API Contract

- [ ] I verified whether internal/external APIs are needed.
- [ ] I defined endpoint, method, request, response, and error format.
- [ ] I documented status transitions for async operations.

## Background Jobs

- [ ] I verified whether queue/worker/cron is needed for MVP.
- [ ] I avoided adding background infrastructure prematurely.
- [ ] I documented future upgrade path if deferred.

## Deployment

- [ ] I chose a deployment target aligned with MVP complexity.
- [ ] I verified runtime and environment requirements.
- [ ] I minimized operational overhead for first release.

## MVP Scope

- [ ] I split scope into Must have / Should have / Later / Do not build yet.
- [ ] I removed non-essential features from MVP.
- [ ] I can explain what is intentionally excluded.

## Risks

- [ ] I listed key product and technical risks.
- [ ] I listed model/API, cost, UX, deployment, and maintenance risks.
- [ ] I added at least one mitigation per major risk.
