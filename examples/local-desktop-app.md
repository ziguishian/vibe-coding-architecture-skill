# Example: Local-First Desktop App

## User Request

“I want to build a local-first desktop app that helps me organize prompts and run them with different AI APIs.”

## Architecture Decision

### 1. Product Type

Local desktop app.

Rationale: Primary usage is personal productivity with local data control and desktop-native behavior.

### 2. Recommended Architecture

Local-first desktop app.

Rationale: No SaaS requirement at MVP stage; user data and API keys should remain on-device.

### 3. Recommended Tech Stack

- Desktop Shell: Tauri
- Frontend: React + TypeScript
- Local Database: SQLite
- Secrets Storage: OS keychain integration
- AI API Layer: local adapter module for multi-provider calls
- Packaging: Tauri bundler for macOS/Windows/Linux

### 4. MVP Scope

#### Must Have

- Create/edit/delete prompts
- Organize prompts by folders/tags
- Save multiple provider configurations
- Execute prompt with selected provider
- Save run history locally

#### Should Have

- Prompt templates
- Variable placeholders
- Response comparison view

#### Later

- Cloud sync
- Team collaboration
- Plugin system

#### Do Not Build Yet

- Multi-tenant SaaS backend
- Server-side user auth
- Billing and subscriptions

### 5. Data Model

- Prompt(id, title, content, tags, created_at, updated_at)
- ProviderProfile(id, provider_name, model_name, api_key_ref, config_json, created_at)
- RunRecord(id, prompt_id, provider_profile_id, input_json, output_text, latency_ms, status, created_at)

Storage strategy:

- SQLite for app data
- API keys stored in OS keychain; database only stores key reference

### 6. Key Risks

- Product risk: scope drifts into SaaS too early. Mitigation: freeze MVP to single-device usage.
- Technical risk: provider API differences. Mitigation: unified adapter interface per provider.
- Security risk: key leakage. Mitigation: never persist raw keys in plain text.
- UX risk: complex provider setup. Mitigation: guided setup flow with validation.
- Maintenance risk: desktop packaging issues. Mitigation: automated build matrix early.

### 7. Final Coding Prompt

Build a local-first desktop application using Tauri + React + TypeScript for organizing prompts and running them against different AI providers. Use SQLite for local persistence and OS keychain for API key storage. Implement prompt CRUD, folder/tag organization, provider profiles, execution runner, and local run history. Do not build SaaS backend, cloud sync, or account system in MVP. Create a provider adapter layer to normalize request/response handling across APIs. Deliver a clean desktop UI with sections for Prompts, Providers, and Runs, plus practical folder structure, implementation plan, and acceptance criteria.
