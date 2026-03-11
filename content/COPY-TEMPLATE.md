# Copy Template — State Landing Pages

> This is the master copy file for all state pages. Dynamic tokens are written as `{{variable}}`. Where state-specific copy blocks are needed, the token references `STATE-DATA.md` for the override. Default copy (used when no state-specific override exists) is provided inline.

---

## Tokens Reference

| Token | Example Value | Source |
|---|---|---|
| `{{state}}` | California | URL / quiz |
| `{{state_slug}}` | california | URL |
| `{{deposit_max}}` | 2 months' rent | STATE-DATA.md |
| `{{deposit_return_days}}` | 21 days | STATE-DATA.md |
| `{{notice_period}}` | 30 days | STATE-DATA.md |
| `{{state_hook}}` | California's tenant laws... | STATE-DATA.md |
| `{{state_law_callout}}` | Landlords who fail to... | STATE-DATA.md |
| `{{state_faq_q}}` | Does my lease need to... | STATE-DATA.md |
| `{{state_faq_a}}` | Yes. California requires... | STATE-DATA.md |
| `{{state_disclosures_list}}` | (bullet list) | STATE-DATA.md |
| `{{final_cta_headline}}` | {{state}} Lease Agreement... | STATE-DATA.md |

---

## Page Meta

```
Title:        {{state}} Residential Lease Agreement — $5 | State-Specific & Attorney-Structured
Description:  Get a legally complete {{state}} residential lease agreement in 5 minutes.
              Attorney-structured, includes all required {{state}} disclosures. $5 one-time.
              No subscription. Delivered to your inbox in 60 seconds.
```

---

## Navigation

```
Logo:         ResidentialLeaseAgreements.com
Nav CTA:      Get My {{state}} Lease — $5
```

---

## Above the Fold — Quiz Panel

### State Badge (above progress bar)
```
{{state}} Residential Lease Agreement
```

### Progress Indicator
```
Step {{current_step}} of 10
```

### Quiz Step Sub-labels
*(One per field. These appear beneath each question as reassuring micro-copy.)*

| Step | Field | Sub-label |
|---|---|---|
| 1 | State | Pre-selected based on your state. You can change this if needed. |
| 2 | Landlord full name | This name will appear on all legal notices and must match your property records. |
| 3 | Tenant full name(s) | List all adults who will be legally responsible for the lease. |
| 4 | Property address | The full street address as it appears on your deed or mortgage. |
| 5 | Monthly rent | Sets the legally binding rent amount and due date terms in your agreement. |
| 6 | Lease start & end dates | Defines the fixed term. Toggle to month-to-month if the tenancy has no end date. |
| 7 | Security deposit | {{state}} law limits how much you can collect. Your lease will reflect the correct terms. |
| 8 | Pet policy | If pets are allowed, you can require a separate pet deposit. Your lease will document both. |
| 9 | Utilities | Clearly defining utility responsibilities prevents the most common landlord-tenant disputes. |
| 10 | Email address | Where should we send your completed lease? You'll receive it within 60 seconds of payment. |

---

### Unlock Screen (replaces quiz after Step 10)

**Heading:**
```
Your {{state}} lease is ready.
```

**Sub-copy:**
```
Review your document, then unlock your copy for $5.
```

**Trust badges (4 items):**
```
✓ Attorney-structured
✓ Includes all required {{state}} disclosures
✓ One-time payment — no subscription
✓ Delivered to your inbox in 60 seconds
```

**Primary CTA:**
```
Get My Lease — $5
```

**Fine print below CTA:**
```
No subscription. No account needed. 30-day money-back guarantee.
```

---

## Trust Bar (below quiz section)

```
[Shield]   Attorney-structured
[Pin]      {{state}}-Specific Disclosures Included
[Clock]    Delivered in 60 Seconds
[Card]     $5. One Time. No Subscription.
```

---

## Section 4 — What's Included

### Heading
```
Everything Your {{state}} Lease Needs to Be Legally Sound
```

### Subheading
```
A lease agreement that covers every required clause — plus every disclosure {{state}} mandates.
Nothing missing. Nothing generic.
```

### Clause List
```
✓ Parties — Landlord and tenant names, contact details, and legal relationship
✓ Property — Full address and description of the rental unit
✓ Rent — Monthly amount, due date, grace period, and accepted payment methods
✓ Security Deposit — Amount, conditions for deductions, and {{state}}-mandated return timeline
✓ Lease Term — Fixed start and end dates, or month-to-month terms
✓ Pet Policy — Whether pets are permitted, breed/size restrictions, and pet deposit terms
✓ Utilities — Which utilities are landlord-paid vs. tenant-paid
✓ Maintenance — Landlord repair obligations and tenant's duty to report damage
✓ Entry Notice — Required advance notice before landlord entry ({{state}} law: {{notice_period}})
✓ Late Fees — Late fee structure and returned check policy
✓ Lease Renewal — Terms for renewal or automatic month-to-month conversion
✓ Governing Law — This agreement is governed by the laws of {{state}}
✓ All Required {{state}} Disclosures (listed below)
```

### Disclosures Callout Block
```
Heading:   {{state}}-Required Disclosures Included
Sub-copy:  Generic leases skip these. Yours won't.
Content:   [SHORT form of {{state_disclosures_list}} — 3–5 key items shown, with "See full list below" link]
```

---

## Section 5 — Why {{state}} Landlords Need a State-Specific Lease

### Heading
*(Use state-specific version from STATE-DATA.md. Default below.)*

```
A Generic Lease Won't Protect You in {{state}}
```

### Body Copy

**Paragraph 1 — The legal landscape (state-specific hook):**
```
{{state_hook}}
```

*(Default fallback if no state-specific hook exists:)*
```
Every state has its own landlord-tenant laws — and {{state}} is no exception. A lease that
complies with federal requirements but ignores {{state}} statutes can be ruled unenforceable,
leave you unable to collect damages, or expose you to penalties you didn't know existed.
The landlord-tenant relationship is only as strong as the document that defines it.
```

**Paragraph 2 — The risk of the free template:**
```
Most landlords who run into legal trouble didn't fail to have a lease. They had the wrong one.
A free PDF from Google, a template passed down from another landlord, or a form designed for
a different state can leave out the specific clauses and disclosures that {{state}} courts
expect to see. When a dispute reaches a judge, the quality of your lease determines the outcome.
```

**Paragraph 3 — The product as the solution:**
```
This lease is built specifically for {{state}}. It includes the required legal language,
the mandatory disclosures, and the correct terms for security deposits and notice periods
under {{state}} law — for $5, delivered to your inbox in under 60 seconds.
```

### Law Callout Block
```
{{state_law_callout}}
```

*(Default fallback:)*
```
{{state}} landlords are responsible for knowing their obligations under state law.
Ignorance of a required disclosure is not a defense — and the cost of getting it wrong
far exceeds the cost of getting it right.
```

---

## Section 6 — Required Disclosures

### Heading
```
Required Disclosures for {{state}} Landlords
```

### Intro sentence
```
{{state}} law requires landlords to provide tenants with specific written disclosures at or
before the start of the tenancy. Omitting any of these can give your tenant grounds to
terminate the lease, withhold rent, or seek damages.
```

### Disclosures List
```
{{state_disclosures_list}}
```

*(Each item format:)*
```
• [Disclosure Name] — [One sentence explaining what it requires and why it matters]
```

### Closing line
```
All of the above are included in your {{state}} Residential Lease Agreement.
```

---

## Section 7 — Security Deposit & Notice Rules

### Heading
```
{{state}} Deposit & Notice Rules at a Glance
```

### Sub-intro
```
Two areas where landlords most often find themselves in legal jeopardy — knowing the rules
upfront prevents disputes that cost far more than $5 to resolve.
```

### Security Deposit Block

**Sub-heading:** Security Deposit Rules in {{state}}

```
Maximum deposit:    {{deposit_max}}
Return deadline:    {{deposit_return_days}} after the tenancy ends
Itemization:        {{deposit_itemization_rules}}
Non-compliance:     {{deposit_noncompliance_consequence}}
```

*(Default for deposit_itemization_rules:)*
```
Landlord must provide written itemization of any deductions
```

*(Default for deposit_noncompliance_consequence:)*
```
Failure to return within the deadline may forfeit your right to make deductions
```

### Notice Requirements Block

**Sub-heading:** Notice to Vacate Requirements in {{state}}

```
To end a month-to-month tenancy:   {{notice_period}} written notice
Tenant notice to landlord:         {{tenant_notice_period}} written notice
Entry notice:                      {{entry_notice}} before non-emergency entry
```

*(Default for entry_notice:)*
```
24–48 hours
```

---

## Section 8 — FAQ

### Heading
```
Common Questions from {{state}} Landlords
```

### Q&A Items

**Q1 — State-specific (from STATE-DATA.md):**
```
Q: {{state_faq_q}}
A: {{state_faq_a}}
```

**Q2 — Universal:**
```
Q: Can I use a generic lease in {{state}}?

A: You can — but it may not protect you. A generic lease is unlikely to include the
specific disclosures {{state}} requires by law, the correct deposit terms, or the
notice language that holds up in a {{state}} court. If a dispute ever reaches a judge,
a lease that omits required state provisions works against you, not for you.
```

**Q3 — Universal:**
```
Q: Do I need an attorney to create a lease agreement?

A: For a standard residential tenancy, no. An attorney-reviewed, state-specific template
covers everything a typical landlord-tenant relationship requires. Attorneys typically
charge $200–$500 for a custom lease — for a single-property landlord, this lease
accomplishes the same legal foundation for $5.
```

**Q4 — Universal:**
```
Q: What if I need to make changes to the lease?

A: Your lease arrives as a PDF that reflects exactly what you entered in the quiz.
If you need to add a custom clause, you can do so before having both parties sign.
For non-standard situations, we recommend consulting an attorney for the specific
clause in question.
```

**Q5 — Universal:**
```
Q: Is this a subscription? What exactly does $5 get me?

A: $5 is a one-time payment. No account, no subscription, no renewal. You pay once and
receive one {{state}} Residential Lease Agreement as a PDF, delivered to your inbox
within 60 seconds. If for any reason you're not satisfied, we offer a 30-day money-back
guarantee — no questions asked.
```

**Q6 — Universal:**
```
Q: How does delivery work?

A: After payment, your completed lease is generated and emailed to the address you
provided. It typically arrives within 60 seconds. The subject line will read:
"Your {{state}} Lease Agreement — Ready to Sign." If it doesn't appear within
5 minutes, check your spam folder.
```

**Q7 — Universal:**
```
Q: What if my tenant refuses to sign?

A: A signed lease is always preferable. However, if a tenant occupies the property
and pays rent, courts in most states will recognize an oral or implied tenancy —
though the terms will default to state law minimums rather than your negotiated
terms. Document any refusal to sign in writing, and consider whether to proceed
with the tenancy.
```

---

## Section 9 — Final CTA Block

### Overline
```
State-Specific. Attorney-Structured. $5.
```

### Heading
*(Use state-specific version from STATE-DATA.md. Default below.)*

```
{{final_cta_headline}}
```

*(Default fallback:)*
```
Your {{state}} Lease Agreement — Ready in 5 Minutes
```

### Sub-copy
```
Answer 10 questions. Your document populates in real time.
Pay once. Receive a legally complete {{state}} lease in your inbox in 60 seconds.
```

### Primary CTA
```
Get My {{state}} Lease — $5
```

### Trust micro-copy
```
No subscription. No account needed. 30-day money-back guarantee.
```

---

## Footer

### State Links Row
```
Also available: California · Texas · Florida · New York · Georgia ·
North Carolina · Ohio · Pennsylvania · Arizona · Illinois
```
*(Link to each respective state page. Hide current state.)*

### Legal Disclaimer
```
ResidentialLeaseAgreements.com provides attorney-structured residential lease templates.
These documents are not a substitute for legal advice and do not create an attorney-client
relationship. Laws change — if you have questions about a specific legal situation,
consult a licensed attorney in your state.
```

### Legal Links
```
Privacy Policy  ·  Terms of Service  ·  Refund Policy  ·  Contact
```
