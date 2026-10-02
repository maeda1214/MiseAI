# Database Design

Use Supabase Postgres.

## users
Managed primarily by Supabase Auth.

## businesses
- id uuid pk
- owner_id uuid fk auth.users
- industry text check in ('salon','restaurant')
- name text
- slug text unique
- description text
- phone text
- address text
- access_text text
- line_url text
- instagram_url text
- x_url text
- facebook_url text
- google_maps_url text
- opening_hours jsonb
- closed_days text
- features jsonb
- faq jsonb
- reviews jsonb
- campaigns jsonb
- reservation_links jsonb
- selected_theme text
- published boolean default false
- created_at timestamptz
- updated_at timestamptz

## salon_services
- id uuid pk
- business_id uuid fk
- category text
- name text
- description text
- price_yen integer
- sort_order integer

## restaurant_profiles
- business_id uuid pk/fk
- restaurant_type text
- cuisine_type text
- seat_count integer
- private_room boolean
- smoking_policy text
- payment_methods jsonb
- takeout boolean
- delivery boolean

## restaurant_menu_categories
- id uuid pk
- business_id uuid fk
- name text
- sort_order integer

## restaurant_menu_items
- id uuid pk
- business_id uuid fk
- category_id uuid fk
- name text
- description text
- price_yen integer
- recommended boolean default false
- photo_id uuid nullable
- sort_order integer

## photos
- id uuid pk
- business_id uuid fk
- storage_path text
- alt_text text
- category text
- sort_order integer
- is_cover boolean default false
- created_at timestamptz

Possible categories:
Salon:
- style
- interior
- exterior
- service
- other

Restaurant:
- food
- drink
- interior
- exterior
- menu
- other

## generated_content
- id uuid pk
- business_id uuid fk
- content_type text
- payload jsonb
- version integer
- created_at timestamptz

## site_versions
- id uuid pk
- business_id uuid fk
- theme text
- content_snapshot jsonb
- created_at timestamptz

## subscriptions
- id uuid pk
- business_id uuid fk
- stripe_customer_id text
- stripe_subscription_id text
- status text
- current_period_start timestamptz
- current_period_end timestamptz

## support_requests
- id uuid pk
- business_id uuid fk
- title text
- body text
- source text check in ('dashboard','line')
- status text
- billable_extra boolean default false
- created_at timestamptz
- completed_at timestamptz

## analytics_events
MVP optional or lightweight.
- id uuid pk
- business_id uuid fk
- event_type text
- created_at timestamptz

Event examples:
- page_view
- line_click
- phone_click
- reservation_click

## RLS
Every private table must use Row Level Security.
Owners can access only their own business data.
Public site may read only published business records and public content.
