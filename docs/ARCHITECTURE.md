# Architecture

## Application
Single Next.js application.

Suggested routes:

/
 /signup
 /login
 /onboarding
 /onboarding/industry
 /onboarding/business
 /onboarding/photos
 /generate
 /designs
 /editor
 /preview
 /dashboard
 /dashboard/site
 /dashboard/photos
 /dashboard/support
 /dashboard/billing
 /dashboard/domain
 /s/[slug]

## Main modules
- auth
- business
- industry-config
- photos
- ai-generation
- themes
- editor
- publishing
- billing
- support
- analytics

## Industry configuration approach
Create an industry config layer.

Example:
industryConfigs = {
  salon: {...},
  restaurant: {...}
}

The renderer and editor should consume config rather than duplicate pages.

## Theme approach
Use one normalized site data schema.
Render it through 3 theme components.

Example:
- PremiumTheme
- NaturalTheme
- ModernTheme

Do not create separate databases per theme.

## AI provider abstraction
Create a provider interface so model/vendor can change later.

Functions:
- generateBusinessCopy()
- generateFaq()
- generateSeo()
- suggestSectionOrder()

Never hardcode the entire app to one AI vendor.

## Storage
Use object storage.
Persist only storage paths/metadata in Postgres.

## Publishing
MVP public route:
`/s/[slug]`

Later, map subdomains/custom domains to the same business record.
