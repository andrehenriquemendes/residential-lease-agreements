# Page Guide — State Landing Pages (`/<state>`)

> This document describes what appears on each state landing page: the sections, their purpose, the elements within them, and the psychological job each section does. It is not a design spec — refer to DESIGN-SYSTEM.md for all visual decisions.

---

## Page Architecture Overview

The state landing page has two distinct zones:

1. **Above the fold — Conversion Zone**: The quiz and live document preview. This is the primary revenue surface. Everything here serves one goal: get the user into the quiz and through to checkout.

2. **Below the fold — Trust & SEO Zone**: Informational content about state-specific landlord law. This zone does three jobs simultaneously: (a) answers the hesitant buyer's research questions so they don't leave to Google, (b) builds legal authority for the product, and (c) earns organic search rankings for state-specific landlord queries.

---

## Above the Fold

### 1. Navigation Bar

**What it contains:**
- Logo / wordmark (links to homepage)
- Single CTA: "Get My [State] Lease — $5"

**Purpose:** Minimal navigation. There is nowhere else to go. The CTA in the nav serves as a persistent anchor — if the user scrolls and loses the quiz from view, they can always click back into it.

**Note:** No additional nav links. State pages are conversion pages, not browsing pages.

---

### 2. Hero / Quiz Section

This is the heart of the page. It occupies the full viewport on desktop as a two-column split layout.

#### Left Column — Live Document Preview

**What it contains:**
- A rendered, realistic-looking residential lease agreement
- State name and "Residential Lease Agreement" displayed as a document header
- Numbered sections with placeholder text (`[Landlord Name]`, `[Property Address]`, etc.) shown as underlined blanks
- As the user fills in quiz fields, the corresponding blanks update in real time
- After quiz completion (pre-payment): document body blurs slightly, diagonal "PREVIEW" watermark appears, a centered overlay card shows the unlock CTA

**Visual purpose:** Makes the product feel real and tangible before purchase. The user sees their actual name and address appearing in a legal document — this is the IKEA Effect in action. They've already "built" part of it.

**What it communicates without words:** This is a real document, not a generic template. It already has your information in it.

---

#### Right Column — Quiz Panel

**What it contains (in order):**

1. **State badge** — "[State] Residential Lease Agreement" displayed as a small labeled tag above the quiz. Confirms to the user they're in the right place.

2. **Progress indicator** — "Step X of 10" with a thin progress bar. Communicates that this is short and completable. Shows momentum.

3. **Question area** — One question at a time, large readable type. Each question includes:
   - The question label (e.g., "Landlord's full name")
   - A sub-label explaining *why* this field matters (e.g., "Required for all legal notices sent to and from your property")
   - The input field

4. **Navigation buttons** — Back (ghost) and Continue (primary). "Continue" advances the quiz and updates the document preview in real time.

5. **Final step (Step 10) — Email capture:**
   - Question: "Where should we send your completed lease?"
   - Sub-label: "Your PDF will be delivered to your inbox within 60 seconds of payment."
   - Input: email address field

**After final step — Unlock Screen (replaces quiz panel):**
- Headline: "Your [State] lease is ready."
- Sub-copy: "Review it below, then unlock your copy for $5."
- Trust badges row (horizontal): ✓ Attorney-structured  ✓ [State]-specific disclosures  ✓ One-time payment  ✓ Delivered in 60 seconds
- Primary CTA button: "Get My Lease — $5"
- Fine print below button: "No subscription. No account needed. 30-day money-back guarantee."

---

### 3. Trust Bar (below quiz, above fold break)

A narrow horizontal strip sitting immediately below the quiz section, before the page scrolls into content.

**What it contains (4 items, icon + label each):**
- Shield icon: "Attorney-structured"
- Map pin icon: "[State]-Specific Disclosures Included"
- Clock icon: "Delivered in 60 Seconds"
- Card icon: "$5. One Time. No Subscription."

**Purpose:** These are the four objections most likely to kill the sale. This strip addresses them passively — the user doesn't have to seek reassurance, it's already in their peripheral vision as they complete the quiz.

---

## Below the Fold

The content below the fold is divided into six sections. They flow from most purchase-relevant (what's in this lease) to most informational (state law education). The ordering is intentional: a user who scrolls immediately after seeing the unlock CTA is looking for a reason to trust the product — not a law school lecture.

---

### Section 4 — What's Included in Your Lease

**Position:** First section below the fold. Highest purchase-intent content.

**What it contains:**
- Section heading: "Everything Your [State] Lease Needs to Be Legally Sound"
- Subheading: A one-sentence framing of completeness and coverage
- A structured list of 10–14 clauses included in the generated lease, each with a short descriptor:
  - Names & parties
  - Property description & address
  - Rent amount, due date & grace period
  - Security deposit terms & conditions
  - Lease term (fixed or month-to-month)
  - Pet policy
  - Utilities & maintenance responsibilities
  - Entry notice requirements
  - Late fees & returned check policy
  - Lease renewal terms
  - All required [State] disclosures (see list below)
  - Governing law clause
- Below the clause list: a callout block highlighting the state-specific required disclosures specifically — the items a generic lease would miss

**Why it's here:** A buyer who has completed the quiz and is hesitating at checkout is asking: "Is this actually complete? Will I get what I need?" This section answers that directly and specifically, not generically.

---

### Section 5 — Why [State] Landlords Need a State-Specific Lease

**Position:** Second section below the fold.

**What it contains:**
- Section heading (state-specific — see `STATE-DATA.md` for per-state variants)
- 2–3 paragraphs covering:
  - What makes a residential lease legally valid in [State]
  - The risk of using a generic or out-of-state lease template
  - The specific legal requirements [State] places on landlords that a proper lease must reflect
- Pull-quote or callout block: a specific, striking state law fact (e.g., penalty amounts, deposit return timelines) that illustrates the cost of getting it wrong

**Why it's here:** Confirmation bias and regret aversion. The user already believes they need a proper lease — this section confirms that belief with specificity. It also preemptively neutralizes the "I'll just use a free template" exit path by naming exactly what a free template won't include.

---

### Section 6 — Required Disclosures in [State]

**Position:** Third section below the fold.

**What it contains:**
- Section heading: "Required Disclosures for [State] Landlords"
- One-sentence intro: contextualizes why disclosures matter and what happens if they're missing
- Bulleted list of all mandatory disclosures for [State] (state-specific — see `STATE-DATA.md`)
  - Each disclosure: name of disclosure + one sentence explaining what it requires
- Closing line: "All of the above are included in your [State] Residential Lease Agreement."

**Why it's here:** This is the single most effective trust-builder on the page for a compliance-anxious landlord. The specificity of a real disclosure checklist signals genuine legal knowledge — not a generic product. It also captures SEO for queries like "[state] required lease disclosures."

---

### Section 7 — Security Deposit & Notice Rules in [State]

**Position:** Fourth section below the fold.

**What it contains:**
Two sub-sections displayed side-by-side (or stacked on mobile):

**Security Deposit Rules:**
- Maximum deposit amount allowed in [State]
- Deadline to return deposit after lease ends
- Required conditions/itemization rules
- Consequence of non-compliance (where notable)

**Notice to Vacate Requirements:**
- Notice period required for landlord to end a month-to-month tenancy
- Notice period required for tenant
- Any notable exceptions (e.g., longer notice for long-term tenants)

**Why it's here:** These are the two most common areas where landlords get into legal disputes. Including them signals that the product is built by people who understand where the real legal risk lies — not just people who slapped "Lease Agreement" on a generic form.

---

### Section 8 — FAQ

**Position:** Fifth section below the fold.

**What it contains:**
5–7 questions in an accordion/expandable format. Mix of universal questions and state-specific ones.

**Universal questions (all states):**
- "Can I use a generic lease in [State]?" — Answer: No. Explains why state-specific matters.
- "Do I need an attorney to create a lease agreement?" — Answer: Positions the product relative to attorney cost.
- "What if my tenant refuses to sign?" — Answer: Practical guidance, reinforces the product's legal structure.
- "Is this a one-time payment or subscription?" — Answer: $5, one time, no account, money-back guarantee.
- "How does the PDF get delivered?" — Answer: Email within 60 seconds of payment, plus download link.

**State-specific question (1 per state — see `STATE-DATA.md`):**
- A question addressing the most common state-specific concern or confusion (e.g., "Does my California lease need to include AB 1482 rent control notices?")

**Why it's here:** FAQ sections serve objection-handling without the awkwardness of a salesy objection-handling section. They also capture long-tail search queries and improve Quality Score for paid search.

---

### Section 9 — Final CTA Block

**Position:** Last section before footer. Dark background, high contrast.

**What it contains:**
- Overline: "State-Specific. Attorney-Structured. $5."
- Heading: "[State] Lease Agreement — Ready in 5 Minutes" (state-specific variant — see `STATE-DATA.md`)
- Sub-copy: One sentence restating the core promise with urgency framing
- Primary CTA button: "Get My [State] Lease — $5"
- Below button: Trust micro-copy: "No subscription. No account needed. 30-day money-back guarantee."

**Purpose:** Catches the reader who scrolled all the way through. At this point they've consumed all the trust-building content and just need a final nudge. This section re-presents the offer without adding new information — the job is friction removal, not persuasion.

---

### 10. Footer

Standard site footer. Contains:
- Links to other state pages ("Also available: Texas · Florida · New York · [+7 more]")
- Legal disclaimer: "ResidentialLeaseAgreements.com provides attorney-structured document templates. This is not legal advice and does not create an attorney-client relationship."
- Privacy Policy, Terms of Service links
- Contact email

---

## Mobile Behavior Notes

- **Above the fold:** Quiz panel is full-width. Document preview is hidden.
- **After quiz completion:** Document preview appears below the quiz (blurred/watermarked) before the unlock CTA.
- **Below the fold:** All sections stack vertically. Section 7 sub-sections stack (security deposit above, notice requirements below).
- The persistent "Get My Lease — $5" CTA in the nav remains visible while scrolling.

---

## What This Page Does NOT Include

- Blog links or content navigation (this is a conversion page, not a hub)
- Competitor comparisons (implied through specificity, not stated)
- Pricing tables or tier selection (one product, one price)
- User account creation or login prompts
- Social media links (footer only, de-emphasized)
