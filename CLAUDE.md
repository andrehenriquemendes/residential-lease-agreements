# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Status

This is a **pre-code planning repository**. The product is fully specced in `PRD.md`. No application code exists yet. The first step when building is to scaffold a Next.js project in this directory.

## Product

ResidentialLeaseAgreements.com — a $5, state-specific residential lease agreement generator. Landlords fill out a guided quiz, see their document populate live, pay via Stripe, and receive a PDF in their inbox within 60 seconds. No user accounts.

## Planned Tech Stack

- **Framework:** Next.js (App Router) with TypeScript
- **Styling:** Tailwind CSS
- **Payments:** Stripe (one-time $5 payment, no subscriptions)
- **PDF generation:** Server-side (puppeteer or pdfkit on an API route)
- **Storage:** AWS S3 (generated PDFs)
- **Email:** SendGrid or AWS SES — from `documents@residentialleaseagreements.com`
- **Deployment:** Vercel

## Commands (once scaffolded)

```bash
npm run dev        # local dev server
npm run build      # production build
npm run lint       # ESLint
npm run test       # Jest tests (if added)
```

## Architecture

### Routing

```
/                        → Homepage — 50-state grid (launch with top 10)
/<state>                 → State landing page (e.g., /texas, /california)
/checkout                → Stripe checkout step
/confirmation            → Thank-you page after successful payment
/api/generate-pdf        → Server-side: merge quiz answers into lease template → S3
/api/send-email          → Server-side: email PDF link/attachment to user
/api/stripe/webhook      → Stripe webhook handler (triggers PDF generation + email)
```

### Core User Flow

```
State page (/<state>)
  → Two-column layout: left = live document preview, right = quiz
  → Quiz: one question at a time, 10 fields, progress bar ("Step 2 of 5")
  → Final quiz step collects email
  → After quiz: preview is visible but watermarked/locked
  → CTA: "Get My Lease — $5"
  → Stripe checkout ($5 one-time, no account needed)
  → On payment success: webhook → generate PDF → upload to S3 → send email
  → Confirmation page shown
```

### Quiz Fields (in order)

1. State (pre-selected from URL, user can change)
2. Landlord full name
3. Tenant full name(s)
4. Property address
5. Monthly rent amount
6. Lease start/end dates (or month-to-month toggle)
7. Security deposit amount
8. Pet policy (yes/no; if yes: deposit amount)
9. Utilities included (multi-select: water, electric, gas, trash, none)
10. Email address

### State Management

Quiz answers should be held in React context (or Zustand) and passed to:
- The live document preview (real-time updates)
- The Stripe checkout session metadata
- The PDF generation API route (triggered by Stripe webhook)

### PDF Templates

Each state has its own lease template that includes state-specific required disclosures. Templates are merged with quiz answers server-side. PDF filename format: `[State]-Lease-Agreement-[Date].pdf`.

### Key Environment Variables

```
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY
STRIPE_SECRET_KEY
STRIPE_WEBHOOK_SECRET
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_S3_BUCKET
AWS_REGION
SENDGRID_API_KEY   # or SES equivalent
NEXT_PUBLIC_SITE_URL
```

## Design Direction

The aesthetic must communicate **legal authority and trust** — not startup/SaaS energy.

- **Primary color:** Deep navy `#1B2F5B`
- **Accent:** Muted gold or forest green
- **Background:** Off-white / warm grey
- **Typography:** Serif or semi-serif headings, clean sans-serif body, minimum 16px base
- **Avoid:** Bright teals, orange CTAs, anything that reads as "startup"
- The document preview panel must look like a real legal document (white paper, section headers, professional typesetting)

Mobile: stacked layout — hide document preview, show quiz full-width. Show preview after quiz completion, before checkout.

## Launch Scope

MVP launches with 10 states: California, Texas, Florida, New York, Georgia, North Carolina, Ohio, Pennsylvania, Arizona, Illinois. Expand to all 50 after conversion is validated.

**Not in MVP:** user accounts, e-signatures, additional document types, subscriptions, admin dashboard.

## Open Decisions (resolve before building)

1. Price point: $5 fixed, or test $9/$19 from day one?
2. Email capture: before or after showing the document preview?
3. `/blog` or `/[state]/laws` SEO content layer — MVP or post-MVP?
