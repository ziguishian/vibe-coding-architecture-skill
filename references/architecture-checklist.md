# Pre-coding Architecture Checklist

Use this checklist before asking Codex or another AI coding agent to implement.

## Product type

- What kind of software is this?
- Is it a website, web app, SaaS, dashboard, automation tool, desktop app, mobile app, API, or agent workflow?
- Is there a primary type and secondary type?

## User roles

- Who uses the product?
- Are there admins, normal users, guests, operators, or paid members?
- What can each role see and do?

## MVP scope

- What is the smallest usable loop?
- What must be built now?
- What should be delayed?
- What should not be built yet?

## Frontend

- What pages or screens are needed?
- What data does each page display?
- What actions can users trigger?

## Backend

- What business rules must be handled behind the interface?
- Does the product need server-side validation?
- Does it call third-party services?

## Database

- Does the product need long-term memory?
- What are the core entities?
- What relationships exist between entities?

## Authentication

- Does the product need login?
- Is private user data involved?
- Are paid plans, quotas, or admin roles needed?

## File storage

- Will users upload images, videos, PDFs, or attachments?
- Are files public or private?
- How long should files be kept?

## AI model layer

- Which AI capability is needed?
- What input goes to the model?
- What output is expected?
- How are failures, retries, and cost limits handled?

## API Contract

- What endpoints are needed?
- What request and response formats are expected?
- What errors can happen?
- What permissions are required?

## Background tasks

- Are there long-running operations?
- Are scheduled tasks needed?
- Should task progress be visible to users?

## Deployment

- Where will the product run?
- Does the user prefer managed services?
- Are there regional access or compliance constraints?

## Logs

- What errors should be recorded?
- What user actions should be traceable?
- Who reviews production issues?

## Cost

- What services charge per usage?
- What happens if traffic suddenly increases?
- Are there monthly budget limits?

## Risks

- What can make the product fail?
- What can make it expensive?
- What can make it hard to maintain?

## Acceptance criteria

- How do we know the MVP is complete?
- What manual flows must work end to end?
- What should be explicitly excluded?
