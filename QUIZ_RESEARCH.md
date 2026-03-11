# Quiz Research: LegalContracts.com Residential Lease

Source: https://www.legalcontracts.com/contracts/lease-agreement-form/?loc=CA
Flow: Canada / Alberta / House selection

## All 19 Questions

| # | Question | Input Type | Options / Notes |
|---|----------|------------|-----------------|
| 1 | What type of premises are you renting? | Visual selector | House, Apartment, Condo, Room, Other |
| 2 | Are the rental premises located in [Province]? | Yes/No | Location confirmation |
| 3 | What is the address of the premises? | Text field | Street, City, Province, Postal Code |
| 4 | Who is the landlord? | Form group | Name, Type (Person/Company), Address + "Add another landlord" |
| 5 | Who will the tenant contact if there is a problem? | Visual selector | Landlord / Property Manager + Phone & Email fields |
| 6 | Who is the tenant? | Form group | Name, Type (Person/Company), Phone, Email + "Add another tenant" |
| 7 | Will any guest be regularly staying more than one week? | Yes/No | If Yes: list permitted occupants by name |
| 8 | When will the lease start/end? | Date pickers | Start date + End type: Fixed date / Renews monthly / Renews annually |
| 9 | Will the tenant be able to move in early? | Yes/No | Early possession |
| 10 | What is the rent? | Inline sentence form | "The tenant will pay $[X] every [Week/2 weeks/Month/Year]. Payments due on [day] of the month." |
| 11 | Will the tenant be charged extra for late payments? | Yes/No | If Yes: amount / grace period |
| 12 | Will any security deposit be required? | Yes/No | If Yes: deposit amount ("refundable deposit of $X for damage or failure to pay rent") |
| 13 | Will any pets be allowed? | Visual selector | Any pet / Only specific pets (description field + "Add another pet") / No pets |
| 14 | Will a refundable pet deposit be required? | Yes/No | If Yes: amount |
| 15 | Is smoking indoors allowed? | Yes/No | |
| 16 | Who will pay utilities? | Visual selector | Tenant pays all / Included in rent / Set per utility → each utility (Electricity, Water, Internet, Garbage, Cable, Natural Gas, Telephone, Heating Oil, Alarm/Security, Other) assigned to Tenant or Landlord |
| 17 | Will the tenant be responsible for any routine maintenance? | Yes/No | Snow removal, lawn care — NOT appliance/building repairs |
| 18 | Will the tenant be required to obtain renters' insurance? | Yes/No | |
| 19 | Would you like to include any additional terms? | Yes/No | Free-text clause if Yes |

---

## Key Observations for Our Quiz Design

- **19 questions vs our 10** — our leaner flow should convert better
- **Inline sentence rent field** — "The tenant will pay $[X] every [period]" is a great UX pattern worth adopting
- **Pets split across 2 steps** (allowed + deposit) — we should merge into one step
- **Landlord contact** is its own step — we can combine with landlord name
- **Smoking, maintenance, insurance** are not in our current PRD — consider adding post-MVP
- **No email capture until the end** (they gate on account creation) — we capture email inline at step 10 per PRD, which is better for our model
- **"Add another" pattern** for tenants, landlords, pets, utilities — supports multi-entry without complexity
- **Visual icon selectors** on first step (House/Apt/Condo) make it feel approachable — worth adopting for property type and pet policy
- **Progress bar** visible throughout — we should do the same ("Step X of 10")
