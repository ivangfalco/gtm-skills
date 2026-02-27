# ABM Measurement — Dashboards

Dashboard templates for ABM reporting: executive, marketing ops, and tactical views with HubSpot configurations.

---

## Dashboard Hierarchy

ABM programs need three levels of dashboards, each serving different stakeholders and cadences.

| Dashboard Level | Audience | Refresh Cadence | Primary Purpose |
|---|---|---|---|
| **Executive** | C-suite, VP Marketing, VP Sales | Quarterly (monthly updates) | ROI justification, strategic decisions |
| **Marketing Ops** | Marketing Director, ABM Manager | Monthly (weekly checks) | Program health, optimization decisions |
| **Tactical** | ABM Specialist, BDRs, Campaign Manager | Weekly (daily for hot accounts) | Day-to-day execution, account alerts |

---

## Executive Dashboard

### Purpose
Answer: "Is ABM working? Should we invest more?"

### Refresh Cadence
Quarterly deep dive, monthly status updates

### Key Components

#### 1. ABM ROI Summary

| Metric | This Quarter | Last Quarter | YoY | Target |
|---|---|---|---|---|
| Total ABM Spend | $_____ | $_____ | ___% | $_____ |
| Pipeline Generated | $_____ | $_____ | ___% | $_____ |
| Pipeline per $ Spent | $_____ | $_____ | ___% | $10+ |
| Closed-Won Revenue | $_____ | $_____ | ___% | $_____ |
| ROAS | ___x | ___x | ___% | 2x+ |

#### 2. ABM vs. Demand Gen Comparison

| Metric | ABM | Demand Gen | Difference |
|---|---|---|---|
| Win Rate | ___% | ___% | +___% |
| Avg Deal Size | $_____ | $_____ | +___% |
| Sales Cycle (days) | _____ | _____ | -___% |
| Cost per Opportunity | $_____ | $_____ | -___% |
| Pipeline per $ | $_____ | $_____ | +___% |

#### 3. Account Funnel Summary

```
Target Accounts:     [████████████████████] 3,400
├─ Reached:          [███████████████     ] 2,890 (85%)
├─ Aware (50+ imp):  [██████████          ] 1,875 (55%)
├─ Engaged (5+ clk): [████                ]   600 (32% of Aware)
├─ Pipeline:         [██                  ]   108 (18% of Engaged)
└─ Closed-Won:       [█                   ]    27 (25% of Pipeline)
```

#### 4. Quarterly Trend

| Quarter | Spend | Pipeline | ROAS | Accounts Closed |
|---|---|---|---|---|
| Q1 | $_____ | $_____ | ___x | _____ |
| Q2 | $_____ | $_____ | ___x | _____ |
| Q3 | $_____ | $_____ | ___x | _____ |
| Q4 | $_____ | $_____ | ___x | _____ |

### Executive Dashboard: What NOT to Include

| Avoid | Why |
|---|---|
| Click-through rates | Too granular, not meaningful at exec level |
| Impression counts | Vanity metric without context |
| Individual campaign performance | Save for marketing ops dashboard |
| Daily/weekly fluctuations | Noise, not signal |

---

## Marketing Ops Dashboard

### Purpose
Answer: "Is the program healthy? What needs optimization?"

### Refresh Cadence
Monthly deep analysis, weekly status checks

### Key Components

#### 1. Stage Progression Tracker

| Stage | Current Count | Last Month | MoM Change | Conversion Rate | Benchmark |
|---|---|---|---|---|---|
| Identified | _____ | _____ | ___% | — | — |
| Aware | _____ | _____ | ___% | ___% | 55% |
| Engaged | _____ | _____ | ___% | ___% | 32% |
| Pipeline | _____ | _____ | ___% | ___% | 18% |
| Closed-Won | _____ | _____ | ___% | ___% | 25%+ |

**Health indicator:** If any conversion rate is 10+ points below benchmark, flag for investigation.

#### 2. Channel Performance

| Channel | Spend | Accounts Reached | Engaged | Pipeline Influenced | Cost/Engaged |
|---|---|---|---|---|---|
| LinkedIn Ads | $_____ | _____ | _____ | $_____ | $_____ |
| Display | $_____ | _____ | _____ | $_____ | $_____ |
| Email | $_____ | _____ | _____ | $_____ | $_____ |
| Direct Mail | $_____ | _____ | _____ | $_____ | $_____ |
| Events | $_____ | _____ | _____ | $_____ | $_____ |

#### 3. Campaign Group Performance

| Campaign Group | Budget | Spend | Accounts | Engaged | CTR | Pipeline | Efficiency |
|---|---|---|---|---|---|---|---|
| ICP Tier A | $_____ | $_____ | _____ | _____ | ___% | $_____ | $_____ |
| ICP Tier B | $_____ | $_____ | _____ | _____ | ___% | $_____ | $_____ |
| Vertical: SaaS | $_____ | $_____ | _____ | _____ | ___% | $_____ | $_____ |
| Vertical: FinTech | $_____ | $_____ | _____ | _____ | ___% | $_____ | $_____ |

#### 4. Persona Engagement Breakdown

| Persona | Impressions | Clicks | CTR | Engaged Accounts | Pipeline Attributed |
|---|---|---|---|---|---|
| Product | _____ | _____ | ___% | _____ | $_____ |
| Engineering | _____ | _____ | ___% | _____ | $_____ |
| Executive | _____ | _____ | ___% | _____ | $_____ |
| Marketing | _____ | _____ | ___% | _____ | $_____ |

#### 5. Content/Creative Performance

| Content Theme | Format | ABM Stage | Impressions | CTR | Engagement Rate | Winner? |
|---|---|---|---|---|---|---|
| Pain Callout | Single Image | Awareness | _____ | ___% | ___% | |
| Customer Proof | Video | Awareness | _____ | ___% | ___% | |
| Product Demo | Carousel | Interested | _____ | ___% | ___% | |
| ROI Calculator | TLA | Considering | _____ | ___% | ___% | |

#### 6. Account Velocity Report

| Cohort (Entry Month) | Avg Days to Aware | Avg Days to Engaged | Avg Days to Pipeline | Total in Pipeline |
|---|---|---|---|---|
| January | _____ | _____ | _____ | _____ |
| February | _____ | _____ | _____ | _____ |
| March | _____ | _____ | _____ | _____ |

#### 7. Budget Pacing

| Item | Monthly Budget | MTD Spend | Projected | Variance |
|---|---|---|---|---|
| LinkedIn Ads | $_____ | $_____ | $_____ | ___% |
| ZenABM/Tools | $_____ | $_____ | $_____ | ___% |
| Creative Production | $_____ | $_____ | $_____ | ___% |
| **Total** | $_____ | $_____ | $_____ | ___% |

---

## Tactical Dashboard

### Purpose
Answer: "Which accounts need attention today? What's working this week?"

### Refresh Cadence
Weekly review, daily hot account alerts

### Key Components

#### 1. Hot Accounts Alert

Accounts that crossed engagement thresholds in the last 7 days:

| Account | Stage Change | Engagement This Week | Top Persona | Last Touch | BDR Assigned |
|---|---|---|---|---|---|
| Acme Corp | Aware → Engaged | 12 clicks, 45 engagements | Product | 2 days ago | Sarah |
| TechCo Inc | Engaged → Pipeline | Demo booked | Executive | Today | Mike |
| SaaS Solutions | New engagement spike | 8 clicks (from 0) | Marketing | 3 days ago | Unassigned |

**Action:** BDR should reach out within 24-48 hours of stage change.

#### 2. Weekly Activity Summary

| Metric | This Week | Last Week | Change | 4-Week Avg |
|---|---|---|---|---|
| New accounts reached | _____ | _____ | ___% | _____ |
| Accounts moved to Aware | _____ | _____ | ___% | _____ |
| Accounts moved to Engaged | _____ | _____ | ___% | _____ |
| BDR outreach sent | _____ | _____ | ___% | _____ |
| Meetings booked | _____ | _____ | ___% | _____ |

#### 3. Campaign Health Check

| Campaign | Status | Daily Spend | Frequency | Issues |
|---|---|---|---|---|
| Q1-ABM-Awareness-TierA | Active | $_____ | ___x | None |
| Q1-ABM-Interested-TierA | Active | $_____ | ___x | Low CTR |
| Q1-ABM-Awareness-TierB | Limited | $_____ | ___x | Budget depleted |
| Q1-ABM-Product-Demo | Paused | $0 | — | Refresh needed |

#### 4. Account Stage Distribution

| Stage | Count | % of Total | Change (7d) |
|---|---|---|---|
| Identified | _____ | ___% | +_____ |
| Aware | _____ | ___% | +_____ |
| Engaged | _____ | ___% | +_____ |
| Pipeline | _____ | ___% | +_____ |
| Closed-Won | _____ | ___% | +_____ |
| Closed-Lost | _____ | ___% | +_____ |

#### 5. BDR Activity Tracker

| BDR | Assigned Accounts | Outreach Sent | Replies | Meetings | Conversion |
|---|---|---|---|---|---|
| Sarah | _____ | _____ | _____ | _____ | ___% |
| Mike | _____ | _____ | _____ | _____ | ___% |
| Alex | _____ | _____ | _____ | _____ | ___% |
| **Team** | _____ | _____ | _____ | _____ | ___% |

#### 6. Creative Fatigue Monitor

| Ad | Days Running | Impressions | CTR (7d) | CTR (30d) | Status |
|---|---|---|---|---|---|
| Pain-Callout-v1 | 45 | 125,000 | 0.32% | 0.48% | Fatigued |
| Customer-Proof-Alex | 30 | 89,000 | 0.55% | 0.52% | Healthy |
| Product-Demo-v2 | 14 | 34,000 | 0.61% | 0.58% | Healthy |

**Fatigue signal:** CTR drop >20% from 30-day average

---

## HubSpot Dashboard Configuration

### Required Custom Properties (Company Level)

Create these properties in HubSpot Settings > Properties > Company:

| Property Name | Internal Name | Type | Options/Notes |
|---|---|---|---|
| ABM Campaign Name | `abm_campaign_name` | Dropdown | Your campaign names |
| ABM Stage | `abm_stage` | Dropdown | Identified, Aware, Engaged, Pipeline, Closed-Won, Closed-Lost |
| ABM Stage Date | `abm_stage_date` | Date | Auto-updated by workflow |
| ICP Score | `icp_score` | Number | 0-100 |
| ICP Tier | `icp_tier` | Dropdown | A, B, C, D |
| LinkedIn Impressions (30d) | `li_impressions_30d` | Number | From ZenABM/Fibbler |
| LinkedIn Clicks (30d) | `li_clicks_30d` | Number | From ZenABM/Fibbler |
| LinkedIn Engagements (30d) | `li_engagements_30d` | Number | From ZenABM/Fibbler |
| ABM BDR Owner | `abm_bdr_owner` | HubSpot user | Assignment |
| Last ABM Touch Date | `last_abm_touch_date` | Date | Auto-updated |
| ABM Intent Signals | `abm_intent_signals` | Multi-checkbox | From campaign engagement |

### HubSpot Report Builder: Key Reports

#### Report 1: Account Stage Funnel

**Type:** Funnel report (Company-based)
**Stages:**
1. ABM Stage = Identified
2. ABM Stage = Aware
3. ABM Stage = Engaged
4. ABM Stage = Pipeline
5. ABM Stage = Closed-Won

**Filter:** ABM Campaign Name is any of [your campaigns]

#### Report 2: Stage Conversion Over Time

**Type:** Line chart
**X-axis:** ABM Stage Date (by week)
**Y-axis:** Count of Companies
**Breakdown:** ABM Stage
**Filter:** ABM Campaign Name is any of [your campaigns]

#### Report 3: Pipeline Influenced by ABM

**Type:** Single value + trend
**Metric:** Sum of Deal Amount
**Filter:**
- Associated Company ABM Stage is any of [Engaged, Pipeline, Closed-Won]
- Deal Stage is not Closed-Lost

#### Report 4: Account Engagement Distribution

**Type:** Histogram
**X-axis:** LinkedIn Engagements (30d) - bucketed
**Y-axis:** Count of Companies
**Buckets:** 0, 1-5, 6-10, 11-20, 21-50, 51+

#### Report 5: Stage Velocity

**Type:** Table
**Rows:** ABM Campaign Name
**Columns:**
- Avg days Identified to Aware
- Avg days Aware to Engaged
- Avg days Engaged to Pipeline

*Note: Requires custom calculated properties for days-in-stage*

### HubSpot Workflow: Stage Progression Automation

**Workflow 1: Update ABM Stage Based on Engagement**

```
Trigger: Company property "LinkedIn Clicks (30d)" is updated

Branch 1:
IF LinkedIn Clicks (30d) >= 5 AND ABM Stage = "Aware"
THEN:
  - Set ABM Stage = "Engaged"
  - Set ABM Stage Date = Today
  - Send internal notification to ABM BDR Owner

Branch 2:
IF LinkedIn Impressions (30d) >= 50 AND ABM Stage = "Identified"
THEN:
  - Set ABM Stage = "Aware"
  - Set ABM Stage Date = Today
```

**Workflow 2: Hot Account Alert**

```
Trigger: Company property "LinkedIn Clicks (30d)" is updated

Enrollment criteria:
- LinkedIn Clicks (30d) increased by 5+ in 7 days
- ABM Stage is any of [Aware, Engaged]

Actions:
- Send Slack notification to #abm-hot-accounts
- Create task for ABM BDR Owner: "Hot account - review engagement"
- Add to list "Hot Accounts - This Week"
```

**Workflow 3: Pipeline Stage Update**

```
Trigger: Deal Stage is updated to any pipeline stage

Enrollment criteria:
- Associated Company ABM Stage is any of [Identified, Aware, Engaged]

Actions:
- Set Associated Company ABM Stage = "Pipeline"
- Set ABM Stage Date = Today
- Send notification to Marketing
```

### HubSpot Dashboard Assembly

**Executive Dashboard (HubSpot)**

| Widget | Type | Position |
|---|---|---|
| Total Pipeline Influenced | Single value | Top left |
| ABM ROI (Pipeline/Spend) | Single value | Top center |
| Closed-Won from ABM | Single value | Top right |
| Account Funnel | Funnel chart | Middle, full width |
| Quarterly Trend | Line chart | Bottom left |
| ABM vs Non-ABM Win Rate | Bar comparison | Bottom right |

**Marketing Ops Dashboard (HubSpot)**

| Widget | Type | Position |
|---|---|---|
| Stage Distribution | Pie chart | Top left |
| Stage Conversion Rates | Table | Top right |
| Weekly Stage Movement | Line chart | Middle left |
| Campaign Performance Table | Table | Middle right |
| Persona Engagement | Bar chart | Bottom left |
| Budget Pacing | Progress bars | Bottom right |

**Tactical Dashboard (HubSpot)**

| Widget | Type | Position |
|---|---|---|
| Hot Accounts (7d) | Table (filtered list) | Top, full width |
| This Week vs Last Week | Comparison metrics | Middle left |
| BDR Activity Summary | Table | Middle right |
| Account Stage Counts | Number widgets | Bottom row |

---

## Dashboard Integration with LinkedIn Campaign Manager

### Data Flow

```
LinkedIn Campaign Manager
    ↓
    [Ad metrics: impressions, clicks, engagements]
    ↓
ZenABM / Fibbler (connector)
    ↓
    [Account-level aggregation]
    ↓
HubSpot (CRM)
    ↓
    [Stage updates, pipeline data]
    ↓
Dashboard Reports
```

### What Each System Contributes

| System | Data Contributed | Update Frequency |
|---|---|---|
| LinkedIn Campaign Manager | Raw ad metrics, campaign performance | Real-time |
| ZenABM/Fibbler | Account-level engagement rollup | Daily |
| HubSpot | Stage progression, pipeline, revenue | Real-time |
| Manual (spreadsheet) | Spend data, ROI calculations | Weekly |

### Sync Schedule Recommendation

| Data Type | Sync Frequency | Tool |
|---|---|---|
| Engagement data (LinkedIn → CRM) | Daily | ZenABM/Fibbler |
| Account stage updates | Real-time (workflow) | HubSpot |
| Pipeline data | Real-time | HubSpot |
| Spend data | Weekly (manual or API) | Spreadsheet/HubSpot |
| Executive metrics | Monthly | Manual calculation |

---

## Dashboard Templates: Quick Start

### Minimum Viable Dashboard (Week 1)

If you're just starting, track only these:

| Metric | How to Track |
|---|---|
| Accounts in campaign | HubSpot list count |
| Accounts with 50+ impressions | HubSpot filtered list |
| Accounts with 5+ clicks | HubSpot filtered list |
| Pipeline from ABM accounts | HubSpot deal report |
| Weekly spend | LinkedIn Campaign Manager |

### 90-Day Dashboard

After 90 days, add:

| Metric | How to Track |
|---|---|
| Stage conversion rates | HubSpot funnel report |
| Pipeline per $ spent | Calculated field |
| Average days per stage | Custom property + calculation |
| Persona breakdown | Campaign naming + HubSpot |
| Creative performance | LinkedIn Campaign Manager |

### Mature Dashboard (6+ months)

Full suite:

| Metric | How to Track |
|---|---|
| Multi-touch attribution | HubSpot attribution reports |
| LTV:CAC for ABM customers | CRM + finance data |
| Cohort analysis | Custom reports |
| Predictive scoring | HubSpot predictive lead scoring |
| Cross-channel attribution | Multi-source integration |

---

## Cross-References

- **Metric definitions and formulas:** See `abm-measurement-framework.md`
- **Troubleshooting dashboard issues:** See `abm-measurement-troubleshooting.md`
- **HubSpot property setup:** See `account-selection-framework.md`
- **LinkedIn campaign structure:** See `linkedin-ads-abm-guide.md`

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
