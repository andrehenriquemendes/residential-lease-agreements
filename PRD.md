# PRD — ResidentialLeaseAgreements.com
**Version:** 1.0 — MVP
**Status:** Draft
**Audience:** Engineering (Claude Code), Design

---

## 1. Overview

### 1.1 Product Summary
ResidentialLeaseAgreements.com is a programmatic, state-specific lease agreement generator. Landlords land on a state-specific page, answer a short guided quiz that populates their document in real time, and pay $5 to receive a professionally formatted, legally structured lease agreement delivered to their inbox.

The MVP targets individual US landlords who need a state-compliant lease agreement quickly and without paying attorney fees.

### 1.2 Core Value Proposition
> "A state-specific lease agreement, tailored to your property, in your inbox in under 5 minutes — for $5."

### 1.3 Business Model
- **Price:** $5 one-time per document (entry-level, volume play)
- **Payment:** Stripe
- **Delivery:** Email (PDF attachment)
- **Traffic strategy:** Google Ads (immediate validation) → SEO (programmatic, long-term)

---

## 2. Goals & Success Metrics

### 2.1 MVP Goals
- Validate that landlords will pay for a state-specific document delivered digitally
- Achieve a positive ROAS on Google Ads within 60 days of launch
- Generate the first 100 paying customers

### 2.2 Key Metrics
| Metric | Target (Month 1) |
|---|---|
| Quiz start rate (visitors who begin the quiz) | > 40% |
| Quiz completion rate | > 70% |
| Checkout conversion (quiz complete → paid) | > 20% |
| Email delivery success rate | > 99% |
| Support tickets per 100 orders | < 3 |

---

## 3. User

### 3.1 Primary Persona
**Name:** The Independent Landlord
**Age:** 45–65
**Portfolio:** 1–3 rental properties, self-managed
**Situation:** Has a new tenant moving in. Needs a lease. Doesn't want to pay a lawyer. Doesn't trust a random free PDF they found on Google.
**Fears:** Signing something that won't hold up if there's a dispute. Accidentally missing a required state disclosure.
**Motivators:** Speed, legal legitimacy, simplicity, low cost.

### 3.2 What They Are NOT
- Not a property management company
- Not a first-time renter (they're the landlord)
- Not looking for full property management software

---

## 4. User Journey

```
Google Ad / Organic Search
        ↓
State Landing Page (/texas, /california, etc.)
  — Trust signals above the fold
  — Quiz starts immediately
        ↓
Quiz Flow (3–5 steps, right panel)
  — Document preview updates live on left panel
        ↓
Preview Screen
  — Full document visible but locked/watermarked
  — Clear CTA to unlock
        ↓
Checkout (Stripe, $5)
  — Email capture at this step if not already collected
        ↓
Email Delivery
  — PDF arrives in inbox within ~60 seconds
  — Confirmation page shown
        ↓
(Future) Upsell / Email Nurture
```

---

## 5. Pages & Features

### 5.1 State Landing Page (`/<state>`)

#### Above the Fold
The quiz lives here. This is the primary conversion surface. The layout is a two-column split:

**Left column — Live Document Preview**
- Shows the lease agreement populating in real time as the user fills out the quiz
- Initial state: a partially greyed-out professional-looking lease with "[Your Name]", "[Property Address]" placeholders visibly waiting to be filled
- As each quiz answer is submitted, the corresponding field in the document updates instantly
- After checkout, the watermark lifts and the full document is unlocked

**Right column — Quiz**
- Clean, one-question-at-a-time format (not all questions at once)
- Progress bar at the top ("Step 2 of 5")
- Large, readable input fields — this audience skews older
- Each step has a short reassuring sub-label (e.g., "This sets the legally required notice period for your state.")
- The final step collects email address ("Where should we send your completed lease?")

#### Quiz Fields (MVP — Residential Lease)
1. State (pre-selected based on URL, but user can change)
2. Landlord full name
3. Tenant full name(s)
4. Property address
5. Monthly rent amount
6. Lease start date / end date (or month-to-month toggle)
7. Security deposit amount
8. Pet policy (yes/no, if yes: deposit amount)
9. Utilities included (multi-select: water, electric, gas, trash, none)
10. Email address (final step before checkout)

#### Below the Fold
This is the SEO and trust-building layer. Content should be informative and genuinely useful — not filler. Each state page includes:

- **What makes a lease legally valid in [State]** — key requirements (2–3 paragraphs)
- **Required disclosures for [State] landlords** — bullet list of mandatory clauses (lead paint, mold, etc.)
- **Security deposit rules in [State]** — limits, return timelines
- **Notice to vacate requirements in [State]**
- **FAQ** — 5–7 questions ("Can I use a generic lease in [State]?", "Do I need an attorney?", etc.)
- **What's included in your lease** — list of clauses covered in the generated document

This content is what earns SEO trust, qualifies Google Ads Quality Score, and reassures hesitant buyers before they start the quiz.

---

### 5.2 Checkout
- Powered by Stripe
- Price: $5
- Minimal fields: email (if not already captured), card details
- No account creation required
- Trust signals: SSL badge, "No subscription. One-time payment.", money-back language

---

### 5.3 Confirmation / Thank You Page
- "Your lease is on its way" message
- Estimated delivery: "Check your inbox in the next 60 seconds"
- Summary of what was generated (state, names, property)
- Soft upsell prompt (future): "Need an eviction notice or rent increase letter for [State]? Coming soon."

---

### 5.4 Email Delivery
- From address: `documents@residentialleaseagreements.com`
- Subject: `Your [State] Lease Agreement — Ready to Sign`
- Body: short, professional, plain-text-style
- Attachment: generated PDF
- PDF filename: `[State]-Lease-Agreement-[Date].pdf`

---

### 5.5 Homepage (`/`)
- Headline + brief explanation of the product
- Grid of all 50 states as clickable cards → routes to `/<state>`
- Trust section: "Attorney-structured. State-specific. $5."
- No quiz on the homepage — state selection is the entry point

---

## 6. Design Direction

### 6.1 Visual Identity
The design language must communicate **security, legality, and trust** — not startup energy, not fun/playful. Think: the aesthetic feeling of a bank or a law firm's client portal, but modern and clean.

**Color palette direction:**
- Primary: Deep navy blue (`#1B2F5B` range) — authority, trust, stability
- Accent: Muted gold or forest green — conveys premium, not cheap
- Background: Off-white or light warm grey — not clinical white
- Text: Near-black — high readability for older users
- Avoid: Bright teals, orange CTAs, anything that reads as "SaaS startup"

**CTA button:** Should feel weighty and confident. "Get My Lease — $5" not "Download Now"

### 6.2 Typography
- Serif or semi-serif for headings — conveys formality and legality
- Clean sans-serif for body and UI elements
- Large base font size — minimum 16px — this audience reads on desktop

### 6.3 Document Preview Aesthetic
The live preview panel should look like a real legal document — not a generic form. White paper, clear section headers, professional typesetting. When it populates with the user's real name and address, it should feel meaningful and personalized, not like a mail merge.

### 6.4 Mobile
Quiz is usable on mobile (stacked layout — preview hidden, quiz full-width). Document preview shown after quiz completion, before checkout. Desktop is primary conversion surface for this audience.

---

## 7. Copy & CRO Principles

### 7.1 Core Messaging Framework
- **Primary fear to address:** "Will this hold up legally?"
- **Primary desire:** Speed + certainty without lawyer fees
- **Proof points:** State-specific, structured clauses, used by landlords in [State]

### 7.2 Above the Fold Headline Options (A/B test)
- "Your [State] Lease Agreement — Done in 5 Minutes"
- "A Legally Structured [State] Lease Agreement for $5"
- "Stop Using Generic Leases. Get a [State]-Specific Agreement Today."

### 7.3 Micro-copy Principles
- Every quiz step should have a reassuring sub-label explaining *why* that field matters
- Error states should never feel like punishment ("Let's fill that in before we continue")
- The paywall moment should feel like unlocking, not a wall — "Your lease is ready. Unlock it below."
- The $5 price should always be contextualized: "Less than a coffee. Less than 0.01% of your first month's rent."

### 7.4 Trust Signals (sprinkle throughout)
- "Attorney-structured lease"
- "Includes all required [State] disclosures"
- "No subscription. No account needed."
- "Delivered in under 60 seconds"
- "30-day money-back guarantee" (eliminates purchase anxiety at $5)

---

## 8. MVP Scope — What's Included

| Feature | In MVP |
|---|---|
| 50 state landing pages (`/<state>`) | ✅ (launch with top 10, expand) |
| Residential lease agreement only | ✅ |
| Quiz → live preview flow | ✅ |
| Stripe checkout ($5) | ✅ |
| PDF generation + S3 storage | ✅ |
| Email delivery of PDF | ✅ |
| Homepage with state directory | ✅ |
| Confirmation page | ✅ |
| Mobile-responsive layout | ✅ |
| User accounts / dashboard | ❌ |
| E-signature integration | ❌ |
| Additional document types | ❌ |
| Annual membership / subscription | ❌ |
| Tenant screening upsell | ❌ |
| Admin dashboard | ❌ |

---

## 9. Launch State Priority

Launch with these 10 states first (highest landlord population + search volume):

1. California
2. Texas
3. Florida
4. New York
5. Georgia
6. North Carolina
7. Ohio
8. Pennsylvania
9. Arizona
10. Illinois

Expand to all 50 after conversion is validated.

---

## 10. Open Questions (Pre-Build Decisions Needed)

| # | Question | Impact |
|---|---|---|
| 1 | Will the $5 price hold, or do we test $9 / $19 from day one? | Unit economics vs. volume |
| 2 | Do we show the document preview before or after email capture? | Conversion rate vs. lead quality |
| 3 | Is the 30-day money-back guarantee enforceable / desirable at $5? | Trust vs. refund risk |
| 4 | Who is responsible for keeping state-specific legal content updated? | Ongoing ops |
| 5 | Do we want a `/blog` or `/[state]/laws` content layer in MVP or post-MVP? | SEO timeline |
