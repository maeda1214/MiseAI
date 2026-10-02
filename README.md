# MiseAI - Codex Handoff

MiseAI is a Japanese-market AI website builder for small local businesses.

Initial supported industries:
1. Beauty salons
2. Restaurants

Core concept:
- Free website creation
- AI-generated 1-page site
- 3 design variants
- LINE-based reservation flow
- Free subdomain
- Optional custom domain
- Free plan funded by ads
- Paid maintenance plan: ¥9,800/month
- Up to 10 support requests/month
- 11th+ request: ¥2,000/request

## Recommended stack
- Next.js (App Router)
- TypeScript
- Supabase
  - Auth
  - Postgres
  - Storage
- Stripe Billing for MVP subscription
- Tailwind CSS
- Zod
- React Hook Form
- AI provider abstraction layer
- Deployment provider must allow commercial use

## Codex workflow
1. Read all files in `/docs`
2. Build only MVP scope from `docs/MVP_SCOPE.md`
3. Create database from `docs/DATABASE.md`
4. Create screens from `docs/SCREENS.md`
5. Follow `docs/IMPLEMENTATION_PLAN.md` in order
6. Do not add extra features without explicit approval
7. Keep the architecture ready for more industries later

## Important product rule
The same core system must support multiple industries.
Do not create separate applications for salon and restaurant.
Use industry-specific schemas/configuration inside one platform.
