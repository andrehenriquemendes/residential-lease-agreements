# Design System — ResidentialLeaseAgreements.com

> A living document defining the visual language, design tokens, and component specifications for ResidentialLeaseAgreements.com. The aesthetic communicates **legal authority, trust, and professional competence** — not startup/SaaS energy.

---

## Table of Contents

1. [Design Principles](#design-principles)
2. [Design Tokens](#design-tokens)
   - [Colors](#colors)
   - [Typography](#typography)
   - [Spacing](#spacing)
   - [Sizing & Layout](#sizing--layout)
   - [Border Radius](#border-radius)
   - [Shadows & Elevation](#shadows--elevation)
   - [Motion & Animation](#motion--animation)
3. [Components](#components)
   - [Navigation](#navigation)
   - [Buttons](#buttons)
   - [Badges & Labels](#badges--labels)
   - [Stat Cards](#stat-cards)
   - [State Cards (50-State Grid)](#state-cards-50-state-grid)
   - [Document Preview Panel](#document-preview-panel)
   - [Quiz Step](#quiz-step)
   - [Progress Bar](#progress-bar)
   - [Form Inputs](#form-inputs)
   - [Accordion / Expandable Row](#accordion--expandable-row)
   - [Trust Indicators](#trust-indicators)
   - [Section Header](#section-header)
   - [Footer](#footer)
4. [Page Patterns](#page-patterns)
   - [Hero Section](#hero-section)
   - [Two-Column Quiz Layout](#two-column-quiz-layout)
   - [CTA Section](#cta-section)
5. [Accessibility](#accessibility)
6. [Responsive Breakpoints](#responsive-breakpoints)
7. [Voice & Content Guidelines](#voice--content-guidelines)

---

## Design Principles

| Principle | Description |
|-----------|-------------|
| **Authority** | Every visual choice should reinforce that this is a serious legal product. Lean into the weight of serif type, dark grounds, and structured layout. |
| **Clarity** | The user must never feel confused. One question at a time. Clear progress. No jargon. |
| **Trust** | No flashy gradients or gamification. Whitespace, restraint, and substance signal credibility. |
| **Speed** | From state selection to PDF in 60 seconds. The UI should feel fast and purposeful — no unnecessary steps. |
| **Restraint** | If in doubt, remove it. Elegance comes from what you leave out. |

---

## Design Tokens

### Colors

#### Primitive Colors (Raw palette — do not use directly in components)

```
--color-navy-950:    #0F1E3D   /* Deepest navy — hero backgrounds */
--color-navy-900:    #1B2F5B   /* Brand primary */
--color-navy-800:    #243D76
--color-navy-700:    #2E4D90
--color-navy-200:    #C5D0E8
--color-navy-100:    #E8EDF6
--color-navy-50:     #F4F6FB

--color-gold-700:    #8A6B1E
--color-gold-600:    #A07C22
--color-gold-500:    #B8952A
--color-gold-400:    #C9A83C   /* Primary accent */
--color-gold-300:    #D9BC6A
--color-gold-100:    #F5EDD0

--color-neutral-950: #0A0A0A
--color-neutral-900: #141414
--color-neutral-800: #1F1F1F
--color-neutral-700: #333333
--color-neutral-600: #4D4D4D
--color-neutral-500: #666666
--color-neutral-400: #808080
--color-neutral-300: #B3B3B3
--color-neutral-200: #D9D9D9
--color-neutral-100: #F0EEEA   /* Warm off-white */
--color-neutral-50:  #F8F6F2   /* Page background */
--color-white:       #FFFFFF

--color-green-700:   #1E5C3A   /* Forest green accent alternative */
--color-green-500:   #2A7D4F
--color-green-100:   #D1EAD8

--color-red-700:     #8B1A1A
--color-red-500:     #C0392B
--color-red-100:     #FDECEA
```

#### Semantic Color Tokens (Use these in components)

```
/* Backgrounds */
--bg-page:           var(--color-neutral-50)      /* Main page background */
--bg-surface:        var(--color-white)            /* Cards, panels */
--bg-surface-alt:    var(--color-neutral-100)      /* Subtle surface variant */
--bg-dark:           var(--color-navy-900)         /* Dark sections */
--bg-darker:         var(--color-navy-950)         /* Hero, CTA sections */
--bg-inverted:       var(--color-neutral-950)      /* Footer, dark elements */

/* Text */
--text-primary:      var(--color-navy-900)         /* Primary headings */
--text-body:         var(--color-neutral-700)      /* Body copy */
--text-muted:        var(--color-neutral-500)      /* Captions, metadata */
--text-inverse:      var(--color-white)            /* Text on dark backgrounds */
--text-inverse-muted: var(--color-neutral-300)    /* Muted text on dark */
--text-accent:       var(--color-gold-400)         /* Gold highlights */
--text-link:         var(--color-navy-700)         /* Inline links */

/* Brand */
--brand-primary:     var(--color-navy-900)
--brand-accent:      var(--color-gold-400)
--brand-accent-alt:  var(--color-green-500)        /* Optional green accent */

/* UI Feedback */
--color-success:     var(--color-green-500)
--color-error:       var(--color-red-500)
--color-warning:     var(--color-gold-500)

/* Borders */
--border-default:    var(--color-neutral-200)
--border-subtle:     var(--color-neutral-100)
--border-dark:       rgba(255,255,255,0.12)        /* On dark surfaces */
--border-accent:     var(--color-gold-400)

/* Document Preview */
--doc-bg:            var(--color-white)
--doc-border:        var(--color-neutral-200)
--doc-text:          var(--color-neutral-900)
--doc-watermark:     rgba(27, 47, 91, 0.08)
```

---

### Typography

#### Font Families

```
--font-serif:        'Playfair Display', 'Georgia', serif
--font-sans:         'Inter', 'Helvetica Neue', Arial, sans-serif
--font-mono:         'JetBrains Mono', 'Courier New', monospace
--font-document:     'Times New Roman', 'Georgia', serif  /* PDF preview */
```

**Usage rule:** Headings use `--font-serif`. Body copy, UI labels, and interactive elements use `--font-sans`. Document preview text uses `--font-document`.

#### Type Scale

```
--text-xs:           0.75rem    /* 12px — captions, footnotes */
--text-sm:           0.875rem   /* 14px — labels, metadata */
--text-base:         1rem       /* 16px — body copy (minimum) */
--text-lg:           1.125rem   /* 18px — lead text */
--text-xl:           1.25rem    /* 20px — small headings */
--text-2xl:          1.5rem     /* 24px */
--text-3xl:          1.875rem   /* 30px */
--text-4xl:          2.25rem    /* 36px */
--text-5xl:          3rem       /* 48px */
--text-6xl:          3.75rem    /* 60px — hero headline */
--text-7xl:          4.5rem     /* 72px — display only */
```

#### Font Weights

```
--font-regular:      400
--font-medium:       500
--font-semibold:     600
--font-bold:         700
--font-extrabold:    800        /* Display headlines only */
```

#### Line Heights

```
--leading-tight:     1.15       /* Headlines */
--leading-snug:      1.3        /* Subheadings */
--leading-normal:    1.5        /* Body copy */
--leading-relaxed:   1.65       /* Long-form, readable text */
--leading-loose:     2          /* Spacious labels */
```

#### Letter Spacing

```
--tracking-tight:    -0.03em    /* Large serif headlines */
--tracking-normal:   0          /* Default */
--tracking-wide:     0.05em     /* UI labels, small caps */
--tracking-widest:   0.15em     /* Section labels, overlines */
```

#### Semantic Text Roles

| Role | Font | Size | Weight | Tracking | Leading |
|------|------|------|--------|----------|---------|
| Display / Hero H1 | serif | 5xl–6xl | extrabold | tight | tight |
| H1 | serif | 4xl–5xl | bold | tight | tight |
| H2 | serif | 3xl–4xl | bold | tight | snug |
| H3 | serif | 2xl | semibold | normal | snug |
| H4 | sans | xl | semibold | normal | normal |
| Body Large | sans | lg | regular | normal | relaxed |
| Body | sans | base | regular | normal | normal |
| Caption / Label | sans | sm | medium | wide | loose |
| Overline | sans | xs | semibold | widest | loose |
| CTA / Button | sans | base–sm | semibold | wide | — |

---

### Spacing

Base unit: **8px**. All spacing values are multiples of 4px.

```
--space-0:    0
--space-1:    0.25rem   /* 4px */
--space-2:    0.5rem    /* 8px */
--space-3:    0.75rem   /* 12px */
--space-4:    1rem      /* 16px */
--space-5:    1.25rem   /* 20px */
--space-6:    1.5rem    /* 24px */
--space-8:    2rem      /* 32px */
--space-10:   2.5rem    /* 40px */
--space-12:   3rem      /* 48px */
--space-16:   4rem      /* 64px */
--space-20:   5rem      /* 80px */
--space-24:   6rem      /* 96px */
--space-32:   8rem      /* 128px */
--space-40:   10rem     /* 160px */
```

**Section padding:** `--space-20` to `--space-32` vertically on desktop, `--space-12` to `--space-16` on mobile.

---

### Sizing & Layout

```
/* Max content widths */
--container-sm:      640px
--container-md:      768px
--container-lg:      1024px
--container-xl:      1280px
--container-2xl:     1440px

/* Standard container with side padding */
--container-padding: var(--space-6)     /* mobile */
--container-padding-lg: var(--space-16) /* desktop */

/* Component sizes */
--nav-height:        72px
--nav-height-mobile: 60px

/* Document preview */
--doc-preview-width: 50%               /* desktop two-column */
--doc-preview-min-w: 420px

/* Quiz panel */
--quiz-panel-width:  50%               /* desktop two-column */
--quiz-panel-max-w:  560px

/* State grid card */
--state-card-min-w:  120px
--state-card-height: 80px

/* Icon sizes */
--icon-xs:           12px
--icon-sm:           16px
--icon-md:           20px
--icon-lg:           24px
--icon-xl:           32px
```

---

### Border Radius

```
--radius-none:       0
--radius-sm:         2px        /* Subtle — document elements */
--radius-md:         4px        /* Inputs, small cards */
--radius-lg:         8px        /* Cards, panels */
--radius-xl:         12px       /* Large cards */
--radius-2xl:        16px       /* Modal overlays */
--radius-full:       9999px     /* Badges, pills, avatar */
```

**Aesthetic note:** This is a legal product. Prefer sharp to medium radius. Avoid `--radius-2xl` or `--radius-full` on large surfaces — it signals "app", not "document".

---

### Shadows & Elevation

```
--shadow-none:       none
--shadow-xs:         0 1px 2px rgba(0,0,0,0.05)
--shadow-sm:         0 1px 3px rgba(0,0,0,0.10), 0 1px 2px rgba(0,0,0,0.06)
--shadow-md:         0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.06)
--shadow-lg:         0 10px 15px rgba(0,0,0,0.10), 0 4px 6px rgba(0,0,0,0.05)
--shadow-xl:         0 20px 25px rgba(0,0,0,0.10), 0 10px 10px rgba(0,0,0,0.04)
--shadow-document:   0 4px 24px rgba(0,0,0,0.12), 0 1px 4px rgba(0,0,0,0.08)
--shadow-inset:      inset 0 2px 4px rgba(0,0,0,0.06)
```

| Elevation Level | Token | Used For |
|----------------|-------|----------|
| Ground | `shadow-none` | Flat sections, dark backgrounds |
| Raised | `shadow-sm` | Navbar (scrolled), subtle cards |
| Floating | `shadow-md` | Cards, dropdowns |
| Overlay | `shadow-lg` | Modals, sticky elements |
| Document | `shadow-document` | PDF preview panel |

---

### Motion & Animation

```
--duration-instant:  0ms
--duration-fast:     100ms
--duration-normal:   200ms
--duration-slow:     350ms
--duration-slower:   500ms

--ease-default:      cubic-bezier(0.4, 0, 0.2, 1)   /* Material standard */
--ease-in:           cubic-bezier(0.4, 0, 1, 1)
--ease-out:          cubic-bezier(0, 0, 0.2, 1)
--ease-spring:       cubic-bezier(0.34, 1.56, 0.64, 1) /* Gentle spring */
```

**Principles:**
- Transitions on interactive elements: `--duration-fast` with `--ease-default`
- Page section reveals: `--duration-slow` with `--ease-out` (fade + subtle upward translate)
- Quiz step transitions: `--duration-normal` slide-left/right
- No looping animations. No bounce. No parallax on legal content.

---

## Components

### Navigation

**Structure:** Logo left | Nav links center | CTA button right

```
States:
  - Default (transparent or --bg-page on light hero)
  - Scrolled (--bg-surface + --shadow-sm, border-bottom --border-default)
  - Mobile (hamburger menu, full-screen overlay or drawer)

Specs:
  Height:       --nav-height (72px desktop), --nav-height-mobile (60px)
  Logo:         Wordmark in --font-serif, --text-2xl, --brand-primary
  Nav Links:    --font-sans, --text-sm, --font-medium, --text-body
                Hover: --text-primary, underline-offset-4
  CTA Button:   Primary button style (see Buttons)
  Mobile:       Hamburger icon at --icon-lg, drawer slides from right
```

**Dark hero variant:** Logo and nav links in `--text-inverse`. CTA button remains solid.

---

### Buttons

#### Primary Button
```
Background:   --brand-primary (#1B2F5B)
Text:         --text-inverse (#FFFFFF)
Font:         --font-sans, --text-sm, --font-semibold, --tracking-wide
Padding:      --space-3 --space-6 (12px 24px)
Radius:       --radius-md (4px)
Border:       none
Hover:        background lightens to --color-navy-800, translateY(-1px), --shadow-md
Active:       translateY(0), --shadow-sm
Focus:        2px offset ring in --brand-accent

Arrow variant: Append → icon (--icon-sm), gap --space-2
               On hover: arrow translates 4px right
```

#### Secondary Button (Outlined)
```
Background:   transparent
Text:         --brand-primary
Border:       1.5px solid --brand-primary
Hover:        Background --color-navy-50
```

#### Ghost Button
```
Background:   transparent
Text:         --text-body
Border:       none
Hover:        --bg-surface-alt
Used for:     Low-priority actions, "Get Started →" text links
```

#### Button on Dark Background
```
Primary:      Background --brand-accent (gold), text --color-navy-950
Secondary:    Border rgba(255,255,255,0.4), text --text-inverse
Ghost:        Text --text-inverse-muted
```

#### Disabled State (all)
```
Opacity:      0.45
Cursor:       not-allowed
No hover effects
```

---

### Badges & Labels

#### Overline Badge (section indicator)
```
Pattern from reference: "• Our Services" / "• Our Lawyers"
Font:       --font-sans, --text-xs, --font-semibold, --tracking-widest, uppercase
Color:      --text-muted or --brand-accent on dark
Prefix:     Small bullet or asterisk (★, •, or custom icon)
Used at:    Top-right of section headers as category label
```

#### Tag / Pill
```
Padding:    --space-1 --space-3
Radius:     --radius-full
Font:       --text-xs, --font-semibold
Variants:
  - Default:  --bg-surface-alt, --text-body
  - Navy:     --bg-dark, --text-inverse
  - Gold:     --color-gold-100, --color-gold-700
  - Success:  --color-green-100, --color-green-700
```

---

### Stat Cards

Modeled after the "550+ Clients / 10+ Years / 96% Success" pattern in the reference.

```
Layout:       Horizontal row of 3 stats, full width within hero
Stat Number:  --font-serif, --text-5xl, --font-bold, --text-inverse
Stat Label:   --font-sans, --text-sm, --text-inverse-muted
Separator:    1px vertical rule in rgba(255,255,255,0.15)
Responsive:   Stack 3-col → 3-col (stays 3-col, shrinks font)
              On mobile: smaller text, no separators

For ResidentialLeaseAgreements.com:
  Stat 1:  "50+" — States Covered
  Stat 2:  "$5"  — One-Time Fee
  Stat 3:  "60s" — Delivery Time
  Stat 4:  "100%" — Legally Compliant
```

---

### State Cards (50-State Grid)

Used on the homepage `/` to display all available states.

```
Card:
  Size:         min-width --state-card-min-w, height --state-card-height
  Background:   --bg-surface
  Border:       1px solid --border-default
  Radius:       --radius-md
  Padding:      --space-3 --space-4
  Shadow:       --shadow-xs (default), --shadow-md (hover)

  Content:
    State abbreviation: --font-serif, --text-lg, --font-bold, --text-primary
    State full name:    --font-sans, --text-xs, --text-muted

  Hover:
    Border color:   --brand-primary
    Background:     --color-navy-50
    translateY:     -2px
    Transition:     --duration-fast

  Available (MVP 10 states):
    Normal styling with hover

  Coming Soon:
    Opacity:        0.5
    Cursor:         default
    Label:          "Coming Soon" pill overlay

Grid: CSS grid, auto-fill, minmax(120px, 1fr), gap --space-3
```

---

### Document Preview Panel

The live-updating lease document shown to the user during quiz completion.

```
Container:
  Background:     --doc-bg (white)
  Border:         1px solid --doc-border
  Shadow:         --shadow-document
  Radius:         --radius-sm
  Padding:        --space-8 --space-10 (mimics print margins)
  Max-width:      680px (A4-like proportion)
  Aspect ratio:   ~0.77 (letter paper)

Typography inside document:
  Font:           --font-document
  Size:           --text-sm (11–12px equivalent for document feel)
  Line height:    --leading-relaxed
  Color:          --doc-text

Document structure (rendered as real document):
  Header:         State name, "Residential Lease Agreement", Date
  Sections:       Numbered 1–N with bold headings
  Fields:         Underlined placeholders replaced by quiz answers
  Empty fields:   Shown as "_______________" until filled

Watermark state (after quiz, pre-payment):
  Diagonal "PREVIEW" text in --doc-watermark color
  Blur filter: blur(1.5px) on body content
  Lock overlay: centered card with lock icon + "Get My Lease — $5" CTA

Responsive:
  Desktop:  Fixed position, sticky in viewport alongside quiz
  Mobile:   Hidden during quiz; shown full-screen after quiz completion
```

---

### Quiz Step

Single-question card shown in the right panel during the quiz flow.

```
Container:
  Background:     --bg-surface
  Padding:        --space-8 --space-10
  No border, no shadow (sits on --bg-page)

Step indicator:
  "Step 2 of 10"
  Font: --font-sans, --text-sm, --font-medium, --text-muted

Question:
  Font: --font-serif, --text-2xl, --font-bold, --text-primary
  Margin-bottom: --space-6

Input area:
  See Form Inputs

Navigation:
  Back (ghost arrow left) + Next / Continue (primary button)
  Layout: space-between flex row
  Back disabled on step 1
```

---

### Progress Bar

```
Track:        height 3px, --bg-surface-alt, --radius-full
Fill:         --brand-primary, animated width transition --duration-slow
Step dots:    Optional: small circles at each step position
              Active: --brand-primary filled; Complete: checkmark; Future: --border-default
```

---

### Form Inputs

```
Text / Email / Number Input:
  Height:       48px
  Padding:      --space-3 --space-4
  Background:   --bg-surface
  Border:       1.5px solid --border-default
  Radius:       --radius-md
  Font:         --font-sans, --text-base, --text-body
  Placeholder:  --text-muted
  Focus:        Border --brand-primary, --shadow-xs (inset), no outline
  Error:        Border --color-error, error message below in --text-xs --color-error
  Filled:       Border --border-default (unchanged)

Label:
  Font:         --font-sans, --text-sm, --font-medium, --text-primary
  Margin-bottom: --space-2

Select:
  Same as input + custom chevron icon in --text-muted
  Avoid native select — use custom accessible dropdown

Toggle (month-to-month):
  Track:        40px × 22px, --border-default (off), --brand-primary (on)
  Thumb:        18px circle, --color-white, translateX transition
  Label:        Inline right, --text-sm

Checkbox / Multi-select (utilities):
  Custom box: 18px × 18px, --radius-sm
  Checked: --brand-primary fill, white checkmark
  Label: --text-base --text-body

Date Range:
  Two text inputs side-by-side: "Start Date" | "End Date"
  Or a date range picker (avoid mobile complexity — simple inputs preferred)
```

---

### Accordion / Expandable Row

Used for the state services list pattern (reference: "01. Real Estate Law →").

```
Row:
  Padding:        --space-5 0
  Border-bottom:  1px solid --border-default (or --border-dark on dark bg)
  Display:        flex justify-between align-center

Number/Index:
  Font:           --font-sans, --text-sm, --text-muted, --tracking-wide
  Width:          32px

Label:
  Font:           --font-sans, --text-base, --font-medium, --text-primary
  Flex:           1

Icon:
  Arrow (→) or chevron (↓ when open)
  Size:           --icon-md
  Color:          --text-muted → --text-primary on hover

Expanded state:
  Sub-content slides down (max-height transition, --duration-slow, --ease-out)
  Padding-bottom: --space-5

Hover:
  Row background: --bg-surface-alt (on light) or rgba(255,255,255,0.04) (on dark)
```

---

### Trust Indicators

Used near CTAs to reduce purchase anxiety.

```
Checkmark list item:
  Icon:   Checkmark in --brand-accent or --color-success
  Text:   --font-sans, --text-sm, --text-body

Social proof chip:
  Avatar stack (3 faces) + star rating + "4.9 Trust Score"
  Background: rgba(0,0,0,0.4) on dark, --bg-surface on light
  Radius: --radius-full
  Font: --text-sm, --font-medium

Trust badge row:
  Icons + labels: "SSL Secure", "Instant Delivery", "State-Compliant", "No Account Needed"
  Horizontal flex, gap --space-6, centered
  Color: --text-muted (subtle, not loud)
```

---

### Section Header

Reusable heading block used at the top of each page section.

```
Layout:       Two-column: heading left, category label right
              OR centered (for symmetric sections)

Overline:     Small badge (see Badges & Labels — Overline Badge)
              Positioned top-right on two-column layout

Heading:      --font-serif, --text-4xl–5xl on desktop, --text-3xl mobile
              --text-primary (light bg) or --text-inverse (dark bg)

Subheading:   Optional paragraph, --text-lg, --text-body, max-width 560px

Margin-bottom: --space-12 to --space-16 before section content
```

---

### Footer

```
Layout:       Dark background (--bg-inverted)
              Top: Newsletter signup row
              Mid: 4-column grid (Practice Areas | Contact | Address | Brand)
              Bottom: Legal links row + social icons

Newsletter:
  Label:      --font-serif, --text-xl, --text-inverse
  Input:      Dark input (--color-neutral-800 bg, --border-dark border)
  Button:     Icon button (arrow) in --brand-accent

Columns:
  Heading:    --text-sm, --font-semibold, --tracking-wide, uppercase, --text-inverse
  Links:      --text-sm, --text-inverse-muted, hover --text-inverse
  Gap between columns: --space-8

Bottom bar:
  Separator:  1px --border-dark
  Text:       --text-xs, --text-inverse-muted
  Links:      Terms | Privacy | Cookies | Legal
  Social:     Icon buttons, --icon-md, --text-inverse-muted hover --text-inverse
```

---

## Page Patterns

### Hero Section

Adapted from the LexGuard two-panel split hero:

```
Layout:
  Desktop: Two equal columns
    Left:  Dark panel (--bg-darker) with headline, subtext, CTA, stats
    Right: Full-bleed imagery (courthouse / legal document / aerial city)

  Mobile:  Single column, dark background, image hidden or shown as background

Left Panel:
  Padding:      --space-12 --space-10
  Background:   --bg-darker with subtle diagonal texture/pattern overlay (low opacity)

  Overline badge:  "✦ State-Specific Legal Documents"
  H1:           --font-serif, --text-5xl–6xl, --font-extrabold, --text-inverse, --tracking-tight
                Example: "Your Lease Agreement, Ready in 60 Seconds"
  Subtext:      --text-lg, --text-inverse-muted, max-width 440px
  CTA:          Primary button (gold on dark variant)
  Stats row:    3–4 stats (see Stat Cards)

Right Panel:
  Overflow:     hidden
  Image:        object-cover, full height
  Optional overlay: gradient from left (so left panel content stays legible on overlap)
  Trust chip:   Bottom-right overlay (see Trust Indicators — Social proof chip)
```

---

### Two-Column Quiz Layout

```
Desktop layout (/<state> page):
  Left 50%:   Document Preview Panel (sticky, scrolls independently)
  Right 50%:  Quiz Step (scrolls with page)
  Gap:        0 (panels touch or have thin separator)
  Background: --bg-page

Mobile layout:
  Only Quiz Step visible
  After quiz completion: Document Preview shown below quiz, blurred/watermarked
  Before checkout CTA
```

---

### CTA Section

Dark, high-contrast section to drive conversion (reference: "Ready to Take the Next Step?").

```
Background:   --bg-darker or --bg-inverted
Padding:      --space-24 vertical
Layout:       Centered text + button (or two-column with image)

Heading:      --font-serif, --text-4xl–5xl, --text-inverse, max-width 600px
Subtext:      --text-base, --text-inverse-muted
Button:       Primary dark variant (gold background)
```

---

## Accessibility

- **Color contrast:** All text must meet WCAG AA (4.5:1 body, 3:1 large text). Never use gold text on white — only on dark or navy backgrounds.
- **Focus indicators:** Visible focus ring on all interactive elements (2px, --brand-accent color, 2px offset)
- **Keyboard navigation:** Full tab order on quiz steps. No keyboard traps.
- **ARIA:** Quiz is a `<form>`. Each step: `aria-label`, progress indicator `aria-valuenow`. Document preview: `aria-live="polite"` for real-time updates.
- **Reduced motion:** All transforms and transitions respect `prefers-reduced-motion: reduce`
- **Font size:** Minimum `--text-base` (16px) for all body copy. No content below `--text-xs` (12px).
- **Alt text:** All images require descriptive alt text.
- **Semantic HTML:** Use `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>` correctly. Heading hierarchy must not skip levels.

---

## Responsive Breakpoints

```
--screen-sm:    640px    /* Large mobile / small tablet */
--screen-md:    768px    /* Tablet */
--screen-lg:    1024px   /* Desktop */
--screen-xl:    1280px   /* Large desktop */
--screen-2xl:   1536px   /* Wide */
```

**Mobile-first approach.** Write base styles for mobile, use `min-width` breakpoints to enhance for larger screens.

| Element | Mobile | Tablet (md) | Desktop (lg+) |
|---------|--------|-------------|---------------|
| Hero | Single column, stacked | Single column | Two-column split |
| Quiz layout | Full-width quiz only | Full-width quiz | Two-column: doc + quiz |
| State grid | 3 columns | 4 columns | 6–8 columns |
| Navigation | Hamburger | Hamburger | Full horizontal nav |
| Stats row | 3-col (smaller text) | 3-col | 4-col |
| Section padding | `--space-12` | `--space-16` | `--space-24` |
| H1 size | `--text-3xl` | `--text-4xl` | `--text-5xl`–`6xl` |

---

## Voice & Content Guidelines

**Tone:** Authoritative, clear, direct. Not casual. Not corporate-stiff. Think "competent attorney explaining something to a friend."

| Do | Don't |
|----|-------|
| "Get your lease agreement" | "Generate your document" |
| "State-specific. Legally compliant." | "AI-powered document generation" |
| "Ready in 60 seconds" | "Lightning fast ⚡" |
| "No account needed" | "Frictionless experience" |
| "$5. One time. No subscription." | "Just $5/month" |
| "Covers all required disclosures" | "Smart legal technology" |

**Number formatting:**
- Currency: `$5` (not `$5.00`, not `5 dollars`)
- Delivery time: `60 seconds` or `< 1 minute`
- Always spell out state names in full on state pages ("California", not "CA")

**CTA copy:**
- Primary: `Get My [State] Lease — $5`
- Secondary: `See How It Works`
- Post-quiz: `Get My Lease — $5`
- After payment: `Download Your Agreement`

**Error messages:**
- Be specific: "Please enter a valid email address" not "Invalid input"
- Be human: "We couldn't process your payment — please check your card details"

---

*Last updated: 2026-03-11 | Version: 1.0.0*
