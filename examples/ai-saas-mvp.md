# Example: AI SaaS MVP

## User Request

“I want to build an AI tool that helps users generate product descriptions from product photos.”

## Architecture Decision

### 1. Product Type

Primary: AI generation tool  
Secondary: SaaS MVP

Rationale: The product generates text from image input and requires user accounts, usage tracking, and hosted access.

### 2. Recommended Architecture

Full-stack SaaS.

Rationale: Needs frontend upload flow, backend orchestration, persistent history, auth, and storage for images.

### 3. Recommended Tech Stack

- Frontend: Next.js + TypeScript + Tailwind
- Backend API: Next.js Route Handlers (or separate Node API)
- Database: PostgreSQL
- Authentication: Auth.js / Clerk
- Object Storage: S3-compatible storage
- AI Model API: Vision-capable model + text generation model
- Deployment: Vercel (app) + managed Postgres

### 4. MVP Scope

#### Must Have

- Sign up / sign in
- Upload product photo
- Generate one description variation
- Save generation history
- Basic usage limit per user

#### Should Have

- Tone/style options
- Regenerate button
- Copy/export text

#### Later

- Team workspaces
- Multi-language output
- Batch generation

#### Do Not Build Yet

- Complex billing plans
- Fine-tuned model pipeline
- Enterprise permission system

### 5. Data Model

- User(id, email, created_at)
- Project(id, user_id, name, created_at)
- Asset(id, user_id, storage_url, mime_type, created_at)
- Generation(id, user_id, asset_id, prompt, output_text, status, tokens_used, created_at)

Relationships:

- User 1..N Projects
- User 1..N Assets
- Asset 1..N Generations

### 6. API Contract

- `POST /api/generations`
  - Request: `{ assetId, style, maxLength }`
  - Response: `{ generationId, status, outputText }`
- `GET /api/generations/:id`
  - Response: `{ generationId, status, outputText, createdAt }`
- `GET /api/history`
  - Response: `{ items: GenerationSummary[] }`

Error format:

`{ error: { code, message, details? } }`

Status flow:

`uploaded -> processing -> completed | failed`

### 7. Key Risks

- Product risk: low retention if output quality is weak. Mitigation: add clear style presets and fast feedback.
- Technical risk: large image upload failures. Mitigation: client-side compression and signed upload URLs.
- Model/API risk: provider latency variance. Mitigation: timeout + retry + fallback model.
- Cost risk: generation cost spikes. Mitigation: rate limits and token/image quotas.
- UX risk: users unclear why output changed. Mitigation: show prompts and model settings used.

### 8. Final Coding Prompt

Build a full-stack SaaS MVP for generating product descriptions from uploaded product photos. Use Next.js + TypeScript + Tailwind for UI and API routes, PostgreSQL for persistence, Auth.js (or Clerk) for auth, and S3-compatible storage for image files. Implement sign-in, image upload, generation endpoint, history list, and status tracking with states `uploaded`, `processing`, `completed`, `failed`. Keep MVP scope limited to single-user projects and one-generation-at-a-time flow. Define entities User, Project, Asset, Generation with clear relations. Implement endpoints `POST /api/generations`, `GET /api/generations/:id`, and `GET /api/history` with standardized error format. Provide a clean dashboard UI with upload, generate, and history panels. Include a simple folder structure, implementation steps, and acceptance criteria focused on end-to-end reliability.
