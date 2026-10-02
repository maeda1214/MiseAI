# Implementation Plan for Codex

Execute in this order.

## Phase 1 - Bootstrap
- Create Next.js TypeScript app
- Configure Tailwind
- Configure linting
- Add env example
- Add project folder structure

## Phase 2 - Supabase
- Add Supabase client/server setup
- Auth
- SQL migrations
- RLS
- Seed/demo data

## Phase 3 - Onboarding
- Signup/login
- Industry selection
- Business form
- Restaurant-specific fields
- Salon-specific fields
- Form validation

## Phase 4 - Photos
- Upload
- Delete
- Reorder
- Minimum 10 validation
- Gallery metadata

## Phase 5 - AI generation
- Provider abstraction
- Generate copy
- FAQ
- SEO
- section ordering
- graceful mock mode when no AI key exists

## Phase 6 - Themes
- Build 3 themes
- Same content schema
- Mobile-first
- Photo-heavy
- Lightbox enlargement

## Phase 7 - Editor
- Edit all content
- Save drafts
- Preview

## Phase 8 - Publish
- Slug validation
- Public route
- Publish/unpublish
- SEO metadata
- LocalBusiness/Restaurant structured data

## Phase 9 - Billing
- Stripe products/prices
- Checkout
- Webhook
- Subscription status
- Billing portal

## Phase 10 - Support
- Request form
- Monthly counter
- 10 included requests
- 11th+ marked billable at ¥2,000

## Phase 11 - QA
- Responsive test
- Auth security
- RLS test
- Publish test
- Stripe test mode
- Restaurant and salon full user journeys

## Definition of MVP done
A completely new user can:
1. Sign up
2. Choose salon or restaurant
3. Enter business info
4. Upload 10+ photos
5. Generate 3 designs
6. Pick one
7. Edit it
8. Preview it
9. Publish it
10. Receive LINE/phone/reservation clicks
11. Subscribe to ¥9,800 support plan
12. Submit support requests
