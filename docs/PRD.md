# MiseAI Product Requirements Document

## 1. Product
MiseAI

## 2. Target market
Japan

## 3. Initial industries
- Beauty salons
- Restaurants

## 4. Main value proposition
A business owner answers questions, uploads photos, and MiseAI generates a complete one-page website with reservation/contact flows.

## 5. User flow
1. Sign up
2. Select industry
3. Enter store/business information
4. Upload at least 10 photos
5. AI generates copy, SEO text, structure, and 3 design variants
6. User selects one design
7. User edits content
8. Preview
9. Publish
10. Manage site from dashboard

## 6. Shared business fields
- Business name
- Address
- Phone
- Opening hours
- Closed days
- Business description
- Features
- Pricing/menu
- LINE URL
- SNS URLs
- FAQ
- Reviews/testimonials
- Access information
- Campaigns
- Photos
- Reservation links
- Google Maps link

## 7. Beauty salon requirements
- No staff profile section
- Service menu
- Prices
- Salon features
- Before/after or style photos
- LINE reservation as primary CTA

## 8. Restaurant requirements
Additional fields:
- Restaurant category
- Cuisine category
- Menu categories
- Menu items
- Menu descriptions
- Prices
- Food photos
- Recommended dishes
- Lunch/dinner hours
- Number of seats
- Private room availability
- Smoking policy
- Payment methods
- Takeout availability
- Delivery availability
- External reservation URLs
- Tap-to-call reservation

Restaurant photo policy:
- Minimum 10 images
- No practical upper limit in product logic
- Food images should be able to be shown extensively
- Click/tap image to enlarge

## 9. Design generation
Generate 3 variants:
1. Premium / refined
2. Natural / friendly
3. Modern / simple

Restaurant wording may adapt style labels slightly, but keep the 3-variant system.

## 10. Page format
Single-page website.

## 11. Content ordering
AI may optimize section order by industry/business data.
Default tendencies:

Salon:
Photos -> Features -> Menu/Prices -> Reviews -> FAQ -> Access -> LINE reservation

Restaurant:
Photos -> Recommended dishes -> Menu/Prices -> Features -> Reservation -> Reviews -> Hours -> Access -> FAQ

Reservation CTA should appear multiple times and be prominent on mobile.

## 12. Editing
After publishing, business owner can edit all site content from dashboard.

## 13. Free plan
- ¥0
- Ads enabled
- Free subdomain
- Self-service editing
- Optional custom domain

## 14. Paid support plan
Price:
- ¥9,800/month

Includes:
- Up to 10 support/edit requests per month
- 1 request = 1 submitted request
- A single request can contain multiple edits
- 11th request onward = ¥2,000 per request

Request channels:
- Dashboard
- LINE

System should record LINE-originated requests in dashboard eventually.

## 15. Payments
MVP:
- Stripe subscription billing

Later:
- Add GMO Payment Gateway or equivalent for Japanese account debit support

## 16. Advertising
Free plan:
- Google AdSense
- Beauty/restaurant relevant affiliate ads

Placement:
- Primarily footer/bottom area
- Avoid degrading official-business-site trust
- Do not design click-inducing or deceptive placements

## 17. Domains
- Free platform subdomain
- Optional custom domain

## 18. Analytics
Business dashboard should eventually show:
- Page views
- LINE clicks
- Phone clicks
- Reservation link clicks

## 19. SEO
Generate:
- title
- meta description
- local SEO text
- alt text
- structured business data where appropriate
- sitemap
- robots metadata

## 20. Mobile
Mobile-first.
