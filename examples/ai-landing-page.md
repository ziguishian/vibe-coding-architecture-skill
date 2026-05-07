# Example: AI Landing Page

## User idea

I want to build a landing page for an AI product. It should introduce the product, show features, pricing, and a call-to-action button.

## Expected Skill behavior

The assistant should not recommend a full backend or database in the first version.

## Architecture decision

### Product type

Static landing page / marketing website.

### Recommended architecture

Frontend-only static site.

### Recommended stack

- Frontend: Next.js or Astro
- Styling: Tailwind CSS
- Content: Markdown or local JSON
- Deployment: Vercel, Netlify, or static hosting
- Backend: Not needed for MVP
- Database: Not needed for MVP
- Auth: Not needed for MVP

### MVP scope

#### Must have

- Hero section
- Problem section
- Solution section
- Feature cards
- Product screenshots or mockups
- Pricing section
- CTA button
- Footer

#### Should have

- FAQ section
- Email capture through a third-party form service
- SEO metadata

#### Later

- User dashboard
- Payment integration
- Product analytics
- CMS

#### Do not build yet

- Custom backend
- User system
- Complex admin panel
- Database schema

### Data model

No database needed for MVP. Static content can live in Markdown, JSON, or component props.

### API contract

No internal API needed for MVP. If email capture is needed, use a third-party form API.

### Key risks

- Overbuilding: Avoid full-stack setup before validating positioning.
- Weak conversion: Prioritize copywriting and visual hierarchy.
- Generic design: Use a strong design system and product screenshots.

### Final coding prompt

Build a static AI product landing page using Next.js and Tailwind CSS. The page should include hero, problem, solution, features, pricing, FAQ, CTA, and footer. Do not add backend, database, or authentication. Use componentized sections and clean responsive design. Optimize for high-end AI startup visual style, clear information hierarchy, and fast deployment.
