# Pipeline Reporting — Framework

Metrics, benchmarks, monitoring cadences, and reporting structures for outbound and inbound pipeline.

---

## Outbound Performance Benchmarks

### Email Metrics

| Metric | Healthy | Warning | Stop & Investigate |
|---|---|---|---|
| Open rate | 50%+ | 30–50% | Below 30% |
| Reply rate | 2%+ | 1–2% | Below 1% |
| Bounce rate | Below 3% | 3–5% | Above 5% |
| Spam complaints | 0 | Any | Multiple |
| Spam rate | <0.1% | 0.1–0.3% | >0.3% |
| Deliverability score | >95% | 90–95% | <90% |

### Reply Rates by Approach

| Approach | Expected Reply Rate |
|---|---|
| Cold prospects (no signal) | 6–8% |
| Signal-based outreach | 18–22% |
| Multi-signal stacked | 35–40% |
| Website visitors | 25–30% |

### Campaign Performance Signals

| Signal | What It Means | Action |
|---|---|---|
| Open rate dropping | Deliverability issue or bad subject lines | Check DNS, test new subject lines |
| Reply rate dropping | Copy or targeting problem | Review messaging, check ICP fit |
| Bounce rate spiking | Bad list quality or DNS issue | Pause, clean list, verify DNS |
| Positive reply rate high | Copy and targeting working | Scale volume, clone approach |
| Negative reply rate high | Wrong audience or bad messaging | Revisit ICP, rewrite copy |

---

## Monitoring Cadences

### Daily (5 minutes)

- [ ] Bounce rates <5%
- [ ] Reply rates consistent
- [ ] No spam complaint notifications
- [ ] No blacklist alerts
- [ ] Spot-check 2–3 warm-up emails

### Weekly (15 minutes)

- [ ] Google Postmaster Tools check
- [ ] Microsoft SNDS scores
- [ ] MXToolbox blacklist status
- [ ] Week-over-week open/reply rate comparison
- [ ] Bounce rate trending
- [ ] Campaign-level performance review

### Monthly (30 minutes)

- [ ] Update suppression list
- [ ] Audit bounce patterns
- [ ] Review domain reputation trends
- [ ] Clean old unresponsive leads
- [ ] Rotate warm-up email content
- [ ] Review infrastructure costs
- [ ] Source performance comparison (which data source gives best results?)

### Quarterly (1 hour)

- [ ] Full DNS audit across all domains
- [ ] Sender reputation deep dive
- [ ] Warm-up service effectiveness review
- [ ] Strategic capacity planning
- [ ] ICP refinement based on conversion data
- [ ] Document lessons learned

---

## Seasonal Expectations

Don't panic during normal seasonal dips. Investigate only if drops exceed these norms.

| Period | Normal Engagement Drop | Expected Recovery |
|---|---|---|
| December holidays | 20–30% | Mid-January |
| July–August (vacation) | 10–20% | September |
| End of quarter | 10–15% | First 2 weeks of new quarter |
| Industry conferences | 15–25% | 1 week post-event |

---

## Scaling Metrics

| Metric | Guideline |
|---|---|
| Volume increase | Max 20% per week |
| New domain launches | 1 per week max, full warm-up cycle each |
| Mailbox send limits (Google) | 15–25/day per mailbox |
| Mailbox send limits (Microsoft) | 10–15/day per mailbox |
| Infrastructure capacity | Scale by adding mailboxes, not pushing limits |

---

## Investigation Framework

When something goes wrong, ask:

1. **What changed?** (list, copy, volume, timing)
2. **When did it start?** (pinpoint date/time)
3. **Which domains affected?** (all or specific)
4. **What do metrics show?** (bounce, spam, open rates)
5. **External factors?** (holidays, news, industry events)

### Default Recovery Process

```
Day 1:  Pause affected campaigns
Day 2:  Fix the identified issue
Day 3–5: Resume at 50% volume
Day 6–8: Monitor, increase to 75%
Day 9–11: Monitor, increase to 100%
Day 12+: Full volume with continued monitoring
```

---

## Full Pipeline Metrics

### Pipeline Velocity Formula

```
Pipeline Velocity = (# of Opportunities × Win Rate × Average Deal Size) ÷ Sales Cycle Length (days)
```

**B2B SaaS benchmark:** ~$1,847/day (ranges $743–$2,456 depending on industry)

**Why it matters:** Single metric that captures volume, quality, deal size, AND speed. Track weekly — organizations with weekly velocity tracking achieve **34% revenue growth** vs 11% for ad-hoc tracking.

*Source: ColdIQ — compiled B2B benchmarks*

---

## Win Rate Benchmarks by Segment

| Segment | ACV Range | Win Rate | Notes |
|---|---|---|---|
| **SMB** | <$10K | 28–35% | Shorter cycles, faster decisions |
| **Mid-Market** | $10K–$50K | 20–28% | Buying committees appear |
| **Upper Mid-Market** | $50K–$100K | 15–22% | More stakeholders, longer eval |
| **Enterprise** | >$100K | 12–18% | Complex procurement, long cycles |

**Overall typical:** 20–30%
**Median deal size (private SaaS):** $26,265

*Source: ColdIQ — compiled B2B benchmarks*

---

## Sales Cycle Length

| Segment | Average Cycle | Optimal Range |
|---|---|---|
| **SMB** | 14–30 days | 14–21 days |
| **Mid-Market** | 30–60 days | 30–45 days |
| **Enterprise** | 90–180+ days | 90–120 days |
| **All B2B SaaS median** | 84 days | 46–75 days |

**Trend:** Cycles lengthened **22% since 2022** due to expanded buying committees and increased due diligence.

---

## Funnel Conversion Rates by Stage

### Overall Benchmarks

| Stage Transition | Benchmark Rate | Key Bottleneck |
|---|---|---|
| **Lead → MQL** | 5–15% | Most leads don't meet qualification criteria |
| **MQL → SQL** | 13–21% (B2B median) | **Biggest bottleneck in most funnels** |
| **SQL → Opportunity** | 50–70% | If qualification is tight, most SQLs should convert |
| **Opportunity → Closed Won** | 20–30% | Depends on segment/ACV |
| **Lead → Customer (end-to-end)** | 2–5% | Healthy if other stages are within range |

### MQL → SQL by Lead Source

| Lead Source | MQL → SQL Rate | Cost Efficiency |
|---|---|---|
| **SEO** | 51% | Best ROI, high intent |
| **Email Marketing** | 46% | High conversion, needs nurture to close |
| **Webinars** | 30% | Good intent, medium cost |
| **PPC** | 26% | Recovers with strong close rates |
| **Events** | 24% | Expensive, long nurture needed |

*Source: ColdIQ — compiled B2B benchmarks*

---

## Attribution Reporting

### Models to Run in Parallel

| Model | Credits | Best For | Use Case |
|---|---|---|---|
| **First-touch** | First interaction | Top-of-funnel channel effectiveness | "Which channels fill the funnel?" |
| **Last-touch** | Final action before conversion | Close attribution | "What closes deals?" |
| **Multi-touch** | Weighted across all touches | Full journey picture | "What's the real buyer journey?" |

### Pipeline Definitions

| Metric | Definition | Use |
|---|---|---|
| **Marketing-Sourced Pipeline (MSP)** | Opportunities whose first touch came from marketing | More accountable, direct attribution |
| **Marketing-Influenced Pipeline (MIP)** | Opportunities that engaged with marketing at any stage | Broader picture, shows marketing's full impact |

**Recommendation:** Track both. Report MSP for accountability. Report MIP for budget justification.

---

## Pipeline Coverage Ratio

**Formula:** Total Pipeline Value ÷ Quota Target

| Coverage Ratio | Meaning | Action |
|---|---|---|
| **4x+** | Healthy pipeline | Maintain, focus on close rates |
| **3x** | Adequate | Monitor, increase if win rates are low |
| **2x** | At risk | Urgently increase pipeline generation |
| **<2x** | Critical | All-hands pipeline generation, escalate |

**Rule of thumb:** If your win rate is 25%, you need **4x coverage** to hit quota. Adjust based on your actual win rate:

```
Required Coverage = 1 ÷ Win Rate
```

---

## Revenue Forecasting Model

### Simple Forecast

```
Forecasted Revenue = Open Pipeline × Historical Win Rate × Stage-Weighted Probability
```

### Stage-Weighted Probabilities

| Stage | Probability |
|---|---|
| SQL | 10% |
| Opportunity Created | 20% |
| Demo Completed | 30% |
| Proposal Sent | 50% |
| Negotiation | 70% |
| Verbal Commit | 90% |

### Forecasting Best Practices

- Only **20% of sales teams forecast with >75% accuracy**
- Marketing-sourced pipeline is the most volatile variable
- Friction points: MQL→SQL handoff, varying lead quality, complex B2B buying cycles
- Use AI-powered forecasting (HubSpot, Salesforce Einstein, Trellus) to reduce human bias
- Conduct structured quarterly RevOps reviews

---

## Rep-Level Performance Metrics

| Metric | What It Measures | Benchmark |
|---|---|---|
| **Activity volume** | Emails, calls, LinkedIn touches per day | 50–80 activities/day |
| **Meeting book rate** | Meetings booked per 100 leads worked | 5–15% |
| **SQL conversion** | % of meetings that become qualified | 40–60% |
| **Pipeline generated** | $ value of pipeline created per month | Varies by quota |
| **Win rate** | % of opportunities closed-won | 20–30% |
| **Quota attainment** | Revenue closed vs quota | 80%+ is healthy |
| **Average deal size** | Revenue per closed deal | Depends on segment |
| **Sales cycle length** | Days from opportunity to close | Compare to segment benchmarks |

---

## Cost Metrics by Channel

| Metric | Formula | What "Good" Looks Like |
|---|---|---|
| **Cost per Lead (CPL)** | Total channel spend ÷ Leads generated | Varies wildly by channel — compare within channel |
| **Cost per Meeting** | Total spend ÷ Meetings booked | $200–$500 for outbound, $100–$300 for inbound |
| **Cost per Opportunity** | Total spend ÷ Opportunities created | < 10% of average deal size |
| **Cost per Acquisition (CPA)** | Total spend ÷ Customers acquired | < 30% of first-year ACV |
| **CAC Payback Period** | CAC ÷ Monthly recurring revenue per customer | < 12 months for SMB, < 18 for Mid-Market |

---

## Dashboard Template (What to Build)

### Executive Dashboard (weekly)
- Total pipeline value
- Pipeline coverage ratio
- Pipeline velocity ($/ day)
- Win rate (trailing 30/60/90 days)
- Revenue forecast vs target
- New pipeline added this week

### Marketing Dashboard (weekly)
- Leads generated by source
- MQL → SQL conversion rate
- Marketing-sourced pipeline (MSP)
- Marketing-influenced pipeline (MIP)
- Cost per lead by channel
- Campaign ROI

### Sales Dashboard (daily/weekly)
- Open opportunities by stage
- Aging deals (stuck in stage too long)
- Rep activity metrics
- Meetings booked vs target
- Pipeline generated per rep
- Close rate per rep

### Outbound Dashboard (daily)
- Email volume sent
- Open rate, reply rate, bounce rate
- Positive vs negative reply split
- Meetings booked from outbound
- Domain health scores
- Campaign-level performance

---

## Outbound vs Inbound Pipeline Split Benchmarks

### 2025 B2B SaaS Pipeline Source Breakdown

| Source | % of Pipeline | % of Revenue | Conversion Efficiency |
|---|---|---|---|
| **Outbound sales** | 42% | 28% | Lower — volume play, needs more pipeline to close |
| **Organic inbound** | 31% | 29% | High — intent-driven, converts efficiently |
| **Paid ads** | 13% | 8% | Medium — good for awareness, variable close rates |
| **Partner referrals** | 10% | 31% | Best — highest revenue quality from smallest pipeline |
| **Events** | 4% | 4% | Low — relationship play, long cycle |

*Source: ColdIQ — compiled B2B benchmarks*

### Key Insights

- **Outbound dominates pipeline generation (42%)** but has the lowest pipeline-to-revenue efficiency.
- **Partner referrals are gold** — 10% of pipeline → 31% of revenue. Invest in partner programs.
- **Organic inbound is the most efficient channel** — nearly 1:1 pipeline-to-revenue ratio.
- **Healthy companies diversify.** Don't depend on one channel for >50% of pipeline.

### What This Means for Reporting

Report pipeline AND revenue by source separately. A channel that generates tons of pipeline but little revenue is a false signal. Track:
- Pipeline generated by source
- Revenue closed by source
- Pipeline-to-revenue conversion rate by source
- Cost per closed deal by source

---

## Cohort Analysis Framework

### What Is Pipeline Cohort Analysis?

Group leads/deals by their **acquisition month** (or quarter) and track how each cohort progresses through the funnel over time. This reveals:
- How long it actually takes leads to convert (not just average cycle time)
- Which acquisition months produce the best customers
- Whether your funnel is getting better or worse over time
- Realistic forecasting based on historical cohort behavior

### How to Build a Cohort Table

**Rows:** Acquisition month (when the lead entered the funnel)
**Columns:** Months since acquisition (Month 0, Month 1, Month 2... Month 12)
**Values:** Conversion rate at each stage

**Example:**

| Cohort | Month 0 (Leads) | Month 1 (MQL) | Month 2 (SQL) | Month 3 (Opp) | Month 6 (Won) | Month 12 (Won) |
|---|---|---|---|---|---|---|
| Jan 2025 | 500 | 75 (15%) | 12 (2.4%) | 8 (1.6%) | 15 (3%) | 20 (4%) |
| Feb 2025 | 600 | 90 (15%) | 18 (3%) | 10 (1.7%) | 18 (3%) | — |
| Mar 2025 | 450 | 80 (18%) | 15 (3.3%) | 12 (2.7%) | — | — |

### What to Look For

| Pattern | What It Means | Action |
|---|---|---|
| Later cohorts convert faster | Funnel is improving (better targeting, better process) | Document what changed, double down |
| Later cohorts convert slower | Something broke (list quality, messaging, market shift) | Investigate by channel, check ICP fit |
| Long tail of conversions (Month 6-12) | Deals close slowly, nurture matters | Invest more in nurture sequences |
| Flat after Month 3 | Leads that don't convert in 3 months rarely do | Focus resources on early engagement |

### Cohort Segmentation Options

Don't just cohort by month. Segment by:

| Dimension | Why |
|---|---|
| **Lead source** | Do outbound cohorts convert differently than inbound? |
| **ICP tier** | Do A-tier leads close faster? (They should.) |
| **Industry vertical** | Some verticals have longer cycles |
| **Product/service** | Different products may have different funnels |
| **Sales rep** | Identifies coaching opportunities |
| **New logo vs expansion** | Track separately — expansion should be faster and higher win rate |

*Source: ColdIQ — compiled B2B benchmarks*

---

## Client Reporting Template (Agency Use)

### Monthly Report Structure

#### Page 1: Executive Summary

```
┌─────────────────────────────────────────┐
│  EXECUTIVE SUMMARY — [Month] [Year]     │
├─────────────────────────────────────────┤
│  Key Wins:                               │
│  • [Top 3 wins this month]              │
│                                          │
│  Key Metrics:                            │
│  • Contacts reached: [X]                │
│  • Meetings booked: [X]                 │
│  • Pipeline generated: $[X]             │
│  • Deals closed: [X] ($[X])            │
│                                          │
│  Month-over-Month:                       │
│  • Meetings: +/-X%                       │
│  • Pipeline: +/-X%                       │
│                                          │
│  Focus for Next Month: [1-2 priorities] │
└─────────────────────────────────────────┘
```

#### Page 2: Outbound Performance

| Metric | This Month | Last Month | Trend | Benchmark |
|---|---|---|---|---|
| Emails sent | | | | |
| Open rate | | | | 50%+ |
| Reply rate | | | | 2%+ |
| Positive reply rate | | | | 50%+ of replies |
| Bounce rate | | | | <3% |
| Meetings booked | | | | |
| Cost per meeting | | | | $200-500 |

#### Page 3: Pipeline Overview

| Stage | # Deals | Total Value | Avg Age (days) | Conversion from Prior |
|---|---|---|---|---|
| MQL | | | | |
| SQL | | | | MQL → SQL: % |
| Opportunity | | | | SQL → Opp: % |
| Proposal | | | | |
| Negotiation | | | | |
| Closed Won | | | | Win rate: % |
| Closed Lost | | | | Top reason: |

#### Page 4: Channel Performance

| Channel | Leads | MQLs | SQLs | Pipeline $ | Revenue $ | CPL | CPA |
|---|---|---|---|---|---|---|---|
| Outbound (email) | | | | | | | |
| Outbound (LinkedIn) | | | | | | | |
| Inbound (organic) | | | | | | | |
| Inbound (paid) | | | | | | | |
| Referral | | | | | | | |

#### Page 5: Recommendations & Next Steps

```
1. What's working → Scale it
2. What's not working → Why + fix plan
3. Tests to run next month
4. ICP/targeting adjustments
5. Copy/messaging changes
6. Infrastructure changes needed
```

### Reporting Cadence

| Report | Frequency | Audience | Focus |
|---|---|---|---|
| **Pulse check** | Weekly (async, Slack/email) | Client POC | Volume, replies, meetings, any flags |
| **Monthly report** | Monthly (deck + call) | Client POC + leadership | Full performance, pipeline, ROI |
| **Quarterly review** | Quarterly (call) | Client executive team | Strategy, ICP refinement, scaling plan |

### What NOT to Include in Client Reports

- Raw email copy (unless they ask)
- Internal process details
- Vanity metrics without context (e.g., "we sent 10,000 emails!" without conversion data)
- Excuses without solutions

---

## HubSpot Dashboard Build Guide

### Dashboard 1: Executive Pipeline Dashboard

**Widgets to include:**

| Widget | Type | Data |
|---|---|---|
| Total pipeline value | Single number | Sum of all open deal amounts |
| Pipeline coverage ratio | Single number | Open pipeline ÷ quarterly quota |
| Pipeline velocity | Single number | (Deals × Win Rate × ACV) ÷ Avg Cycle |
| Win rate (30/60/90 day) | Line chart | Closed Won ÷ (Closed Won + Closed Lost) |
| Revenue closed vs target | Bar chart | Monthly closed revenue vs quota |
| Pipeline by stage | Funnel chart | Deal count and value per stage |
| Pipeline by source | Pie chart | Inbound vs Outbound vs Referral vs Partner |
| Aging deals | Table | Deals in stage > 2x average time |

### Dashboard 2: Marketing Performance

**Widgets to include:**

| Widget | Type | Data |
|---|---|---|
| MQLs generated (this month) | Single number | New MQLs created |
| MQL → SQL conversion rate | Single number | SQLs ÷ MQLs (trailing 90 days) |
| Marketing-sourced pipeline | Single number | Pipeline from marketing-first-touch |
| Leads by source | Bar chart | Organic, Paid, Social, Referral, Direct |
| Campaign performance | Table | Top campaigns by pipeline generated |
| Cost per MQL by channel | Bar chart | Spend ÷ MQLs per channel |
| Content engagement | Table | Top pages/assets by conversion rate |

### Dashboard 3: Sales Activity

**Widgets to include:**

| Widget | Type | Data |
|---|---|---|
| Meetings booked (this week) | Single number | New meetings scheduled |
| Rep leaderboard | Table | Meetings, pipeline, closed per rep |
| SLA compliance | Percentage | % of leads contacted within SLA |
| Deal stage duration | Bar chart | Average days in each stage |
| Activity volume | Table | Calls, emails, tasks per rep |
| Stalled deals | Table | Deals with no activity in 14+ days |
| Forecast vs actual | Bar chart | Committed vs closed revenue |

### Build Steps in HubSpot

1. **Reports** → Create custom report → Single object or cross-object
2. **Choose data source:** Contacts, Deals, or Companies (or cross-object)
3. **Add filters:** Date range, pipeline, deal stage, source, owner
4. **Select visualization:** Chart type matches the insight you want
5. **Add to dashboard:** Drag reports onto dashboard
6. **Set permissions:** Share with team, set as default for specific roles
7. **Schedule emails:** Auto-send dashboard summary weekly to stakeholders

*Source: ColdIQ*

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
