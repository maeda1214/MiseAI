# First Prompt to Give Codex

You are the lead engineer for a project called MiseAI.

Read every file in this repository before changing code, especially:
- README.md
- docs/PRD.md
- docs/MVP_SCOPE.md
- docs/SCREENS.md
- docs/DATABASE.md
- docs/ARCHITECTURE.md
- docs/IMPLEMENTATION_PLAN.md

Goal:
Build the MVP of MiseAI, a Japanese AI website builder for beauty salons and restaurants.

Rules:
1. Follow MVP scope exactly.
2. Do not add speculative features.
3. Build one shared multi-industry platform, not two separate apps.
4. Use Next.js App Router + TypeScript.
5. Use Supabase for Auth, Postgres, and Storage.
6. Use Stripe for the paid support subscription.
7. Use mobile-first UI.
8. Public sites are single-page and photo-focused.
9. Restaurant menu data must be structured, not just free text.
10. All private data must be protected by RLS.
11. Keep AI integration behind a provider abstraction.
12. If API credentials are missing, create a mock generation mode so development continues.
13. Use Japanese UI copy by default.
14. Keep implementation simple and production-oriented.

Start with Phase 1 from docs/IMPLEMENTATION_PLAN.md.
Before coding, inspect the existing repository and report:
- current state
- files you will create/change
- first implementation step

Then implement Phase 1 only.
After Phase 1, stop and summarize completed work and remaining tasks.
