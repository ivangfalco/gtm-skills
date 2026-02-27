# Inbound Orchestration — Framework

How to capture, qualify, and activate inbound signals to drive outbound motions. Turning warm intent into booked meetings.

---

## The Inbound-Led Outbound Model

Traditional cold outreach: 6–8% reply rate.
Signal-based outreach: 18–22% reply rate.
Multi-signal stacked: 35–40% reply rate.

**The principle:** Don't just wait for inbound leads to fill out a form. Detect intent signals, enrich them, and trigger outbound before the prospect even reaches out.

---

## The 5 Inbound Signals That Matter

| Signal | Reply Rate | Best Timing | How to Detect |
|---|---|---|---|
| **Website Visitors** | 25–30% | Same day | Clearbit Reveal, 6sense, RB2B, Leadfeeder |
| **Job Changes** (0–90 days) | 3x higher than cold | Days 14–45 | Clay job change tracking, LinkedIn |
| **Hiring for Specific Roles** | Signals budget + growth | Within days of posting | PredictLeads, Apollo, LinkedIn |
| **Funding Announcements** | Fresh capital | 2–4 weeks after announcement | Crunchbase, Intellizence, news |
| **Technology Changes** | Active buying window | Immediately | BuiltWith, HG Insights, 6sense |

---

## Signal Detection → Enrichment → Activation Flow

### Step 1: Detect

Capture signals from:
- **Website visitor identification** — de-anonymize company/person visiting your site
- **Content engagement** — downloads, pricing page views, case study reads
- **Social engagement** — LinkedIn post interactions, ad engagement
- **Intent data providers** — 6sense, Bombora (researching your category)
- **Job change monitoring** — champions moving to new companies
- **Hiring signals** — companies posting roles your solution supports
- **Funding/news** — Crunchbase, press releases, Claygent monitoring

### Step 2: Enrich

Run detected signals through Clay:
- Company enrichment (firmographics, technographics, ICP scoring)
- Contact discovery (find the right person at the company)
- Email waterfall (verify contact info)
- ICP fit scoring (A/B/C/D tier)

### Step 3: Qualify

Apply ICP scoring to determine priority:
- **A-tier (80–100 points):** Hot — route to sales immediately, trigger personalized sequence
- **B-tier (60–79):** Warm — add to nurture sequence with signal-based messaging
- **C-tier (40–59):** Cool — add to content/awareness campaigns
- **D-tier (<40):** Disqualify — don't waste outreach

### Step 4: Activate

Based on tier and signal type:
- **Hot (A-tier + strong signal):** Slack alert to rep + personalized email same day
- **Warm (B-tier or weaker signal):** Automated sequence in Instantly/Smartlead
- **Cool (C-tier):** Content drip, LinkedIn connection, long-term nurture

---

## Signal Stacking

The more signals that overlap, the hotter the lead:

| Signals Stacked | Classification | Action |
|---|---|---|
| 1 signal | Warm | Add to sequence |
| 2 signals | Hot | Priority outreach within 24 hours |
| 3+ signals | On fire | Same-day outreach, Slack alert, sales call |

**Example:** Company visited your pricing page (signal 1) + recently raised Series B (signal 2) + hiring for the role your product serves (signal 3) = immediate, personalized outreach.

---

## Clay Templates for Inbound Orchestration

| Template | What It Does |
|---|---|
| Website Visitor → Enrichment → Sequence | De-anonymize → enrich → push to outbound |
| Job Change Tracker | Monitor champion movements → trigger re-engagement |
| Funding Announcement Tracker | Detect funding → enrich → route to sales |
| Hiring Signal Detector | Detect relevant job posts → enrich → sequence |
| Multi-Signal Stacker | Combine 3+ signals → heat score → prioritize |
| Slack Notification Workflow | Alert reps on hot inbound signals |

---

## Intent Data Providers

| Provider | Best For | Notes |
|---|---|---|
| **Clearbit Reveal** | Website visitor identification | Company-level de-anonymization |
| **6sense** | Buyer intent, account identification | Category-level intent signals |
| **Bombora** | Topic-based intent | Shows what topics companies research |
| **RB2B** | Person-level website visitor ID | Individual visitor identification |
| **Leadfeeder** | Website visitor tracking | Company-level with page-level detail |

---

## Inbound Lead Source Performance

Not all inbound channels convert equally. Channel selection impacts conversion more than messaging optimization.

| Lead Source | MQL → SQL Conversion | Notes |
|---|---|---|
| **SEO** | 51% | Highest mid-funnel conversion. Strong intent from organic search. |
| **Email Marketing** | 46% | High conversion but lower opportunity-to-close rates (needs nurture). |
| **Webinars** | 30% | Engaged audiences, time investment = qualified interest. |
| **PPC** | 26% | Lower mid-funnel but recovers with strong opportunity-to-close rates. |
| **Events** | 24% | Relationship-building, requires long-term nurture. |

*Source: ColdIQ — compiled B2B benchmarks*

**Key insight:** SEO-generated leads convert at nearly 2x the rate of PPC. Evaluate whether paid budgets could generate better returns through organic investment.

---

## MQL → SQL Handoff

### Definitions

- **MQL (Marketing Qualified Lead):** Lead who raised their hand through bottom-of-funnel engagement (demo request, pricing page, content download).
- **SAL (Sales Accepted Lead):** Discovery call booked with intended prospect.
- **SQL (Sales Qualified Lead):** Meeting held with intended prospect where basic needs fit is identified.

### Qualification: BANT Framework

To convert an MQL to an Opportunity, gather:
- **Budget** — Do they have budget allocated?
- **Authority** — Are you talking to the decision-maker?
- **Need** — Do they have the problem you solve?
- **Timeline** — When are they looking to act?

### Speed-to-Lead SLA

| Response Time | MQL → SQL Conversion |
|---|---|
| Within 1 hour | 53% |
| After 24 hours | 17% |

**The gap is 36 percentage points.** Slow handoffs punish conversion more than any other funnel factor.

**Recommendations:**
- Automated chat sequences and calendar links to eliminate coordination delays
- Slack alerts for hot inbound leads
- Sub-1-hour response SLA for A-tier signals

---

## Attribution Models

Run multiple models in parallel:

| Model | What It Credits | Best For |
|---|---|---|
| **First-touch** | First interaction that generated the lead | Understanding top-of-funnel channel effectiveness |
| **Last-touch** | Final action before conversion/opportunity | Understanding what closes deals |
| **Multi-touch** | Weighted credit across all touchpoints | Full picture of the buyer journey |

### Pipeline Definitions

- **Marketing-Sourced Pipeline (MSP):** Opportunities whose first recorded touch came from marketing. More accountable.
- **Marketing-Influenced Pipeline (MIP):** Opportunities that engaged with marketing at any stage. Richer but less accountable.

*Source: ColdIQ*

---

## The RevOps Framework (3 Pillars)

1. **Demand Generation** — Attracting ICP-fit leads through referrals, content, paid, outbound
2. **Pipeline Management** — Standardizing stages, lead scoring, clearing bottlenecks
3. **Customer Success** — Retention, expansion, upsells

Companies with aligned RevOps see **19% faster revenue growth YoY**. Misaligned operations lose **up to 10% of potential revenue**.

---

## Tech Stack for Inbound Orchestration

| Function | Recommended Tools |
|---|---|
| CRM | HubSpot, Salesforce |
| Data enrichment | Clay, Clearbit |
| Lead sourcing | Apollo, LinkedIn Sales Navigator |
| Intent data | 6sense, Bombora, Clearbit Reveal, RB2B |
| Automation | N8N (no-code), Zapier, Segment |
| Engagement routing | Calendly (route meetings back to CRM) |
| Sales engagement | Outreach, SalesLoft, Instantly, Smartlead |
| Conversation intelligence | Gong, Chorus |

**Integration requirements:**
- Standardized UTM templates
- Server-side tagging
- Nightly syncs for enrichment
- Consistent field naming across systems

*Source: ColdIQ*

---

## Chat/Chatbot → Routing Workflow

### The Flow

```
Visitor lands on site
  → Chatbot triggers (high-intent pages: pricing, demo, features)
  → Bot qualifies with 3-4 BANT-lite questions:
     1. "What brings you here today?" (need)
     2. "How many people on your team?" (company size → fit)
     3. "Are you evaluating solutions now or researching?" (timeline)
     4. "What's your role?" (authority)
  → Score based on responses:
     High-intent: Route to live rep OR auto-book via Calendly
     Medium-intent: Offer content + add to nurture sequence
     Low-intent: Self-serve resources
```

### Chatbot Best Practices

- **Trigger on high-intent pages only** — pricing, demo request, product pages. Don't interrupt blog readers.
- **Keep it to 3-4 questions max** — long chatbot flows kill conversion.
- **Offer instant booking** — integrate Calendly/HubSpot Meetings so qualified visitors can book immediately.
- **CRM auto-create** — every chatbot conversation creates a contact in CRM with transcript attached.
- **Fallback to human** — if bot can't qualify, route to live chat during business hours, email outside hours.

### HubSpot Chatbot Setup

1. **Chatflows tool** → Create a targeted chatbot
2. Set trigger rules: URL contains `/pricing` or `/demo` or `/product`
3. Build qualification branches (if/then based on responses)
4. Qualified path → "Book a meeting" action (connects to team calendar)
5. Unqualified path → "Send content" action + add to nurture workflow
6. All conversations → auto-create contact with lifecycle stage = Lead

---

## Demo Request → Booking Flow

### The Ideal Flow (Sub-5-Minute Experience)

```
Prospect clicks "Book a Demo"
  → Short form (5 fields max):
     - Work email
     - First name
     - Company name
     - Company size (dropdown)
     - What are you looking to solve? (dropdown or free text)
  → Auto-enrich via Clay/Clearbit (firmographics, ICP score)
  → Auto-score:
     ICP fit ≥ 60? → Show calendar immediately (Calendly/HubSpot Meetings)
     ICP fit < 60? → "We'll be in touch" + route to SDR for manual review
  → Meeting booked:
     - CRM deal auto-created
     - AE/SDR assigned via round-robin
     - Confirmation email with prep materials
     - Slack alert to assigned rep
     - Reminder sequence triggered (24hr + 1hr before)
```

### Critical Rules

- **Never make them wait.** If they're qualified, show calendar instantly. Sub-1-hour response = 53% conversion.
- **Minimize form fields.** Every extra field reduces conversion ~10%. Enrich later with Clay, not upfront with forms.
- **Calendar integration required.** No "someone will contact you" for A-tier prospects.
- **No-show follow-up.** If they miss the meeting: auto-email within 1 hour with reschedule link.
- **Prep the rep.** Auto-send rep a brief with company info, ICP score, what the prospect said, and relevant content to reference.

---

## Content Engagement Scoring Weights

### Which Content Signals Higher Intent?

| Content Type | Intent Level | Score Weight | Reasoning |
|---|---|---|---|
| **Demo/product tour views** | Very High | +30 | 9+ demo views = 8-10x higher close rate (2025 B2B Buyer Behavior Report) |
| **Pricing page visit** | Very High | +25 | Active evaluation, comparing options |
| **Case study download** | High | +20 | Evaluating proof, building business case |
| **ROI calculator usage** | High | +20 | Quantifying value, preparing for internal sell |
| **Comparison page visit** | High | +18 | Actively evaluating competitors |
| **Whitepaper download** | Medium-High | +15 | 76% of B2B decision-makers rely on whitepapers; 84% of C-suite influenced |
| **Webinar attendance** | Medium | +12 | Time investment = genuine interest |
| **Blog post read** | Low-Medium | +5 | Awareness stage, not buying signal |
| **Newsletter subscribe** | Low | +3 | Interest, but far from purchase |
| **Social media engage** | Low | +2 | Awareness only |

### Scoring Modifiers

| Modifier | Adjustment | Reasoning |
|---|---|---|
| **Recency** | +50% if within last 7 days | Recent activity = more likely to convert |
| **Frequency** | +25% if 3+ visits in a week | Multiple visits = active research |
| **Time decay** | -10% per week of inactivity | Old signals lose relevance |
| **Page depth** | +10% if 3+ pages in session | Deeper engagement = higher intent |
| **Repeat pricing visit** | +15 (extra) | Coming back to pricing = strong signal |

### Three-Dimensional Scoring (Best Practice)

Combine three dimensions for accurate lead scoring:

1. **Fit** (firmographic/technographic) — ICP scoring, company size, industry, tech stack
2. **Intent** (third-party signals) — topic research, competitor research, keyword clusters
3. **Engagement** (first-party actions) — content consumed, pages visited, emails clicked

*Source: ColdIQ — compiled B2B benchmarks*

---

## HubSpot Workflow Configurations

### Workflow 1: Inbound Lead → Qualification → Routing

**Trigger:** Contact created with source = "Organic" or "Paid" or "Direct"

```
IF HubSpot Score ≥ 80 (A-tier):
  → Set lifecycle stage = MQL
  → Assign to SDR (round-robin)
  → Send Slack notification (#hot-leads)
  → Enroll in "MQL Follow-up" sequence
  → Create task: "Contact within 1 hour"

IF HubSpot Score 60-79 (B-tier):
  → Set lifecycle stage = MQL
  → Assign to SDR (round-robin)
  → Enroll in "Warm Lead" nurture workflow
  → Create task: "Contact within 4 hours"

IF HubSpot Score 40-59 (C-tier):
  → Set lifecycle stage = Lead
  → Enroll in "Content Nurture" workflow
  → No sales assignment yet

IF HubSpot Score < 40 (D-tier):
  → Set lifecycle stage = Subscriber
  → Enroll in "Newsletter" workflow only
```

### Workflow 2: Demo Request → Meeting Booking

**Trigger:** Form submission on "Book a Demo" page

```
→ Set lifecycle stage = MQL
→ Enrich via Clay integration (company data, ICP score)
→ IF ICP score ≥ 60:
    → Assign to AE/SDR (round-robin, weighted by capacity)
    → Send Slack alert with contact details + ICP score
    → Send confirmation email with calendar link
    → Create deal in pipeline (stage: "Demo Requested")
    → Set deal amount based on company size estimate
→ IF ICP score < 60:
    → Assign to SDR for manual review
    → Send "Thanks, we'll be in touch" email
    → Create task: "Review demo request" (due: 24 hours)
```

### Workflow 3: Website Visitor Signal → Outbound

**Trigger:** Clearbit Reveal / RB2B identifies company visiting high-intent pages

```
→ Push to Clay table
→ Clay enriches: company firmographics, contact discovery, email waterfall
→ IF ICP score ≥ 70 AND visited pricing/demo page:
    → Push to Instantly with signal-based personalization
    → Slack alert to SDR
→ IF ICP score 50-69:
    → Push to warm nurture sequence
→ IF ICP score < 50:
    → Log for analysis, don't outreach
```

### Key HubSpot Settings

| Setting | Configuration | Why |
|---|---|---|
| **Lifecycle stage sync** | Enable contact → company sync | Keeps records aligned |
| **Lead scoring** | Build in Contact Properties → HubSpot Score | Foundation for routing |
| **Required properties per deal stage** | Settings → Deals → Stage Properties | Forces data quality |
| **Notification preferences** | Enable Slack integration | Real-time hot lead alerts |
| **Meeting scheduling** | HubSpot Meetings or Calendly embed | Sub-1-minute booking experience |

*Source: ColdIQ*

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
