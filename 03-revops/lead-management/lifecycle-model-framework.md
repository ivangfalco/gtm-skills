# Lifecycle Model — Framework

How contacts and companies move through stages from unknown → qualified → customer → retained/expanded.

---

## The Lifecycle Principle

Every contact exists in a stage. Knowing the stage determines:
- What messaging they receive
- Who owns them (marketing vs sales vs CS)
- What actions are appropriate
- When to escalate or nurture

---

## ICP-Based Qualification Layers (from List Building)

Before a lead enters the pipeline, it passes through 4 qualification layers:

### Layer 1: Firmographics
Industry, company size, revenue, location, funding stage, business model.

### Layer 2: Technographics
CRM, marketing automation, sales tools, analytics, infrastructure, competitor tools.

### Layer 3: Behavioral Signals
Hiring, funding, expansion, leadership changes, product launches, tech stack changes, content engagement.

### Layer 4: Psychographics
Growth mindset, innovation vs stability, data-driven culture, customer-centric, compliance-focused.

**Scoring:** 0–100 points across these layers → A/B/C/D tier.

---

## Qualification Framework

### Must-Haves (Non-negotiable)
- Industry: [defined per client]
- Company size: [range]
- Revenue: [range]
- Location: [regions]
- Tech stack: [must use X]

### Nice-to-Haves (Bonus)
- Funding stage
- Hiring signals
- Complementary tools

### Disqualifiers (Anti-ICP)
- Too small
- Wrong industry
- Wrong tech stack
- On blocklist

---

## Re-Engagement Cycles

### Closed-Lost Deals (6+ months old)
These are gold. They had the problem, just bad timing or price. Circumstances change.

**Re-engagement approach:**
1. Export from CRM (past 6–12 months)
2. Import to Clay
3. Enrich with fresh data: new funding? new leadership? headcount growth? tech stack changes?
4. Re-engage with a new angle based on what changed

### Churned Customers (past 12 months)
Circumstances may have changed. New leadership, new budget, new priorities.

**Re-engagement approach:**
1. Export churned customers from CRM
2. Enrich for changes
3. Reach out with "what's changed" angle

### CRM Sync Principle
**Enrich, don't overwrite.** CRM sync should add new data (enrichment) without destroying manually entered notes, deal context, or relationship data.

---

## Data Decay

Contact and company data decays at ~30% per year:
- People change jobs
- Companies get acquired, rebrand, shut down
- Emails become invalid
- Phone numbers change

**Implication:** Refresh lists monthly. Re-enrich existing CRM data quarterly.

---

## Full Lifecycle Stage Definitions

### Pre-Pipeline Stages

| Stage | Definition | Entry Criteria | Owner |
|---|---|---|---|
| **Subscriber** | Known contact, no engagement yet | Filled a form, subscribed to newsletter | Marketing |
| **Lead** | Showing awareness-level interest | Visited website, downloaded content, attended webinar | Marketing |
| **MQL (Marketing Qualified Lead)** | Raised hand through bottom-of-funnel engagement | Demo request, pricing page visit, high engagement score (50+) | Marketing → SDR handoff |
| **SAL (Sales Accepted Lead)** | Discovery call booked with intended prospect | SDR booked the meeting, confirmed ICP fit | SDR |
| **SQL (Sales Qualified Lead)** | Meeting held, basic needs fit identified | BANT confirmed: Budget, Authority, Need, Timeline | AE |

*Source: ColdIQ RevOps framework*

### Pipeline Stages

| Stage | Definition | Entry Criteria | Owner |
|---|---|---|---|
| **Opportunity** | Qualified prospect in active sales process | BANT confirmed, deal created in CRM | AE |
| **Proposal** | Solution presented, pricing shared | Demo completed, proposal sent | AE |
| **Negotiation** | Terms being discussed | Proposal reviewed, pricing/legal discussions | AE |
| **Closed Won** | Deal signed | Contract executed | AE → CS handoff |
| **Closed Lost** | Deal lost | Prospect declined, went with competitor, went dark | AE (re-engagement later) |

### Post-Sale Stages

| Stage | Definition | Entry Criteria | Owner |
|---|---|---|---|
| **Onboarding** | New customer setup and activation | Contract signed | CS |
| **Adoption** | Customer actively using the product | Key milestones hit (first campaign, first result) | CS |
| **Expansion** | Customer growing usage | Upsell/cross-sell opportunity identified | CS + AE |
| **Renewal** | Contract renewal period | 90 days before renewal date | CS |
| **Evangelist** | Customer actively referring others | NPS 9–10, case study, referral | CS + Marketing |

---

## BANT Qualification Framework

Before an MQL becomes an Opportunity, gather all four:

| Criteria | Questions to Ask | Red Flags |
|---|---|---|
| **Budget** | "Do you have budget allocated for this?" "What's the expected investment range?" | "We don't have budget" / "We'd need to get approval" (still okay — just longer timeline) |
| **Authority** | "Who else would be involved in this decision?" "Are you the final decision-maker?" | No access to economic buyer after 2+ calls |
| **Need** | "What problem are you trying to solve?" "What happens if you don't solve it?" | No clear pain or urgency |
| **Timeline** | "When are you looking to implement?" "Is there a trigger driving this?" | "Sometime next year" with no urgency driver |

---

## MQL → SQL Conversion Benchmarks by Industry

| Industry | MQL → SQL Rate | Key Factors |
|---|---|---|
| CRM & Sales Tech | 42% | Precise targeting, strong product-need fit |
| Legaltech | 40% | Sophisticated buyers, email + SEO work well |
| B2B SaaS (Enterprise, top) | Up to 40% | Advanced scoring + tight alignment |
| Project Management SaaS | 37% | High initial interest, trial qualification needed |
| Edtech | 35% | Strong once in funnel; acquisition is the hard part |
| Adtech | 35% | Saturated market, differentiation critical |
| PPC/Paid | 26% | Lower mid-funnel, recovers at close stage |
| Industrial & Manufacturing SaaS | 16–18% | Limited competition, pricing transparency helps |
| Cybersecurity (SMB) | 15–18% | Multi-stakeholder approvals extend cycles 35% |
| B2B SaaS (General median) | 13–15% | Baseline — longer cycles, buying committees |
| Fintech | 11–19% | Market maturity creates wide variance |
| IT & Managed Services | 13% | Technical complexity, evolving security |
| Financial Services | 13% | Conservative, sensitive data, multiple decision-makers |
| Healthcare & Medtech | 13–14% | HIPAA compliance, multi-stage approvals |
| Biotech & Pharma | 14–15% | Regulatory environments, 22% monthly data decay |

*Source: ColdIQ — compiled B2B industry benchmarks*

---

## Stage Transition Rules

### Entry/Exit Criteria

| Transition | Trigger | Automation |
|---|---|---|
| Lead → MQL | Engagement score hits 50+, OR demo request, OR pricing page visit | CRM auto-updates lifecycle stage |
| MQL → SAL | SDR books discovery call | CRM workflow: assign to SDR, Slack alert |
| SAL → SQL | Meeting held + BANT confirmed | SDR marks as qualified, AE accepts |
| SQL → Opportunity | Deal created in CRM | AE creates deal with amount, close date |
| Opportunity → Proposal | Demo completed, proposal sent | CRM stage update + task to follow up |
| Any → Closed Lost | Prospect declines or goes dark | CRM closed-lost reason required (dropdown) |

### Lead Aging Rules

| Stage | Max Time Before Action | Action |
|---|---|---|
| MQL (not contacted) | 48 hours | Re-route to next SDR, manager alert |
| SAL (no meeting held) | 7 days | Recycle back to MQL for re-nurture |
| SQL (no deal created) | 14 days | AE required to update with reason |
| Opportunity (no activity) | 21 days | Manager review, potential recycle |

### Recycling Rules

| Scenario | Action |
|---|---|
| SQL → no deal after 14 days | Recycle to MQL, re-enter nurture |
| Closed-Lost (timing) | Re-enter nurture for 90 days, then re-qualify |
| Closed-Lost (competitor) | 6-month wait, then re-engage with new angle |
| Closed-Lost (no budget) | Monitor for funding signals, re-engage when detected |

---

## Ownership Transitions

| From Stage | To Stage | Handoff From → To | What Transfers |
|---|---|---|---|
| MQL | SAL | Marketing → SDR | Lead record, engagement history, ICP score |
| SQL | Opportunity | SDR → AE | Qualification notes, BANT details, contact info |
| Closed Won | Onboarding | AE → CS | Deal context, expectations set, key contacts |
| Expansion | Renewal | CS → CS + AE | Usage data, expansion opportunity notes |

**Handoff rule:** The outgoing owner must leave a brief note in CRM with context. No "cold" handoffs.

---

## Churn Risk Signals & Early Warning

| Signal | Risk Level | Action |
|---|---|---|
| Product usage drops 40%+ | High | CS outreach within 48 hours |
| Support tickets spike 3x+ | High | CS escalation, executive sponsor check-in |
| No login in 30 days | Medium-High | Automated "how can we help" email + CS call |
| Missed QBR / no-show | Medium | Reschedule within 1 week, escalate if missed again |
| Key champion leaves | Medium | Identify new champion, re-onboard |
| NPS drops below 7 | Medium | CS deep dive, recovery plan |
| Competitor mentioned on call | Low-Medium | Flag to AE, prepare competitive battle card |

---

## HubSpot CRM Property/Field Mapping per Stage

### Contact Properties

| Property | Type | Used At Stage | Purpose |
|---|---|---|---|
| `Lifecycle Stage` | Dropdown (default) | All | Tracks current stage (Subscriber → Customer → Evangelist) |
| `Lead Status` | Dropdown (default) | Lead → SQL | Tracks sales engagement (New, Attempting, Connected, Qualified, Disqualified) |
| `ICP Score` | Number (custom) | Lead onward | 0-100 firmographic/technographic fit score |
| `Lead Tier` | Dropdown (custom) | MQL onward | A/B/C/D classification |
| `Signal Type` | Multi-checkbox (custom) | MQL onward | Website visit, Job Change, Funding, Hiring, Tech Change |
| `BANT - Budget` | Dropdown (custom) | SQL | Confirmed / Unknown / No Budget |
| `BANT - Authority` | Dropdown (custom) | SQL | Decision Maker / Influencer / End User |
| `BANT - Need` | Single-line text (custom) | SQL | Primary pain point identified |
| `BANT - Timeline` | Dropdown (custom) | SQL | This month / This quarter / Next quarter / No timeline |
| `First Response Time` | DateTime (custom) | MQL | Stamps when rep first contacted |
| `Original Source` | Dropdown (default) | All | Organic, Paid, Direct, Referral, Outbound |
| `NPS Score` | Number (custom) | Customer | Last NPS response |
| `Churn Risk` | Dropdown (custom) | Customer | High / Medium / Low based on health score |

### Deal Properties

| Property | Type | Used At Stage | Purpose |
|---|---|---|---|
| `Deal Stage` | Pipeline (default) | Opportunity onward | Demo Requested → Discovery → Proposal → Negotiation → Closed |
| `Amount` | Currency (default) | Opportunity | Expected deal value |
| `Close Date` | Date (default) | Opportunity | Expected close date |
| `Deal Source` | Dropdown (custom) | Opportunity | Inbound / Outbound / Referral / Partner |
| `ICP Tier` | Dropdown (custom) | Opportunity | A/B/C (mirrors contact tier) |
| `Closed Lost Reason` | Dropdown (custom) | Closed Lost | Timing / Budget / Competitor / No Need / Went Dark / Other |
| `Competitor` | Dropdown (custom) | Closed Lost | Which competitor they chose |
| `Expansion Type` | Dropdown (custom) | Expansion | Upsell / Cross-sell / Additional Seats |
| `Contract End Date` | Date (custom) | Customer | Renewal tracking |

### Company Properties

| Property | Type | Purpose |
|---|---|---|
| `Lifecycle Stage` | Dropdown (default) | Mirrors highest contact stage at company |
| `ICP Score` | Number (custom) | Company-level fit score |
| `Industry` | Dropdown (default) | Vertical |
| `Annual Revenue` | Number (default) | Revenue range |
| `Number of Employees` | Number (default) | Company size |
| `Tech Stack` | Multi-checkbox (custom) | Known technologies |
| `Target Account` | Checkbox (custom) | Is this a named/strategic account? |
| `Account Owner` | HubSpot user (default) | Assigned rep |

### Lifecycle Stage Sync Rules (HubSpot)

- **Contact → Company:** When a contact moves forward, the associated company automatically moves forward (if company is at an earlier stage).
- **Deal → Contact:** When a deal moves to "Closed Won," associated contacts move to "Customer."
- **Never regress automatically.** Lifecycle stages only move forward in HubSpot. Manual intervention required to recycle.

---

## Automation Workflows per Stage Transition

### Subscriber → Lead

**Trigger:** Contact engages beyond subscription (visits 2+ pages, clicks email link, downloads content)

```
→ Set Lifecycle Stage = Lead
→ Enrich via Clay/Clearbit (company data, tech stack)
→ Calculate ICP score
→ Set Lead Tier (A/B/C/D)
→ IF A or B tier: Enroll in "Warm Nurture" workflow
→ IF C or D tier: Stay in "Newsletter" workflow
```

### Lead → MQL

**Trigger:** HubSpot Score ≥ 50 OR form submission on high-intent page (demo, pricing, contact sales)

```
→ Set Lifecycle Stage = MQL
→ Set Lead Status = "New"
→ Assign to SDR (round-robin by territory/capacity)
→ Send Slack notification with contact details + ICP score
→ Create task: "Contact within [SLA time based on tier]"
→ Start SLA enforcement timer
```

### MQL → SAL

**Trigger:** Task completed "Discovery call booked" OR meeting booked via Calendly/HubSpot Meetings

```
→ Set Lifecycle Stage = SAL
→ Set Lead Status = "Connected"
→ Send prep email to AE/SDR with:
    - Company background
    - ICP score + tier
    - Signal(s) detected
    - Content the prospect engaged with
→ Log meeting in CRM
```

### SAL → SQL

**Trigger:** Meeting held + SDR marks as "Qualified" after BANT confirmed

```
→ Set Lifecycle Stage = SQL
→ Set Lead Status = "Qualified"
→ Transfer ownership to AE (if SDR-sourced)
→ Create deal in pipeline (Stage: "Discovery Complete")
→ Populate deal with: Amount estimate, close date, source, ICP tier
```

### SQL → Opportunity → Closed Won

**Trigger:** Deal stage progression

```
Demo Completed:
  → Update deal stage
  → Create task: "Send proposal within 48 hours"

Proposal Sent:
  → Update deal stage
  → Set required properties: Amount, Close Date, Decision Criteria
  → Create task: "Follow up in 3 business days"

Negotiation:
  → Update deal stage
  → Set required: Contract terms, Legal status
  → Send Slack alert to manager if deal value > $50K

Closed Won:
  → Set Lifecycle Stage = Customer (contact + company)
  → Create task for CS: "Begin onboarding within 48 hours"
  → Send internal Slack celebration
  → Trigger onboarding email sequence to customer

Closed Lost:
  → Required: Closed Lost Reason (dropdown)
  → Required: Competitor (if applicable)
  → Enroll in "Closed Lost Re-engagement" workflow (6-month timer)
```

---

## Customer Health Score Model

### Weighted Signal Framework

| Category | Weight | Signals | Scoring |
|---|---|---|---|
| **Product Usage** | 40% | DAU/MAU ratio, feature breadth, license utilization, session frequency | High usage = 100, Declining = 50, Minimal = 20 |
| **Support Health** | 20% | Ticket volume, severity, resolution time, reopen rate, CSAT on tickets | Few low-severity = 100, Frequent high-severity = 20 |
| **Relationship Quality** | 20% | Meeting frequency, executive sponsor engagement, QBR attendance, responsiveness | Active engagement = 100, Ghosting = 20 |
| **NPS / Sentiment** | 10% | NPS score, qualitative feedback, social mentions | Promoter (9-10) = 100, Passive (7-8) = 60, Detractor (0-6) = 20 |
| **Expansion Signals** | 10% | ARR growth, upsell conversations, new team adoption, feature requests | Growing = 100, Flat = 50, Contracting = 20 |

### Composite Score Calculation

```
Health Score = (Usage × 0.4) + (Support × 0.2) + (Relationship × 0.2) + (NPS × 0.1) + (Expansion × 0.1)
```

### Score Bands

| Score | Status | Color | Action |
|---|---|---|---|
| 80-100 | Healthy | Green | Maintain cadence, look for expansion opportunities |
| 60-79 | Okay | Yellow | Monitor closely, proactive check-in, address emerging issues |
| 40-59 | At Risk | Orange | Escalate to CS manager, create recovery plan, exec sponsor outreach |
| 0-39 | Critical | Red | Immediate escalation, executive intervention, save plan within 48 hours |

### Segment-Specific Weights

| Segment | Usage | Support | Relationship | NPS | Expansion |
|---|---|---|---|---|---|
| **Enterprise** | 30% | 15% | 30% | 15% | 10% |
| **Mid-Market** | 40% | 20% | 20% | 10% | 10% |
| **SMB** | 50% | 20% | 10% | 10% | 10% |

**Why:** Enterprise accounts depend more on relationship quality and executive engagement. SMB accounts are more product-driven — if they use it, they stay.

### Implementation Rules

1. **Use 6-10 KPIs max.** Overly complex models become unmaintainable.
2. **Validate against history.** Check if low scores actually predicted churn in the past.
3. **Every score must have a clear action.** If you can't act on a signal, don't include it.
4. **Update weekly.** Health scores are useless if stale.
5. **AI advantage:** AI-driven scoring detects issues **60-90 days** before renewal, compared to manual methods.

*Source: ColdIQ — compiled B2B benchmarks*

---

## Upsell / Cross-Sell Trigger Definitions

### The 7 Behavioral Expansion Triggers

These signals predict upsell readiness **2-6 weeks** before the customer realizes they need more:

| # | Trigger | Signal | Success Rate | Timing |
|---|---|---|---|---|
| 1 | **Team Growth** | Rapid increase in active users within account | 47% conversion | When new user count jumps 30%+ |
| 2 | **Usage Limit Hits** | Bumping against plan limits (seats, API calls, storage) | High | When usage hits 80%+ of plan limits |
| 3 | **Feature Adoption** | Using premium/advanced features on free/lower tier | High | When 3+ premium features used regularly |
| 4 | **Cross-Team Expansion** | New departments or regions start using the product | High | When new team/geo detected |
| 5 | **Renewal Window** | Contract 30-120 days from end | Medium | 90 days out = ideal expansion conversation |
| 6 | **Success Signals** | High NPS, case study participant, referral given | Medium | When NPS = 9-10 + strong usage |
| 7 | **Premium Feature Pilot** | Trialing higher-tier features in one team | High | When trial adoption exceeds 50% |

### Key Insight: Timing is Everything

- **Proactive, behavior-triggered expansion:** 35-45% conversion rate
- **Reactive expansion (customer asks):** 8-12% conversion rate
- **67% of failed upsells** are due to poor timing, not poor product fit

### Cross-Sell vs Upsell

| Type | Definition | Example | Best Trigger |
|---|---|---|---|
| **Upsell** | Move to a higher tier/plan | Basic → Pro | Usage limits, feature adoption |
| **Cross-sell** | Add a complementary product | CRM + Marketing Hub | Cross-team expansion, new use case |
| **Expansion** | Add seats/licenses | 10 seats → 25 seats | Team growth signal |

### Expansion Revenue Impact

- Successful SaaS companies generate **70-80% of revenue growth from existing customers**
- Net Revenue Retention target: **120%+**
- Expanding accounts is **5-25x more cost-effective** than new acquisition

### Automation

```
IF Usage ≥ 80% of plan limit:
  → Slack alert to CS owner
  → Auto-send "You're growing!" email with upgrade options
  → Create expansion deal in CRM

IF NPS = 9-10 AND usage is growing:
  → Flag as expansion candidate
  → CS schedules "growth conversation" in next check-in

IF new team/department detected:
  → Slack alert to CS + AE
  → Create cross-sell opportunity in CRM
  → Send relevant case study for that department's use case
```

*Source: ColdIQ*

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
