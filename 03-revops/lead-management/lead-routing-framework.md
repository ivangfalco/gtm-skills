# Lead Routing — Framework

How leads get scored, tiered, and routed to the right destination (rep, sequence, nurture, or disqualify).

---

## The Routing Principle

Not all leads are equal. Routing determines WHERE a lead goes and HOW FAST based on:
1. **ICP fit** (firmographic/technographic match)
2. **Signal strength** (behavioral intent)
3. **Lead tier** (A/B/C/D classification)

**Speed to lead is the #1 conversion lever.** Data shows responding within 1 hour yields **53% MQL→SQL conversion**, compared to **17% after 24 hours** — a 36-point gap that punishes slow handoffs more than any other funnel factor.

---

## ICP Scoring → Tier → Route

### Scoring System (from List Building)

| Criteria | Points |
|---|---|
| Right industry | +20 |
| Right company size | +20 |
| Right revenue range | +15 |
| Uses key tech | +15 |
| Recent funding | +10 |
| Hiring for relevant role | +10 |
| Target location | +10 |
| **Total possible** | **100** |

### Tier Classification

| Tier | Score | Fit | Action |
|---|---|---|---|
| **A-tier** | 80–100 | Perfect fit, strong signals | Priority — route to sales, personalized sequence |
| **B-tier** | 60–79 | Good fit, some signals | Pursue — automated sequence, medium priority |
| **C-tier** | 40–59 | Okay fit, weak signals | Nurture — content campaigns, long-term |
| **D-tier** | <40 | Poor fit | Disqualify — do not outreach |

---

## Routing Destinations

### By Tier

| Tier | Destination | Channel | Timing |
|---|---|---|---|
| **A-tier + hot signal** | Sales rep (Slack alert) | Personalized email + LinkedIn | Same day |
| **A-tier** | Premium sequence (Instantly/Smartlead) | Personalized cold email | Within 24 hours |
| **B-tier** | Automated sequence | Signal-based cold email | Within 48 hours |
| **C-tier** | Content/nurture campaign | Newsletter, content drip | Ongoing |
| **D-tier** | Blocklist or disqualify | None | N/A |

### By Signal Type

| Signal | Route |
|---|---|
| Website visitor (pricing page) | Immediate Slack alert + same-day outreach |
| Job change (champion at new company) | Personalized re-engagement sequence |
| Funding announcement | Sequence triggered 2–4 weeks after |
| Hiring for relevant role | Signal-based sequence |
| Content download | Nurture sequence |

---

## Clay → Sequencer Push

### Clay → Instantly

Push qualified leads directly from Clay to Instantly campaigns:
- Filter by tier (A-tier and B-tier only)
- Map fields: email, first name, company, personalization columns
- Use campaign tags to organize by signal type

### Clay → Smartlead

Same principle, push to Smartlead sequences:
- Filter by qualification criteria
- Map required fields
- Tag by campaign/signal

### Conditional Logic

Only push leads that meet ALL criteria:
- Email is verified (not catch-all, not risky)
- ICP score ≥ 60 (B-tier or above)
- Not on blocklist
- Not already in an active sequence (dedupe check)

---

## Blocklist System

**Build before your first campaign. Non-negotiable.**

### What to Track

| Field | Purpose |
|---|---|
| Domain or email | What's blocked |
| Reason | Opted out, competitor, wrong fit, bounce, do-not-contact |
| Date added | When it was blocked |
| Campaign | Which campaign triggered the block |
| Added by | Which team member |

### Blocklist Checks

Every Clay table should check against the blocklist BEFORE pushing to any sequence. Automate this — saves 10+ hours/week.

---

## Slack Alerts for Hot Leads

When a lead meets hot criteria (A-tier + strong signal), trigger a Slack notification:

**Alert should include:**
- Contact name, title, company
- ICP score and tier
- Signal(s) detected
- LinkedIn URL
- Suggested next action

---

## Lead Scoring Intelligence

### Static vs Behavioral Scoring

| Approach | How It Works | MQL → SQL Rate |
|---|---|---|
| **Demographic/firmographic only** | Points for company size, industry, title | ~13% (baseline) |
| **Behavioral scoring models** | Adds engagement signals, page visits, content consumption | 39–40% |
| **Shared CRM dashboards + unified definitions** | Marketing and sales operate from same lead definitions | 30%+ |

*Source: ColdIQ — compiled B2B benchmarks*

**Key insight:** Companies using behavioral scoring achieve **3x the conversion rate** of demographic-only approaches. Static point systems can't handle modern SaaS buyer journeys spanning multiple stakeholders.

### Engagement Scoring Signals

| Signal | Weight | Reasoning |
|---|---|---|
| Demo/pricing page visit | High (+25) | Bottom-of-funnel intent |
| Booked meeting | Very High (+30) | Direct action |
| Case study download | Medium (+15) | Evaluating solutions |
| Blog post read | Low (+5) | Top-of-funnel awareness |
| Email open (no click) | Minimal (+2) | Passive engagement |
| Webinar attendance | Medium (+15) | Time investment = qualified interest |
| Multiple site visits (3+ in a week) | High (+20) | Researching actively |

---

## SLA Definitions by Tier

| Tier | Initial Response SLA | Follow-Up Cadence | Escalation Trigger |
|---|---|---|---|
| **A-tier + hot signal** | < 1 hour | Same day, then daily x3 | If not contacted in 2 hours |
| **A-tier** | < 4 hours | Within 24 hours, then every 2 days | If not contacted in 8 hours |
| **B-tier** | < 24 hours | Within 48 hours, then every 3 days | If not contacted in 48 hours |
| **C-tier** | < 48 hours | Auto-nurture weekly | N/A — automated |

### Escalation Path

1. **Alert owner** — Slack reminder if SLA is about to breach
2. **Alert manager** — If SLA breaches by 2x
3. **Re-route** — If no action after 3x SLA, lead gets reassigned to next available rep

---

## Routing Logic Patterns

### Round-Robin Assignment
- Distribute leads equally among reps
- Weight by rep capacity (if Rep A has 20 active deals, Rep B has 10, prioritize Rep B)
- Skip reps on PTO or at capacity

### Territory-Based Routing

| Territory Type | Routing Logic |
|---|---|
| **Geographic** | West Coast → Rep A, East Coast → Rep B |
| **Vertical** | Healthcare → Rep C, SaaS → Rep D |
| **Account size** | Enterprise (500+) → Sr. AE, SMB (<100) → Jr. AE |

### Named Account Routing
- Strategic/target accounts → pre-assigned specific rep
- Override round-robin for named accounts
- Maintain named account list in CRM, update quarterly

### Inbound Form Routing Flow

```
Form Fill → CRM (auto-create contact/lead)
  → Enrich via Clay (firmographics, tech stack)
  → Score (ICP fit + engagement)
  → Route by tier:
     A-tier: Slack alert + assign to rep
     B-tier: Assign to rep + auto-sequence
     C-tier: Auto-nurture campaign
     D-tier: Blocklist/disqualify
```

---

## MQL → SQL Conversion by Lead Source

Understanding which channels produce the best SQLs informs routing priority:

| Lead Source | MQL → SQL Rate | Routing Implication |
|---|---|---|
| **SEO** | 51% | Route aggressively — these are high-intent |
| **Email Marketing** | 46% | Route quickly but needs nurture to close |
| **Webinars** | 30% | Medium priority, engaged but early stage |
| **PPC** | 26% | Lower mid-funnel, route to nurture + sequence |
| **Events** | 24% | Long-term nurture, don't rush |

*Source: ColdIQ — compiled B2B benchmarks*

---

## HubSpot Routing Workflow Configurations

### Workflow 1: New Lead → Score → Route

**Trigger:** Contact created (any source)

```
Step 1: Wait 2 minutes (allow enrichment to populate)
Step 2: Branch by HubSpot Score

IF Score ≥ 80 (A-tier):
  → Set lifecycle stage = MQL
  → Set lead status = "New"
  → IF contact property "State/Region" = West:
      → Assign to Rep A
  → ELIF "State/Region" = East:
      → Assign to Rep B
  → ELSE:
      → Round-robin assign (Team: SDR)
  → Send Slack notification to #hot-leads
  → Create task: "Follow up within 1 hour"

IF Score 60-79 (B-tier):
  → Set lifecycle stage = MQL
  → Round-robin assign (Team: SDR)
  → Enroll in "B-tier Outreach" sequence
  → Create task: "Follow up within 4 hours"

IF Score 40-59 (C-tier):
  → Set lifecycle stage = Lead
  → Enroll in "Nurture" workflow
  → No rep assignment

IF Score < 40 (D-tier):
  → Set lifecycle stage = Subscriber
  → Enroll in "Newsletter Only" workflow
```

### Workflow 2: Demo Request → Instant Route

**Trigger:** Form submission on demo/pricing page

```
→ Set lifecycle stage = MQL
→ Set lead status = "Attempting to Contact"
→ Branch by company size:
    IF employees ≥ 500 (Enterprise):
      → Assign to Sr. AE (named account list check first)
      → Send Slack to #enterprise-leads
      → Create deal: Stage = "Demo Requested", Amount = estimated
    IF employees 50-499 (Mid-Market):
      → Round-robin assign (Team: MM AEs)
      → Send Slack to #mm-leads
      → Create deal
    IF employees < 50 (SMB):
      → Round-robin assign (Team: SMB AEs)
      → Auto-send calendar link email
→ Send confirmation email with prep materials
→ Create task: "Confirm meeting within 30 minutes"
```

### Workflow 3: SLA Enforcement

**Trigger:** Contact property "Lead Status" = "New" for > [SLA time]

```
IF A-tier AND uncontacted for > 2 hours:
  → Send Slack alert to rep: "SLA BREACH: A-tier lead unworked"
  → Wait 2 hours
  → IF still uncontacted:
      → Send Slack to manager
      → Reassign to next available rep (round-robin)

IF B-tier AND uncontacted for > 48 hours:
  → Reassign to next available rep
  → Send Slack to manager

IF any lead uncontacted for > 7 days:
  → Recycle: Set lifecycle stage back to "Lead"
  → Remove rep assignment
  → Enroll in "Recycled Lead Nurture" workflow
```

### Key HubSpot Configuration Steps

1. **Contact properties to create:**
   - `ICP Score` (number, 0-100)
   - `Lead Tier` (dropdown: A/B/C/D)
   - `Signal Type` (multi-checkbox: Website Visit, Job Change, Funding, Hiring, Tech Change)
   - `First Response Time` (date/time — stamps when rep first acts)

2. **Team setup:**
   - Create teams: Enterprise AEs, MM AEs, SMB AEs, SDRs
   - Enable round-robin within teams
   - Set capacity limits per rep

3. **Slack integration:**
   - Connect HubSpot → Slack via native integration
   - Create channels: #hot-leads, #enterprise-leads, #mm-leads, #sla-alerts

4. **Required deal properties per stage:**
   - Demo Requested: Company size, Source
   - Discovery: BANT fields (budget range, decision-maker confirmed, need identified, timeline)
   - Proposal: Deal amount, Close date, Decision criteria
   - Negotiation: Contract terms, Legal status

---

## Capacity-Based Routing

### Why It Matters

Round-robin alone doesn't account for rep workload. A rep with 30 active deals shouldn't get the same lead volume as one with 10.

### Capacity Model

| Factor | Weight | How to Measure |
|---|---|---|
| **Active deals** | High | Open deals in pipeline (HubSpot deal count) |
| **Meeting load this week** | Medium | Calendar meetings scheduled |
| **Deal stage distribution** | Medium | Rep heavy in late-stage = less capacity for new leads |
| **PTO / availability** | High | Calendar blocks, OOO status |
| **Quota attainment** | Low | Reps ahead of quota can absorb more |

### Implementation Options

| Tool | How It Works | Best For |
|---|---|---|
| **HubSpot round-robin + manual** | Set round-robin, manually adjust when reps are at capacity | Small teams (2-5 reps) |
| **Chili Piper** | Automated routing with capacity rules, instant calendar booking | Mid-market teams, demo-heavy flows |
| **LeanData** | Visual routing flowcharts with capacity, territory, account matching | Enterprise, Salesforce-first |
| **Ringlead** | Dedup + route with capacity balancing | Large teams with data quality issues |
| **Custom (N8N/Zapier)** | Build capacity logic: pull deal count from CRM → route to lightest rep | Budget-friendly, custom rules |

### Simple Capacity Formula

```
Available Capacity = Max Deals per Rep - Current Active Deals

IF Available Capacity > 0:
  → Eligible for new leads
IF Available Capacity ≤ 0:
  → Skip in round-robin until capacity opens
```

**Benchmark:** Most B2B SDRs can effectively work 20-30 active leads at a time. AEs: 15-25 active deals.

---

## Re-Engagement Routing (Dormant Leads Reactivated)

### When Dormant Leads Come Back

| Re-Engagement Signal | What Happened | Routing Action |
|---|---|---|
| **Website revisit** (after 60+ days of silence) | They're researching again | Route to original owner if available, otherwise round-robin |
| **Email re-engagement** (clicked after 90+ days) | Something triggered interest | Enrich with Clay for new data → re-score → route by tier |
| **Job change** (champion moved to new company) | New opportunity at new org | Route as NEW lead to SDR, reference old relationship |
| **Closed-lost revisit** (pricing page after 6+ months) | Circumstances may have changed | Route to original AE, Slack alert with deal history |
| **Content re-engagement** (downloads new asset) | Back in research mode | Add to warm sequence, don't hard-sell yet |

### HubSpot Re-Engagement Workflow

**Trigger:** Contact last activity date was > 90 days ago AND new activity detected today

```
→ Re-enrich via Clay (new company data? new role? new tech stack?)
→ Re-score ICP fit
→ Branch:
    IF previously Closed-Lost:
      → Route to original deal owner
      → Slack alert: "Closed-lost [Name] from [Company] is back on your site"
      → Include: old deal notes, new activity, updated ICP score
    IF previously in nurture (C-tier):
      → Re-score: did they upgrade to B or A tier?
      → IF yes: route to SDR, upgrade lifecycle stage
      → IF no: keep in nurture, note the activity
    IF previously D-tier:
      → Re-score: circumstances may have changed
      → IF now ≥ 60: route as new lead
      → IF still < 60: log and monitor
```

### Rules for Re-Engagement

1. **Never treat a re-engaged lead as fully cold.** They have history — reference it.
2. **Check for data changes first.** They may have switched companies, gotten promoted, or changed tech stack.
3. **Route to the original owner when possible.** Relationship continuity converts better.
4. **Don't auto-blast.** Re-engaged leads get a thoughtful, personalized touch — not a generic sequence.
5. **Update CRM notes.** Log the re-engagement signal so the rep has full context.

*Source: ColdIQ*

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
