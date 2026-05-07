# Example: Landing Page

## User Request

“I want to build a landing page for my AI startup.”

## Architecture Decision

### 1. Product Type

Static landing page.

### 2. Recommended Architecture

Frontend-only.

Rationale: Marketing page does not require persistent data, user accounts, or complex business logic.

### 3. Recommended Tech Stack

- Framework: Next.js or Astro
- Styling: Tailwind CSS
- Forms: simple email capture service (optional)
- Deployment: Vercel or Cloudflare Pages

### 4. MVP Scope

#### Must Have

- Hero section with value proposition
- Feature highlights
- Social proof/testimonials section
- CTA buttons
- Contact or waitlist form

#### Should Have

- FAQ section
- Basic SEO metadata

#### Later

- Blog/content system
- A/B testing

#### Do Not Build Yet

- Custom backend
- User login
- Database-driven dashboard

### 5. Data Model

No database required for MVP.

Reason: Static content + optional third-party form handling is enough.

### 6. API Contract

No internal API required for MVP.

Reason: Frontend-only deployment with optional external form endpoint.

### 7. Final Coding Prompt

Build a static landing page for an AI startup using Next.js (or Astro) and Tailwind CSS. Keep architecture frontend-only with no custom backend, no auth, and no database. Include hero, feature sections, social proof, CTA, and contact/waitlist form. Optimize for performance and SEO basics, and deploy to Vercel or Cloudflare Pages. Provide clear file structure, component breakdown, implementation steps, and acceptance criteria focused on clarity, speed, and conversion readiness.
