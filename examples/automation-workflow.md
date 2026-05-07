# Example: Automation Workflow

## User Request

“I want to build an automation tool that takes a topic, generates a draft, reviews it, and saves it to a document.”

## Architecture Decision

### 1. Product Type

Automation workflow / Agent workflow.

### 2. Recommended Architecture

Workflow-first architecture with explicit task states.

Rationale: Value is in multi-step orchestration and observable state transitions, not UI complexity.

### 3. Recommended Tech Stack

- Orchestration layer: Node.js service with workflow module
- API: REST endpoints for job creation and status retrieval
- Storage: PostgreSQL (jobs, steps, outputs)
- Optional queue (later): Redis-based queue
- Optional scheduler (later): cron for recurring runs
- Deployment: managed container platform

### 4. MVP Scope

#### Must Have

- Submit topic
- Run sequential steps: draft -> review -> save
- Persist job status and outputs
- View status and final document link

#### Should Have

- Retry failed step
- Basic run logs

#### Later

- Parallel branches
- Scheduled runs
- Human approval checkpoints

#### Do Not Build Yet

- Multi-tenant billing platform
- Complex distributed queue system

### 5. Data Model

- WorkflowJob(id, topic, status, created_at, completed_at)
- WorkflowStep(id, job_id, step_name, status, input_json, output_json, started_at, ended_at)
- DocumentArtifact(id, job_id, storage_url, format, created_at)

Status strategy:

- Job: `queued | running | completed | failed`
- Step: `pending | running | completed | failed`

### 6. API Contract

- `POST /api/workflows`
  - Request: `{ topic }`
  - Response: `{ jobId, status }`
- `GET /api/workflows/:jobId`
  - Response: `{ jobId, status, steps, artifact? }`
- `POST /api/workflows/:jobId/retry`
  - Request: `{ stepName }`
  - Response: `{ jobId, status }`

Error format:

`{ error: { code, message, retriable } }`

Status flow:

`queued -> running -> completed | failed`

### 7. Key Risks

- Product risk: low output usefulness. Mitigation: define quality rubric for review step.
- Technical risk: step failure propagation. Mitigation: isolate steps and store intermediate output.
- Model/API risk: inconsistent model responses. Mitigation: schema-validated outputs per step.
- Cost risk: excessive retries. Mitigation: retry cap and alerting.
- UX risk: unclear progress visibility. Mitigation: expose step-level timeline.
- Deployment risk: long-running task timeouts. Mitigation: async worker separation.

### 8. Final Coding Prompt

Build an MVP automation workflow service that accepts a topic, generates a draft, reviews it, and saves a final document artifact. Use a workflow-first design with explicit job/step states, REST APIs for create/status/retry, and PostgreSQL for persistence. Implement synchronous sequential orchestration first; keep queue/cron as future extensions. Define entities WorkflowJob, WorkflowStep, and DocumentArtifact, with status enums and transition rules. Return standardized error responses and expose step-level progress. Provide a practical folder structure, implementation sequence, and acceptance criteria focused on reliable state handling.
